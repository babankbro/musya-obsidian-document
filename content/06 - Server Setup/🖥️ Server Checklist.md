# 🖥️ Server Setup Checklist — MUSYA AI Production

> **Deadline: May 20, 2026** ⚠️ Must be live 5 days before the demo
> Server must be stable and fully tested before demo prep begins on May 20

---

## 📋 Phase 1 — Environment Setup (May 8–14)

### Infrastructure
- [ ] Provision production server (cloud/on-prem)
- [ ] Install OS (Ubuntu 22.04 LTS recommended)
- [ ] Configure firewall rules and security groups
- [ ] Setup SSH access with key-based auth
- [ ] Install Docker + Docker Compose

### Dependencies
- [ ] Install Python runtime
- [ ] Install Node.js (for frontend build)
- [ ] Configure environment variables (.env)
- [ ] Install database clients (PostgreSQL, Vector DB)

---

## 📋 Phase 2 — Application Deployment (May 15–19)

### Backend
- [ ] Deploy Backend API container
- [ ] Configure API gateway / reverse proxy (nginx)
- [ ] Set up SSL/TLS certificate (HTTPS)
- [ ] Connect production databases
- [ ] Test all DB connections (ThaiJO fix deployed here)
- [ ] Configure HDC database connector
- [ ] Set up AI model API keys (OpenAI)
- [ ] Test LangGraph agent workflow end-to-end

### Frontend
- [ ] Build production frontend bundle
- [ ] Deploy static frontend
- [ ] Configure domain / subdomain routing
- [ ] Test full user flow: login → query → report → download

### Vector Database
- [ ] Deploy Vector DB (e.g., Qdrant / Weaviate / ChromaDB)
- [ ] Load Document RAG embeddings
- [ ] Verify semantic search returns correct results

---

## 📋 Phase 3 — Production Hardening (May 19–20)

### Performance
- [ ] Configure load balancer
- [ ] Run load tests (simulate concurrent users)
- [ ] Optimize AI processing pipeline for speed
- [ ] Add processing queue / job management

### Monitoring & Observability
- [ ] Set up application monitoring (e.g., Grafana/Prometheus)
- [ ] Configure error alerting
- [ ] Enable audit logging (for citation traceability)
- [ ] Set up log rotation and retention

### Security
- [ ] PDPA compliance review
- [ ] Data encryption at rest and in transit
- [ ] API rate limiting
- [ ] Input sanitization check

### Final Checks
- [ ] Run full regression test suite on production
- [ ] Verify DOCX export works cleanly
- [ ] Verify all citation links are valid
- [ ] Test "Insufficient Evidence" warning triggers correctly
- [ ] Perform final security scan
- [ ] Write server runbook / ops documentation
- [ ] Hand off to ops team

---

## 🚀 Go-Live Criteria

All of the following must be true before marking server as LIVE:

- [ ] All P1 bugs resolved in production
- [ ] Full workflow completes without errors
- [ ] Processing time < 60 seconds for standard reports
- [ ] DOCX exports are clean and properly formatted
- [ ] Monitoring and alerting active
- [ ] At least 1 ops team member trained

---

## 📊 Server Progress

| Phase | Dates | Status |
|-------|-------|--------|
| Phase 1 — Environment | May 8–14 | 🔵 Not Started |
| Phase 2 — Deployment | May 15–19 | 🔵 Not Started |
| Phase 3 — Hardening | May 19–20 | 🔵 Not Started |
| ✅ Go-Live | **May 20** | 🔵 Not Started |

---

*[[00 - Overview/🏠 Project Home | ← Back to Project Home]]*
*[[01 - Sprint Plan/📅 Sprint Overview | → Sprint Plan]]*
