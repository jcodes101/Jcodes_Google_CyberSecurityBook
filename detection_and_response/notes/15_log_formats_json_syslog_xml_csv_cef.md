# Log formats for analysis: JSON, Syslog, XML, CSV, CEF

Logs record events on networks and systems. **Log analysis** is the process of **examining** logs to find **events of interest**. Analysts must **read and interpret** different **log formats** to extract who did what, when, and where—and to spot **unusual** or **malicious** activity.

There is **no single standard** format; sources vary. This note reviews common formats: **JSON**, **Syslog**, **XML**, **CSV**, and **CEF**.

---

## JavaScript Object Notation (JSON)

**JSON** is a lightweight format used to **store** and **transmit** data. It is common in **web** stacks and **cloud** environments. JSON syntax borrows from **JavaScript**.

### Building blocks

**Key-value pairs**  
A **key** and its **value**, separated by a colon. For readability, include a **space** before or after the colon.

Example: `"Alert": "Malware"`

**Commas**  
Separate multiple fields in an object or list.

Example: `"Alert": "Malware", "Alert code": 1090, "severity": 10`

**Double quotes**  
Enclose **string** values: `"Alert": "Malware"`. Numeric values are typically **not** quoted: `"Alert code": 1090`.

**Curly brackets `{ }`**  
Enclose an **object**: a comma-separated list of key-value pairs. JSON log entries often start and end with `{` `}`.

Nested object example (`User` is an object with multiple properties):

```json
"User": {
    "id": "1234",
    "name": "user",
    "role": "engineer"
}
```

**Square brackets `[ ]`**  
Enclose an **array**: an ordered, comma-separated list.

Example: `["Administrators", "Users", "Engineering"]`

---

## Syslog

**Syslog** can mean three related things:

1. **Protocol** — transports logs to a **central** log server. Common ports: **514** (plaintext), **6514** (encrypted).  
2. **Service** — receives syslog entries and **forwards** them to a remote server.  
3. **Log format** — a very common format, especially on **Unix** systems.

### Syslog message structure (format)

A syslog entry often has:

- **Header** (timestamp, hostname, app name, message ID, etc.)  
- **Structured-data** (optional; often key-value pairs inside `[ ]`)  
- **Message** (human-readable detail)

### Example (header + structured-data + message)

```text
<236>1 2022-03-21T01:11:11.003Z virtual.machine.com evntslog - ID01 [user@32473 iut="1" eventSource="Application" eventID="9999"]
This is a log entry!
```

**Header (illustrated)**  
- **PRI (priority):** `<236>` — indicates urgency of the logged event, carried in angle brackets. Generally, the **lower** the priority level, the **more urgent** the event is.  
- **Timestamp:** `2022-03-21T01:11:11.003Z` — date `YYYY-MM-DD`, `T` separator, 24-hour time with milliseconds `.003`, `Z` = **UTC**.  
- **Hostname:** `virtual.machine.com`  
- **Application:** `evntslog`  
- **Message ID:** `ID01`  

**Structured-data**  
Inside `[ ]`: key-value style metadata, e.g. `iut="1"`, `eventSource="Application"`, `eventID="9999"`.

**Message**  
`This is a log entry!`

**Note:** Syslog headers can be combined with **JSON** or **XML** payloads; **custom** vendor formats also exist.

---

## XML (eXtensible Markup Language)

**XML** is both a **language** and a **format** for storing and transmitting data. It is a **native** style for many **Windows** logging and export scenarios.

### Concepts

**Tags**  
Start and end pairs: `<tag>` … `</tag>`.

**Elements**  
The **tags plus the data** between them. Every XML document has a **root element**; nested **child** elements sit underneath.

Example:

```xml
<Event>
    <EventID>4688</EventID>
    <Version>5</Version>
</Event>
```

`<Event>` is the root; `<EventID>` and `<Version>` are children.

**Attributes**  
Extra metadata on an opening tag; values are quoted with **single** or **double** quotes.

Example (Windows-style event data):

```xml
<EventData>
    <Data Name='SubjectUserSid'>S-2-3-11-160321</Data>
    <Data Name='SubjectUserName'>JSMITH</Data>
    <Data Name='SubjectDomainName'>ADCOMP</Data>
    <Data Name='SubjectLogonId'>0x1cf1c12</Data>
    <Data Name='NewProcessId'>0x1404</Data>
</EventData>
```

Here `<Data>` is the tag; `Name='SubjectUserSid'` is an **attribute** describing the enclosed value.

---

## CSV (Comma-Separated Values)

**CSV** uses **commas** to separate values. **Field names may be omitted** from each row; **position** maps to a predefined schema. You must know **which column is which** for that device (IPS, firewall, scanner, etc.).

Example row:

```text
2009-11-24T21:27:09.534255,ALERT,192.168.2.7,1041,x.x.250.50,80,TCP,ALLOWED,1:2001999:9,"ET MALWARE BTGrab.com Spyware Downloading Ads",1
```

---

## CEF (Common Event Format)

**CEF** structures vendor logs using **pipes** `|` for the main header fields; the **Extension** section uses **key=value** pairs.

### CEF header pattern

```text
CEF:Version|Device Vendor|Device Product|Device Version|Signature ID|Name|Severity|Extension
```

**Syslog transport:** When syslog prepends a message, you may see a **timestamp** and **hostname** before the `CEF:` portion.

### Example (worm-related alert)

```text
Sep 29 08:26:10 host CEF:1|Security|threatmanager|1.0|100|worm successfully stopped|10|src=10.0.0.2 dst=2.1.2.2 spt=1232
```

| Part | Value |
|------|--------|
| Syslog timestamp | `Sep 29 08:26:10` |
| Syslog hostname | `host` |
| CEF version | `CEF:1` |
| Device vendor | `Security` |
| Device product | `threatmanager` |
| Device version | `1.0` |
| Signature ID | `100` |
| Name | `worm successfully stopped` |
| Severity | `10` |
| Extension (key=value) | `src=10.0.0.2 dst=2.1.2.2 spt=1232` |

Interpretation (from the course narrative): a **Security** application **threatmanager** reported stopping a **worm** from spreading from internal `10.0.0.2` toward external `2.1.2.2` using source port `1232`, with **high** severity **10**.

**Note:** The **Extension** block and the **syslog prefix** are **optional** in some deployments.

---

## Key takeaways

- Analysts work with **many log formats**; there is **no** universal layout.  
- **JSON** — objects `{}`, arrays `[]`, key-value pairs, strings in double quotes.  
- **Syslog** — protocol/service/format; know **header**, **structured-data**, **message**, and **PRI**; ports **514** / **6514**.  
- **XML** — tags, elements, root/child structure, **attributes**.  
- **CSV** — positional fields; **document** the schema for each source.  
- **CEF** — pipe-delimited header + optional **key=value** extension; often shipped over **syslog**.
