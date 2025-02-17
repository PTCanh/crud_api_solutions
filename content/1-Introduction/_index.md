+++
title = "Introduction"
date = 2025-02-10
weight = 1
chapter = false
pre = "<b>1. </b>"
+++


#### AWS Lambda
**AWS Lambda** is a serverless computing service that lets you run code without managing servers. It is widely used for handling short tasks, such as data processing, API calls, or managing events.

**Advantages of using AWS Lambda**:

+ **No server management**: AWS automatically handles resource allocation and scaling.
+ **Event-driven execution**: Runs code in response to events, such as HTTP requests (when integrated with API Gateway) or changes in DynamoDB data.

**Pay-as-you-go**: You only pay for the execution time and number of requests.

**Application in CRUD API**: Lambda handles specific API functions like creating, reading, updating, and deleting resources.

#### Amazon DynamoDB
**DynamoDB** is a fully managed NoSQL database by AWS, designed for applications requiring high performance and scalable solutions.

**Advantages of using Amazon DynamoDB**:

+ **High performance**: Optimized to handle millions of requests per second with low latency.
+ **No infrastructure management**: DynamoDB automatically scales and backs up data.
+ **Seamless integration**: Works efficiently with AWS Lambda, API Gateway, and other AWS services.

**Application in CRUD API**: DynamoDB serves as the application’s data store. You perform create, read, update, and delete operations on data stored in DynamoDB tables.

#### AWS API Gateway
**API Gateway** is an AWS service that enables you to create, deploy, and manage RESTful or WebSocket APIs.
**Advantages of using API Gateway**:

+ **Seamless integration with Lambda**: Easily connects API Gateway with AWS Lambda to process requests.
+ **Security**: Supports API key management, rate limiting, and authentication (IAM, Lambda Authorizer).
+ **Multi-protocol support**: Includes REST, HTTP, and WebSocket.

**Application in CRUD API**: API Gateway acts as the entry point for the API, receiving HTTP requests (GET, POST, PUT, DELETE) and routing them to the appropriate Lambda functions for processing.

#### CRUD API Workflow Summary

+ The user sends an HTTP request to API Gateway.
+ API Gateway forwards the request to the corresponding Lambda function.
+ Lambda handles the logic and interacts with DynamoDB to perform operations on the data.
+ Lambda returns the result via API Gateway, which is sent back to the user.

This system is not only flexible but also cost-efficient due to its pay-as-you-go resource model.