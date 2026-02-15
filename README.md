# 🛡️ VOID-CRYPT: Advanced Forensic Encryption Suite

![Python](https://img.shields.io/badge/Python-3.8+-blue?style=for-the-badge&logo=python)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)
![Security](https://img.shields.io/badge/Security-AES--256--GCM-red?style=for-the-badge)
![Standard](https://img.shields.io/badge/Compliance-DoD--5220.22--M-orange?style=for-the-badge)

**VOID-CRYPT** is a high-performance, command-line security utility engineered for cryptographically secure data lifecycle management. It bridges the gap between **Military-Grade Encryption** and **Anti-Forensic Data Destruction**.

---

## ⚡ Key Capabilities

| Feature | Technical Implementation | Security Standard |
| :--- | :--- | :--- |
| **Data Locking** | AES-256-GCM (Authenticated Encryption) | NIST Compliant |
| **Key Derivation** | PBKDF2 with HMAC-SHA256 (100k Iterations) | FIPS 140-2 |
| **Anti-Forensics** | 3-Pass Cryptographic Overwrite Engine | DoD 5220.22-M |
| **Integrity Check** | AEAD Tag Verification | Zero-Trust |

---

## 🛠️ Security Architecture



### 🔒 Authenticated Encryption (AEAD)
Unlike standard AES, VOID-CRYPT uses **Galois/Counter Mode (GCM)**. This ensures that if even a single bit of the encrypted file is tampered with by an attacker, the tool will detect it and refuse to decrypt, preventing "padding oracle" and "bit-flipping" attacks.

### 🌪️ Forensic Sanitization (Shredding)
Standard file deletion only removes the pointer to the data. VOID-CRYPT's **Shredder Engine** performs deep-level byte-stream manipulation:
1.  **Bit-Level Nullification:** Overwrites data with `0x00`.
2.  **Saturation:** Overwrites with `0xFF`.
3.  **Entropy Injection:** Final pass with high-entropy random bytes to neutralize residual magnetic traces.

---
![IMG_20260215_190431](https://github.com/user-attachments/assets/8045b64c-dafd-4a3b-8b9a-25d5cbfe75d0)
---

## 🚀 Quick Start

### 1. Clone & Install
```
git clone https://github.com/karndeepbaror/voidcrypt
cd voidcrypt
cd VOID-CRYPT
pip install -r requirements.txt
```

### 2. Execution
```
python voidcrypt.py
```

---


## 🤝 Contributing

We welcome contributions to strengthen the engine. Please check the Contributing Guidelines before submitting a Pull Request.

## 🌐 Join Our Cyber-Intelligence Community

<div align="center">
  <img src="https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png" width="100%">
  
  ### 🚀 **CONNECT WITH THE CRYPTONIC AREA**
  *Join a network of Security Researchers, Developers, and Ethical Hackers.*
  
  <br>
  
  [![WhatsApp Community](https://img.shields.io/badge/WhatsApp-Join%20Community-7289DA?style=for-the-badge&logo=whatsapp&logoColor=white)](https://whatsapp.com/channel/0029Vb6plDSBKfi3qGz2fq0f)
  [![Telegram](https://img.shields.io/badge/Telegram-Shadow%20Network-0088cc?style=for-the-badge&logo=telegram&logoColor=white)](https://t.me/CryptonicArea)
  
  <br>
  
  > **"Security is not a product, but a process. Be part of the evolution."**
  
 

  <img src="https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png" width="100%">
</div>

---


## 📜 License & Legal
This project is licensed under the MIT License.
Disclaimer: VOID-CRYPT is intended for legal security auditing and personal privacy. The developer is not responsible for any misuse or data loss.

## 🔗 CONNECT WITH ME

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/karndeepbaror)
[![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/karndeepbaror)
[![Community](https://img.shields.io/badge/Community-FF5722?style=for-the-badge&logo=react&logoColor=white)](https://whatsapp.com/channel/0029Vb6plDSBKfi3qGz2fq0f)

**"In the world of zero-days, I build zero-trust."**
