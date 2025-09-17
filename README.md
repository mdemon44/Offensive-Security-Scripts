# Offensive Security Toolkit

A comprehensive collection of penetration testing scripts for various security assessment scenarios including Active Directory, web application testing, network reconnaissance, and cloud security.

> **Warning / Disclaimer**
> These tools are intended **only** for authorized security testing, education, research, and CTFs. Always obtain written permission before testing any system. The authors are not responsible for misuse.

---

## 🔖 Table of Contents
- [Overview](#overview)
- [Script Categories](#script-categories)
  - [Active Directory Pentesting Scripts](#active-directory-pentesting-scripts)
  - [Web Application Scripts](#web-application-scripts)
  - [Reconnaissance & Enumeration](#reconnaissance--enumeration)
  - [Cloud Security Scripts](#cloud-security-scripts)
  - [Utility Scripts](#utility-scripts)
- [Requirements & Prerequisites](#requirements--prerequisites)
- [Quick Start / Installation](#quick-start--installation)
- [Usage Examples](#usage-examples)
- [Active Directory Attack Chain (Example)](#active-directory-attack-chain-example)
- [Contributing](#contributing)
- [Legal & Ethical Considerations](#legal--ethical-considerations)
- [Contact](#contact)
- [License](#license)

---

## Overview
This repository bundles useful scripts and helpers for penetration testers, red-teamers, security researchers, and CTF players. Scripts are grouped by category and provide convenient wrappers and automation for common offensive tasks (AD, web, recon, cloud).

> **Note:** Read each script header and comments before running. Many scripts call third-party tools that require correct installation and credentials.

---

## Script Categories

### 🔐 Active Directory Pentesting Scripts
| Script Name | Description | Usage |
|-------------|-------------|-------|
| `ad-asrep.sh` | AS-REP Roasting attack | `GetNPUsers.py` wrapper |
| `ad-bloodhound.sh` | BloodHound data collection | Automated BloodHound Python |
| `ad-dcsync.sh` | DCSync attack implementation | `secretsdump.py` wrapper |
| `ad-hashcat-asrep.sh` | Crack AS-REP hashes with Hashcat | Hashcat automation |
| `ad-hashcat-kerberoast.sh` | Crack Kerberoasting hashes | Hashcat automation |
| `ad-kerberoast.sh` | Kerberoasting attack | `GetUserSPNs.py` wrapper |
| `ad-launch-bloodhound.sh` | BloodHound CE startup | Docker automation |
| `ad-passthehash.sh` | Pass-the-Hash attack | `pth-winexe` wrapper |
| `ad-passwordspray.sh` | Password spraying with CrackMapExec | Automated spraying |

---

### 🌐 Web Application Scripts
| Script Name | Description | Usage |
|-------------|-------------|-------|
| `jenkins-rce.sh` | Jenkins RCE via script console | Remote code execution |
| `flask-key-session-generator.py` | Flask session key brute force | Session fixation attacks |
| `ldap-data-exfiltration.py` | LDAP injection data exfiltration | HTB Academy style attacks |
| `lfi-service-check.py` | LFI to service enumeration | Process discovery via LFI |

---

### 🔍 Reconnaissance & Enumeration
| Script Name | Description | Usage |
|-------------|-------------|-------|
| `ipsweep.sh` | Basic IP range ping sweeper | Network discovery |
| `cat-and-search.sh` | File content search utility | Pattern matching in files |
| `email-generator.py` | Email permutation generator | OSINT and user enumeration |

---

### ☁️ Cloud Security Scripts
| Script Name | Description | Usage |
|-------------|-------------|-------|
| `ec2-public-scanner.sh` | AWS EC2 public instance finder | Cloud security assessment |
| `get_access_token_from_azure_app.ps1` | Azure access token retrieval | Cloud privilege escalation |

---

### 🛠️ Utility Scripts
| Script Name | Description | Usage |
|-------------|-------------|-------|
| `anticheater.py` | Duplicate name finder | Competition/CTF utility |
| `vhost_enum.sh` | Virtual host enumeration | Web app reconnaissance |
| `nmap_scan.sh` | Comprehensive port scanning | Network enumeration |
| `dirbust-toolkit.sh` | Directory brute forcing | Web content discovery |
| `setup_machine_folders.sh` | Pentest directory structure | Organized assessment workflow |

---

## Requirements & Prerequisites
- OS: Kali Linux or another pentesting distro (or packages installed on Debian/Ubuntu)
- Python 3.x
- `impacket-scripts`
- `bloodhound` (or BloodHound CE)
- `hashcat`
- `crackmapexec`
- `nmap`
- `dirsearch`
- `gobuster`
- `ffuf`

### Example install on Kali / Debian:
```bash
sudo apt update
sudo apt install -y python3 python3-pip nmap hashcat gobuster
# Many tools are available via apt or pip; use distro packaging / official install guides:
sudo apt install -y impacket-scripts bloodhound crackmapexec dirsearch ffuf
