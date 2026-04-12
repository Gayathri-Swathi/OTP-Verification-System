# 🔐 OTP Verification System

A simple Python-based OTP (One-Time Password) authentication system that sends a 6-digit OTP to a user's email and verifies it securely.

---

## 🚀 Live Preview

```bash
$ python otp_verification.py

Enter Your OTP:
```

📩 OTP sent to your email

```bash
Enter Your OTP: 482913
OTP Verified Successfully. Access granted.
```

---

## ❌ Failed Attempt Preview

```bash
Enter Your OTP: 123456
Invalid OTP. Attempts left: 2

Enter Your OTP: 111111
Invalid OTP. Attempts left: 1

Maximum attempts reached. Access denied.
```

---

## ⚙️ Features

* 🔢 Generates secure 6-digit OTP
* 📧 Sends OTP via email using SMTP
* 🔁 Allows multiple attempts
* ✅ Validates OTP format
* 🔒 Basic authentication system

---

## 🛠️ Tech Stack

* Python
* smtplib (Email handling)
* Random module

---

## 📂 Project Structure

```bash
OTP-Verification-System/
│── otp_verification.py
│── README.md
```

---

## ▶️ How to Run

1. Install Python
2. Update credentials in code:

   ```python
   MYEMAIL = "your_email@gmail.com"
   PASSWORD = "your_app_password"
   ```
3. Run the file:

   ```bash
   python otp_verification.py
   ```

---

## ⚠️ Important

* Use **App Password**, not your real email password
* Do not upload sensitive credentials to GitHub

---

## 🌟 Future Improvements

* Add OTP expiry timer ⏱️
* Build GUI (Tkinter) 🎨
* Convert to Web App (Flask) 🌐

---

## ⭐ Conclusion

This project demonstrates basic authentication logic, email integration, and user input validation using Python.

