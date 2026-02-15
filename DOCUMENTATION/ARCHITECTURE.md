# System Architecture - VOID-CRYPT 🛡️

## 1. Overview
VOID-CRYPT is engineered as a zero-trust cryptographic utility. The architecture follows a modular approach to separate the user interface from the core cryptographic engine, ensuring that security primitives remain isolated and verifiable.

## 2. Cryptographic Pipeline
The tool implements an **Authenticated Encryption with Associated Data (AEAD)** flow:

1. **Entropy Injection:** Every encryption operation starts with a 12-byte cryptographically secure random Nonce.
2. **KDF (Key Derivation Function):** Uses PBKDF2 with SHA-256. 
   - **Salt:** 64-bit static salt (Production versions should implement dynamic salts).
   - **Iterations:** 100,000 passes to increase the cost of offline GPU-based brute-force attacks.
3. **Cipher Core:** AES-256 in Galois/Counter Mode (GCM). This provides:
   - **Confidentiality:** Data is unreadable without the key.
   - **Integrity:** Any bit-flip in the ciphertext will trigger an authentication failure.

## 3. Data Sanitization Protocol (Anti-Forensics)
The shredding engine is designed based on the **DoD 5220.22-M** standard:
- **Pass 1:** Overwrite with zeros.
- **Pass 2:** Overwrite with ones.
- **Pass 3:** Overwrite with random noise.
- **Verification:** The file is flushed to the disk buffer before the final system unlink.
