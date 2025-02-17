+++
title = "Tạo một API HTTP"
date = 2025
weight = 3
chapter = false
pre = "<b>2.3. </b>"
+++

API HTTP cung cấp một điểm cuối HTTP cho hàm Lambda của bạn. Trong bước này, bạn sẽ tạo một API trống. Trong các bước tiếp theo, bạn sẽ cấu hình các route và tích hợp để kết nối API của bạn với hàm Lambda.

#### Tạo một API HTTP

1. Đăng nhập vào [Bảng điều khiển API Gateway](https://ap-southeast-1.console.aws.amazon.com/apigateway/main/apis?region=ap-southeast-1)

2. Chọn **Create API**, và sau đó đối với **HTTP API**, chọn **Build**.
![Create API Gateway](/images/crud-api-solutions/CreateAPIGateway.png?width=70pc)
3. Đối với **API name**, nhập **http-crud-tutorial-api-demo**.

4. Chọn **Next**.
![Create API Gateway 2](/images/crud-api-solutions/CreateAPIGateway_2.png?width=70pc)
5. Đối với **Configure routes**, chọn **Next** để bỏ qua việc tạo route. Bạn sẽ tạo các route sau.
![Create API Gateway 3](/images/crud-api-solutions/CreateAPIGateway_3.png?width=70pc)
6. Xem xét giai đoạn mà **API Gateway** tạo cho bạn, sau đó chọn **Next**
![Create API Gateway 4](/images/crud-api-solutions/CreateAPIGateway_4.png?width=70pc)
7. Chọn **Create**.
![Create API Gateway 5](/images/crud-api-solutions/CreateAPIGateway_5.png?width=70pc)
#### Tạo một API HTTP thành công:
![Create API Gateway 6](/images/crud-api-solutions/CreateAPIGateway_6.png?width=70pc)