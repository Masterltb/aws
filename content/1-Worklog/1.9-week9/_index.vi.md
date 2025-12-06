---
title: "Nhật ký Tuần 9"
date: ""
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

### Mục tiêu Tuần 9

- **Khởi động song song:** Dựng khung cho **Program Service** và **Chat Service** bằng Java 25 và Spring Boot.
- **Thiết kế DB:** Thiết kế và triển khai schema cho cả hai service.
- **Triển khai logic ban đầu:** Xây dựng luồng Đánh giá & Gợi ý cho Program Service và áp dụng lớp bảo mật chung.

### Các công việc thực hiện trong tuần

| Ngày | Công việc                                                                                                                                                                                            | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo                                                    |
| ---- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | --------------------------------------------------------------------- |
| 2    | - **Program Service:** Khởi tạo dự án Spring Boot và thiết kế ERD cho `Programs`, `Quizzes`. <br>- **Chat Service:** Thiết kế ERD cho `ChatRooms`, `Messages`.                                        | 03/11/2025   | 03/11/2025      | <https://start.spring.io/>                                            |
| 3    | - **Program Service:** Triển khai logic `MeQuizController` để phân loại mức độ nghiện. <br>- **Chat Service:** Khởi tạo dự án Spring Boot và tạo các lớp Entity (`ChatRoom`, `Message`).              | 04/11/2025   | 04/11/2025      | —                                                                     |
| 4    | - **Program Service:** Seed dữ liệu `ProgramTemplates` và phát triển Engine Gợi ý. <br>- **Cơ sở dữ liệu:** Áp dụng schema cho cả hai service bằng Flyway.                                           | 05/11/2025   | 05/11/2025      | <https://flywaydb.org/>                                               |
| 5    | - **Program Service:** Xây dựng API Đăng ký Lộ trình (Enrollment). <br>- **Bảo mật chung:** Tích hợp JWT authentication filter có thể tái sử dụng cho cả hai service.                               | 06/11/2025   | 06/11/2025      | <https://spring.io/guides/gs/securing-web/>                           |
| 6    | - **Kiểm thử:** Dùng Postman để test luồng Đánh giá & Đăng ký của Program Service. <br>- **Rà soát:** Code review cấu trúc của cả hai project, đảm bảo tính nhất quán.                               | 07/11/2025   | 07/11/2025      | —                                                                     |

### Kết quả đạt được Tuần 9

- **Thiết lập thành công khung sườn cho cả hai service:** `Program Service` và `Chat Service`.
- **Hoàn thành triển khai Database Schema** cho cả hai service trên PostgreSQL, được quản lý bởi Flyway.
- **Program Service:** Hệ thống Đánh giá & Gợi ý đã hoạt động, cho phép phân loại và đề xuất lộ trình.
- **Bảo mật:** Lớp bảo mật JWT đã được tích hợp và sẵn sàng để bảo vệ các API trong tương lai.

**Bài học rút ra:**

- **Kiến trúc Microservices:** Hiểu được cách thiết lập và quản lý nhiều service trong cùng một hệ thống.
- **Quản lý Schema DB:** Sử dụng Flyway giúp việc quản lý và triển khai các thay đổi về cơ sở dữ liệu trở nên an toàn và tự động.
- **Tái sử dụng:** Thiết kế các thành phần chung (như lớp bảo mật) để có thể áp dụng cho nhiều service, tránh lặp code.
