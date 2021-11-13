# Cognito

*The Amplify Auth category provides an interface for authenticating a user. Behind the scenes, it provides the necessary authorization to the other Amplify categories. It comes with default, built-in support for Amazon Cognito User Pool and Identity Pool. The Amplify CLI helps you to create and configure the auth category with an authentication provider.*

![](https://miro.medium.com/max/1838/1*5Lwi-RU4Sq1DYvKn91dukg.png)


**To start provisioning auth resources in the backend, go to your project directory and execute the command:**

###  `amplify add auth`

- Enter the following when prompted:

```bash
? Do you want to use the default authentication and security configuration?
    `Default configuration`
? How do you want users to be able to sign in?
    `Username`
? Do you want to configure advanced settings?
    `No, I am done.`
```

- To push your changes to the cloud, execute the command:

### `amplify push`

### Install Amplify Libraries

- Add the following dependency to your app‘s `build.gradle` along with others you added above in Prerequisites and click “Sync Now” when prompted:

```java
dependencies {
    implementation 'com.amplifyframework:aws-auth-cognito:1.17.4'
}
```

### Initialize Amplify Auth

- Add the Auth plugin before calling  **Amplify.configure**

```java
// Add this line, to include the Auth plugin.
Amplify.addPlugin(new AWSCognitoAuthPlugin());
Amplify.configure(getApplicationContext());
```

### Check the current auth session

- We can now check the current auth session.

- For testing purposes, you can run this from your MainActivity’s `onCreate` method.

```java
Amplify.Auth.fetchAuthSession(
    result -> Log.i("AmplifyQuickstart", result.toString()),
    error -> Log.e("AmplifyQuickstart", error.toString())
);
```

### Sign in

- The Auth category can be used to register a user, confirm attributes like email/phone, and sign in with optional multi-factor authentication. It is set up to use Amazon Cognito User Pools which manages the users and their properties.
