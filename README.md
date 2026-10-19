# 📱 PharmaDesk Mobile - Smart Pharmacy Management & AI Assistant

![Kotlin](https://img.shields.io/badge/Kotlin-Android-purple?style=flat-square&logo=kotlin)
![Jetpack Compose](https://img.shields.io/badge/UI-Jetpack%20Compose-brightgreen?style=flat-square&logo=android)
![Architecture](https://img.shields.io/badge/Architecture-MVVM-blue?style=flat-square)
![Backend](https://img.shields.io/badge/Backend-NodeJS%20%7C%20Express-green?style=flat-square&logo=nodedotjs)
![Database](https://img.shields.io/badge/Database-MySQL%20%7C%20Room-orange?style=flat-square)
![AI Integration](https://img.shields.io/badge/AI-Gemini%20Assistant-blueviolet?style=flat-square)

**PharmaDesk Mobile** là ứng dụng di động hỗ trợ quản lý nhà thuốc toàn diện, kê đơn thuốc điện tử và chăm sóc khách hàng tự động với trợ lý dược sĩ AI 24/7. Được thiết kế hiện đại, giao diện mượt mà bằng **Jetpack Compose**, ứng dụng giúp tối ưu hóa quy trình từ đặt hàng, bán hàng, kiểm soát tồn kho cho đến tư vấn sức khỏe.

---

## 🌟 Tính Năng Cốt Lõi

### 🤖 1. Trợ Lý Dược Sĩ AI (Gemini Integrated) & Kê Đơn Thông Minh
- **Tư vấn AI 24/7:** Giải đáp thắc mắc người dùng tức thời về liều dùng, tác dụng phụ và cách chăm sóc sức khỏe.
- **Gợi ý đơn thuốc tự động:** Phân tích triệu chứng nhập vào và truy vấn danh mục thuốc phù hợp để đề xuất đơn mẫu cho dược sĩ/y sĩ.
- **Xuất đơn thuốc PDF:** Hỗ trợ render đơn thuốc/hóa đơn thành file PDF chuẩn hóa.

### 🛒 2. Đặt Hàng & Mua Sắm Dành Cho Khách Hàng
- **Danh mục & Chi tiết thuốc:** Hiển thị sản phẩm theo phân loại, quy cách, giá cả và hướng dẫn sử dụng.
- **Giỏ hàng & Thanh toán:** Cập nhật tổng tiền thời gian thực, quản lý giỏ hàng và đặt hàng trực tuyến.
- **Theo dõi đơn hàng:** Theo dõi trạng thái từng đơn hàng và xem lại lịch sử đơn hàng/hóa đơn.

### 💼 3. Bảng Quản Trị Dành Cho Admin / Dược Sĩ (Admin Dashboard)
- **Quản lý đơn hàng:** Tiếp nhận, duyệt đơn, hủy đơn hoặc xác nhận vận chuyển.
- **Quản lý kho thuốc & Sản phẩm:** Thêm, sửa, xóa danh mục sản phẩm, cảnh báo thuốc sắp hết hạn / sắp hết hàng.
- **Quản lý khách hàng & Bài viết:** Theo dõi thông tin người dùng và xuất bản bài báo tư vấn sức khỏe.
- **Chấm công tự động:** Ghi nhận ca làm việc và quản lý nhân sự nhà thuốc.

---

## 🏗️ Kiến Trúc Hệ Thống & Công Nghệ

Ứng dụng được thiết kế theo mô hình **MVVM (Model - View - ViewModel)** chuẩn Android Jetpack giúp tách biệt hoàn toàn UI và Logic nghiệp vụ:

### 📱 Android Frontend
- **Ngôn ngữ:** Kotlin
- **UI Framework:** Jetpack Compose (Declarative UI)
- **Architecture:** MVVM + Clean Architecture principles
- **Local Database:** Room Persistence Library (SQLite)
- **Networking:** Retrofit2 + OkHttp (REST API Calls)

### 🖥️ Backend & Database
- **Server:** Node.js (Express framework)
- **Database:** MySQL Server
- **AI Engine:** Google Gemini API

### 📂 Cấu trúc thư mục Android:

```text
DoAn/
└── src/
    └── main/
        └── java/com/pharmadesk/
            ├── data/
            │   ├── api/          # Retrofit Interfaces & REST Client
            │   ├── model/        # Data Models (Product, Order, User...)
            │   └── repository/   # Repository Pattern layer
            ├── viewmodel/        # ViewModels chứa Business Logic
            └── view/
                ├── screen/       # Các màn hình Compose (Home, Cart, Admin...)
                └── theme/        # Material Design 3 Theme & Colors
```

🚀 Hướng Dẫn Cài Đặt & Khởi Chạy
Yêu Cầu Hệ Thống
Android Studio: Jellyfish / Koala trở lên.

Android SDK: API Level 24+ (Android 7.0 trở lên).

Backend Environment: Node.js v18+ và MySQL Server.

Các Bước Thực Hiện
Clone Repository:

Bash
git clone [https://github.com/Tên_Account_Của_Bạn/pharmadesk-mobile.git](https://github.com/Tên_Account_Của_Bạn/pharmadesk-mobile.git)
cd pharmadesk-mobile
Cấu hình Backend Server:

Import file cơ sở dữ liệu pharmacy_db.sql vào MySQL.

Chạy server Node.js và cập nhật BASE_URL trong file RetrofitClient.kt:

Kotlin
private const val BASE_URL = "http://YOUR_IP_ADDRESS:3000/api/"
Chạy ứng dụng Android:

Mở project trong Android Studio.

Đồng bộ hóa Gradle dependencies (Sync Project with Gradle Files).

Chọn thiết bị giả lập (Emulator) hoặc máy thật và bấm Run 'app'.

📄 License
Dự án được phát hành dưới bản quyền MIT License.
