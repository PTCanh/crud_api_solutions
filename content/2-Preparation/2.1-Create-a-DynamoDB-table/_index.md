+++
title = "Create a DynamoDB table"
date = 2025
weight = 1
chapter = false
pre = "<b>2.1. </b>"
+++

Here’s how to create a DynamoDB table for storing data for your API, with each item having a unique ID that will be used as the partition key for the table.

#### To create a DynamoDB table:

1. [Open the DynamoDB Console](https://ap-southeast-1.console.aws.amazon.com/dynamodbv2/home?region=ap-southeast-1#service)
+ Select **Create table**.
![Create DynamoDB](/images/crud-api-solutions/CreateDynamoDB.png?width=70pc)
+ For **Table name**, enter **http-crud-tutorial-items**.

+ For **Partition key**, enter **id**.
![Create DynamoDB 2](/images/crud-api-solutions/CreateDynamoDB_2.png?width=70pc)
+ Select **Create table**.
![Create DynamoDB 3](/images/crud-api-solutions/CreateDynamoDB_3.png?width=70pc)
#### Successfully created a DynamoDB table:
![Create DynamoDB 4](/images/crud-api-solutions/CreateDynamoDB_4.png?width=70pc)