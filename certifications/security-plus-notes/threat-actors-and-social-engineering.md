# Lab: Threat Actors, Attack Vectors & Social Engineering

**Date:** 19 March 2026
**Environment:** Study session + scenario-based drills
**Domain:** CompTIA Security+ SY0-701 — Domain 2.1, 2.2
**Type:** Concept application + scenario analysis

---

## Objective

Identify threat actor types, attack vectors, and social engineering techniques from scenario descriptions. Apply the 80/20 principle — exam scenarios, not theory recitation.

---

## Threat Actor Classification

### Types and Attributes

| Actor | Resources | Sophistication | Primary Motivation |
|---|---|---|---|
| Nation-state | Very high (gov funded) | Very high (zero-days) | Espionage, sabotage, disruption |
| Organised crime | High | High | Financial gain |
| Hacktivist | Low–medium | Medium | Ideology, political message |
| Insider threat | Varies (already has access) | Varies | Revenge, financial, negligence |
| Shadow IT | Low | Low | Convenience — not malicious |
| Script kiddie | Low | Very low | Notoriety, curiosity |

### Key Exam Attributes

- **Internal vs External** — insiders already have legitimate access; external actors must breach first
- **Intent** — intentional (malicious) vs unintentional (negligent employee clicking phishing link)
- **Resources** — nation-states have government budgets; hacktivists operate on minimal resources
- **Sophistication** — nation-states write zero-days; script kiddies download tools they do not understand

---

## Scenario Drills — Threat Actors

| Scenario | Actor | Reasoning |
|---|---|---|
| Power grid attack, no ransom, sophisticated TTPs | Nation-state | Critical infrastructure + no financial motive + high sophistication |
| Website defaced with political messaging, public claim | Hacktivist | Ideology driven, public visibility goal |
| Employee copies customer DB to USB before resigning | Insider threat | Already has access, intentional data theft |
| Random port scanning with downloaded automated tool | Script kiddie | No specific target, pre-built tools, low sophistication |

---

## Attack Vectors — Domain 2.2

### Message-Based Vectors (Highest Frequency on Exam)

| Vector | Target | Key Identifier |
|---|---|---|
| Phishing | Mass audience | Generic email, malicious link/attachment |
| Spear phishing | Specific named individual | Personalised, researched content |
| Whaling | Executives (CEO, CFO) | High-value target, financial or data impact |
| Vishing | Any | Voice call, impersonation, urgency |
| Smishing | Any | SMS with malicious link |
| BEC | Finance teams | Impersonates executive, requests wire transfer — NO link |

### Other Attack Vectors

| Vector | Definition |
|---|---|
| Supply chain | Compromise vendor/update to reach the real target |
| Watering hole | Compromise a site the target regularly visits |
| Typosquatting | Register lookalike domain — `cryptasph3re.co.zw` |
| Brand impersonation | Fake email/site mimicking trusted brand |
| Removable media | USB drop attack — infected USB left in car park |
| Shadow IT / BYOD | Unapproved apps/devices expanding attack surface without IT knowledge |

### BEC vs Spear Phishing — Critical Distinction

| | BEC | Spear Phishing |
|---|---|---|
| Contains link? | No | Usually yes |
| Contains attachment? | No | Sometimes |
| Goal | Wire transfer / credential theft via impersonation | Click malicious link / open attachment |
| Impersonates | Executive (CEO, CFO) | Any trusted contact |
| Exam trigger | "urgent wire transfer", "new supplier account" | "targeted email with link" |

---

## Scenario Drills — Attack Vectors

| Scenario | Vector | Reasoning |
|---|---|---|
| CFO receives personalised exec email requesting wire transfer | Whaling / BEC | Executive target + wire transfer = BEC; highly personalised = whaling angle |
| Software update server compromised, all customers infected | Supply chain | Attacker reached targets through a trusted vendor |
| Fake domain `cryptasph3re.co.zw` with login page | Typosquatting | Lookalike domain to capture credentials |
| Attacker embeds malware on a site the target frequently visits | Watering hole | Compromised third-party site used as delivery mechanism |
| Employees using personal cloud storage for work files | BYOD / Shadow IT | Unapproved service, IT has no visibility or control |

---

## Social Engineering Techniques

### Psychological Triggers

| Trigger | Attack example |
|---|---|
| Authority | "I'm from IT — you must comply immediately" |
| Urgency | "Your account will be locked in 10 minutes" |
| Scarcity | "This is your last chance to verify" |
| Social proof | "Everyone on your team has already done this" |
| Familiarity | Attacker uses LinkedIn research to reference real names and projects |
| Intimidation | "Failure to comply will result in disciplinary action" |

### Physical and Observational Techniques

| Technique | Definition |
|---|---|
| Pretexting | Fabricated scenario to manipulate — "I'm from the bank's fraud team" |
| Impersonation | Posing as someone trusted physically or digitally |
| Tailgating | Following someone through a secured door without authenticating |
| Dumpster diving | Retrieving discarded documents, hardware, or printed data |
| Shoulder surfing | Observing someone enter credentials or PIN |

---

## Scenario Drills — Social Engineering

| Scenario | Technique | Triggers Used |
|---|---|---|
| IT help desk call demanding immediate password verification | Vishing + pretexting | Authority + Urgency |
| Searching company recycling bins for printed emails and org charts | Dumpster diving | N/A |
| Attacker uses LinkedIn to reference real manager and project, requests system access | Pretexting + Familiarity | Familiarity — victim assumes attacker must be genuine |
| Observing someone enter PIN at ATM | Shoulder surfing | N/A |
| Attacker impersonates CEO via email requesting urgent $45,000 wire transfer | BEC | Authority (CEO impersonation) + Urgency (travelling, act now) |

---

## Key Exam Rules

- Nation-state = critical infrastructure + no ransom + high sophistication
- BEC has no malicious link — it is purely social manipulation via impersonation
- Whaling = spear phishing against executives specifically
- BYOD = personal device risk; Shadow IT = unapproved app/service risk
- Dumpster diving is a legitimate attack vector — physical OSINT
- Tailgating and shoulder surfing are physical social engineering — no tech required

---

## Exam Concepts Mapped to SY0-701

| Topic | Domain |
|---|---|
| Threat actor types and attributes | 2.1 |
| Attack vectors — message, physical, supply chain | 2.2 |
| Social engineering techniques | 2.2 |
| BEC vs spear phishing distinction | 2.2 |
| Psychological triggers in SE attacks | 2.2 |

---

*Lab documented as part of the [cryptasphere-labs](https://github.com/Nsindamanzi/cryptasphere-labs) portfolio.*
*Author: Thamsanqa Ngwenya — CryptaSphere, Bulawayo, Zimbabwe*
