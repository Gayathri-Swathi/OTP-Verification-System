## 🔐 OTP Verification System - Preview

### ▶️ How it Works

1. The system generates a **6-digit OTP**
2. OTP is sent to the user's email
3. User enters the OTP in the console
4. System verifies the OTP
5. Access is granted or denied based on input

---

### 💻 Sample Output

```bash
Enter Your OTP: 
```

📩 (Check your email)

```bash
Enter Your OTP: 123456
OTP Verified Successfully. Access granted.
```

---

### ❌ Invalid OTP Case

```bash
Enter Your OTP: 654321
Invalid OTP. Attempts left: 2

Enter Your OTP: 111111
Invalid OTP. Attempts left: 1

Maximum attempts reached. Access denied.
```

---

### 📸 Workflow


User → Request OTP → Email Sent → Enter OTP → Verification → Access Granted/Denied
