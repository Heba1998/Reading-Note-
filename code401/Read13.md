# Related Resources and Integration Testing


* ***Relationships in Spring Data REST***

![img](https://miro.medium.com/max/1362/1*wAT6A6Cka5vKpTrm_rFzIw.png)


   1- `One-to-One Relationship` 

```
Define two entity classes Library and Address having a one-to-one relationship, using the @OneToOne annotation.
```
![](https://vertabelo.com/blog/one-to-one-relationship-in-database/1-to-1-pk-plus-fk.png)



2- `One-to-Many Relationship`

```
    where a record in one entity can be referenced by multiple records in another entity.
```

![](https://www.teach-ict.com/as_a2_ict_new/ocr/AS_G061/315_database_concepts/attributes_entities/miniweb/images/one2many.jpg)



3- `Many-to-Many Relationship` 

```
A many-to-many relationship occurs when multiple records in a table are associated with multiple records in another table. For example, a many-to-many relationship exists between customers and products: customers can purchase various products, and products can be purchased by many customers.
```

![](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcS4bkL_BqEZYjY3FIvDdIQz94clFluHHp23m34tWhXIsACmZKfNWgx_9D2lNRPX2Fs5Xv4&usqp=CAU)
    



* ***Integration Testing in Spring***

    * Verify View Name
    * Verify Response Body
    * Send GET Request With Path Variable
    * Send GET Request With Query Parameters
    * Send POST Request
