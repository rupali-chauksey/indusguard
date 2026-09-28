# 🏭 IndusGuard - Agentic AI for Industrial Intelligence

**Industrial Intelligence. Guaranteed.**

> Agentic AI for industrial predictive maintenance: 4 autonomous agents (Diagnostic, Predictive, Planning, CRM), 47h+ RUL forecasting, 3D Digital Twin, Salesforce SFDC + FSL integration & Human-in-the-Loop governance.

**Multi-Agent Autonomous Orchestration | LLM-Powered Predictive Maintenance | Digital Twin | Human-in-the-Loop Governance at Scale**

[![Python 3.11+](https://img.shields.io/badge/python-3.11+-blue.svg)](https://www.python.org/downloads/)
[![Streamlit 1.40+](https://img.shields.io/badge/streamlit-1.40+-FF4B4B.svg)](https://streamlit.io/)
[![ChromaDB](https://img.shields.io/badge/vector_store-ChromaDB-purple.svg)](https://www.trychroma.com/)
[![Groq Cloud](https://img.shields.io/badge/LLM-Groq_Cloud_120B-orange.svg)](https://groq.com/)
[![Salesforce](https://img.shields.io/badge/Salesforce-SFDC%20%2B%20FSL-blue.svg)](https://salesforce.com)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

An enterprise-grade, agentic manufacturing intelligence platform designed for reliability engineering, plant operations, and quality assurance. Combines **Deterministic Analytics**, **Isolation Forest Anomaly Detection**, **Gradient-Boosted Predictive RUL (Remaining Useful Life)**, **Spatial 3D Digital Twin**, **Multi-Agent Orchestration (Diagnostic, Predictive, Planning, CRM)**, **Salesforce Integration (SFDC + FSL)**, and **Human-in-the-Loop (HITL) Governance**.

**Topics:** `agentic-ai` · `multi-agent-systems` · `predictive-maintenance` · `digital-twin` · `industrial-iot` · `streamlit` · `groq` · `llm` · `rag` · `chromadb` · `salesforce` · `field-service-lightning` · `isolation-forest` · `anomaly-detection` · `remaining-useful-life` · `human-in-the-loop` · `manufacturing` · `industry-4-0` · `python`

---

## 🎯 Link

> **[https://indusguard-ai-m855.onrender.com]**
>
> 
> Try the IndusGuard AI live dashboard with sample industrial telemetry data.

---

## 📸 Screenshots


## 🏭 Problem Statement

Modern industrial plants generate high-frequency sensor streams (temperature, vibration, pressure) alongside unstructured technician logs and work orders. Reliability engineers struggle with:

1. **Unplanned Outages**: Critical machines failing without advance warning (e.g. thermal runaway on injection molding units).
2. **Disconnected Data**: Sensor spikes are isolated from technician repair histories and SOP manuals.
3. **Safety & Cost Risks**: Autonomous AI actions without human authorization risk physical safety and expensive line shutdowns.
4. **Execution Gap**: Even when AI detects problems, there is no automated path to create Work Orders, dispatch technicians, or notify customers.

**IndusGuard AI** bridges this divide with **47+ hour advance RUL predictions**, **Monte Carlo scenario simulation**, **multi-agent root cause analysis**, **Salesforce integration for execution**, and **strict Human-in-the-Loop safety approval gates**.

---



## 🏗️ System Architecture

<img width="4760" height="6181" alt="deepseek_mermaid_20260927_050029" src="https://github.com/user-attachments/assets/017d5a4c-053a-4e59-90f3-8010860bc634" />





## 🤖 The 4 Autonomous AI Agents

| Agent | Core Responsibility | Tool Arsenal | Primary Output |
|---|---|---|---|
| **1. Diagnostic Agent** | Real-time telemetry surveillance & anomaly grading | SensorTool, FaultTool, AnomalyDetector | Current telemetry state, anomaly score, severity badge, sensor evidence |
| **2. Predictive Agent** | Remaining Useful Life & failure horizon forecasting | RULPredictor, SensorTool | RUL (hours), 90% confidence interval, 24h/48h/7d failure probabilities, degradation rate |
| **3. Planning Agent** | Autonomous mitigation planning & financial ROI | CostCalculator, RiskAssessor | Action steps, total repair cost, expected gross savings, net ROI ratio, optimal window |
| **4. CRM Agent** | Execution via Salesforce or Local CRM | SFDCService, MockSalesforceService, WorkOrderService | Work Order ID, FSL dispatch, technician assignment, customer notification, audit log |

---

## 🎮 Digital Twin Capabilities

- **Spatial 3D Factory Floor**: Interactive 3D Plotly visualizer mapping all 5 machines in physical coordinates with color-coded operational states.
- **Temporal Time-Travel**: Slide from -48 hours (historical outages) to PRESENT (live sync) to +48 hours (predicted critical failures).
- **What-If Scenario Simulator**: 1,000-iteration Monte Carlo engine exploring maintenance intervals, spare part buffers, and staffing levels.
- **Failure Cascade Modeling**: Simulates sequential downstream starvation and financial exposure if a specific machine experiences an unplanned outage.

---

## 🏢 Salesforce Integration (SFDC + FSL)

IndusGuard AI integrates with Salesforce Manufacturing Cloud + Service Cloud (FSL) for enterprise-grade execution:

| Step | Salesforce Object | What Happens |
|---|---|---|
| 1. Work Order | `WorkOrder` | Created automatically after approval |
| 2. Asset Link | `Asset` | MACH-003 linked to Work Order |
| 3. Account Link | `Account` | ABC Manufacturing linked |
| 4. Case Creation | `Case` | Predictive Maintenance Case created |
| 5. FSL Dispatch | `ServiceAppointment` | Intelligent scheduling → best technician |
| 6. Customer Notify | `Case` + `EmailMessage` | Impacted customers notified |
| 7. Audit Log | `Task` + `ContentVersion` | ISO-9001 compliant trail |

### Dual-Mode Support

- **SFDC Mode (Primary)**: Real Salesforce integration via `simple-salesforce`
- **Local CRM Mode (Fallback)**: SQLite-based CRM with 7 tables
- **Auto-detection**: Checks credentials → picks SFDC or Local CRM automatically

---

## 🛑 Human-in-the-Loop (HITL) Governance & RBAC

Industrial plant safety requires strict human verification before modifying production schedules or ordering costly replacements:

- **Operator Persona**: Authorized to approve minor operational adjustments under ₹5,000.
- **Supervisor Persona**: Authorized to approve repair actions under ₹50,000.
- **Plant Head / Reliability Manager**: Unlimited authorization across all budget tiers.
- **Audit Logging**: Every action, timestamp, approver, and comment is saved to an immutable SQLite audit trail.

---

## 🔄 Post-Repair Feedback Loop (Closed-Loop System)

When a technician completes the repair, the system automatically:

1. **FSL Update**: Work Order Status → COMPLETED
2. **Digital Twin Update**: MACH-003 RED → GREEN, Temp 107.9°C → 78.5°C
3. **State Persistence**: SQLite update (refresh-safe)
4. **Salesforce Update**: Work Order CLOSED, Case RESOLVED
5. **Customer Update**: "Your order will be ON TIME"
6. **Agent Dashboard Update**: "Problem Solved" badge + timeline
7. **Audit Log**: Complete trail for compliance

---

## 📊 Projected Business Impact

> **Note:** These are projected figures based on simulation and industry benchmarks. Actual deployment results may vary.

### 6-Month Field Simulation (5 Machines)

| Metric | Baseline | Projected | Improvement |
|---|---|---|---|
| Unplanned Downtime | 240 hrs | 158 hrs | ▼ 34.2% |
| Mean Time Between Failures (MTBF) | 180 hrs | 285 hrs | ▲ 58.3% |
| Mean Time To Repair (MTTR) | 4.2 hrs | 3.1 hrs | ▼ 26.2% |
| Emergency Repair Spend | ₹18.5 Lakh | ₹12.2 Lakh | ▼ 34.1% |
| Production Outage Loss | ₹45.0 Lakh | ₹29.7 Lakh | ▼ 34.0% |

### Financial Summary

- **Total Annual Fleet Savings**: ₹18,39,500 (₹18.4 Lakh)
- **Platform Year 1 ROI**: 1,008% (Payback Period: 1.1 months)
- **Enterprise 100-Machine Scale**: ₹3.68 Crore / year
- **Cost per AI Query**: ₹0.02

### Methodology

- **Historical Data**: 3,525 records analyzed
- **Simulation**: Monte Carlo (1,000 iterations)
- **Benchmarks**: Industry standards for predictive maintenance AI
- **Assumptions**: Documented in `docs/assumptions.md`

---

## 💻 Tech Stack

| Layer | Technology |
|---|---|
| Frontend / Multi-page UI | Streamlit 1.40+ (Industrial Dark Theme, Port 8000) |
| LLM Reasoning | Groq Cloud API (`openai/gpt-oss-120b`) |
| Semantic Embeddings | `sentence-transformers/all-MiniLM-L6-v2` |
| Vector Database | ChromaDB (local persistent storage) |
| Machine Learning | scikit-learn (IsolationForest), Prophet (RUL) |
| Causal Knowledge Graph | NetworkX DiGraph |
| Data Analytics & Charts | Pandas, NumPy, Plotly Express & Plotly Graph Objects |
| CRM Integration | Salesforce (SFDC + FSL) via `simple-salesforce` |
| Database | SQLite (CRM + Audit) |
| PDF Reporting | fpdf2 |
| Audio / Voice TTS | gTTS |
| Testing | pytest |
| Deployment | Docker + Docker Compose |

---

## 📁 Project Structure

```text
indusguard-ai/
├── app.py                              # Home page
├── requirements.txt
├── .env.example
├── README.md
├── Dockerfile
├── docker-compose.yml
├── LICENSE
│
├── .streamlit/
│   └── config.toml                     # Dark theme, port 8000
│
├── assets/
│   └── style.css                       # Custom premium CSS
│
├── data/
│   ├── sensor_logs.csv                 # 2,001 records
│   ├── downtime_events.csv             # 121 records
│   ├── quality_inspections.csv         # 801 records
│   ├── maintenance_records.csv         # 201 records
│   ├── production_summary.csv          # 406 records
│   ├── customers.csv                   # 3 customers
│   └── crm.db                          # SQLite CRM
│
├── models/
│   ├── anomaly_iforest.pkl
│   ├── rul_MACH-001.pkl … rul_MACH-005.pkl
│   └── knowledge_graph.gpickle
│
├── pages/
│   ├── 1_🏭_Live_Floor.py
│   ├── 2_🔮_Predictive.py
│   ├── 3_🎮_Digital_Twin.py
│   ├── 4_🎛️_WhatIf_Simulator.py
│   ├── 5_💬_Copilot.py
│   ├── 6_🛑_Approvals.py
│   ├── 7_💰_ROI_Dashboard.py
│   ├── 8_🏢_CRM_Dashboard.py
│   └── 9_✅_Resolved_Problems.py
│
├── src/
│   ├── config.py
│   ├── agents/                         # 4 AI agents
│   ├── reasoning/                      # Synthesizer
│   ├── digital_twin/                   # 3D + simulation
│   ├── ml/                             # IsolationForest + Prophet
│   ├── tools/                          # 5 tools
│   ├── rag/                            # ChromaDB RAG
│   ├── hitl/                           # Human-in-the-Loop
│   ├── crm/                            # SQLite CRM (7 tables)
│   ├── integrations/                   # SFDC + Mock
│   ├── feedback/                       # Post-repair loop
│   └── services/                       # LLM, Voice, Reports
│
├── scripts/
│   ├── 00_generate_data.py
│   ├── 01_build_index.py
│   ├── 02_train_anomaly.py
│   ├── 03_train_rul.py
│   ├── 04_build_graph.py
│   ├── 05_init_crm.py
│   └── 06_generate_customers.py
│
└── tests/
    ├── test_agents.py
    ├── test_digital_twin.py
    ├── test_crm.py
    └── test_feedback_loop.py
```

---

## 🚀 Quickstart & Installation Guide

### 1. Clone and Configure Environment

```bash
# Clone the repository
git clone https://github.com/rupali-chauksey/indusguard-ai.git
cd indusguard-ai

# Create virtual environment
python -m venv venv
.\venv\Scripts\activate      # Windows
source venv/bin/activate     # Linux / macOS

# Install dependencies
pip install -r requirements.txt
```

### 2. Configure API Keys

Copy `.env.example` to `.env` and insert your credentials:

```env
# LLM
GROQ_API_KEY=your_actual_groq_api_key_here
GROQ_MODEL=openai/gpt-oss-120b

# Salesforce (Optional — for SFDC mode)
SF_USERNAME=your_salesforce_username
SF_PASSWORD=your_salesforce_password
SF_SECURITY_TOKEN=your_security_token
SF_DOMAIN=login

# App
PORT=8000
HOST=localhost
```

### 3. Build Vector Index and ML Models

```bash
# 1. Generate synthetic data (if not present)
python scripts/00_generate_data.py

# 2. Generate customers
python scripts/06_generate_customers.py

# 3. Initialize CRM database
python scripts/05_init_crm.py

# 4. Build ChromaDB semantic vector index
python scripts/01_build_index.py

# 5. Train Isolation Forest anomaly detector
python scripts/02_train_anomaly.py

# 6. Train RUL degradation predictors
python scripts/03_train_rul.py

# 7. Build causal knowledge graph
python scripts/04_build_graph.py
```

### 4. Launch Application

```bash
streamlit run app.py --server.port 8000
```

Open your browser at `http://localhost:8000`.

---

## 🐳 Docker Deployment

```bash
docker compose up --build
```

Access at `http://localhost:8000`.

---

## 🧪 Running Automated Tests

```bash
python -m pytest tests/ -v
```





