# **Maps, primitives, File I/O**

## ***Java Primitives versus Objects***

![IMG](https://cdn.ttgtmedia.com/rms/onlineImages/server_side-java_primitive_types-f_mobile.png)


* *Java has a two-fold type system consisting of primitives such as int, boolean and reference types such as Integer, Boolean. Every primitive type corresponds to a reference type.*

* *The primitive type variables have the following impact on the memory:*

```
boolean – 1 bit.

byte – 8 bits.

short, char – 16 bits.

int, float – 32 bits.

long, double – 64 bits.
```

* **Performance**

*The performance of a Java code is quite a subtle issue, it depends very much on the hardware on which the code runs, on the compiler that might perform certain optimizations, on the state of the virtual machine, on the activity of other processes in the operating system.*



## ***Exceptions***

![IMG](https://static.javatpoint.com/core/images/types-of-exception-in-java.png)


* *An exception is an event, which occurs during the execution of a program, that disrupts the normal flow of the program's instructions.*

* *Three are Kinds of Exceptions:*
1- **checked exception:** like handling the un expect input from the users
2- **error:** if something wrong happened related to the hardware or system malfunction.
3- **runtime exception:** These usually indicate programming bugs, such as logic errors or improper use of an API

## ***Scanning***

![IMG](https://www.sitesbay.com/java/images/scanner-class-in-java.png)

* *Objects of type Scanner are useful for breaking down formatted input into tokens and translating individual tokens according to their data type.*

* *A simple text scanner which can parse primitive types and strings using regular expressions.*

```
Scanner myObj = new Scanner(System.in);  // Create a Scanner object
```
