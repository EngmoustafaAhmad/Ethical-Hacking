# 🛡️ Ethical Hacking Lab – Lecture 1 (README)

## 📌 Overview

This lab introduces the fundamental concepts of **Information Security**, **Hacking Methodologies**, and **Hacker Types**. It also explains how to safely perform experiments using a virtual lab environment.

---

# 🎯 Learning Objectives

## LO#01: Information Security Concepts

* Understand core security principles
* تعرف دوافع وأنواع الهجمات

## LO#02: Hacking Methodologies

* فهم مراحل الاختراق
* التعرف على **Cyber Kill Chain**
* فهم العلاقة بين Vulnerability, Threat, Risk

## LO#03: Hacking Concepts & Hacker Types

* تعريف الهاكر
* أنواع الهاكرز ودوافعهم

---

# 🔐 1. Elements of Information Security (CIA + 2)

### 1. Confidentiality (السرية)

حماية البيانات بحيث لا يطلع عليها غير المصرح لهم.

### 2. Integrity (سلامة البيانات)

ضمان عدم تعديل البيانات بشكل غير مصرح.

### 3. Availability (الإتاحة)

توفر الأنظمة والبيانات عند الحاجة.

### 4. Authenticity (الموثوقية)

التأكد أن المصدر حقيقي.

### 5. Non-Repudiation (عدم الإنكار)

لا يمكن للمرسل أو المستقبل إنكار العملية.

---

# ⚠️ 2. Attack Formula

```
Attack = Motive + Method + Vulnerability
```

### ✔️ Motive (الدافع)

* سرقة بيانات
* تعطيل خدمات
* أهداف سياسية أو دينية

### ✔️ Method (الطريقة)

أدوات وتقنيات الاختراق

### ✔️ Vulnerability (الثغرة)

نقطة ضعف مثل:

* كلمة سر ضعيفة
* برنامج غير محدث
* بورت مفتوح

---

# 🧨 3. Types of Attacks

## 🔎 Passive Attacks

* مراقبة فقط بدون تعديل
* مثال: eavesdropping  ,  Sniffing

## 💥 Active Attacks

* تعديل أو تخريب
* مثال:

  * DoS
  * MitM
  * SQL Injection

## 👀 Close-in Attacks

* قرب فيزيائي من الهدف
* مثال:

  * Social Engineering
  * Shoulder Surfing
  * dumpster diving

## 🏢 Insider Attacks

* من داخل المؤسسة
* مثال: موظف يسرق بيانات
* Examples: Theft of physical devices, keyloggers, backdoors, malware.

## 📦 Distribution Attacks

* التلاعب قبل تثبيت النظام

---

# 🧑‍💻 4. Phases of Hacking

## المرحلة 1: Footprinting

جمع معلومات عن الهدف

## المرحلة 2: Scanning

فحص البورتات والثغرات

## المرحلة 3: Enumeration

استخراج بيانات مثل المستخدمين

## المرحلة 4: Vulnerability Analysis

تحديد نقاط الضعف

---

## 🔓 System Hacking Steps

5. Gaining Access → دخول النظام
6. Escalating Privileges → زيادة الصلاحيات
7. Maintaining Access → الحفاظ على الوصول
8. Clearing Logs → إخفاء الآثار

---

# ⚔️ 5. Cyber Kill Chain

1. Reconnaissance → جمع معلومات
2. Weaponization → إعداد الهجوم
3. Delivery → إرسال الهجوم
4. Exploitation → تنفيذ الكود
5. Installation → تثبيت malware
6. Command & Control → التحكم بالجهاز
7. Actions → تنفيذ الهدف

---

# ⚖️ 6. Vulnerability, Threat, Risk

### Vulnerability (ثغرة)

ضعف في النظام
➡️ مثال: Weak password

### Threat (تهديد)

جهة تستغل الثغرة
➡️ مثال: Hacker

### Risk (خطر)

```
Risk = Probability × Impact
```

---

# 🧠 7. What is Hacking?

هو استغلال الثغرات للحصول على:

* وصول غير مصرح
* تعديل الأنظمة
* سرقة البيانات

---

# 👨‍💻 8. Who is a Hacker?

شخص لديه مهارات:

* برمجة
* فهم الشبكات
* تحليل الأنظمة

### دوافعه:

* تعلم
* تحدي
* ربح مادي
* أهداف سياسية

---

# 🕶️ 9. Hacker Classes

## ⚫ Black Hat

* اختراق ضار

## ⚪ White Hat

* اختراق أخلاقي (حماية)

## ⚙️ Gray Hat

* بين الاثنين

## 💣 Suicide Hacker

* لا يهتم بالعواقب

## 🧰 Script Kiddie

* يستخدم أدوات جاهزة

## 🧨 Cyber Terrorist

* لنشر الخوف

## 🏛️ State-Sponsored

* يعمل لصالح دولة

## ✊ Hacktivist

* أهداف سياسية

## 🧑‍🤝‍🧑 Hacker Teams

* فرق منظمة

## 🏭 Industrial Spy

* تجسس صناعي

## 🏢 Insider

* من داخل المؤسسة

## 💰 Criminal Syndicate

* عصابات إلكترونية

---

# 🧪 10. Lab Environment

## 🐉 Kali Linux

نظام مخصص للاختبار الأمني يحتوي على:

* أدوات الشبكات
* اختبار المواقع
* كسر كلمات المرور

## 🖥️ Virtualization

يسمح بـ:

* تشغيل أكثر من نظام
* إنشاء شبكة وهمية
* عزل التجارب

---

# 🧱 Lab Architecture

* جهاز الطالب (Host)
* Kali Linux (Attacker)
* جهاز ضعيف (Victim)
* شبكة داخلية فقط

---

# ⚠️ Why Isolation is Important?

بدون عزل:

* ممكن تعمل Scan على الإنترنت الحقيقي
* مشاكل قانونية
* خطر على الجامعة

✔️ الحل:
بيئة افتراضية آمنة للتجربة

---

# ✅ Conclusion

هذا اللاب يضع الأساس لفهم:

* كيف تتم الهجمات
* كيف نحمي الأنظمة
* الفرق بين أنواع الهاكرز

---

## 💡 Tip

ابدأ تفكر دائمًا كـ **Defender مش Attacker** 😉
