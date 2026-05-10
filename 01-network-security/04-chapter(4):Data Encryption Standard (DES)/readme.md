# Data Encryption Standard (DES)

## What is DES?
DES (Data Encryption Standard) is a symmetric block cipher used for encrypting data.

- Developed by IBM
- Standardized in 1977
- Uses the same key for encryption and decryption

---

# DES Features

| Feature | Value |
|---|---|
| Block Size | 64 bits |
| Key Size | 56 bits |
| Structure | Feistel Network |
| Number of Rounds | 16 |
| Cipher Type | Block Cipher |

---

# Block Cipher

A block cipher encrypts data in fixed-size blocks.

DES:
- Takes 64-bit plaintext
- Produces 64-bit ciphertext

Example:

```text
HELLO -> Binary -> Encrypted Ciphertext
```
Confusion and Diffusion

DES is based on two important cryptography principles introduced by Claude Shannon.

## 1. Confusion

Makes the relationship between:

plaintext
ciphertext
key

difficult to understand.

DES achieves confusion using:

S-Boxes
## 2. Diffusion

Spreads the effect of one plaintext bit across many ciphertext bits.

If one bit changes:

many output bits change

DES achieves diffusion using:

permutations
expansion functions
DES Structure

DES uses a Feistel Network.

Encryption steps:
```
Plaintext
   ↓
Initial Permutation (IP)
   ↓
16 Rounds
   ↓
Final Permutation (IP⁻¹)
   ↓
Ciphertext
Initial Permutation (IP)
```
DES first rearranges bits using a permutation table.

Purpose:

Increase diffusion
Prepare data for processing

No encryption happens here.
Only bit rearrangement.

## Splitting the Data

After IP:
```
64 bits
↓
L0 = Left Half (32 bits)
R0 = Right Half (32 bits)
DES Round Operation
```
Each round performs:
```
Li = Ri-1

Ri = Li-1 XOR f(Ri-1, Ki)
```
Where:

Ki = Round subkey
f() = DES f-function
The f-Function

The f-function is the core of DES security.

It contains 4 steps.

### Step 1 — Expansion (E)

Expands:
```
32 bits → 48 bits
```
Purpose:

Improve diffusion
Prepare for XOR with key

### Step 2 — XOR with Round Key

The expanded data is XORed with:

48-bit subkey
```
Expanded Data XOR Round Key
```
Purpose:

Mix plaintext with secret key
### Step 3 — S-Boxes

DES contains:

8 S-Boxes

Each S-Box:
```
Input: 6 bits
Output: 4 bits
```
Purpose:

Add nonlinearity
Resist attacks
Why S-Boxes Are Important

Without S-Boxes:

DES becomes predictable
Easier to attack mathematically

S-Boxes provide:

Security
Nonlinearity

### Step 4 — Permutation P

After S-Boxes:

Bits are rearranged again

Purpose:

Spread bits across future rounds
Improve diffusion
Key Schedule

DES generates:

16 subkeys

Process:

Remove parity bits
Split key into halves
Rotate halves
Apply PC-2 permutation

Result:
```
K1, K2, K3 ... K16
```
Each subkey:

48 bits
Why DES Uses 16 Rounds

More rounds provide:

Better security
Better diffusion

After many rounds:

Every ciphertext bit depends on many plaintext bits and key bits

This creates:

Avalanche Effect

Changing one input bit changes many output bits.

DES Decryption

DES decryption uses:

The same algorithm as encryption

Difference:

Subkeys are used in reverse order

Encryption:
```
K1 → K2 → K3 → ... → K16
```
Decryption:
```
K16 → K15 → ... → K1
```
Security Problems of DES

Main issue:

Small key size (56 bits)

Modern computers can:

brute-force DES keys

Therefore:

DES is no longer secure today
Cryptanalysis Attacks

DES resisted:

Differential Cryptanalysis
Linear Cryptanalysis

This proved:

DES design was strong

But:

brute-force attacks eventually broke DES
Triple DES (3DES)

3DES improves DES by encrypting data three times.
```
Encrypt → Decrypt → Encrypt
```
Advantages:

Stronger security
Effective key length ≈ 112 bits

Used in:

Banking systems
Legacy applications
# DES vs AES

| DES | AES |
|---|---|
| 56-bit key | 128 / 192 / 256-bit key |
| Old standard | Modern standard |
| Weak today | Very secure |
| 64-bit block size | 128-bit block size |
| Slower and outdated | Faster and stronger |

AES replaced DES in 2000.

AES replaced DES in 2000.

Important Concepts

DES uses:

Symmetric encryption
Feistel Network
XOR operations
S-Boxes
Permutations
16 rounds
Most Important Exam Topics

Focus on:

DES structure
Feistel rounds
f-function
S-Boxes
Key schedule
DES vs 3DES
Why DES became insecure
Simple Memory Formula
```
Permutation + XOR + S-Boxes + Multiple Rounds
= Strong Encryption
```
Most important component:

S-Boxes = Security + Nonlinearity





