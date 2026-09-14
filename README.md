# Vulnerability Assessment and Penetration Testing (VAPT)

A hands-on Vulnerability Assessment and Penetration Testing (VAPT) project
conducted against intentionally vulnerable laboratory environments and
documented as a simulated client engagement.

##  Overview

This project simulates a professional VAPT engagement for:

**Rabbit Pvt. Ltd. — Simulated Client**

The assessment focused on reconnaissance, service enumeration,
vulnerability identification, and controlled exploitation/validation of
intentionally vulnerable systems in an isolated laboratory environment.

The project covers both network/service-level and web application
vulnerabilities.

## Scope

The assessment covered the following intentionally vulnerable targets:

- **Metasploitable 2**
- **Bee-Box / bWAPP**
- **DVWA** — included within the project scope

All testing was performed within a controlled laboratory environment.

---

## Assessment Workflow

The assessment was organized into two major stages.

### 1. Reconnaissance & Enumeration

The reconnaissance phase involved gathering information about the target
systems and identifying available services and technologies.

Tools used included:

- dig
- smbclient
- Gobuster
- enum4linux
- Nmap
- Nmap NSE Scripts
- WhatWeb
- IP / network identification

Evidence for this phase is organized under:
screenshots/
└── reconnaissance/

##2. Vulnerability Assessment & Exploitation
The identified services and applications were assessed for vulnerabilities.
Where applicable, vulnerabilities were validated through controlled testing
within the laboratory environment.
Evidence is organized by target and vulnerability:
screenshots/
└── vulnerabilities_and_exploits/

Metasploitable 2
The following areas were assessed on Metasploitable 2:
- UnrealIRCd — Backdoor Remote Code Execution
- Samba — Username Map Script Remote Code Execution
- VSFTPD — Exploitation attempted but not confirmed
- PHP — Information Disclosure
Key Findings
Severity	Finding
Critical	UnrealIRCd Backdoor RCE
Critical	Samba Username Map Script RCE
Medium	  PHP Information Disclosure

The VSFTPD exploitation attempt was not treated as a confirmed finding because
an active session was not successfully established.

bWAPP
The following web application vulnerabilities were assessed in bWAPP:
- SQL Injection
- Reflected Cross-Site Scripting (XSS)
Key Findings
Severity	Finding
High	SQL Injection
Medium	Reflected XSS


## Tools & Technologies
- Kali Linux
- Nmap
- Nmap NSE Scripts
- Metasploit Framework
- Gobuster
- enum4linux
- smbclient
- dig
- WhatWeb
- Metasploitable 2
- Bee-Box / bWAPP
- DVWA

## Repository Structure
VAPT/
│
├── README.md
│
├── report/
│   └── VAPT_Report.pdf
│
└── screenshots/
    │
    ├── reconnaissance/
    │   ├── dig/
    │   ├── smbclient/
    │   ├── gobuster/
    │   ├── enum4linux/
    │   ├── nmap/
    │   ├── nse_script/
    │   ├── whatweb/
    │   └── IP/
    │
    └── vulnerabilities_and_exploits/
        │
        ├── metasploitable/
        │   ├── unrealircd/
        │   ├── samba/
        │   ├── vsftpd_attempted/
        │   └── php_disclosure/
        │
        └── bwapp/
            ├── sqli/
            └── xss/
## Evidence
The screenshots/ directory contains supporting evidence from the
assessment.
The evidence is separated into:
- Reconnaissance — tool-specific enumeration and information gathering
- Vulnerabilities & Exploits — findings grouped by target and vulnerability
Unsuccessful or unconfirmed testing is retained and clearly labeled to
accurately represent the assessment process.
  report
The complete VAPT documentation, including findings, evidence, impact,
and recommendations, is available in:
[VAPT Report](report/VAPT_Report.pdf)

## Learning Outcomes
This project provided practical experience with:
- Reconnaissance and information gathering
- Network and service enumeration
- Web application security testing
- Vulnerability identification
- Vulnerability validation
- Controlled exploitation in an isolated environment
- Risk assessment
- Security documentation and reporting

## Disclaimer
Rabbit Pvt. Ltd. is a simulated client created for educational purposes.
All testing documented in this repository was performed against intentionally
vulnerable laboratory environments.
No unauthorized systems or real-world organizations were targeted.
This repository is intended solely for educational and portfolio purposes.
