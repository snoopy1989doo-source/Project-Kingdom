---
tags: [gdd, mvp, roadmap, versions]
version: "3.0"
related:
  - "[[00-Index]]"
  - "[[15-Risks-Scope-Reduction]]"
---

# 🚀 MVP, Roadmap & Version Plan

> หมายเหตุสำคัญ: โปรเจกต์นี้**ไม่มีข้อจำกัดเวลา** เป็นเกมในฝัน (Self-Funded, No Kickstarter) ดังนั้น Timeline ด้านล่างเป็น**แนวทางประมาณการ** ไม่ใช่ Deadline บังคับ

## Victory Conditions (ตัดสินใจ: ครบ 4 แบบ)

| วิธีชนะ | คำอธิบาย | เผ่าที่ถนัด |
|---|---|---|
| **Conquest Victory** | ยึดควบคุมพื้นที่ >60% ของแผนที่ | Orc |
| **Economic Victory** | มีเงิน/ทรัพยากรมากที่สุดในเกม | Dwarf (Industrial) |
| **Diplomatic Victory** | มีพันธมิตรครบ 3 เผ่า + ควบคุมตลาดกลาง | Human |
| **Prosperity Victory** | Happiness > 80% นาน 10 ปีในเกม | Elf |

ทุกเผ่ามี Victory Bias (ถนัดกว่าเผ่าอื่น 30%) แต่ไม่ปิดกั้นไม่ให้เผ่าอื่นชนะด้วยวิธีอื่น — เพิ่ม Replayability

## Session & Map Configuration
- ผู้เล่นกำหนดขนาดแผนที่และจำนวนเมืองเองได้ (สูงสุด 20 เมือง)
- AI Cities เริ่มต้นแนะนำ: 3 เมือง (ปรับได้ตามขนาดแผนที่)
- Session Length เป้าหมาย: 1-2 ชั่วโมง/ครั้ง

---

## MVP Scope (Prototype/Testing Phase) — ✅ Completed (Master Prototype v1.0)
*ทดสอบระบบ Playable Prototype ในเบราว์เซอร์ได้ที่ `[[Game/index.html]]` หรือผ่าน `[[Project_Kingdom_Master_Hub]]`*

| ระบบ | MVP Scope | สถานะใน Master Prototype v1.0 |
|---|---|---|
| เผ่า | ครบ 4 เผ่า (Human, Orc, Elf, Dwarf) | ✅ ครบ 4 เผ่า พร้อม Wonder เฉพาะเผ่า + สไปรต์แท้ |
| แผนที่ | Grassland + Forest + Water + Mountains | ✅ สุ่มด้วย Perlin Noise Noise-grid |
| ทรัพยากร | Wood, Stone, Iron, Food, Gold | ✅ ครบ 5 ทรัพยากร + Upkeep + Live Graph |
| ประชากร | Physical Simulation แบบเต็ม | ✅ Tiny Builders เดินจริง + จัดสรร Worker Slots |
| สงคราม | Squad-Based บก + การปะทะ | ✅ ฝึกทหารจาก Barracks + ปะทะ AI + HP Bar |
| AI | AI City + Auto Expansion + War/Peace | ✅ AI สร้างเมือง ขยายฟาร์ม ฝึกทหาร และโจมตี |
| Tech Tree | Era I Tech Innovations | ✅ วิจัย 5 สาขา (เกษตร, กำแพง, โลหะ, โลจิสติกส์, กองทัพ) |
| Diplomacy | การทูต & สนธิสัญญา | ✅ มอบของขวัญ, ทำสัญญาการค้า, ประกาศสงคราม |
| UI & Audio | HUD + F1 Dashboard + Web Audio | ✅ F1 Dashboard + Web Audio SFX ในตัว |
| Save/Load | ระบบเซฟข้อมูล | ✅ LocalStorage Save & Auto-save ทุกสิ้นปี |

---

## Version 1.0 — Official Launch
- 4 เผ่าครบ พร้อม Asymmetric Balance Framework + Unique Units x2/เผ่า
- Hybrid Population 1,000 คน/เมือง (Full Physical Sim)
- Tile-Based Naval ครบ
- Disease Hybrid C ครบ 3 ระยะ
- Casus Belli ครบ 4 ประเภท + War Exhaustion + Reparations
- Tech Tree ครบ 4 Ages
- AI 4 บุคลิก
- PC UI ครบ F1–F5
- Localization: ไทย + อังกฤษ
- Multiplayer Foundation (Lockstep, เตรียมไว้)

## Version 2.0 — Major Update
- Steam Workshop + Level Editor (Mod Support เต็มรูปแบบ)
- Multiplayer 2–4 ผู้เล่น
- Geopolitical Megastructures
- Physics Naval System
- Localization เพิ่ม: สเปน, เกาหลี
- Mobile Port (UI Redesign)

## Patch ต่อจาก v2.0
- Localization เพิ่ม: ญี่ปุ่น, ฟิลิปปินส์/อาเซียน
- เผ่าพันธุ์ใหม่เพิ่มเติม

## Localization Rollout (Phased — ตัดสินใจแล้ว)
```
Launch (v1.0):     English + Thai
Patch 1.1:         Spanish + Korean
Patch 1.2:         Japanese + Vietnamese/ASEAN
Patch 1.3+:        เพิ่มตามความต้องการ
```

---

## Future DLC

**DLC 1 — Abyssal Waters**
- Physics Naval System (Wind, Broadside, Boarding)
- Volcanic Island Biome / Sea Monster Events

**DLC 2 — Steam & Clockwork Revolution**
- Crude Oil + Steam Engine
- Physical Railway Supply Chains
- Dwarf Steam-Ironclad

## Development Roadmap (แนวทางประมาณการ ไม่ใช่ Deadline)

| ช่วง | งาน |
|---|---|
| ระยะต้น | Core Foundation: Grid, Pathfinding, Tiny Movement, Save Architecture |
| ระยะกลาง 1 | Economy & Simulation: Resources, Workers, Market House, Buildings |
| ระยะกลาง 2 | Military & AI: Squad, Combat, Utility AI, Fog of War |
| ระยะปลาย | Crisis & UI Polish: Disease, Casus Belli, F1-F5 UI, Balancing, Sound |

## เชื่อมโยง
- ความเสี่ยงของ Timeline ที่ยาว → [[15-Risks-Scope-Reduction]]
