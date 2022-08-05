---
title: So sánh manual và automation test
subtitle: Bài viết so sánh sự khác biệt giữa manual testing và automation testing 
description: Bài viết so sánh sự khác biệt giữa manual testing và automation testing 
date: 2022-08-04
slug: "so-sanh-manual-va-automation-test"
categories: ['testing']
tags: ['testing', 'auto test', 'manual test']
ruby: true
---

Trong những năm gần đây, automation testing phát triển mạnh mẽ. Các frameworks hỗ trợ cho việc phát triển automation testing như WebdriverIO, Cypress, TestCafe, Codeceptjs, JunitTest… đua nhau ra đời. Điều này có thể thấy rằng thị trường automation testing thật sự mở rộng. Nhiều dự án, nhiều công ty đầu tư một cách nghiêm túc cho automation testing. Điều này đặt ra một câu hỏi mà nhiều người quan tâm: *liệu rằng automation testing có thực sự thay thế được manual testing hay không?*

Để trả lời cho câu hỏi nêu trên, chúng ta sẽ đi so sánh sự khác biệt giữa manual testing và automation testing, điểm mạnh và điểm yếu của 2 phương pháp test này.

## 1. Kiểm thử thủ công (Manual testing)

Kiểm thử thủ công (manual testing) *là việc tiến hành kiểm thử phần mềm mà các test case được thực hiện thủ công bởi người kiểm thử (QA/QC/Tester) mà không sử dụng bất kì công cụ tự động nào hỗ trợ.*

Hiện nay, khi truy cập các trang tuyển dụng về mảng test như ITviec, Vietnamwork,..., bạn sẽ thấy nhu cầu tuyển dụng và QA, QC và Manual testing rất phổ biến với mức lương phong phú và đa dạng. Điều đó cũng cho thấy manual testing hiện nay đóng vai trò quan trọng trong việc kiểm thử phần mềm.

![Một góc tuyển dụng QA/QC của trang tuyển dụng ITviec](https://i.imgur.com/782q5TF.png "Một góc tuyển dụng QA/QC của trang tuyển dụng ITviec")

**Điểm mạnh**

1. Các lỗi về giao diện (UX/UI) được phát hiện nhanh, phản hồi sớm về cho bộ phận phát triển (developer)
2. Các thay đổi nhỏ về cấu trúc website (bao gồm id, class name,...), giao diện mobile app và api sẽ không ảnh hưởng đến quá trình kiểm thử
3. Đối với các dự án nhỏ, manual test giúp release sản phẩm trong một thời gian ngắn
4. Không yêu cầu người kiểm thử có kỹ năng về lập trình
5. Việc thực thi test case mô phỏng đúng hành vi người dùng cuối
6. Người kiểm thử có thể dùng phương pháp ad-hoc (adhoc test) một cách linh động

**Điểm yếu**

1. Tốn nhiều thời gian và nhân lực cho việc test
2. Có những bộ test case sẽ phải thực hiện lặp đi lặp lại mỗi lần release (ví dụ như gửi tiền tiết kiệm online khi phát triển ứng dụng ngân hàng số). Điều này dẫn đến việc release gặp nhiều khó khăn và trở ngại nếu bộ test case có số lượng quá lớn
3. Các vấn đề về lỗi của người kiểm thử (human error), ví dụ như quên thực hiện một thao tác nào đó trong kịch bản test, điều này có thể xảy ra dẫn đến kết quả kiểm thử không chính xác

**Khi nào nên sử dụng manual testing**

Dựa trên những thông tin về điểm mạnh và điểm yếu, chúng ta có thể đưa ra quyết định phù hợp khi nào sử dụng manual testing. Hiện nay, nhiều công ty về phần mềm đều đưa ra chiến lược thực hiện manual testing song song với automation testing. Qua đó có thể thấy manual testing được thực hiện khi: 

- Triển khai tính năng mới của sản phẩm nhưng không ảnh hưởng quá nhiều đến tính năng cũ. Do đó, manual testing vẫn được ưu tiên sử dụng hơn trong trường hợp này để thời gian release được đảm bảo

## 2. Kiểm thử tự động (Automation testing)
