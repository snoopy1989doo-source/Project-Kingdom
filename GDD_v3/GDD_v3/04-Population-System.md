---
tags: [gdd, population, tiny-builders]
version: "3.0"
related:
  - "[[00-Index]]"
  - "[[01-Vision-Pillars]]"
priority: core-pillar
---

# 👥 Population System — Hybrid 1,000/เมือง

> นี่คือหนึ่งใน 5 ระบบที่ต้อง "Perfect" ที่สุด — ตัดสินใจแล้วว่าทำแบบ **Full Physical Simulation** (ไม่ลด Scope) เพราะเป็นเกมในฝัน ไม่มีข้อจำกัดเวลา

```
ประชากรทั้งหมด <= 1,000 คน/เมือง
│
├── ทหาร & Builders (~150 คน) = Full Physical Simulation
│   → เดินจริงบน Grid, A* Pathfinding, แบกของจริง
│
├── คนงาน (~700 คน) = Hybrid Abstract
│   → Visual Representatives 5-10 ตัว/อาคาร
│   → ผลผลิตคำนวณจาก Quota + Skill Level
│
└── ผู้สูงอายุ/เด็ก/ป่วย (~150 คน) = Pure Statistical
    → ตัวเลขใน Dashboard เท่านั้น
    → กระทบ Happiness, Birth Rate, Tax Income
```

## Micro Proficiency System
- Tiny สะสม XP ตามงานที่ทำ: Tier 1 → 2 → 3
- Tier 3: ผลผลิต +50% แต่ถ้าเสียชีวิต = Economic Loss ทันที

## คุณสมบัติชีวิตของ Tiny (ตามที่ต้องการ)
- อาชีพ (Farmer, Builder, Soldier, Merchant, Commander, Blacksmith ฯลฯ)
- ความต้องการพื้นฐาน: หิว, ที่พัก, ความสุข
- ความเครียด / Happiness
- โรคภัย (เชื่อมกับ [[09-Naval-Disease]])
- ครอบครัว, อายุ, เกิด-แก่-ตาย
- ย้ายเมือง / ตกงาน
- การศึกษา / ทักษะ (Skill Tier)

## Performance Consideration
- Physical Sim จำกัดที่ ~150 ตัว/เมือง (ทหาร+builder) เพื่อรักษา Performance
- คนงานที่เหลือใช้ Visual Representative (ไม่ต้องคำนวณทุกตัว) — ประหยัด CPU/Memory มาก
- ถ้าผู้เล่นตั้งค่าแผนที่ใหญ่ + เมืองเยอะ (สูงสุด 20) ต้องมี Object Pooling + LOD (Level of Detail) สำหรับ Tiny ที่อยู่นอกจอ

## เชื่อมโยง
- Job assignment → [[11-Building-Resource-Flow]]
- Disease → [[09-Naval-Disease]]
- Happiness → กระทบ Victory Condition แบบ Prosperity ([[03-Races/Elf]])
