# SQL queries (and SQL injection basics)

SQL is commonly used to retrieve, insert, update, or delete information stored in database tables.

---

## Databases, tables, and queries

A **database** is an organized collection of information (data). In SQL, data is organized into **tables**.

A **SQL query** is a request for data from a database. For example, a query might retrieve employee IDs, names, and job titles from an employee directory table.

Many web applications accept user input and use it to build queries (for example, HR apps that search directories).

---

## How SQL injection happens

A **SQL injection** occurs when an attacker exploits an input field that is not designed to filter out unexpected text. Input fields are places users can type text, such as:

- login forms
- search bars
- comment submission boxes

If inputs aren’t handled safely, attackers can inject malicious SQL that manipulates a database, steals sensitive data, or even helps take control of a vulnerable application.

---

## SQL injection categories

SQL injection types differ based on how the attack is initiated and how results are returned.

### In-band SQL injection

**In-band** (classic) SQL injection uses the same communication channel to launch the attack and receive results.

Example: a retailer’s product search box is vulnerable; an attacker submits a malicious query and sensitive data (like passwords) is returned and displayed in the same search interface.

### Out-of-band SQL injection

**Out-of-band** SQL injection uses a different channel to exfiltrate results.

Example: an attacker uses a malicious query to create a connection between the target and a database the attacker controls, enabling data theft through that separate channel.

**Note:** Out-of-band attacks are uncommon and typically require specific server features to be enabled.

### Inferential SQL injection

**Inferential** SQL injection happens when the attacker cannot directly see query results. Instead, they infer information by observing system behavior.

Example: injecting into a login form triggers error messages; the attacker uses those responses to learn database structure and then crafts follow-on attacks.

---

## Injection prevention (escaping user input)

Many queries are written assuming users will only enter “expected” values (e.g., an email field like `jdoe@domain.com`). Preventing SQL injection requires escaping user inputs so unexpected code can’t be interpreted as SQL.

Common defensive techniques:

- **Prepared statements**: execute SQL statements before passing user inputs to the database (separating code from data).
- **Input sanitization**: remove or neutralize user input that could be interpreted as code.
- **Input validation**: ensure input meets expectations (format, type, length, allowed characters).

Using these together helps prevent SQL injection. In practice, security professionals often work with application developers to remediate SQLi vulnerabilities.

If you want to explore further, **OWASP’s SQL injection detection techniques** are a useful reference.

---

## Key takeaways

- SQL queries are widely used by web applications to interact with databases.
- SQL injection is a common risk when applications accept unexpected user input.
- SQLi can be in-band, out-of-band, or inferential, depending on how results are returned.
- Prevention relies on safe input handling (prepared statements, sanitization, validation) and developer collaboration.

