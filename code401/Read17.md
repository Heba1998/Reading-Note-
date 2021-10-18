# Spring Boot and OAuth2

![](https://innovationm.co/wp-content/uploads/2018/06/Oauth-architecture.png)

**steps to create sample app has Oauth with spring boot**


* simple: a very basic static app with just a home page and unconditional login via Spring Boot’s OAuth 2.0 configuration properties (if you visit the home page, you will be automatically redirected to GitHub).

* click: adds an explicit link that the user has to click to login.

* logout: adds a logout link as well for authenticated users.

* two-providers: adds a second login provider so the user can choose on the home page which one to use.

* custom-error: adds an error message for unauthenticated users, and a custom authentication based on GitHub’s API.



Securing the Application with GitHub and Spring Security To make the application secure, you can simply add Spring Security as a dependency. Since you’re wanting to do a "social" login (delegate to GitHub), you should include the Spring Security OAuth 2.0 Client starter:

```java
<dependency>
	<groupId>org.springframework.boot</groupId>
	<artifactId>spring-boot-starter-oauth2-client</artifactId>
</dependency>

```