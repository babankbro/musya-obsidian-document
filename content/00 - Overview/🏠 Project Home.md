# 🤖 MUSYA AI — Project Hub

> **ระบบสร้างเอกสารแผนสุขภาพด้วย AI Agent & RAG**
> Health Policy Document Generator for เขตสุขภาพที่ 10

---

## 🚦 Current Status

| Item | Detail |
|------|--------|
| **Phase** | Beta Improvement |
| **Sprint** | Pre-Release Sprint (May 2–24) |
| **Next Milestone** | 🎯 Demo Presentation — May 25, before lunch |
| **Server Deadline** | 🖥️ Production Server Live — before end of May |

---

## 📌 Critical Deadlines

```
May  2 ──── May 11 ──── May 15 ──── May 20 ──── May 25
│                           │            │           │
Sprint 1              Sprint 2      🖥️ Server    🎤 DEMO
Bug Fixes            UX + Data         Live        Lunch
```

---

## 📁 Navigation

- [[01 - Sprint Plan/📅 Sprint Overview]] — Full schedule & tasks
- [[02 - Feedback Analysis/📊 Survey Results Summary]] — What users said
- [[02 - Feedback Analysis/🐛 Bug Report from Feedback]] — Issues found
- [[02 - Feedback Analysis/💡 Feature Requests from Feedback]] — What to build
- [[03 - Architecture/🏗️ MUSYA System Architecture]] — System design
- [[04 - Feature Backlog/📋 Backlog]] — All pending features
- [[05 - Meeting Notes/📝 Meeting Index]] — Meeting log
- [[06 - Server Setup/🖥️ Server Checklist]] — Server deployment plan

---

## 🏗️ System at a Glance

| Layer | Component | Status |
|-------|-----------|--------|
| Frontend | Web UI (Input + Preview + Download) | 🟡 Improving |
| Backend API | Orchestration + Auth | 🟡 Improving |
| AI Agent | OpenAI SDK + LangGraph | 🟢 Running |
| RAG | Document RAG + Database RAG | 🟡 Expanding |
| Domain Agents | Road Accidents / Mental Health / NCDs | 🟢 Running |
| Citation Agent | Evidence + Anti-hallucination | 🟢 Running |
| Observability | Tracing + Audit Logs | 🟢 Running |

---

## 🎯 Beta Improvement Goals (from Survey)

1. ⚡ Fix slow processing & add progress indicators
2. 🐛 Fix 403 Forbidden errors (ThaiJO, Diabetes DB)
3. 📄 Fix DOCX output formatting issues
4. 🖥️ Redesign preview layout (vertical → horizontal)
5. 📝 Add prompt templates for new users
6. 📊 Add Executive Summary + SWOT to all reports
7. 🗂️ Expand data to district/sub-district level
8. 📦 Expand data sources (HDC, PubMed, NHES)

---

*Project started: 2026-05-02 | Contact: paweena.k@ubu.ac.th*
