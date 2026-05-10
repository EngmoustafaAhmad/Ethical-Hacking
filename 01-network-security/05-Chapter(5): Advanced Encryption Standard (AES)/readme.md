# Advanced Encryption Standard (AES) – Part 1

# Content

- Number Sets
- Algebraic Structures
  - Groups
  - Rings
  - Fields
- Finite Fields (Galois Fields)
- Extension Fields GF(2m)
- Arithmetic in GF(2m)

---

# Number Sets

| Symbol | Meaning |
|---|---|
| N | Natural Numbers |
| Z | Integers |
| Q | Rational Numbers |
| R | Real Numbers |
| C | Complex Numbers |
| Zn | {0,1,2,...,n−1} |
| Zn* | Non-zero elements in Zn |

---

# Algebraic Structure: Groups

A group is a set of elements with an operation that satisfies:

1. Closure
2. Associativity
3. Identity element
4. Inverse element

If:
```text
a ◦ b = b ◦ a
```

then the group is called:

Abelian Group (Commutative)
## Examples of Groups

Examples:
```
(Z, +)
(R, +)
(Z5, +)
(Z5*, ×)
```
Important theorem:
```
(Zn, +) forms a group
```
and
```
(Zp*, ×) forms a multiplicative group if p is prime
```
## Algebraic Structure: Rings

A ring contains:

Addition
Multiplication

Properties:

Addition forms an Abelian group
Multiplication is associative
Distributive law holds
```
a(b + c) = ab + ac
```
Examples:
```
(Z, +, ×)
(R, +, ×)
(Z5, +, ×)
```
## Algebraic Structure: Fields

A field is a ring where:

All non-zero elements have multiplicative inverses

A field supports:

Addition
Subtraction
Multiplication
Division

Examples:
```
R
Q
C
GF(5)
```

## Finite Fields (Galois Fields)

Finite fields are called:

Galois Fields (GF)

Notation:
```
GF(p)
```
Where:

p is prime

Example:
```
GF(5) = {0,1,2,3,4}
```
Arithmetic is performed modulo p.

### Important Theorem

A finite field exists only if:

m=p
n

Where:

p = prime number
n = positive integer

Examples:

GF(11)
GF(81)
GF(256)

Not possible:

GF(12)

because 12 is not a prime power.


## Prime Fields

Prime fields are written as:
```
GF(p)
```
Examples:
```
GF(2)
GF(5)
GF(7)
```
All arithmetic is done modulo p.

### Example: GF(2)

GF(2):

{0,1}

Addition modulo 2:

| A | B | A + B |
| - | - | ----- |
| 0 | 0 | 0     |
| 0 | 1 | 1     |
| 1 | 0 | 1     |
| 1 | 1 | 0     |

## Extension Fields GF(2m)

AES uses:

GF(2^8)

because:

256 elements
each element represented by 1 byte

Elements are represented as:

Polynomials

instead of normal integers.


## Polynomial Representation

Example polynomial:

A(x)=x3+x2+1

Binary representation:
```
1101
```
because coefficients are:
```
1x³ + 1x² + 0x + 1
```









## Addition in GF(2m)

Addition uses XOR.

Example:

(x
3
+x
2
+1)+(x
2
+x)=x
3
+x+1

Rules:

Same powers cancel out
Arithmetic is modulo 2
Multiplication in GF(2m)

## Polynomials are multiplied normally.

Then:

reduced modulo an irreducible polynomial

Example irreducible polynomial:

P(x)=x
4
+x+1

Example Multiplication

Given:

A(x)=x
3
+x
2
+1

and

B(x)=x
2
+x

## Intermediate multiplication:

C(x)=x
5
+x
3
+x
2
+x

After reduction modulo:

P(x)=x
4
+x+1

Final result:

A(x)B(x)≡x
3

## AES Irreducible Polynomial

AES uses:

P(x)=x
8
+x
4
+x
3
+x+1

This polynomial defines arithmetic in AES.

Inversion in GF(2m)

Every non-zero element has:

Multiplicative inverse

Meaning:

A(x)⋅A
−1
(x)=1

This operation is extremely important in:

## AES S-Box construction
Why GF(2^8) is Important in AES

AES operations:

SubBytes
MixColumns

all depend on arithmetic in:

GF(2^8)

This provides:

strong security
nonlinearity
resistance against attacks
Key Concepts to Remember
Groups
One operation
Identity + inverse
Rings
Addition + multiplication
Fields
Addition, subtraction, multiplication, division
Finite Fields
Limited number of elements
GF(2^8)
Used in AES
AES Uses Polynomial Arithmetic

instead of normal integer arithmetic.

Most Important Exam Topics

Focus on:

Difference between Group, Ring, and Field
GF(p)
GF(2m)
Polynomial arithmetic
XOR addition
Irreducible polynomial
Why AES uses GF(2^8)
Simple Memory Notes
Group  → One operation
Ring   → Two operations
Field  → Full arithmetic
AES works inside GF(2^8)
Addition in GF(2^m) = XOR
