---
title: Hướng dẫn cài đặt postman
subtitle: Bài viết hướng dẫn cài đặt postman 
description: Bài viết hướng dẫn cài đặt postman
date: 2022-03-05
slug: "huong-dan-cai-dat-postman"
categories: ['postman']
tags: ['postman', 'tutorial']
ruby: true
---

## 1. Postman là gì ?

Postman hiện là một trong những công cụ phổ biến nhất được sử dụng trong quá trình thử nghiệm các API. Được phát triển vào năm 2012 như một dự án phụ của Abhinav Asthana để đơn giản hóa quy trình làm việc API trong thử nghiệm và phát triển. API là viết tắt của Application Programming Interface (Giao diện lập trình ứng dụng) cho phép các ứng dụng phần mềm giao tiếp với nhau thông qua các lệnh gọi API.

## 2. Tại sao lại sử dụng postman 

Với hơn 10 triệu developer sử dụng hiện nay, Postman đã trở thành một công cụ không thể thiếu vì lý do như sau: 
1. Khả năng truy cập – Để sử dụng Postman, người dùng chỉ cần đăng nhập vào tài khoản của chính họ để dễ dàng truy cập tệp mọi lúc, mọi nơi miễn là ứng dụng Postman được cài đặt trên máy tính.
2. Sử dụng Collections (Bộ sưu tập) – Postman cho phép người dùng tạo bộ sưu tập cho các lệnh gọi API của họ. Mỗi bộ sưu tập có thể tạo các thư mục con và nhiều yêu cầu (request). Điều này giúp việc tổ chức các bộ thử nghiệm.
3. Cộng tác – Bộ sưu tập và môi trường có thể được nhập hoặc xuất giúp chia sẻ tệp dễ dàng. Liên kết trực tiếp cũng có thể được sử dụng để chia sẻ bộ sưu tập.
4. Tạo môi trường – Có nhiều môi trường hỗ trợ ít lặp lại các bài kiểm tra vì người dùng có thể sử dụng cùng một bộ sưu tập nhưng cho một môi trường khác. Đây là nơi tham số hóa sẽ diễn ra mà chúng ta sẽ thảo luận trong các bài học tiếp theo.
5. Tạo thử nghiệm – Các điểm kiểm tra thử nghiệm như xác minh trạng thái phản hồi HTTP thành công có thể được thêm vào mỗi lệnh gọi API giúp đảm bảo phạm vi kiểm tra.
6. Kiểm tra tự động hóa – Thông qua việc sử dụng Bộ sưu tập chạy hoặc Newman, các thử nghiệm có thể được chạy trong nhiều lần lặp lại tiết kiệm thời gian cho các thử nghiệm lặp đi lặp lại.
7. Gỡ lỗi – Bảng điều khiển Postman giúp kiểm tra dữ liệu nào đã được truy xuất giúp dễ dàng gỡ lỗi kiểm tra.
8. Tích hợp liên tục - Với khả năng hỗ trợ tích hợp liên tục, các hoạt động phát triển luôn được duy trì

![Thống kê số lượng developer sử dụng postman](https://i.imgur.com/YznTjAb.png)

*Thống kê số lượng developer sử dụng postman*

## 3. Cách download và cài đặt postman 

Là một công cụ mã nguồn mở, bạn có thể download và cài đặt theo các bước dưới đây: 
- **Bước 1:** Truy cập vào trang [https://www.postman.com/downloads/](https://www.postman.com/downloads/) và chọn nền tảng bạn muốn tải về như Mac, Window và Linux. Ở đây mình chọn nền tảng window 

![](https://i.imgur.com/bkpofNz.png)

- **Bước 2:** File tải về được hiển thị ở dưới cửa sổ trình duyệt. Khi quá trình tải về hoàn tất, bấm nút khởi động 
- **Bước 3:** Bấm nút next để bắt đầu cài đặt 
- **Bước 4:** Trong màn hình kế tiêp, đăng nhập với tài khoản Postman
- **Bước 5:** Chọn workspace (màn hình làm việc) và bâm nút **Save My Preferences**
- **Bước 6:** Hiển thị màn hình Startup

## Tóm tắt

- Postman là công cụ phổ biến nhất được sử dụng trong việc thử nghiêm API 
- Các tính năng thông dụng nhất trong Postman là khả năng truy cập, sử dụng bộ sưu tập (collection), cộng tác, tích hợp liên tục 
- Bạn nên tạo tài khoản khi sử dụng Postman, vì các collection được lưu sẵn và có sẵn trực tuyến 
- Bạn có thể tham số hóa Request
- Bạn có thể  tạo ra các bài test để kiểm tra các request trong postman 
