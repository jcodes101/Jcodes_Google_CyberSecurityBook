# SIEM search methods: Splunk (SPL) and Google SecOps (Chronicle)

**Security information and event management (SIEM)** tools collect and analyze **log data** to monitor important activity—for example, **failed login** attempts.

Organizations use **different** SIEM products. As an analyst, you should be ready to learn **vendor-specific** search interfaces and languages so you can **find**, **filter**, and **reshape** evidence quickly during investigations.

This note compares two common patterns: **Splunk** (Search Processing Language, **SPL**) and **Google Security Operations** (**Chronicle**) (**UDM** vs **Raw Log** search).

---

## Splunk searches (SPL)

Splunk uses **Search Processing Language (SPL)** to retrieve events from **indexes** in the **Search & Reporting** app. A single SPL search can chain many **commands** and **arguments**—for example, **filter** results or **transform** them into a **chart**.

Deeper SPL reference: [Splunk Search Reference](https://docs.splunk.com/Documentation/Splunk/latest/SearchReference/Welcome).

### Basic search example

```spl
index=main fail
```

- **`index=main`**: read events from the Splunk **index** named `main` (an index stores collected, processed event data).  
- **`fail`**: return events whose raw text **contains** the term `fail`.

Effective SPL reduces time-to-answer and helps you pull the **right** fields from **many** source types.

### Pipes (`|`)

Like **bash**, SPL uses **`|`** to send the **output** of one command into the **next** command so you can refine results in one pipeline.

Example:

```spl
index=main fail | chart count by host
```

- **`index=main fail`**: initial event set from `main` containing `fail`.  
- **`| chart count by host`**: aggregate into a chart of **event counts** grouped by **`host`** (device name)—useful to spot hosts with unusually high failure volume.

### Wildcards (`*`)

A **wildcard** substitutes for other characters; in Splunk this is often **`*`** when the command supports it.

Example:

```spl
index=main fail*
```

Matches strings that **start with** `fail`, such as **failed** or **failure**, not only the exact token `fail`.

### Exact phrase search (double quotes)

Use **double quotes** to search for an **exact phrase**:

```spl
index=main "login failure"
```

This targets the full phrase **login failure**, not unrelated events that merely contain **login** or **failure** separately.

---

## Google Security Operations (Chronicle) searches

In Chronicle, you search from the **Search** field. **Procedural Filtering** can **include** or **exclude** results based on event type, log source, or other criteria to narrow the dataset.

Chronicle supports two primary search modes:

1. **Unified Data Model (UDM) Search** (default for structured hunting on normalized data)  
2. **Raw Log Search** (search unparsed/raw text when UDM is not enough)

### UDM Search (default)

**UDM** searches operate on ingested data that has been **parsed** and **normalized** into **UDM**. UDM searches are typically **faster** than raw searches because they query **indexed**, **structured** fields.

UDM events expose many field types; the full catalog is large. For field names and meanings, see Google’s documentation: [Chronicle UDM field list](https://cloud.google.com/chronicle/docs/unified-data-model/udm-field-list).

Common UDM groupings this course highlights:

- **Entities (“nouns”)** — at least one per event; context about **device**, **user**, or **process** (for example hostname, username, IP).  
- **Event metadata** — what happened, **timestamps**, event typing, and related descriptors.  
- **Network metadata** — network-oriented details and **protocol** context.  
- **Security results** — security outcomes (for example an antivirus message like **virus detected and quarantined**).

#### Example UDM search (login-related)

```text
metadata.event_type = "USER_LOGIN"
```

- **`metadata.event_type`**: describes the class of activity (authentication, network session, etc.).  
- **`"USER_LOGIN"`**: restricts to **user login**–style authentication events.

Starting with **metadata** fields is a practical way to learn UDM querying before layering more specific predicates.

### Raw Log Search

When answers are not visible in **normalized** UDM fields, **Raw Log Search** scans **raw**, **unparsed** log text. Select **Raw Log Search** from the Search menu after entering criteria.

Raw search is often **slower** but can match **usernames**, **filenames**, **hashes**, free-text tokens, and similar strings that may not yet map cleanly into UDM.

**Pro tip:** Raw Log Search can use **regular expressions** to match complex patterns.

---

## Key takeaways

- SIEMs differ by vendor; learn each tool’s **search model** and **performance** characteristics.  
- **Splunk SPL** uses **indexes**, keywords, **pipes** to chain transforms, **wildcards**, and **quoted phrases** for precision.  
- **Chronicle** emphasizes **UDM** (structured, faster) vs **Raw Log** (flexible, slower); use **Procedural Filtering** to scope results.  
- Strong search skills speed up **threat detection** and **incident response** by turning centralized logs into **actionable** evidence.
