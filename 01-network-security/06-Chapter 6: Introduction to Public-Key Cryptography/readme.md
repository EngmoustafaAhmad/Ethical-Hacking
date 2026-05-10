# Chapter 6: Introduction to Public-Key Cryptography

This repository contains a professional overview of the transition from symmetric to asymmetric cryptographic systems, based on the instructional materials by **Dr. Safi Ibrahim**.

---

## 📖 Overview
[cite_start]Cryptography is the cornerstone of modern digital security[cite: 1, 2]. [cite_start]While symmetric systems have served as the historical standard [cite: 39][cite_start], the advent of public-key (asymmetric) cryptography in 1976—pioneered by Diffie, Hellman, and Merkle—addressed critical scalability and trust issues in open networks[cite: 64, 83].

## 🔑 Core Concepts

### Symmetric Cryptography (Secret-Key)
[cite_start]In symmetric systems, a single secret key $K$ is shared between parties[cite: 28].
* [cite_start]**Mechanism**: The same key is used for both encryption $e_K(x)$ and decryption $d_K(y)$[cite: 28].
* [cite_start]**Functionality**: Encryption and decryption are very similar or even identical functions[cite: 29].
* [cite_start]**Analogy**: A physical safe where both Alice and Bob possess an identical key[cite: 35, 36].
* **Limitations**:
    * [cite_start]**Key Distribution**: The secret key must be transported through a secure channel[cite: 40].
    * [cite_start]**Scalability**: In a network of $n$ users, $\frac{n \cdot (n-1)}{2}$ individual keys are required[cite: 40, 44].
    * [cite_start]**Non-repudiation**: Since keys are identical, a user can deny an action, claiming the other party fabricated the message[cite: 48, 49].

### Asymmetric Cryptography (Public-Key)
[cite_start]Asymmetric systems "split" the key into a mathematically linked pair[cite: 67].
* [cite_start]**Key Pair**: Consists of a **Public Key** ($K_{pub}$) for encryption and a **Secret (Private) Key** ($K_{pr}$) for decryption[cite: 70, 71].
* [cite_start]**The Mailbox Principle**: Anyone can drop a letter into the slot (public encryption), but only the owner with the correct key can open the box (private decryption) [cite: 61-63].
* [cite_start]**Advantages**: Solves the key distribution problem and provides mechanisms for digital signatures[cite: 83, 85].

---

## 🛠 Practical Implementation

### The Hybrid Protocol
[cite_start]Public-key algorithms are computationally intensive and roughly **1000 times slower** than symmetric algorithms[cite: 85, 95]. [cite_start]Modern systems use a hybrid approach to maintain performance[cite: 86]:

1.  [cite_start]**Asymmetric Phase**: Used for secure key exchange and digital signatures[cite: 86].
2.  [cite_start]**Symmetric Phase**: A fast cipher (like AES) uses the exchanged key to encrypt the actual bulk data[cite: 86, 87].

### Hard Mathematical Problems
[cite_start]Security relies on one-way functions that are easy to compute but computationally infeasible to invert[cite: 89]. [cite_start]These are based on three main families[cite: 90]:
* [cite_start]**Integer Factoring**: Finding prime factors of a composite integer (e.g., RSA)[cite: 90].
* [cite_start]**Discrete Logarithm (DL)**: Finding $x$ such that $a^x = y \pmod m$ (e.g., Diffie-Hellman, DSA)[cite: 90].
* [cite_start]**Elliptic Curve (EC)**: A generalization of the discrete logarithm problem offering high security with shorter keys[cite: 90].

---

## 🛡 Security Levels
[cite_start]Key lengths vary significantly across families to achieve equivalent security strengths[cite: 91].

| Security Level | Symmetric | ECC (Elliptic Curve) | RSA / DL |
| :--- | :--- | :--- | :--- |
| **Short Term** | 64 Bit | 128 Bit | [cite_start]$\approx$ 700 Bit [cite: 91] |
| **Medium** | 80 Bit | 160 Bit | [cite_start]$\approx$ 1024 Bit [cite: 91] |
| **Long Term** | 128 Bit | 256 Bit | [cite_start]$\approx$ 3072 Bit [cite: 91] |


# Chapter 6: Introduction to Public-Key Cryptography (Part 1 & 2)

This repository contains a professional overview of the transition from symmetric to asymmetric cryptographic systems, based on the instructional materials by **Dr. Safi Ibrahim**.

---

## 📖 Overview
[cite_start]Cryptography is the cornerstone of modern digital security[cite: 39]. [cite_start]While symmetric systems have served as the historical standard [cite: 39][cite_start], the advent of public-key (asymmetric) cryptography in 1976—pioneered by Diffie, Hellman, and Merkle—addressed critical scalability and trust issues in open networks[cite: 64].

## 🔑 Core Concepts

### Symmetric Cryptography (Secret-Key)
[cite_start]In symmetric systems, a single secret key $K$ is shared between parties[cite: 28].
* [cite_start]**Mechanism**: The same key is used for both encryption $e_K(x)$ and decryption $d_K(y)$[cite: 28].
* [cite_start]**Functionality**: Encryption and decryption are very similar or even identical functions[cite: 29].
* [cite_start]**Analogy**: A physical safe where both Alice and Bob possess an identical key[cite: 35, 36].
* **Limitations**:
    * [cite_start]**Key Distribution**: The secret key must be transported through a secure channel[cite: 40].
    * [cite_start]**Scalability**: In a network of $n$ users, $\frac{n \cdot (n-1)}{2}$ individual keys are required[cite: 44].
    * [cite_start]**Non-repudiation**: Since keys are identical, a user can deny an action, claiming the other party fabricated the message[cite: 48, 49].

### Asymmetric Cryptography (Public-Key)
[cite_start]Asymmetric systems "split" the key into a mathematically linked pair[cite: 67].
* [cite_start]**Key Pair**: Consists of a **Public Key** ($K_{pub}$) for encryption and a **Secret (Private) Key** ($K_{pr}$) for decryption[cite: 69, 70, 71].
* [cite_start]**The Mailbox Principle**: Anyone can drop a letter into the slot (public encryption), but only the owner with the correct key can open the box (private decryption)[cite: 61, 62, 63].
* [cite_start]**Advantages**: Solves the key distribution problem and provides mechanisms for digital signatures[cite: 83, 85].

---

## 🛠 Practical Implementation

### The Hybrid Protocol
[cite_start]Public-key algorithms are computationally intensive and roughly **1000 times slower** than symmetric algorithms[cite: 85, 95]. [cite_start]Modern systems use a hybrid approach to maintain performance[cite: 86]:

1.  [cite_start]**Asymmetric Phase**: Used for secure key exchange and digital signatures[cite: 86].
2.  [cite_start]**Symmetric Phase**: A fast cipher (like AES) uses the exchanged key to encrypt the actual bulk data[cite: 86, 87].

### Hard Mathematical Problems
[cite_start]Security relies on one-way functions that are easy to compute but computationally infeasible to invert[cite: 89]. [cite_start]These are based on three main families[cite: 90]:
* [cite_start]**Integer Factoring**: Finding prime factors of a composite integer (e.g., RSA)[cite: 90].
* [cite_start]**Discrete Logarithm (DL)**: Finding $x$ such that $a^x = y \pmod m$ (e.g., Diffie-Hellman, DSA)[cite: 90].
* [cite_start]**Elliptic Curve (EC)**: A generalization of the discrete logarithm problem offering high security with shorter keys[cite: 90].

---

## 🛡 Security Levels
[cite_start]Key lengths vary significantly across families to achieve equivalent security strengths[cite: 91].

| Security Level | Symmetric | ECC (Elliptic Curve) | RSA / DL |
| :--- | :--- | :--- | :--- |
| **Short Term** (hours/days) | 64 Bit | 128 Bit | $\approx$ 700 Bit |
| **Medium** | 80 Bit | 160 Bit | $\approx$ 1024 Bit |
| **Long Term** | 128 Bit | 256 Bit | $\approx$ 3072 Bit |

> [cite_start][cite: 91]

> [!CAUTION]
> [cite_start]The existence of quantum computers would likely render RSA, DL, and ECC obsolete, though they are estimated to be at least 2-3 decades away[cite: 91, 92].

---
*Reference: Ibrahim, S. "Chapter 6 - Introduction to Public-Key Cryptography."*


> [!CAUTION]
> [cite_start]The existence of quantum computers would likely render RSA, DL, and ECC obsolete, though they are estimated to be at least 2-3 decades away[cite: 91].

---
[cite_start]*Reference: Ibrahim, S. "Chapter 6 - Introduction to Public-Key Cryptography"[cite: 1, 2].*
