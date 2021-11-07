# Serverless and Amplify

![](https://external-preview.redd.it/IDbFW1E81QtslJ-0E5Yzow-z0qzmFJ29SDzRyCy7vCw.jpg?auto=webp&s=dcb63851813b14cdd47c27c547291c5c34fe2807)

## What is Serverless?

*Serverless is a cloud computing execution model where the cloud provider dynamically manages the allocation and provisioning of servers. A serverless application runs in stateless compute containers that are event-triggered, ephemeral (may last for one invocation), and fully managed by the cloud provider. Pricing is based on the number of executions rather than pre-purchased compute capacity*

*Serverless applications are event-driven cloud-based systems where application development rely solely on a combination of third-party services, client-side logic and cloud-hosted remote procedure calls (Functions as a Service).*

## Traditional vs. Serverless Architecture:

![](https://cdn.hackernoon.com/hn-images/1*x_v5NRC3TTMt1MaYl1gMUg.jpeg)


* **Traditional:** *applications have run on servers which you had to patch, update, and continuously look after late nights and early mornings due to all the unimaginable errors that broke your production.*

* **Serveless:** *users are no longer need to worry about the underlying servers.beacuse they are not managed by users anymore and with management out of the picture the responsibility falls on the Cloud vendors.*


## AWS Amplify

* *AWS Amplify is a set of tools and services that can be used together or on their own, to help front-end web and mobile developers build scalable full stack applications, powered by AWS. With Amplify, you can configure app backends and connect your app in minutes, deploy static web apps in a few clicks, and easily manage app content outside the AWS console.*


## The GraphQL

![](https://cdn.netlify.com/f77989acee58aa60fe4f29f0cf0e751e3996d9c0/0f5ec/img/blog/graphql2.png)


* *The GraphQL Transform provides a simple to use abstraction that helps you quickly create backends for your web and mobile applications on AWS. With the GraphQL Transform, you define your application's data model using the GraphQL Schema Definition Language (SDL) and the library handles converting your SDL definition into a set of fully descriptive AWS CloudFormation templates that implement your data model.*

### Create a GraphQL API

1. `amplify init`
2. `amplify add api`
- Select GraphQL
- When asked if you have a schema, say No
- Select one of the default samples; you can change this later
- Choose to edit the schema and it will open the new schema.graphql in your editor
3. `amplify push`

## API Category Project Structure

*At a high level, the transform libraries take a schema defined in the GraphQL Schema Definition Language (SDL) and converts it into a set of AWS CloudFormation templates and other assets that are deployed as part of amplify push. The full set of assets uploaded can be found at amplify/backend/api/YOUR-API-NAME/build.*