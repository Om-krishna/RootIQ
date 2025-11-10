# RootIQ

RootIQ is an **AI-powered On-Call Assistant** that reads and analyzes logs, detects issues, identifies their root causes, and provides actionable fix suggestions — all in real time.

---

## 🚀 Features
- **Smart Log Analysis** — Automatically detects and groups similar errors.  
- **AI-Powered RCA** — Classifies issues as *Infrastructure* or *Functional*.  
- **Actionable Insights** — Generates probable causes and suggested fixes.  
- **Real-Time Alerts** — Sends structured incident summaries to chat or monitoring tools.  
- **Noise Filtering** — Ignores harmless logs to reduce false alerts.

---

## ⚙️ Architecture Overview

Logs (Local / Cloud)
│
▼
Error Detection & Clustering
│
▼
AI Engine → RCA JSON
(Classification, Causes, Fixes, Confidence)
│
▼
Notification (Console / Webhook / Chat)


---

## 🧩 Getting Started

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/your-username/RootIQ.git
cd RootIQ


python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt

SERVICE_NAME=
LOCAL_LOG_DIR=./logs
WEBHOOK_URL=your_webhook_here

#Run the application
export PYTHONPATH=$(pwd)
python -m src.lambdas.triage.handler


