# AI Customer Support Copilot

An AI-powered customer support assistant that helps support agents generate intelligent, context-aware draft responses for customer tickets.

## Overview
This project uses Large Language Models (LLMs), Retrieval-Augmented Generation (RAG), and customer memory to assist support teams in handling customer queries efficiently.

The system analyzes support tickets, retrieves relevant customer history and knowledge base information, and generates empathetic, actionable response drafts for support agents.

---

## Features

- Automated AI-generated support response drafts
- Context-aware replies using customer interaction history
- Knowledge base search using RAG
- Billing, account, and plan-related tool integrations
- Memory-based personalization using past resolutions
- Interactive dashboard for support agents
- Dockerized deployment for easy setup

---

## Workflow

1. Customer submits support ticket  
2. System reads:
   - Ticket subject
   - Ticket description
   - Customer information  
3. AI retrieves relevant context from:
   - Customer Memory (Mem0)
   - Knowledge Base (ChromaDB)
   - Support Tools  
4. Groq-powered LLM generates draft response  
5. Support agent reviews and sends response  
6. Accepted resolutions are stored for future learning  

---

## Tech Stack

- Python
- Docker
- Streamlit
- Groq LLM
- LangChain
- LangGraph
- ChromaDB
- Mem0

---

## Project Structure

```bash
customer_support_agent/
│
├── customer_support_agent/
│   ├── core/
│   ├── services/
│   ├── integrations/
│
├── knowledge_base/
├── data/
├── app.py
├── main.py
├── Dockerfile
├── docker-compose.yml
└── README.md
```

---

## Installation

### Clone Repository
```bash
git clone <repo-url>
cd customer_support_agent
```

### Setup Environment
Create `.env` file:

```env
GROQ_API_KEY=your_groq_api_key
ENABLE_LOCAL_EMBEDDINGS=true
```

### Run with Docker
```bash
docker compose up --build
```

---

## Access Application

- API: `http://localhost:8000`
- Dashboard: `http://localhost:8501`

---

## Future Improvements

- Multi-language support  
- Ticket priority prediction  
- Sentiment analysis  
- CRM integration  
- Better memory ranking  

---

## Author
Developed by Divyam Talreja
