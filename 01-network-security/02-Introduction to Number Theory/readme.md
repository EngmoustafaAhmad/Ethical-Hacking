# 🔢 Introduction to Number Theory

## 📘 Overview

This module introduces the mathematical foundation used in **cryptography**, including divisibility, modular arithmetic, prime numbers, and important theorems like **Fermat’s Little Theorem** and **Euler’s Theorem**.

---

## 🔹 1. Divisibility

We say **b divides a** if:

```
a = m × b
```

* Notation: `b | a`
* Example:

  * 3 | 12 ✔️
  * 5 | 12 ❌

### 📌 Key Notes

* If `b | a` → no remainder
* Divisors of 24:

  ```
  1, 2, 3, 4, 6, 8, 12, 24
  ```

---

## 🔹 2. Properties of Divisibility

* If `a | b` and `b | c` → then `a | c`
* If `a | b` and `a | c` → then:

  ```
  a | (mb + nc)
  ```
* Any number divides 0
* If `a | b` and `b | a` → then `a = ±b`

---

## 🔹 3. Division Algorithm

For any integers `a` and `n`:

```
a = qn + r
0 ≤ r < n
```

* `q` = quotient
* `r` = remainder

---

## 🔹 4. Greatest Common Divisor (GCD)

```
gcd(a, b)
```

هو أكبر عدد يقسم `a` و `b`

### 📌 Examples

```
gcd(60, 24) = 12
gcd(a, 0) = |a|
```

### 📌 Relatively Prime

إذا:

```
gcd(a, b) = 1
```

---

## 🔹 5. Euclidean Algorithm

طريقة سريعة لحساب GCD:

```
gcd(a, b) = gcd(b, a mod b)
```

### ✅ Example

```
gcd(973, 301)

973 mod 301 = 70
301 mod 70 = 21
70 mod 21 = 7
21 mod 7 = 0

→ gcd = 7
```

✔️ Efficient حتى مع الأرقام الكبيرة

---

## 🔹 6. Modular Arithmetic

### 📌 التعريف

```
a ≡ r mod m
```

يعني:

```
m | (a - r)
```

### 📌 Examples

```
12 ≡ 3 mod 9
34 ≡ 7 mod 9
-7 ≡ 2 mod 9
```

---

## 🔹 7. Properties of Modular Arithmetic

### ✔️ العمليات

```
(a + b) mod m
(a × b) mod m
```

### ✔️ Important Rule

يمكنك تقليل الأرقام أثناء الحساب:

```
(a × b) mod m = [(a mod m)(b mod m)] mod m
```

---

## 🔹 8. Modular Inverse

نبحث عن:

```
a⁻¹ mod m
```

حيث:

```
a × a⁻¹ ≡ 1 mod m
```

### 📌 شرط وجوده:

```
gcd(a, m) = 1
```

### ✅ Example

```
7⁻¹ mod 9 = 4
```

---

## 🔹 9. Prime Numbers

* عدد أولي → يقبل القسمة فقط على:

  * 1
  * نفسه

### 📌 مثال

```
2, 3, 5, 7, 11
```

---

## 🔹 10. Fundamental Theorem of Arithmetic

أي عدد يمكن كتابته كحاصل ضرب أعداد أولية:

```
a = p1^a1 × p2^a2 × ...
```

---

## 🔹 11. Euler’s Totient Function φ(n)

تمثل عدد الأعداد التي:

* أصغر من n
* و coprime مع n

### ✅ Examples

```
φ(5) = 4
φ(6) = 2
```

### 📌 Formula

إذا:

```
n = p × q
```

```
φ(n) = (p - 1)(q - 1)
```

---

## 🔹 12. Fermat’s Little Theorem

إذا كان p عدد أولي:

```
a^(p-1) ≡ 1 mod p
```

### 📌 استخدام:

* إيجاد modular inverse
* أساس في RSA

---

## 🔹 13. Euler’s Theorem

تعميم لـ Fermat:

```
a^φ(m) ≡ 1 mod m
```

إذا:

```
gcd(a, m) = 1
```

---

## 🔐 14. لماذا مهم في Cybersecurity؟

Number Theory هو أساس:

* RSA Encryption
* Digital Signatures
* Key Exchange

---

## 🔥 15. Practical Insight (للـ Ethical Hacking)

| Concept            | Use             |
| ------------------ | --------------- |
| GCD                | Key generation  |
| Modular Arithmetic | Encryption      |
| Prime Numbers      | RSA             |
| Euler Function     | Key calculation |

---

## 📌 Summary

في هذا الفصل تعلمت:

* Divisibility
* GCD & Euclidean Algorithm
* Modular Arithmetic
* Prime Numbers
* Fermat & Euler Theorems

💡 هذا الفصل هو **الأساس الرياضي للتشفير**، وبدونه مش هتفهم:

* RSA
* Cryptography Algorithms
* Secure Communications

---
