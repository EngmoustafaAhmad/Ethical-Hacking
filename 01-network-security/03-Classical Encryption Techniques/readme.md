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

# 🔐 Stream Ciphers

## 📘 Overview

This section covers **Stream Ciphers**, one of the main types of symmetric encryption. It explains how they work, random number generation, One-Time Pad (OTP), and Linear Feedback Shift Registers (LFSRs).

---

## 🔹 1. What is a Stream Cipher?

* Encrypts **one bit at a time**
* Uses a **keystream** (random-like sequence)
* Fast and lightweight

### ⚡ مقارنة:

| Feature    | Stream Cipher    | Block Cipher          |
| ---------- | ---------------- | --------------------- |
| Processing | Bit by bit       | Block (e.g., 128-bit) |
| Speed      | Fast             | Slower                |
| Usage      | Embedded systems | Internet security     |

---

## 🔹 2. Encryption & Decryption

تعتمد على عملية XOR:

```text
Encryption:  yi = xi ⊕ si
Decryption:  xi = yi ⊕ si
```

* `x` = plaintext
* `y` = ciphertext
* `s` = keystream

### 💡 ملاحظة:

✔️ نفس العملية للتشفير وفك التشفير

---

## 🔹 3. Why XOR?

* سهلة وسريعة
* قابلة للعكس بنفس العملية
* تعطي توزيع عشوائي جيد

---

## 🔹 4. Types of Stream Ciphers

### 🔸 Synchronous

* يعتمد فقط على المفتاح و IV
* لا يعتمد على ciphertext

### 🔸 Asynchronous (Self-Synchronizing)

* يعتمد على ciphertext
* يعيد التزامن تلقائيًا

---

## 🔹 5. Random Number Generators (RNG)

### 🎲 Types:

#### ✅ True Random Generator (TRNG)

* يعتمد على ظواهر فيزيائية
* غير قابل للتنبؤ
* غير قابل لإعادة الإنتاج

#### ⚠️ Pseudorandom Generator (PRNG)

* يعتمد على Seed
* قابل للتكرار
* **غير آمن للتشفير غالبًا**

---

## 🔐 6. Cryptographically Secure PRNG (CSPRNG)

* نوع خاص من PRNG
* يجب أن يكون:

  * غير قابل للتنبؤ
  * آمن ضد التحليل

📌 يستخدم في:

* Stream Ciphers
* Key Generation

---

## 🔒 7. One-Time Pad (OTP)

### 📌 الفكرة:

```text
Ciphertext = Plaintext ⊕ Key
```

### ✅ المميزات:

* غير قابل للكسر (Perfect Security)
* عشوائية كاملة

### ❌ العيوب:

* المفتاح = طول الرسالة
* صعب التوزيع

---

## 🔁 8. Linear Feedback Shift Registers (LFSRs)

### 📌 الفكرة:

* Register + Feedback باستخدام XOR
* يولد keystream

### ⚙️ الخصائص:

* Output دوري
* أقصى طول:

```text
2^m - 1
```

---

## 🔢 9. Mathematical Representation

```text
si+m = si+k ⊕ si
```

أو باستخدام Polynomial:

```text
P(x) = x^m + p1x^(m-1) + ... + p0
```

---

## ⚠️ 10. Security of LFSR

### ❌ المشكلة:

* يمكن التنبؤ بالمخرجات
* يمكن كسره بسهولة إذا عُرف عدد كافٍ من البتات

### ✅ الحل:

* دمج عدة LFSRs

---

## 🔥 11. Lessons Learned

* Stream ciphers أسرع من block ciphers
* مناسبة للأجهزة الضعيفة (IoT, Mobile)
* تحتاج RNG قوي جدًا
* OTP آمن تمامًا لكنه غير عملي
* LFSR وحده غير آمن

---

## ⚔️ 12. Attack vs Defense

| Component | Weakness         | Solution               |
| --------- | ---------------- | ---------------------- |
| PRNG      | Predictable      | Use CSPRNG             |
| OTP       | Key distribution | Secure channels        |
| LFSR      | Linear           | Combine multiple LFSRs |

---

## 🔐 13. Why Important in Cybersecurity?

Stream ciphers تُستخدم في:

* Wireless security
* Embedded systems
* Real-time encryption

---


## 📌 Summary

في هذا الفصل تعلمت:



* Stream Ciphers vs Block Ciphers
* XOR Encryption
* RNG / PRNG / CSPRNG
* One-Time Pad
* LFSR

💡 هذا الجزء مهم لفهم:

* RC4
* Modern Stream Ciphers
* Secure Key Generation

---

*  أساسيات التشفير
* أنواع الأنظمة (Substitution / Transposition)
* طرق الهجوم (Brute Force / Cryptanalysis)
* أشهر الخوارزميات الكلاسيكية

💡 هذه التقنيات رغم بساطتها هي الأساس لفهم:

* AES
* RSA
* Modern Cryptography

---
