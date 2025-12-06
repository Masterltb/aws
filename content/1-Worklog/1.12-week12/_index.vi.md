---
title: "Nhật ký Tuần 12"
date: ""
weight: 12
chapter: false
pre: " <b> 1.12. </b> "
---

### Mục tiêu Tuần 12

- **Đảm bảo chất lượng toàn hệ thống:** Thực hiện Unit & Integration Testing cho cả `Program Service` và `Chat Service`.
- **Tối ưu hóa hiệu năng:** Phân tích và tối ưu hóa các truy vấn PostgreSQL ở cả hai service.
- **Hoàn thiện & Bàn giao:** Hoàn tất tài liệu API và chuẩn bị bàn giao hệ thống.

### Các công việc thực hiện trong tuần

| Ngày | Công việc                                                                                                                                                                                                                           | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo                                           |
| ---- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ------------------------------------------------------------ |
| 2    | - **Program Service:** Viết Unit Test cho `StreakService` và `QuizService`. <br>- **Chat Service:** Viết Unit Test cho `ChatService` để kiểm tra logic lấy tin nhắn.                                                                 | 24/11/2025   | 24/11/2025      | <https://site.mockito.org/>                                  |
| 3    | - **Program Service:** Viết Integration Test cho luồng "Sự kiện hút thuốc -> Khôi phục". <br>- **Chat Service:** Viết Integration Test cho luồng "Lấy danh sách phòng chat -> Lấy lịch sử tin nhắn". | 25/11/2025   | 25/11/2025      | —                                                            |
| 4    | - **Tối ưu hóa:** Dùng `EXPLAIN ANALYZE` để phân tích và thêm index cho các bảng của cả hai service, đặc biệt là các cột khóa ngoại và cột dùng để sắp xếp.                                                                          | 26/11/2025   | 26/11/2025      | <https://www.postgresql.org/docs/current/using-explain.html> |
| 5    | - **Tài liệu:** Cập nhật `api-docs.md` với đầy đủ thông tin chi tiết cho tất cả các API của cả hai service. <br>- **Báo cáo:** Hoàn thiện báo cáo thực tập, mô tả kiến trúc microservices.                | 27/11/2025   | 27/11/2025      | <https://swagger.io/>                                        |
| 6    | - **Rà soát:** Dọn dẹp code, kiểm tra lại cấu hình và các biến môi trường. <br>- **Thuyết trình:** Chuẩn bị demo và trình bày kiến trúc tổng thể của cả hai service cho mentor.                                                       | 28/11/2025   | 28/11/2025      | —                                                            |

### Kết quả đạt được Tuần 12

- **Chất lượng hệ thống:** Cả hai service đều có độ bao phủ kiểm thử tốt, đảm bảo tính ổn định và đúng đắn của các luồng nghiệp vụ.
- **Tối ưu hiệu năng:** Hiệu suất truy vấn của cả hai service được cải thiện, sẵn sàng cho lượng tải thực tế.
- **Tài liệu hoàn chỉnh:** Bàn giao tài liệu API thống nhất và rõ ràng cho toàn bộ hệ thống.
- **Hoàn thành:** Xây dựng và bàn giao thành công một hệ thống backend microservices hoàn chỉnh.

**Tổng kết kỳ thực tập:**
Trong 4 tuần cuối, tôi đã thiết kế và triển khai một hệ thống microservices từ con số 0, bao gồm `Program Service` và `Chat Service`. Tôi đã áp dụng các nguyên tắc phát triển phần mềm chuyên nghiệp từ việc thiết kế, triển khai, kiểm thử, tối ưu hóa cho đến việc viết tài liệu, và đã chuyển đổi thành công các yêu cầu nghiệp vụ phức tạp thành một sản phẩm phần mềm hoạt động.
