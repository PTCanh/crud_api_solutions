+++
title = "Tạo các Route"
date = 2025
weight = 4
chapter = false
pre = "<b>2.4. </b>"
+++

#### Tạo các Route
Routes là cách để gửi các yêu cầu API đến các tài nguyên backend. Một route bao gồm hai phần: phương thức HTTP và đường dẫn tài nguyên, ví dụ: GET /items. Đối với API ví dụ này, chúng ta tạo bốn route:

+ GET ```/items/{id}```
+ GET ```/items```
+ PUT ```/items```
+ DELETE ```/items/{id}```

#### Để tạo các route:

1. Đăng nhập vào [Bảng điều khiển API Gateway](https://ap-southeast-1.console.aws.amazon.com/apigateway/main/apis?api=unselected&region=ap-southeast-1)
2. Chọn **your API**
![Create Route](/images/crud-api-solutions/CreateRoute.png?width=70pc)
3. Chọn **Routes**

4. Chọn **Create**
![Create Route 2](/images/crud-api-solutions/CreateRoute_2.png?width=70pc)
5. Đối với **Method**, chọn **GET**.

6. Đối với **Path**, nhập ```/items/{id}```. Phần **{id}** ở cuối đường dẫn là một tham số đường dẫn mà API Gateway sẽ lấy từ đường dẫn yêu cầu khi một khách hàng gửi yêu cầu.

7. Chọn **Create**
![Create Route 3](/images/crud-api-solutions/CreateRoute_3.png?width=70pc)
8. Lặp lại các bước 4-7 đối với **GET /items, DELETE /items/{id}, và PUT /items**
![Create Route 4](/images/crud-api-solutions/CreateRoute_4.png?width=70pc)
