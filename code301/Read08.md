#  APIs
![img](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQUr8KKl8RZbmxRtTsGu3fk5_w-el-vGZNHmg&usqp=CAU)


## API Design Best Practices:



![img](https://miro.medium.com/max/2000/1*8EzUfS1wBhvgp2SP_dQhkQ.png)


* *What does REST stand for?*

`representational state transfer`

* *REST APIs are designed around a ____.*

`resources`

* *What is an identifer of a resource? Give an example.*

```
resource has an identifier, which is a URI that uniquely identifies that resource.

For example https://adventure-works.com/orders

```


* *What are the most common HTTP verbs?*

`GET, POST, PUT, PATCH, and DELETE.`


* *What should the URIs be based on?*

`resource URIs should be based on nouns and not verbs`

* *Give an example of a good URI.*

`https://adventure-works.com/orders`

* *What does it mean to have a ‘chatty’ web API? Is this a good or a bad thing?*

`Chatty API is one that requires consumer to make tremendous (subjective matter) amount of distinct API calls to get needed information about a resource. George Reese has defined chatty API as any API that requires consumer to do more than a single call to perform a single, common operation.SO That’s means the web APIs that expose a large number of small resources.And it’s a bad thing we should try to avoid chatty web APIs.`


* *What status code does a successful `GET` request return?*

`status 200`


* *What status code does an unsuccessful `GET` request return?*

`status 404`


* *What status code does a successful `POST` request return?*

`status 201`

* *What status code does a successful `DELETE` request return?*

`status 204`


