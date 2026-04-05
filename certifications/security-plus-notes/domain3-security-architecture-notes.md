# Domain 3.0 — Security Architecture Study Notes

**Date:** April 2026
**Domain:** CompTIA Security+ SY0-701 — Domain 3.0 (18% of exam)
**Mini-exam result:** 24/25 = 96% ✅ PASS

---

## 3.1 Cloud Models

### Service Models

| Model | You manage | Provider manages | Exam trigger |
|---|---|---|---|
| IaaS | OS, apps, data | Hardware, hypervisor | "manage the OS", "EC2", "VMs" |
| PaaS | Apps and data only | OS, runtime, everything else | "push code only", "Heroku", "no OS management" |
| SaaS | Data and user access | Everything | "just log in", "Microsoft 365", "Gmail" |

### Deployment Models

| Model | Definition |
|---|---|
| Public cloud | Multi-tenant, shared infrastructure — AWS, Azure, GCP |
| Private cloud | Single organisation, dedicated resources |
| Hybrid cloud | Mix of on-premises and public cloud |
| Community cloud | Shared by organisations with common requirements |

### Key Concepts

- **IaC (Infrastructure as Code)** — infrastructure defined in version-controlled code files, deployed automatically. Risk: one bad template = thousands of misconfigured resources.
- **Containers** — lightweight, share host OS kernel. Risk: container escape.
- **Serverless** — event-driven, no server management. Risk: code vulnerabilities still your responsibility.
- **Shared responsibility** — provider secures the cloud. You secure what's in it.

---

## 3.2 Network Security

### Network Segmentation & Zones

| Zone | Definition |
|---|---|
| DMZ | Buffer zone between internet and internal network — hosts public-facing servers |
| Air-gapped network | Physically isolated, zero connectivity |
| VLAN | Logical separation of traffic on same physical hardware |
| Microsegmentation | Per-workload security policy — limits lateral movement |

### Firewall Types

| Type | What it inspects | Exam trigger |
|---|---|---|
| Packet filtering | IP, ports only | "Layer 3/4", "stateless" |
| Stateful | Connection state | "tracks sessions" |
| WAF | HTTP/HTTPS only — blocks SQLi, XSS | "web application", "HTTP traffic" |
| UTM | All-in-one appliance | "single box", "firewall + AV + IPS" |
| NGFW | Application identity regardless of port | "app-aware", "Layer 7", "port 443 identified as file-sharing" |

### IDS vs IPS

| | IDS | IPS |
|---|---|---|
| Position | Passive — mirrors traffic | Inline — traffic passes through |
| Action | Alerts only | Blocks |
| Exam trigger | "passive", "alerts only", "never drops" | "inline", "drops packets", "prevents" |

### VPN & Secure Protocols

| Protocol | Use case | Exam trigger |
|---|---|---|
| IPSec Tunnel mode | Site-to-site VPN — full packet encryption | "two offices", "gateway-to-gateway" |
| SSL VPN | Browser-only, no client software | "hotel laptop", "browser only", "port 443" |
| SFTP | Encrypted file transfer over SSH | "secure file transfer", "replace FTP" |
| SASE | Cloud-delivered VPN + firewall + CASB combined | "replace separate appliances", "single cloud service" |

---

## 3.3 Data Protection

### Data States

| State | Definition | Protection |
|---|---|---|
| At rest | Stored on disk, USB, backup | Encryption (AES-256, BitLocker) |
| In transit | Moving across a network | TLS, HTTPS, VPN, SFTP |
| In use | Being processed in RAM | Access controls, secure enclaves |

### Protection Techniques

| Technique | Definition | Exam trigger |
|---|---|---|
| Tokenisation | Replaces real data with random token — real data in secure vault | "payment cards", "random reference" |
| Data masking | Realistic but fake data for test environments | "developers", "test data", "fake but realistic" |
| Salting | Random string added before hashing — prevents rainbow table attacks | "random string", "password storage" |
| Hashing | One-way transformation — integrity verification | "cannot be reversed", "SHA-256" |
| DLP | Monitors and blocks data leaving the organisation | "blocks email", "prevents upload", "auto-detects sensitive data" |
| IRM/DRM | Controls what recipients can do with data they have | "can't forward", "can't print", "can't copy" |

---

## 3.4 Resilience & Recovery

### Backup Types

| Type | Backs up | Speed to backup | Speed to restore |
|---|---|---|---|
| Full | Everything | Slowest | Fastest |
| Incremental | Changes since last backup (any) | Fastest | Slowest |
| Differential | Changes since last full backup | Medium | Medium |

**Restore order for incremental:** Full backup FIRST, then each incremental in chronological sequence.

### Recovery Metrics

| Metric | Definition |
|---|---|
| RTO | Maximum acceptable downtime — how fast must you recover? |
| RPO | Maximum acceptable data loss measured in time |

### Resilience Concepts

| Concept | Definition |
|---|---|
| Fault tolerance | Continues operating even when a component fails — zero interruption |
| High availability | Designed for maximum uptime — close to 100% |
| Redundancy | Duplicate components — no single point of failure |
| Replication | Real-time copy to secondary site |

---

## 3.5 Embedded & Specialised Systems

| System | Security concern | Mitigation |
|---|---|---|
| SCADA/ICS | Legacy, unpatched, increasingly internet-connected | Network segmentation, IDS monitoring |
| IoT | Default credentials, no patching | Change credentials, isolate on separate VLAN |
| RTOS | Timing-critical — cannot tolerate latency from security controls | Compensating controls only |
| Embedded | Firmware vulnerabilities, rarely updated | End-of-life classification + compensating controls |

**Key rule:** Specialised systems prioritise availability and safety over confidentiality. You cannot simply patch or reboot a power grid controller or a pacemaker.

---

## Mini-Exam Analysis

**Score:** 24/25 = 96% ✅
**Q4 gap:** IaC — "infrastructure defined in code files, version-controlled, deployed automatically" = Infrastructure as Code. Not SDN (which controls live traffic routing).

---

*Lab documented as part of the [cryptasphere-labs](https://github.com/Nsindamanzi/cryptasphere-labs) portfolio.*
*Author: Thamsanqa Ngwenya — CryptaSphere, Bulawayo, Zimbabwe*
