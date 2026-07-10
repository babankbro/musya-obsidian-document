# 📅 Sprint Overview — MUSYA AI Beta Improvement

> **Phase:** Beta Improvement
> **Total Window:** May 2 – May 25, 2026
> **Key Deadlines:**
> - 🖥️ Production Server Live → **May 20**
> - 🎤 Demo Presentation → **May 25, before lunch (12:00)**

---

## 🗓️ Sprint Timeline

```
May  2 ──── May 11 ──── May 15 ──── May 20 ──── May 25
│                           │            │           │
Sprint 1              Sprint 2      🖥️ Server    🎤 DEMO
Bug Fixes            UX + Data         Live        Lunch
```

---

## 🔴 Sprint 1 — Critical Bug Fixes (May 2–11)

**Goal:** Fix all blockers that prevent correct output. Use the extra days to also begin server environment setup.

- [ ] #fix Fix **403 Forbidden** errors — ThaiJO connection timeout
- [ ] #fix Fix **403 Forbidden** — Diabetes database access denied
- [ ] #fix Fix **DOCX word-wrap** and text overflow issues in exported file
- [ ] #fix Fix **broken citation links** — some reference URLs return 404
- [ ] #fix Fix **incorrect data mapping** — e.g. diabetes query returning TB data
- [ ] #infra Begin server environment setup (OS, Docker, dependencies)
- [ ] #infra Configure production database connections
- [ ] #infra Set up SSL/TLS and reverse proxy (nginx)
- [ ] #test Write regression tests for all bug fixes

**Definition of Done:** All 403 errors resolved, DOCX exports cleanly, no broken links, server environment ready

---

## 🟡 Sprint 2 — UX + Data (May 11–15) ⚠️ 4 Days Only

**Goal:** Ship highest-impact UX changes and critical data connections. Prioritize ruthlessly — server deployment begins May 15.

### UX / Frontend (Must-have for demo)
- [ ] #ux Add **progress bar / % indicator** during AI processing
- [ ] #ux Add **estimated time remaining** display during generation
- [ ] #ux Redesign **preview layout** from vertical → **horizontal/landscape**
- [ ] #ux Reduce **font size** in preview panel (currently too large)
- [ ] #ux Add **prompt template library** — preset prompts for beginners
- [ ] #ux Add **"Forgot Password"** feature on login page

### Report Structure (Must-have for demo)
- [ ] #report Add **Executive Summary (บทสรุปผู้บริหาพ)** section to all reports
- [ ] #report Add **SWOT Analysis** section to reports

### Data (Critical only)
- [ ] #data Connect **HDC (Health Data Center)** — Ministry of Public Health
- [ ] #data Add **district/village level risk point data** (จุดเสี่ยงระดับหมู่บ้าน)

### Deferred to Post-Demo
> The following were planned for Sprint 2 but are deferred due to the tight 4-day window:
> output format selector, pre-built menu buttons, PDCA, Six Building Blocks, PubMed, NHES, Police data

**Definition of Done:** Progress bar works, preview is horizontal, executive summary + SWOT appear in all new reports

---

## 🖥️ Server Deployment Sprint (May 15–20) — Deadline May 20

**Goal:** Production server live and stable by May 20 — 5 days before demo

- [ ] #infra Deploy Backend API to production
- [ ] #infra Deploy frontend (production build)
- [ ] #infra Deploy Vector DB + load document embeddings
- [ ] #infra Connect all production databases (with bug fixes from Sprint 1)
- [ ] #infra Configure AI model API keys (OpenAI)
- [ ] #infra Configure monitoring + error alerting
- [ ] #infra Run load tests
- [ ] #infra Full end-to-end test on production environment
- [ ] ✅ **Server Live — May 20**

**Definition of Done:** Full workflow runs on production server without errors. DOCX export clean. All critical bugs confirmed fixed in prod.

---

## 🟢 Demo Prep Sprint (May 20–24)

**Goal:** Polish and rehearse — server is already live, focus only on demo quality

- [ ] #ux Add **output format selector** (DOCX, XLSX, JPG) — if time allows
- [ ] #ux Add **pre-built menu buttons** (Strategic Plan / Action Plan) — if time allows
- [ ] #demo Write demo script and scenario (แนวทางการสาธิต)
- [ ] #demo Select 3 showcase use cases: Road Accidents / Mental Health / NCDs
- [ ] #demo **Dry run 1** — full end-to-end on production (May 21)
- [ ] #demo Fix issues from dry run 1
- [ ] #demo **Dry run 2** — final rehearsal (May 23)
- [ ] #demo Prepare Q&A answers for anticipated questions
- [ ] #demo Set up backup demo environment
- [ ] ⛔ **May 24 — Code freeze** (bug fixes only)

**Definition of Done:** 3 demo scenarios run cleanly on production, Q&A prepared, backup env ready

---

## 🎤 Demo Day — May 25 (Before Lunch)

- [ ] Final environment check (morning)
- [ ] Demo: Road Accidents use case
- [ ] Demo: Mental Health use case
- [ ] Demo: NCDs use case
- [ ] Showcase: progress bar, horizontal preview, executive summary, SWOT
- [ ] Collect post-demo feedback

---

## 📊 Progress Tracker

| Sprint | Dates | Tasks | Done | % |
|--------|-------|-------|------|---|
| Sprint 1 (Bug Fixes) | May 2–11 | 9 | 0 | 0% |
| Sprint 2 (UX + Data) | May 11–15 | 10 | 0 | 0% |
| Server Deployment | May 15–20 | 9 | 0 | 0% |
| Demo Prep | May 20–24 | 10 | 0 | 0% |

---

*[[01 - Sprint Plan/📆 Daily Schedule July 10-29 (เฟส 2) | → ตารางกำหนดงานรายวัน 10–29 ก.ค. (เฟส 2)]]*
*[[00 - Overview/🏠 Project Home | ← Back to Project Home]]*
