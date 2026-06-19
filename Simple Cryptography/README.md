# 🔐 Cryptography Fundamentals

<div align="center">

![Cryptography](https://img.shields.io/badge/Cybersecurity-Cryptography-blue?style=for-the-badge\&logo=hackaday)
![Learning](https://img.shields.io/badge/Learning-Journey-green?style=for-the-badge)
![Encryption](https://img.shields.io/badge/Encryption-Classical%20Ciphers-orange?style=for-the-badge)

### 📚 Cybersecurity Learning Journey

*"Protecting information through encryption and secure communication."*

</div>

---

## 🎯 Overview

Cryptography is the practice of securing information by transforming readable data (**plaintext**) into an unreadable format (**ciphertext**).

It plays a vital role in cybersecurity by providing:

* 🔒 Confidentiality
* ✅ Integrity
* 👤 Authentication
* 📝 Non-Repudiation

---

## 🛡️ What is Cryptography?

```text
Plaintext
    │
    ▼
Encryption Algorithm + Key
    │
    ▼
Ciphertext
    │
    ▼
Decryption Algorithm + Key
    │
    ▼
Plaintext
```

Example:

```text
HELLO
  ↓ Encryption
KHOOR
  ↓ Decryption
HELLO
```

---

# 📖 Classical Cryptographic Algorithms

This repository covers the following classical encryption techniques:

| Cipher                   | Type                 | Key             |
| ------------------------ | -------------------- | --------------- |
| Caesar Cipher            | Substitution         | Shift Number    |
| Playfair Cipher          | Digraph Substitution | Keyword         |
| Rail Fence Cipher        | Transposition        | Number of Rails |
| Row Transposition Cipher | Transposition        | Numeric Key     |

---

## 🔹 1. Caesar Cipher

### Description

The Caesar Cipher is a substitution cipher where each letter is shifted by a fixed number of positions.

### Formula

Encryption:

```text
C = (P + K) mod 26
```

Decryption:

```text
P = (C - K) mod 26
```

Where:

* P = Plaintext
* C = Ciphertext
* K = Shift Key

### Example

```text
Plaintext : HELLO
Key       : 3
Ciphertext: KHOOR
```

### Characteristics

✅ Simple to understand

✅ Easy to implement

❌ Vulnerable to brute-force attacks

---

## 🔹 2. Playfair Cipher

### Description

The Playfair Cipher encrypts pairs of letters (digraphs) instead of individual characters.

It uses a **5×5 matrix** generated from a keyword.

### Encryption Rules

### ➡️ Same Row

Replace each letter with the letter immediately to its right.

### ⬇️ Same Column

Replace each letter with the letter immediately below it.

### 🔲 Rectangle Rule

Replace each letter with the character at the opposite corner of the rectangle.

---

### Example Keyword

```text
KINGS
```

Generated Matrix:

```text
K I N G S
A B C D E
F H J L M
O P Q R T
U V W X Y
```

*(I and J share the same position.)*

### Example

```text
Plaintext : KAUSAR

Pairs:
KA | US | AR

Ciphertext:
AF | YK | DO

Final:
AFYKDO
```

### Characteristics

✅ More secure than Caesar Cipher

✅ Encrypts digraphs

❌ Still vulnerable to frequency analysis

---

## 🔹 3. Rail Fence Cipher

### Description

The Rail Fence Cipher is a transposition cipher that writes characters in a zigzag pattern.

### Example

```text
Plaintext : HELLOWORLD
Rails     : 3
```

Visual Pattern:

```text
H      O      L
  E  L  W  R   D
    L      O
```

Read row-wise:

```text
HOL
ELWRD
LO
```

Ciphertext:

```text
HOLELWRDLO
```

### Characteristics

✅ Simple transposition technique

✅ Rearranges positions rather than letters

❌ Weak against pattern analysis

---

## 🔹 4. Row Transposition Cipher

### Description

Characters are written row-wise into a table and read column-wise according to a numeric key.

### Example

```text
Plaintext : KAUSARRAMI
Key       : 3421
```

Table:

```text
3 4 2 1

K A U S
A R R A
M I X X
```

Column Reading Order:

```text
1 → Column 4
2 → Column 3
3 → Column 1
4 → Column 2
```

Ciphertext:

```text
SAXURXKAMARI
```

### Characteristics

✅ Stronger than simple substitution

✅ Uses positional rearrangement

❌ Key discovery breaks the cipher

---

# ⚔️ Quick Comparison

| Cipher            | Technique            | Security Level |
| ----------------- | -------------------- | -------------- |
| Caesar            | Letter Shifting      | Low            |
| Playfair          | Digraph Substitution | Medium         |
| Rail Fence        | Zigzag Transposition | Low            |
| Row Transposition | Column Rearrangement | Medium         |

---

## 🎯 Key Differences

### Caesar Cipher

* Changes individual letters
* Uses a shift key

### Playfair Cipher

* Encrypts letter pairs
* Uses a keyword matrix

### Rail Fence Cipher

* Rearranges character positions
* Uses rails

### Row Transposition Cipher

* Rearranges columns
* Uses a numeric key

---

## 🚨 Why Study Classical Ciphers?

Although these ciphers are no longer used for modern security, they help build foundational knowledge for understanding:

* Modern Encryption Algorithms
* Cryptanalysis Techniques
* Symmetric Cryptography
* Secure Communication Systems

---

## 📚 Learning Outcomes

After studying these ciphers, I learned:

✅ Difference between substitution and transposition ciphers

✅ How encryption and decryption work

✅ The importance of keys in cryptography

✅ Strengths and weaknesses of classical encryption techniques

✅ Foundations of modern cryptographic systems

---

### 🚀 Cybersecurity Journey

This project is part of my Cybersecurity Learning Journey where I document networking, cryptography, security concepts, tools, and hands-on labs while building a strong foundation in cybersecurity.
