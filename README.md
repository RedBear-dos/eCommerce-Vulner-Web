

🔒 **eCommerce Vulnerable Web**  
A deliberately insecure eCommerce web application designed for learning and practicing web application penetration testing. This project helps security enthusiasts, developers, and students understand common web vulnerabilities in online shopping platforms.

**Features:**
- Simulates a basic eCommerce platform (users, products, orders, etc.)
- Contains vulnerabilities like SQL Injection, Cross-Site Scripting (XSS), Insecure Direct Object References (IDOR), Broken Authentication, and more.
- Ideal for Capture The Flag (CTF) challenges and security workshops.

**⚠️ For educational purposes only!**  
Use responsibly in a controlled environment.

---

## 🛒 CyberSam - eCommerce Vulnerable Web  
**CyberSam** là một website thương mại điện tử mô phỏng, xây dựng nhằm phục vụ mục đích học tập và thực hành kiểm thử bảo mật web (Web Pentest). Hệ thống bao gồm giao diện người dùng, trang quản trị admin và các chức năng cơ bản của một website bán hàng trực tuyến.

---

### **🌐 Trang chính (User Website)**
- Địa chỉ: `http://192.168.1.7/prototype/`
- Giao diện mô phỏng một cửa hàng bán laptop trực tuyến.
- Hiển thị các chương trình khuyến mãi, quảng cáo sản phẩm nổi bật.
- Các menu điều hướng gồm:
  - `News`: Tin tức sản phẩm.
  - `About Us`: Giới thiệu về cửa hàng.
  - `Shop`: Danh sách sản phẩm.
  - `Local Stores`: Hệ thống cửa hàng.
  - `My Account`: Đăng ký / Đăng nhập tài khoản.
- Chức năng:
  - Xem thông tin chi tiết sản phẩm.
  - Thêm sản phẩm vào giỏ hàng.
  - Đăng ký / Đăng nhập tài khoản người dùng.
  - Đặt hàng (Checkout).

(image) 

---

### **🔐 Trang Admin (Admin Panel)**
- Địa chỉ: `http://192.168.1.7/prototype/admin_area/`
- Trang đăng nhập dành riêng cho quản trị viên (`Admin Login`).
- Sau khi đăng nhập thành công, truy cập vào giao diện quản lý với các tính năng chính:
  
#### **Chức năng quản trị:**

(image) 

---

### **👤 Trang User (Người dùng)**
- Đăng ký và đăng nhập tài khoản khách hàng.
- Chức năng:
  - Xem danh sách và chi tiết sản phẩm.
  - Thêm sản phẩm vào giỏ hàng.
  - Thực hiện thanh toán đơn hàng.
  - Theo dõi đơn hàng và trạng thái vận chuyển.
  - Nhận mã giảm giá và khuyến mãi.
  
---

### **🚩 Lưu ý**
Đây là môi trường mô phỏng **cố tình chứa lỗ hổng bảo mật** để phục vụ việc học tập và nghiên cứu về an toàn thông tin như:
- SQL Injection
- XSS (Cross Site Scripting)
- IDOR (Insecure Direct Object References)
- Broken Authentication
- CSRF (Cross-Site Request Forgery)
- Và nhiều lỗ hổng khác...

⚠️ **Chỉ sử dụng trong môi trường kiểm thử nội bộ!**

(image) 

---

Dưới đây là bản hướng dẫn ngắn gọn như Anh Hai yêu cầu nè:

---

## 🚀 Hướng Dẫn Khởi Động Website CyberSam

1. **Cài đặt XAMPP**  
   - Tải và cài XAMPP tại [https://www.apachefriends.org](https://www.apachefriends.org)  
   - Khởi động **Apache** và **MySQL** trong XAMPP Control Panel.

2. **Upload source code**  
   - Giải nén và copy folder project vào:  
     ```
     C:\xampp\htdocs\
     ```  
   - Ví dụ:  
     ```
     C:\xampp\htdocs\cybersam
     ```

3. **Tạo database và import file**  
   - Truy cập `http://localhost/phpmyadmin`  
   - Tạo database mới (ví dụ `cybersam_db`)  
   - Import file `database.sql` vào database này.

4. **Truy cập website**  
   - Trang chính: `http://localhost/cybersam/`  
   - Trang admin: `http://localhost/cybersam/admin_area/`

(image) 

---
Dưới đây là bản mô tả các lỗ hổng (vulnerabilities) cho project **CyberSam eCommerce Vulnerable Web** của Anh Hai. Anh chỉ cần dán thêm hình ảnh minh họa vào từng phần là xong.

---

## 🔥 Các lỗ hổng bảo mật mô phỏng trong hệ thống

### 1. Recon Directory
- **Mô tả**: Một số thư mục nhạy cảm (ví dụ: `/admin_area/`, `/backup/`, `/uploads/`) không được bảo vệ, có thể phát hiện qua các công cụ scan thư mục như Gobuster, Dirb, hoặc tự tìm kiếm thủ công.
- **Rủi ro**: Hacker có thể tìm thấy các trang quản trị hoặc file backup chứa thông tin nhạy cảm.
- **Ảnh minh họa**:  
  _(Dán ảnh kết quả scan thư mục tại đây)_

---

### 2. Brute Force Login
- **Mô tả**: Trang đăng nhập admin không giới hạn số lần thử sai, không có CAPTCHA hay cơ chế khóa tài khoản sau nhiều lần thất bại.
- **Rủi ro**: Dễ bị tấn công brute force để dò tìm mật khẩu admin.
- **Ảnh minh họa**:  
  _(Dán ảnh sử dụng Hydra, Burp Suite Intruder brute force vào login form tại đây)_

---

### 3. File Upload Vulnerability
- **Mô tả**: Chức năng upload ảnh không kiểm tra đúng loại file, cho phép upload file thực thi (như `.php`) lên server.
- **Rủi ro**: Hacker có thể upload webshell để điều khiển máy chủ từ xa.
- **Ảnh minh họa**:  
  _(Dán ảnh upload shell thành công + truy cập shell tại đây)_

---

### 4. IDOR (Insecure Direct Object References)
- **Mô tả**: Người dùng có thể thay đổi tham số trên URL để truy cập hoặc sửa thông tin không thuộc quyền quản lý (ví dụ: `user_id=2`).
- **Rủi ro**: Tiết lộ thông tin khách hàng khác hoặc chỉnh sửa dữ liệu đơn hàng trái phép.
- **Ảnh minh họa**:  
  _(Dán ảnh thao tác IDOR, chỉnh sửa đơn hàng khác hoặc xem thông tin khách tại đây)_

---

### 5. Stored XSS / DOM XSS
- **Mô tả**: Ứng dụng không lọc dữ liệu nhập từ người dùng, cho phép chèn mã JavaScript độc hại. Kịch bản XSS được lưu lại và thực thi trên trình duyệt các nạn nhân khác.
- **Rủi ro**: Tấn công đánh cắp cookie, chiếm quyền session hoặc phát tán mã độc.
- **Ảnh minh họa**:  
  _(Dán ảnh payload XSS và kết quả thực thi script trên giao diện tại đây)_


---

Dưới đây là phiên bản hoàn chỉnh, em thêm luôn dòng chúc nha Anh Hai:

---

## 📞 Contact
Nếu bạn muốn khởi động và trải nghiệm website này, tôi sẽ cung cấp:
- 📂 **File database đầy đủ**
- 📄 **Tài liệu mô tả chi tiết các lỗ hổng bảo mật**

👉 Vui lòng liên hệ trực tiếp qua:  
- **Telegram**: [@yourtelegram](https://t.me/yourtelegram)  
- **Gmail**: yourmail@gmail.com  

---

### 🛒 Mẫu Form Đăng Ký Nhận File
```
Tên người nhận:  
Số điện thoại:  
Email liên hệ:  
Yêu cầu nhận file: [ Database / Tài liệu lỗ hổng / Cả hai ]  
Ghi chú thêm (nếu có):  
```

---

### 🌿 Chúc các bạn có một ngày học tập và làm việc thật hiệu quả và tốt lành!

---


