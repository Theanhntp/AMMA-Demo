# AMMA – Nền Tảng Tư Vấn Y Tế Thông Minh Tích Hợp AI

<p align="center">
  <img src="/IMG/logo.png" alt="MediAI Logo" width="200" />
</p>

**AMMA** là một hệ thống hỗ trợ tư vấn sức khỏe và quản lý khám bệnh thông minh, tích hợp AI sử dụng công nghệ **Prompt Engineering** trên nền tảng Coze. Dự án giúp người dùng đánh giá triệu chứng, kết nối với bác sĩ, lưu trữ hồ sơ y tế và cung cấp kiến thức sức khỏe một cách trực quan.

---

## 🎯 DEMO TẠI
<p align="center">
  https://theanhntp.github.io/AMMA-Demo/
</p>
<p align="center">
  #lưu ý đây chỉ là trang HTML tĩnh#
</p>
---

## 🎯 Mục Tiêu Hệ Thống

- 🚀 **Tự đánh giá sức khỏe**: Hỗ trợ người dùng tra cứu và tự đánh giá tình trạng sức khỏe ban đầu.
- 🤖 **Tư vấn AI hiệu quả**: Sử dụng công nghệ Prompt Engineering trên Coze để phân tích triệu chứng.
- 📅 **Quản lý khám bệnh**: Hỗ trợ quản lý lịch khám, bác sĩ, bệnh án và ảnh y tế.
- 💬 **Kết nối trực quan**: Tạo nền tảng giao tiếp thân thiện giữa bệnh nhân và bác sĩ.

---

## 🔧 Chức Năng Chính

### 👤 Đối Với Người Dùng
- Đăng ký, đăng nhập với xác thực **JWT**.
- Tư vấn sức khỏe qua **AI chatbot**.
- Phân tích triệu chứng thông qua bảng hỏi thông minh.
- Tải lên ảnh xét nghiệm để phân tích sơ bộ.
- Đặt lịch hẹn với bác sĩ.
- Xem lịch sử khám và kết quả.
- Đọc bài viết blog về y tế.

### 🩺 Đối Với Bác Sĩ
- Cập nhật thông tin cá nhân.
- Quản lý lịch hẹn khám.
- Xem triệu chứng và ảnh xét nghiệm từ bệnh nhân.
- Gửi kết quả khám và tư vấn.
- Viết bài chia sẻ chuyên môn.

### ⚙️ Đối Với Quản Trị Viên
- Quản lý người dùng, bác sĩ và bài viết.
- Theo dõi lịch sử khám và hoạt động hệ thống.
- Duyệt/phê duyệt nội dung blog.

<p align="center">
  <img src="/IMG/Usecase.png" alt="Use Case Diagram" width="800" />
  <br><i>Sơ đồ Use Case mô tả các chức năng chính theo vai trò người dùng</i>
</p>

<p align="center">
  <img src="/IMG/Chatbot.png" alt="AI Chatbot" width="400" />
  <br><i>AI Chatbot hỗ trợ tư vấn sức khỏe</i>
</p>

---

## 🧠 Luồng Nghiệp Vụ Tổng Quát

1. **Đăng ký/Đăng nhập**: Người dùng tạo tài khoản hoặc đăng nhập.
2. **Tra cứu triệu chứng**: Sử dụng chatbot AI hoặc bảng hỏi.
3. **Tải ảnh xét nghiệm**: Upload ảnh để phân tích (nếu cần).
4. **Đặt lịch khám**: Chọn bác sĩ và thời gian phù hợp.
5. **Bác sĩ tư vấn**: Xác nhận lịch hẹn và gửi kết quả.
6. **Nhận kết quả**: Người dùng xem kết quả khám.
7. **Lưu trữ lịch sử**: Cập nhật và lưu trữ hồ sơ khám.
8. **Tra cứu kiến thức**: Đọc các bài viết y tế trên blog.

---

## 🧩 Kiến Trúc Hệ Thống

| **Thành Phần**         | **Công Nghệ**                     |
|-------------------------|-----------------------------------|
| **Frontend**           | React + Vite + SCSS              |
| **Backend**            | Node.js + Express + TypeScript   |
| **Database**           | MongoDB                          |
| **Cloud Storage**      | Firebase (cho ảnh xét nghiệm)    |
| **AI Tư Vấn**          | Prompt Engineering trên Coze     |

---

## 📸 Chụp Màn Hình Giao Diện

Dưới đây là một số hình ảnh chụp màn hình minh họa giao diện của MediAI:

| **Tính Năng**            | **Hình Ảnh**                                                                 |
|--------------------------|------------------------------------------------------------------------------|
| **Giao diện chính**      | <img src="/IMG/Main-menu.png" alt="Main Interface" width="300" /> |
| **Đặt lịch khám**        | <img src="/IMG/BookingAppointment.png" alt="Booking Appointment" width="300" /> |
| **Đặt lịch bác sĩ**      | <img src="/IMG/DoctorBooking.png" alt="Doctor Appointment" width="300" /> |
| **Cập nhật hồ sơ**            | <img src="/IMG/Updateprofile.png" alt="Update Profile" width="300" /> |

---

## 📂 Cấu Trúc Thư Mục

### Client
```
client/
├── src/
│   ├── Pages/        # Các trang chính: Chat, Doctor, Blog, v.v.
│   ├── components/   # Navbar, Button, Modal, v.v.
│   ├── services/     # Gọi API đến server
│   ├── utils/        # Hàm tiện ích
│   └── styles/       # SCSS toàn cục
├── public/
└── .env
```

### Server
```
server/
├── src/
│   ├── controllers/  # Logic xử lý API
│   ├── routes/       # Định tuyến API
│   ├── models/       # Mongoose Schema
│   ├── middleware/   # Xác thực, xử lý lỗi, upload
│   ├── services/     # Firebase, AI, logic đặc thù
│   └── config/       # Cấu hình DB, Firebase, JWT
├── firebase-service-account.json
└── .env
```

---

## 🚀 Hướng Dẫn Khởi Động

### 1. Frontend (Client)
```bash
cd client
npm install
npm run dev
```
- **Mặc định chạy tại**: `http://localhost:5173`

**Tạo file `.env`**:
```ini
VITE_FE_URL=http://localhost:5173
VITE_BE_URL=http://localhost:8080
```

### 2. Backend (Server)
```bash
cd server
yarn install
yarn dev
```

**Tạo file `.env`**:
```ini
EMAIL_USER=your_email
EMAIL_PASSWORD=your_password
JWT_SECRET=your_jwt_secret
REACT_APP_FE_URL=http://localhost:5173
REACT_APP_BE_URL=http://localhost:8080
```

**Lưu ý**: Thêm file `firebase-service-account.json` vào thư mục `server/` để sử dụng Firebase Storage cho ảnh xét nghiệm.

---

## 📝 Ghi Chú
- Đảm bảo cài đặt đầy đủ các phụ thuộc trước khi chạy.
- File `firebase-service-account.json` phải được cấu hình chính xác để lưu trữ ảnh xét nghiệm.
- Kiểm tra các biến môi trường trong file `.env` để đảm bảo kết nối đúng giữa client và server.

---

<p align="center">
  <strong>MediAI</strong> – Sức khỏe trong tầm tay bạn!
</p>
<p align="center">
  theanhntp@gmail.com
</p>
