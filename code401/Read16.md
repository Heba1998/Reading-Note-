# Spring Authentication


![img](https://prod-acb5.kxcdn.com/wp-content/uploads/2020/07/DaoAuthenticationProvider.png)



* ***Spring Security Architecture***

*Spring security is framework used for securing Spring applications. It stands between client and application and gives possibility of configuring what data and functionalities are exposed to which users.*

**Authentication***The main strategy interface for authentication is AuthenticationManager,* which has only one method:

```java
public interface AuthenticationManager {

  Authentication authenticate(Authentication authentication)
    throws AuthenticationException;
}
```

*An AuthenticationManager can do one of 3 things in its authenticate() method:*

1. Return an Authentication (normally with authenticated=true) if it can verify that the input represents a valid principal.

2. Throw an AuthenticationException if it believes that the input represents an invalid principal.

3. Return null if it cannot decide.

The most commonly used implementation of AuthenticationManager is ProviderManager, which delegates to a chain of AuthenticationProvider instances. An AuthenticationProvider is a bit like an AuthenticationManager, but it has an extra method to allow the caller to query whether it supports a given Authentication type:

```java
public interface AuthenticationProvider {

	Authentication authenticate(Authentication authentication)
			throws AuthenticationException;

	boolean supports(Class<?> authentication);
}
```


* ***Web Security***

![WebSecurity](https://raw.githubusercontent.com/spring-guides/top-spring-security-architecture/main/images/filters.png)

*Servlet Filters are used in the web layer of Spring Security. A single HTTP request client submits a request to the application, and the container determines which filters and servlets apply to it based on the path of the request URI. Filters create a chain, and the order in which they are applied is crucial, as a servlet can only handle one request at a time. If a filter wishes to handle the request directly, it can veto the remainder of the chain, and it can even change the request or response used by downstream filters and servlets. FilterChainProxy is the concrete kind of Spring Security, which is implemented as a single Filter in the chain. There are more filters within the single filter. Another layer of indirection in the security filter, DelegatingFilterProxy, which does not have to be a Spring @Bean, is generally deployed in the container as a DelegatingFilterProxy. There can be numerous filter chains, all of which are unknown to the container and are maintained by Spring Security in the same top-level FilterChainProxy.*


* ***Method Security***

*As well as support for securing web applications, Spring Security offers support for applying access rules to Java method executions. For Spring Security, this is just a different type of “protected resource”. For users, it means the access rules are declared using the same format of ConfigAttribute strings (for example, roles or expressions) but in a different place in your code. The first step is to enable method security.*


The first step is to enable method security :

```java
@EnableGlobalMethodSecurity(securedEnabled = true)
public class SampleSecureApplication {
}
```


then :

```java
public class MyService {

  @Secured("ROLE_USER")
  public String secure() {
    return "Hello Security";
  }

}

```




* ***Working with Threads***

* If you need access to the currently authenticated user in a web endpoint, you can use a method parameter in a @RequestMapping this annotations pulls the current Authentication out of the SecurityContext and calls the getPrincipal() method on it to yield the method parameter.

```java
public String foo(@AuthenticationPrincipal User user) {
  ... // do stuff with user
}
```