---
title: "Nhật ký Tuần 11"
date: ""
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---

### Mục tiêu Tuần 11

- **Chat Service:** Triển khai các API cốt lõi (lấy phòng chat, lịch sử tin nhắn).
- **Program Service:** Tinh chỉnh logic nghiệp vụ (Slip/Relapse) và bổ sung các tính năng quản trị.

### Các công việc thực hiện trong tuần

| Ngày | Công việc                                                                                                                                                                                             | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo                              |
| ---- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------------- |
| 2    | - **Chat Service:** Triển khai `ChatController` và API `GET /api/v1/chat-rooms/me` để lấy danh sách phòng chat của người dùng.                                                                          | 17/11/2025   | 17/11/2025      | —                                               |
| 3    | - **Chat Service:** Triển khai API `GET /api/v1/chat-rooms/{roomId}/messages` với logic phân trang và sắp xếp. <br>- **Chat Service:** Triển khai API nội bộ `POST /internal/api/v1/chat-rooms`.       | 18/11/2025   | 18/11/2025      | —                                               |
| 4    | - **Program Service:** Triển khai logic phân biệt **Slip** (khôi phục ngay) và **Relapse** (hard reset). <br>- **Program Service:** Bổ sung Flyway để quản lý các thay đổi schema.                      | 19/11/2025   | 19/11/2025      | <https://flywaydb.org/>                         |
| 5    | - **Program Service:** Xây dựng Admin API (CRUD) cho `Quiz Templates`. <br>- **Program Service:** Tối ưu hóa logic bộ đếm reset (tối đa 3 lần khôi phục).                                               | 20/11/2025   | 20/11/2025      | —                                               |
| 6    | - **Program Service:** Phát triển bộ lập lịch `@Scheduled` cho Đánh giá Hàng tuần. <br>- **Kiểm thử:** Dùng Postman để test các API của Chat Service.                                                 | 21/11/2025   | 21/11/2025      | <https://spring.io/guides/gs/scheduling-tasks/> |

### Kết quả đạt được Tuần 11

- **Chat Service:**
  - Các API chính để lấy danh sách phòng chat và lịch sử tin nhắn đã hoạt động.
  - API nội bộ để tạo phòng chat đã sẵn sàng cho các service khác gọi.
- **Program Service:**
  - Logic **Slip vs Relapse** đã hoàn thiện, giúp hệ thống xử lý các tình huống thất bại một cách linh hoạt.
  - **Module Admin** cho phép quản lý nội dung Quiz một cách độc lập.
  - Hệ thống **Đánh giá Hàng tuần** được tự động hóa.

**Bài học rút ra:**

- **Thiết kế API Phân trang:** Tầm quan trọng của việc triển khai phân trang hiệu quả cho các API trả về danh sách lớn (lịch sử tin nhắn).
- **Lập lịch (Scheduling):** Sử dụng Spring Scheduler là một cách hiệu quả để chạy các công việc định kỳ mà không cần cấu hình phức tạp.
- **Phân bổ công việc:** Chuyển đổi trọng tâm giữa các service trong một sprint/tuần giúp duy trì tiến độ đồng đều cho toàn bộ hệ thống.
