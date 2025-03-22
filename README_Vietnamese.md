![image](https://github.com/user-attachments/assets/c9886c8a-109d-4ae5-bdad-8e75a9f377bd)

---

<div align="center">

# 🚨⚠️ CẢNH BÁO QUAN TRỌNG ⚠️🚨  
🚧 **Đây là một dự án website eCommerce có chủ đích để lộ lỗ hổng, được phát triển bởi cá nhân, KHÔNG liên quan tới bất kỳ tổ chức hay cá nhân nào khác.**  
🚧 **Chỉ dùng cho mục đích giáo dục**, dành cho sinh viên ngành **An toàn thông tin, Pentesting, Ethical Hacking**, v.v.  
🚧 **Để mở khóa quyền truy cập đầy đủ**, hãy kéo xuống cuối trang này để xem hướng dẫn.

---

# 🔒 CyberSam - Website eCommerce Lỗ Hổng  
Một **website eCommerce có chủ đích thiếu an toàn**, phục vụ cho việc học và thực hành.  
Dự án giúp **người yêu thích bảo mật**, **lập trình viên** và **sinh viên** hiểu rõ và rèn luyện các **lỗ hổng bảo mật web phổ biến** trong môi trường mua sắm trực tuyến.

</div>

---

## 🚀 Tính Năng Chính
✅ Mô phỏng nền tảng eCommerce cơ bản (người dùng, sản phẩm, đơn hàng, v.v.)  
✅ Cố tình tích hợp các lỗ hổng như:
- 💉 SQL Injection (SQLi)
- 🐞 Cross-Site Scripting (XSS)
- 🆔 Insecure Direct Object References (IDOR)
- 🔑 Broken Authentication
- 🕸️ Cross-Site Request Forgery (CSRF)
- 📂 Unrestricted File Upload
- ... và nhiều hơn nữa!

🎯 Phù hợp cho:
- Tham gia các cuộc thi Capture The Flag (CTF)  
- Thực hành kiểm thử xâm nhập (Pentesting)  
- Workshop và đào tạo bảo mật  

⚠️ **Chỉ dùng cho giáo dục và kiểm thử! Không sử dụng trong môi trường thật.**

---

## 🌐 Cấu Trúc Website

### 🛒 **Trang Người Dùng**
- **URL**: `http://localhost/Prototype/`  
- Mô phỏng một cửa hàng bán laptop trực tuyến với:
  - Khuyến mãi & Sản phẩm nổi bật  
  - Menu điều hướng:  
    `Tin tức`, `Giới thiệu`, `Sản phẩm`, `Cửa hàng địa phương`, `Tài khoản` (Đăng ký / Đăng nhập)  
- Các tính năng:  
  ✅ Duyệt và xem chi tiết sản phẩm  
  ✅ Thêm sản phẩm vào giỏ hàng  
  ✅ Đăng ký / Đăng nhập  
  ✅ Thanh toán và quản lý đơn hàng  

---

### 🔐 **Trang Quản Trị (Admin Panel)**
- **URL**: `localhost/Prototype/admin_area/`  
- Trang đăng nhập quản trị viên  
- Các tính năng:  
  ✅ Quản lý sản phẩm  
  ✅ Quản lý đơn hàng  
  ✅ Quản lý người dùng  
  ✅ Quản lý khuyến mãi / mã giảm giá

![image](https://github.com/user-attachments/assets/6d06aaaa-bcca-4747-82c5-b8373b96f4b0)

![image](https://github.com/user-attachments/assets/22b01471-4b45-4770-8d0f-f84eaff44145)

---

### 👤 **Tài Khoản Người Dùng**
- Chức năng đăng ký / đăng nhập  
- Các tính năng:  
  ✅ Xem sản phẩm và chi tiết  
  ✅ Thêm vào giỏ hàng và thanh toán  
  ✅ Theo dõi đơn hàng & vận chuyển  
  ✅ Nhận mã giảm giá và khuyến mãi  

![image](https://github.com/user-attachments/assets/a64efda6-a315-4d76-a502-847d6f0d3969)

---

## ⚠️ Tổng Quan Về Lỗ Hổng

CyberSam bao gồm **nhiều lỗ hổng web phổ biến** để người học có thể hiểu, khai thác và khắc phục trong môi trường an toàn.

| Lỗ hổng                        | Mô tả                                                        |
|-------------------------------|--------------------------------------------------------------|
| 🔍 **Directory Enumeration**    | Các thư mục nhạy cảm (`/admin_area/`, `/backup/`, `/uploads/`) có thể bị dò tìm bằng công cụ **Gobuster**, **Dirb** hoặc duyệt thủ công. |
| 🔑 **Brute Force Login**        | Không có bảo vệ chống brute force (không CAPTCHA, không khóa tài khoản). Có thể khai thác bằng **Hydra** hoặc **Burp Suite Intruder**. |
| 🗂️ **File Upload Vulnerability** | Không kiểm tra định dạng file đúng cách. Kẻ tấn công có thể upload shell `.php` để thực thi mã từ xa (RCE). |
| 🆔 **IDOR**                    | Thao tác tham số URL (`user_id=2`) để truy cập / chỉnh sửa dữ liệu người dùng khác. |
| 🐞 **Stored/DOM XSS**           | Không lọc dữ liệu đầu vào. Kẻ tấn công có thể chèn mã script đánh cắp cookie hoặc chiếm quyền tài khoản. |
| 💉 **SQL Injection (SQLi)**     | Truy vấn không an toàn cho phép truy xuất hoặc chỉnh sửa dữ liệu cơ sở dữ liệu. |

---

## 🔍 Dò Thư Mục (Directory Enumeration)
- **Mô tả**: Thư mục nhạy cảm như `/admin_area/`, `/backup/` và `/uploads/` dễ dàng truy cập công khai.
- **Nguy cơ**: Tin tặc có thể dò quét và khai thác bằng **Gobuster**, **Dirb**, hoặc duyệt tay.

![image](https://github.com/user-attachments/assets/510ec3e5-c4c0-41e7-8bf6-cd1d42da588b)

![image](https://github.com/user-attachments/assets/bd6a2b26-dce9-4d1a-838a-3c8efa442926)

---

## 🔑 Tấn Công Brute Force Đăng Nhập
- **Mô tả**: Trang đăng nhập quản trị viên không có bảo vệ brute force như CAPTCHA hay khóa tài khoản.
- **Nguy cơ**: Dễ dàng thực hiện tấn công brute force hoặc credential stuffing bằng **Hydra** hoặc **Burp Suite Intruder**.

![image](https://github.com/user-attachments/assets/96676bbd-8049-4586-bf00-fd9b917e09da)

---

## 🗂️ Lỗ Hổng Tải File
- **Mô tả**: Chức năng tải file không kiểm tra đúng định dạng file. Tin tặc có thể tải lên file độc hại như shell `.php`.
- **Nguy cơ**: Thực thi mã từ xa (RCE), chiếm quyền kiểm soát máy chủ.

![image](https://github.com/user-attachments/assets/a3ac57b2-cc8a-4b4d-be7d-55a0bf8abce0)

---

## 🆔 IDOR - Truy Xuất Trực Tiếp Đối Tượng Không An Toàn
- **Mô tả**: Người dùng có thể chỉnh tham số URL (ví dụ `user_id=2`) để truy cập / chỉnh sửa dữ liệu người khác.
- **Nguy cơ**: Truy cập trái phép thông tin người dùng và đơn hàng.

![image](https://github.com/user-attachments/assets/9ee6fd1f-619d-4a01-a53f-f7d289b65788)

---

## 🐞 Stored XSS / DOM XSS
- **Mô tả**: Ứng dụng không lọc dữ liệu nhập vào, dễ bị tấn công XSS tồn tại hoặc XSS DOM.
- **Nguy cơ**: Đánh cắp cookie phiên, chiếm tài khoản, cài mã độc.

![image](https://github.com/user-attachments/assets/55262042-4e81-43d6-922e-f5c382070a19)

![image](https://github.com/user-attachments/assets/651c6b46-8e2e-498f-b827-93b5313e887c)

---

## 💉🗄️  SQL Injection

![image](https://github.com/user-attachments/assets/6339b559-43ea-477f-903d-cecc5030f48b)

---

## 📦⚠️ Các Lỗ Hổng Khác

---

## 🛠️ Hướng Dẫn Cài Đặt Nhanh

### 1️⃣ Cài Đặt XAMPP  
👉 Tải và cài [XAMPP](https://www.apachefriends.org)  
👉 Khởi động **Apache** và **MySQL** từ Control Panel của XAMPP  

### 2️⃣ Tải Và Giải Nén Source Code  
👉 Giải nén thư mục dự án vào:  
```
C:\xampp\htdocs\
```  
👉 Ví dụ:  
```
C:\xampp\htdocs\cybersam
```

### 3️⃣ Import Cơ Sở Dữ Liệu  
👉 Truy cập `http://localhost/phpmyadmin`  
👉 Import file `database.sql` (đi kèm trong gói tải về)  
👉 CSDL sẽ được tạo tự động  

### 4️⃣ Truy Cập Website  
👉 Trang người dùng: `http://localhost/Prototype/`  
👉 Trang quản trị: `http://localhost/Prototype/admin_area/`

---

## 📝 Mẫu Yêu Cầu (Tùy Chọn)

<div align="center">

# 🚀🔥 CHỈ $10 ĐỂ MỞ KHÓA TOÀN BỘ 🔥🚀  
### (Database + Tài liệu lỗ hổng chi tiết)

<table>
<tr><td><strong>Họ và tên</strong></td><td>Điền họ tên đầy đủ</td></tr>
<tr><td><strong>Số điện thoại</strong></td><td>Số liên hệ</td></tr>
<tr><td><strong>Email</strong></td><td>Email của bạn</td></tr>
<tr><td><strong>Nội dung yêu cầu</strong></td><td>[Database] / [Tài liệu lỗ hổng] / [Cả hai]</td></tr>
<tr><td><strong>Ghi chú (nếu có)</strong></td><td>Yêu cầu đặc biệt nếu cần</td></tr>
</table>

</div>

---

## 📞 Liên Hệ

Nếu bạn muốn **trải nghiệm đầy đủ** nền tảng CyberSam, tôi có thể cung cấp:  
📂 **Toàn bộ cơ sở dữ liệu**  
📄 **Tài liệu chi tiết về các lỗ hổng bảo mật**  

👉 **Liên hệ trực tiếp với tôi:**  
- **Telegram**: [@mytelegram](https://t.me/redbeardos)  
- **Email**: phamphudong0112@gmail.com  

---

## 🌿 Lời Nhắn Nhủ Cuối

✨ **Chúc bạn học tập hiệu quả và thành công!**  
🚀 **Happy learning và luôn bảo mật!** 🚀  
⚡ **Hack để học, đừng học để hack!!** ⚡  
