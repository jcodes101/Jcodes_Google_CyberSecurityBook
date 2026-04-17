# Hash functions (origins, collisions, and secure password storage)

Hash functions are important controls in security strategies. Hashing is widely used for **authentication** and **non-repudiation** (the concept that the authenticity of information can’t be denied).

Hash functions are algorithms that produce a code that **can’t be decrypted**. They convert information into a **unique value** that can be used to determine **integrity**.

---

## Origins of hashing

Hash functions have existed since the early days of computing. They were originally created to quickly search for data.

These algorithms represent data of any size as small, **fixed-size** values (digests). A **hash table** is a data structure used to store and reference hash values, making it efficient for computers to reference data.

### MD5 (Message Digest 5)

One early hash function is **MD5**, developed in the early 1990s by Professor Ronald Rivest (MIT). It was designed to verify that a file sent over a network matched its source file.

MD5 converts data into a **128-bit** value. In practice, it is commonly displayed as a 32-character string. Any change to the source input produces a completely different hash output.

In general, longer hash values tend to be more secure. MD5’s 128-bit digest was later found to be vulnerable.

---

## Hash collisions

All hash functions map an input of any length to a fixed-size output of letters and numbers. Since there are infinitely many possible inputs but only a finite set of outputs, it is possible for two different inputs to produce the same hash.

A **hash collision** occurs when different inputs produce the same hash value.

Because hashes are used for authentication, collisions can be dangerous—similar to copying someone’s identity. Attackers can use collision attacks to impersonate authentic data.

---

## Next-generation hashing (SHA family)

To reduce collision risks, hash functions with longer outputs were needed. MD5’s shortcomings led to the **Secure Hash Algorithms (SHA)** family.

The **National Institute of Standards and Technology (NIST)** approves these algorithms. The number in the name indicates the size of the digest in bits. Except for **SHA-1** (160-bit digest), these are commonly considered collision-resistant, though no control is invulnerable to every exploit.

Five functions in the SHA family:

- **SHA-1**
- **SHA-224**
- **SHA-256**
- **SHA-384**
- **SHA-512**

---

## Secure password storage (why hashing helps)

Passwords are typically stored in a database mapped to usernames. When a user authenticates, the server looks up the username and verifies the supplied password matches.

Storing passwords in plaintext is risky: if an attacker accesses the database, they can steal credentials directly. Hashing adds protection because hash values **can’t be reversed**, making it harder for an attacker to recover passwords even if the database is compromised.

---

## Rainbow tables

A **rainbow table** is a file of pre-generated hash values and their associated plaintext. Attackers can use rainbow tables like dictionaries of weak passwords to compare against an organization’s password database.

Rainbow table attacks are more likely to succeed against hashing approaches with shorter digests (such as MD5).

---

## Salting (adding more protection)

Even with longer digests, no control is perfect. **Salting** strengthens hashing by adding a random string of characters to data **before** hashing.

A **salt** makes the resulting hash more unique, improving resilience against rainbow table attacks.

Example: If a database has many users with the same password (e.g., `"password"`), salting causes each stored hash to be different, preventing a simple rainbow table lookup from matching across entries.

Salt quality matters: the longer and more unique the salt, the harder it is to crack.

---

## Key takeaways

- Hashing helps validate **integrity** of files and data.
- Shorter digests (like **MD5**) are more vulnerable to collisions and rainbow table attacks.
- The **SHA** family provides longer digests and improved collision resistance (with **SHA-1** as an older, weaker member).
- For passwords, hashing reduces breach impact, and **salting** further improves resilience against rainbow table attacks.

