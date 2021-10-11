# Spring RESTful Routing & Static Files


* ***Spring Request Mapping***

*`@RequestMapping` is one of the most common annotation used in Spring Web applications. This annotation maps HTTP requests to handler methods of MVC and REST controllers.*

![img](https://i2.wp.com/springframework.guru/wp-content/uploads/2017/09/mvc.png?w=800&ssl=1)



* ***Accessing Data with JPA***

 *JPA Stands for Java Persistence API (JPA) JPA is an abbreviation that stands for Java Persistence API. It's a specification which is part of Java EE and defines an API for object-relational mappings and for managing persistent objects.*

![img](https://2.bp.blogspot.com/-EebmrWpAqO4/W9vzgI61vtI/AAAAAAAAEkw/Kb5YL-e8Ja8ENTWx445hvovrwTlpo3iGACLcBGAs/s1600/dataaccess_jpa_basic_flow.png)



* ***CrudRepository*** 


    * `save(…)` save an Iterable of entities. Here, we can pass multiple objects to save them in a batch.

    * `findOne(…)` get a single entity based on passed primary key value.

    * `findAll()` get an Iterable of all available entities in database.

    * `count()` return the count of total entities in a table.

    * `delete(…)` delete an entity based on the passed object.

    * `exists(…)` verify if an entity exists based on the passed primary key value.


