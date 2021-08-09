#  CRUD
![img](https://www.dorusomcutean.com/wp-content/uploads/2020/03/crud.jpg)

## Status Codes Based On REST Methods:


![img](https://miro.medium.com/max/920/1*w_iicbG7L3xEQTArjHUS6g.jpeg)


* *In your own words, describe what each group of status code represents:*

1- 100’s =`the request has been received from the client and waiting for the server to comply.`
2- 200’s =`success request, tells the client that the request has been accepted.`
3- 300’s =`redirection, which means that the request that has been sent to the server is invalid.`
4- 400’s =`client error, invalid request.`
5- 500’s =`server errors`

* *What is a status code `202`?*

`202 Accepted, Often used for asynchronous processing. This code tells the client that the request was valid, but its processing will finish sometime in the future. The response body should include an URL to the finished resource with some information about when it will be available, or an URL to some monitoring endpoint that tells the client when the resource is available.`


* *What is a status code 308?*

`308 Permanent Redirect - This tells the client to use another URL to access the resource and not use the current URL anymore. It’s helpful when we have multiple endpoints for one resource, but don’t want to implement reading from all of them.`


* *What code would you use if an update didn’t return data to a client?*

`204 No Content`

* *What code would you use if a resource used to exist but no longer does?*

`410 Gone`

* *What is the `Forbidden` status code?*

`The client has authorized or doesn’t need to authorize itself, but still has no permissions to access the resource.`



## Build A REST API With Node.js, Express, & MongoDB - Quick : 


![img](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTyklqtY8IxT9icYd5mtoJ6otPnMI95oL8lBQ&usqp=CAU)



* *Why do we need to pull our MongoDB database string out of our server and put it into our .env?*


`To keep it secure`


* *What is middleware?*

`Middleware is software that provides common services and capabilities to applications outside of what’s offered by the operating system. Data management, application services, messaging, authentication, and API management are all commonly handled by middleware`

* *What does `app.use(express.json())` do?*

`express. json() is a method inbuilt in express to recognize the incoming Request Object as a JSON Object. This method is called as a middleware in your application using the code: app. … urlencoded() is a method inbuilt in express to recognize the incoming Request Object as strings or arrays`


* *What does the `/:id` mean in a route?*

`The Route ID is a number which uniquely identifies the route. The name or title of a route is NOT unique. So if you want to refer to a specific route to mention a problem in an email, you better provide the Route ID.`

* *What is the difference beween `PUT` and `PATCH`?*

`The main difference between the PUT and PATCH method is that the PUT method uses the request URI to supply a modified version of the requested resource which replaces the original version of the resource, whereas the PATCH method supplies a set of instructions to modify the resource`

* *How do you make a defalut value in a schema?*

`You can specify a default value for an item using the default keyword. When a data doesn’t have a corresponding value, the value of this keyword will be used instead to do the validation checks. This keyword is not mandatory and the value of this keyword can be anything.`

* *What does a `500` error status code mean?*

`The HyperText Transfer Protocol (HTTP) 500 Internal Server Error server error response code indicates that the server encountered an unexpected condition that prevented it from fulfilling the request. This error response is a generic “catch-all” response.`

* *What is the difference between a status `200` and a status `201`?*

`201 Created The most fitting for Create operations. This code should signal backend-side`

`200 OK - It’s the basic status code to tell the client everything went good. Since we don’t create endpoint accessible resource when creating an access token, we can use 200 as a status for that action.`