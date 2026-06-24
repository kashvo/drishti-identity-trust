# Drishti — Identity Trust Framework

> *From Sanskrit: the watchful eye. A system that never stops watching, never stops learning, and never gets it wrong twice.*

---

## The Problem

Banks verify identity once — at login — and then walk away. But fraud doesn't happen at the door. It happens inside.

Current rule-based systems are rigid. They cannot reason about combinations of signals they haven't seen before. They block genuine users with false positives. They miss real threats with false negatives. And in India, where UPI processes over 8,000 transactions every second - Each one instant, each one final — the system must be right before the money moves, not after.

Bank of Baroda serves an extraordinarily diverse customer base: a farmer in rural Gujarat making his first digital payment, and a startup founder in Mumbai making his fifteenth transfer of the day. Their normal looks nothing alike. A system that treats them the same will fail both.

---

## The Solution

Drishti is an **Agentic AI-powered Identity Trust Framework** that continuously monitors user sessions across all digital banking channels.

Instead of reacting to rules, Drishti **thinks**. It maintains a quiet memory for every user — not their personal details, just their patterns. Their habits. Their normal. And when something breaks that picture, it doesn't immediately block. It **investigates first**, weighs what it knows, and then decides.

---

## How It Works

```
User Action (login / transaction / device change / account recovery)
        ↓
Signal Collection
(device fingerprint · location · behavioural signals · transaction context)
        ↓
Context Builder
(live signals compared against per-user memory profile)
        ↓
Agentic AI Brain — ReAct Loop
THINK → ACT (call tools) → OBSERVE → THINK → DECIDE
        ↓
Decision + Full Explanation
(Allow · Soft Verify OTP · Hard Verify Video KYC · Block)
        ↓
Memory Update
(user profile learns from this session)
        ↓
Audit Log Created
(full reasoning chain stored for RBI compliance)
```

---

## Key Features

**Continuous Session Monitoring**
Identity is verified throughout the entire session — not just at login. Behaviour is watched at every step.

**Per-User Memory Profiles**
Every user has a lightweight profile capturing their behavioural baseline. The system learns what normal looks like for each individual — not a generic average.

**Agentic AI Reasoning**
The system uses a shared AI agent brain with a ReAct reasoning loop. It thinks, calls tools to investigate, observes results, and decides — the way a human fraud analyst would, at machine speed.

**Explainable Decisions**
Every decision comes with a full reasoning chain. Not just a risk score — a clear explanation of *why*, auditable for RBI compliance.

**Privacy First**
Stores behaviour patterns, not raw personal data. Compliant with India's DPDP Act and RBI Cybersecurity Framework.

**Adaptive Learning**
After every session, the user's memory profile updates. The system gets smarter and less disruptive over time.

---

## Risk Coverage

- Account Takeover (ATO)
- KYC Fraud
- Insider Threats & Privileged Access Misuse
- Suspicious Onboarding & Account Recovery
- New Device Risk
- Behavioural Anomalies
- Session Hijacking

---

## Technology Stack

| Layer | Technology |
|---|---|
| Agent Brain | Large Language Model API with ReAct Framework |
| User Memory | JSON-based per-user profiles |
| Backend | Python, FastAPI |
| Frontend / Dashboard | Streamlit |
| User Simulation | Faker, Locust |
| Location Intelligence | IP Geolocation API |
| Device Trust | Device Fingerprinting |
| Privacy | Data minimisation, hashed identifiers, DPDP-compliant storage |

---

## Architecture

```
ONE SHARED AGENT BRAIN
         +
MILLIONS OF INDIVIDUAL MEMORY PROFILES
         =
Personalised decisions at scale
without the cost of individual agents
```

Each user gets their own memory. The agent reads it fresh every time. Adding users means adding a lightweight JSON file — not adding compute. The architecture is designed for cloud deployment at India's UPI scale.

---

## Demo

> Prototype under active development as part of PSB Hackathon Series 2026 — Bank of Baroda x IIT Gandhinagar.

---

## Team Drishti

PSG College of Technology, B.Tech Information Technology

*Built for the PSB Hackathon Series 2026 — Cybersecurity & Fraud Domain*
*Guided by the Department of Financial Services, Ministry of Finance, Government of India*
