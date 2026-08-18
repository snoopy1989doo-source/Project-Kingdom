---
tags: [gdd, combat, squad, tactics]
version: "3.0"
related:
  - "[[00-Index]]"
  - "[[03-Races/Race-Balance-Overview]]"
---

# ⚔️ Combat Design

> ตัดสินใจใช้ **Full Tactical Combat (Option A)** — ไม่ลด Scope เพราะเป็นเกมในฝัน มีเวลาไม่จำกัด

## Squad System
- ทหาร 12-16 นาย/Squad ควบคุมผ่าน Commander
- Pathfinding คำนวณเฉพาะ Commander
- ทหารที่เหลือใช้ Local Steering Behaviors

## Army Scale
```
1 เมือง  = ~10 Squad  → ปะทะชายแดน
3 เมือง  = ~30 Squad  → สงครามจริงจัง
5+ เมือง = ~50 Squad  → สงครามมหาภาพ
```

## Tactical Formations
| Formation | ผล | ใช้เมื่อ |
|---|---|---|
| Shield Wall | DEF +50%, SPD -30% | รับการโจมตีหน้า |
| Wedge | ATK +40%, ทำลาย Morale ศัตรู | เจาะแนวรบ |
| Square | ป้องกัน Commander, Morale +30% | ป้องกัน Flanking |

## Morale System
- Morale ดี → สู้นาน, Retreat ช้า
- Morale แตก → Desertion เพิ่ม
- Commander ตาย → Morale ตก -50 ทันที

## หน่วยพิเศษแต่ละเผ่าที่กระทบการรบ
ทุกเผ่ามี Mount Unit + Unique Unit ที่มี Combat Value จริง — ดูรายละเอียดที่หน้าเผ่าแต่ละอัน:
- [[03-Races/Human]] — Envoy Guard, Crossbowman
- [[03-Races/Elf]] — Stag Rider, Grove Archer
- [[03-Races/Orc]] — Boar Rider, Warchief
- [[03-Races/Dwarf]] — Goat Rider, Siege Engineer

## เชื่อมโยง
- ทหารม้าใช้ Mount System ที่ตกลงกันไว้ที่ [[03-Races/Race-Balance-Overview]]
- Casus Belli นำไปสู่สงคราม → [[07-Diplomacy]]
- Naval Combat แยกออกไปที่ [[09-Naval-Disease]]
