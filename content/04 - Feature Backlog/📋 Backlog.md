# 📋 Feature Backlog — MUSYA AI

> All features, improvements, and data requests. Sorted by priority and sprint.

---

## 🔴 Sprint 1 — Must Fix (May 2–9)

- [ ] `BUG` Fix 403 Forbidden — ThaiJO database
- [ ] `BUG` Fix 403 Forbidden — Diabetes database  
- [ ] `BUG` Fix data mismatch — wrong domain returned (diabetes→TB)
- [ ] `BUG` Fix broken citation URLs (404)
- [ ] `BUG` Fix DOCX word-wrap / text overflow
- [ ] `INFRA` Server OS + Docker environment setup
- [ ] `INFRA` Configure production DB connections

---

## 🟡 Sprint 2 — Ship Before Demo (May 10–16)

### Frontend
- [ ] ==`UX` Add processing progress bar + % complete==
- [ ] ==`UX` Add estimated time remaining during generation==
- [ ] ~~`UX` Redesign preview: vertical → horizontal layout~~  ย่อ 3 ส่วนได้ ประวัติ chart เอกสาร
- [ ] `UX` Reduce font size in preview panel (format เอกสารตอนเริ่ม)
- [ ] `UX` Add scrollbar to report preview
- [ ] `UX` Add prompt template library (preset prompts for beginners)
- [ ] `UX` Add "Forgot Password" on login
- [ ] `UX` Add output format selector (DOCX, XLSX, JPG)
	- [ ] รายงาน WORD PDF
	- [ ] อยุ่ใน ช่อง chat ตอนตอบ จะมีตาราง -> XLSX  มีปุ่ม download 
	- [ ] graph เป็น JPG มีปุ่ม download 
- [ ] `UX` Add pre-built menu buttons (Strategic Plan / Action Plan / Project)

### Reports
- [ ] `REPORT` Add Executive Summary section (บทสรุปผู้บริหาร)
- [ ] `REPORT` Add SWOT Analysis section
- [ ] `REPORT` Improve objective clarity in generated plans

### Data
- [ ] `DATA` Connect HDC (Health Data Center) — Ministry of Public Health
- [ ] `DATA` Add NHES survey data (ครั้งที่ 1–7)
- [ ] `DATA` Add police road accident database
- [ ] `DATA` Add village/sub-district level risk point data

---

## 🟢 Sprint 3 — Polish Before Demo (May 17–24)

- [ ] `UX` Visual redesign — modern UI, better colors and layout
- [ ] `UX` Dummy table input for custom output structure
- [ ] `REPORT` Add PDCA analysis framework
- [ ] `REPORT` Add Six Building Blocks of Health System template
- [ ] `REPORT` Add budget allocation analysis section
- [ ] `REPORT` Add sub-district/village level recommendations
- [ ] `FEATURE` PDPA warning on user file upload
- [ ] `FEATURE` User file upload for personal AI analysis
- [ ] `DATA` Add PubMed / Scopus / Web of Science integration
- [ ] `DATA` Add Thai university research databases
- [ ] `INFRA` Production server final configuration

---

## 🔵 Post-Demo / Future Releases

### New Features
- [ ] PowerPoint / Slide export engine
- [ ] Token/usage quota management per user
- [ ] AI asks user for file upload when data is missing (with PDPA check)

### New Data Domains
- [ ] Communicable disease control
- [ ] Elderly care / aging population planning
- [ ] Cancer program data
- [ ] อสม. (Village Health Volunteer) program
- [ ] HR / workforce planning (กรอบอัตรากำลัง)
- [ ] Legal / regulatory framework for public health
- [ ] Mental health: suicide stats by gender/age/method
- [ ] Mental health: drug abuse / addiction data

### Data Expansion
- [ ] Road accidents: time patterns, frequent routes
- [ ] Road accidents: environmental factors (lighting, signs)
- [ ] NCDs: disease-specific diet recommendations
- [ ] NCDs: school nutrition / dietary behavior
- [ ] Medication data across all domains

---

*[[02 - Feedback Analysis/💡 Feature Requests from Feedback | ← Feature Requests]]*
*[[01 - Sprint Plan/📅 Sprint Overview | → Sprint Plan]]*
