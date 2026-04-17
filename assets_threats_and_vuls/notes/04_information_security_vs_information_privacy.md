# Information security vs. information privacy

Security and privacy are often used interchangeably outside of cybersecurity, but they represent different (and connected) functions.

---

## Definitions

- **Information privacy**: protection from unauthorized access and distribution of data
- **Information security (InfoSec)**: the practice of keeping data in all states away from unauthorized users

**Key difference:** Privacy focuses on giving people control over their personal information and how it’s shared. Security focuses on protecting people’s choices and keeping their information safe from threats.

---

## Example (consent + controls)

A retail company might want to collect personal information for marketing (e.g., age, gender, location). How the information will be used should be disclosed **before** collecting it, and customers should be able to **opt out**.

After the company gets consent, it should implement security controls to protect that private data from unauthorized access, use, or disclosure. It should also ensure controls respect the privacy of stakeholders, including those who opted out.

**Note:** Privacy and security are both essential for maintaining customer trust and brand reputation.

---

## Why privacy matters in security

Data privacy and protection gained major attention in the late 1990s as companies shifted from simply processing data to storing and using it for business purposes.

Example: if a user searched for a product online, organizations began storing search history and sharing access to it with other companies—enabling personalized experiences.

This drove global debate about whether organizations have the right to collect and share private data. It also raised security concerns: the more data an organization collects, the more opportunities exist for abuse, misuse, or theft.

Without clear rules, protections were inconsistently applied.

**Note:** The more data is collected, stored, and used, the more vulnerable it is to breaches and threats.

---

## Notable privacy regulations

Businesses must follow laws to operate. **Regulations** are rules set by a government or other authority that control how something is done. Privacy regulations protect users from having their information collected, used, or shared without consent. They may also specify required security measures.

Three influential regulations every security professional should know:

- **General Data Protection Regulation (GDPR)**
- **Payment Card Industry Data Security Standard (PCI DSS)**
- **Health Insurance Portability and Accountability Act (HIPAA)**

### GDPR

**GDPR** is a set of EU rules that places data owners in control of their personal information. Personal information can include name, address, phone number, financial information, and medical information.

GDPR applies to businesses that handle the data of EU citizens or residents, regardless of where the business operates (e.g., a U.S.-based company handling EU visitors’ website data).

### PCI DSS

**PCI DSS** is a set of security standards created by major organizations in the financial industry. It aims to secure credit and debit card transactions against data theft and fraud.

### HIPAA

**HIPAA** is a U.S. law requiring protection of sensitive patient health information. It prohibits disclosing medical information without the person’s knowledge and consent.

**Note:** These regulations influence data handling at many organizations worldwide, even though they were developed by specific nations.

---

## Security assessments and audits

Organizations should comply with regulations to meet minimum expectations and demonstrate commitment to privacy.

Compliance is often supported by two activities:

- **Security audit**: a review of an organization’s security controls, policies, and procedures against a set of expectations
- **Security assessment**: a check to determine how resilient current security implementations are against threats

Example: if a regulation requires multi-factor authentication (MFA) for administrator accounts:

- an **audit** might check whether admin accounts have MFA enabled
- an internal **assessment** might find many users still use weak passwords, leading the organization to enable MFA for all accounts to improve posture

**Note:** Compliance with regulations (e.g., GDPR) can be determined during audits.

Security analysts often participate in audits and assessments:

- **Audits** are usually less frequent (about once per year) and can be internal or external (including third parties).
- **Assessments** are usually more frequent (about every three-to-six months), often run by internal teams, and can prepare the organization for an audit.

Both are important for ensuring systems protect people’s privacy.

---

## Key takeaways

More organizations are prioritizing protecting and governing sensitive data to maintain customer trust.

- **Privacy**: control over personal information and how it’s shared
- **Security**: protecting information and the choices people make about it
- Key regulations include **GDPR**, **PCI DSS**, and **HIPAA**
- Organizations use **assessments** and **audits** to identify gaps; delaying fixes can lead to serious consequences (fines or data breaches)

