# Web App Security

## **Many to many relationships**

![](https://aspblogs.blob.core.windows.net/media/zeeshanhirani/WindowsLiveWriter/ManyToManyMappingsinEntityFrameWork_103F4/image_thumb.png)


* `@ManyToMany` *annotation can be used for specifying this type of relationships in Hibernate.*

* *simple Entity Relationship which is the many-to-many association between two entities employee and project:*

*both the Employee class and Project classes refer to one another, which means that the association between them is bidirectional.*

    * employee can be assigned to multiple projects
    * project may have multiple employees working for it
    * many-to-many association between the two.



**In order to map a many-to-many association, we use the `@ManyToMany`, `@JoinTable` and `@JoinColumn` annotations.**

The `@ManyToMany` annotation is used in both classes to create the many-to-many relationship between the entities.

This association has two sides i.e. the owning side and the inverse side.

The `@JoinColumn` annotation is used to specify the join/linking column with the main table.

## **The Model Classes**

* The model classes Employee and Project need to be created with JPA annotations:

```java

@Entity
@Table(name = "Employee")
public class Employee {

    @ManyToMany(cascade = { CascadeType.ALL })
    @JoinTable(
        name = "Employee_Project",
        joinColumns = { @JoinColumn(name = "employee_id") },
        inverseJoinColumns = { @JoinColumn(name = "project_id") }
    )
    Set<Project> projects = new HashSet<>();

}
```

```java
 @Entity
 @Table(name = "Project")
 public class Project {    

 @ManyToMany(mappedBy = "projects")
  private Set<Employee> employees = new HashSet<>();
 
 }     
```