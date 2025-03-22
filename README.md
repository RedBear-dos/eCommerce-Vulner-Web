![image](https://github.com/user-attachments/assets/c9886c8a-109d-4ae5-bdad-8e75a9f377bd)

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

![image](https://github.com/user-attachments/assets/6d06aaaa-bcca-4747-82c5-b8373b96f4b0)

![image](https://github.com/user-attachments/assets/22b01471-4b45-4770-8d0f-f84eaff44145)

---

### 👤 **User Account**
- User Sign-up / Login  
- Features:  
  ✅ View products & details  
  ✅ Add to cart and checkout  
  ✅ Track orders & shipping  
  ✅ Receive discount codes and promotions  

![image](https://github.com/user-attachments/assets/a64efda6-a315-4d76-a502-847d6f0d3969)

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
- **Telegram**: [@mytelegram](https://t.me/redneardos)  
- **Email**: phamphudong0112@gmail.com  

---

## 🌿 Final Note

✨ **Wishing you a productive and successful day ahead!**  
🚀 **Happy learning and stay secure!** 🚀  
⚡ **Hack to learn, don't learn to hack!!** ⚡  

---

Anh Hai copy từ đây là chạy ngon luôn! Nếu muốn làm thêm **ảnh banner** "JUST $10 🔥" hoặc thêm **icon social**, em làm thêm cho nhé! 🚀
