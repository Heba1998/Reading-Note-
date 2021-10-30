# Android Fundamentals


![](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSZidWSMyBcx8Ucl8-tD-TE9zjoK4v1hv_EdA&usqp=CAU)


* **Android apps can be written using Kotlin, Java, and C++ languages.**

* **Each Android app lives in its own security sandbox, protected by the following Android security features:**
    * The Android operating system is a multi-user Linux system in which each app is a different user.
    * By default, the system assigns each app a unique Linux user ID (the ID is used only by the system and is unknown to the app). The system sets permissions for all the files in an app so that only the user ID assigned to that app can access them.
    * Each process has its own virtual machine (VM), so an app's code runs in isolation from other apps.
    * By default, every app runs in its own Linux process. The Android system starts the process when any of the app's components need to be executed, and then shuts down the process when it's no longer needed or when the system must recover memory for other apps.






## **App components**

![](https://androidframework.com/wp-content/uploads/2019/04/Screen-Shot-2019-04-27-at-8.37.48-PM-720x340.png)

**App components are the essential building blocks of an Android app. Each component is an entry point through which the system or a user can enter your app. Some components depend on others.**


* *There are four different types of app components:*
    * Activities: An activity is the entry point for interacting with the user. It represents a single screen with a user interface.

    * Services: is a general-purpose entry point for keeping an app running in the background for all kinds of reasons.
        * A service is a general-purpose entry point for keeping an app running in the background for all kinds of reasons. It is a component that runs in the background to perform long-running operations or to perform work for remote processes. A service does not provide a user interface.

    * Broadcast receivers: allowing the app to respond to system-wide broadcast announcements , is implemented as a subclass of BroadcastReceiver and each broadcast is delivered as an Intent object . 
         * A broadcast receiver is a component that enables the system to deliver events to the app outside of a regular user flow, allowing the app to respond to system-wide broadcast announcements. Because broadcast receivers are another well-defined entry into the app, the system can deliver broadcasts even to apps that aren't currently running.


    * Content providers: manages a shared set of app data that you can store in the file system, in a SQLite database, on the web, or on any other persistent storage location that your app can access , is implemented as a subclass of ContentProvider and must implement a standard set of APIs that enable other apps to perform transactions.


### The manifest file
* Before the Android system can start an app component, the system must know that the component exists by reading the app's manifest file, AndroidManifest.xml. Your app must declare all its components in this file, which must be at the root of the app project directory.


**manifest file can declare an activity as follows:**

```java
<?xml version="1.0" encoding="utf-8"?>
<manifest ... >
    <application android:icon="@drawable/app_icon.png" ... >
        <activity android:name="com.example.project.ExampleActivity"
                  android:label="@string/example_label" ... >
        </activity>
        ...
    </application>
</manifest>
```