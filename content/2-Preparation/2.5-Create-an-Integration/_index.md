+++
title = "Create an Integration"
date = 2025
weight = 5
chapter = false
pre = "<b>2.5. </b>"
+++

#### Create an Integration

To connect a route to a backend resource, you need to create an integration. In this example, you’ll configure a Lambda integration that handles all API routes. This integration ensures incoming requests are routed to the Lambda function for processing, making it the core of your API.

1. Log in to the [API Gateway Console](https://ap-southeast-1.console.aws.amazon.com/apigateway/main/apis?api=unselected&region=ap-southeast-1).
2. Select **APIs**
![Create Integration](/images/crud-api-solutions/CreateIntegration.png?width=70pc)
3. Go to **Integrations**

4. Click **Manage integrations**, then select **Create**
![Create Integration 2](/images/crud-api-solutions/CreateIntegration_2.png?width=70pc)
5. At **Attach this integration to a route**, choose **a API route**.

6. For **Integration type**, choose **Lambda function**.

7. In **Lambda function**, choose the name of your Lambda function **http-crud-tutorial-function**

8. Click **Create**.
![Create Integration 3](/images/crud-api-solutions/CreateIntegration_3.png?width=70pc)