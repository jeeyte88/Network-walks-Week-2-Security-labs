# Network-walks-Week-2-Security-labs
Week 2 Cybersecurity practical exercises covering domain footprinting, reconnaissance, DNS enumeration, website technology identification, HTTP header analysis, Web Application Firewall detection, and local network scanning using Kali Linux and Zenmap. Includes practical commands, scan results, screenshots, risk analysis, security recommendations.

# 🔐 Networkwalks Cybersecurity Program – Week 2

![Cybersecurity](https://img.shields.io/badge/Field-Cybersecurity-c0392b?style=flat&labelColor=555555)
![Footprinting](https://img.shields.io/badge/Skill-Footprinting-f39c12?style=flat&labelColor=555555)
![Kali Linux](https://img.shields.io/badge/Tool-Kali%20Linux-4285F4?style=flat&labelColor=555555)
![Zenmap](https://img.shields.io/badge/Tool-Zenmap-1976D2?style=flat&labelColor=555555)
![Network Scanning](https://img.shields.io/badge/Skill-Network%20Scanning-8e44ad?style=flat&labelColor=555555)
![Cybersecurity Training](https://img.shields.io/badge/Program-Networkwalks-b22222?style=flat&labelColor=555555)

# Cybersecurity Practical Assessment Report

| **Author** | Abdikani Mohamud Jeite |
|---|---|
| **Batch** | B084 |
| **Program** | Networkwalks Cybersecurity Program |
| **Week** | 02 |
| **Date** | 13 November 2026 |
| **Practical Modules** | W2-PM1 – Multiple Kali Linux Tools; W2-PM5 – Zenmap Network Scanning |

## Assessment Scope

**Target Systems:**
- `networkwalks.com` – Domain footprinting and reconnaissance, conducted with written authorization.
- My own local network – Network discovery and scanning using Zenmap.

**Authorization:** Written permission obtained for the domain assessment. Local network scanning was conducted on my own network.

## Phases Covered

- **Phase 1: Reconnaissance and Footprinting** – Gathering publicly available domain information using WHOIS, WhatWeb, Nslookup, cURL, WAFW00F, and DNSRecon.
- **Phase 2: Scanning and Network Discovery** – Identifying active hosts, IP addresses, and MAC addresses on my local network using Zenmap.

## Tools and Technologies

Kali Linux, WHOIS, WhatWeb, Nslookup, cURL, WAFW00F, DNSRecon, Windows CMD, Zenmap, and Nmap.



**Author:** Abdikani Mohamud Jeite  
**Cybersecurity Student | B084**  
**LinkedIn:** https://www.linkedin.com/in/abdikani-jeite-8a714a262?utm_source=share_via&utm_content=profile&utm_medium=member_ios

**GitHub Repository:** `networkwalks-cybersecurity-week02-footprinting-reconnaissance`.

**Liability Disclaimer**

- All activities documented here were carried out only on systems and devices that I own or for which I had obtained proper authorization. The information and materials shared are strictly for educational and research purposes. They should not be used for any illegal or unauthorized activities. I take full responsibility for my actions and how I apply the knowledge gained. Any misuse of these techniques may result in legal consequences, including criminal charges, financial penalties, or other serious consequences. Unauthorized access to computer systems is illegal in many countries, even if no damage is caused.


**Introduction**

In this report, I carried out two main cybersecurity activities as part of Week 2 of my Networkwalks Cybersecurity Program. The first activity involved gathering publicly available information about the networkwalks.com domain using different reconnaissance tools in Kali Linux (W2-PM1). The second activity focused on scanning my own local network using Zenmap to identify active devices and collect network information (W2-PM5).
For the practical exercises, I used a Kali Linux virtual machine running on Oracle VirtualBox to perform the domain reconnaissance activities. I also used Zenmap, installed on my Windows PC, to scan my local network.
Throughout this report, I have included the commands I executed, the results I obtained, screenshots of my activities, and brief explanations of the security importance of each finding. All activities were conducted for educational purposes and within systems and networks I was authorized to assess.

 **Tools Used**
## Tools Used

The following tools and operating systems were used during the practical exercises. Each tool served a specific purpose in gathering domain information, identifying website technologies, or discovering devices connected to my local network.

| **Tool** | **Purpose** |
|---|---|
| Kali Linux & Windows | Operating systems used to perform reconnaissance and network scanning activities. |
| WHOIS | Used to retrieve domain registration information, including registration dates and name servers. |
| WhatWeb | Used to identify website technologies, such as the web server, CMS, plugins, and IP address. |
| Nslookup | Used to query DNS and find the IP address associated with a domain name. |
| cURL (`curl -I`) | Used to retrieve and examine HTTP response headers returned by a website. |
| WAFW00F | Used to check whether a Web Application Firewall (WAF) protects the website. |
| DNSRecon | Used to gather DNS information and identify available DNS records, such as NS, MX, SPF, TXT, and SRV records. |
| Zenmap (Nmap GUI) | Used to scan my local network and identify active hosts, IP addresses, and available MAC address information. |
| Windows CMD | Used to check my computer's local IP address and MAC address. |






## Footprinting & Reconnaissance

### Tool 1: WHOIS – Domain Information Gathering

**Objective**

The objective of this activity was to collect publicly available registration information about the `networkwalks.com` domain using the WHOIS command in Kali Linux.

**Command Used**

```bash
whois networkwalks.com
```

**Results and Observations**

After executing the WHOIS command, I retrieved several details about the domain registration and DNS infrastructure. The results included the domain registrar, registration and expiration dates, name servers, DNSSEC status, and domain protection settings.

The following information was collected during the lookup:

| **Information** | **Observed Result** |
|---|---|
| Domain Name | NETWORKWALKS.COM |
| Registrar | GoDaddy.com, LLC |
| Registrar WHOIS Server | whois.godaddy.com |
| Creation Date | 06 November 2019 |
| Last Updated | 12 November 2025 |
| Expiration Date | 06 November 2027 |
| Name Server 1 | NS6135.HOSTGATOR.COM |
| Name Server 2 | NS6136.HOSTGATOR.COM |
| DNSSEC | Unsigned |
| Domain Status | ClientTransferProhibited |


**Analysis and Security Relevance**

The WHOIS lookup provided useful information about the domain's registration and DNS infrastructure.

- **Registrar Information:** The domain is registered through GoDaddy, which identifies the company responsible for its domain registration.
- **Registration Dates:** The domain was created on 06 November 2019 and is scheduled to expire on 06 November 2027.
- **Name Servers:** The domain uses HostGator name servers, providing information about its DNS hosting infrastructure.
- **Domain Protection:** The transfer, update, deletion, and renewal restrictions indicate that certain domain management operations are restricted.
- **DNSSEC:** The WHOIS result showed that DNSSEC is unsigned, meaning the domain does not currently have DNSSEC signing enabled according to the lookup result.

From a cybersecurity perspective, WHOIS information helps security professionals understand a domain's registration details, hosting infrastructure, and publicly available technical information before conducting further reconnaissance activities.

**Screenshot Evidence**

*Figure 1: Performing a WHOIS lookup on networkwalks.com using Kali Linux to collect domain registration and DNS information.*
