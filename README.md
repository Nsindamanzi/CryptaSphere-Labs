# CryptaSphere-Labs
cryptasphere-labs

> **Security research, lab documentation, and professional portfolio by Thamsanqa Ngwenya**
> Bulawayo, Zimbabwe · CompTIA Security+ SY0-701 (in progress) · Founder @ CryptaSphere

---

## Who This Is For

Recruiters, hiring managers, and clients looking for evidence of hands-on security skills — not just certifications. Every folder in this repo is a lab I built, broke, fixed, and documented.

Target roles: SOC Analyst I · Junior Penetration Tester · Junior Network Administrator · Systems Administrator

---

## Repository Structure

```
cryptasphere-labs/
│
├── 01-cryptography/
│   ├── openssl-self-signed-cert/        ← Lab write-up + commands
│   ├── key-exchange-analysis/           ← DHE vs RSA vs ECDHE notes
│   └── hashing-and-salting/             ← Concepts + demo scripts
│
├── 02-network-security/
│   ├── ufw-firewall-rules/              ← Ubuntu UFW config + nmap test results
│   ├── nmap-enumeration/                ← Kali scanning lab write-ups
│   └── wireshark-packet-analysis/       ← Packet captures + annotated findings
│
├── 03-siem-and-monitoring/
│   ├── wazuh-deployment/                ← Full Wazuh SIEM setup (Ubuntu)
│   ├── alert-triage/                    ← Real alert analysis + decisions
│   └── rule-tuning/                     ← False positive reduction write-ups
│
├── 04-incident-response/
│   ├── ransomware-tabletop/             ← IR scenario walkthrough
│   ├── ir-playbooks/                    ← Detection → Containment → Recovery
│   └── forensics-chain-of-custody/      ← Evidence handling procedures
│
├── 05-vulnerability-management/
│   ├── metasploitable-labs/             ← Controlled exploitation + CVSS scoring
│   ├── cvss-scoring-exercises/          ← Real CVE scoring practice
│   └── remediation-reports/             ← Client-style findings reports
│
├── 06-hardening/
│   ├── linux-baseline-hardening/        ← Ubuntu hardening checklist + scripts
│   ├── ssh-configuration/               ← Secure SSH setup
│   └── service-minimisation/            ← Attack surface reduction
│
├── 07-pen-testing-basics/
│   ├── recon-methodology/               ← Passive + active recon write-ups
│   ├── kali-tooling/                    ← Netdiscover, Nikto, nmap workflows
│   └── reporting-template/              ← Professional findings report template
│
└── certifications/
    ├── security-plus-notes/             ← Domain-by-domain study notes
    └── exam-prep/                       ← Practice question analysis
```

---

## Labs Completed

| Lab | Folder | Skills Demonstrated | Date |
|-----|--------|--------------------|----|
| OpenSSL Self-Signed Certificate | `01-cryptography/openssl-self-signed-cert` | PKI, CSR generation, cert inspection | Mar 2026 |
| Wazuh SIEM Deployment | `03-siem-and-monitoring/wazuh-deployment` | SIEM setup, agent enrollment, alert config | Mar 2026 |

*Updated after every lab session.*

---

## Skills Index

**Defensive / Blue Team**
- SIEM deployment and alert triage (Wazuh)
- Incident response lifecycle
- Digital forensics fundamentals
- Vulnerability scanning and CVSS scoring
- Linux system hardening

**Networking**
- Firewall configuration (UFW)
- Packet analysis (Wireshark)
- Network enumeration (nmap, Netdiscover)
- VPN and tunneling concepts

**Cryptography**
- PKI and certificate management (OpenSSL)
- Key exchange protocols (DHE, ECDHE, RSA)
- Hashing, salting, digital signatures

**Tools**
`Wazuh` `Kali Linux` `nmap` `Wireshark` `OpenSSL` `UFW` `Metasploit` `Nikto` `Netdiscover`

---

## Certifications

| Cert | Status | Expected |
|------|--------|----------|
| CompTIA Security+ SY0-701 | In Progress | May 2026 |

---

## About CryptaSphere

CryptaSphere is a cybersecurity consultancy based in Zimbabwe serving the SME market — a sector where cyber defences are largely underdeveloped. This repository documents the technical foundation being built to support CryptaSphere's service delivery.

**Contact:** thamueengwenya@gmail.com
**LinkedIn:** https://www.linkedin.com/in/thamsanqa-ngwenya-77405028b?utm_source=share_via&utm_content=profile&utm_medium=member_ios

---

*Last updated: March 2026*
