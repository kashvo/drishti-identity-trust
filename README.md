<div align="center">

# 👁️ Drishti
### *The watchful eye. Continuous. Contextual. Certain.*

[![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=flat-square&logo=python&logoColor=white)](https://python.org)
[![Streamlit](https://img.shields.io/badge/Streamlit-Dashboard-FF4B4B?style=flat-square&logo=streamlit&logoColor=white)](https://streamlit.io)
[![LLM](https://img.shields.io/badge/Agentic_AI-ReAct_Framework-7F77DD?style=flat-square)](https://arxiv.org/abs/2210.03629)
[![Hackathon](https://img.shields.io/badge/PSB_Hackathon-2026-orange?style=flat-square)](https://bankofbaroda.in)
[![Domain](https://img.shields.io/badge/Domain-Cybersecurity_%26_Fraud-red?style=flat-square)]()

**An Agentic AI-powered Identity Trust Framework for continuous digital banking security.**

*PSB Hackathon Series 2026 · Bank of Baroda × IIT Gandhinagar*

</div>

---

## The Problem

Banks verify identity once — at login — and then walk away. But fraud doesn't happen at the door. It happens inside.

Current rule-based systems are rigid. They cannot reason about combinations of signals they haven't seen before. They block genuine users with false positives. They miss real threats with false negatives. And in India, where UPI processes over 8,000 transactions every second — each one instant, each one final — the system must be right before the money moves, not after.

Today's threats go further. Generative AI can clone a customer's voice in seconds. Deepfake tools can replicate faces convincingly enough to fool verification systems. Fraudsters no longer need to steal credentials. They manufacture identities. And systems that rely on a single signal — a voice match, a face scan, a known device — are no longer enough.

Bank of Baroda serves an extraordinarily diverse customer base: a farmer in rural Gujarat making his first digital payment, and a startup founder in Mumbai making his fifteenth transfer of the day. Their normal looks nothing alike. A system that treats them the same will fail both.

In FY2024-25, over 6.32 lakh UPI fraud cases were reported in India with losses exceeding ₹485 crore. The IMF has formally noted that traditional fraud models are becoming ineffective in the age of autonomous transactions — and that the industry must shift from single authentication to continuous identity verification. Yet most banking systems still verify identity only once — at the door.

---

## The Solution

Drishti is an Agentic AI-powered Identity Trust Framework that continuously monitors user sessions across all digital banking channels — not just at login, but across every action, every screen, every transaction.

It maintains a quiet memory for every user — not their personal details, just their patterns. Their habits. Their normal. When something breaks that picture, Drishti doesn't immediately block. It investigates first, reasons through the evidence using chain-of-thought tool calling, and then decides. The way a human fraud analyst would — at machine speed.

No single signal makes a decision. A deepfake can clone a voice. It cannot simultaneously replicate how someone types, how they navigate, what they usually transfer, which device they always use, and where they always transact from — all at once, in real time. That combination is what Drishti watches.

---

## Why Drishti is Different

It is the difference between a security camera that records and a security guard that understands.

| What Exists Today | Drishti |
|---|---|
| Checks identity at login only | Monitors the entire session continuously |
| Rule-based and rigid | Reasons contextually about every combination |
| One-size-fits-all model | Personalised baseline per user |
| Black box risk score | Full reasoning chain with explanation |
| Reacts after fraud occurs | Investigates before deciding |
| Batch processing after transaction | Stream processing during authorization |
| Trusts a single signal | Cross-validates across all signals simultaneously |
| Vulnerable to deepfakes and voice clones | Spectrogram analysis and real-time liveness detection |

---

## Architecture

One shared agent brain. Millions of individual memory profiles.

Every user has a lightweight JSON profile capturing their behavioural baseline — usual device, location, transaction amounts, login patterns, and session behaviour. The agent reads this profile fresh at every event. Same brain, different context every time. Adding users means adding a JSON file — not adding compute. Personalised decisions at scale, without the cost of individual agents.

The architecture is designed for cloud deployment at India's UPI scale — sub-50 millisecond decisions for instant, irreversible payments.

Each user memory profile looks like this:

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
    "trust_score": 92,
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

This profile stores patterns — never raw personal data. It grows smarter with every verified session and is the only context the agent needs to make a fully personalised decision.

---

## How It Works

```
User Action
(login · transaction · device change · account recovery)
        ↓
Signal Collection
(device fingerprint · location · behavioural biometrics · transaction context)
        ↓
Context Builder
(live signals compared against per-user memory profile)
        ↓
Agentic AI Brain — Chain-of-Thought Tool Calling
THINK → ACT (call tools) → OBSERVE → THINK → DECIDE
        ↓
Decision + Full Explanation
(Allow · OTP · Video KYC · Block)
        ↓
Memory Update
(user profile learns from this session)
        ↓
Audit Log Created
(full reasoning chain stored for RBI compliance)
        ↓
↺ continuous — next event
```

---

## Key Features

**Continuous Session Monitoring**
Identity is verified throughout the entire session — not just at login. Every action is watched, every shift in behaviour is noticed. Aligned with the IMF's 2026 recommendation that the industry move from single authentication to continuous identity verification.

**Per-User Memory Profiles**
Every user has a lightweight JSON profile capturing their behavioural baseline. The system learns what normal looks like for each individual — not a generic average. A farmer in Gujarat and a professional in Mumbai are understood differently.

**Agentic AI Reasoning**
A single shared AI agent brain uses chain-of-thought reasoning with tool calling — think, call tools, observe, repeat — the way a human fraud analyst would, at machine speed. It investigates before it decides.

**Deepfake and Voice Clone Resistant**
No single biometric is trusted in isolation. For voice verification, Drishti runs spectrogram analysis as a tool call — detecting synthetic artifacts in pitch and frequency that human ears miss but machines can spot. For video KYC, unpredictable real-time liveness challenges are triggered that current deepfake tools cannot respond to in real time.

**Explainable Decisions**
Every decision comes with a full reasoning chain — not just a risk score. A clear explanation of why, fully auditable for RBI compliance.

**Privacy First**
Stores behaviour patterns, not raw personal data. Hashed identifiers. Data minimisation by design. Compliant with India's DPDP Act and RBI Cybersecurity Framework.

**Adaptive Learning**
After every session, the user's memory profile is updated. The system gets smarter and less disruptive over time as trust builds.

---

## Risk Coverage

Drishti directly addresses every risk category in the problem statement — and goes further.

| Risk | How Drishti Addresses It |
|---|---|
| Account Takeover (ATO) | Continuous session monitoring catches mid-session hijacking |
| KYC Fraud | Agent cross-validates identity signals against KYC records in real time |
| Insider Threats | Same monitoring framework applied to internal privileged users |
| Suspicious Account Recovery | High-risk flows automatically trigger elevated verification |
| New Device Risk | Device fingerprinting detects unknown devices at first signal |
| Behavioural Anomalies | Per-user baseline catches deviations invisible to rule engines |
| Session Hijacking | Behaviour shifts mid-session trigger immediate re-evaluation |
| Deepfake and Voice Clones | Spectrogram analysis and real-time liveness detection |

---

## Technology Stack

| Layer | Technology |
|---|---|
| Agent Brain | LLM API with chain-of-thought tool calling |
| User Memory | JSON-based per-user behavioural profiles |
| Backend | Python, FastAPI |
| Frontend and Dashboard | Streamlit |
| User Simulation | Faker, Locust |
| Location Intelligence | IP Geolocation API |
| Device Trust | Device Fingerprinting |
| Voice Deepfake Detection | Spectrogram Analysis — librosa |
| Video Deepfake Detection | Real-time Liveness Detection — MediaPipe |
| Privacy | Data minimisation, hashed identifiers, DPDP Act compliant |

---

## Project Structure

```
Drishti/
├── agent/
│   ├── brain.py          # Core agentic reasoning loop
│   ├── tools.py          # Tool definitions and handlers
│   └── memory.py         # Per-user profile management
├── signals/
│   ├── device.py         # Device fingerprinting
│   ├── location.py       # IP geolocation and geo-checks
│   ├── behaviour.py      # Behavioural biometrics
│   └── transaction.py    # Transaction signal analysis
├── deepfake/
│   ├── spectrogram.py    # Voice deepfake detection
│   └── liveness.py       # Video liveness challenges
├── data/
│   └── users/            # Per-user JSON memory profiles
├── dashboard/
│   └── app.py            # Streamlit UI
├── simulation/
│   ├── generate_users.py # Faker user generation
│   └── locustfile.py     # Load testing scenarios
└── README.md
```

---

## Getting Started

```bash
# Clone the repository
git clone https://github.com/[your-username]/Drishti.git
cd Drishti

# Install dependencies
pip install -r requirements.txt

# Generate simulated users
python simulation/generate_users.py

# Run the dashboard
streamlit run dashboard/app.py
```

---

## Roadmap

| Week | Focus | Milestone |
|---|---|---|
| Week 1 | Core agent and memory | AI agent brain, per-user JSON profiles, reasoning loop |
| Week 2 | Signal collection and tools | Device fingerprinting, location, behaviour signals, tool calls |
| Week 3 | Dashboard and demo scenarios | Streamlit UI, 5 live demo scenarios, risk decision display |
| Week 4 | Deepfake defence and polish | Spectrogram analysis, liveness detection, full explainability layer |

---

## Research Foundation

Drishti is grounded in current academic and industry research.

- **IMF Digital Finance Notes (2026)** — validates the shift from single authentication to continuous identity verification across banking channels
- **World Journal of Advanced Research (2025)** — validates per-user behavioural profiling with stream processing architecture for real-time fraud decisions during payment authorization
- **Yao et al. (2023)** — ReAct: Synergizing Reasoning and Acting in Language Models — foundational framework for agentic chain-of-thought reasoning
- **Accenture Top Banking Trends 2026** — confirms agent identity frameworks as a critical banking priority for 2026

---

## Demo

Prototype under active development as part of PSB Hackathon Series 2026 — Bank of Baroda x IIT Gandhinagar.

Demo link will be updated here before submission deadline.

---

## Team Drishti

**PSG College of Technology — B.Tech Information Technology**

| Member | Role |
|---|---|
| Kavesha Sakthivel | Team Lead and AI/ML Engineer |
| Sanjit | Backend Developer and Cybersecurity Analyst |
| Sabare Periyasamy | Frontend Developer and Privacy Compliance |

---

<div align="center">

*Built for the PSB Hackathon Series 2026 — Cybersecurity and Fraud Domain*

*Guided by the Department of Financial Services, Ministry of Finance, Government of India*

</div>
