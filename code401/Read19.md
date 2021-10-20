# Using WebSocket to build an interactive web application


![](https://quarkus.io/guides/images/websocket-guide-architecture.png)


* WebSoecket is a protocol work differently from http.

**http depend on the rquest response cycle so the communication is one direction:**

* request.
*  response.




**when a user send a request, it open a connection with server known as hand shake.the server will open a connection and hold it. the connection will remain opened until someone close it.**


## **To create a “Hello, world” application that sends messages back and forth between a browser and a server:**

## Spring Initializr

1- Navigate to https://start.spring.io. This service pulls in all the dependencies you need for an application and does most of the setup for you.

2- Choose either Gradle or Maven and the language you want to use.

3- Click Dependencies and select Spring Web, Thymeleaf, and Spring Boot DevTools.

4- Click Generate.

5- Download the resulting ZIP file


* Adding Dependencies:

```java
dependencies {
implementation 'org.webjars:webjars-locator-core'
implementation 'org.webjars:sockjs-client:1.0.2'
implementation 'org.webjars:stomp-websocket:2.3.3'
implementation 'org.webjars:bootstrap:3.3.7'
implementation 'org.webjars:jquery:3.1.1-1'
}
```

## Create a Resource Representation Class


* The service will accept messages that contain a name in a STOMP message whose body is a JSON object.

* Upon receiving the message and extracting the name, the service will process it by creating a greeting and publishing that greeting on a separate queue to which the client is subscribed. The greeting will also be a JSON object.

* To model the message that carries the name, you can create a plain old Java object with a name property and a corresponding getName() method.




## Create a Message-handling Controller

example : 

 ```java
 @Controller
public class GreetingController {


  @MessageMapping("/hello")
  @SendTo("/topic/greetings")
  public Greeting greeting(HelloMessage message) throws Exception {
    Thread.sleep(1000); // simulated delay
    return new Greeting("Hello, " + HtmlUtils.htmlEscape(message.getName()) + "!");
  }

}
 ```

## Configure Spring for STOMP messaging


example : 

 ```java
 @Configuration
@EnableWebSocketMessageBroker
public class WebSocketConfig implements WebSocketMessageBrokerConfigurer {

  @Override
  public void configureMessageBroker(MessageBrokerRegistry config) {
    config.enableSimpleBroker("/topic");
    config.setApplicationDestinationPrefixes("/app");
  }

  @Override
  public void registerStompEndpoints(StompEndpointRegistry registry) {
    registry.addEndpoint("/gs-guide-websocket").withSockJS();
  }

 ```