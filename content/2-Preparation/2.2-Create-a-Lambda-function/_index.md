+++
title = "Create a Lambda Function"
date = 2025
weight = 2
chapter = false
pre = "<b>2.2. </b>"
+++

Create a Lambda function to handle the backend for your API, performing Create, Read, Update, and Delete (CRUD) operations on DynamoDB. The function uses events from API Gateway to determine the appropriate action. For simplicity, this guide uses a single function, though it’s best practice to create separate functions for each route.

#### Create a Lambda Function:

+ Log in to the [Lambda Console](https://ap-southeast-1.console.aws.amazon.com/lambda/home?region=ap-southeast-1#/begin)

1. Click **Create a function**
![Create Lamda](/images/crud-api-solutions/CreateLamda.png?width=70pc)
2. For **Function name**, enter **http-crud-tutorial-function**.

3. For **Runtime**, select the latest supported version of **Node.js** or **Python**.
![Create Lamda 2](/images/crud-api-solutions/CreateLamda_2.png?width=70pc)
4. Under **Permissions**, click **Change default execution role**.
5. Choose **Create a new role from AWS policy templates**.
6. For **Role name**, enter **http-crud-tutorial-role-demo**.
7. For **Policy templates**, select **Simple microservice permissions**. To grant the Lambda function access to DynamoDB.
8.  Click **Create function**.
![Create Lamda 3](/images/crud-api-solutions/CreateLamda_3.png?width=70pc)
![Create Lamda 4](/images/crud-api-solutions/CreateLamda_4.png?width=70pc)
9.  Open the function in the code editor, replace its contents with the code below, and click Deploy to update the function.
```json
import { DynamoDBClient } from "@aws-sdk/client-dynamodb";
import {
  DynamoDBDocumentClient,
  ScanCommand,
  PutCommand,
  GetCommand,
  DeleteCommand,
} from "@aws-sdk/lib-dynamodb";

const client = new DynamoDBClient({});

const dynamo = DynamoDBDocumentClient.from(client);

const tableName = "http-crud-tutorial-items";

export const handler = async (event, context) => {
  let body;
  let statusCode = 200;
  const headers = {
    "Content-Type": "application/json",
  };

  try {
    switch (event.routeKey) {
      case "DELETE /items/{id}":
        await dynamo.send(
          new DeleteCommand({
            TableName: tableName,
            Key: {
              id: event.pathParameters.id,
            },
          })
        );
        body = `Deleted item ${event.pathParameters.id}`;
        break;
      case "GET /items/{id}":
        body = await dynamo.send(
          new GetCommand({
            TableName: tableName,
            Key: {
              id: event.pathParameters.id,
            },
          })
        );
        body = body.Item;
        break;
      case "GET /items":
        body = await dynamo.send(
          new ScanCommand({ TableName: tableName })
        );
        body = body.Items;
        break;
      case "PUT /items":
        let requestJSON = JSON.parse(event.body);
        await dynamo.send(
          new PutCommand({
            TableName: tableName,
            Item: {
              id: requestJSON.id,
              price: requestJSON.price,
              name: requestJSON.name,
            },
          })
        );
        body = `Put item ${requestJSON.id}`;
        break;
      default:
        throw new Error(`Unsupported route: "${event.routeKey}"`);
    }
  } catch (err) {
    statusCode = 400;
    body = err.message;
  } finally {
    body = JSON.stringify(body);
  }

  return {
    statusCode,
    body,
    headers,
  };
};
```
![Create Lamda 5](/images/crud-api-solutions/CreateLamda_5.png?width=70pc)
#### Lambda Function Successfully Created
![Create Lamda 6](/images/crud-api-solutions/CreateLamda_6.png?width=70pc)