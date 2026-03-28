# 🛡️ Ethical Hacking Lab – Lecture 4 

## 📌 Overview

This lab focuses on **Port Scanning and Service Discovery**, which is a critical step in identifying **open ports, running services, and potential vulnerabilities** in a target system.

---

# 🎯 Learning Objectives

## 1. Ports and Services Overview

## 2. Impact of Firewalls on Scanning

## 3. Port Scanning Techniques

---

# 🌐 1. Ports and Services Overview

## 📌 الفكرة الأساسية

* الـ **IP Address** يحدد الجهاز
* الـ **Port** يحدد الخدمة داخل الجهاز

---

## 🔢 Common Ports

| Service | Port | Protocol |
| ------- | ---- | -------- |
| HTTP    | 80   | TCP      |
| HTTPS   | 443  | TCP      |
| DNS     | 53   | UDP      |

---

## ⚠️ Important Notes

* ممكن تغيير الـ ports من قبل الـ admin
* كل Port عليه **Service واحدة فقط لكل IP**

---

# 🔍 2. Port States (Nmap View)

## 🟢 1. Open

* فيه service شغالة على البورت

---

## 🔴 2. Closed

* مفيش service لكن البورت reachable

---

## 🟡 3. Filtered

* Firewall مانع الوصول

---

## ⚪ 4. Unfiltered

* البورت reachable لكن الحالة غير واضحة

---

## 🟠 5. Open | Filtered

* مش واضح هل مفتوح أو محجوب

---

## ⚫ 6. Closed | Filtered

* مش واضح هل مغلق أو محجوب

---

# 🔥 3. Impact of Firewalls

* Firewalls بتخلي عملية الـ scanning أصعب
* ممكن:

  * تمنع الردود
  * تخفي حالة البورت
* عشان كده Nmap بيستخدم حالات متقدمة

---

# 🧪 4. Port Scanning Techniques

---

## 🔹 1. TCP Connect Scan (-sT)

### 📌 الفكرة:

* بيكمل **3-way handshake بالكامل**

### 🔄 الخطوات:

1. SYN
2. SYN/ACK
3. ACK

ثم:

* يتم قطع الاتصال (RST)

---

### ✅ المميزات:

* دقيق جدًا

### ❌ العيوب:

* سهل اكتشافه (Logged)

---

## 🔹 2. Stealth Scan / SYN Scan (-sS)

### 📌 الفكرة:

* لا يكمل الاتصال

---

### 🔄 السيناريو:

* SYN → SYN/ACK → RST

---

### ✅ المميزات:

* أقل قابلية للاكتشاف

### ❌ العيوب:

* يحتاج صلاحيات (root)

---

## 🔹 3. Xmas Scan (-sX)

### 📌 الفكرة:

* يرسل flags:

```
FIN + PSH + URG
```

---

### 📊 النتيجة:

* RST → البورت مغلق
* No Response → Open | Filtered

---

## 🔹 4. FIN Scan (-sF)

### 📌 الفكرة:

* يرسل FIN فقط

---

### 📊 النتيجة:

* No Response → Open أو Filtered
* RST → Closed

---

### 🎯 Use Case:

* تجاوز بعض أنواع firewall

---

## 🔹 5. NULL Scan (-sN)

### 📌 الفكرة:

* لا يرسل أي flags

---

### 📊 النتيجة:

* No Response → Open | Filtered
* RST → Closed

---

## 🔹 6. UDP Scan (-sU)

### 📌 الفكرة:

* UDP لا يستخدم handshake

---

### 📊 النتيجة:

* ICMP Unreachable → Closed
* No Response → Open أو Filtered

---

### ⚠️ ملاحظات:

* بطيء نسبيًا
* أقل دقة من TCP

---

# 🛠️ Examples (Nmap)

## 🔍 TCP Connect Scan

```id="z6g0q2"
nmap -sT 192.168.1.1
```

---

## 🔍 SYN Scan

```id="y0g7ha"
nmap -sS 192.168.1.1
```

---

## 🔍 Xmas Scan

```id="1g4m5h"
nmap -sX 192.168.1.1
```

---

## 🔍 FIN Scan

```id="h2k8qp"
nmap -sF 192.168.1.1
```

---

## 🔍 NULL Scan

```id="k9d3sj"
nmap -sN 192.168.1.1
```

---

## 🔍 UDP Scan

```id="p4x7lm"
nmap -sU 192.168.1.1
```

---

# ⚠️ Important Notes

* كل تقنية لها استخدام مختلف
* مفيش Scan واحد ينفع لكل الحالات
* لازم Permission قبل أي Scan 🚫

---

# ✅ Conclusion

في هذا اللاب تعلمت:

* الفرق بين Ports و Services
* حالات البورت في Nmap
* تأثير الـ Firewalls
* تقنيات الـ Port Scanning المختلفة

---

## 💡 Tip

> الـ Stealth مش دايمًا الأفضل… اختار التقنية حسب الهدف 😉

---
