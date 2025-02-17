+++
title = "Dọn dẹp tài nguyên"
date = 2025
weight = 4
chapter = false
pre = "<b>4. </b>"
+++

Để tránh các chi phí không cần thiết, hãy xóa các tài nguyên mà bạn đã tạo trong quá trình bài tập bắt đầu này. Các bước sau đây sẽ xóa HTTP API, hàm Lambda và các tài nguyên liên quan.

### Để xóa bảng DynamoDB:

1. Mở [bảng điều khiển DynamoDB](https://ap-southeast-1.console.aws.amazon.com/dynamodbv2/home?region=ap-southeast-1#service).

+ Chọn bảng của bạn.

+ Chọn **Delete**.
![Clean Up](/images/crud-api-solutions/CleanUp.png?width=70pc)
+ Xác nhận lựa chọn của bạn và chọn **Delete**.
![Clean Up 2](/images/crud-api-solutions/CleanUp_2.png?width=70pc)
#### Để xóa một HTTP API:

2. Đăng nhập vào [bảng điều khiển API Gateway](https://ap-southeast-1.console.aws.amazon.com/apigateway/main/apis?region=ap-southeast-1).

+ Trên trang **APIs**, chọn một **API**. Chọn **Actions**, sau đó chọn **Delete**.

+ Chọn **Delete**.
![Clean Up 3](/images/crud-api-solutions/CleanUp_3.png?width=70pc)
+ Xác nhận và chọn **Delete**.
![Clean Up 4](/images/crud-api-solutions/CleanUp_4.png?width=70pc)
#### Để xóa một hàm Lambda:
3. Đăng nhập vào [bảng điều khiển Lambda](https://ap-southeast-1.console.aws.amazon.com/lambda/home?region=ap-southeast-1#/begin).

+ Trên trang **Functions**, chọn **function** của bạn. Chọn **Actions**, sau đó chọn **Delete**.
![Clean Up 5](/images/crud-api-solutions/CleanUp_5.png?width=70pc)
+ Xác nhận và chọn **Delete**.
![Clean Up 6](/images/crud-api-solutions/CleanUp_6.png?width=70pc)
#### Để xóa vai trò thực thi của hàm Lambda:
4.Mở bảng điều khiển AWS IAM
+ Mở trang **Roles** và chọn **Lambda role**, ví dụ, **http-crud-tutorial-role**.

+ Chọn **Delete role**.
![Clean Up 7](/images/crud-api-solutions/CleanUp_7.png?width=70pc)
+ Xác nhận và chọn **delete**.
![Clean Up 8](/images/crud-api-solutions/CleanUp_8.png?width=70pc)
