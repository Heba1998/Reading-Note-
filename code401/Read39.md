# Kinesis

![](https://www.blazeclan.com/wp-content/uploads/2014/01/Setting-the-Stage-to-Design-a-Kinesis-Application-on-AWS-Cloud-%E2%80%93-The-High-Level-Architecture.png)

*The Analytics category enables you to collect analytics data for your App. The Analytics category comes with built-in support for Amazon Pinpoint and Amazon Kinesis (Kinesis support is currently only available in the Amplify JavaScript library).*

## Set up Analytics backend

* `amplify add analytics`



```java
? Select an Analytics provider (Use arrow keys)
    `Amazon Pinpoint`
? Provide your pinpoint resource name:
    `yourPinpointResourceName`
? Apps need authorization to send analytics events. Do you want to allow guests and unauthenticated users to send analytics events? (we recommend you allow this when getting started)
    `Yes`

```


* Add Analytics by adding these libraries into the dependencies block:

```java
dependencies {
    // Add these lines in `dependencies`
    implementation 'com.amplifyframework:aws-analytics-pinpoint:1.28.3'
    implementation 'com.amplifyframework:aws-auth-cognito:1.28.3'
}
```


* Add these line on onCreate() method in Main class:

```java
Amplify.addPlugin(new AWSCognitoAuthPlugin());
Amplify.addPlugin(new AWSPinpointAnalyticsPlugin(this));

```


## Record events


```java
AnalyticsEvent event = AnalyticsEvent.builder()
    .name("PasswordReset")
    .addProperty("Channel", "SMS")
    .addProperty("Successful", true)
    .addProperty("ProcessDuration", 792)
    .addProperty("UserAge", 120.3)
    .build();

Amplify.Analytics.recordEvent(event);
```


## View Analytics console

`amplify console analytics`
