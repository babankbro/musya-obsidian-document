# 📋 Feature Backlog — MUSYA AI

> All features, improvements, and data requests. Sorted by priority and sprint.

> [!info] Backlog แบ่งตามรอบประเมิน
> - **รอบ 1 (เฟส 1):** Sprint 1–3 + Post-Demo ด้านล่าง — โฟกัส UX/Performance
> - **รอบ 2 (เฟส 2):** ส่วน "Phase 2 — Trust Through Accuracy" ท้ายไฟล์ ([[#🆕 Phase 2 — Trust Through Accuracy (จากผลประเมินรอบ 2)|กระโดดไปเฟส 2]])

---

# ═══════════ เฟส 1 (จากผลประเมินรอบ 1) ═══════════

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
	- [ ] อยุ่ใน ช่อง chat ตอนตอบ จะมีตาราง -> CSV or XLSX  มีปุ่ม download 
	- [ ] graph เป็น JPG มีปุ่ม download 
- [ ] `UX` Add pre-built menu buttons (Strategic Plan / Action Plan / Project)

### Reports
- [ ] ==`REPORT` Add Executive Summary section (บทสรุปผู้บริหาร)==  *default*
- [ ] ==`REPORT` Add SWOT Analysis section==
- [ ] ==`REPORT` Improve objective clarity in generated plans==

### Data
- [ ] `DATA` Connect HDC (Health Data Center) — Ministry of Public Health
- [ ] `DATA` Add NHES survey data (ครั้งที่ 1–7)
- [ ] `DATA` Add police road accident database
- [ ] `DATA` Add village/sub-district level risk point data

---

## 🟢 Sprint 3 — Polish Before Demo (May 17–24)

- [ ] `UX` Visual redesign — modern UI, better colors and layout
- [ ] ==`UX` Dummy table input for custom output structure==
- [ ] ==`REPORT` Add PDCA analysis framework==
- [ ] ==`REPORT` Add Six Building Blocks of Health System template==
- [ ] ==`REPORT` Add budget allocation analysis section==
- [ ] REPORT Add sub-district/village level recommendations
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

# ═══════════ 🆕 Phase 2 — Trust Through Accuracy (จากผลประเมินรอบ 2) ═══════════

> ที่มา: แบบประเมินรอบ 2 (n=6, พ.ค. 2569) — ดู [[02 - Feedback Analysis/💡 Feature Requests from Feedback#🆕 รอบ 2 — Feature Requests (พ.ค. 2569)|FR-R2-xx]]
> **ธีม:** เปลี่ยนจาก UX/Performance → ความแม่นยำ ความเสถียร และการพยากรณ์

## 🔴 Phase 2-A — Stability & Accuracy (เร่งด่วนสุด)

- [ ] `STABILITY` **(FR-R2-01)** ตรึงผลลัพธ์ให้นิ่ง — temperature=0 / seed / cache (prompt เดิม → ผลเดิม)
  - *แนวทางเพิ่มเติม:* ล็อคพารามิเตอร์ของ AI (Temperature = 0) เฉพาะส่วนดึงสถิติ เพื่อป้องกันผลลัพธ์คลาดเคลื่อน
- [ ] `DATA` **(FR-R2-02)** Year-accurate retrieval — filter ตามปี; ถ้าไม่มีต้องแจ้ง ไม่สลับปีเงียบๆ
  - *แนวทางเพิ่มเติม:* เพิ่ม "ป้ายกำกับปีข้อมูล (Data Year Badge)" บนหัวรายงานให้เห็นชัดเจน
- [ ] `BUG` **(BUG-R2-04 / FR-R2-05)** แก้ตัวแปรในการคำนวณคลาดเคลื่อน
  - *แนวทางเพิ่มเติม:* เพิ่มฟังก์ชัน "อัปโหลดไฟล์เป้าหมาย KPI เฉพาะกิจ" (Custom KPI Upload)
- [ ] `BUG` **(BUG-R2-03)** แก้ "รายงานผลไม่ตรงกับคำสั่ง"
  - *แนวทางเพิ่มเติม:* เพิ่มปุ่ม "ปรับแก้เฉพาะจุด (Partial Edit)" ลดภาระให้ผู้ใช้ไม่ต้องพิมพ์สั่งใหม่ทั้งหมด
- [ ] `BUG` **(BUG-R2-05)** เช็ค Citation regression — คืนการอ้างอิงแหล่งที่มาให้เห็นชัด
  - *แนวทางเพิ่มเติม:* เพิ่มหน้าต่าง "Preview Source Document" ด้านข้าง และบล็อค "Insufficient Evidence" หากไม่พบอ้างอิง
- [ ] `UX` **(FR-003 ค้างจากรอบ 1)** Prompt Template พื้นฐานให้เลือก
  - *แนวทางเพิ่มเติม:* เพิ่ม "คำถามแนะนำถัดไป (Suggested Follow-ups)" ท้ายรายงาน เพื่อไกด์ผู้ใช้

## 🟡 Phase 2-B — User Tools & Data Foundation

- [ ] `FEATURE` **(FR-R2-03)** ช่องป้อนกรอบ KPI/ตัวชี้วัดเป็นตัวเลขก่อน generate แผน
- [ ] `DATA` **(FR-R2-06)** นำเข้านโยบายชาติ: ยุทธศาสตร์ 20 ปี, 30 บาทรักษาทุกที่, นโยบายรัฐ
  - *แนวทางเพิ่มเติม:* สร้าง "ระบบซิงค์ข้อมูลอัตโนมัติ (Automated Data Pipeline)" เชื่อม MOPH API
- [ ] `DATA` **(FR-R2-07)** เชื่อม MOPH Open Data
- [ ] `DATA` **(FR-R2-09)** Controlled vocabulary — กำหนดคำเฉพาะให้เป็นทิศทางเดียวกัน
  - *แนวทางเพิ่มเติม:* จัดทำ "พจนานุกรมข้อมูล (Data Dictionary) เขตสุขภาพที่ 10" ฝังใน System Prompt
- [ ] `PROCESS` **(FR-R2-10)** Data Governance — มาตรฐานนำเข้าข้อมูลครบ/อัปเดต ทุกจังหวัด
  - *แนวทางเพิ่มเติม:* สร้างระบบตรวจสอบคุณภาพข้อมูลก่อนนำเข้า (Data Validation & QA Tool) เพื่อกรอง Human Error
- [ ] `FEATURE` **(NEW)** Custom Template RAG — เปิดให้ สสจ. อัปโหลดต้นแบบเอกสารของตนเองให้ AI เรียนรู้รูปแบบอัตโนมัติ

## 🟢 Phase 2-C — Advanced Analytics

- [ ] `FEATURE` **(FR-R2-04)** Forecasting + Trend Analysis (พยากรณ์ + แนวโน้ม 5 ปี)
  - *แนวทางเพิ่มเติม:* ใช้ Machine Learning พื้นฐานวิเคราะห์เส้นแนวโน้มควบคู่กับ LLM เพื่อเพิ่มความแม่นยำ
- [ ] `REPORT` **(FR-R2-08)** สรุปข้อมูลเชิงเปรียบเทียบ (Comparative Summary)

## 🎯 เป้าหมายคะแนนเฟส 2

- [ ] `KPI` SUS: 55.4 → 70+
- [ ] `KPI` AI Trust: 3.23 → 4.0+
- [ ] `KPI` Policy Impact: 3.87 → 4.3+
- [ ] `EVAL` เก็บข้อมูลเพิ่มให้ครบ 5 จังหวัด (เพิ่มมุกดาหาร + อำนาจเจริญ)
- [ ] `EVAL` จัดทำ Focus Group แยกรายจังหวัด (Provincial Focus Group) เพื่อเจาะ Requirement เชิงลึก

---

# ═══════════ ✅ Checklist ปฏิบัติการต่อแบบฟอร์มประเมิน 10 ชุด ═══════════

> ที่มา: [[08 - Analysis/📊 การวิเคราะห์ Gap ต่อแบบฟอร์มประเมิน 10 ชุด|การวิเคราะห์ Gap ต่อแบบฟอร์ม 10 ชุด]]
> แต่ละ checkbox ผูกกับ FR-R2/BUG-R2 และกลุ่ม Phase 2 (A/B/C) ด้านบน

## 📋 ฟอร์ม 1 — Demographics (⬜ ไม่ให้คะแนน)
- [ ] เก็บข้อมูลผู้ตอบให้ครบ (เพศ/อายุ/ตำแหน่ง/ประสบการณ์) เพื่อใช้ segment ผลฟอร์มอื่น
- [ ] ครอบให้ครบ 5 จังหวัด (รวมมุกดาหาร + อำนาจเจริญ) ก่อนสรุปเชิงปริมาณ

## 📋 ฟอร์ม 2 — SUS (55.4 → 70+)
- [ ] FR-003 Prompt Template พื้นฐาน *(ค้าง 2 รอบ)*
- [ ] รักษาผลเฟส 1 ไม่ให้ regress (progress bar, layout)
- [ ] FR-008 ปุ่มเมนูสำเร็จรูปลดขั้นตอน
- [ ] ทดสอบซ้ำเฉพาะ 5 จังหวัด เพื่อลด outlier

## 📋 ฟอร์ม 3 — UEQ
- [ ] FR-R2-01 ผลนิ่ง + FR-R2-05 citation → ยกด้าน Dependability
- [ ] คงความเร็วเฟส 1 → ด้านประสิทธิภาพ
- [ ] FR-R2-04 พยากรณ์ → ด้านแปลกใหม่/กระตุ้น

## 📋 ฟอร์ม 4 — NASA-TLX (ลดภาระคิด < 40)
- [ ] FR-003 Prompt Template + FR-008 เมนู → ลด Mental Demand
- [ ] BUG-R2-03 แก้รายงานไม่ตรงคำสั่ง → ลด Frustration
- [ ] Exec Summary นำหน้า → ลด Effort การอ่าน

## 📋 ฟอร์ม 5 — TAM3 (≥ 4/5, รวม Trust in AI §5.4)
- [ ] §5.1 รักษา PU (ประโยชน์สูงอยู่แล้ว)
- [ ] §5.2 FR-003 + UI เฟส 1 → ยก PEOU
- [ ] §5.3 แก้ Phase 2-A (G1–G4) → ยก BI เจตนาใช้ต่อ
- [ ] §5.4 Trust in AI → แก้ stability+accuracy + FR-R2-05 citation + FR-R2-06/07/10 ข้อมูลครบ

## 📋 ฟอร์ม 6 — Policy Quality Rubric (≥ 3.5/5)
- [ ] FR-001/002/009/010 เติม Exec Summary/SWOT/PDCA/6BB
- [ ] BUG-R2-04 ตัวแปรคำนวณ + FR-R2-02 ข้อมูลตรงปี
- [ ] FR-R2-03 KPI numeric input
- [ ] งบประมาณ + FR-R2-04 พยากรณ์

## 📋 ฟอร์ม 7 — Benchmark Scenario (F.Acc ≥ 0.85)
- [ ] FR-R2-01 ผลนิ่ง *(เงื่อนไขจำเป็นก่อนวัด)*
- [ ] FR-R2-02 ตรงปี + FR-R2-05 citation
- [ ] BUG-R2-04 แก้สูตรคำนวณ
- [ ] FR-R2-06/07/10 ข้อมูลครบ 5 จังหวัด + นโยบายชาติ

## 📋 ฟอร์ม 8 — Comparative Study
- [ ] FR-001/002/009/010 ชนะ baseline ด้านโครงสร้าง
- [ ] FR-R2-04/08 พยากรณ์/เปรียบเทียบ = จุดต่างจากงานมือ
- [ ] FR-R2-03 KPI input เทียบกับแผนจริง

## 📋 ฟอร์ม 9 — Focus Group
- [ ] เตรียมตอบประเด็น Trust (citation, ผลนิ่ง)
- [ ] โชว์ roadmap เฟส 2 + เคลียร์ FR-003 ที่ค้าง

## 📋 ฟอร์ม 10 — Think-Aloud (5 Tasks)
- [ ] FR-003 แก้ "ไม่รู้จะพิมพ์อะไร"
- [ ] BUG-R2-03 instruction-following
- [ ] คง scrollbar/layout เฟส 1

## 📌 (นอกชุด 10 ฟอร์ม) — Policy Impact Survey (≥ 4/5)
> [!danger] คนละเครื่องมือ — Trust in AI อยู่ในฟอร์ม 5 (TAM3 §5.4) ไม่ใช่ฟอร์มที่ 10
- [ ] Phase 2-A (G1–G4) แก้ stability+accuracy ก่อน
- [ ] FR-R2-05 citation เห็นชัด = ตรวจสอบย้อนได้
- [ ] FR-R2-04 พยากรณ์ + FR-R2-06 นโยบายชาติ → ยก Impact

---

*[[02 - Feedback Analysis/💡 Feature Requests from Feedback | ← Feature Requests]]*
*[[08 - Analysis/📊 การวิเคราะห์ Gap ต่อแบบฟอร์มประเมิน 10 ชุด | → การวิเคราะห์ Gap ต่อฟอร์ม 10 ชุด]]*
*[[04 - Feature Backlog/🛠️ Consolidated Backlog — Root Fixes (เฟส 2) | → Consolidated Backlog (9 Epic ราก)]]*
*[[01 - Sprint Plan/📅 Sprint Overview | → Sprint Plan]]*
*[[08 - Analysis/📊 MUSYA AI เปรียบเทียบผลประเมิน รอบ 1-2 | → รายงานเปรียบเทียบรอบ 1-2]]*
