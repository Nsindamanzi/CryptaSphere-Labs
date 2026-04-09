# CryptaSphere Security+ SY0-701 Study App

A locally-hostable, zero-dependency flashcard and quiz app built for CompTIA Security+ SY0-701 exam preparation.

## Features

- **65 Flashcards** across all 5 SY0-701 domains with full definitions
- **Quiz Mode** — 45 MCQ questions with domain filtering, configurable count (10/20/50), instant feedback and explanations
- **Progress Tracking** — per-domain mastery %, quiz history, session log (persists via localStorage)
- **Gap Tracker** — pre-loaded with flagged weak areas, fully editable
- **Terminal-style UI** — green-on-black, Orbitron/Share Tech Mono, CryptaSphere branding

## Usage

No install, no server, no internet required.

```bash
# Just open the HTML file in any browser
xdg-open cryptasphere-secplus.html
# or double-click in your file manager
```

## Domain Coverage

| Domain | Weight | Cards | Questions |
|--------|--------|-------|-----------|
| 1.0 General Security Concepts | 12% | 15 | 5 |
| 2.0 Threats, Vulnerabilities & Mitigations | 22% | 17 | 7 |
| 3.0 Security Architecture | 18% | 15 | 5 |
| 4.0 Security Operations | 28% | 15 | 5 |
| 5.0 Security Program Management & Oversight | 20% | 13 | 5 |

## Extending

Add cards to the `CARDS` array and questions to the `QUESTIONS` array at the top of the HTML file. Each follows a simple object schema — no build step needed.

## Built by

[CryptaSphere](https://github.com/Nsindamanzi/cryptasphere-labs) · Bulawayo, Zimbabwe
