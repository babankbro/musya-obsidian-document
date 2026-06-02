# 🐛 Bug Report — Derived from User Survey Feedback

> Priority: P1 = Must fix before demo | P2 = Fix in Sprint 2 | P3 = Backlog

> [!info] เอกสารนี้แยกเป็น 2 รอบการประเมิน
> - **รอบ 1** (22 เม.ย. 2569, n=24) — BUG-001 ถึง BUG-015 ด้านล่าง
> - **รอบ 2** (25–27 พ.ค. 2569, n=6) — BUG-R2-xx ท้ายไฟล์ ([[#🆕 รอบ 2 — Bug Report (พ.ค. 2569)|กระโดดไปรอบ 2]])

---

# ═══════════ รอบ 1 (22 เม.ย. 2569) ═══════════

> All bugs identified from the April 22, 2026 user survey responses.

## 🔴 P1 — Critical (Must Fix Before Demo May 25)

| ID | Bug | Source | Details |
|----|-----|--------|---------|
| BUG-001 | 403 Forbidden — ThaiJO | n.prasertpong, sdokdung | "การเชื่อมต่อฐานข้อมูล ThaiJO ขัดข้องเนื่องจากหมดเวลา (Timeout)" |
| BUG-002 | 403 Forbidden — Diabetes DB | n.prasertpong | "การเข้าถึงข้อมูล Diabetes ถูกปฏิเสธ (Forbidden)" |
| BUG-003 | Wrong data returned | saopothar | "ขอข้อมูลผู้ป่วยเบาหวาน ไปออกข้อมูลวัณโรค" (asked diabetes, returned TB data) |
| BUG-004 | Broken citation links | saopothar, n.prasertpong | "บางลิงค์กดเข้าไปไม่พบข้อมูล" |
| BUG-005 | DOCX word-wrap issue | kongsila04 | "ส่งไฟล์ออกมา พบปัญหาต้องมาแก้ไขคำที่ตกบรรทัด" |
| BUG-006 | No progress indicator | n.prasertpong, jit_tapon | "progress bar หรือ % ความคืบหน้า ไม่มีแสดง" |
| BUG-007 | Slow processing | 10+ users | Almost every respondent mentioned "ประมวลผลช้า" |

---

## 🟡 P2 — High (Fix in Sprint 2, before May 25)

| ID | Bug | Source | Details |
|----|-----|--------|---------|
| BUG-008 | Preview layout is vertical | panwanlee | "หน้าจอปฏิบัติการเป็นแนวตั้ง อ่านไม่ถนัด" |
| BUG-009 | Font too large in preview | saopothar, nualchaweenualnurse | "ตัวอักษรอ่านค่อนข้างยาก" / "ตัวใหญ่ล้นหน้า" |
| BUG-010 | No scroll bar in report view | n.prasertpong | "Scrollbar หลังสร้างแผนงาน ที่ให้ส่งออกมาแล้วยังไม่มี" |
| BUG-011 | Output not ready to submit directly | nugrataeee | "ไฟล์งานที่ได้ยังไม่สามารถใช้งานได้ทันที ไม่ใช่รูปแบบของเอกสารวิชาการ" |
| BUG-012 | Unit mismatch in data input | panwanlee | "เรื่องหน่วยนับ เช่น ราย อัตราป่วย/ประชากร" affects output accuracy |

---

## 🟢 P3 — Medium (Post-demo / Backlog)

| ID | Bug | Source | Details |
|----|-----|--------|---------|
| BUG-013 | No "Forgot Password" | charinrat | "อยากให้เพิ่ม ลืมรหัสผ่าน" |
| BUG-014 | Text objectives unclear | nugrataeee | "วัตถุประสงค์ไม่ตอบโจทย์ยังไม่ค่อยชัดเจน" |
| BUG-015 | Province-only analysis | rangsan2517 | "ยังไม่สามารถจัดการเป็นระดับอำเภอได้" |

---

## 📋 Bug Fix Assignment Template

```markdown
## BUG-XXX: [Title]

**Priority:** P1 / P2 / P3
**Status:** Open / In Progress / Fixed / Verified
**Assigned to:** 
**Found by:** [user email from survey]
**Sprint:** Sprint 1 / 2 / 3

### Description
[What goes wrong]

### Steps to Reproduce
1. 
2. 

### Expected Behavior


### Actual Behavior


### Fix Notes

```

---

# ═══════════ 🆕 รอบ 2 — Bug Report (พ.ค. 2569) ═══════════

> สกัดจากแบบประเมินรอบ 2 (n=6, 25–27 พ.ค. 2569)
> **ลักษณะบั๊กรอบ 2 ต่างจากรอบ 1:** รอบ 1 = บั๊กเชิงเทคนิคพื้นฐาน (timeout, 403, UI) / รอบ 2 = **บั๊กเชิงคุณภาพข้อมูลและความเสถียร**

## 🔴 รอบ 2 — P1 Critical

| ID | Bug | Source | Details |
|----|-----|--------|---------|
| **BUG-R2-01** | **ผลลัพธ์ไม่เสถียร (Non-deterministic)** | nugrataeee | "ใช้ Prompt เดียวกัน ในต่างช่วงเวลา ให้ผลลัพธ์ไม่ตรงกัน" — บั๊กร้ายแรงสุดของรอบ 2 |
| **BUG-R2-02** | **ข้อมูลไม่ตรงปีที่ขอ** | nugrataeee | "ขอข้อมูลปี 2568 แต่ได้ข้อมูลปี 2565–2567" |
| **BUG-R2-03** | **รายงานผลไม่ตรงกับคำสั่ง** | saengpakman | "การรายงานผล ยังไม่ตรงกับคำสั่ง" |
| **BUG-R2-04** | **ตัวแปรในการคำนวณคลาดเคลื่อน** | paithulkhamsombat | "ความถูกต้องของตัวแปรในการคำนวณ" |

## 🟡 รอบ 2 — P2 High

| ID | Bug | Source | Details |
|----|-----|--------|---------|
| **BUG-R2-05** | **Citation หายไป (เสี่ยง Regression)** | dr.weerapan.s | "ยังไม่พบการอ้างอิงแหล่งที่มาในรอบ 2" — รอบ 1 เคยมีแต่ลิงก์เสีย รอบ 2 ไม่เห็นเลย ต้องเช็คว่าฟีเจอร์หายหรือไม่ |
| **BUG-R2-06** | **เนื้อหาขึ้นกับคลังข้อมูล/คำเฉพาะ** | meltarchy | ความถูกต้องผันแปรตามไฟล์และคำเฉพาะในคลัง — ต้องมี controlled vocabulary |

## 🟢 รอบ 2 — P3 Medium (Data Quality Root Cause)

| ID | Issue | Source | Details |
|----|-------|--------|---------|
| **BUG-R2-07** | **ข้อมูลนำเข้าไม่สมบูรณ์/ไม่ทันสมัย** | thanasith1986 | "ข้อมูลที่ update เข้า AI อาจไม่สมบูรณ์/ไม่ทันสมัย ปัญหาอาจเกิดที่ผู้บันทึก" — root cause เชิง data governance |

---

## 🔗 บั๊กรอบ 2 ที่สืบเนื่องจากรอบ 1

| รอบ 1 | รอบ 2 | สถานะ |
|-------|-------|-------|
| BUG-004 ลิงก์ citation เสีย | BUG-R2-05 ไม่เห็น citation เลย | ⚠️ อาจ regress หนักขึ้น |
| BUG-003 ขอ A ได้ B (เบาหวาน→วัณโรค) | BUG-R2-01/02 ผลไม่นิ่ง + ผิดปี | 🔴 ปัญหา retrieval ยังอยู่ คนละอาการ |

---

*[[02 - Feedback Analysis/📊 Survey Results Summary | ← Survey Summary]]*
*[[01 - Sprint Plan/📅 Sprint Overview | → Sprint Plan]]*
*[[08 - Analysis/📊 MUSYA AI เปรียบเทียบผลประเมิน รอบ 1-2 | → รายงานเปรียบเทียบรอบ 1-2]]*
