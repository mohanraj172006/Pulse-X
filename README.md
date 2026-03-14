
# ⚡ Pulse X — Enterprise Startup Trust Intelligence

> *Know Your Partner's Pulse — Before and After You Sign.*

Pulse X is an AI-powered startup verification platform that analyzes any startup URL and generates a **Governance-Grade Trust Score (0–100)** using 3 parallel AI agents, 5 IoT continuous monitoring sensors, and adaptive learning. Built for **VIHANSA 2K26 — 11:11 Hackathon** conducted by **Sri Ramakrishna Institute of Technology**.

---

## 🚀 Live Demo

| Service | URL |
|---|---|
| Frontend | http://localhost:3000 |
| Backend API | http://localhost:8000 |
| API Docs | http://localhost:8000/docs |

---

## ✨ Features

- 🔎 **Verification Agent** — Cross-checks LinkedIn, MCA21 Government Registry, News mentions
- 🧠 **Insight Agent** — Classifies tech stack, innovation maturity, industry category
- 🛡️ **Security Agent** — SSL, Domain Age, HIBP Credential Breaches, DNS, SPF/DKIM/DMARC, Open Ports
- 📡 **IoT Monitoring** — 5 continuous background sensors watching 24/7
- 🔄 **Adaptive Learning** — Trust Score improves based on enterprise feedback
- 📊 **Batch Analysis** — Analyze up to 20 startups simultaneously
- ⬇️ **Health Card Download** — Governance-grade report with source citations
- 🇮🇳 **MCA21 Integration** — India-specific legal company verification

---

## 🏗️ Architecture

```
Startup URL
     │
     ▼
Agent Orchestrator (asyncio.gather)
     │
     ├── Verification Agent → LinkedIn + MCA21 + News
     ├── Insight Agent      → Tech Stack + Maturity + Industry
     └── Security Agent     → SSL + HIBP + DNS + Ports
     │
     ▼
Trust Score = (V × 0.30) + (I × 0.30) + (S × 0.40)
     │
     ▼
Governance-Grade Startup Health Card

IoT Layer (Background 24/7)
├── SSL Sensor        → Every 6 hours
├── Domain Sensor     → Every 24 hours
├── Credential Sensor → Every 7 days
├── DNS Sensor        → Every 4 hours
└── Email Sensor      → Every 7 days
     │
     ▼
WebSocket Real-Time Alerts → Frontend Dashboard
```

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Backend | FastAPI + Python 3.11 |
| AI Agents | httpx + BeautifulSoup + asyncio |
| Database | MongoDB (Motor async driver) |
| Cache | Redis |
| Real-time | WebSockets |
| IoT Sensors | Async background tasks |
| Frontend | Pure HTML + CSS + Vanilla JS |
| Security | HIBP API + dnspython + ssl + socket |
| India Verify | MCA21 Government Registry |

---

## 📁 Project Structure

```
pulse-x/
├── backend/
│   ├── main.py
│   ├── requirements.txt
│   ├── .env.example
│   └── app/
│       ├── agents/
│       │   ├── verification_agent.py
│       │   ├── insight_agent.py
│       │   ├── security_agent.py
│       │   └── orchestrator.py
│       ├── iot/
│       │   ├── ssl_sensor.py
│       │   ├── domain_sensor.py
│       │   ├── credential_sensor.py
│       │   ├── dns_sensor.py
│       │   ├── email_sensor.py
│       │   └── monitor_service.py
│       ├── services/
│       │   ├── trust_score.py
│       │   ├── adaptive_learning.py
│       │   ├── websocket_manager.py
│       │   └── cache_service.py
│       ├── api/routes/
│       │   ├── startup.py
│       │   ├── batch.py
│       │   ├── monitor.py
│       │   ├── feedback.py
│       │   └── health.py
│       └── models/
└── frontend/
    ├── index.html
    ├── css/
    │   ├── style.css
    │   └── animations.css
    └── js/
        ├── app.js
        ├── api.js
        ├── dashboard.js
        ├── monitor.js
        ├── batch.js
        └── charts.js
```

---

## ⚙️ Setup

```bash
# Backend
cd backend
pip install -r requirements.txt
cp .env.example .env
uvicorn main:app --reload --port 8000

# Frontend
cd frontend
python -m http.server 3000
```

---

## 📡 API Endpoints

| Method | Endpoint | Description |
|---|---|---|
| POST | `/api/startups/verify` | Verify a startup |
| GET | `/api/startups/{id}` | Get startup details |
| POST | `/api/batch/verify` | Batch analyze startups |
| WS | `/api/monitor/{startup_id}` | Real-time IoT alerts |
| POST | `/api/feedback/` | Submit score correction |
| GET | `/api/health` | Health check |

---

## 🎯 Trust Score Formula

```
Trust Score = (Verification × 0.30) + (Insight × 0.30) + (Security × 0.40)
```

Security has the highest weight as it provides the most objective and measurable signals.

---

## 👥 Team

| Role | Responsibility |
|---|---|
| Frontend Developer | UI/UX, Dashboard, Real-time updates |
| IoT Engineer | 5 sensors, WebSocket alerts |
| AI/ML Engineer | 3 agents, Orchestrator, Adaptive learning |
| Backend/Security | FastAPI, MongoDB, Redis, Cybersecurity |

---

## 🏆 Hackathon

**Event:** VIHANSA 2K26 — 11:11 Hackathon
**Organized by:** Sri Ramakrishna Institute of Technology
**Track:** AI/ML + IoT + Cybersecurity + Web
**Challenge:** Building a Trust-Engine for Enterprise-Startup Co-Innovation
**Theme:** Noiseless Information for enterprise decision-makers
