# 📆 Daily Schedule — May 2 to May 25

> Revised plan following updated milestone timeline:
> 🖥️ **Server Live → May 20** | 🎤 **Demo → May 25 before lunch**

---

## 🗓️ Timeline at a Glance

```
May  2 ──── May 11 ──── May 15 ──── May 20 ──── May 25
│                           │            │           │
Sprint 1              Sprint 2      🖥️ Server    🎤 DEMO
Bug Fixes            UX + Data         Live        Lunch
(10 days)            (4 days)       (5 days)    (5 days)
```

---

## 🔴 Sprint 1: May 2–11 — Bug Fixes (10 days)

| Date | Day | Focus | Key Tasks |
|------|-----|-------|-----------|
| May 2 | Fri | **Kickoff + Triage** | Review all survey bugs, assign to devs, create tickets |
| May 3 | Sat | **Backend** | Fix 403 Forbidden — ThaiJO API timeout |
| May 4 | Sun | **Backend** | Fix 403 Forbidden — Diabetes DB access denied |
| May 5 | Mon | **Backend** | Fix data mismatch bug (diabetes query → TB result) |
| May 6 | Tue | **Frontend** | Fix DOCX word-wrap / text overflow on export |
| May 7 | Wed | **Frontend** | Fix broken citation links (404 URLs) |
| May 8 | Thu | **Testing** | Regression tests for all 5 bug fixes |
| May 9 | Fri | **Infra** | Server OS setup, Docker install, nginx config |
| May 10 | Sat | **Infra** | Configure production DB connections + SSL/TLS |
| May 11 | Sun | **Sprint 1 Review** | Verify all bugs fixed, hand off to Sprint 2 team |

✅ **Sprint 1 Exit Criteria:** All P1 bugs resolved, server environment provisioned

---

## 🟡 Sprint 2: May 11–15 — UX + Data (4 days) ⚡

> ⚠️ Only 4 days — focus on demo-critical items only.

| Date | Day | Focus | Key Tasks |
|------|-----|-------|-----------|
| May 11 | Sun | **UX** | Progress bar + % + estimated time remaining |
| May 12 | Mon | **UX** | Redesign preview: vertical → horizontal layout; fix font size |
| May 13 | Tue | **Report** | Add Executive Summary section to report engine |
| May 14 | Wed | **Report + UX** | Add SWOT Analysis section; add prompt template library |
| May 15 | Thu | **Data + Wrap-up** | Connect HDC database; Sprint 2 review → hand off to Infra team |

✅ **Sprint 2 Exit Criteria:** Progress bar live, horizontal preview, Executive Summary + SWOT in all reports, HDC connected

---

## 🖥️ Server Deployment: May 15–20 — Go-Live by May 20

| Date | Day | Focus | Key Tasks |
|------|-----|-------|-----------|
| May 15 | Thu | **Deploy Backend** | Deploy Backend API container to production |
| May 16 | Fri | **Deploy Frontend** | Build + deploy production frontend |
| May 17 | Sat | **Deploy AI + DB** | Deploy Vector DB, load embeddings, connect OpenAI API |
| May 18 | Sun | **Integration Test** | Full end-to-end test on production environment |
| May 19 | Mon | **Load Test + Fix** | Run load tests, fix any performance issues found |
| May 20 | Tue | **🖥️ Server Live** | Final verification — all systems go. Server declared LIVE ✅ |

✅ **Server Exit Criteria:** Full workflow runs on production, DOCX exports cleanly, monitoring active

---

## 🟢 Demo Prep: May 20–24

| Date | Day | Focus | Key Tasks |
|------|-----|-------|-----------|
| May 20 | Tue | **Demo Script** | Write demo script, choose 3 use cases (Accidents / Mental Health / NCDs) |
| May 21 | Wed | **Dry Run 1** | Full end-to-end demo on production — note all issues |
| May 22 | Thu | **Fix + Polish** | Fix issues from dry run 1; polish UI; add "Forgot Password" if time |
| May 23 | Fri | **Dry Run 2** | Final rehearsal — must run perfectly |
| May 24 | Sat | **⛔ Code Freeze** | Bug fixes only. Prepare Q&A. Set up backup demo env. Rest. |

✅ **Demo Prep Exit Criteria:** 3 scenarios run without errors, Q&A prepared, backup env ready

---

## 🎤 May 25 — DEMO DAY

| Time | Activity |
|------|----------|
| Morning | Final environment check + warm-up run |
| Before Lunch | 🎤 **Demo Presentation** |
| After Demo | Collect feedback, document Q&A answers |

---

*[[01 - Sprint Plan/📅 Sprint Overview | ← Sprint Overview]]*
*[[00 - Overview/🏠 Project Home | ← Project Home]]*
