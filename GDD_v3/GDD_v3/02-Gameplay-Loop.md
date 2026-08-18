---
tags: [gdd, gameplay-loop]
version: "3.0"
related:
  - "[[00-Index]]"
  - "[[01-Vision-Pillars]]"
---

# 🔄 Gameplay Loop

```
[1. บริหารภายใน — Micro]
   จัดผัง, มอบหมายงาน Tiny, คำนวณ Supply Chain
         ↓
[2. ขยายโครงข่าย — Macro]
   ส่งเกวียนผู้อพยพ, ตั้ง Enclave, สร้างท่าเรือ
         ↓
[3. การทูตและสงคราม — Tactical]
   ส่งสายลับ, สะสม Casus Belli, สั่งกองพัน Squad
         ↓
[4. ผลกระทบย้อนกลับ]
   ภัยพิบัติ, โรคระบาด, กบฏ, AI ประกาศสงคราม
         ↓
   กลับไป [1]
```

## พารามิเตอร์ Session
- **Session Length Target:** 1–2 ชั่วโมง/ครั้ง
- **Replay Value:** สูง — เผ่าพันธุ์ + แผนที่สุ่ม (ผู้เล่นกำหนดขนาดเองได้) ให้ประสบการณ์ต่างกันทุก Run

## การตั้งค่าก่อนเริ่มเกม (Player Configuration)
ผู้เล่นสามารถกำหนดเองได้ก่อนเริ่ม:
- ขนาดแผนที่ (เล็ก/กลาง/ใหญ่)
- จำนวนเมืองในแผนที่ (**สูงสุด 20 เมือง**)
- จำนวน Save Slot (3–5 slots)
- โหมด: **Scenario Mode** (แผนที่กำหนดไว้) vs **Free Play** (สุ่ม)

> หมายเหตุ: ยิ่งเมืองเยอะ ยิ่งกระทบ Performance ของ AI + Economic Simulation — ต้องมี Warning UI เตือนผู้เล่นถ้าเลือกจำนวนเมืองสูงเกินสเปกเครื่อง (ดู [[15-Risks-Scope-Reduction]])

## เชื่อมโยงกับระบบอื่น
- Micro → [[04-Population-System]], [[11-Building-Resource-Flow]]
- Macro → [[05-Economy-Design]]
- Tactical → [[07-Diplomacy]], [[08-Combat-Design]]
- ผลกระทบย้อนกลับ → [[09-Naval-Disease]], [[06-AI-Design]]
