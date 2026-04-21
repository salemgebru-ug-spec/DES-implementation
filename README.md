# 🔐 DES Encryption Implementation in Python

This project is a Python implementation of the Data Encryption Standard (DES), a symmetric-key block cipher used for secure data encryption.

---

## 📌 Features

* 64-bit block encryption
* Full DES key schedule (16 subkeys)
* Initial and final permutations
* Feistel structure with 16 rounds
* Expansion, S-box substitution, and P-box permutation
* Bitwise XOR operations

---

## 🛠️ How It Works

The DES algorithm follows these steps:

1. Apply **Initial Permutation (IP)** to the plaintext
2. Split into left (L) and right (R) halves
3. Perform **16 rounds** of:

   * Expansion (32 → 48 bits)
   * XOR with subkey
   * S-box substitution
   * P-box permutation
   * XOR with left half
   * Swap halves
4. Perform final swap
5. Apply **Final Permutation (IP⁻¹)**

---

## 🔑 Key Schedule

* Original key: 64 bits (56 effective bits)
* Apply **PC-1** → 56 bits
* Split into two halves (C, D)
* Perform left shifts
* Apply **PC-2** → generate 16 subkeys

---

## ▶️ How to Run

1. Make sure you have Python installed (Python 3.x)

2. Run the script:

```bash
python your_file_name.py
```

3. Output will display:

* Generated subkeys
* Encryption process
* Final ciphertext

---

## 📥 Input Example

```python
plaintext = "0001001000110100010101100111100010011010101111001101111011110001"
key       = "0001001100110100010101110111100110011011101111001101111111110001"
```

---

## 📤 Output

```text
Ciphertext: <generated binary output>
```

---

## 📚 Concepts Used

* Feistel Network
* Bitwise Operations
* Substitution-Permutation Network
* Symmetric Key Cryptography

---

## ⚠️ Note

DES is now considered **insecure** due to its small key size (56 bits) and is not used in modern secure systems. This project is for educational purposes.

---

## 👩‍💻 Authors

Lydia Yoseph

Meseret Ghebiresilassie 

Mikiyas Fasil

Salem Gebru

Computer Science Department Students, Addis Ababa University
