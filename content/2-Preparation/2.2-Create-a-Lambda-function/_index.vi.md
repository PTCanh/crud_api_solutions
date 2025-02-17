+++
title = "Tạo hàm Lambda"
date = 2025
weight = 2
chapter = false
pre = "<b>2.2. </b>"
+++

Tạo một hàm Lambda để xử lý backend cho API, thực hiện các thao tác Tạo, Đọc, Cập nhật và Xóa (CRUD) trên DynamoDB. Hàm này sử dụng sự kiện từ API Gateway để xác định hành động phù hợp. Để đơn giản, hướng dẫn này sử dụng một hàm duy nhất, nhưng theo nguyên tắc tốt nhất, bạn nên tạo các hàm riêng cho từng route.

#### Tạo hàm Lambda:

+ Đăng nhập vào [Bảng điều khiển Lambda](https://ap-southeast-1.console.aws.amazon.com/lambda/home?region=ap-southeast-1#/begin)

1. Chọn **Create a function**
![Create Lamda](/images/crud-api-solutions/CreateLamda.png?width=70pc)
2. Đối với **Function name**, nhập **http-crud-tutorial-function**.

3. Đối với **Runtime**, chọn **Node.js** hoặc **Python phiên bản mới nhất** được hỗ trợ.
![Create Lamda 2](/images/crud-api-solutions/CreateLamda_2.png?width=70pc)
4. Dưới **Permissions**, chọn **Change default execution role**.
5. Chọn **Create a new role from AWS policy templates**.
6. Đối với **Role name**, nhập **http-crud-tutorial-role-demo**.
7. Đối với **Policy templates**, chọn **Simple microservice permissions**. Chính sách này cấp quyền cho hàm Lambda để tương tác với DynamoDB.
8. Chọn **Create function**.
![Create Lamda 3](/images/crud-api-solutions/CreateLamda_3.png?width=70pc)
![Create Lamda 4](/images/crud-api-solutions/CreateLamda_4.png?width=70pc)
9.  Mở hàm Lambda trong trình chỉnh sửa mã của bảng điều khiển, và thay thế nội dung hiện tại bằng mã sau. Chọn Deploy để cập nhật hàm của bạn.
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
#### Tạo thành công hàm Lambda
![Create Lamda 6](/images/crud-api-solutions/CreateLamda_6.png?width=70pc)