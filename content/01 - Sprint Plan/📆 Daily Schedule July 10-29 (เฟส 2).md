# 📆 ตารางกำหนดงาน วันต่อวัน — 10–29 กรกฎาคม (เฟส 2)

> แผนลงมือรายวัน ยก Epic **E1–E18** จาก [[04 - Feature Backlog/🛠️ Consolidated Backlog — Root Fixes (เฟส 2)|🛠️ Consolidated Backlog (เฟส 2)]]
> เรียง **จากสำคัญมากไปน้อย** ภายใต้กรอบเวลา 4 หมุดหมาย (Milestone)

> [!success] 🎯 หมุดหมายหลัก (Milestones)
> - 🟢 **15 ก.ค.** — ระบบ **พร้อมนำเข้าข้อมูล 95%** · เชื่อม API ได้ **3 โดเมนหลัก** (อุบัติเหตุ · สุขภาพจิต · NCD)
> - 🟢 **18 ก.ค.** — **นำเข้าข้อมูลเสร็จ 100%** (รวม accident database ที่ยังค้าง)
> - 🟡 **22 ก.ค.** — ระบบ **พร้อม 85%** (ผลนิ่ง + ดึงตรงปี + คำนวณแม่น + เริ่มงานง่าย)
> - 🔴 **29 ก.ค.** — **วันสุดท้าย** ระบบเสร็จสมบูรณ์ ส่งมอบ 100%

---

## 🗓️ Timeline at a Glance

```
ก.ค. 10 ─────── 15 ─────── 18 ─────── 22 ─────────── 29
  │             │           │           │              │
เฟส 1        🟢 นำเข้า    🟢 นำเข้า   🟡 ระบบ        🔴 เสร็จ
วางฐาน+API   95% + API   เสร็จ 100%   พร้อม 85%     100% ส่งมอบ
3 โดเมน      3 โดเมน     (accident)  (AI คุณภาพ)   (final)
(6 วัน)      ▲          (3 วัน)     (4 วัน)        (7 วัน)
```

---

## 🔢 สรุป Epic E1–E18 (เรียงตามลำดับความสำคัญ)

> ชื่อย่อภาษาไทย + ลิงก์ไปหัวข้อเต็มใน Consolidated Backlog · 🔴 = ทำก่อน/ผลกระทบสูงสุด

### 🔴 แกนหลักผลกระทบสูง (ทำก่อน)
| Epic | ชื่อย่อ (ไทย) | ทำเมื่อ |
|------|---------------|---------|
| [[04 - Feature Backlog/🛠️ Consolidated Backlog — Root Fixes (เฟส 2)#🔴 E1 — Determinism / Reproducibility\|E1]] | ผลลัพธ์นิ่ง / ทำซ้ำได้ | 10, 19 ก.ค. |
| [[04 - Feature Backlog/🛠️ Consolidated Backlog — Root Fixes (เฟส 2)#🔴 E2 — Retrieval ตรงปี + Citation\|E2]] | ดึงข้อมูลตรงปี + อ้างอิง (Citation) | 14, 20 ก.ค. |
| [[04 - Feature Backlog/🛠️ Consolidated Backlog — Root Fixes (เฟส 2)#🔴 E3 — Calculation Accuracy\|E3]] | คำนวณแม่นยำ + หน่วยถูก | 20 ก.ค. |
| [[04 - Feature Backlog/🛠️ Consolidated Backlog — Root Fixes (เฟส 2)#🔴 E13 — Evaluation Harness & Observability\|E13]] | Harness วัดผล + Observability | 19, 22, 26 ก.ค. |

### 🟡 ยกประสบการณ์ผู้ใช้ + โครงเอกสาร
| Epic                                                                                                               | ชื่อย่อ (ไทย)                      | ทำเมื่อ |
| ------------------------------------------------------------------------------------------------------------------ | ---------------------------------- | ------- |
| [[04 - Feature Backlog/🛠️ Consolidated Backlog — Root Fixes (เฟส 2)#🟡 E5 — Prompt Template + Preset Menu\|E5]]   | เทมเพลต Prompt + เมนูสำเร็จรูป     | 21 ก.ค. |
| [[04 - Feature Backlog/🛠️ Consolidated Backlog — Root Fixes (เฟส 2)#🟡 E4 — Instruction-Following\|E4]]           | ทำตามคำสั่งผู้ใช้                  | 21 ก.ค. |
| [[04 - Feature Backlog/🛠️ Consolidated Backlog — Root Fixes (เฟส 2)#🟡 E6 — Report Structure Templates\|E6]]      | โครงรายงานมาตรฐาน (Exec/SWOT/PDCA) | 23 ก.ค. |
| [[04 - Feature Backlog/🛠️ Consolidated Backlog — Root Fixes (เฟส 2)#🟡 E10 — Export & Output Formats\|E10]]       | ส่งออกหลายรูปแบบ                   | 25 ก.ค. |
| [[04 - Feature Backlog/🛠️ Consolidated Backlog — Root Fixes (เฟส 2)#🟡 E11 — PDPA & Security / File Upload\|E11]] | PDPA + อัปโหลดไฟล์ปลอดภัย          | 13 ก.ค. |
| [[04 - Feature Backlog/🛠️ Consolidated Backlog — Root Fixes (เฟส 2)#🟡 E17 — In-App Feedback Loop\|E17]]          | Feedback ในแอป                     | 26 ก.ค. |

### 🟢 ฐานข้อมูล + ต่อยอด
| Epic                                                                                                                    | ชื่อย่อ (ไทย)                      | ทำเมื่อ         |
| ----------------------------------------------------------------------------------------------------------------------- | ---------------------------------- | --------------- |
| [[04 - Feature Backlog/🛠️ Consolidated Backlog — Root Fixes (เฟส 2)#🟢 E9 — Data Foundation\|E9]]                      | ฐานข้อมูล 5 จังหวัด + นโยบายชาติ   | 11, 17 ก.ค.     |
| [[04 - Feature Backlog/🛠️ Consolidated Backlog — Root Fixes (เฟส 2)#🟢 E14 — Domain Data Expansion\|E14]]              | ขยายโดเมนข้อมูล (pipeline นำเข้า)  | 11–16 ก.ค.      |
| [[04 - Feature Backlog/🛠️ Consolidated Backlog — Root Fixes (เฟส 2)#🟢 E18 — Academic / Reference DB\|E18]]            | คลังอ้างอิงวิชาการ (ThaiJO/PubMed) | 17 ก.ค.         |
| [[04 - Feature Backlog/🛠️ Consolidated Backlog — Root Fixes (เฟส 2)#🟢 E7 — KPI Numeric Input\|E7]]                    | ป้อน KPI ตัวเลข                    | 23 ก.ค.         |
| [[04 - Feature Backlog/🛠️ Consolidated Backlog — Root Fixes (เฟส 2)#🟢 E8 — Forecasting + Comparative\|E8]]            | พยากรณ์ 5 ปี + เปรียบเทียบ         | 24 ก.ค.         |
| [[04 - Feature Backlog/🛠️ Consolidated Backlog — Root Fixes (เฟส 2)#🟢 E12 — Sub-district / Village Granularity\|E12]] | เจาะระดับตำบล/หมู่บ้าน             | หลัง E9 (สำรอง) |
| [[04 - Feature Backlog/🛠️ Consolidated Backlog — Root Fixes (เฟส 2)#🟢 E15 — Token / Quota / Cost Management\|E15]]    | Token / Quota / ต้นทุน             | 26 ก.ค.         |
| [[04 - Feature Backlog/🛠️ Consolidated Backlog — Root Fixes (เฟส 2)#🟢 E16 — Accessibility & Readability\|E16]]        | การเข้าถึง / อ่านง่าย              | 25 ก.ค.         |

---

## 🟢 เฟส 1 — 10–15 ก.ค. (6 วัน) · นำเข้าข้อมูลพร้อม 95% + API 3 โดเมน

> ⚡ เร่งสาย **ข้อมูล** ก่อน เพราะหมุดหมาย 15 ก.ค. คือ "พร้อมนำเข้า 95%" · เดิน E1 คู่ขนานเป็นฐานทุกอย่าง

| วันที่  | วัน     | โฟกัส                               | งานหลัก (Epic)                                                                                            |
| ------- | ------- | ----------------------------------- | --------------------------------------------------------------------------------------------------------- |
| 10 ก.ค. | ศุกร์   | **Kickoff + วางฐาน**                | ตั้ง ingestion pipeline + schema มาตรฐาน (E14) · ตั้งค่า `temperature=0`+pin model+corpus versioning (E1) |
| 11 ก.ค. | เสาร์   | **API โดเมน 1: NCD**                | เชื่อม HDC / MOPH Open Data โรคไม่ติดต่อ (E14+E9) · validate schema                                       |
| 12 ก.ค. | อาทิตย์ | **API โดเมน 2: สุขภาพจิต**          | เชื่อมสายด่วน/ฆ่าตัวตาย/ยาเสพติด (E14)                                                                    |
| 13 ก.ค. | จันทร์  | **API โดเมน 3: อุบัติเหตุ (เริ่ม)** | เชื่อม endpoint อุบัติเหตุ + **PDPA guard/PII mask ก่อนข้อมูลจริง (E11)**                                 |
| 14 ก.ค. | อังคาร  | **Retrieval ตรงปี**                 | Year-as-filter + คืน citation ต่อย่อหน้า (E2) · controlled vocabulary (E9)                                |
| 15 ก.ค. | พุธ     | **🟢 หมุดหมาย 95%**                 | ตรวจรับ: นำเข้า/ดึงข้อมูล 3 โดเมนได้ 95%, ดึงตรงปี, มี citation · ⚠️ accident DB ยังค้าง                  |

✅ **เกณฑ์ออกเฟส:** API 3 โดเมนเชื่อมได้ · pipeline นำเข้าเสถียร · retrieve ตรงปีมี citation

---

## 🟢 เฟส 2 — 16–18 ก.ค. (3 วัน) · นำเข้าข้อมูลเสร็จ 100%

> 🎯 ปิดงานข้อมูลให้ครบ — เป้าเน้น **accident database** ที่ยังค้าง

| วันที่ | วัน | โฟกัส | งานหลัก (Epic) |
|-------|-----|-------|-----------------|
| 16 ก.ค. | พฤหัส | **นำเข้า Accident DB** | นำเข้า accident database ที่ค้าง (เวลา/เส้นทาง/ตำรวจ) + validate (E14) |
| 17 ก.ค. | ศุกร์ | **เติมฐานให้ครบ** | เพิ่มมุกดาหาร+อำนาจเจริญ ครบ 5 จว. + นโยบายชาติ (E9) · เชื่อมคลังอ้างอิง ThaiJO/PubMed (E18) |
| 18 ก.ค. | เสาร์ | **🟢 หมุดหมาย 100% ข้อมูล** | ตรวจรับ: 3 โดเมน + accident DB ครบ · corpus versioned · SOP/ผู้รับผิดชอบต่อจังหวัด (E9) |

✅ **เกณฑ์ออกเฟส:** นำเข้าข้อมูลครบทุกโดเมนหลัก + accident DB · ข้อมูล 5 จังหวัดครบ

---

## 🟡 เฟส 3 — 19–22 ก.ค. (4 วัน) · ระบบพร้อม 85% (AI คุณภาพ)

> ยก Epic ที่ฉุดคะแนนรอบ 2 มากสุด — ผลนิ่ง → ดึงตรงปี → คำนวณแม่น → เริ่มงานง่าย

| วันที่ | วัน | โฟกัส | งานหลัก (Epic) |
|-------|-----|-------|-----------------|
| 19 ก.ค. | อาทิตย์ | **ผลลัพธ์นิ่ง** | deterministic retrieval + response cache ครบ (E1) · สร้าง golden test set (E13) |
| 20 ก.ค. | จันทร์ | **ตรงปี + คำนวณแม่น** | citation validation/URL ping (E2) · ย้ายคำนวณออกจาก LLM + formula lib + unit registry (E3) |
| 21 ก.ค. | อังคาร | **เริ่มงานง่าย + ตรงคำสั่ง** | คลัง prompt template ≥8 + preset menu (E5) · structured intent + output contract (E4) |
| 22 ก.ค. | พุธ | **🟡 หมุดหมาย 85%** | ตรวจรับ: ผลนิ่ง 100%, ดึงตรงปี+citation, คำนวณผ่าน unit-test · benchmark อัตโนมัติทุก build (E13) |

✅ **เกณฑ์ออกเฟส:** E1+E2+E3+E5+E4 ผ่านเกณฑ์ตรวจรับ · benchmark/regression detector ทำงาน

---

## 🔴 เฟส 4 — 23–29 ก.ค. (7 วัน) · ดันสู่ 100% + ส่งมอบ

> เติมโครงเอกสาร + พยากรณ์ + ส่งออก + ทดสอบเต็มระบบ → ส่งมอบ

| วันที่  | วัน     | โฟกัส                      | งานหลัก (Epic)                                                                        |
| ------- | ------- | -------------------------- | ------------------------------------------------------------------------------------- |
| 23 ก.ค. | พฤหัส   | **โครงรายงาน + KPI**       | section templates: Exec Summary/SWOT/PDCA/6BB (E6) · ฟอร์มป้อน KPI ก่อน generate (E7) |
| 24 ก.ค. | ศุกร์   | **พยากรณ์ + เปรียบเทียบ**  | trend/forecast 5 ปี + ช่วงความเชื่อมั่น · ตารางเทียบจังหวัด/ปี (E8)                   |
| 25 ก.ค. | เสาร์   | **ส่งออก + อ่านง่าย**      | export DOCX/XLSX/PDF/JPG + แก้ word-wrap (E10) · ปรับฟอนต์/contrast (E16)             |
| 26 ก.ค. | อาทิตย์ | **Feedback + ต้นทุน**      | ปุ่ม 👍/👎 + รายงานผิด (E17) · quota/cost dashboard (E15) · regression detector (E13) |
| 27 ก.ค. | จันทร์  | **Integration Test**       | ทดสอบ E2E เต็มระบบ ทุกโดเมน + แก้บั๊กที่เจอ                                           |
| 28 ก.ค. | อังคาร  | **UAT + Polish**           | ทดสอบผู้ใช้จริง + ขัดเกลา + เตรียม code freeze                                        |
| 29 ก.ค. | พุธ     | **🔴 วันสุดท้าย — ส่งมอบ** | ตรวจรับสมบูรณ์ ระบบเสร็จ 100% · ส่งมอบ ✅                                              |

✅ **เกณฑ์ส่งมอบ:** ทุกโดเมนใช้งานได้จริง · export ไม่เพี้ยน · benchmark ผ่าน · เป้าคะแนน SUS 70+ / Trust 4.0+ / Impact 4.3+

---

## ⚠️ ประเด็นค้าง / ความเสี่ยง

> [!warning] ต้องเฝ้าระวัง
> - **Accident database** ยังไม่ได้นำเข้า → จัดคิวแรกในเฟส 2 (16 ก.ค.) หากแหล่งข้อมูลล่าช้าจะกระทบหมุดหมาย 18 ก.ค.
> - **เฟส 1 อัดแน่น** — เชื่อม API 3 โดเมนใน 4 วัน (11–14) หากโดเมนใดติดขัด ให้เลื่อน E18/E12 (งานสำรอง) ออกก่อน
> - **E12 (เจาะตำบล/หมู่บ้าน)** เป็นงานสำรอง หยิบทำเมื่อมี bandwidth เหลือหลัง E9
> - **PDPA (E11)** ต้องเสร็จ **ก่อน** เปิดรับข้อมูลผู้ป่วยจริง (บังคับ 13 ก.ค.)

---

*[[04 - Feature Backlog/🛠️ Consolidated Backlog — Root Fixes (เฟส 2) | ← Consolidated Backlog (รายละเอียด Epic E1–E18)]]*
*[[01 - Sprint Plan/📅 Sprint Overview | ← Sprint Overview]]*
*[[01 - Sprint Plan/📆 Daily Schedule May 2-25 | ← ตารางรายวัน พ.ค. (เฟส 1)]]*
