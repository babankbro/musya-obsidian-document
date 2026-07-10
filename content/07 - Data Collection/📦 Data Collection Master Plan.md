# 📦 Data Collection Master Plan — เขตสุขภาพที่ 10

> **Goal:** Collect all required health data from 5 provinces before server goes live on May 20
> **Start:** May 2 (อุบลราชธานี first)
> **End:** May 19 (QA + upload complete → server ready May 20)

---

## 🗺️ 5 Provinces — เขตสุขภาพที่ 10

| #   | Province       | Key Contact     | Status         | Schedule   |
| --- | -------------- | --------------- | -------------- | ---------- |
| 1   | 🔴 อุบลราชธานี | สสจ.อุบลราชธานี | 🔵 Not Started | May 2–5    |
| 2   | 🟠 ศรีสะเกษ    | สสจ.ศรีสะเกษ    | 🔵 Not Started | May 6–8    |
| 3   | 🟡 ยโสธร       | สสจ.ยโสธร       | 🔵 Not Started | May 9–11   |
| 4   | 🟢 อำนาจเจริญ  | สสจ.อำนาจเจริญ  | 🔵 Not Started | May 12–14  |
| 5   | 🔵 มุกดาหาร    | สสจ.มุกดาหาร    | 🔵 Not Started | May 15–17  |
| —   | QA + Upload    | Data Team       | 🔵 Not Started | May 18–19  |
| —   | ✅ Server Live  | Infra Team      | 🔵 Not Started | **May 20** |

---

## 📊 Data Domains Required (All 5 Provinces)

| #   | Domain               | Data Type              | Source                   |
| --- | -------------------- | ---------------------- | ------------------------ |
| D1  | Road Accidents       | อุบัติเหตุทางถนน       | ตำรวจ + สธ. + บริษัทกลาง |
| D2  | Mental Health        | สุขภาพจิต + ฆ่าตัวตาย  | กรมสุขภาพจิต + HDC       |
| D3  | NCDs                 | เบาหวาน + ความดัน + ไต | HDC + NHES               |
| D4  | Nutrition            | โภชนาการ + BMI         | HDC + โรงเรียน           |
| D5  | Elderly Care         | ผู้สูงอายุ             | HDC + ท้องถิ่น           |
| D6  | Communicable Disease | โรคติดต่อ              | สธ. + กรมควบคุมโรค       |
| D7  | Cancer               | โรคมะเร็ง              | ทะเบียนมะเร็ง            |
| D8  | Population           | ประชากรรายอำเภอ/ตำบล   | กรมการปกครอง             |

---

## 📁 Province Files

- [[07 - Data Collection/🔴 อุบลราชธานี Data]] — May 2–5
- [[🟠 ศรีสะเกษ Data]] — May 6–8
- [[🟡 ยโสธร Data]] — May 9–11
- [[07 - Data Collection/🟢 อำนาจเจริญ Data]] — May 12–14
- [[07 - Data Collection/🔵 มุกดาหาร Data]] — May 15–17
- [[07 - Data Collection/✅ QA & Upload Checklist]] — May 18–19

---

## 🗂️ Data Sources Directory

> [!tip] ข้อมูลนำเข้าชุดใหม่ (ก.ค. 2569)
> แหล่ง + วิธีดึง Open Data ครบ 13 หมวด (แผนเขต · ประชากร · OPD/IPD/ตาย · กำลังคน 7 วิชาชีพ · Service Plan/CMI · งบค่าเสื่อม · ตรวจราชการ ฯลฯ) ดูที่ [[07 - Data Collection/🌐 แหล่งข้อมูลนำเข้าใหม่ & วิธีดึง Open Data|🌐 แหล่งข้อมูลนำเข้าใหม่ & วิธีดึง Open Data]]

| Source                                 | Data Available                                            | Access Method    |
| -------------------------------------- | --------------------------------------------------------- | ---------------- |
| **HDC** (hdcservice.moph.go.th)        | NCD, elderly, maternal, all health indicators by district | Web portal / API |
| **กรมสุขภาพจิต** (dmh.go.th)           | Suicide stats, psychiatric patients, hotline              | Web / request    |
| **ตำรวจภูธรภาค 3**                     | Road accident stats by province/district                  | ขอข้อมูลราชการ   |
| **บริษัทกลางคุ้มครองผู้ประสบภัยจากรถ** | Insurance claims, accident severity                       | ขอข้อมูลราชการ   |
| **NHES** (กรมอนามัย)                   | National Health Examination Survey ครั้งที่ 1–7           | Download / API   |
| **ทะเบียนมะเร็งแห่งชาติ**              | Cancer incidence by province                              | กรมการแพทย์      |
| **กรมการปกครอง**                       | Population by district/sub-district                       | data.go.th       |
| **สสจ. แต่ละจังหวัด**                  | Local stats, risk maps, sub-district breakdowns           | Contact directly |
| **โรงพยาบาลจังหวัด**                   | Admission data, disease burden                            | HIS / request    |

---

## 📋 Data Format Requirements

All data must be delivered in one of these formats to be RAG-ready:

| Format  | Use                                           |
| ------- | --------------------------------------------- |
| `.csv`  | Structured stats (prevalence, rates, counts)  |
| `.xlsx` | Multi-sheet tables with district breakdowns   |
| `.pdf`  | Policy documents, research papers, guidelines |
| `.docx` | Reports, meeting minutes, local studies       |

**Granularity required:** Province → District (อำเภอ) → Sub-district (ตำบล) where available

---

## ⚠️ Collection Rules

1. **PDPA:** Any file containing personally identifiable patient data must be de-identified before upload
2. **Source tagging:** Every dataset must include source name, date, and version in filename: `[province]_[domain]_[source]_[YYYYMM].csv`
3. **Missing data:** If data unavailable, log in [[07 - Data Collection/✅ QA & Upload Checklist]] with reason
4. **Priority order:** HDC first (most complete) → สสจ. → ตำรวจ → hospitals → other

---

*[[00 - Overview/🏠 Project Home | ← Project Home]]* | *[[01 - Sprint Plan/📅 Sprint Overview | Sprint Plan]]*
