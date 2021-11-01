#  Intents, Activities, and SharedPreferences


![](https://static.javatpoint.com/kotlin/images/kotlin-android-explicit-intent.png)


## **Android Tasks and the Back Stack**


![](https://developer.android.com/images/fundamentals/diagram_backstack.png)

* The activities are arranged in a stack—the back stack—in the order in which each activity is opened. If the user presses the Back button, that new activity is finished and popped off the stack.

* When the user touches an icon in the app launcher, If no task exists for the app, then a new task is created and the "main" activity for that app opens as the root activity in the stack.

* When the current activity starts another, the new activity is pushed on the top of the stack and takes focus. When the user presses the Back button, the current activity is popped from the top of the stack and the previous activity resumes.

* While in the background, all the activities in the task are stopped, but the back stack for the task remains intact. A task can then return to the "foreground" so users can pick up where they left off.

* one activity in your app might be instantiated multiple times. As such, if the user navigates backward using the Back button, each instance of the activity is revealed in the order they were opened. you can modify this behavior if you do not want an activity to be instantiated more than once.


* **In this regard, the principal <activity> attributes you can use are:**
    * taskAffinity
    * launchMode
    * allowTaskReparenting
    * clearTaskOnLaunch
    * alwaysRetainTaskState
    * finishOnTaskLaunch


* **principal intent flags you can use are:**
    * FLAG_ACTIVITY_NEW_TASK
    * FLAG_ACTIVITY_CLEAR_TOP
    * FLAG_ACTIVITY_SINGLE_TOP




* **Handling affinities**

- affinity indicates which task an activity prefers to belong to.

-  By default, all the activities from the same app have an affinity for each other.

-  we can modify that, and activities in different apps can have the same affinity or activity in task can do different tasks.

-  The taskAffinity attribute takes unique string value

* **affinity comes into play in two circumstances**

- When the intent that launches an activity contains the `FLAG_ACTIVITY_NEW_TASK flag`.

- when activity has its `allowTaskReparenting` attribute true

* **Clearing the back stack**

- when user leave his system for a while, the system will clear all tasks except for root.

- when user back to system, only root is restored.

* **to modify this behaviour**

- alwaysRetainTaskState:

- clearTaskOnLaunch

- finishOnTaskLaunch

* **Starting a task**

- intent filter allow me to setup activity to be entry point.

- intent filter of this kind causes an icon and label for the activity to be displayed in the app launcher.

- Users must be able to leave a task and then come back to it later using activity launcher.

- singleTask" and "singleInstance", should be used only when the activity has an `ACTION_MAIN` and a `CATEGORY_LAUNCHER` filter.
- 

* Save key-value data

- SharedPreferences APIs is used to save **key - value** pairs.

-  **SharedPreferences** object points to a file containing key-value pairs and provides methods to read and write them.

-  SharedPreferences file is managed by the framework and can be private or shared.





* **Get a handle to shared preferences**

- to create or access shared preference, following method i should use:

  - `getSharedPreferences()`

    - Use it when i need multiple shared preference files identified by name.
    
  - `getPreferences()`

    - Use it from an Activity if i need to use only one shared preference file for the activity.

    - code:

```java
Context context = getActivity();
SharedPreferences sharedPref = context.getSharedPreferences(
        getString(R.string.preference_file_key), Context.MODE_PRIVATE);
```

* **Write to shared preferences**

- To write to a shared preferences file, create a `SharedPreferences.Editor`.

- to do so i must call `edit()` on `SharedPreferences`.

- Pass the keys and values with methods `putInt()` and `putString()`.

-  Then call `apply()` or `commit()` to save the changes.

```java
SharedPreferences sharedPref = getActivity().getPreferences(Context.MODE_PRIVATE);
SharedPreferences.Editor editor = sharedPref.edit();
editor.putInt(getString(R.string.saved_high_score_key), newHighScore);
editor.apply();
```

* **Read from shared preferences**

- call methods such as `getInt()` and `getString()` to read from shared preference.

```java
SharedPreferences sharedPref = getActivity().getPreferences(Context.MODE_PRIVATE);
int defaultValue = getResources().getInteger(R.integer.saved_high_score_default_key);
int highScore = sharedPref.getInt(getString(R.string.saved_high_score_key), defaultValue);
```
