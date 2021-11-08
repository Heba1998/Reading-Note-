# GraphQL @connection

![](https://cdn-images-1.medium.com/max/1024/1*YD3ygZD30y8c4A6Md5XT_g.jpeg)

## AWS Amplify

* *It is a set of tools and services that can be used together or on their own, to help front-end web and mobile developers build scalable full stack applications*

**With Amplify, user can configure app backends and connect app in minutes, deploy static web apps in a few clicks, and easily manage app content outside the AWS console.**

## Add relationships between types:

![](https://acg-wordpress-content-production.s3.us-west-2.amazonaws.com/app/uploads/2020/12/1_Uxinsykys6_R_o-GDq2SaQ.jpeg)

* The `@connection` directive enables you to specify relationships between @model types. Currently, this supports one-to-one, one-to-many, and many-to-one relationships.

* **Has one:**
    * In the simplest case, you can define a one-to-one connection where a project has one team:


```java
    type Project @model {
  id: ID!
  name: String
  team: Team @connection
}

type Team @model {
  id: ID!
  name: String!
}
```

* **Has many:**
    * The following schema defines a Post that can have many comments:

```java
type Post @model {
  id: ID!
  title: String!
  comments: [Comment] @connection(keyName: "byPost", fields: ["id"])
}

type Comment @model
  @key(name: "byPost", fields: ["postID", "content"]) {
  id: ID!
  postID: ID!
  content: String!
}
```

* **Many-to-many connections:**
    * You can implement many to many using two 1-M @connections, an @key, and a joining @model. For example:


```java
type Post @model {
  id: ID!
  title: String!
  editors: [PostEditor] @connection(keyName: "byPost", fields: ["id"])
}
type PostEditor
  @model(queries: null)
  @key(name: "byPost", fields: ["postID", "editorID"])
  @key(name: "byEditor", fields: ["editorID", "postID"]) {
  id: ID!
  postID: ID!
  editorID: ID!
  post: Post! @connection(fields: ["postID"])
  editor: User! @connection(fields: ["editorID"])
}

type User @model {
  id: ID!
  username: String!
  posts: [PostEditor] @connection(keyName: "byEditor", fields: ["id"])
}
```
