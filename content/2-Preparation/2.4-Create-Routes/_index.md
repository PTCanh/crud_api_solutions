+++
title = "Create Routes"
date = 2025
weight = 4
chapter = false
pre = "<b>2.4. </b>"
+++

#### Create Routes
Routes define how API requests are sent to backend resources. A route consists of an HTTP method and a resource path, such as GET /items. For this example, we’ll create four routes.

+ GET ```/items/{id}```
+ GET ```/items```
+ PUT ```/items```
+ DELETE ```/items/{id}```

#### Steps to Create Routes

1. Login to the [API Gateway Console](https://ap-southeast-1.console.aws.amazon.com/apigateway/main/apis?api=unselected&region=ap-southeast-1)
2. Select **your API**
![Create Route](/images/crud-api-solutions/CreateRoute.png?width=70pc)
3. Go to **Routes**

4. Click **Create**
![Create Route 2](/images/crud-api-solutions/CreateRoute_2.png?width=70pc)
5. For **Method**, choose **GET**.

6. For **Path**, enter ```/items/{id}```. The **{id}** part is a path parameter that API Gateway will extract from the request URL.

7. Click **Create**
![Create Route 3](/images/crud-api-solutions/CreateRoute_3.png?width=70pc)
8. Repeat steps 4-7 for **GET /items, DELETE /items/{id}, and PUT /items**
![Create Route 4](/images/crud-api-solutions/CreateRoute_4.png?width=70pc)
