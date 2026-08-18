---
tags: [gdd, races, balance]
version: "3.0"
related:
  - "[[00-Index]]"
---

# ⚖️ Race Design — ภาพรวมความสมดุล 4 เผ่า

เผ่าพันธุ์ทั้ง 4 เปิดตัวพร้อมกันตั้งแต่ v1.0 (ตัดสินใจแล้ว — ไม่ทยอยปล่อย เพื่อรักษาความสอดคล้องของการออกแบบ) อนาคตอาจเพิ่มเผ่าใหม่ผ่าน Patch/DLC

## หลักการ Balance ที่ใช้
- **Rule of 2+1:** ข้อดีหลัก 2 อย่าง + ข้อเสียบังคับ 1 อย่าง
- **Forbidden Action:** สิ่งที่ทำไม่ได้เด็ดขาด (Hard Block)
- **Unique Building:** อาคารที่เผ่าอื่นสร้างไม่ได้
- **Unique Units (x2):** หน่วยพิเศษ 2 ตัว/เผ่า (Mount Unit + Special Unit) — ทุกตัวต้องมี Combat Value จริง ไม่ใช่แค่ Support เฉย ๆ
- **Victory Bias:** เส้นทางชนะที่ถนัดกว่าเผ่าอื่น 30%
- **Resource Counter-Chain:** ทุกเผ่าต้องพึ่งพาเผ่าอื่นในบางจุด

---

## 🐴 Mount System (สรุปการตัดสินใจ)

| เผ่า | Mount | เหตุผล Lore | Gameplay Role |
|---|---|---|---|
| Human | 🐴 ม้า (Horse) | คลาสสิก, นักการทูต/ผู้ส่งสาร | Speed-focus, Scout/Messenger + Cavalry เบา |
| Elf | 🦌 กวางเขาใหญ่ (Great Stag) | ผูกกับป่า/ธรรมชาติ | Stealth + Mobility, Ambush Bonus ในป่า |
| Orc | 🐗 หมูป่า (Boar) | ดุดัน เข้ากับนักรบ | Charge + Morale Damage สูง |
| Dwarf | 🐐 แพะภูเขา (Mountain Goat) | อยู่ใต้ดิน/ภูเขา ไม่เลี้ยงม้า | เข้าถึง Terrain พิเศษ (หน้าผา/ภูเขา) ที่เผ่าอื่นเข้าไม่ได้ |

> เหตุผลที่ Dwarf ไม่ใช้หมูป่าซ้ำกับ Orc: เพื่อไม่ให้ Sprite/Function ซ้ำกัน และแพะภูเขาให้ Gameplay Function ที่ไม่มีเผ่าไหนมี (Terrain Access)

---

## Resource Counter-Chain
```
Human  ต้องการ Medicine    จาก Elf
Elf    ต้องการ Tools/Steel จาก Dwarf
Dwarf  ต้องการ ตลาดขาย    จาก Human
Orc    ปล้นได้ทุกคน แต่ถูกทุกคนเกลียด
→ ทุกเผ่าต้องติดต่อกัน ไม่มีใคร Self-Sufficient 100%
```

## Dominant Strategy Prevention
- **Environmental Pressure:** ภัยพิบัติแต่ละอย่างกดเผ่าที่แข็งที่สุดในแมป
- **Coalition AI:** เผ่าที่แข็งกว่าในแมปจะถูก AI อื่นรวมตัวกดดัน
- **Matchup Testing:** ทดสอบทีละ 6 คู่ (4C2) ไม่ใช่ทั้งหมดพร้อมกัน

---

## ลิงก์ไปแต่ละเผ่า
- [[03-Races/Human]]
- [[03-Races/Elf]]
- [[03-Races/Orc]]
- [[03-Races/Dwarf]]

ดูระบบชนะเกมที่ [[14-MVP-Roadmap-Versions]] (Victory Conditions ผูกกับแต่ละเผ่า)
