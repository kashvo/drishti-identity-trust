<div align="center">

# 👁️ Drishti
### *The watchful eye. Continuous. Contextual. Certain.*

[![Status](https://img.shields.io/badge/Status-Active_Development-brightgreen?style=flat-square)]()
[![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=flat-square&logo=python&logoColor=white)](https://python.org)
[![Dashboard](https://img.shields.io/badge/Dashboard-Streamlit-FF4B4B?style=flat-square&logo=streamlit&logoColor=white)](https://streamlit.io)
[![AI](https://img.shields.io/badge/AI-Agentic_Reasoning_Engine-7F77DD?style=flat-square)]()
[![Privacy](https://img.shields.io/badge/Privacy-DPDP_Act_Compliant-0F6E56?style=flat-square)]()
[![License](https://img.shields.io/badge/License-MIT-yellow?style=flat-square)]()
[![Hackathon](https://img.shields.io/badge/PSB_Hackathon-2026-orange?style=flat-square)](https://bankofbaroda.in)

**A privacy-first, Agentic AI-powered Identity Trust Framework for continuous digital banking security.**

*PSB Hackathon Series 2026 · Bank of Baroda × IIT Gandhinagar*
*Domain: Cybersecurity & Fraud — Identity Trust, Protection & Safety*

[Problem](#the-problem) · [Real-World Context](#real-world-context) · [Solution](#the-solution) · [Architecture](#architecture) · [How It Works](#how-it-works) · [Features](#key-features) · [Tech Stack](#technology-stack) · [Research](#research-foundation) · [Team](#team-drishti)

</div>

---

## The Problem

Banks verify identity once — at login — and then walk away. But fraud doesn't happen at the door. It happens inside.

Current rule-based systems are rigid. They cannot reason about combinations of risk signals they have not seen before. They block genuine users with false positives and miss real threats with false negatives. In India, where UPI processes over **8,000 transactions every second** — each one instant and irreversible — the system must be right before the money moves, not after.

Today's threats go further. Generative AI can clone a customer's voice in seconds. Deepfake tools replicate faces convincingly enough to fool verification systems. Fraudsters no longer steal credentials. They manufacture identities. Systems that rely on a single signal — a voice match, a face scan, a known device — are no longer sufficient.

Bank of Baroda serves an extraordinarily diverse customer base: a farmer in rural Gujarat making his first digital payment, and a startup founder in Mumbai making his fifteenth transfer of the day. Their normal looks nothing alike. A system that treats them the same will fail both.

> **In FY2024-25, over 6.32 lakh UPI fraud cases were reported in India with losses exceeding ₹485 crore.** The IMF has formally noted that traditional fraud models are becoming ineffective and that the industry must shift from single authentication to **continuous identity verification**. Yet most banking systems still verify identity only once — at the door.

---

## Real-World Context

Drishti is not built for a hypothetical problem. Bank of Baroda has faced real, documented fraud incidents — each one a failure that continuous agentic identity monitoring could have prevented.

| Incident | What Happened | How Drishti Prevents It |
|---|---|---|
| **bob World App Crisis (2023)** | Bank agents linked unauthorized mobile numbers to over 4.22 lakh customer accounts to boost app registrations. RBI banned new onboarding. ₹22 lakh stolen from 362 customers. | Agent flags account detail changes as high-risk events and triggers hard verification before any mobile number change is saved |
| **RBI Currency Chest Theft (2026)** | A joint custodian at BoB's Ahmedabad branch manipulated e-Kuber portal records to steal ₹8.70 crore over four months — undetected until a routine RBI inspection | Continuous privileged access monitoring detects unusual portal activity patterns. Four months of anomalous behaviour would have been flagged on day one |
| **Gold Loan Fraud (2025)** | Accused conspired with a bank valuer to approve gold loans against fake ornaments using forged valuation certificates across multiple accounts | Agent cross-validates transaction patterns and flags collusion signals — multiple accounts, same valuer, same branch, same time window |
| **₹9 Crore Loan Fraud (2026)** | A 53-person network including bank staff used fake identities and forged documents across multiple districts to secure and withdraw loans | KYC signal cross-validation and identity trust scoring detects synthetic identity patterns and flags document-based anomalies in real time |
| **Digital Arrest Scams** | Fraudsters impersonating authorities coerce customers into transferring large sums under psychological pressure | Behavioural biometrics detect distressed navigation patterns — rushed clicks, unusual transfer amounts, unknown beneficiaries — and trigger intervention mid-session |

> *These are not edge cases. They are systemic failures — of monitoring, of verification, and of trust. Drishti addresses each one at the architectural level.*

---

## The Solution

**Drishti** is an Agentic AI-powered Identity Trust Framework that continuously monitors user sessions across all digital banking channels — not just at login, but across every action, every screen, every transaction.

> **Identity is not a one-time event. It is a continuously updated state. That is the architectural shift Drishti introduces.**

It maintains a quiet memory for every user — not their personal details, just their patterns. Their habits. Their normal. When something breaks that picture, Drishti does not immediately block. It **investigates first**, reasons through the evidence, and then decides — the way a human fraud analyst would, at machine speed.

No single signal makes a decision. A deepfake can clone a voice. It cannot simultaneously replicate how someone types, how they navigate, what they usually transfer, which device they always use, and where they always transact from — all at once, in real time. **That combination is what Drishti watches.**

---

## Why Drishti is Different

> *The difference between a security camera that records and a security guard that understands.*

| What Exists Today | Drishti |
|---|---|
| Verifies identity at login only | Monitors the entire session continuously |
| Rule-based and rigid | Reasons contextually about every signal combination |
| One-size-fits-all fraud model | Personalised baseline per user |
| Black box risk score | Full reasoning chain with explanation |
| Reacts after fraud occurs | Investigates before deciding |
| Batch processing after transaction | Stream processing during authorization |
| Trusts a single biometric signal | Cross-validates across all signals simultaneously |
| Vulnerable to deepfakes and voice clones | Deepfake-aware multi-modal verification |
| Cannot explain its decisions | Full audit trail for RBI compliance |

---

## Architecture

**One shared agent brain. Millions of individual memory profiles.**

Every user has a lightweight JSON profile capturing their behavioural baseline. The agent reads this profile fresh at every event — same brain, different context every time. Adding users means adding a JSON file, not adding compute. Personalised decisions at scale, without the cost of individual agents.

> Research validated: The World Journal of Advanced Research (2025) confirms that per-user behavioural profiling with stream processing architecture achieves fraud detection **during** payment authorization rather than after — the exact model Drishti implements.

The system is optimised for low-latency authorization workflows — designed to make decisions fast enough for UPI's instant, irreversible payment window.

**Sample user memory profile:**

```json
{
  "user_id": "U10234",
  "account_type": "savings",
  "kyc_verified": true,
  "onboarding_date": "2024-01-15",

  "behaviour_baseline": {
    "usual_login_times": ["8am-10am", "6pm-9pm"],
    "usual_devices": [
      {
        "fingerprint_hash": "a3f8c9d2",
        "label": "iPhone 13",
        "first_seen": "2024-01-15",
        "times_seen": 847
      }
    ],
    "usual_locations": ["Bengaluru", "Chennai"],
    "known_ip_hashes": ["b7d2e4f1", "c9a3d8e2"],
    "avg_transaction_amount": 8000,
    "max_ever_transaction": 50000,
    "usual_beneficiaries": ["ACC123", "ACC456"],
    "avg_sessions_per_week": 4,
    "usual_navigation_pattern": ["balance", "transactions", "transfer"],
    "avg_typing_speed_ms": 320,
    "avg_session_duration_mins": 6
  },

  "risk_history": {
    "identity_trust_score": 92,
    "past_flags": 0,
    "last_suspicious_event": null,
    "verified_new_locations": ["Mumbai"],
    "blacklisted_devices": []
  },

  "compliance": {
    "dpdp_consent_given": true,
    "data_minimisation": true,
    "last_profile_audit": "2026-06-01"
  }
}
```

> This profile stores **patterns, never raw personal data.** It grows smarter with every verified session and is the only context the agent needs to make a fully personalised decision.

---

## How It Works

```
USER ACTION
(login · transaction · device change · account recovery · KYC update)
          ↓
SIGNAL COLLECTION
(device fingerprint · location · behavioural biometrics · transaction context)
          ↓
CONTEXT BUILDER
(live signals vs per-user memory profile · delta computation)
          ↓
AGENTIC REASONING ENGINE — Multi-step Tool Orchestration
┌──────────┐      ┌──────────┐      ┌──────────┐
│  THINK   │ ───▶ │   ACT    │ ───▶ │ OBSERVE  │
│ reasoning│      │tool call │      │ process  │
└──────────┘      └──────────┘      └──────────┘
      ▲________________________loop until confident_│
          ↓
IDENTITY TRUST SCORE + FULL EXPLANATION
[ ALLOW ] · [ OTP ] · [ VIDEO KYC ] · [ BLOCK + ESCALATE ]
          ↓
ACTION EXECUTION
(transaction processed · verification triggered · fraud team alerted)
          ↓
MEMORY UPDATE
(user profile recalibrated · identity trust score adjusted · baseline learns)
          ↓
AUDIT LOG CREATED
(full reasoning chain stored — RBI compliance)
          ↓
↺ continuous — next event
```

**Identity Trust Score — Live Session Example:**

```
User logs in                →  Trust Score: 94  (known device, usual time)
New device detected         →  Trust Score: 81  (unfamiliar device signal)
Unusual typing pattern      →  Trust Score: 62  (behavioural deviation)
₹1,80,000 transfer attempt  →  Trust Score: 31  (3.6x historical maximum)
                            →  Video KYC triggered
User verified successfully  →  Trust Score: 90  (identity confirmed)
                            →  Transfer allowed
```

**Example Agent Decision Output:**

```
Identity Trust Score:  29
Confidence:            High

Evidence:
  • Device fingerprint never seen before
  • Transfer 3.6x user's historical maximum
  • Login at 3:14 AM — outside usual window
  • Device linked to fraud reports from 2 other accounts

Missing Information:
  • Identity not yet verified on this device

Next Step:
  Block transaction → Trigger Video KYC → Await verification

Audit Trail:
  Tools called: check_device_registry(), check_global_fraud_signals()
  Reasoning chain: stored for RBI compliance review
```

---

## Key Features

**🔍 Continuous Identity Trust Monitoring**
Identity is not verified once — it is continuously updated throughout the entire session. Every action shifts the Identity Trust Score. The system watches every step, every screen, every signal.

**🧠 Per-User Memory Profiles**
Lightweight JSON profiles capture each user's behavioural baseline. A farmer in Gujarat and a professional in Mumbai are understood differently. The system learns — and never stops learning.

**⚡ Agentic Reasoning Engine**
A single shared AI brain with multi-step tool orchestration. Thinks, investigates, observes, decides — the way a human fraud analyst would, at machine speed. Never reacts blindly. Always explains.

**🎭 Deepfake-Aware Identity Verification**
No single biometric is trusted in isolation. Voice verification incorporates spectrogram-based signal analysis as one layer of evidence. Video KYC triggers unpredictable real-time liveness challenges that static deepfakes cannot respond to. Multi-modal cross-validation reduces the risk posed by synthetic identities.

**📋 Explainable Decisions**
Every decision ships with a full reasoning chain, confidence score, and evidence list. Not a score — a story. Fully auditable for RBI compliance and customer dispute resolution.

**🔒 Privacy First by Design**
Stores behaviour patterns, not personal data. Hashed identifiers. Data minimisation enforced. Compliant with India's DPDP Act and RBI Cybersecurity Framework.

**📈 Adaptive Learning**
Every session updates the user's memory profile. The Identity Trust Score evolves. The system gets smarter, more accurate, and less disruptive as trust builds over time.

---

## Risk Coverage

| Risk Category | How Drishti Addresses It |
|---|---|
| Account Takeover (ATO) | Continuous trust monitoring catches mid-session hijacking instantly |
| KYC Fraud | Agent cross-validates identity signals against KYC records in real time |
| Insider Threats | Same monitoring framework applied to internal privileged access users |
| Suspicious Account Recovery | Elevated verification automatically triggered for high-risk recovery flows |
| New Device Risk | Device fingerprinting flags unknown devices at the first signal |
| Behavioural Anomalies | Per-user baseline catches deviations invisible to any rule engine |
| Session Hijacking | Mid-session trust score drops trigger immediate agent re-evaluation |
| Deepfake and Voice Clones | Multi-modal deepfake-aware verification with liveness detection |
| Privileged Access Misuse | Insider access patterns monitored identically to customer sessions |

---

## Technology Stack

| Layer | Technology | Purpose |
|---|---|---|
| Agent Brain | LLM API + Multi-step Tool Orchestration | Core reasoning and investigation |
| User Memory | JSON per-user behavioural profiles | Personalised baseline storage |
| Backend | Python, FastAPI | API and business logic |
| Dashboard | Streamlit | Real-time trust score visualization |
| User Simulation | Faker, Locust | Realistic load testing at scale |
| Location Intelligence | IP Geolocation API | Geo-anomaly detection |
| Device Trust | Device Fingerprinting | Known vs unknown device detection |
| Voice Deepfake Detection | Spectrogram Signal Analysis — librosa | One layer of synthetic voice detection |
| Video Deepfake Detection | Real-time Liveness — MediaPipe | Challenge-response verification |
| Privacy Layer | Hashed identifiers, data minimisation | DPDP Act compliance |

---

## Project Structure

```
drishti-identity-trust/
├── agent/
│   ├── brain.py              # Core agentic reasoning loop
│   ├── tools.py              # Tool definitions and handlers
│   └── memory.py             # Per-user profile management
├── signals/
│   ├── device.py             # Device fingerprinting
│   ├── location.py           # IP geolocation and geo-checks
│   ├── behaviour.py          # Behavioural biometrics
│   └── transaction.py        # Transaction signal analysis
├── deepfake/
│   ├── spectrogram.py        # Voice deepfake signal analysis
│   └── liveness.py           # Video liveness challenges
├── data/
│   └── users/                # Per-user JSON memory profiles
├── dashboard/
│   └── app.py                # Streamlit UI
├── simulation/
│   ├── generate_users.py     # Faker user generation
│   └── locustfile.py         # Load testing scenarios
├── requirements.txt
└── README.md
```

---

## Getting Started

```bash
# Clone the repository
git clone https://github.com/kashvo/drishti-identity-trust.git
cd drishti-identity-trust

# Install dependencies
pip install -r requirements.txt

# Generate simulated users (run once)
python simulation/generate_users.py

# Run the dashboard
streamlit run dashboard/app.py
```

---

## Roadmap

| Week | Focus | Deliverable |
|---|---|---|
| Week 1 | Core agent and memory | AI agent brain, per-user JSON profiles, reasoning loop |
| Week 2 | Signal collection and tools | Device, location, behaviour signals, full tool library |
| Week 3 | Dashboard and demo scenarios | Streamlit UI, live trust score visualization, 5 demo scenarios |
| Week 4 | Deepfake defence and polish | Spectrogram analysis, liveness detection, full explainability layer |

---

## Research Foundation

Drishti is grounded in current peer-reviewed research and industry intelligence.

| Source | Relevance |
|---|---|
| IMF Digital Finance Notes (2026) | Validates shift from single authentication to continuous identity verification across banking channels |
| World Journal of Advanced Research (2025) | Validates per-user behavioural profiling with stream processing for real-time fraud decisions during payment authorization |
| Yao et al. (2023) — ReAct, arXiv:2210.03629 | Foundational framework for agentic multi-step reasoning and tool orchestration |
| NVIDIA AI Blueprint — Financial Fraud Detection (2025) | Confirms agentic multi-signal approach reduces false positives significantly |
| Accenture Banking Trends (2026) | Confirms agent identity frameworks as a critical banking priority for 2026 |
| Al Jazeera — bob World Investigation (2023) | Documents real-world insider fraud at Bank of Baroda that Drishti directly addresses |

---

## Demo

> 🔧 Prototype under active development — PSB Hackathon Series 2026, Bank of Baroda × IIT Gandhinagar.
>
> Demo link will be updated here before submission deadline.

---

## Team Drishti

**PSG College of Technology — B.Tech Information Technology**

| Member | Role |
|---|---|
| Kavesha Sakthivel | Team Lead and AI/ML Engineer |
| Sanjit | Backend Developer and Cybersecurity Analyst |
| Sabare Periyasamy | Frontend Developer and Privacy Compliance |

---

## Citation

If you reference this work, please cite:

```
Team Drishti (2026). Drishti: An Agentic AI-powered Identity Trust Framework
for Continuous Digital Banking Security. PSB Hackathon Series 2026,
Bank of Baroda × IIT Gandhinagar.
PSG College of Technology, B.Tech Information Technology.
```

---

## License

This project is licensed under the MIT License.

---

<div align="center">

*Built for the PSB Hackathon Series 2026 — Cybersecurity and Fraud Domain*

*Guided by the Department of Financial Services, Ministry of Finance, Government of India*

**See clearly. Protect completely.**

</div>
