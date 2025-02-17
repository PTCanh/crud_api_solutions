+++
title = "Tạo bảng DynamoDB"
date = 2025
weight = 1
chapter = false
pre = "<b>2.1. </b>"
+++

Bạn sẽ sử dụng một bảng DynamoDB để lưu trữ dữ liệu cho API của mình. Mỗi mục sẽ có một ID duy nhất, mà chúng ta sẽ sử dụng làm khóa phân vùng (partition key) cho bảng.

#### Để tạo một bảng DynamoDB:

1. Mở [bảng điều khiển DynamoDB](https://ap-southeast-1.console.aws.amazon.com/dynamodbv2/home?region=ap-southeast-1#service)
+ Chọn **Create table**.
![Create DynamoDB](/images/crud-api-solutions/CreateDynamoDB.png?width=70pc)
+ Đối với **Table name**, nhập **http-crud-tutorial-items**.

+ Đối với **Partition key**, nhập **id**.
![Create DynamoDB 2](/images/crud-api-solutions/CreateDynamoDB_2.png?width=70pc)
+ Chọn **Create table**.
![Create DynamoDB 3](/images/crud-api-solutions/CreateDynamoDB_3.png?width=70pc)
#### Tạo thành công một bảng DynamoDB:
![Create DynamoDB 4](/images/crud-api-solutions/CreateDynamoDB_4.png?width=70pc)