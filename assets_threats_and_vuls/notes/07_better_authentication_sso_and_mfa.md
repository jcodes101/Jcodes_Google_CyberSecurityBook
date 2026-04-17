# A better approach to authentication (SSO and MFA)

Single sign-on (SSO) combines multiple logins into one. More companies adopt SSO because it can improve user experience, reduce cost, and reduce the number of authentication targets attackers can focus on.

---

## Why organizations use SSO

SSO is widely used for three reasons:

- **Better user experience**: fewer usernames/passwords to remember
- **Lower cost**: streamlined management of connected services
- **Improved security**: fewer access points for attackers to target

SSO became available in the mid-1990s to address **password fatigue** (people reusing passwords across services). SSO shifts more of the authentication burden away from the user.

---

## How SSO works

SSO automates how trust is established between a user and a service provider.

Instead of relying on the user to authenticate separately to each service, SSO uses a trusted third party to prove identity by exchanging **encrypted access tokens** between:

- an **identity provider (IdP)**
- a **service provider (SP)**

SSO tokens are exchanged using protocols. Two common ones are:

- **LDAP (Lightweight Directory Access Protocol)**: mostly used on-premises
- **SAML (Security Assertion Markup Language)**: mostly used off-premises (e.g., cloud)

**Note:** LDAP and SAML are often used together.

---

## Limitations of SSO

SSO provides benefits, but it can still concentrate risk in a single authentication method. If a password is lost or stolen, multiple connected services could be exposed.

---

## MFA to the rescue

**Multi-factor authentication (MFA)** requires a user to verify identity in **two or more** ways to access a system or network.

Analogy: withdrawing cash at an ATM

- **something you have**: a debit card
- **something you know**: a PIN

Together, the factors verify identity before access is granted.

---

## Strengthening authentication (factors)

MFA extends SSO’s benefits by requiring additional proof. Organizations may require:

- **2FA** (two factors)
- **3FA** (three factors)

Common factor categories:

- **Something you know**: usually a username and password
- **Something you have**: e.g., a one-time passcode (OTP) sent via SMS
- **Something you are**: physical characteristics such as fingerprints or facial scans

Requiring multiple factors is especially effective in cloud environments where verifying remote users is harder. MFA reduces the risk of authenticating the wrong user by requiring proofs that are difficult to imitate or brute force.

---

## Key takeaways

- **SSO** improves UX, reduces costs, and reduces attack surface by consolidating logins.
- SSO commonly relies on protocols like **LDAP** (on-prem) and **SAML** (cloud/off-prem).
- SSO alone can increase the blast radius of a stolen password.
- Combining **SSO + MFA** strengthens security without sacrificing user experience.

