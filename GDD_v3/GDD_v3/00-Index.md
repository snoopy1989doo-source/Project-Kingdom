---
tags:
  - gdd
  - project-kingdom
  - index
  - project-management
version: "3.0"
status: active
last_updated: 2026-07-14
linked_project: 04_PROJECT
---

# 📜 Project Kingdom — Game Design Document v3.0

> เกมสร้างเมือง + บริหารเศรษฐกิจ + สงคราม + การทูต แบบ Pixel Art 2D
> Solo Dev Project — ไม่มีกำหนดเวลา, ทำเพื่อสมบูรณ์แบบ, อาจขายเชิงพาณิชย์ในอนาคต

---

## 🧭 สารบัญ (คลิกเพื่อไปยังแต่ละหมวด)

### รากฐานของเกม
- [[01-Vision-Pillars]] — วิสัยทัศน์, Core Pillars, แรงบันดาลใจ
- [[02-Gameplay-Loop]] — Loop หลักของเกม

### เผ่าพันธุ์
- 03-Races/Race-Balance-Overview — ภาพรวมความสมดุลระหว่าง 4 เผ่า
- 03-Races/Human
- 03-Races/Elf
- 03-Races/Orc
- 03-Races/Dwarf
- [[18-Asset-Gallery]] - ไฟล์รูปภาพ

### ระบบหลัก
- [[04-Population-System]] — ประชากร, Tiny Builders, ชีวิตจริง
- [[05-Economy-Design]] — เศรษฐกิจ, ตลาด, Supply-Demand
- [[06-AI-Design]] — AI แต่ละเมือง, บุคลิก, การค้า
- [[07-Diplomacy]] — การทูต, Casus Belli, สนธิสัญญา
- [[08-Combat-Design]] — สงคราม, Squad, Tactics
- [[09-Naval-Disease]] — ระบบเรือ + ระบบโรคระบาด
- [[10-Tech-Tree]] — ต้นไม้เทคโนโลยี 4 ยุค
- [[11-Building-Resource-Flow]] — ผังอาคาร + การไหลของทรัพยากร
- [[12-UI-Flow]] — หน้าจอ, Dashboard, การควบคุม

### โครงสร้างเทคนิค & แผนพัฒนา
- [[13-Save-Multiplayer-LiveService]] — ระบบเซฟ, Multiplayer, Live Service
- [[14-MVP-Roadmap-Versions]] — MVP, Roadmap, v1.0, v2.0
- [[15-Risks-Scope-Reduction]] — ความเสี่ยง + วิธีลด Scope
- [[16-Art-Asset-Prompts]] — คลังคำสั่งสร้างภาพ (Prompt) แยกหมวดหมู่
- [[17-Tech-Stack-Dev-Environment]] — Unity, Git, เครื่องมือ

---

## 🏷️ Quick Facts

| หัวข้อ | ค่าที่ตัดสินใจแล้ว |
|---|---|
| Engine | Unity (C#) |
| Platform เปิดตัว | PC (Keyboard + Mouse) |
| Art Pipeline | AI Generate (GPT/Gemini) + Krita ปรับแต่ง |
| Sound | ทำเอง — Medium-Premium Quality (~10 BGM, 50-70+ SFX) |
| Backup | GitHub |
| Localization เปิดตัว | ไทย + อังกฤษ → ตามด้วย สเปน/เกาหลี/ญี่ปุ่น/ฟิลิปปินส์ (Phased) |
| Funding | Self-Funded — ไม่ทำ Kickstarter |
| Multiplayer | เลื่อนไป v2.0 |
| Map/City Count | ผู้เล่นกำหนดเองได้ (สูงสุด 20 เมือง) |
| เผ่าพันธุ์เปิดตัว | ครบ 4 เผ่า (Human, Elf, Orc, Dwarf) |
| Victory Conditions | 4 แบบ (Conquest / Economic / Diplomatic / Prosperity) |
| AI Cities เริ่มต้น | 3 เมือง (ปรับได้) |
| Session Length | 1-2 ชั่วโมง/ครั้ง |
| Save Slots | 3-5 slots |

---

*เอกสารนี้เป็น Living Document — ปรับปรุงได้เรื่อย ๆ ตามการพัฒนา*
