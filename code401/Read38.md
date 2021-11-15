## What is Amazon SNS?


![](https://techspawn.com/wp-content/uploads/2016/10/CLOUD.png)


Amazon Simple Notification Service

Pub/sub messaging for microservices and serverless applications.
Amazon SNS is a highly available, durable, secure, fully managed pub/sub messaging service that enables you to decouple microservices, distributed systems, and event-driven serverless applications. Amazon SNS provides topics for high-throughput, push-based, many-to-many messaging.

## Features and capabilities

**Amazon SNS provides the following features and capabilities:**

* Reliably deliver messages with durability
Amazon SNS uses cross availability zone message storage to provide high message durability. Amazon SNS reliably delivers messages to valid AWS endpoints, such as Amazon SQS queues and AWS Lambda functions.

* Simplify your architecture with Message Filtering
Amazon SNS helps you simplify your pub/sub messaging architecture by offloading the message filtering logic from your subscriber systems, and message routing logic from your publisher systems.

* Automatically scale your workload
Amazon SNS leverages the proven AWS cloud to dynamically scale with your application. Amazon SNS is a fully managed service, taking care of the heavy lifting related to capacity planning, provisioning, monitoring, and patching.

* Keep messages private and secure
Amazon SNS topic owners can set topic policies that restrict who can publish and subscribe to a topic. Amazon SNS also ensures that data is encrypted in transit and at rest, and provides VPC endpoints for message privacy.

## Related services

**You can use the following services with Amazon SNS:**

* `Amazon SQS` offers a secure, durable, and available hosted queue that lets you integrate and decouple distributed software systems and components.

* `AWS Lambda` enables you to build applications that respond quickly to new information. Run your application code in Lambda functions on highly available compute infrastructure.

* `AWS Identity and Access Management (IAM)` helps you securely control access to AWS resources for your users. Use IAM to control who can use your Amazon SNS topics (authentication), what topics they can use, and how they can use them (authorization).

* `AWS CloudFormation` enables you to model and set up your AWS resources. Create a template that describes the AWS resources that you want, including Amazon SNS topics and subscriptions. AWS CloudFormation takes care of provisioning and configuring those resources for you.



# Notifications

![](https://miro.medium.com/max/1200/1*SuBtEPb-V2g1eaIX7lxDOQ.png)

To create your Android platform application in Amazon SNS, you must have credentials from Firebase Cloud Messaging (FCM).

### Create a Firebase project on the Firebase website:

1. In the Firebase console, choose your project.

2. In the left navigation pane, choose the gear icon, and then choose Project settings.

3. Choose Cloud Messaging.

4. Under Project credentials, find the Server key. This your FCM project's API key. Copy it to your clipboard.

### Create a platform application in Amazon SNS

1.  Open the Amazon SNS console.

2.  In the left navigation pane, choose Mobile. Then, choose Push notifications.

3.  On the Mobile push notifications page, next to Platform applications, choose Create platform application.

4.  On the Create platform application page, under Details, do the following:
    For Application name, enter the name of your application.
    For Push notification platform, choose Firebase Cloud Messaging (FCM).
    Under Firebase Cloud Messaging Credentials, for API key, enter the server key that you copied earlier.

5.  (Optional) Set up event notifications and delivery status logging.

6.  Choose Create platform application.
