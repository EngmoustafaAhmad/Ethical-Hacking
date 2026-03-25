# 🛡️ Ethical Hacking Lab – Lecture 2 (README)

## 📌 Overview

This lab focuses on **Footprinting**, the first phase of ethical hacking. You will learn how attackers and ethical hackers gather information about a target using **passive and active techniques**, especially through search engines and Google hacking.

---

# 🎯 Learning Objectives

## 1. Explain Footprinting Concepts

* What is Footprinting
* Types of Footprinting
* Information gathered
* Footprinting methodology

## 2. Footprinting using Search Engines

* Search engine reconnaissance
* Google Hacking
* Advanced search operators

## 3. Google Hacking Database (GHDB)

* Google Dorks
* Practical activities

---

# 🔍 1. What is Footprinting?

Footprinting is the **first step in any cyberattack or security assessment**.
It involves collecting as much information as possible about a target system to identify potential vulnerabilities.

---

## 🧠 Types of Footprinting

### 🟢 Passive Footprinting

* بدون تفاعل مباشر مع الهدف
* صعب اكتشافه
* مثال:

  * مواقع عامة
  * سوشيال ميديا

---

### 🔴 Active Footprinting

* فيه تفاعل مباشر مع الهدف
* ممكن يتم اكتشافه
* مثال:

  * إرسال requests
  * DNS queries

---

# 📊 2. Information Gathered

## 🏢 Organization Information

* أسماء الموظفين
* أرقام التليفونات
* الفروع
* التكنولوجيا المستخدمة

---

## 🌐 Network Information

* Domain & Subdomains
* IP addresses
* DNS records
* Network topology

---

## 💻 System Information

* نوع السيرفر (OS)
* Email addresses
* Usernames
* Login portals

---

# 🧩 3. Footprinting Methodology

## 📌 Techniques Used:

### 🔎 1. Search Engines

جمع معلومات باستخدام Google وغيرها

### 🌍 2. Web Services

استخراج metadata

### 📱 3. Social Networking

تحليل حسابات السوشيال ميديا

### 🌐 4. Website Footprinting

تحليل هيكل الموقع

### 📧 5. Email Footprinting

تحليل headers

### 🧾 6. Whois Lookup

معرفة بيانات تسجيل الدومين

### 🌐 7. DNS Footprinting

تحليل DNS records

### 🛰️ 8. Network Footprinting

رسم خريطة الشبكة

### 🧠 9. Social Engineering

استغلال العنصر البشري

---

# 🌍 4. Footprinting Through Search Engines

## 🎯 الهدف

استخدام محركات البحث لجمع معلومات مثل:

* صفحات تسجيل الدخول
* بيانات الموظفين
* التكنولوجيا المستخدمة

---

## 🔎 أشهر محركات البحث

* Google
* Bing
* Yahoo
* DuckDuckGo

---

## ⚡ مميزات الطريقة

* Passive (صعب اكتشافها)
* سريعة وسهلة
* تعتمد على معلومات عامة

---

# 💣 5. What is Google Hacking?

Google Hacking هو استخدام **Advanced Search Operators**
للوصول إلى معلومات مخفية أو حساسة.

---

# 🧰 6. Important Search Operators

## 🔹 Basic Operators

```
site:example.com
```

يحدد البحث داخل موقع معين

```
filetype:pdf
```

يبحث عن نوع ملف معين

```
cache:
```

يعرض نسخة محفوظة من الصفحة

---

## 🔹 Title-Based

```
intitle:login
allintitle:admin login
```

---

## 🔹 URL-Based

```
inurl:login
allinurl:admin panel
```

---

## 🔹 Location-Based

```
location:Egypt
```

---

# 🗂️ 7. Google Hacking Database (GHDB)

GHDB هو:

> قاعدة بيانات تحتوي على Google Dorks جاهزة

---

## 🎯 الهدف منها

* اكتشاف ثغرات
* العثور على بيانات حساسة
* تحليل الأنظمة

---

# 🧪 8. Google Dorks (Activities)

## ✅ Activity 1

```
site:testphp.vulnweb.com inurl:login
```

🎯 الهدف:

* إيجاد صفحات تسجيل الدخول

---

## ✅ Activity 2

```
site:certifiedhacker.com filetype:pdf
```

🎯 الهدف:

* استخراج ملفات PDF

---

## ✅ Activity 3

```
site:testphp.vulnweb.com intitle:"Index of /"
```

🎯 الهدف:

* العثور على Open Directories

---

# 🌐 9. WHOIS Footprinting

## 📌 الفكرة

استخدام أدوات Whois للحصول على معلومات عن الدومين

---

## 🧾 المعلومات التي يتم جمعها:

* Owner details
* Name servers
* IP address
* Location

---

## 🛠️ مثال عملي

* ادخل على: https://whois.domaintools.com
* ابحث عن:

```
www.certifiedhacker.com
```

---

# ⚠️ Important Notes

* كل العمليات دي تستخدم فقط في **Ethical Hacking**
* لازم يكون عندك **Permission**
* استخدام الأدوات بدون إذن = مخالفة قانونية 🚫

---

# ✅ Conclusion

في هذا اللاب تعلمت:

* مفهوم Footprinting
* طرق جمع المعلومات
* استخدام Google Hacking
* تحليل البيانات باستخدام GHDB

---

## 💡 Tip

> أفضل Hacker هو اللي يعرف يجمع معلومات كويس قبل ما يبدأ الهجوم 😉

---
