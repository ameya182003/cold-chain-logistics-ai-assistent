
# 🚚 Cold Chain Logistics AI Assistant

### An Autonomous AI-Powered Logistics Intelligence System

An AI-powered logistics assistant that transforms traditional fleet monitoring into intelligent, data-driven decision-making using **LangGraph, LLMs, SQL Server, Pinecone RAG, and real-time Weather API integration.**

## 📌 Project Overview

Traditional cold-chain logistics systems rely on static dashboards and manual analysis to identify shipment risks.

This project introduces an autonomous AI agent that understands natural-language queries, retrieves enterprise logistics data, accesses company SOPs, analyzes weather conditions, and generates actionable recommendations.

## 🏗️ System Architecture

![Cold Chain Logistics AI Assistant Architecture](docs/architecture.png)

### Key Components

1. **Enterprise Database:** Microsoft SQL Server for GPS, sensor, and logistics data.
2. **AI Agent:** LangGraph-based agent for reasoning, planning, and tool execution.
3. **Vector RAG:** Pinecone for retrieving company SOPs, compliance rules, and safety guidelines.
4. **Weather API:** Open-Meteo for external weather information.
5. **SQL Audit Trail:** Records agent interactions and tool executions.
6. **Deployment:** AWS EC2 with GitHub Actions CI/CD.

## ✨ Key Features

- Natural-language interaction with logistics data.
- AI-powered agent orchestration using LangGraph.
- Secure SQL Server integration with read-only access.
- SOP-based knowledge retrieval using RAG.
- Live weather information and risk assessment.
- Automated incident analysis and recommendations.
- SQL-based audit logging for transparency.
- AWS deployment with GitHub Actions.

## 🛠️ Technology Stack

| Category | Technologies |
|---|---|
| Language | Python |
| AI Framework | LangGraph, LangChain |
| LLMs | OpenAI, Gemini, DeepSeek |
| Database | Microsoft SQL Server |
| Vector Database | Pinecone |
| Embeddings | HuggingFace, OpenAI |
| External API | Open-Meteo |
| Frontend | Streamlit |
| Deployment | AWS EC2 |
| CI/CD | GitHub Actions |

## 📂 Project Structure

```text
cold-chain-logistics-ai-assistent/
│
├── .github/workflows/   # CI/CD deployment
├── .streamlit/          # Streamlit configuration
├── Misc/Materials/      # Project documentation
├── data/
│   ├── policy/          # Company SOP documents
│   ├── raw/             # Logistics dataset
│   └── source/          # Dataset references
├── docs/                # Project documentation
├── scripts/             # Data and SOP ingestion
├── src/
│   ├── prompts/         # AI system prompts
│   ├── agent_tools.py   # SQL, Weather and RAG tools
│   ├── orchestrator.py  # LangGraph agent
│   └── ui.py            # Streamlit application
├── requirements.txt
└── README.md
```

## ⚙️ Installation & Setup

**1. Clone the repository**

```bash
git clone https://github.com/ameya182003/cold-chain-logistics-ai-assistent.git

cd cold-chain-logistics-ai-assistent
```

**2. Create a virtual environment**

```bash
python -m venv venv
```

**3. Activate the environment**

```bash
# Windows
venv\Scripts\activate

# Linux / macOS
source venv/bin/activate
```

**4. Install dependencies**

```bash
pip install -r requirements.txt
```

**5. Configure environment variables**

Create a `.env` file with your SQL Server, Pinecone, and LLM provider credentials.

**6. Run the application**

```bash
streamlit run src/ui.py
```

## ☁️ Deployment

The application uses an AWS EC2 deployment workflow:

```text
GitHub → GitHub Actions → SSH → AWS EC2 → Streamlit
```

Deployment is triggered through GitHub Actions using the `workflow_dispatch` workflow.

## 🎯 Project Impact

The architecture transforms traditional logistics monitoring into an intelligent system through:

- Natural-language querying.
- Autonomous reasoning and tool execution.
- Real-time external information.
- Context-aware SOP recommendations.
- Enterprise auditability and automated deployment.
