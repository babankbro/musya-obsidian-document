# 🔗 Traceability Matrix — Epic ↔ แบบฟอร์มประเมิน

> **วัตถุประสงค์:** แทร็กความเชื่อมโยงแบบสองทาง (Bi-directional Traceability)
> - **(A) Epic ตอบฟอร์มไหน:** เพื่อให้ทีมพัฒนารู้ว่า ฟีเจอร์ที่กำลังทำ (Epic) จะไปช่วยดึงคะแนนของฟอร์มไหนหรือข้อย่อยใดขึ้นบ้าง
> - **(B) ฟอร์มไหนแก้ด้วยอะไร:** เพื่อให้นักวิจัยสามารถไล่ดูได้ว่า ถ้าฟอร์มนี้คะแนนตก จะต้องไปจี้ทีมพัฒนาที่งานไหน (Epic/FR/BUG)
> 
> **ผูกกับเอกสารอื่น:** 
> - ปัญหาทั้งหมด: [[04 - Feature Backlog/🛠️ Consolidated Backlog — Root Fixes (เฟส 2)|Consolidated Backlog (E1–E18)]] 
> - วิธีแก้ต่อคำถาม: [[08 - Analysis/🧩 วิธีแก้รายหัวข้อย่อย ครบ 10 แบบฟอร์ม|วิธีแก้รายหัวข้อย่อย]] 
> - สรุปปัญหาภาพรวม: [[08 - Analysis/📊 การวิเคราะห์ Gap ต่อแบบฟอร์มประเมิน 10 ชุด|Gap Analysis]]

> [!info] กติกาตาราง
> - ทิศ A: Epic ที่ตอบ **หลายฟอร์ม** แตกเป็น **หลายแถว** (แถวละ 1 ฟอร์ม)
> - ทิศ B: ใช้ไล่ย้อนจากฟอร์ม → หางาน/FR/BUG ที่เกี่ยวข้องทั้งหมด

---

# 🅰️ ทิศ A — Epic → แบบฟอร์ม → ข้อย่อย/คำถาม

| Epic | งาน | เติมช่องว่างเรื่อง | ปรากฏในแบบฟอร์ม | ข้อย่อย / คำถาม |
|------|-----|-------------------|-----------------|------------------|
| **E0** | Phase-1 Regression Guard | ความเร็ว/layout/scrollbar คงไว้ | 2 SUS | Q3 ใช้ง่าย |
| E0 | " | " | 3 UEQ | Efficiency |
| E0 | " | " | 4 NASA-TLX | Temporal Demand |
| E0 | " | " | 10 Think-Aloud | หา scrollbar/ปุ่ม export |
| E0 | " | " | (นอกชุด) Policy Impact | ลดเวลาวิเคราะห์ |
| **E1** | Determinism / Reproducibility | ผลไม่นิ่ง (FR-R2-01/BUG-R2-01) | 2 SUS | Q6 ความสอดคล้อง, Q9 มั่นใจ |
| E1 | " | " | 3 UEQ | Dependability |
| E1 | " | " | 4 NASA-TLX | Frustration |
| E1 | " | " | 5 TAM3 §5.3 | BI เจตนาใช้ต่อ |
| E1 | " | " | 5 TAM3 §5.4 | Trust in AI: ผลเชื่อถือได้ |
| E1 | " | " | 7 Benchmark | ROUGE-L (วัดซ้ำได้) |
| E1 | " | " | 9 Focus Group | "เชื่อผลได้แค่ไหน" |
| E1 | " | " | 10 Think-Aloud | "ผลแต่ละครั้งไม่เหมือน" |
| **E2** | Retrieval ตรงปี + Citation | ผิดปี/citation หาย (FR-R2-02/05, BUG-004) | 3 UEQ | Dependability |
| E2 | " | " | 6 Rubric | ความถูกต้อง, Evidence-based |
| E2 | " | " | 7 Benchmark | Factual Accuracy |
| E2 | " | " | 8 Comparative | ความน่าเชื่อถือผล |
| E2 | " | " | 9 Focus Group | citation |
| E2 | " | " | 5 TAM3 §5.4 | Trust in AI: ใช้ข้อมูลเหมาะสม, มั่นใจตัดสินใจ |
| **E3** | Calculation Accuracy | ตัวแปร/หน่วยคลาด (BUG-R2-04, BUG-012) | 6 Rubric | ความถูกต้องข้อมูล |
| E3 | " | " | 7 Benchmark | Factual Accuracy |
| E3 | " | " | 5 TAM3 §5.4 | Trust in AI: ผลเชื่อถือได้ |
| **E4** | Instruction-Following | รายงานไม่ตรงคำสั่ง (BUG-R2-03) | 2 SUS | Q5 ฟังก์ชันเข้ากัน |
| E4 | " | " | 4 NASA-TLX | Performance |
| E4 | " | " | 6 Rubric | Clarity |
| E4 | " | " | 10 Think-Aloud | "สั่งแล้วได้ไม่ตรง", Partial Edit |
| E4 | " | " | 5 TAM3 §5.4 | Trust in AI: ลดข้อผิดพลาดวิเคราะห์ |
| **E5** | Prompt Template + Menu | ไม่รู้จะพิมพ์อะไร (FR-003/008) | 2 SUS | Q2, Q4, Q7, Q10 |
| E5 | " | " | 3 UEQ | Perspicuity |
| E5 | " | " | 4 NASA-TLX | Mental Demand |
| E5 | " | " | 5 TAM3 §5.2 | PEOU |
| E5 | " | " | 9 Focus Group | "ขอแล้วยังไม่มี" |
| E5 | " | " | 10 Think-Aloud | "ไม่รู้จะพิมพ์อะไร" |
| **E6** | Report Structure Templates | ขาด Exec/SWOT/PDCA/6BB/งบ (FR-001/002/009/010/011) | 4 NASA-TLX | Effort (Exec Summary) |
| E6 | " | " | 6 Rubric | ความครบโครงสร้าง, งบประมาณ |
| E6 | " | " | 8 Comparative | ความครบโครงสร้าง |
| E6 | " | " | (นอกชุด) Policy Impact | จัดสรรทรัพยากร |
| **E7** | KPI Numeric Input | เป้าลอย ไม่อิงตัวเลข (FR-R2-03) | 6 Rubric | Feasibility |
| E7 | " | " | 8 Comparative | อิงเป้า KPI จริง |
| E7 | " | " | (นอกชุด) Policy Impact | จัดสรรทรัพยากร |
| **E8** | Forecasting + Comparative | แค่สรุปอดีต (FR-R2-04/08) | 3 UEQ | Stimulation, Novelty |
| E8 | " | " | 5 TAM3 §5.1 | PU |
| E8 | " | " | 6 Rubric | มุมมองอนาคต |
| E8 | " | " | 8 Comparative | ความสามารถวิเคราะห์ |
| E8 | " | " | (นอกชุด) Policy Impact | ตัดสินใจเร็ว, ยกคุณภาพนโยบาย |
| **E9** | Data Foundation (5 จว.+ชาติ) | ข้อมูลไม่ครบ (FR-R2-06/07/09/10) | 2 SUS | Q6 (controlled vocab) |
| E9 | " | " | 6 Rubric | คุณภาพข้อมูลต้นทาง |
| E9 | " | " | 7 Benchmark | BERTScore (ข้อมูลครบ) |
| E9 | " | " | 9 Focus Group | "ครอบคลุมเขต 10 ไหม" |
| E9 | " | " | 5 TAM3 §5.4 | Trust in AI: ใช้ข้อมูลเหมาะสม, ใช้ในราชการ |
| **E10** | Export & Output Formats | รูปแบบไฟล์/DOCX ตกบรรทัด (FR-007/015, BUG-005) | 2 SUS | Q1 อยากใช้บ่อย |
| E10 | " | " | 6 Rubric | นำไปใช้จริงได้ทันที |
| E10 | " | " | 8 Comparative | ผลผลิตพร้อมใช้ |
| **E11** | PDPA & Security / File Upload | ความปลอดภัย/กฎหมาย (FR-013/014/036) | 5 TAM3 §5.3 | BI (ความเชื่อมั่น) |
| E11 | " | " | 5 TAM3 §5.4 | Trust in AI: ใช้ในราชการได้ |
| **E12** | Sub-district / Village | เจาะตำบล/หมู่บ้าน (FR-006/016, BUG-015) | 6 Rubric | ความครบถ้วน/ระบุปัญหาชัด |
| E12 | " | " | 8 Comparative | ความละเอียดวิเคราะห์ |
| E12 | " | " | (นอกชุด) Policy Impact | ระบุปัญหาชัด |
| **E13** | Eval Harness & Observability | วัดผล/จับ regression (งานใหม่) | ทุกฟอร์ม | ทางอ้อม (ยืนยันว่าแก้แล้วดีขึ้น) |
| **E14** | Domain Data Expansion | ขยายโดเมน (FR-016–031) | 6 Rubric | ครอบคลุมโดเมน |
| E14 | " | " | 7 Benchmark | Factual Accuracy |
| E14 | " | " | (นอกชุด) Policy Impact | ครอบคลุมปัญหาสุขภาพ |
| **E15** | Token / Quota / Cost | คุมต้นทุน/abuse (FR-034) | (Ops) | ไม่ผูกฟอร์มโดยตรง |
| **E16** | Accessibility & Readability | ฟอนต์/contrast (FR-035, BUG-009) | 2 SUS | Q3 ใช้ง่าย |
| E16 | " | " | 3 UEQ | Attractiveness, Perspicuity |
| **E17** | In-App Feedback Loop | เก็บ feedback ในระบบ (งานใหม่) | 9 Focus Group | ช่องรับความเห็น |
| E17 | " | " | 10 Think-Aloud | รายงานปัญหาทันที |
| E17 | " | " | 5 TAM3 §5.4 | Trust in AI: ลดข้อผิดพลาด (loop ปรับปรุง) |
| **E18** | Academic / Reference DB | แหล่งวิชาการ + 403 ThaiJO (FR-032/033, BUG-001) | 6 Rubric | Evidence-based |
| E18 | " | " | 7 Benchmark | Factual Accuracy |

---

# 🅱️ ทิศ B — ย้อนกลับ: แต่ละแบบฟอร์ม ตอบด้วยอะไรบ้าง

> ใช้ไล่ตรวจ "ฟอร์มนี้คะแนนต่ำ ต้องไปแตะงานไหน/FR/BUG ไหน"

## 📋 ฟอร์ม 1 — Demographics
| ข้อย่อย | Epic | Feature / BUG |
|--------|------|---------------|
| ⬜ ไม่ให้คะแนน — ใช้แบ่งกลุ่ม (segment) วิเคราะห์ผลฟอร์มอื่น | — | (ตัวแปรควบคุม/บริบทผู้ใช้) |

## 📋 ฟอร์ม 2 — SUS
| ข้อย่อย | Epic | Feature / BUG |
|--------|------|---------------|
| Q2,Q4,Q7,Q10 ใช้ง่าย/เรียนเร็ว | E5 | FR-003, FR-008 |
| Q3 ใช้ง่าย | E0, E16 | (เฟส 1), FR-035, BUG-009 |
| Q5 ฟังก์ชันเข้ากัน | E4 | BUG-R2-03 |
| Q6 ความสอดคล้อง | E1, E9 | FR-R2-01, FR-R2-09 |
| Q9 มั่นใจ | E1, E2 | FR-R2-01, FR-R2-05 |
| Q1 อยากใช้บ่อย | E8, E10 | FR-R2-04, FR-007 |

## 📋 ฟอร์ม 3 — UEQ
| ด้าน | Epic | Feature / BUG |
|------|------|---------------|
| Attractiveness | E16, E0 | FR-035 |
| Perspicuity | E5 | FR-003 |
| Efficiency | E0, E1 | (เฟส 1), cache |
| Dependability | E1, E2 | FR-R2-01, FR-R2-05, BUG-R2-01 |
| Stimulation / Novelty | E8 | FR-R2-04, FR-R2-08 |

## 📋 ฟอร์ม 4 — NASA-TLX
| มิติ | Epic | Feature / BUG |
|------|------|---------------|
| Mental Demand | E5 | FR-003, FR-008 |
| Physical Demand | E4 | (Partial Edit) |
| Temporal Demand | E0 | (เฟส 1) |
| Performance | E4 | BUG-R2-03 |
| Effort | E6 | FR-001 |
| Frustration | E1, E2 | FR-R2-01, FR-R2-02 |

## 📋 ฟอร์ม 5 — TAM3 (รวม Trust in AI §5.4)
| แกน | Epic | Feature / BUG |
|-----|------|---------------|
| §5.1 PU | E8 | FR-R2-04 |
| §5.2 PEOU | E5 | FR-003 |
| §5.3 BI | E1, E2, E3, E11 | FR-R2-01/02/05, BUG-R2-04, FR-014 |
| §5.4 Trust: ผลเชื่อถือได้ | E1, E3 | FR-R2-01, BUG-R2-04 |
| §5.4 Trust: ใช้ข้อมูลเหมาะสม | E2, E9 | FR-R2-02, FR-R2-09 |
| §5.4 Trust: ลดข้อผิดพลาด | E4, E9, E17 | BUG-R2-03, FR-R2-10 |
| §5.4 Trust: มั่นใจตัดสินใจ | E2 | FR-R2-05 |
| §5.4 Trust: ใช้ในราชการ | E9, E11 | FR-R2-06, FR-014 |

## 📋 ฟอร์ม 6 — Policy Quality Rubric
| เกณฑ์ย่อย | Epic | Feature / BUG |
|-----------|------|---------------|
| ความครบโครงสร้าง | E6 | FR-001/002/009/010 |
| ความถูกต้องข้อมูล | E2, E3 | FR-R2-02, BUG-R2-04, BUG-012 |
| Evidence-based | E2, E18 | FR-R2-05, FR-032/033, BUG-001 |
| Feasibility | E7 | FR-R2-03 |
| Clarity | E4 | BUG-R2-03 |
| งบประมาณ | E6 | FR-011 |
| มุมมองอนาคต | E8 | FR-R2-04 |
| คุณภาพข้อมูลต้นทาง | E9, E14 | FR-R2-10, FR-016–031 |
| ระดับตำบล | E12 | FR-006, BUG-015 |
| พร้อมใช้ทันที | E10 | FR-007, BUG-005, BUG-011 |

## 📋 ฟอร์ม 7 — Benchmark Scenario
| ตัวชี้วัด | Epic | Feature / BUG |
|----------|------|---------------|
| Factual Accuracy | E2, E3, E14, E18 | FR-R2-02/05, BUG-R2-04, FR-032 |
| ROUGE-L | E1 | FR-R2-01 |
| BERTScore | E4, E9 | BUG-R2-03, FR-R2-06/07 |
| G-Eval (Coherence/Relevance) | E4, E6 | BUG-R2-03, FR-001 |

## 📋 ฟอร์ม 8 — Comparative Study
| มิติ | Epic | Feature / BUG |
|------|------|---------------|
| ความเร็ว | E0 | (เฟส 1) |
| ความครบโครงสร้าง | E6, E10 | FR-001/002, FR-007 |
| ความสามารถวิเคราะห์ | E8, E12 | FR-R2-04/08, FR-006 |
| อิง KPI จริง | E7 | FR-R2-03 |
| ความน่าเชื่อถือผล | E1, E2 | FR-R2-01/05 |

## 📋 ฟอร์ม 9 — Focus Group
| ประเด็น | Epic | Feature / BUG |
|---------|------|---------------|
| "เชื่อผลได้แค่ไหน" | E1, E2 | FR-R2-01/05 |
| "Prompt Template ยังไม่มี" | E5 | FR-003 |
| "ครอบคลุมเขต 10 ไหม" | E9 | FR-R2-06/07/10 |
| "ต่างจากแชตบอตยังไง" | E8 | FR-R2-04 |
| ช่องรับความเห็น | E17 | (งานใหม่) |

## 📋 ฟอร์ม 10 — Think-Aloud (5 Tasks)
| จุดสะดุด | Epic | Feature / BUG |
|----------|------|---------------|
| "ไม่รู้จะพิมพ์อะไร" | E5 | FR-003 |
| "สั่งแล้วได้ไม่ตรง" | E4 | BUG-R2-03 |
| "แก้นิดเดียวต้องสั่งใหม่" | E4 | (Partial Edit) |
| "หา scrollbar/export ไม่เจอ" | E0 | BUG-010 |
| "ผลแต่ละครั้งไม่เหมือน" | E1 | FR-R2-01, BUG-R2-01 |
| รายงานปัญหาทันที | E17 | (งานใหม่) |

## 📌 (นอกชุด 10 ฟอร์ม) — Policy Impact + AI Trust Survey
> [!danger] คนละเครื่องมือ
> คะแนน **AI Trust (3.56→3.23)** และ **Policy Impact (3.56→3.87)** มาจาก **แบบสำรวจรอบ 1–2** ที่ใช้จริง — เป็นคนละชุดกับ battery 10 ฟอร์มนี้ Trust ในฟอร์ม 5 (TAM3 §5.4) เป็นข้อย่อยภายในฟอร์ม ไม่ใช่ฟอร์มที่ 10
| ข้อย่อย | Epic | Feature / BUG |
|--------|------|---------------|
| Impact: ลดเวลา | E0 | (เฟส 1) |
| Impact: ตัดสินใจเร็ว | E6, E8 | FR-001, FR-R2-04 |
| Impact: ระบุปัญหาชัด | E9, E12 | FR-R2-06, FR-006 |
| Impact: จัดสรรทรัพยากร | E6, E7 | FR-011, FR-R2-03 |
| Impact: ยกคุณภาพนโยบาย | E8, E9 | FR-R2-04, FR-R2-06 |

---

> [!success] วิธีใช้แทร็กสองทาง
> - **ออกฟีเจอร์ใหม่ → ทิศ A:** เช็คว่า Epic นี้จะขยับฟอร์ม/ข้อย่อยใดบ้าง
> - **คะแนนฟอร์มตก → ทิศ B:** เปิดฟอร์มนั้น ไล่ Epic/FR/BUG ที่ต้องแตะ

> [!danger] คงไว้ทุกรายงานทางการ
> n=6 เล็ก · ยังไม่ครบเขต 10 (ขาดมุกดาหาร+อำนาจเจริญ) · รอบ 1/2 คนละกลุ่มตัวอย่าง

---

*[[04 - Feature Backlog/🛠️ Consolidated Backlog — Root Fixes (เฟส 2) | ← Consolidated Backlog (E1–E18)]]*
*[[08 - Analysis/🧩 วิธีแก้รายหัวข้อย่อย ครบ 10 แบบฟอร์ม | → วิธีแก้รายหัวข้อย่อย]]*
*[[08 - Analysis/📊 การวิเคราะห์ Gap ต่อแบบฟอร์มประเมิน 10 ชุด | → Gap Analysis]]*
