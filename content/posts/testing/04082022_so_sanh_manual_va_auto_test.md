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
- Cần thực hiện **exploratory testing**. Khi manual tester có kinh nghiệm trên sản phẩm thì có thể thực hiện các test case *"Khám phá"* và phát hiện ra nhiều bất thường của sản phẩm
- Đối với các dự án ngắn hạn, cần triển khai nhanh và không đòi hỏi nhiều kinh phí thì manual testing là lựa chọn phù hợp cho trường hợp này
- Đối với dự án tần suất thực hiện test thấp, khoảng 2-3 lần/năm thì không nên đầu tư vào automation testing (Ví dụ: dự án bảo trì phần mềm, dự án website nhanh, bản patch,...)

## 2. Kiểm thử tự động (Automation testing)

Kiểm thử tự động *là kiểm thử trong đó người kiểm thử phải viết cách kịch bản kiểm thử và sau đó sử dụng tool hỗ trợ để kiểm thử. Nhờ đó mà việc kiểm thử sẽ trở nên hiệu quả và ít tốn thời gian hơn.* Kiểm thử tự động giúp cho các kịch bản kiểm thử lặp đi lặp lại nhiều lần và hỗ trợ các task kiểm thử khác khó thực hiện bằng manual hay performance test.

**Điểm mạnh**

1. Sử dụng tool tự động giúp tìm kiếm nhiều lỗi hơn
2. Automation thực hiện test nhanh và hiệu quả 
3. Kết quả kiểm thử tự động chính xác
4. Phạm vi kiểm thử tự động rộng vì kiểm tra tự động không bỏ qua kiểm tra đơn vị nhỏ nhất
5. Automation thực hiện bằng phần mềm và tool, do đó nó hoạt động không mệt mỏi so với manual tester
6. Quá trình kiểm thử được ghi lại, điều đó giúp kịch bản kiểm thử được thực hiện nhiều lần và thực hiện trên nhiều nền tảng khác nhau

**Điểm yếu**

Ngoài các điểm mạnh nêu trên, kiểm thử tự động còn tồn tại một số điểm yếu như sau:

1. Chi phí cho các tool kiểm thử tốn kém, có thể làm tăng chi phí trong khâu kiểm thử dự án (ví dụ: network không ổn định, môi trường test không đảm bảo, mã nguồn sản phẩm thay đổi,...)
2. Nếu có một thay đổi nhỏ cũng làm mất thời gian để update lại kịch bản và các đoạn script kiểm thử
3. Tester cần phải có kiến thức lập trình để viết các script tự động kiểm thử

**Khi nào nên sử dụng automation testing**

Để sử dụng automation testing, chúng ta nên có chiến lược rõ ràng trong dự án để lựa chọn test case cho automation. Vì automation sẽ tốn nhiều thời gian để lên kịch bản, viết script, nguồn nhân lực thực hiện và chi phí cho các tool kiểm thử tự động. Qua đó, có thể cân nhắc những trường hợp nên sử dụng automation testing là: 

- Test case thường xuyên thực hiện, chẳng hạn như acceptance testing, regression testing,...Việc thực hiện automation testing cho các test case này giúp giảm thời gian cho QA khi thực hiện những test case lặp lại, qua đó họ có nhiều thời gian để đầu tư nghiên cứu thực hiện các test case khác.
- Test case cần thực hiện trên nhiều môi trường khác nhau.
- Phù hợp với các dự án lớn, dự án phát triển liên tục trong dài hạn.

## So sánh khác biệt chính giữa manual testing và automation testing

Bài viết đã trình bày những điểm mạnh cũng như điểm yếu của từng loại testing. Bảng so sánh dưới đây sẽ giúp người đọc có cái nhìn vắn tắt đặc điểm của 2 loại test này.

|Yếu tố| Manual testing| Automation testing|
|--|--|--|
|Chi phí thời gian|Tốn thời gian thực hiện kiểm thử|Thời gian kiểm thử được rút ngắn, đặc biệt có thể chạy daily tự động trên CI/CD, không cần người chạy |
|Độ tin cậy|Việc kiểm thử manual được thực hiện bởi hành động bởi con người, do đó dễ gặp lỗi do con người gây ra. Vì thế mà độ tin cậy chính xác thấp|Thực hiện bởi các công cụ và phần mềm tự động nên có độ tin cậy cao hơn| 
|Giao diện thay đổi|Thay đổi nhỏ về class, id,... không ảnh hưởng nhiều đến kịch bản test|Dễ bị ảnh hưởng bởi source code sản phẩm|
|Kiến thức lập trình|Không đòi hỏi phải có kiến thức lập trình|Phải có kiến thức lập trình để thực hiện test script|
|Kiểm thử khám phá|Dễ dàng triển khai kiểm thử khám phá|Không thể thực hiện kiểm thử khám phá|
|Thực thi song song|Khi dự án có nhiều môi trường thì số lượng QA sẽ tăng lên|Dễ dàng thực thi trên nhiều môi trường, không cần quá nhiều QA do có sự hỗ trợ của tool tự động|
|Áp dụng|Dự án nhỏ, thời gian thực hiện ngắn hay các test case không chạy thường xuyên|Dự án lớn, đòi hỏi test case phải chạy nhiều lần|

## Tóm tắt

Dựa vào định nghĩa, điểm mạnh và điểm yếu của manual testing và automation testing, có thể tóm tắt như sau:

- Manual testing là kiểm thử phần mềm trong đó kiểm thử được thực hiện bởi QA
- Đối với automation testing, người kiểm thử phải viết kịch bản bằng các tập lệnh, các đoạn script kiểm thử và có sự trợ giúp của các tool tự động kiểm thử
- Manual testing giúp có các nhìn trực quan và chính xác về ứng dụng
- Automation testing giúp tìm thấy nhiều lỗi hơn so với manual testing
- Manual testing cho kết quả ít tin cậy hơn do người test vẫn có thể mắc lỗi
- Automation testing làm tiêu tốn chi phí cho các tool kiểm thử, do đó làm gia tăng chi phí của dự án
- Manual testing tiêu tốn nhiều thời gian và nguồn nhân lực
- Automation testing cho tốc độ nhanh hơn, hiệu quả hơn so với manual testing
- Manual testing không yêu cầu người test phải biết ngôn ngữ lập trình
  
Qua các vấn đề được nêu trên, để tối ưu hóa chi phí và thời gian trong quá trình kiểm thử dự án, chúng ta không nên nghiêng quá nhiều vào phương pháp thủ công hoặc tự động. Vì vậy, cần có sự kết hợp linh hoạt giữa kiểm thử thủ công và kiểm thử tự động để có thể tạo ra một sản phẩm tốt nhất cho người dùng.

## Tài liệu tham khảo

- https://www.guru99.com/difference-automated-vs-manual-testing.html

