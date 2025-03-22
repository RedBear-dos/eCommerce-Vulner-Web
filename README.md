Dạ, đây là bản chỉnh sửa lại toàn bộ nội dung README cho **CyberSam - eCommerce Vulnerable Web**. Em đã căn chỉnh, làm gọn, trình bày đẹp hơn, chuyên nghiệp hơn, đảm bảo nhìn là muốn đọc luôn! Anh Hai copy và dán qua GitHub là chuẩn ngay.

---

<div align="center">

# 🚨⚠️ Important Disclaimer ⚠️🚨  
🚧 **This project is a deliberately vulnerable eCommerce website, self-developed by an individual, and has NO connection with any other organizations or individuals.**  
🚧 **Created for educational purposes ONLY**, targeting students in **Cybersecurity, Pentesting, Ethical Hacking**, etc.  
🚧 **To unlock full access**, please scroll to the end of this page for instructions.

---

# 🔒 CyberSam - eCommerce Vulnerable Web  
A **deliberately insecure eCommerce web application** built for educational purposes.  
This project helps **security enthusiasts**, **developers**, and **students** practice and understand **common web vulnerabilities** in an online shopping environment.

</div>

---

## 🚀 Key Features
✅ Basic eCommerce platform simulation (users, products, orders, etc.)  
✅ Intentionally includes vulnerabilities such as:
- 💉 SQL Injection (SQLi)
- 🐞 Cross-Site Scripting (XSS)
- 🆔 Insecure Direct Object References (IDOR)
- 🔑 Broken Authentication
- 🕸️ Cross-Site Request Forgery (CSRF)
- 📂 Unrestricted File Upload
- ...and more!

🎯 Perfect for:
- Capture The Flag (CTF) challenges  
- Penetration testing practice  
- Security workshops  

⚠️ **For educational and testing purposes only! Always use in a controlled environment.**

---

## 🌐 Website Structure

### 🛒 **User Website**
- **URL**: `http://192.168.1.7/prototype/`  
- Simulates a laptop eCommerce store with:
  - Promotions & Featured products  
  - Menu Navigation:  
    `News`, `About Us`, `Shop`, `Local Stores`, `My Account` (Sign Up / Login)  
- Features:  
  ✅ Product browsing and details  
  ✅ Add items to cart  
  ✅ User registration / login  
  ✅ Checkout and order processing  

---

### 🔐 **Admin Panel**
- **URL**: `localhost/prototype/admin_area/`  
- Admin login page  
- Features:  
  ✅ Product management  
  ✅ Order management  
  ✅ User management  
  ✅ Promotions / Coupons management  

---

### 👤 **User Account**
- User Sign-up / Login  
- Features:  
  ✅ View products & details  
  ✅ Add to cart and checkout  
  ✅ Track orders & shipping  
  ✅ Receive discount codes and promotions  

---

## ⚠️ Vulnerabilities Overview

CyberSam includes **multiple web vulnerabilities** for learners to understand, exploit, and patch in a controlled scenario.

| Vulnerability                  | Description                                                |
|------------------------------- |------------------------------------------------------------|
| 🔍 **Directory Enumeration**    | Exposed directories (`/admin_area/`, `/backup/`, `/uploads/`) can be discovered using tools like **Gobuster** or **Dirb**. |
| 🔑 **Brute Force Login**        | No protection against brute force attacks (no CAPTCHA, no lockout). Tools like **Hydra** or **Burp Suite Intruder** can be used. |
| 🗂️ **File Upload Vulnerability** | No proper file type validation. Attackers can upload `.php` shells for Remote Code Execution (RCE). |
| 🆔 **IDOR**                    | Manipulate URL params to access or modify data (`user_id=2`). |
| 🐞 **Stored/DOM XSS**           | No input sanitization. Attackers can inject scripts to steal cookies or hijack sessions. |
| 💉 **SQL Injection (SQLi)**     | Vulnerable queries allow attackers to exfiltrate or modify database contents. |

---

## 🛠️ Quick Start Guide

### 1️⃣ Install XAMPP  
👉 Download & Install [XAMPP](https://www.apachefriends.org)  
👉 Start **Apache** and **MySQL** from XAMPP Control Panel  

### 2️⃣ Upload Source Code  
👉 Extract project folder into:  
```
C:\xampp\htdocs\
```  
👉 Example:  
```
C:\xampp\htdocs\cybersam
```

### 3️⃣ Import Database  
👉 Go to `http://localhost/phpmyadmin`  
👉 Import `database.sql` (provided in the package)  
👉 Database will be created automatically  

### 4️⃣ Access the Website  
👉 User site: `http://localhost/Prototype/`  
👉 Admin panel: `http://localhost/Prototype/admin_area/`

---

## 📝 Request Form (Optional)

<div align="center">

# 🚀🔥 JUST $10 for FULL ACCESS 🔥🚀  
### (Database + Vulnerability Documentation)

<table>
<tr><td><strong>Full Name</strong></td><td>Your Full Name</td></tr>
<tr><td><strong>Phone Number</strong></td><td>Your Contact Number</td></tr>
<tr><td><strong>Email</strong></td><td>Your Email Address</td></tr>
<tr><td><strong>Request</strong></td><td>[Database] / [Vulnerability Documentation] / [Both]</td></tr>
<tr><td><strong>Notes (Optional)</strong></td><td>Any special instructions or requests</td></tr>
</table>

</div>

---

## 📞 Contact

If you would like to **launch and experience** the CyberSam platform, I can provide:  
📂 **The full database**  
📄 **Detailed documentation about the vulnerabilities**  

👉 **Contact me directly:**  
- **Telegram**: [@yourtelegram](https://t.me/yourtelegram)  
- **Email**: phamphudong0112@gmail.com  

---

## 🌿 Final Note

✨ **Wishing you a productive and successful day ahead!**  
🚀 **Happy learning and stay secure!** 🚀  
⚡ **Hack to learn, don't learn to hack!!** ⚡  

---

Anh Hai copy từ đây là chạy ngon luôn! Nếu muốn làm thêm **ảnh banner** "JUST $10 🔥" hoặc thêm **icon social**, em làm thêm cho nhé! 🚀
