+++
title = "Tạo một Tích hợp (Integration)"
date = 2025
weight = 5
chapter = false
pre = "<b>2.5. </b>"
+++

#### Tạo một Tích hợp (Integration)

Để kết nối một route với tài nguyên backend, bạn cần tạo một tích hợp. Trong ví dụ này, bạn sẽ thiết lập một tích hợp Lambda dùng chung cho tất cả các route trong API. Tích hợp này đảm bảo rằng các yêu cầu gửi đến sẽ được chuyển đến hàm Lambda để xử lý, trở thành trung tâm hoạt động của API.

1. Đăng nhập vào [Bảng điều khiển API Gateway](https://ap-southeast-1.console.aws.amazon.com/apigateway/main/apis?api=unselected&region=ap-southeast-1).
2. Chọn **APIs**
![Create Integration](/images/crud-api-solutions/CreateIntegration.png?width=70pc)
3. Chọn **Integrations**

4. Chọn **Manage integrations**, sau đó chọn **Create**
![Create Integration 2](/images/crud-api-solutions/CreateIntegration_2.png?width=70pc)
5. Tại **Attach this integration to a route**, chọn **a API route**.

6. Đối với **Integration type**, chọn **Lambda function**.

7. Đối với **Lambda function**, chọn tên hàm Lambda của bạn **http-crud-tutorial-function**

8. Chọn **Create**.
![Create Integration 3](/images/crud-api-solutions/CreateIntegration_3.png?width=70pc)