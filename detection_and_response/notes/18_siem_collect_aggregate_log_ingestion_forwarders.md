# SIEM process overview: collection, aggregation, and log ingestion

The SIEM workflow is often described in **three** steps (see also note **01**):

1. **Collect and aggregate data** — ingest event data from many sources into the SIEM.  
2. **Normalize data** — convert ingested data into a **consistent**, **structured** format so it is easier to read, search, and compare. *(Capabilities differ by vendor.)*  
3. **Analyze data** — organize and **index** data for **search**, **correlation**, and **pattern** detection that can surface **unusual** activity.

This note focuses on **step 1**: **collection** and **aggregation**, especially **log ingestion** and **log forwarders**.

---

## Why SIEMs need data

SIEM tools only work well when they **receive** enough of the **right** telemetry. Analysts use SIEMs to **access events**, **query logs**, and **investigate** incidents—often including configuring **how** data gets in.

---

## Log ingestion

**Log ingestion** is the process of **collecting** and **importing** data from **log sources** into the SIEM.

Sources can be any system that **emits** logs—**servers**, workstations, firewalls, cloud services, applications, and more. Typical event categories include **authentication** attempts, **network** activity, configuration changes, and application errors.

### Copy for analysis (without changing the source)

During ingestion, the SIEM typically stores a **copy** of received events in **SIEM storage**. That lets the platform **parse**, **enrich**, and **analyze** without **modifying** the original logs on the source system.

Central ingestion gives analysts a **single place** to search and correlate across the environment.

---

## How data gets in: log forwarders and alternatives

Ingestion methods include **manual uploads** (small tests, one-off investigations) and **automated** collection.

### Why forwarders matter

Manual uploads do not scale when an environment has **thousands** of systems. **Automation** is the norm.

### Log forwarders

**Log forwarders** are software components that **automate** collecting logs from hosts or applications and **sending** them to a destination such as a SIEM (or a log broker ahead of the SIEM).

**Native forwarders:** Some operating systems include built-in forwarding capabilities.

**Third-party forwarders:** If the OS has no suitable native option, install **vendor** or **open-source** forwarding agents, then **configure**:

- **which** logs to collect  
- **where** to send them (SIEM endpoint, queue, collector tier)  

The SIEM then **processes** and **normalizes** (when supported) so data can be **searched**, **explored**, **correlated**, and **analyzed**.

**Note:** Many SIEM vendors ship **proprietary** forwarders; SIEMs may also integrate with **open-source** forwarders (for example, agents used in broader observability stacks). The right choice depends on **compatibility**, **scale**, **cost**, **security** of the pipeline, and **organizational** standards.

---

## Key takeaways

- SIEM value starts with **reliable ingestion**—without data, there is little to detect or investigate.  
- **Log ingestion** centralizes copies of events for analysis while preserving original sources.  
- **Log forwarders** scale collection; configure **scope** and **destinations** deliberately.  
- Understanding **where logs come from** helps you trace activity during incidents and validate **coverage** gaps.
