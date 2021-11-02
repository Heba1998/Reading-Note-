# Room

![](https://developer.android.com/codelabs/android-room-with-a-view-kotlin/img/8e4b761713e3a76b.png?hl=ru)

## Save data in a local database using Room 

* The Room persistence library provides an abstraction layer over SQLite to allow fluent database access while harnessing the full power of SQLite. In particular, Room provides the following benefits:

    * Compile-time verification of SQL queries.
    * Convenience annotations that minimize repetitive and error-prone boilerplate code.
    * Streamlined database migration paths.


* There are three major components in Room:

    * The `database class` that holds the database and serves as the main access point for the underlying connection to your app's persisted data.
    * `Data entities` that represent tables in your app's database.
    * `Data access objects (DAOs)` that provide methods that your app can use to query, update, insert, and delete data in the database.

**After you have defined the data entity, the DAO, and the database object, you can use the following code to create an instance of the database:**
```java
AppDatabase db = Room.databaseBuilder(getApplicationContext(),
        AppDatabase.class, "database-name").build();
```


## Defining data using Room entities

**define each Room entity as a class that is annotated with `@Entity`. A Room entity includes fields for each column in the corresponding table in the database, including one or more columns that comprise the primary key.**

```java
@Entity
public class User {
    @PrimaryKey
    public int id;

    public String firstName;
    public String lastName;
}

```

**By default, Room creates a column for each field that's defined in the entity. If an entity has fields that you don't want to persist, you can annotate them using `@Ignore`, as shown in the following code snippet:**

```java
@Entity
public class User {
    @PrimaryKey
    public int id;

    public String firstName;
    public String lastName;

    @Ignore
    Bitmap picture;
}

```


## Define relationships between objects

In Room, there are two ways to define and query a relationship between entities: you can model the relationship using either an intermediate data class with embedded objects, or a relational query method with a multimap return type.


**For example, you can define a `UserBook` data class to represent library users with specific books checked out, and define a query method to retrieve a list of `UserBook` instances from the database:**

```java
@Dao
public interface UserBookDao {
   @Query("SELECT user.name AS userName, book.name AS bookName " +
          "FROM user, book " +
          "WHERE user.id = book.user_id")
   public LiveData<List<UserBook>> loadUserAndBookNames();
}

public class UserBook {
    public String userName;
    public String bookName;
}


```

## Accessing data using Room DAOs

You can define each DAO as either an interface or an abstract class. For basic use cases, you should usually use an interface. In either case, you must always annotate your DAOs with `@Dao`. DAOs don't have properties, but they do define one or more methods for interacting with the data in your app's database.

**The following code is an example of a simple DAO that defines methods for inserting, deleting, and selecting User objects in a Room database:**

```java

@Dao
public interface UserDao {
    @Insert
    void insertAll(User... users);

    @Delete
    void delete(User user);

    @Query("SELECT * FROM user")
    List<User> getAll();
}

```