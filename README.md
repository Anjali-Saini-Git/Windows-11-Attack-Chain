# Windows 11 Attack Chain – Complete VAPT Lab

##  Overview

This repository documents a complete penetration testing attack chain on a Windows 11 target system. The project demonstrates payload generation, advanced evasion techniques, privilege escalation, and persistence – all performed in an isolated, authorized lab environment.

**Key Deliverable:** A formal Vulnerability Assessment & Penetration Testing (VAPT) report with executive summary, findings, and actionable recommendations.

---

##  Objective

To simulate a real-world advanced attack scenario and demonstrate:
- How an attacker can bypass fully enabled Windows Defender
- Privilege escalation from standard user to SYSTEM
- Persistence mechanisms that survive system reboots
- The importance of behavioral detection over static signatures

---

## Repository Contents

| File | Description |
|------|-------------|
| `Final_Project_Attack_Chain.pdf` | Step-by-step technical execution with commands and screenshots |
| `VAPT_Report.pdf` | Formal client-ready report with findings, risk assessment, and recommendations |


---

## Tools Used

| Tool | Purpose |
|------|---------|
| **Metasploit Framework** | Exploitation and post-exploitation |
| **msfvenom** | Payload generation |
| **HollowGhost** | AES-256 encryption + process hollowing |
| **PowerShell** | UAC bypass and defense evasion |
| **Kali Linux** | Attacker machine |
| **Windows 11 Pro** | Target machine (fully updated, Defender enabled) |

---

## Attack Chain Summary

| Phase | Technique | Tool | Result |
|-------|-----------|------|--------|
| 1 | Raw Shellcode Generation | msfvenom | `staged.bin` |
| 2 | AES + Process Hollowing | HollowGhost | `payload.exe`  |
| 3 | USB Delivery | Manual | Payload delivered |
| 4 | Persistence | Startup Folder (install.bat) | Runs on boot |
| 5 | Access | Meterpreter | Session established |
| 6 | Privilege Escalation | UAC Bypass + Migration | SYSTEM access |
| 7 | Defense Evasion | Exclusions | Defender bypassed |

---

## Key Findings

| Finding | Severity | Impact |
|---------|----------|--------|
| Windows Defender Bypass | **Critical** | Full system compromise |
| Privilege Escalation | **Critical** | Administrative access |
| Persistence Mechanism | **High** | Long-term unauthorized access |
| Process Migration | **Medium** | Detection evasion |

---

## VAPT Report

The formal VAPT report includes:
- **Executive Summary** – Overview of findings
- **Scope of Assessment** – Target, tools, methodology
- **Detailed Findings** – Observations, impact, recommendations
- **Risk Assessment Summary** – Prioritized risks
- **Conclusion & Recommendations** – Actionable next steps

---

## Disclaimer

> **This project was conducted in an isolated, controlled lab environment with explicit authorization. All techniques demonstrated are for educational purposes only. The goal is to help security professionals understand attack vectors for better defense. Misuse of this information is strictly discouraged.**

---

## Connect with Me

- **LinkedIn:** [Anjali Saini](https://linkedin.com/in/anjalisaini92)
- **TryHackMe:** [CipherDusk](https://tryhackme.com/p/CipherDusk)

---

⭐ **Star this repo** if you find it helpful!
