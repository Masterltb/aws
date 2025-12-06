# Tài Liệu API

Đây là tài liệu mô tả các API của project.

## Mục Lục
1.  [Authentication](#authentication)
2.  [Chat Rooms](#chat-rooms)
3.  [Files](#files)
4.  [Internal Tools (Dev)](#internal-tools-dev)

---

## 1. Authentication

Không có endpoint đăng nhập/đăng ký trực tiếp. Thay vào đó, hệ thống sử dụng JWT (JSON Web Token) để xác thực. Token phải được gửi kèm trong header `Authorization` của mỗi request yêu cầu xác thực.

**Định dạng Header:**
`Authorization: Bearer <your_jwt_token>`

Để lấy token cho mục đích thử nghiệm ở môi trường `dev`, hãy sử dụng endpoint trong mục [Internal Tools (Dev)](#internal-tools-dev).

---

## 2. Chat Rooms

Controller quản lý các phòng chat và tin nhắn.

### 2.1 Lấy danh sách phòng chat của tôi

Lấy danh sách tất cả các phòng chat mà người dùng hiện tại là thành viên.

*   **Phương thức:** `GET`
*   **Endpoint:** `/api/v1/chat-rooms/me`
*   **Yêu cầu xác thực:** Có
*   **Response (200 OK):**
    *   **Content-Type:** `application/json`
    *   **Body:** `List<ChatRoomResponse>`
        ```json
        [
            {
                "id": "uuid-string-cua-phong-chat",
                "name": "Tên phòng chat",
                "participantIds": ["user-id-1", "user-id-2"]
            }
        ]
        ```

### 2.2 Lấy lịch sử tin nhắn của phòng chat

Lấy lịch sử tin nhắn trong một phòng chat cụ thể, có phân trang.

*   **Phương thức:** `GET`
*   **Endpoint:** `/api/v1/chat-rooms/{roomId}/messages`
*   **Yêu cầu xác thực:** Có
*   **Path Variable:**
    *   `roomId` (String): ID của phòng chat.
*   **Query Parameters (Phân trang):**
    *   `page` (int, optional, default: 0): Số trang.
    *   `size` (int, optional, default: 50): Số lượng tin nhắn trên mỗi trang.
    *   `sort` (string, optional, default: `timestamp,desc`): Thuộc tính và thứ tự sắp xếp.
*   **Response (200 OK):**
    *   **Content-Type:** `application/json`
    *   **Body:** `Page<MessageResponse>`
        ```json
        {
            "content": [
                {
                    "id": "uuid-string-cua-tin-nhan",
                    "roomId": "uuid-string-cua-phong-chat",
                    "senderId": "user-id-cua-nguoi-gui",
                    "content": "Nội dung tin nhắn",
                    "timestamp": "2023-10-27T10:00:00.000Z"
                }
            ],
            "pageable": { ... },
            "last": true,
            "totalPages": 1,
            "totalElements": 1,
            "size": 50,
            "number": 0,
            "sort": { ... },
            "first": true,
            "numberOfElements": 1,
            "empty": false
        }
        ```

### 2.3 Tạo phòng chat mới (Internal)

Tạo một phòng chat mới với các thành viên được chỉ định.

*   **Phương thức:** `POST`
*   **Endpoint:** `/internal/api/v1/chat-rooms`
*   **Yêu cầu xác thực:** Không (nhưng là API nội bộ)
*   **Request Body:**
    *   **Content-Type:** `application/json`
    *   **Body:** `CreateChatRoomRequest`
        ```json
        {
            "name": "Tên phòng chat mới",
            "participantIds": ["user-id-1", "user-id-2"]
        }
        ```
*   **Response (200 OK):**
    *   **Content-Type:** `application/json`
    *   **Body:** `ChatRoomResponse`
        ```json
        {
            "id": "uuid-string-moi-tao",
            "name": "Tên phòng chat mới",
            "participantIds": ["user-id-1", "user-id-2"]
        }
        ```

---

## 3. Files

Controller quản lý việc tải file lên server.

### 3.1 Tải file lên

Tải một file lên server. Server sẽ tự động phân loại file vào các thư mục `images`, `audio`, hoặc `documents` dựa trên `Content-Type`.

*   **Phương thức:** `POST`
*   **Endpoint:** `/api/v1/files/upload`
*   **Yêu cầu xác thực:** Không
*   **Request Body:**
    *   **Content-Type:** `multipart/form-data`
    *   **Form Data:**
        *   `file`: File cần tải lên.
*   **Response (200 OK):**
    *   **Content-Type:** `application/json`
    *   **Body:** `FileUploadResponse`
        ```json
        {
            "fileDownloadUri": "http://<server_address>/uploads/images/uuid-random.jpg",
            "metadata": {
                "originalFileName": "ten-file-goc.jpg",
                "size": 123456,
                "contentType": "image/jpeg"
            }
        }
        ```
*   **Responses Lỗi:**
    *   `400 Bad Request`: Nếu không có file nào được chọn hoặc loại file không được hỗ trợ.
    *   `500 Internal Server Error`: Nếu có lỗi xảy ra trong quá trình lưu file.

---

## 4. Internal Tools (Dev)

Các API này chỉ dành cho mục đích phát triển và thử nghiệm, chỉ hoạt động khi project chạy với profile `dev`.

### 4.1 Tạo Token Thử Nghiệm (Profile: dev)

Tạo một JWT token để sử dụng cho việc thử nghiệm các API yêu cầu xác thực.

*   **Phương thức:** `POST`
*   **Endpoint:** `/test/generate-token`
*   **Profile:** `dev`
*   **Request Body:**
    *   **Content-Type:** `application/json`
    *   **Body:** `TestTokenRequest`
        ```json
        {
            "userId": "my-test-user",
            "roles": ["USER", "ADMIN"]
        }
        ```
*   **Response (200 OK):**
    *   **Content-Type:** `application/json`
    *   **Body:** `TestTokenResponse`
        ```json
        {
            "accessToken": "your.generated.jwt.token"
        }
        ```

### 4.2 Tạo Token Nhanh cho User (Internal)

Tạo nhanh một JWT token cho một `userId` bất kỳ với danh sách quyền rỗng.

*   **Phương thức:** `GET`
*   **Endpoint:** `/internal/api/v1/gentoken/{userId}`
*   **Path Variable:**
    *   `userId` (String): User ID bạn muốn tạo token.
*   **Response (200 OK):**
    *   **Content-Type:** `application/json`
    *   **Body:**
        ```json
        {
            "token": "your.generated.jwt.token"
        }
        ```
