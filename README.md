# 🔐 Footprinting and Network Scanning — Week 2

A hands-on cybersecurity internship project covering OSINT footprinting with tools like Whois, Whatweb, Nslookup amongst other tools on kali Linux and local network discovery with Zenmap.

![Cybersecurity](https://img.shields.io/badge/Skill-Cybersecurity-red)
![Kali Linux](https://img.shields.io/badge/Kali-Linux-blue)
![theHarvester](https://img.shields.io/badge/theHarvester-4.10-orange)
![Zenmap](https://img.shields.io/badge/Zenmap-Nmap_GUI-green)
![Footprinting](https://img.shields.io/badge/Skill-Footprinting-purple)
![Network Scanning](https://img.shields.io/badge/Skill-Network_Scanning-blue)
![Ethical Hacking](https://img.shields.io/badge/Ethical_Hacking-orange)

---

**W2-PM-FINAL | CYBERSECURITY | NETWORKWALKS**

---

### 👤 Pentester Information

| Information | Details |
|---|---|
| **Pentester Name** | Josiah Ayuba |
| **Role** | Cybersecurity Professional |
| **Program / Batch** | B083-Networkwalks |
| **Date** | 16 September 2026 |
| **Client / Target** | Networkwalks / My own local LAN Network |
| **Permission Secured?** | Yes |

### 📚 Modules Completed

- **W2-PM1** — Multiple Kali Tools
- **W2-PM5** — Zenmap Scanning

### 🔎 Phases Covered

- **Phase 1:** Reconnaissance & Footprinting
- **Phase 2:** Scanning & Network Discovery
- **Phase 3–5:** Penetration Testing Report

---

# 1. Liability Disclaimer

I have performed these activities only on the systems & devices where I had secured written permission or the devices/systems that I own myself.

All these materials are for education and research purpose only. Do not use anything from here to break the law.

The instructor, the authors and Networkwalks are not responsible for what you do with this knowledge.

Every action you take is your own responsibility.

Misuse can lead to criminal charges, heavy fines, loss of your job and a permanent record.

In most countries unauthorised access is a crime even when nothing is damaged.

---

# 2. Introduction

This report covers footprinting the networkwalks.com domain using multiple Kali Linux tools (W2-PM1) and scanning my own local network with Zenmap (W2-PM5).

One module covers the footprinting phase and the other covers the scanning phase, so together they show how an attacker moves from gathering public information to mapping live hosts on a network.

It is the Week 2 part of my ongoing internship program at Networkwalks.

All commands were run in Kali Linux (footprinting) and on a Windows PC with Zenmap installed (scanning).

Every step below includes the exact command used, the result I observed, a screenshot as evidence, and a short note on why the finding matters from an attacker's point of view.

---

# 3. Tools Used

The table below lists each tool used in this report and its purpose.

| Tool | Purpose |
|---|---|
| **Kali Linux & Windows** | Operating systems used for reconnaissance activities |
| **WHOIS** | Find domain registration details (owner, dates, name servers). |
| **WhatWeb** | Fingerprint web technologies (server, CMS, plugins, IP). |
| **Nslookup** | Resolve the domain name to its IP address using DNS. |
| **curl -I** | Read the HTTP response headers of the website. |
| **wafw00f** | Detect whether a Web Application Firewall protects the site. |
| **dnsrecon** | Enumerate all DNS records (NS, MX, SPF, TXT, SRV). |
| **theHarvester** | Gather publicly available information about a target domain, including email addresses, hostnames and other OSINT information. |
| **Zenmap (Nmap GUI)** | Scan the local subnet to find live hosts, IPs and MAC addresses. |
| **Windows CMD** | Local IP and MAC address identification |

---

# 4. Activities Performed

## 4.1 Footprinting & Reconnaissance

I performed reconnaissance against the networkwalks.com domain using six Kali Linux tools: WHOIS, WhatWeb, Nslookup, Curl, Wafw00f and DNSRecon.

Each tool was used to collect a different type of information about the target.

### 🔎 WHOIS

I used WHOIS to obtain publicly available domain registration information and identify the domain's name servers.

The results provided information about the domain registration and hosting infrastructure.

#### Evidence

![WHOIS Results](images/whois-results.png)

---

### 🌐 WhatWeb

I then used WhatWeb to identify technologies used by the website.

The results identified WordPress 7.1 and WP Download Manager 3.3.58, along with other information exposed by the website.

#### Evidence

![WhatWeb Results](images/whatweb-results.png)

---

### 🔍 Nslookup

Using Nslookup, I resolved the domain name to its IP address.

The provided result identified:

```text
192.232.216.135
