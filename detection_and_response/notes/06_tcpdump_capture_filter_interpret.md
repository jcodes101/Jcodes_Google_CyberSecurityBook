# tcpdump: CLI packet capture and analysis

**tcpdump** is a **command-line** network protocol analyzer. A **command-line interface (CLI)** is a text-based interface where you run commands to interact with the computer.

tcpdump captures network traffic. Captures can be saved to a **packet capture (p-cap)**: a file of packets taken from an interface or network. That file can be analyzed or shared later. Analysts use tcpdump for troubleshooting, security investigations, and spotting malicious activity. It is often **pre-installed on Linux** and can be installed on other Unix-based systems such as **macOS**.

**Note:** Much network traffic is **encrypted**. Data may be unreadable without decryption using the correct keys.

---

## Privileges (sudo / root)

Capturing packets usually requires **administrator-level** privileges: run as **root** or use **sudo**, similar to many packet-sniffing tools.

---

## Basic command syntax

```text
sudo tcpdump [-i interface] [option(s)] [expression(s)]
```

- **sudo**: runs tcpdump with elevated permissions.
- **-i interface**: network interface to capture on. You must choose an interface to capture. **-i any** sniffs all interfaces on the system.
- **option(s)**: optional flags that change how tcpdump runs (e.g., write to file, verbosity).
- **expression(s)**: optional filters to narrow which packets are captured or shown.

**Listing interfaces:** use **-D** to list available interfaces before you capture.

---

## Essential options

tcpdump has many options (50+); see the **manual page** (`man tcpdump`) for the full list. Options are **case sensitive** (e.g., **-w** and **-W** differ). Short options look like **-i**; long options use **--** (e.g., **--interface**).

**Spacing:** short options can be written with or without a space before the value, e.g. `sudo tcpdump -i any -c 3` and `sudo tcpdump -iany -c3` are equivalent.

### -w (write p-cap)

Writes captured packets to a file instead of only printing to the terminal.

Example: capture from all interfaces and save to `packetcapture.pcap`:

```text
sudo tcpdump -i any -w packetcapture.pcap
```

### -r (read p-cap)

Reads an existing capture file.

```text
sudo tcpdump -r packetcapture.pcap
```

### -v, -vv, -vvv (verbose)

By default, tcpdump does not print full packet detail. **-v** increases printed detail; **-vv** and **-vvv** add more. Helpful when you need header-level detail.

Example:

```text
sudo tcpdump -r packetcapture.pcap -v
```

### -c (count)

Limits how many packets are captured or printed (e.g. **-c 1** = one packet, **-c 10** = ten).

Example: capture the first three packets from any interface:

```text
sudo tcpdump -i any -c 3
```

### -n and -nn (no name resolution)

By default, tcpdump may **resolve** IPs to hostnames and ports to service names. That can be misleading (e.g., port 80 labeled “HTTP” when the protocol isn’t always HTTP) and **reverse DNS** can tip off an attacker that you are investigating.

- **-n**: do not resolve hostnames.
- **-nn**: do not resolve hostnames **or** port names.

Using **-n** (or **-nn**) is common best practice when sniffing or analyzing.

Example:

```text
sudo tcpdump -r packetcapture.pcap -v -n
```

**Pro tip:** combine short options when it makes sense, e.g. **-vn**. You cannot merge options that take an immediate argument (e.g. **-c 1**, **-r file.pcap**) the same way.

---

## Filter expressions

Expressions are optional but useful to isolate traffic. Examples:

- By protocol: e.g. **ip6** for IPv6-only traffic.
- Boolean logic: **and**, **or**, **not** for IPs, ports, etc.

Example: read a p-cap and show IPv4 traffic on port 80:

```text
sudo tcpdump -r packetcapture.pcap -n 'ip and port 80'
```

**Quotes:** use single or double quotes so the shell passes the full expression to tcpdump.

**Parentheses:** group expressions, e.g. `ip and (port 80 or port 443)` runs the grouped part first.

---

## Interpreting live output

Each packet is typically **one line**, starting with a **timestamp** (hours, minutes, seconds, fractions of a second).

Example command:

```text
sudo tcpdump -i any -v -c 1
```

Typical fields in the summary line include:

- **Timestamp**: when the packet was seen.
- **Source IP** and **source port**: origin of the packet.
- **Destination IP** and **destination port**: where the packet is going.

Additional lines or fields from **-v** (and higher) may show protocol details (e.g., TCP flags, sequence numbers).

---

## Key takeaways

- **tcpdump** is a CLI tool to **capture**, **filter**, and **inspect** packets; saves to **p-cap** files with **-w**, reads with **-r**.
- Use **sudo** (or root) to capture on most systems; use **-D** to list interfaces, **-i** to select one (or **any**).
- **-v/-vv/-vvv** add detail; **-c** limits packet count; **-n/-nn** avoid risky or misleading name resolution.
- **Expressions** filter by protocol, IP, port, and combinations using **and** / **or** / **not** and parentheses.
- Output lines start with a **timestamp**, then addresses/ports; verbose mode adds header and protocol details.
