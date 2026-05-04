# 🐛 Bug Report — Derived from User Survey Feedback

> All bugs identified from the April 22, 2026 user survey responses.
> Priority: P1 = Must fix before demo | P2 = Fix in Sprint 2 | P3 = Backlog

---

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

*[[02 - Feedback Analysis/📊 Survey Results Summary | ← Survey Summary]]*
*[[01 - Sprint Plan/📅 Sprint Overview | → Sprint Plan]]*
