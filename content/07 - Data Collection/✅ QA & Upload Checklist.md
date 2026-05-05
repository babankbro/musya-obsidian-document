# ✅ QA & Upload Checklist — All 5 Provinces

> **Schedule: May 18–19**
> **Goal:** Verify every dataset, fix gaps, and upload all files to the server before May 20 go-live
> **Owner:** Data Team

---

## 📅 Day-by-Day Plan

| Date | Day | Tasks |
|------|-----|-------|
| May 18 | Sun | QA all province files — completeness + format + naming check |
| May 19 | Mon | Fix gaps, de-identify PDPA data, upload to server, verify RAG ingestion |
| May 20 | Tue | ✅ Server Live — data ingested and searchable |

---

## 📊 Province Completion Tracker

| Province | Prefix | Files Due | Received | QA Pass | Uploaded |
|----------|--------|-----------|----------|---------|---------|
| 🔴 อุบลราชธานี | `ubon_` | May 5 | ⬜ | ⬜ | ⬜ |
| 🟠 ศรีสะเกษ | `ssk_` | May 8 | ⬜ | ⬜ | ⬜ |
| 🟡 ยโสธร | `yst_` | May 11 | ⬜ | ⬜ | ⬜ |
| 🟢 อำนาจเจริญ | `amn_` | May 14 | ⬜ | ⬜ | ⬜ |
| 🔵 มุกดาหาร | `mkd_` | May 17 | ⬜ | ⬜ | ⬜ |

---

## 📋 Domain Completion Matrix

> ✅ = Complete | ⚠️ = Partial | ❌ = Missing | — = Not applicable

| Domain            | อุบล | ศรีสะเกษ | ยโสธร | อำนาจเจริญ | มุกดาหาร |
| ----------------- | ---- | -------- | ----- | ---------- | -------- |
| D1 Road Accidents | 🔵   | 🔵       | 🔵    | 🔵         | 🔵       |
| D2 Mental Health  | 🔵   | 🔵       | 🔵    | 🔵         | 🔵       |
| D3 NCDs           | 🔵   | 🔵       | 🔵    | 🔵         | 🔵       |
| D4 Nutrition      | 🔵   | 🔵       | 🔵    | 🔵         | 🔵       |
| D5 Elderly        | 🔵   | 🔵       | 🔵    | 🔵         | 🔵       |
| D6 Communicable   | 🔵   | 🔵       | 🔵    | 🔵         | 🔵       |
| D7 Cancer         | 🔵   | 🔵       | 🔵    | 🔵         | 🔵       |
| D8 Population     | 🔵   | 🔵       | 🔵    | 🔵         | 🔵       |

> Update status: 🔵 Not Started → ⚠️ Partial → ✅ Done → ❌ Missing/Blocked

---

## 🔍 QA Checklist — Per File

For every file received, verify all of the following before upload:

### Format & Naming
- [ ] Filename follows convention: `[prefix]_[domain]_[source]_[YYYYMM].csv`
- [ ] File is in correct format (`.csv` / `.xlsx` / `.pdf` / `.docx`)
- [ ] File opens without encoding errors (UTF-8 for Thai text)
- [ ] No corrupted or empty sheets

### Content
- [ ] Data covers at least **3 years** (minimum), ideally 5 years
- [ ] Data is broken down to **district (อำเภอ) level** minimum
- [ ] Sub-district (ตำบล) level included where available
- [ ] Column headers are in Thai or English — no mixed/unclear labeling
- [ ] Units are clearly labeled (ราย / อัตราต่อแสนประชากร / %)
- [ ] No blank rows or merged cells in structured data files
- [ ] Source name and year are documented in the file or filename

### PDPA Compliance
- [ ] No patient names, ID card numbers, or full addresses
- [ ] No individually identifiable data — aggregated to village level minimum
- [ ] If in doubt: escalate to data lead before upload

### Source Verification
- [ ] Source institution is noted (HDC / ตำรวจ / กรมสุขภาพจิต / etc.)
- [ ] Data aligns with known regional statistics (no obvious outliers)
- [ ] At least one cross-check done (e.g., HDC vs. hospital report for same indicator)

---

## 📝 Missing Data Log

> Log all data that could NOT be collected, with reason. This feeds into the "Data Gaps" backlog for post-demo follow-up.

| Province | Domain | Data Item | Reason Missing | Alternative / Next Step |
|----------|--------|-----------|----------------|------------------------|
| | | | | |

---

## 🚀 Upload Procedure (May 19)

1. **Organize** — place all verified files in `/data/[province]/[domain]/` folder structure
2. **Vector embedding** — run embedding pipeline for all `.pdf` and `.docx` files (Document RAG)
3. **Database import** — import all `.csv` and `.xlsx` files into Health Statistics DB (Database RAG)
4. **Index verification** — run sample queries against each domain per province to confirm data is searchable
5. **Smoke test** — generate 1 test report per province using MUSYA AI and verify citations resolve correctly
6. **Sign off** — data lead confirms all 5 provinces ingested → hand off to infra team for May 20 go-live

---

## 🧪 Smoke Test Queries (May 19)

Run one query per province after upload to verify end-to-end RAG works:

| Province | Test Query | Expected Output |
|----------|-----------|----------------|
| อุบลราชธานี | "อัตราป่วยเบาหวานรายอำเภอ จังหวัดอุบลราชธานี" | ตาราง + citation จาก HDC |
| ศรีสะเกษ | "จุดเสี่ยงอุบัติเหตุทางถนน จังหวัดศรีสะเกษ" | รายการจุดเสี่ยง + citation |
| ยโสธร | "อัตราฆ่าตัวตาย จังหวัดยโสธร 5 ปีล่าสุด" | กราฟ/ตาราง + citation |
| อำนาจเจริญ | "ผู้สูงอายุติดเตียง จังหวัดอำนาจเจริญ" | ตัวเลขรายอำเภอ + citation |
| มุกดาหาร | "โรคไข้เลือดออก จังหวัดมุกดาหาร รายปี" | สถิติรายปี + citation |

---

## 📁 Expected Total File Count

| Province | Min Files | Max Files |
|----------|-----------|-----------|
| อุบลราชธานี | 18 | 25 |
| ศรีสะเกษ | 16 | 22 |
| ยโสธร | 16 | 22 |
| อำนาจเจริญ | 16 | 22 |
| มุกดาหาร | 16 | 22 |
| **Total** | **82** | **113** |

---

*[[07 - Data Collection/🔵 มุกดาหาร Data | ← มุกดาหาร]]* | *[[07 - Data Collection/📦 Data Collection Master Plan | ← Master Plan]]*
