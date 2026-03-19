# Analysis: Week 1 Gap Resolution — Security Controls & Cryptography

**Date:** 19 March 2026
**Domain:** CompTIA Security+ SY0-701 — Domain 1.0, 1.1, 1.2, 1.3, 1.4
**Type:** Post-exam gap analysis and resolution

---

## Context

After completing the Week 1 mini-exam (19/25 = 76%), six gaps were identified. This document records the analysis, the corrected understanding, and the exam-ready answers.

---

## Gap 1 — Implicit Trust Zone

**Question:** An employee inside the corporate network accesses HR data freely because they are already inside the perimeter. What security model is this?

**Wrong answer given:** Physical

**Why it was wrong:** Physical is a control category. The question asked for a security model — specifically the concept that Zero Trust was designed to eliminate.

**Correct answer:** Implicit trust zone (legacy perimeter model)

**Explanation:** Traditional perimeter security assumes that anything inside the network boundary is trusted. Zero Trust eliminates this by requiring verification of every access request regardless of source location — inside or outside the perimeter.

**Exam trigger:** "trusted because inside the network" = implicit trust zone. The fix = Zero Trust.

---

## Gap 2 — Fire Suppression Control Category

**Question:** An automated fire suppression system activates when smoke is detected. What category and type?

**Wrong answer given:** Physical + Corrective

**Why it was wrong:** Physical controls are tangible things you touch — locks, bollards, fences. An automated system uses sensors, logic processing, and triggered responses — that is software and hardware combined = Technical.

**Correct answer:** Technical + Corrective

**Rule:** Anything automated = Technical category. The Corrective type was right — it responds to an incident to minimise damage.

---

## Gap 3 — Non-Repudiation vs Hashing

**Question:** Prove a software update was not modified AND came from the legitimate vendor.

**Wrong answer given:** Hashing (SHA-256)

**Why it was wrong:** Hashing proves integrity — the file was not changed. It does not prove origin. Anyone can hash a file. Non-repudiation requires proof that a specific private key holder created it — only one person in the world has that key.

**Correct answer:** Digital signature

**Process:**
1. Vendor hashes the software package
2. Vendor encrypts the hash with their private key = digital signature
3. Recipient decrypts with vendor's public key and rehashes to verify
4. Match = unmodified AND from the legitimate vendor

**Exam rule:** Non-repudiation = digital signature. Hashing alone = integrity only.

---

## Gap 4 — Emergency Change Process vs Ownership

**Question:** A critical zero-day patch needs immediate deployment. Normal 5-day CAB review is not possible. What change management element allows this?

**Wrong answer given:** Ownership

**Why it was wrong:** Ownership identifies who is accountable if a change goes wrong — it is not a bypass mechanism.

**Correct answer:** Emergency change process

**Distinction:**
- Ownership = accountability (who is responsible)
- Emergency change process = expedited approval pathway for critical patches requiring immediate action
- Both are change management elements but they serve different purposes

---

## Gap 5 — Visitor Log Control Type

**Question:** A guard writes visitor names, arrival times, and departure times in a physical book. What category and type?

**Wrong answer given:** Physical + Deterrent/Preventive (then Operational + Directive)

**Why it was wrong:** Directive tells people what to do — a policy document, an AUP, a procedure. A log does not tell anyone to do anything. It records what happened after the fact.

**Correct answer:** Operational + Detective

**Distinction:**
- Directive = instructs (AUP, security policy, password policy)
- Detective = records/identifies (logs, CCTV footage, audit trails, IDS alerts)
- Operational = people and process controls (guards, training, procedures)

---

## Gap 6 — Downgrade Attack vs MITM

**Question:** An attacker intercepts a TLS 1.3 connection and forces both parties to use TLS 1.0 with RC4. What is this attack?

**Wrong answer given:** Man-in-the-Middle (MITM)

**Why it was wrong:** MITM describes the attacker's position — intercepting traffic between two parties. It does not describe what the attacker did from that position.

**Correct answer:** Downgrade attack

**Distinction:**
- MITM = where the attacker stands (between client and server)
- Downgrade attack = what the attacker does (forces weaker cipher/protocol version)
- An attacker can use MITM positioning to execute a downgrade attack — they are not the same thing

**Additional gaps identified (Week 2 carry-forward):**
- BEC vs Spear Phishing: BEC = no link, executive impersonation, wire transfer. Spear phishing = targeted email with malicious link/attachment.
- BEC controls: DMARC/SPF/DKIM + out-of-band verification policy.

---

## Summary Table

| Gap | Correct Answer | Status |
|---|---|---|
| Implicit trust zone | Implicit trust zone / legacy perimeter model | Closed |
| Fire suppression category | Technical + Corrective | Closed |
| Non-repudiation mechanism | Digital signature | Closed |
| Emergency change exception | Emergency change process | Closed |
| Visitor log type | Operational + Detective | Closed |
| Downgrade attack | Downgrade attack (not MITM) | Closed |

---

*Lab documented as part of the [cryptasphere-labs](https://github.com/Nsindamanzi/cryptasphere-labs) portfolio.*
*Author: Thamsanqa Ngwenya — CryptaSphere, Bulawayo, Zimbabwe*
