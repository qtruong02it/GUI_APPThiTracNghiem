# GUI_APPThiTracNghiem

**Ứng dụng Java GUI Thi Trắc Nghiệm** dùng Java Swing và JDBC theo mô hình MVC. Cho phép:
- Đăng nhập người dùng, kiểm tra quyền
- Thi trắc nghiệm, chấm điểm, lưu kết quả
- Quản lý câu hỏi, đề thi (thêm/sửa/xóa)
- Xem lịch sử kết quả

---

## 📋 Mục lục
1. [Công nghệ sử dụng](#công-nghệ-sử-dụng)  
2. [Cài đặt](#cài-đặt)  
3. [Chạy ứng dụng](#chạy-ứng-dụng)  
4. [Cấu trúc dự án](#cấu-trúc-dự-án)  

---

## 💻 1. Công nghệ sử dụng
- **Ngôn ngữ:** Java (JDK ≥ 8)  
- **GUI:** Java Swing  
- **Cơ sở dữ liệu:** MySQL (hoặc SQL Server) via JDBC  
- **Kiến trúc:** MVC  

---

## 🔧 2.Cài đặt

1. Clone repo:
   ```bash
   git clone https://github.com/qtruong02it/GUI_APPThiTracNghiem.git
   cd GUI_APPThiTracNghiem/appthitracnghiem
   
2. Tạo database (MySQL):
   ```bash
   CREATE DATABASE quiz_app;
   
3. Cập nhật cấu hình kết nối ở JDBCHelper/JDBCUtil.java:
   ```bash
   url = "jdbc:mysql://localhost:3306/quiz_app";
   user = "root";
   pass = "yourpassword";

4. Chạy ứng dụng:
   
   Mở dự án trong IDE (IntelliJ/Eclipse/NetBeans) 
   -> Chạy src/Main/Main.java

## 📂 4. Cấu trúc dự án:

src/
├── DAO/        → lớp truy xuất DB: UserDAO, ExamDAO, ...
├── Model/      → Entity: User, Exam, Question, ...
├── View/       → GUI forms: LoginForm, ExamForm, ...
├── JDBCHelper/ → helper kết nối JDBC
└── Main/       → Main.java (entry point)
