# 🧭 Configuring Directive Controls Using a Login Warning Banner

![Badge](https://img.shields.io/badge/Directive%20Control-Login%20Banner%20%7C%20Compliance-orange?style=for-the-badge)

📄 **Full Lab Report:**  
👉 [Click here to open the complete lab report](https://github.com/Pelumi-Johnson/-Configuring-Detective-Controls-for-Object-Access-Activity-Windows-Auditing-Lab-/blob/main/Configuring%20Detective%20Controls%20for%20Object%20Access%20Activity.pdf)

## 📌 Lab Overview
This lab demonstrates the implementation of a **directive security control** by configuring a
login warning banner on a Windows system. Directive controls are designed to **guide user
behavior** by clearly communicating acceptable use policies and compliance requirements
before system access is granted.

Unlike preventive or detective controls, directive controls rely on **instruction and awareness**
rather than enforcement or logging.

---

## 🎯 Objective
Configure and test a directive control by implementing a login warning banner that:
- Informs users the system is for authorized use only
- References acceptable use policy (AUP) compliance
- Requires acknowledgment prior to authentication

---

## 🧰 Tools & Environment
- uCertify Virtual Lab  
- Windows Client Machine (PC10)  
- Windows PowerShell (Administrator)  
- Windows Registry  
- Domain Administrator Account  

---

## ⚙️ Implementation Summary

### Step 1: Administrator Access
- Connected to the PC10 virtual machine
- Signed in as **jaime** with administrative privileges

### Step 2: PowerShell Configuration
- Opened **Windows PowerShell** as Administrator
- Defined a variable containing the full warning banner text

### Step 3: Registry Configuration
Created registry entries at the following path:

```
HKLM:\Software\Microsoft\Windows\CurrentVersion\Policies\System

```


Configured:
- **legalnoticecaption** → `Authorized Use Only`
- **legalnoticetext** → Full warning banner message

These settings define the title and body of the login warning banner.

### Step 4: Validation
- Signed out of the system
- Accessed the login screen again using **Ctrl + Alt + Delete**
- Verified the warning banner displayed prior to authentication
- Selected **OK** to acknowledge the notice
- Completed sign-in successfully

---

## ✅ Results
- Login warning banner successfully configured
- Registry keys `legalnoticecaption` and `legalnoticetext` created
- Banner displayed before user authentication
- Users informed of acceptable use and compliance requirements
- Directive control tested and validated

---

## 🧠 Key Takeaways
- Directive controls guide user behavior through clear instruction
- Login banners establish legal notice and acceptable use expectations
- Registry-based configuration enables centralized policy enforcement
- Directive controls support **compliance**, not prevention or monitoring
- Validation requires confirming the banner appears during login

---

## 📂 Documentation
📄 [Full lab report available in PDF format](screenshots and step-by-step validation included)
