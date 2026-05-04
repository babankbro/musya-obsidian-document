# 🏗️ MUSYA AI — System Architecture

> Source: MUSYA AI Application PDF (Architecture Overview)

---

## 🧱 Architecture Overview

MUSYA AI is a unified architecture for generating health policy documents using **AI Agent technology + Retrieval Augmented Generation (RAG)**.

```
┌─────────────────────────────────────────────────────────┐
│                    WEB FRONTEND                         │
│   Login → Define Query → Dashboard → Download DOCX     │
└───────────────────┬─────────────────────────────────────┘
                    │
┌───────────────────▼─────────────────────────────────────┐
│                  BACKEND API                            │
│     Orchestration Center + Workflow Control + Auth      │
└──────┬───────────────────────────────────────┬──────────┘
       │                                       │
┌──────▼──────────────┐             ┌──────────▼──────────┐
│   AI AGENT LAYER    │             │     RAG LAYER       │
│                     │             │                     │
│ • Request Interpreter│            │ • Document RAG      │
│ • Planner           │             │   (Semantic Search  │
│ • Domain Analysts   │             │    PDF/DOCX/Policy) │
│   - Road Accidents  │◄───────────►│                     │
│   - Mental Health   │             │ • Database RAG      │
│   - NCDs            │             │   (Health DB Stats) │
│ • Report Generator  │             │                     │
└──────┬──────────────┘             └──────────┬──────────┘
       │                                       │
┌──────▼───────────────────────────────────────▼──────────┐
│                 DATA STORAGE                            │
│     Document Store (PDF/Word) + Vector DB + Health DB  │
└─────────────────────────────────────────────────────────┘
       │
┌──────▼──────────────────────────────────────────────────┐
│              OBSERVABILITY LAYER                        │
│         Tracing + Eval + Audit Logs + Citations         │
└─────────────────────────────────────────────────────────┘
```

---

## 📦 Component Details

### 1. Web Frontend
- User authentication (login/logout)
- Query definition interface
- Report dashboard / preview
- DOCX download

**Beta Issues:** Vertical layout, font size too large, no prompt guidance

### 2. Backend API
- Central orchestration hub
- Workflow management
- Access control / permissions

### 3. AI Agent Layer (OpenAI SDK + LangGraph)

| Agent | Role |
|-------|------|
| Request Interpreter | Parse and classify user's request |
| Planner | Plan retrieval steps across data sources |
| Retrieval & Analyst | Domain-specific analysis (accidents/mental/NCDs) |
| Report Generator | Synthesize data, add citations, format report |
| Citation & Evidence Agent | Convert raw RAG data → Evidence Package |
| Review Agent | QA check — verifies all citations before export |

### 4. RAG Layer (Dual)

| RAG Type | Source | Use |
|----------|--------|-----|
| Document RAG | PDF, DOCX, Policy docs | Semantic search for qualitative content |
| Database RAG | Health DB (structured stats) | Precise numerical/statistical lookups |

### 5. Data Storage

| Store | Content |
|-------|---------|
| Document Store | PDFs, Word files, research papers, policies |
| Vector DB | Embeddings for semantic search |
| Health Statistics DB | Structured numerical health data |

### 6. Observability
- Full tracing of every AI step
- Evaluation metrics
- Audit logs
- Citation traceability — every fact tagged with source

---

## 🔄 End-to-End Workflow

```
User defines query
       ↓
AI Agent interprets request
       ↓
Planner creates retrieval plan
       ↓
Document RAG ──► Agent synthesizes ◄── Database RAG
       ↓
Citation Agent validates sources
       ↓
Review Agent checks completeness
       ↓
Report generated → Preview → DOCX Export
```

---

## 🔒 Anti-Hallucination Mechanism

- Every fact in the report is tagged with a **Citation Code**
- If a conclusion has insufficient evidence → system flags **"Insufficient Evidence"** automatically
- No export until Review Agent confirms all citations are complete

---

## ⚠️ Known Architecture Issues (from Beta)

| Issue                                  | Layer        | Priority |
| -------------------------------------- | ------------ | -------- |
| ThaiJO API timeout                     | Database RAG | P1       |
| Diabetes DB 403 Forbidden              | Database RAG | P1       |
| Data retrieval mismatch (wrong domain) | AI Agent     | P1       |
| Slow processing                        | Agent + RAG  | P2       |
| Province-only data granularity         | Data Storage | P2       |
| Limited international references       | Document RAG | P3       |
|                                        |              |          |

---

## 🚀 Planned Architecture Improvements (Beta → Production)

- [ ] Add HDC (Ministry Health Data Center) connector
- [ ] Add NHES survey database
- [ ] Add PubMed/Scopus API integration
- [ ] Add Police department data API
- [ ] Expand to district/sub-district level granularity
- [ ] Add user file upload pipeline (with PDPA screening)
- [ ] Add PowerPoint/Slide export engine

---

*[[00 - Overview/🏠 Project Home | ← Back to Project Home]]*
