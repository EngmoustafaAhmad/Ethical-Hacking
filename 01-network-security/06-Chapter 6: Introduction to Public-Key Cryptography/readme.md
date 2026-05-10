# Chapter 6: Introduction to Public-Key Cryptography

[cite_start]This document summarizes the fundamental concepts of asymmetric cryptography as presented by Dr. Safi Ibrahim[cite: 1, 2].

## 1. Symmetric Cryptography Revisited
Symmetric systems (secret-key cryptography) rely on a single shared key[cite: 28].
  **Key Usage**: The same secret key $K$ is used for both encryption and decryption[cite: 28].
  **Functionality**: Encryption and decryption are very similar or even identical functions[cite: 29].
  **Analogy**: A safe with a strong lock where only Alice and Bob have a copy of the key[cite: 35].
* **Shortcomings**:
    **Key Distribution**: The secret key must be transported securely[cite: 40].
    **Number of Keys**: In a network of $n$ users, $\frac{n \cdot (n-1)}{2}$ keys are required[cite: 41, 44].
    **Non-repudiation**: Since keys are identical, one party can claim the other fabricated a message[cite: 48, 49].

## 2. Principles of Asymmetric Cryptography
Asymmetric cryptography introduced the "mailbox" principle: everyone can drop a letter, but only the owner has the key to open the box[cite: 61, 63].
**Split Keys**: The system uses a key pair consisting of a **Public Key** ($K_{pub}$) for encryption and a **Secret (Private) Key** ($K_{pr}$) for decryption[cite: 67, 69, 70].
**Origin**: First published in 1976 by Whitfield Diffie, Martin Hellman, and Ralph Merkle[cite: 64].
**Analogy**: A safe with a public lock (for deposits) and a private lock (for retrieval)[cite: 74, 79].

## 3. Practical Aspects and Hybrid Systems
[cite_start]Public-key algorithms are computationally intensive and roughly **1000 times slower** than symmetric algorithms[cite: 85, 95].
* **Security Mechanisms**:
    * [cite_start]**Key Distribution**: Exchange keys without a pre-shared secret (e.g., Diffie-Hellman)[cite: 85].
    * [cite_start]**Digital Signatures**: Provide message integrity and non-repudiation (e.g., RSA, DSA)[cite: 85].
    * [cite_start]**Identification**: Accomplished via challenge-response protocols[cite: 85].
* [cite_start]**Hybrid Systems**: In practice, asymmetric algorithms are used for key exchange, while fast symmetric ciphers (like AES) handle bulk data encryption[cite: 86, 87].

## 4. Mathematical Foundations
[cite_start]Public-key algorithms are based on "one-way functions" that are easy to compute but infeasible to invert[cite: 89]. [cite_start]These are grouped into three main families[cite: 90]:
1. [cite_start]**Factoring Integers**: Finding prime factors of a composite integer (RSA)[cite: 90].
2. [cite_start]**Discrete Logarithm**: Finding $x$ such that $a^x = y \pmod m$ (Diffie-Hellman, Elgamal, DSA)[cite: 90].
3. [cite_start]**Elliptic Curves (EC)**: A generalization of the discrete logarithm problem (ECDH, ECDSA)[cite: 90].

## 5. Security Levels and Key Lengths
| Symmetric | ECC | RSA / DL | Security Level |
| :--- | :--- | :--- | :--- |
| 64 Bit | 128 Bit | $\approx$ 700 Bit | [cite_start]Short term (hours/days) [cite: 91] |
| 80 Bit | 160 Bit | $\approx$ 1024 Bit | [cite_start]Medium security [cite: 91] |
| 128 Bit | 256 Bit | $\approx$ 3072 Bit | [cite_start]Long term security [cite: 91] |

[cite_start]*Note: The existence of quantum computers would likely end the effectiveness of ECC, RSA, and DL[cite: 91, 92].*
