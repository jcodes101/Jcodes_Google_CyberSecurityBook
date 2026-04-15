# Cloud computing processes and software-defined networks (SDN)

## On-premise vs cloud computing

- **On-premise (traditional) networks**: Network devices, servers, and storage are kept at a **physical location owned by the company** (e.g., an office building or company data center).
- **Cloud computing**: Using **remote servers, applications, and network services** hosted on the **internet**, rather than at a company-owned physical location.

## Cloud service provider (CSP)

A **cloud service provider (CSP)** is a company that offers cloud computing services from large **global data centers** containing massive numbers of servers.

- **How customers consume services**:
  - **API** (application programming interface)
  - **Web console**
  - Typically **pay-as-you-go** for compute, storage, and networking consumed

## The three main cloud service categories (SaaS, IaaS, PaaS)

### SaaS — Software as a service

**Software suites operated by the CSP** that an organization uses remotely.

- **You manage**: primarily your data/configuration and how users access the app
- **CSP manages**: the application, runtime, infrastructure, and underlying hardware
- **Mental model**: “Use the software; don’t host it.”

### IaaS — Infrastructure as a service

**Virtualized compute, storage, and networking building blocks** offered by the CSP (e.g., virtual machines/instances, containers, and storage) configured through the CSP’s **API** or **web console**.

- **You manage**: OS configuration (often), network configuration, applications, and most security controls above the infrastructure layer
- **CSP manages**: physical servers, data center operations, and virtualization layer
- **Why it’s useful**: run existing workloads with minimal changes, then optionally refactor to take advantage of cloud capabilities (availability, scalability, managed security features)

### PaaS — Platform as a service

**Developer-focused tools and managed platforms** used to **build and deploy custom applications** in the cloud.

- **You manage**: your application code and some configuration
- **CSP manages**: the underlying platform/runtime, scaling primitives, and much of the infrastructure
- **Mental model**: “Build apps on a managed platform.”

## How SaaS / PaaS / IaaS connect to physical data centers

Even though cloud resources feel “virtual,” they ultimately run on **physical hardware** in a CSP’s **data centers**.

- **Data center**: racks of servers, storage systems, and networking equipment
- **Virtualization**: software layers carve physical resources into **virtual** resources (compute, storage, networks)
- **You access**: the virtual services through the internet (API/console)

## Hybrid cloud vs multi-cloud

- **Hybrid cloud**: an organization uses **CSP services** *in addition to* its **on‑premise** computers, networks, and storage.
- **Multi‑cloud**: an organization uses **more than one CSP**.

Why hybrid is common:

- **Cost control**: avoid building/refreshing everything on-prem
- **Control**: keep sensitive or legacy workloads on-prem while using cloud where it helps

## Software-defined networks (SDNs)

**Software-defined networks (SDNs)** are networks built from **virtual network devices and services**.

- SDNs can include virtual versions of:
  - **Switches**
  - **Routers**
  - **Firewalls**
  - Other network services
- In cloud networking, these SDN tools run on servers hosted in the **CSP’s data center**.
- Many modern “physical” network devices also rely heavily on software (network virtualization) to perform tasks like routing and switching.

## Benefits of cloud computing and SDNs (why businesses like them)

### Reliability

**Reliability** relates to:

- How **available** services/resources are
- How **secure** connections are
- How consistently services run with minimal interruption

Cloud services can improve reliability because CSPs design for redundancy and global availability.

### Cost

Traditional on-prem networks can require large **upfront** purchases and ongoing costs (patching, upgrades, maintenance).

CSPs can lower cost by:

- Massive economies of scale (data centers at huge scale)
- Offering services that are cheaper than building/maintaining equivalents in-house
- Shifting spend to consumption-based pricing

### Scalability

Cloud enables rapid scaling up/down using an **elastic utility model**:

- You can consume more/less compute, storage, and networking as needed
- You typically pay only for what you use when you use it

Cloud changes can usually be made quickly through:

- **APIs**
- **Web consoles**

Security-relevant examples that can be configured quickly when needed:

- **WAFs** (web application firewalls)
- **IDS/IPS**
- **L3/L4 firewalls**

## Key takeaways

- **CSPs** run huge global **data centers** and sell **compute, storage, and networking** over the internet.
- **SaaS / PaaS / IaaS** are three common service models that describe *how much the CSP manages vs how much you manage*.
- **Hybrid cloud** mixes on-prem + cloud; **multi-cloud** uses multiple CSPs.
- **SDNs** virtualize networking components, enabling faster and more programmatic network configuration.
