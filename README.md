# Penetration Testing Report: Footprinting & Network Scanning

# Project Overview
This repository documents my Week 2 practical cybersecurity assessment at Networkwalks, focusing on two fundamental phases of penetration testing:

1. Reconnaissance & Footprinting
2. Scanning & Network Discovery
   
The project demonstrates the use of multiple Kali Linux reconnaissance tools to gather publicly available information about an authorised assessment target, alongside Zenmap (Nmap GUI) for discovering live hosts within my own local lab network.

The objective was to understand how information gathering and network discovery contribute to identifying potential security risks and improving an organisation's security posture.

# Project Information

| Category |	Details |
|----------|----------|
| Project	| W2-PM-Final |
| Program |	Cybersecurity |
| Training Institution |	Networkwalks |
| Batch |	B084-Networkwalks |
| Author | Elizabeth Ogijoh |
| Date |	11 November 2026 |
| Modules |	W2-PM1 & W2-PM5 |
| Assessment Type |	Practical Penetration Testing
| Status |	Phases 1 & 2 completed |

# Objectives
- Understand the fundamentals of reconnaissance and footprinting.
- Identify publicly available domain information.
- Examine website technologies and HTTP response headers.
- Explore DNS records and email configurations.
- Identify the presence of Web Application Firewall (WAF) technology.
- Discover active devices on an authorised local network.
- Interpret scanning results and identify potential security concerns.
- Document findings and provide security recommendations.

# Tools & Technologies Used

| Tool |	Purpose|
|------|---------|
| Kali Linux |	Operating system for reconnaissance |
| WHOIS |	Domain registration information |
| WhatWeb	| Website technology fingerprinting
| Nslookup |	DNS resolution |
| cURL |	HTTP response header analysis |
| Wafw00f |	WAF detection |
| DNSRecon |	DNS enumeration |
| Zenmap |	Network discovery and visualisation |
| Nmap |	Network scanning engine |
| Windows CMD |	Local IP and MAC address identification |

# Project Phases
# Phase 1: Reconnaissance & Footprinting

This phase involved gathering publicly available information about an authorised assessment target using six different Kali Linux tools.

Target : **networkwalks.com**

## 1. WHOIS : domain information gathering.

```bash
whois networkwalks.com
```
<img width="609" height="403" alt="WHOIS Results" src="https://github.com/user-attachments/assets/a991f1a4-a532-4a63-a8be-e369ef4db8f5" />

## 2. Whatweb : Website technology identification.

```bash
whatweb networkwalks.com
```
<img width="388" height="262" alt="Whatweb Results" src="https://github.com/user-attachments/assets/80992229-67b8-44e1-a51a-f543af582ae8" />

## 3. Nslookup : DNS resolution.

```bash
nslookup networkwalks.com
```
<img width="391" height="268" alt="Nslookup Result" src="https://github.com/user-attachments/assets/9a264ece-0eb3-4416-9682-6ebb7d8fdaf2" />

## 4. Curl : HTTP header analysis.

```bash
curl -I networkwalks.com
```
<img width="414" height="269" alt="Curl-I Results" src="https://github.com/user-attachments/assets/0ebff73e-dffc-4222-9652-a0a069b4e218" />

## 5. Wafw00f : Web Application Firewall identification.

```bash
wafw00f networkwalks.com
```
<img width="409" height="266" alt="Wafw00f Results" src="https://github.com/user-attachments/assets/46e48ba6-2305-4d87-b484-5cbae311e16c" />

## 6. DNSRecon : DNS record enumeration.

```bash
dnsrecon -d networkwalks.com
```
<img width="442" height="356" alt="Dnsrecon Results" src="https://github.com/user-attachments/assets/485a995f-47d1-4565-a41f-dd464b12fa93" />


## Phase 2: Scanning & Network Discovery
This phase involved scanning my own virtual lab network using Zenmap.

## Activities performed:

- Identifying the local IP address.
- Determining the network subnet.

  Steps:
  
  open command prompt and enter the command ipconfig to get your local IP address and subnet
  
- Performing a host discovery scan.
- Identifying active hosts.
- Examining IP and MAC address information.
- Analysing the network topology.
  Steps:
  1. Entered the subnet in Zenmap and selected the **Ping Scan** profile (equivalent to `nmap -sn <subnet>`).
  2. Collected the live hosts with their IP and MAC addresses.
  3. Opened the **Topology** tab, enabled the legend, and saved the network map as a PDF.

<img width="602" height="418" alt="NMAP Scan1" src="https://github.com/user-attachments/assets/eeb1c879-8a1c-42c4-b6c2-24c5bc5c2219" />

<img width="816" height="419" alt="NMAP Topology1" src="https://github.com/user-attachments/assets/05e841d4-52d0-4b1c-b871-a4411f6ecb83" />

# Key Findings
The practical assessment provided the following learning outcomes:

| Area |	Observation|
|------|-------------|
| Domain Information |	Identified domain registration and name server information. |
| Web Technologies | Identified the website's underlying technologies. |
| DNS	| Examined DNS records and configurations.
| HTTP Headers |	Identified information disclosed through HTTP responses. |
| WAF	| Identified the presence of a Web Application Firewall. |
| Network Discovery |	Successfully identified three active hosts in my lab network. |
| Network Topology |	Generated a visual representation of discovered hosts. |
| Risk Assessment |	Documented potential security risks and recommendations. |

These observations are indicators for further authorised security assessment, not confirmed vulnerabilities.

# Risk Analysis
The assessment highlighted several areas worth reviewing:

- Public disclosure of technology information.
- DNS software version disclosure.
- Email security configuration.
- HTTP header information exposure.
- Publicly identifiable infrastructure information.
- Visibility of devices within a local network.

No vulnerabilities were exploited or validated during these exercises.

# Recommendations
Based on the observations, the following security improvements were recommended:

- Minimise unnecessary public technology disclosures.
- Keep WordPress and its plugins updated.
- Review HTTP security headers and REST API exposure.
- Avoid unnecessary DNS software version disclosure.
- Improve email authentication and DNS security configurations.
- Maintain and regularly update WAF rules.
- Perform periodic internal network discovery.
- Investigate unidentified network devices.
- Maintain accurate network documentation.
- Conduct security assessments only with proper authorisation.

  # Evidence & Documentation
The repository contains supporting documentation and evidence of the practical activities, including:

- Terminal outputs.
- Screenshots of reconnaissance activities.
- DNS enumeration evidence.
- Zenmap scanning results.
- Network topology visualisation.
- Complete penetration testing report.

Full Report: W2-PM-FINAL_Penetration_Testing_Report.pdf

# Disclaimer
All practical activities documented in this repository were conducted for educational and research purposes on systems for which authorisation was obtained or within my own local lab environment.

No exploitation or unauthorised access was performed.

This repository is intended to demonstrate cybersecurity learning and responsible security assessment practices. Do not use the techniques discussed here against systems without explicit permission.

## Author
**Elizabeth Ogijoh**

Cybersecurity Professional
Networkwalks | Batch B084

⭐ This project represents my practical learning journey in cybersecurity, particularly in reconnaissance, footprinting, network discovery, security assessment and technical documentation.
