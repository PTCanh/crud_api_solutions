+++
title = "Giới thiệu"
date = 2025-02-10
weight = 1
chapter = false
pre = "<b>1. </b>"
+++


#### AWS Lambda
**AWS Lambda** là một dịch vụ điện toán không máy chủ (serverless), cho phép bạn chạy mã mà không cần quản lý máy chủ. Lambda được sử dụng phổ biến để thực hiện các tác vụ ngắn gọn, chẳng hạn như xử lý dữ liệu, gọi API, hoặc quản lý các sự kiện.

**Với việc sử dụng AWS Lambda, bạn sẽ có được những ưu điểm sau**:

+ **Không cần quản lý máy chủ**: AWS tự động quản lý việc phân bổ tài nguyên và điều chỉnh quy mô.
+ **Kích hoạt dựa trên sự kiện**: Chạy mã khi xảy ra sự kiện, chẳng hạn như yêu cầu HTTP (khi tích hợp với API Gateway), hoặc thay đổi dữ liệu trong DynamoDB.

**Thanh toán theo yêu cầu**: Chỉ trả tiền cho thời gian thực thi và số lượng yêu cầu.

**Ứng dụng trong CRUD API**: Lambda sẽ xử lý các chức năng cụ thể của API như tạo, đọc, cập nhật và xóa tài nguyên.

#### Amazon DynamoDB
**DynamoDB** là cơ sở dữ liệu NoSQL được quản lý hoàn toàn bởi AWS, thiết kế cho các ứng dụng yêu cầu hiệu năng cao và khả năng mở rộng linh hoạt.

**Với việc sử dụng AWS DynamoDB, bạn sẽ có được những ưu điểm sau**:

+ **Tốc độ cao**: Được tối ưu hóa để xử lý hàng triệu yêu cầu mỗi giây với độ trễ thấp.
+ **Không cần quản lý hạ tầng**: DynamoDB tự động mở rộng và sao lưu dữ liệu.
+ **Dễ dàng tích hợp**: Làm việc hiệu quả với AWS Lambda, API Gateway, và các dịch vụ AWS khác.

**Ứng dụng trong CRUD API**: DynamoDB sẽ lưu trữ dữ liệu của ứng dụng. Bạn sẽ thực hiện các thao tác thêm, sửa, xóa và truy vấn dữ liệu thông qua bảng DynamoDB.

#### AWS API Gateway
**API Gateway** là một dịch vụ AWS cho phép bạn tạo, triển khai, và quản lý các API RESTful hoặc WebSocket.
**Với việc sử dụng API Gateway, bạn sẽ có được những ưu điểm sau**:

+ **Tích hợp tốt với Lambda**: Dễ dàng kết nối API Gateway với AWS Lambda để xử lý yêu cầu.
+ **Bảo mật**: Hỗ trợ quản lý khóa API, giới hạn tốc độ, và xác thực (IAM, Lambda Authorizer).
+ **Hỗ trợ đa giao thức**: Bao gồm REST, HTTP, và WebSocket.

**Ứng dụng trong CRUD API**: API Gateway sẽ là điểm vào của API, nhận các yêu cầu HTTP (GET, POST, PUT, DELETE) và định tuyến chúng đến các hàm Lambda tương ứng để xử lý.

#### Tổng hợp luồng hoạt động CRUD API

+ Người dùng gửi yêu cầu HTTP đến API Gateway.
+ API Gateway chuyển yêu cầu đến hàm Lambda tương ứng.
+ Lambda xử lý logic và tương tác với DynamoDB để thực hiện các thao tác trên dữ liệu.
+ Lambda trả về kết quả thông qua API Gateway, gửi lại cho người dùng.

Hệ thống này không chỉ linh hoạt, mà còn tiết kiệm chi phí nhờ vào mô hình tính phí theo tài nguyên sử dụng.