# A matter of trial and error (brute force attacks)

Threat actors sometimes try to “open a lock” by testing many combinations until they find one that works. In cybersecurity, similar tactics are used to gain unauthorized access to applications and networks.

---

## Brute force tactics (common variants)

Attackers use multiple trial-and-error approaches:

- **Simple brute force attacks**: guess a user’s login credentials by trying many username/password combinations until one works.
- **Dictionary attacks**: use a list of commonly used credentials (like using a dictionary of common words) to attempt access.
- **Reverse brute force attacks**: start with a single credential and try it across many systems until a match is found.
- **Credential stuffing**: reuse stolen credentials from previous breaches to access accounts at another organization.
  - **Pass the hash**: a specialized credential stuffing tactic that reuses stolen, **unsalted hashed** credentials to trick an authentication system into creating a new authenticated session.

**Note:** Besides access credentials, encrypted information can sometimes be brute forced through **exhaustive key search**.

Because these methods involve lots of guessing, attackers often rely on automation.

---

## Tools of the trade

The number of possible credential combinations is huge, making manual brute forcing impractical. Threat actors commonly use software tools to automate attempts.

Common brute forcing tools include:

- **Aircrack-ng**
- **Hashcat**
- **John the Ripper**
- **Ophcrack**
- **THC Hydra**

Security professionals may also use these tools to test their own environments. For example, **Aircrack-ng** can be used to test a Wi‑Fi network for brute force-related weaknesses.

---

## Prevention measures

Organizations defend against brute force attacks using a mix of technical and managerial controls:

- **Hashing and salting**
- **Multi-factor authentication (MFA)**
- **CAPTCHA**
- **Password policies**

### Hashing and salting

**Hashing** converts information into a unique value that can be used to verify integrity. **Salting** strengthens hashing by adding random characters to data (like passwords) before hashing. This increases complexity, makes hashes harder to brute force, and reduces susceptibility to dictionary-style attacks.

### Multi-factor authentication (MFA)

**MFA** requires users to verify identity in two or more ways. It reduces brute force success because an attacker is unlikely to satisfy multiple authentication factors even if one credential is compromised.

### CAPTCHA

**CAPTCHA** (Completely Automated Public Turing test to tell Computers and Humans Apart) is a challenge-response system that helps distinguish humans from automated software attempting password guessing.

Common examples:

- distorted letters/numbers users must type
- image matching (select images that match a word/prompt)

### Password policy

Password policies standardize stronger password practices across an organization. Common requirements include:

- minimum length (e.g., 8+ characters)
- a mix of letters, numbers, and symbols
- lockout policies that limit attempts before an account is suspended
- periodic password changes and/or requirements for new unique passwords

The purpose is to increase the number of possible combinations, raising the time and effort required for attackers.

Organizations often reference guidance such as **NIST Special Publication 800-63B** when building password policies.

---

## Key takeaways

- Brute force attacks are simple but effective methods for gaining unauthorized access.
- Attackers often automate attempts with specialized tools.
- Stronger passwords, hashing+salting, MFA, CAPTCHA, and well-designed password policies help reduce brute force risk.
- Understanding tactics and tools is a key step toward stopping attackers.

