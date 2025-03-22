---

# 🔒 CyberSam - eCommerce Vulnerable Web
A **deliberately insecure eCommerce web application** built for educational purposes. This project is designed to help **security enthusiasts**, **developers**, and **students** practice and understand **common web vulnerabilities** in an online shopping platform environment.

---

## 🚀 Key Features
- Basic eCommerce platform simulation (users, products, orders, etc.)
- Intentionally includes vulnerabilities such as:
  - SQL Injection (SQLi)
  - Cross-Site Scripting (XSS)
  - Insecure Direct Object References (IDOR)
  - Broken Authentication
  - Cross-Site Request Forgery (CSRF)
  - Unrestricted File Upload, and more!
  - And others vulnerbilities ...
- Perfect for Capture The Flag (CTF) challenges, penetration testing practice, and security workshops.

⚠️ **For educational and testing purposes only!**  
Always use in a **controlled environment**.

---

# 🌐 Website Structure

### 🛒 **User Website**
- URL: `http://192.168.1.7/prototype/`
- Simulates a laptop eCommerce store with:
  - Promotions & Featured products
  - Menu Navigation:
    - `News`
    - `About Us`
    - `Shop`
    - `Local Stores`
    - `My Account` (Sign Up / Login)
- Features:
  - Product browsing and details
  - Add items to cart
  - User registration / login
  - Checkout and order processing
  - Others function ... 

---

### 🔐 **Admin Panel**
- URL: `localhost/prototype/admin_area/`
- Admin login page
![image](https://github.com/user-attachments/assets/811cba21-4f4c-4be8-890c-b030f49a5688)

- After successful login, the admin dashboard provides:
  - Product management
  - Order management
  - User management
  - Promotions / Coupons management

![image](https://github.com/user-attachments/assets/673cddf3-9cb2-4b8a-b040-28afa9723d41) 

---

### 👤 **User Account**
- User sign-up and login functionality
- Features:
  - View product listings and details
  - Add products to cart and checkout
  - Track orders and shipping status
  - Receive discount codes and promotions

---

# ⚠️ Vulnerabilities Overview

CyberSam intentionally includes **multiple web vulnerabilities** to help learners understand, exploit, and patch them in a controlled scenario.

---

## 🔍 Recon - Directory Enumeration
- **Description**: Sensitive directories such as `/admin_area/`, `/backup/`, and `/uploads/` are publicly accessible.
- **Risk**: Attackers can discover and exploit these directories using tools like **Gobuster**, **Dirb**, or manual browsing.
- _(Add directory scan screenshots here)_

---

## 🔑 Brute Force Login
- **Description**: The admin login page lacks brute force protections like CAPTCHA or account lockout mechanisms.
- **Risk**: Enables attackers to perform credential stuffing or brute-force attacks using tools like **Hydra** or **Burp Suite Intruder**.
- _(Add brute force attack screenshots here)_

---

## 🗂️ File Upload Vulnerability
- **Description**: The file upload functionality does not validate file types properly. Attackers can upload malicious files such as `.php` shells.
- **Risk**: Remote Code Execution (RCE), allowing attackers full server control.
- _(Add shell upload and webshell access screenshots here)_

---

## 🆔 IDOR - Insecure Direct Object References
- **Description**: Users can manipulate URL parameters (e.g., `user_id=2`) to access or modify resources belonging to other users.
- **Risk**: Unauthorized access to sensitive user data and orders.
- _(Add IDOR exploitation screenshots here)_

---

## 🐞 Stored XSS / DOM XSS
- **Description**: The application does not sanitize user input properly, allowing persistent or DOM-based Cross-Site Scripting attacks.
- **Risk**: Stealing session cookies, hijacking accounts, or injecting malware.
- _(Add XSS payload and execution screenshots here)_

---

# 🛠️ Quick Start Guide

## 1. Install XAMPP
- Download and install XAMPP:  
  [https://www.apachefriends.org](https://www.apachefriends.org)
- Start **Apache** and **MySQL** from the XAMPP control panel.

## 2. Upload Source Code
- Extract the project folder and move it to:  
  ```
  C:\xampp\htdocs\
  ```
  Example:  
  ```
  C:\xampp\htdocs\cybersam
  ```

## 3. Import Database
- Go to `http://localhost/phpmyadmin`
- Create a new database, e.g., `cybersam_db`
- Import the `database.sql` file provided.

## 4. Access the Website
- User site: `http://localhost/cybersam/`
- Admin panel: `http://localhost/cybersam/admin_area/`

---

# 📞 Contact
If you would like to **launch and experience** the CyberSam platform, I can provide:
- 📂 **The full database**
- 📄 **Detailed documentation about the vulnerabilities**

👉 Please contact me directly:  
- **Telegram**: [@yourtelegram](https://t.me/yourtelegram)  
- **Email**: yourmail@gmail.com  

---

### 📝 Request Form (Optional)
```
Full Name:  
Phone Number:  
Email:  
Request: [Database] / [Vulnerability Documentation] / [Both]  
Notes (if any):  
```

---

# 🌿 Final Note
✨ **Wishing you a productive and successful day ahead!**  
Happy learning and stay secure!

---

Anh Hai check thử nha! Nếu muốn anh em mình làm thêm bản markdown file `README.md` hoặc thêm chi tiết CTF lab thì em làm liền luôn! 🚀
