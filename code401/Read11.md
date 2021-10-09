# ***Spring***

## ***Serving Web Content with Spring MVC***

*A `Spring MVC` is a Java framework which is used to build web applications. It follows the Model-View-Controller design pattern. It implements all the basic features of a core spring framework like Inversion of Control, Dependency Injection.*

![IMG](https://cdn.crunchify.com/wp-content/uploads/2013/02/Simplest-Spring-MVC-tutorial-by-Crunchify.com_.png)



* ***Spring model attributes***

*The `@ModelAttribute` is an annotation that binds a method parameter or method return value to a named model attribute and then exposes it to a web view.*

```java
@ModelAttribute
public void addAttributes(Model model) {
    model.addAttribute("msg", "Welcome to My project 💛");
}
```

* ***Request parameters*** 

*the `@RequestParam` annotation is used to read the form data and bind it automatically to the parameter present in the provided method*


* ***Session attributes***

*The `@SessionAttributes` annotation is used to store the model attribute in the session*


* ***ServletContext attributes***
*The `ServletContext attributes` allows a servlet container to give the servlet additional information not already provided by this interface*

* ***Spring beans*** 

*When you create a bean definition, you create a recipe for creating actual instances of the class defined by that bean definition. The idea that a bean definition is a recipe is important, because it means that, as with a class, you can create many object instances from a single recipe.*

*You can control not only the various dependencies and configuration values that are to be plugged into an object that is created from a particular bean definition but also control the scope of the objects created from a particular bean definition. This approach is powerful and flexible, because you can choose the scope of the objects you create through configuration instead of having to bake in the scope of an object at the Java class level. Beans can be defined to be deployed in one of a number of scopes. The Spring Framework supports six scopes, four of which are available only if you use a web-aware ApplicationContext*


