+++
title = "Gán Tích hợp vào Các Route"
date = 2025
weight = 6
chapter = false
pre = "<b>2.6. </b>"
+++

Đối với API ví dụ này, bạn sử dụng cùng một tích hợp Lambda cho tất cả các route. Sau khi gán tích hợp cho tất cả các route của API, hàm Lambda của bạn sẽ được gọi khi một khách hàng gọi bất kỳ route nào của bạn.

#### Để gán tích hợp vào các route:

1. Đăng nhập vào [Bảng điều khiển API Gateway](https://ap-southeast-1.console.aws.amazon.com/apigateway/main/apis?api=unselected&region=ap-southeast-1).

2. Chọn **API của bạn**.

3. Chọn **Integrations**.

4. Chọn **1 route**.

5. Dưới **Choose an existing integration**, chọn hàm Lambda ```http-crud-tutorial-function```.

6. Chọn **Attach integration**.
![Create Integration 4](/images/crud-api-solutions/CreateIntegration_4.png?width=70pc)
7. **Lặp lại các bước 4-6 cho tất cả các route**
![Create Integration 5](/images/crud-api-solutions/CreateIntegration_5.png?width=70pc)