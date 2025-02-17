+++
title = "Test Your API"
date = 2025
weight = 3
chapter = false
pre = "<b>3. </b>"
+++

To ensure your API is working correctly curl commands to interact with it.

#### Steps to Retrieve the API URL

1. Log in to the [API Gateway Console](https://ap-southeast-1.console.aws.amazon.com/apigateway/main/apis?api=unselected&region=ap-southeast-1).

2. Select your API.

3. Note the URL gọi API của bạn. displayed on the Details page
![Test API](/images/crud-api-solutions/TestAPI.png?width=70pc)
4. Copy the full API Invoke URL. It should look like: ```https://vp87s7rd3h.execute-api.ap-southeast-1.amazonaws.com/```

#### Create or Update an Item:
+ Use the following command to create or update an item. This command sends a request body with an ID, price, and name

```json
curl -X "PUT" -H "Content-Type: application/json" -d "{\"id\": \"123\", \"price\": 12345, \"name\": \"myitem\"}" https://vp87s7rd3h.execute-api.ap-southeast-1.amazonaws.com/items
```

#### Retrieve All Items:
+ Use this command to list all items.

```json
curl https://vp87s7rd3h.execute-api.ap-southeast-1.amazonaws.com/items
```

#### Retrieve a Single Item by ID:
+ Use this command to get a specific item by its ID

```json
curl https://vp87s7rd3h.execute-api.ap-southeast-1.amazonaws.com/items/123
```

#### Delete an Item:
+ Use this command to delete an item by its ID

```json
curl -X "DELETE" https://vp87s7rd3h.execute-api.ap-southeast-1.amazonaws.com/items/123
```
#### The results:
![Test API 2](/images/crud-api-solutions/TestAPI_2.png?width=70pc)