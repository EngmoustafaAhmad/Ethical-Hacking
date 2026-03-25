# 🛡️ Ethical Hacking Lab – Lecture 3

## 📌 Overview

This lab covers **Network Scanning**, a critical phase after footprinting.
You will learn how to discover live hosts, identify open ports, and analyze network services using tools like **Nmap** and **Hping3**.

---

# 🎯 Learning Objectives

## 1. Explain Network Scanning Concepts

## 2. Revision of Networking Protocols

## 3. Use Network Scanning Tools

## 4. Host Discovery Techniques

---

# 🌐 1. What is Network Scanning?

Network scanning is the process of:

> Probing a network to collect information about systems and services.

---

## 🎯 أهداف Network Scanning

* اكتشاف الأجهزة المتصلة (Live Hosts)
* معرفة IP addresses
* تحديد الـ open ports
* معرفة الخدمات (Services)
* اكتشاف الثغرات

---

# 🔄 2. TCP/IP Communication

## 📡 TCP Protocol

بروتوكول مسؤول عن نقل البيانات بشكل موثوق

---

## 🚩 TCP Flags

* **SYN** → بدء الاتصال
* **ACK** → تأكيد الاستلام
* **FIN** → إنهاء الاتصال
* **RST** → إعادة ضبط الاتصال
* **PSH** → إرسال البيانات فورًا
* **URG** → بيانات عاجلة

---

## 🤝 Three-Way Handshake

1. Client → SYN
2. Server → SYN + ACK
3. Client → ACK

✅ الاتصال تم بنجاح

---

## ❌ Session Termination

* باستخدام FIN + ACK لإنهاء الاتصال

---

# 🌍 3. Networking Basics (Revision)

## 🧱 Network Segment

مجموعة أجهزة على نفس الشبكة

## 🌐 Subnet

شبكة فرعية لها:

* IP Range خاص
* Router

---

## 📊 Subnet Examples

* `/16` → حوالي 65,000 جهاز
* `/24` → حوالي 250 جهاز

---

# 📡 Important Protocols

## 🔗 ARP

* يحول IP → MAC Address
* يستخدم داخل الشبكة المحلية

---

## 🌐 ICMP

* يستخدم في ping
* Types:

  * Echo Request (8)
  * Echo Reply (0)

---

## 🚀 TCP / UDP

* يستخدموا لفحص البورتات والخدمات

---

# 🔍 4. Host Discovery Techniques

## 🧠 الهدف

معرفة الأجهزة "الـ Online" داخل الشبكة

---

## 🟢 1. ARP Ping Scan

* الأفضل داخل LAN
* سريع ودقيق

---

## 🔵 2. ICMP Ping Scan

### الأنواع:

* Echo Ping
* Timestamp Ping
* Address Mask Ping
* Ping Sweep

---

## 🟡 3. TCP Ping Scan

### الأنواع:

* SYN Ping
* ACK Ping

---

## 🟠 4. UDP Ping Scan

* يعتمد على ICMP response

---

## 🔴 5. IP Protocol Scan

* يستخدم بروتوكولات مختلفة لاكتشاف الأجهزة

---

# 🛠️ 5. Network Scanning Tools

---

## 🔥 1. Nmap

### 📌 الاستخدام:

* اكتشاف الأجهزة
* فحص البورتات
* معرفة الخدمات
* تحديد نظام التشغيل

---

### 💻 مثال:

```
nmap -p 1-65535 -T4 -A -v 10.10.1.11
```

---

### ⚡ Features:

* عرض البورتات المفتوحة
* تحديد OS
* كشف الخدمات

---

## ⚡ 2. Hping3

أداة قوية للتحكم في الباكيتات

---

### 📌 أمثلة:

#### 🔹 ICMP Ping

```
hping3 -1 10.0.0.25
```

---

#### 🔹 ACK Scan

```
hping3 -A 10.0.0.25 -p 80
```

---

#### 🔹 UDP Scan

```
hping3 -2 10.0.0.25 -p 80
```

---

#### 🔹 SYN Scan Range

```
hping3 -8 50-60 -S 10.0.0.25
```

---

#### 🔹 Stealth Scan

```
hping3 -F -P -U 10.0.0.25 -p 80
```

---

## 🧨 3. Metasploit

### 📌 الاستخدام:

* فحص الثغرات
* استغلالها

### ⚡ Features:

* يحتوي على modules جاهزة
* يستخدم في penetration testing

---

# 🧪 6. Host Discovery باستخدام Nmap

---

## 🔹 ARP Scan

* يعمل فقط داخل نفس الشبكة

---

## 🔹 ICMP Ping Sweep

```
nmap -PE -sn 192.168.1.0/24
```

---

### ⚠️ عيوبه:

* بطيء
* ممكن firewall يمنعه

---

## 🔹 ICMP Timestamp

```
nmap -PP -sn <target>
```

---

## 🔹 ICMP Address Mask

```
nmap -PM -sn <target>
```

---

## 🔹 TCP SYN Ping

```
nmap -PS80 -sn <target>
```

---

### 📊 النتيجة:

* SYN/ACK → الجهاز شغال
* RST → البورت مغلق

---

## 🔹 TCP ACK Ping

```
nmap -PA80 -sn <target>
```

---

## 🔹 UDP Ping

* يستخدم لاكتشاف الأجهزة خلف firewall

---

# ⚠️ Important Notes

* بعض الشبكات تمنع ICMP
* لازم تستخدم تقنيات مختلفة
* استخدام الأدوات بدون إذن = غير قانوني 🚫

---

# ✅ Conclusion

في هذا اللاب تعلمت:

* مفهوم Network Scanning
* أساسيات TCP/IP
* طرق اكتشاف الأجهزة
* استخدام أدوات قوية مثل Nmap و Hping3

---

## 💡 Tip

> أفضل Ethical Hacker هو اللي يعرف "يقرأ الشبكة" قبل ما يهاجمها 😉

---
