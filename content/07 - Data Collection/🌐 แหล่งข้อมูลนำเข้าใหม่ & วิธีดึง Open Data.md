# 🌐 แหล่งข้อมูลนำเข้าใหม่ & วิธีดึง Open Data — เขตสุขภาพที่ 10

> **ที่มา:** ข้อสรุปหลังเห็นการทำงานของระบบ — จะรวม "ข้อมูลนำเข้าชุดใหม่" โดยดึงจากแหล่งราชการ/Open Data ด้านล่าง และอาจขอให้จังหวัดช่วย **ถ่วงน้ำหนัก Priority Matrix** บางประเด็นอีกครั้ง
> **ใช้คู่กับ:** [[07 - Data Collection/📦 Data Collection Master Plan|Data Collection Master Plan]]
> **จัดทำ:** กรกฎาคม 2569

> [!info] วิธีอ่าน
> แต่ละหมวด = ข้อมูลนำเข้าที่ต้องการ → **แหล่ง** → **วิธีดึง** (🔓 Open API / 📥 ดาวน์โหลด / 🔑 ต้องขอสิทธิ์ / 📄 ขอข้อมูลราชการ / 🎤 เก็บเอง)

---

## 🔌 Open Data API หลักที่ใช้ซ้ำได้หลายหมวด

| ระบบ                            | Endpoint / ทางเข้า                                                                       | รูปแบบ                           | หมายเหตุ                                                                                                                     |
| ------------------------------- | ---------------------------------------------------------------------------------------- | -------------------------------- | ---------------------------------------------------------------------------------------------------------------------------- |
| **MoPH Open Data**              | `https://opendata.moph.go.th/api/report_data/{ServiceName}/{Year}`                       | 🔓 JSON                          | บริการข้อมูลป่วย/ตาย/KPI ย้อนหลัง ~10 ปี เลือกจังหวัดได้ — สมัคร key ที่ [opendata.moph.go.th](https://opendata.moph.go.th/) |
| **HDC Dashboard**               | [hdcservice.moph.go.th](https://hdcservice.moph.go.th/)                                  | 📥 Excel/CSV ราย KPI             | เลือกเขต 10 → จังหวัด → อำเภอ/ตำบล แล้ว export ต่อรายงาน · API ระดับจังหวัดขอผ่าน สสจ.                                       |
| **GD Catalog / data.go.th**     | [gdcatalog.go.th](https://gdcatalog.go.th/) · [data.go.th](https://data.go.th/)          | 🔓 CKAN API + CSV/XLSX           | บัญชีข้อมูลภาครัฐ ค้นตามกระทรวง — ใช้หา dataset ที่ไม่มี portal เฉพาะ                                                        |
| **กรมการปกครอง (ทะเบียนราษฎร)** | [stat.bora.dopa.go.th](https://stat.bora.dopa.go.th/stat/statnew/statMenu/newStat/stat/) | 📥 รายจังหวัด/อำเภอ/ตำบล/รายอายุ | ประชากรตั้งแต่ปี 2536 + [catalog.dopa.go.th](https://catalog.dopa.go.th/dataset/)                                            |
| **Air4Thai (คพ.)**              | `http://air4thai.pcd.go.th/services/getNewAQI_JSON.php`                                  | 🔓 JSON/XML รายชั่วโมง           | PM2.5 รายสถานี + dataset ย้อนหลังที่ [envilink.go.th](https://envilink.go.th/dataset/air-quality-pm2point5)                  |

---

## 📥 แมปข้อมูลนำเข้า 13 หมวด → แหล่ง → วิธีดึง

### 1. แผนปฏิบัติราชการเขตสุขภาพ (2565–2569)
| แหล่ง | วิธีดึง |
|-------|---------|
| [สำนักงานเขตสุขภาพที่ 10](https://healthregion10.moph.go.th/) | 📥 PDF จากเว็บเขต / 📄 ขอไฟล์ต้นฉบับ (docx) จากกลุ่มยุทธศาสตร์เขต |
| กองยุทธศาสตร์และแผนงาน สป.สธ. ([spd.moph.go.th](https://spd.moph.go.th/health-data/)) | 📥 แผนระดับกระทรวงประกอบ |

### 2. ภูมิศาสตร์ · วัฒนธรรม
| แหล่ง | วิธีดึง |
|-------|---------|
| [ข้อมูลทั่วไปเขตสุขภาพที่ 10](https://healthregion10.moph.go.th/%E0%B8%82%E0%B9%89%E0%B8%AD%E0%B8%A1%E0%B8%B9%E0%B8%A5%E0%B8%97%E0%B8%B1%E0%B9%88%E0%B8%A7%E0%B9%84%E0%B8%9B-%E0%B9%80%E0%B8%82%E0%B8%95%E0%B8%AA%E0%B8%B8%E0%B8%82%E0%B8%A0%E0%B8%B2%E0%B8%9E%E0%B8%97/) | 📥 พื้นที่ 36,276 ตร.กม. · 5 จังหวัด · ~4.6 ล้านคน |
| แผนพัฒนาจังหวัด (สนจ. แต่ละจังหวัด) + data.go.th | 📥 บริบทภูมิศาสตร์/วัฒนธรรม/ชายแดน |

### 3. หน่วยบริการ · ลักษณะการจัดบริการ
| แหล่ง | วิธีดึง |
|-------|---------|
| [GIS Health](https://gishealth.moph.go.th/) + [ระบบปฐมภูมิ](http://gishealth.moph.go.th/pcu/) | 🔓 พิกัด/ประเภทหน่วยบริการรัฐ-เอกชน (`gmap.php?code=<รหัส รพ.>`) |
| [รหัสหน่วยบริการ (hcode)](https://hcode.moph.go.th/) | 🔓 มาตรฐานรหัส 9 หลัก ใช้ join ทุกฐาน |
| [หน่วยบริการตาม Service Plan เขต 10 (สปสช.)](https://ubon.nhso.go.th/starter/region/hosp.php) | 📥 รายหน่วย + ระดับบริการ |

### 4. ประชากรตามกลุ่มวัย · กลุ่มเปราะบาง · ภาวะพึ่งพิง
| แหล่ง | วิธีดึง |
|-------|---------|
| [stat.bora.dopa.go.th](https://stat.bora.dopa.go.th/new_stat/webPage/statByAge.php) | 📥 ประชากรรายอายุ/ตำบล (ทางการ) |
| HDC กลุ่มรายงานผู้สูงอายุ/LTC (ADL, ติดบ้านติดเตียง) | 📥 Export ราย KPI · 🔑 API ผ่าน สสจ. |
| ฐาน LTC สปสช. + อปท. (ผู้มีภาวะพึ่งพิง) | 📄 ขอข้อมูลราชการ |

### 5. การป่วยโรคสำคัญ (OPD/IPD/ตาย) ตามกลุ่มวัย + ระบาด + ปัจจัยภายนอก (PM2.5 · ขยะ · สิ่งแวดล้อม)
| แหล่ง | วิธีดึง |
|-------|---------|
| **MoPH Open Data API** `report_data/{service}/{year}` | 🔓 ป่วย OPD/IPD + ตาย รายโรค/จังหวัด ~10 ปี |
| HDC (Service/ระบาด/NCD) | 📥 รายอำเภอ/ตำบล/กลุ่มวัย |
| กรมควบคุมโรค [opendata.ddc.moph.go.th](https://opendata.ddc.moph.go.th/) | 🔓 โรคระบาด/รายงาน 506 |
| **Air4Thai** `getNewAQI_JSON.php` + [Envilink](https://envilink.go.th/dataset/air-quality-pm2point5) | 🔓 PM2.5 รายชั่วโมง/ย้อนหลัง |
| ขยะ/สิ่งแวดล้อม: คพ. + สถจ. (data.go.th) | 📥 ปริมาณขยะรายจังหวัด |

### 6. กำลังคน · อัตรากำลัง 7 วิชาชีพ
| แหล่ง | วิธีดึง |
|-------|---------|
| **HROPS** [hrops.moph.go.th](https://hrops.moph.go.th/) | 🔑 ต้องสมัคร/ขอสิทธิ์ (ผ่าน สสจ./เขต) — แพทย์ ทันตแพทย์ เภสัชกร พยาบาล เทคนิคการแพทย์ กายภาพ นักวิชาการ สธ. |
| [รายงานบุคลากรประจำปี (กยผ.)](https://spd.moph.go.th/) | 📥 PDF รายปี (2568 มีแล้ว) |
| [GD Catalog — บุคลากรสาธารณสุข](https://gdcatalog.go.th/dataset/gdpublish-dataset-5-01-08) | 🔓 dataset รวม |

### 7. แผนการจัดบริการ Service Plan · เตียง · วันนอน · CMI
| แหล่ง | วิธีดึง |
|-------|---------|
| **ระบบรายงาน Service Plan / CMI** [cmi.moph.go.th](https://cmi.moph.go.th/isp/sp_main/index) | 🔑 CMI/RW/วันนอน ราย รพ. (สิทธิ์ผ่าน สสจ./รพ.) |
| [กองบริหารการสาธารณสุข (phdb)](https://phdb.moph.go.th/main/index/downloadlist/57/0) | 📥 หน่วยบริการตาม Service Plan + จำนวนเตียง |
| สปสช. เขต 10 [ubon.nhso.go.th](https://ubon.nhso.go.th/starter/region/hosp.php) | 📥 Service Base รายเขต |

### 8. กฎหมาย · การเบิกจ่าย · กองทุน
| แหล่ง | วิธีดึง |
|-------|---------|
| [NHSO Budget Report](https://ucapps1.nhso.go.th/budgetreport/) | 🔓 การโอนเงินกองทุนราย รพ. (เปิดตั้งแต่ปีงบ 66) |
| คู่มือบริหารกองทุน สปสช. ([e-library.nhso.go.th](https://e-library.nhso.go.th/)) | 📥 ระเบียบเบิกจ่ายรายปี |
| NHSO Standard Data Set (13 แฟ้ม, เริ่มปีงบ 2567) | 📄 โครงสร้างข้อมูลเบิกจ่ายมาตรฐาน |
| กฎหมาย สธ.: ราชกิจจานุเบกษา + krisdika.go.th | 📥 PDF |

### 9. การลงทุน · งบลงทุน · ค่าเสื่อม
| แหล่ง | วิธีดึง |
|-------|---------|
| งบค่าเสื่อม สปสช. ([budgetreport](https://ucapps1.nhso.go.th/budgetreport/)) | 🔓 รายการโอนราย รพ./ปี |
| คำของบลงทุน สป.สธ. (กองแผน/เขต) | 📄 ขอไฟล์จากกลุ่มยุทธศาสตร์เขต 10 |
| ภาษีไปไหน? govspending (data.go.th) | 🔓 API โครงการจัดซื้อจัดจ้างรายจังหวัด |

### 10. Template กระทรวงสาธารณสุข 5 ปีย้อนหลัง
| แหล่ง | วิธีดึง |
|-------|---------|
| [กองตรวจราชการ — แนวทาง/แบบฟอร์ม](https://inspection.moph.go.th/e-inspection/) | 📥 แบบฟอร์มตรวจราชการ + KPI template รายปี (69 มี [kpi_14.pdf](https://inspection.moph.go.th/uploads/kpi_files/kpi_14.pdf)) |
| กยผ. สป.สธ. ([spd.moph.go.th](https://spd.moph.go.th/)) | 📥 แผน/template ยุทธศาสตร์รายปี ไล่ย้อน 2565–2569 |

### 11. สัมภาษณ์เชิงลึก — Descriptive 7S + PESTEL (Add-on: Health ID · Telemed · AI Usage ใน รพ.)
| แหล่ง | วิธีดึง |
|-------|---------|
| ผู้บริหาร/ผู้ปฏิบัติ 5 จังหวัด | 🎤 **เก็บเอง** — แบบสัมภาษณ์กึ่งโครงสร้าง 7S + PESTEL |
| Add-on ดิจิทัล: Health ID ([สุขภาพดิจิทัล สป.](https://ddigital.spo.moph.go.th/)) + สถิติ Telemed/AI ราย รพ. | 📄 ขอสถิติการใช้จากเขต/รพ. ประกอบการสัมภาษณ์ |

### 12. นโยบาย New Service · One Region ฯลฯ
| แหล่ง | วิธีดึง |
|-------|---------|
| [เขตสุขภาพที่ 10](https://healthregion10.moph.go.th/) + มติผู้บริหารเขต | 📄 เอกสารนโยบาย/มติประชุม (ขอจากสำนักงานเขต) |
| นโยบายกระทรวง (moph.go.th) | 📥 ประกาศ/แถลง |

### 13. ข้อมูลการตรวจราชการ 5 ปีย้อนหลัง (2565–2569)
| แหล่ง | วิธีดึง |
|-------|---------|
| **e-Inspection** [inspection.moph.go.th/e-inspection](https://inspection.moph.go.th/e-inspection/) | 📥 รายงานผลตรวจราชการรายจังหวัด/รอบ (PDF) — ไล่รายปี 65→69 เขต 10 |
| สรุปตรวจราชการระดับเขต | 📄 ขอไฟล์รวมจากกลุ่มตรวจราชการเขต 10 |

---

## ⚖️ Priority Matrix — ขั้นถ่วงน้ำหนักโดยจังหวัด

> [!important] ข้อเสนอกระบวนการ
> 1. ทีมสรุป **ประเด็น/ตัวชี้วัดตั้งต้น** จากข้อมูล 13 หมวดข้างต้น
> 2. ส่งให้ **สสจ. 5 จังหวัด** ถ่วงน้ำหนักผ่านแบบฟอร์ม (เกณฑ์แนะนำ: ขนาดปัญหา · ความรุนแรง · ความเป็นไปได้ · ความสอดคล้องนโยบาย)
> 3. รวมเป็น **Priority Matrix รายจังหวัด + ภาพเขต** แล้วส่งอาจารย์ยืนยันอีกครั้ง
> 4. ผล priority ใช้กำหนดลำดับ ingest ข้อมูลเข้า RAG และหัวข้อรายงานของระบบ

---

## ✅ ข้อแนะนำการนำเข้า (ต่อจาก Collection Rules เดิม)

> [!tip]
> - แหล่ง 🔓 API (MoPH Open Data, Air4Thai, NHSO Budget, govspending) → เขียน **connector ดึงอัตโนมัติ + tag ปีข้อมูล** สอดรับ Epic E2 (year-accurate + citation)
> - แหล่ง 🔑 (HROPS, CMI) → ขอสิทธิ์ผ่านเขต/สสจ. ตั้งแต่ต้นโครงการ (lead time นาน)
> - แหล่ง 📄 ขอราชการ → ทำหนังสือขอครั้งเดียวรวมทุกรายการต่อจังหวัด
> - ตั้งชื่อไฟล์ตามกติกาเดิม: `[province]_[domain]_[source]_[YYYYMM]`

---

*[[07 - Data Collection/📦 Data Collection Master Plan | ← Data Collection Master Plan]]*
*[[08 - Analysis/📊 การวิเคราะห์ Gap ต่อแบบฟอร์มประเมิน 10 ชุด | → Gap Analysis]]*
*[[04 - Feature Backlog/🛠️ Consolidated Backlog — Root Fixes (เฟส 2) | → Consolidated Backlog]]*
