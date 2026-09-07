# Practical 4: Cryptography for Data Privacy

## Aim

To understand the role of cryptography in protecting personal and sensitive data and to study how encryption, hashing, and digital signatures are used to provide confidentiality, integrity, authentication, and data protection.

## Introduction

Cryptography is the technique of protecting information by converting it into a form that unauthorized users cannot easily understand.

It is an important part of data privacy and cybersecurity because it helps protect information during storage and transmission.

The major security properties provided by cryptography are:

- **Confidentiality** – prevents unauthorized access to information.
- **Integrity** – ensures that data has not been modified or tampered with.
- **Authentication** – verifies the identity of a user or system.
- **Non-repudiation** – provides evidence that a particular party performed an action.

## Major Cryptographic Techniques

### 1. Symmetric Encryption

Symmetric encryption uses the **same secret key** for both encryption and decryption.

```text
Plaintext
    ↓
Encryption + Secret Key
    ↓
Ciphertext
    ↓
Decryption + Same Key
    ↓
Plaintext
```

**Example:** AES (Advanced Encryption Standard)

**Applications:**
- Database encryption
- File encryption
- Secure storage
- Protecting sensitive information

*The main challenge is securely sharing the secret key between communicating parties.*

### 2. Asymmetric Encryption

Asymmetric cryptography uses a pair of mathematically related keys:
- **Public Key** – can be shared with others.
- **Private Key** – must be kept secret.

```text
Public Key
    ↓
Encryption
    ↓
Ciphertext
    ↓
Private Key
    ↓
Decryption
    ↓
Original Data
```

**Examples:** RSA and ECC

**Applications:**
- Secure communication
- Key exchange
- Digital signatures
- Authentication

*Asymmetric cryptography helps solve key-distribution problems but is generally slower than symmetric encryption.*
### 3. Hashing

Hashing converts input data into a fixed-length value called a hash.

```text
Input Data
    ↓
Hash Function
    ↓
Hash Value
```

A secure cryptographic hash function is designed to make it computationally impractical to recover the original input from the hash.

**Examples:**
- SHA-256
- SHA-3

**Applications:**
- Data integrity verification
- Password protection
- File verification
- Digital signatures

> **Note:** Passwords should be protected using dedicated password-hashing algorithms such as Argon2, bcrypt, or scrypt rather than simply storing a SHA-256 hash.

### 4. Digital Signatures

A digital signature uses asymmetric cryptography to verify the authenticity and integrity of digital information.

```text
Message
   ↓
Hash Function
   ↓
Message Hash
   ↓
Private Key
   ↓
Digital Signature
```

The receiver can use the sender's public key to verify the signature.

**Applications:**
- Digital documents
- Software signing
- Digital certificates
- Secure communication
- Authentication

## Cryptography and Data Privacy

Cryptographic techniques protect data at different stages of its lifecycle:

| Data State / Purpose | Cryptographic Technique | Example |
|---|---|---|
| Data in Transit | Encryption | HTTPS/TLS |
| Data at Rest | Encryption | Encrypted database |
| Password Protection | Password Hashing | Argon2, bcrypt |
| Data Integrity | Hashing | File integrity verification |
| Authentication | Digital Signatures | Digital certificates |

## Example: LeetCode

For an online educational platform such as LeetCode, cryptographic technologies can help protect:

- User account information
- Login credentials
- Communication between users and servers
- Sensitive stored information
- Data transmitted over the internet

HTTPS/TLS helps protect information while it is being transmitted between a user's browser and the server.

Cryptographic protection is especially important when users access online services through public or untrusted networks.
## Privacy Risks Without Cryptography

Without appropriate cryptographic protection:

1. Attackers may intercept sensitive information.
2. Stored information may be exposed after unauthorized access.
3. Data may be modified without detection.
4. User credentials may be compromised.
5. Communication may become vulnerable to interception.
6. The authenticity of digital information may be difficult to verify.

## Recommended Security Practices

- Use modern and well-tested cryptographic algorithms.
- Use HTTPS/TLS to protect data in transit.
- Encrypt sensitive data stored on servers.
- Never store passwords in plain text.
- Use secure password-hashing algorithms with unique salts.
- Protect cryptographic keys using secure key-management practices.
- Regularly review and update cryptographic implementations.
- Avoid outdated or weak cryptographic algorithms.
- Limit access to encryption keys and sensitive data.

## Difference Between Encryption and Hashing

| Feature | Encryption | Hashing |
|---|---|---|
| Main Purpose | Protect confidentiality | Protect integrity / support secure password storage |
| Reversible | Yes, with the appropriate key | Designed to be one-way |
| Uses a Key | Usually | No secret key for ordinary hashing |
| Example | AES | SHA-256 |
| Example Use | Encrypting files | Integrity checking |

## Conclusion

Cryptography is a fundamental technology for data privacy and cybersecurity. Symmetric encryption provides efficient protection of data, asymmetric cryptography supports secure communication and authentication, hashing helps verify integrity and protect passwords when appropriate algorithms are used, and digital signatures provide authenticity and integrity.

Using appropriate cryptographic techniques can significantly reduce the risk of data exposure, unauthorized modification, and communication attacks.

**Overall Importance:** High

## References

- NIST Cryptography: https://www.nist.gov/cryptography
- NIST Cybersecurity: https://www.nist.gov/cybersecurity
- LeetCode Privacy Policy: https://leetcode.com/privacy/
- LeetCode Terms of Service: https://leetcode.com/terms/
- 
