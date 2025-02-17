+++
title = "Assign Integrations to Routes"
date = 2025
weight = 6
chapter = false
pre = "<b>2.6. </b>"
+++

In this example, you’ll use the same Lambda integration for all routes. Once the integration is assigned to each route, the Lambda function will be invoked whenever a request is made to your API

#### Steps to Assign Integrations to Routes:

1. Log in to the [API Gateway Console](https://ap-southeast-1.console.aws.amazon.com/apigateway/main/apis?api=unselected&region=ap-southeast-1).

2. Select **your API**.

3. Choose **Routes** from the left menu.

4. Select **a route to assign the integration**.

5. Under **Choose an existing integration**, select the Lambda function ```http-crud-tutorial-function```.

6. Click **Attach integration**.
![Create Integration 4](/images/crud-api-solutions/CreateIntegration_4.png?width=70pc)
7. **Repeat steps 4-6 for all routes**
![Create Integration 5](/images/crud-api-solutions/CreateIntegration_5.png?width=70pc)