---
title: "Nhật ký Tuần 10"
date: ""
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

### Mục tiêu Tuần 10

- **Program Service:** Triển khai logic cốt lõi (Nhiệm vụ Hàng ngày, Theo dõi Chuỗi, Sự kiện Hút thuốc).
- **Chat Service:** Chuẩn bị lớp truy cập dữ liệu (Data Access Layer).

### Các công việc thực hiện trong tuần

| Ngày | Công việc                                                                                                                                                                                             | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo          |
| ---- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------ | --------------- | --------------------------- |
| 2    | - **Program Service:** Triển khai logic sinh ra 4 bước nhiệm vụ hàng ngày cho người dùng. <br>- **Chat Service:** Tạo các interface `ChatRoomRepository` và `MessageRepository`.                        | 10/11/2025   | 10/11/2025      | —                           |
| 3    | - **Program Service:** Xây dựng API đánh dấu hoàn thành bước và triển khai `StreakService`. <br>- **Chat Service:** Viết các truy vấn JPQL tùy chỉnh để tìm tin nhắn theo phòng chat có phân trang.     | 11/11/2025   | 11/11/2025      | —                           |
| 4    | - **Program Service:** Phát triển trigger "Sự kiện Hút thuốc" và logic "Soft Reset" (Trạng thái: PENDING_RECOVERY).                                                                                    | 12/11/2025   | 12/11/2025      | —                           |
| 5    | - **Program Service:** Triển khai logic khôi phục: gán "Bài Quiz Khôi phục" và xử lý kết quả (tối đa 3 lần).                                                                                            | 13/11/2025   | 13/11/2025      | —                           |
| 6    | - **Program Service:** Viết Unit Test cho `StreakService` và thực hiện kiểm thử tích hợp cho toàn bộ luồng.                                                                                             | 14/11/2025   | 14/11/2025      | <https://junit.org/junit5/> |

### Kết quả đạt được Tuần 10

- **Program Service:**
  - Engine **Nhiệm vụ Hàng ngày** và **Hệ thống Streak** đã hoạt động hoàn chỉnh.
  - **Cơ chế Khôi phục** xử lý thành công "Sự kiện Hút thuốc" một cách nhân văn.
- **Chat Service:**
  - Lớp **Truy cập Dữ liệu (Repository)** đã được định nghĩa và sẵn sàng để triển khai ở tuần tiếp theo.

**Bài học rút ra:**

- **Quản lý Trạng thái Phức tạp:** Xử lý các trạng thái của người dùng (Active, Pending Recovery) đòi hỏi một logic máy trạng thái (state machine) vững chắc.
- **Tập trung vào một Service:** Dành phần lớn thời gian cho một service phức tạp giúp đảm bảo chất lượng và tiến độ, trong khi vẫn có thể thực hiện các công việc chuẩn bị cho service khác.
- **JPQL cho Truy vấn Tùy chỉnh:** Sử dụng JPQL là một cách mạnh mẽ để viết các truy vấn phức tạp mà Spring Data JPA không tự động hỗ trợ.
