

🔒 **eCommerce Vulnerable Web**  
A deliberately insecure eCommerce web application designed for learning and practicing web application penetration testing. This project helps security enthusiasts, developers, and students understand common web vulnerabilities in online shopping platforms.

**Features:**
- Simulates a basic eCommerce platform (users, products, orders, etc.)
- Contains vulnerabilities like SQL Injection, Cross-Site Scripting (XSS), Insecure Direct Object References (IDOR), Broken Authentication, and more.
- Ideal for Capture The Flag (CTF) challenges and security workshops.

**⚠️ For educational purposes only!**  
Use responsibly in a controlled environment.

---

Dựa trên các hình ảnh Anh Hai cung cấp, đây là phần mô tả chi tiết về website và các chức năng từng trang. Anh Hai có thể dùng để ghi README hoặc mô tả cho dự án nhé!

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

---

### **🔐 Trang Admin (Admin Panel)**
- Địa chỉ: `http://192.168.1.7/prototype/admin_area/`
- Trang đăng nhập dành riêng cho quản trị viên (`Admin Login`).
- Sau khi đăng nhập thành công, truy cập vào giao diện quản lý với các tính năng chính:
  
#### **Chức năng quản trị:**
1. **Dashboard (Bảng điều khiển):**
   - Tổng quan về sản phẩm, khách hàng, đơn hàng, coupon giảm giá...
2. **Products (Quản lý sản phẩm):**
   - Thêm mới sản phẩm.
   - Sửa, xoá và gán sản phẩm vào danh mục cụ thể.
3. **Bundles (Quản lý combo sản phẩm):**
   - Tạo các gói combo để bán theo set.
4. **Manufacturers (Nhà sản xuất):**
   - Quản lý thông tin các nhà sản xuất laptop.
5. **Categories (Danh mục sản phẩm):**
   - Tạo và chỉnh sửa danh mục như: Laptop Gaming, Văn phòng...
6. **Stores (Cửa hàng):**
   - Thông tin các chi nhánh bán lẻ.
7. **Customers (Khách hàng):**
   - Xem danh sách khách hàng đã đăng ký.
8. **Orders (Đơn hàng):**
   - Kiểm tra trạng thái đơn hàng, xử lý đơn chờ và hoàn tất đơn hàng.
9. **Coupons (Mã giảm giá):**
   - Tạo mã giảm giá cho các chương trình khuyến mãi.
10. **Users (Quản lý tài khoản admin):**
    - Quản lý quyền truy cập admin khác.
11. **Payments (Thanh toán):**
    - Xem chi tiết thanh toán của từng đơn hàng.

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

---


