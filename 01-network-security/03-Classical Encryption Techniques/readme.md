# 🔐 Classical Encryption Techniques

## 📘 Overview

This chapter introduces **classical cryptography techniques**, including substitution and transposition ciphers. These methods form the historical foundation of modern encryption systems.

---

## 🔑 1. Basic Definitions

* **Plaintext** → Original message
* **Ciphertext** → Encrypted message
* **Encryption (Enciphering)** → تحويل النص إلى مشفر
* **Decryption (Deciphering)** → استرجاع النص الأصلي

---

## 🧠 2. Cryptology Fields

* **Cryptography** → تصميم التشفير
* **Cryptanalysis** → كسر التشفير
* **Cryptology** → الاثنين معًا

---

## 🔄 3. Types of Cryptographic Systems

### 🔸 Based on Operation

* Substitution → استبدال الحروف
* Transposition → تغيير ترتيب الحروف

### 🔸 Based on Keys

* Symmetric → مفتاح واحد
* Asymmetric → مفتاحين

### 🔸 Based on Processing

* Block Cipher
* Stream Cipher

---

## ⚔️ 4. Attacks on Encryption

### 🔍 Cryptanalysis

* تحليل الخوارزمية لاكتشاف المفتاح أو النص

### 💣 Brute Force Attack

* تجربة كل المفاتيح الممكنة

📌 في المتوسط:

* تحتاج تجربة نصف عدد المفاتيح

---

## 🛡️ 5. Encryption Security

### 🔒 Unconditionally Secure

* مستحيل كسره حتى بوقت غير محدود

### ⚡ Computationally Secure

* كسره غير عملي (وقت/تكلفة عالية)

---

## 🔤 6. Substitution Techniques

### 🧩 الفكرة:

استبدال كل حرف بحرف آخر

---

## 🏛️ 7. Caesar Cipher

### 📌 الفكرة:

إزاحة الحروف بمقدار ثابت

### 🧮 المعادلة:

```
C = (P + k) mod 26
P = (C - k) mod 26
```

### ✅ Example:

```
HELLO → KHOOR (shift = 3)
```

---

## 🔠 8. Monoalphabetic Cipher

* استخدام permutation كامل للحروف
* عدد المفاتيح:

```
26! ≈ 4 × 10^26
```

### ❌ المشكلة:

* سهل الكسر باستخدام **Frequency Analysis**

---

## 🔡 9. Playfair Cipher

* يعتمد على **Pairs (Digrams)**
* يستخدم Matrix 5×5

### ✅ مميزاته:

* أقوى من Caesar
* يخفي التكرار البسيط

---

## 🧮 10. Hill Cipher

* يعتمد على **Matrix Multiplication**

### ✅ مميزاته:

* يخفي تكرار الحروف
* قوي ضد ciphertext-only

### ❌ ضعيف ضد:

* Known Plaintext Attack

---

## 🔁 11. Polyalphabetic Ciphers

* استخدام أكثر من substitution

### 🎯 الهدف:

تقليل تأثير Frequency Analysis

---

## 🔐 12. Vigenère Cipher

### 📌 الفكرة:

* استخدام كلمة مفتاح متكررة

### ✅ Example:

```
Plaintext:  WEAREDISCOVERED
Key:        DECEPTIVEDECEPTIVE
Ciphertext: ZICVTWQNGRZGVTW
```

---

## 🔄 13. Autokey Cipher

* المفتاح = Keyword + Plaintext

### ❌ المشكلة:

* قابل للتحليل الإحصائي

---

## 🧨 14. Vernam Cipher

* يعتمد على XOR

---

## 🔒 15. One-Time Pad (OTP)

### ✅ أقوى نظام تشفير:

* مفتاح عشوائي
* نفس طول الرسالة
* يستخدم مرة واحدة

### 🔥 الميزة:

* **Unbreakable (Perfect Secrecy)**

### ❌ المشاكل:

* صعوبة توليد مفاتيح
* مشكلة توزيع المفاتيح

---

## 🔀 16. Transposition Techniques

### 🧩 الفكرة:

تغيير ترتيب الحروف بدل استبدالها

---

## 🚆 17. Rail Fence Cipher

* كتابة النص بشكل zigzag

### ✅ Example:

```
MEETME → MEMETE
```

---

## 🔢 18. Row Transposition Cipher

* كتابة النص في جدول
* إعادة ترتيب الأعمدة حسب المفتاح

---

## 🔥 19. Attack vs Defense Insight

| Technique      | Weakness        | Attack             |
| -------------- | --------------- | ------------------ |
| Caesar         | Small key space | Brute Force        |
| Monoalphabetic | Frequency       | Frequency Analysis |
| Vigenère       | Repeating key   | Kasiski Attack     |
| OTP            | None            | Not breakable      |

---

## 🔐 20. Why Important in Cybersecurity?

Classical ciphers are the foundation of:

* Modern Encryption Algorithms
* Cryptanalysis Techniques
* Security Thinking

---

## 📌 Summary

في هذا الفصل تعلمت:

* أساسيات التشفير
* أنواع الأنظمة (Substitution / Transposition)
* طرق الهجوم (Brute Force / Cryptanalysis)
* أشهر الخوارزميات الكلاسيكية

💡 هذه التقنيات رغم بساطتها هي الأساس لفهم:

* AES
* RSA
* Modern Cryptography

---
