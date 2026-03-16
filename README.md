# Cryptography Toolkit

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python) ![Cryptography](https://img.shields.io/badge/Cryptography-Classical%20%26%20Modern-purple) ![Status](https://img.shields.io/badge/Status-Active-brightgreen)

> Python implementations of classical ciphers, symmetric and asymmetric encryption, key exchange protocols, and an exploration of post-quantum cryptography concepts.

## Table of Contents
- [Overview](#overview)
- [Algorithms Implemented](#algorithms-implemented)
- [Technologies](#technologies)
- [Project Structure](#project-structure)
- [How to Run](#how-to-run)
- [Post-Quantum Notes](#post-quantum-notes)
- [Author](#author)

## Overview

This toolkit explores cryptographic algorithms from classical substitution ciphers to modern asymmetric encryption. Each implementation is accompanied by explanations of the underlying mathematical principles and security analysis.

## Algorithms Implemented

### Classical Ciphers
| Cipher | Type | Key Space |
|--------|------|----------|
| Caesar | Substitution | 26 keys |
| Vigenère | Polyalphabetic | Variable |
| Playfair | Digraph substitution | 25-char keyword |

### Symmetric Encryption
- **AES (Advanced Encryption Standard)** — CBC and ECB modes using `pycryptodome`
- **XOR cipher** — educational implementation with key reuse vulnerability demo

### Asymmetric Encryption
- **RSA** — key generation, encryption/decryption, digital signatures
- **Diffie-Hellman** — key exchange protocol simulation
- **ElGamal** — probabilistic public-key encryption

### Hashing & Integrity
- **SHA-256 / SHA-3** — message digests
- **HMAC** — message authentication codes
- **MD5 collision demo** — illustrating weaknesses

## Technologies

- **Language:** Python 3.x
- **Libraries:** `pycryptodome`, `hashlib`, `secrets`, `math`
- **Concepts:** Number theory, modular arithmetic, elliptic curves (intro)

## Project Structure

```
cryptography-toolkit/
├── classical/
│   ├── caesar.py
│   ├── vigenere.py
│   └── playfair.py
├── symmetric/
│   ├── aes_demo.py
│   └── xor_cipher.py
├── asymmetric/
│   ├── rsa.py
│   ├── diffie_hellman.py
│   └── elgamal.py
├── hashing/
│   ├── sha_demo.py
│   └── hmac_demo.py
├── post-quantum/
│   └── notes.md
└── README.md
```

## How to Run

```bash
git clone https://github.com/anastasia638/cryptography-toolkit.git
cd cryptography-toolkit
pip install pycryptodome

# Run RSA demo
python3 asymmetric/rsa.py

# Run Caesar cipher
python3 classical/caesar.py
```

## Post-Quantum Notes

The `post-quantum/notes.md` file contains a research overview of:
- **Lattice-based cryptography** (CRYSTALS-Kyber, CRYSTALS-Dilithium)
- **NIST PQC standardization** status
- **Why current RSA/ECC are vulnerable** to quantum attacks (Shor's algorithm)

## Author

**Meriem Silmi** — Computer Science Student, France  
Licence 3 | Université Lyon 1  
Interests: Cryptography, Network Security, Post-Quantum Cryptography
