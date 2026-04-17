# Types of encryption

Encryption is a core security control used to protect data. Security professionals should understand the main types of encryption, why key length matters, and common approved algorithms used in practice.

---

## Two main types of encryption

### Symmetric encryption

**Symmetric encryption** uses a **single secret key** to exchange information. Because the same key is used for encryption and decryption, both the sender and receiver must know the secret key to lock/unlock the cipher.

### Asymmetric encryption

**Asymmetric encryption** uses a **public and private key pair**:

- the **public key** encrypts data
- the **private key** decrypts data

The private key is only provided to users with authorized access.

---

## The importance of key length

Ciphers can be vulnerable to **brute force** attacks, which use trial-and-error to discover private information (like trying every combination on a lock).

In modern encryption, **longer key lengths** are generally more secure because they create more possible keys an attacker must try. A trade-off is performance: longer keys can mean **slower processing**, while shorter keys are faster but typically less secure.

Providing fast communication while keeping information safe is a balancing act.

---

## Approved algorithms (common examples)

Many web applications use a combination of symmetric and asymmetric encryption to balance user experience with safeguarding information.

### Symmetric algorithms

**Triple DES (3DES)** is a **block cipher** that converts plaintext to ciphertext in blocks. It builds on the older **DES** algorithm (early 1970s). DES produced 64-bit keys, but only **56 bits** are used for encryption. 3DES applies DES three times using three different 56-bit keys, resulting in an effective key length of **168 bits**.

Despite longer keys, many organizations are moving away from 3DES due to limitations on the amount of data that can be encrypted, but it may remain for backward compatibility.

**Advanced Encryption Standard (AES)** is one of the most secure symmetric algorithms widely used today. AES key sizes are **128**, **192**, or **256** bits. Keys of this size are considered safe from brute force attacks (for example, brute forcing AES-128 is estimated to take billions of years with modern computing).

### Asymmetric algorithms

**Rivest Shamir Adleman (RSA)** is named after its creators and was developed at MIT. RSA is one of the first widely used asymmetric algorithms that produces a public/private key pair. RSA uses longer key sizes—commonly **1,024**, **2,048**, or **4,096** bits—and is mainly used to protect highly sensitive data.

**Digital Signature Algorithm (DSA)** is a standard asymmetric algorithm introduced by NIST in the early 1990s. DSA commonly uses key lengths of **2,048** bits and is widely used as a complement to RSA in public key infrastructure (PKI).

---

## Generating keys (OpenSSL example)

Organizations must implement these algorithms by generating keys. One common tool is **OpenSSL**, an open-source command-line tool used to generate public/private keys and to verify digital certificates as part of **public key infrastructure (PKI)**.

**Note:** OpenSSL is only one option; other tools exist for generating keys using common algorithms.

In early 2014, OpenSSL disclosed a vulnerability called the **Heartbleed bug**, which exposed sensitive data in memory for websites and applications. The bug was patched later in 2014, highlighting the importance of using up-to-date software.

---

## Obscurity is not security (Kerckhoff’s principle)

Cryptography should be designed so that the security of the system does **not** depend on keeping the algorithm secret—only the private key must remain secret.

According to **Kerckhoff’s principle**, all algorithm details (except the private key) can be knowable without sacrificing security. For example, AES is publicly documented but remains secure.

Custom “secret” encryption algorithms are often cracked quickly once made public.

**Pro tip:** A cryptographic system should not be considered secure if it requires secrecy around how it works.

---

## Encryption is everywhere (and often required)

Organizations use both symmetric and asymmetric encryption—often together—to balance security and performance.

Example: a website might use **asymmetric** encryption to secure small, important blocks of data (like usernames and passwords during login). After login, the session often switches to **symmetric** encryption for speed.

Encryption is also increasingly required by law. Regulations like **FIPS 140-3** and **GDPR** outline expectations for collecting, using, and handling data. Compliance helps demonstrate responsible data handling.

---

## Key takeaways

- **Symmetric** encryption uses one secret key.
- **Asymmetric** encryption uses a public/private key pair.
- **Longer keys** generally improve resistance to brute force but can reduce performance.
- Common algorithms: **3DES**, **AES**, **RSA**, **DSA**.
- Tools like **OpenSSL** support key generation and PKI; keep software up to date (e.g., Heartbleed history).
- Encryption supports security goals and compliance requirements.

