# Espresso

![](https://marvel-b1-cdn.bc0a.com/f00000000131077/www.perfecto.io/sites/perfecto/files/image/2019-06/espresso-logo.jpg)

## What is a Espresso?

*Espresso is an Android UI tests. Espresso tests state expectations, interactions, and assertions clearly without the distraction of boilerplate content, custom infrastructure, or messy implementation details getting in the way.*


* **Packages:**

    * `espresso-core` Contains core and basic View matchers, actions, and assertions. See Basics and Recipes.
    * `espresso-web` Contains resources for WebView support.
    * `espresso-idling-resource` Espresso's mechanism for synchronization with background jobs.
    * `espresso-contrib` External contributions that contain DatePicker, RecyclerView and Drawer actions, accessibility checks, and CountingIdlingResource.
    * `espresso-intents` Extension to validate and stub intents for hermetic testing.
    * `espresso-remote` Location of Espresso's multi-process functionality.



* **Create UI tests with Espresso Test Recorder**

The Espresso Test Recorder tool lets you create UI tests for your app without writing any test code. Test Recorder then takes the saved recording and automatically generates a corresponding UI test that you can run to test your app.


* **Record an Espresso test**

```
1. Click Run > Record Espresso Test.

2. In the Select Deployment Target window, choose the device on which you want to record the test.

3. Recorded interactions will appear in the main panel in the Record Your Test window, When you run the test, the Espresso test will try executing these actions in the same order.

```


* **Add assertions to verify UI elements**

```
1. Click Add Assertion.
2. To select a View element on which to create an assertion, click on the element in the screenshot or use the first drop-down menu in the Edit assertion box at the bottom of the window.
3. Select the assertion you want to use from the second drop-down menu in the Edit assertion box.
4. Click Save and Add Another to create another assertion or click Save Assertion to close the assertion panels.
```

* **Save a recording**
```
1. Click Complete Recording.
2. Use the Test class name text field if you want to change the suggested name. Click Save.
3. Android Studio shows the test class as selected in the Project window of the IDE.
```