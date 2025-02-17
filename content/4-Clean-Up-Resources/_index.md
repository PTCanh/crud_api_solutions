+++
title = "Clean Up Resources"
date = 2025
weight = 4
chapter = false
pre = "<b>4. </b>"
+++

To avoid unnecessary costs, delete the resources you created during this exercise. The following steps will remove the HTTP API, Lambda function, and related resources.

### Delete the DynamoDB Table

1. Go to the [DynamoDB Console](https://ap-southeast-1.console.aws.amazon.com/dynamodbv2/home?region=ap-southeast-1#service).

+ Select your **table**.

+ Click **Delete**.
![Clean Up](/images/crud-api-solutions/CleanUp.png?width=70pc)
+ Confirm your choice by clicking **Delete**.
![Clean Up 2](/images/crud-api-solutions/CleanUp_2.png?width=70pc)
#### Delete the HTTP API

2. Log in to the [API Gateway Console](https://ap-southeast-1.console.aws.amazon.com/apigateway/main/apis?region=ap-southeast-1).

+ On the **APIs**, page, select your **API**.

+ Click **Delete**.
![Clean Up 3](/images/crud-api-solutions/CleanUp_3.png?width=70pc)
+ Confirm by selecting **Delete**.
![Clean Up 4](/images/crud-api-solutions/CleanUp_4.png?width=70pc)
#### Delete the Lambda Function
3. Go to the [Lambda Console](https://ap-southeast-1.console.aws.amazon.com/lambda/home?region=ap-southeast-1#/begin).

+ On the **Functions** page, select your **function**. Click **Actions**, then select **Delete**.
![Clean Up 5](/images/crud-api-solutions/CleanUp_5.png?width=70pc)
+ Confirm by selecting **Delete**.
![Clean Up 6](/images/crud-api-solutions/CleanUp_6.png?width=70pc)
#### Delete the Lambda Execution Role
4. Open the AWS IAM Console
+ Go to **Roles** and select the **Lambda role**, for example, **http-crud-tutorial-role**.

+ Click **Delete role**.
![Clean Up 7](/images/crud-api-solutions/CleanUp_7.png?width=70pc)
+ Confirm by selecting **delete**.
![Clean Up 8](/images/crud-api-solutions/CleanUp_8.png?width=70pc)
