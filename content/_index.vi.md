+++
title = "Giải pháp CRUD API"
date = 2025
weight = 1
chapter = false
+++

# Xây Dựng API CRUD với AWS Lambda và DynamoDB

#### Tổng quan
Hướng dẫn này sẽ chỉ bạn cách tạo một API CRUD (Tạo, Đọc, Cập nhật, Xóa) không cần máy chủ bằng AWS Lambda và DynamoDB. Bạn sẽ sử dụng API Gateway để định tuyến các yêu cầu HTTP đến hàm Lambda, hàm này sẽ tương tác với bảng DynamoDB để lưu trữ dữ liệu. Các bước thực hiện bao gồm:

![Structure CRUD API](/images/crud-api-solutions/structure_crud_api.png?width=70pc)

#### Nội dung

1. [Giới thiệu](1-Introduction/)
2. [Các bước chuẩn bị)](2-Preparation/)
3. [Kiểm Tra API Của Bạn](3-Test-Your-API/)
4. [Dọn dẹp tài nguyên](4-Clean-Up-Resources/)