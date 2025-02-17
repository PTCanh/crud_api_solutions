+++
title = "Kiểm tra API của bạn"
date = 2025
weight = 3
chapter = false
pre = "<b>3. </b>"
+++

Để đảm bảo rằng API của bạn đang hoạt động, bạn sử dụng curl tương tác với nó.

#### Để lấy URL để gọi API của bạn:

1. Đăng nhập vào [bảng điều khiển API Gateway](https://ap-southeast-1.console.aws.amazon.com/apigateway/main/apis?api=unselected&region=ap-southeast-1).

2. Chọn **API** của bạn.

3. Ghi lại **URL gọi API** của bạn. Nó xuất hiện dưới **Invoke URL** trên trang **Details**.
![Test API](/images/crud-api-solutions/TestAPI.png?width=70pc)
4. Sao chép URL gọi API của bạn. URL đầy đủ trông giống như ```https://vp87s7rd3h.execute-api.ap-southeast-1.amazonaws.com/```

#### Để tạo hoặc cập nhật một mục:
+ Sử dụng lệnh sau để tạo hoặc cập nhật một mục. Lệnh này bao gồm một body yêu cầu với ID, giá, và tên của mục.

```json
curl -X "PUT" -H "Content-Type: application/json" -d "{\"id\": \"123\", \"price\": 12345, \"name\": \"myitem\"}" https://vp87s7rd3h.execute-api.ap-southeast-1.amazonaws.com/items
```

#### Để lấy tất cả các mục:
+ Sử dụng lệnh sau để liệt kê tất cả các mục.

```json
curl https://vp87s7rd3h.execute-api.ap-southeast-1.amazonaws.com/items
```

#### Để lấy một mục:
+ Sử dụng lệnh sau để lấy một mục theo ID của nó.

```json
curl https://vp87s7rd3h.execute-api.ap-southeast-1.amazonaws.com/items/123
```

#### Để xóa một mục:
+ Sử dụng lệnh sau để xóa một mục.

```json
curl -X "DELETE" https://vp87s7rd3h.execute-api.ap-southeast-1.amazonaws.com/items/123
```
#### Kết quả của các lệnh:
![Test API 2](/images/crud-api-solutions/TestAPI_2.png?width=70pc)