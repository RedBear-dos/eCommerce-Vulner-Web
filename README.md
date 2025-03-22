![image](https://github.com/user-attachments/assets/5c3fe0cd-6f25-402a-9db2-f2e4991a430f)

---

## 🚨⚠️ Important Disclaimer ⚠️🚨

🚧 **This project is a deliberately vulnerable eCommerce website, self-developed by an individual, and has NO connection with any other organizations or individuals.**  
🚧 **Created for educational purposes ONLY**, targeting students in **Cybersecurity, Pentesting, Ethical Hacking**, etc.  
🚧 **To unlock full access**, please scroll to the end of this page for instructions.

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

![image](https://github.com/user-attachments/assets/08f4b8c7-0dba-4302-af34-1162bb7c23b1)

---

# ⚠️ Vulnerabilities Overview

CyberSam intentionally includes **multiple web vulnerabilities** to help learners understand, exploit, and patch them in a controlled scenario.

---

## 🔍 Recon - Directory Enumeration
- **Description**: Sensitive directories such as `/admin_area/`, `/backup/`, and `/uploads/` are publicly accessible.
- **Risk**: Attackers can discover and exploit these directories using tools like **Gobuster**, **Dirb**, or manual browsing.

![image](https://github.com/user-attachments/assets/510ec3e5-c4c0-41e7-8bf6-cd1d42da588b)

![image](https://github.com/user-attachments/assets/bd6a2b26-dce9-4d1a-838a-3c8efa442926)

## 🔑 Brute Force Login
- **Description**: The admin login page lacks brute force protections like CAPTCHA or account lockout mechanisms.
- **Risk**: Enables attackers to perform credential stuffing or brute-force attacks using tools like **Hydra** or **Burp Suite Intruder**.

  ![image](https://github.com/user-attachments/assets/96676bbd-8049-4586-bf00-fd9b917e09da)

## 🗂️ File Upload Vulnerability
- **Description**: The file upload functionality does not validate file types properly. Attackers can upload malicious files such as `.php` shells.
- **Risk**: Remote Code Execution (RCE), allowing attackers full server control.

![image](https://github.com/user-attachments/assets/a3ac57b2-cc8a-4b4d-be7d-55a0bf8abce0)

## 🆔 IDOR - Insecure Direct Object References
- **Description**: Users can manipulate URL parameters (e.g., `user_id=2`) to access or modify resources belonging to other users.
- **Risk**: Unauthorized access to sensitive user data and orders.

  ![image](https://github.com/user-attachments/assets/9ee6fd1f-619d-4a01-a53f-f7d289b65788)

## 🐞 Stored XSS / DOM XSS
- **Description**: The application does not sanitize user input properly, allowing persistent or DOM-based Cross-Site Scripting attacks.
- **Risk**: Stealing session cookies, hijacking accounts, or injecting malware.

![image](https://github.com/user-attachments/assets/55262042-4e81-43d6-922e-f5c382070a19)

![image](https://github.com/user-attachments/assets/651c6b46-8e2e-498f-b827-93b5313e887c)

## 💉🗄️  SQL Injection

![image](https://github.com/user-attachments/assets/6339b559-43ea-477f-903d-cecc5030f48b)

## 📦⚠️ Other Vulnerabilities

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
- Import the `database.sql` file provided.
- It will Automatically Create DB 

## 4. Access the Website
- User site: `http://localhost/Prototype/`
- Admin panel: `http://localhost/Prototype/admin_area/`

---

# 📞 Contact
If you would like to **launch and experience** the CyberSam platform, I can provide:
- 📂 **The full database**
- 📄 **Detailed documentation about the vulnerabilities**

👉 Please contact me directly:  
- **Telegram**: [@yourtelegram](https://t.me/yourtelegram)  
- **Email**: phamphudong0112@gmail.com  

### 📝 **Request Form** (Optional)  
#### 🚀 **🔥 JUST $10 for FULL ACCESS 🔥**

```
Full Name:  
Phone Number:  
Email:  
Request: [Database] / [Vulnerability Documentation] / [Both]  
Notes (if any):  
```

# 🌿 Final Note
✨ **Wishing you a productive and successful day ahead!**  
Happy learning and stay secure!


🚀✨ **Hack to learn, don't learn to hack!!** ✨🚀

