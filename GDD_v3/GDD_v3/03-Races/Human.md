---
tags:
  - gdd
  - race
  - human
version: "3.0"
related:
  - "03-Races/Race-Balance-Overview"
---

# 👤 Human — นักการทูต

| | รายละเอียด |
|---|---|
| **ข้อดี #1** | ราคาค้าขายดีกว่า +25% ในตลาดกลาง |
| **ข้อดี #2** | สร้างพันธมิตรได้ง่ายกว่า — ต้นทุน Influence -30% |
| **ข้อเสีย** | ทหารอ่อนแอที่สุด (ATK -20%, HP -15%) |
| **Forbidden** | ไม่สามารถเกณฑ์หน่วย Berserker ได้เลย |
| **Unique Building** | Grand Embassy — Influence Points 2x, Diplomatic Options พิเศษ |
| **Victory Bias** | Diplomatic Victory — พันธมิตรครบ 3 เผ่า + ควบคุมตลาดกลาง |
| **วิธีคิด** | ชนะด้วยเครือข่าย ไม่ใช่กำลัง |

## Roles ทั้งหมด (Character Sprite Sheet)
1. Farmer
2. Builder / Worker
3. Soldier / Guard
4. **Crossbowman** (หน่วยยิงไกล — เพิ่มใหม่ v3.0)
5. Merchant
6. Commander / General
7. Blacksmith

> เดิม Human Sheet ขาด Role ที่ 4 เมื่อเทียบกับเผ่าอื่น (Elf มี Archer, Orc มี Raider, Dwarf มี Berserker) — ตัดสินใจเพิ่ม **Crossbowman** เพื่อให้ Human มีหน่วยยิงไกล ตรงกับธีม "นักการทูต" ที่ไม่เน้น Melee

## Mount Unit
🐴 **ม้า (Horse)** — Speed-focus, ใช้เป็น Scout/Messenger และ Cavalry เบา

## Unique Units (Exclusive, x2 — Combat Value จริง)

| Unit | Role | Combat Value |
|---|---|---|
| **Envoy Guard** | คุ้มกันคาราวาน/ทูต | ATK ปานกลาง + Aura ลดโอกาส Casus Belli จากศัตรูรอบข้าง 10% |
| **Crossbowman** | หน่วยยิงไกลหลัก | DMG สูง ระยะไกล, ช้าเวลาบรรจุกระสุน |

## เหตุผลเชิงออกแบบ
Human เป็นเผ่าที่ชนะด้วย "เครือข่ายพันธมิตร" ไม่ใช่กำลังทหาร ดังนั้นหน่วยพิเศษทั้งสองเน้น **สนับสนุนการทูต** (Envoy Guard ลด Casus Belli) และ **ป้องกันระยะไกล** (Crossbowman) แทนการรุกด้วยกำลังดิบ — ตรงกับ Victory Bias แบบ Diplomatic

!Human_Character_Sheet.png

!Human_Mount_Horse.png

!Human_Building_GrandEmbassy.png
