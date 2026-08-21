---
type: project
status: in-progress
tags:
  - game-development
  - project-kingdom
  - pixel-art
  - simulation
  - strategy
  - second-brain
created: 2026-08-19
last_updated: 2026-08-19
agent_in_charge: "[[Agent_Marshmallow]]"
playable_prototype: "Game/index.html"
---

# 👑 Project Kingdom — Master Dashboard & Development Hub

> **Game Concept:** เกมสร้างเมือง 2D Pixel Art ผสมผสานระบบเศรษฐกิจสมจริง (Physical Logistics), การทูต (Diplomacy), การวิจัย (Tech Tree) และสงครามชิงดินแดน (Conquest) ระหว่าง 4 มหาเผ่าพันธุ์
> **สถานะปัจจุบัน:** 🟢 **Master Prototype v1.2 (Transparent Character Sheet Sprites & Animated Mounts)**

---

## 🎮 วิธีเปิดเล่นเกม Prototype (Playable Demo)

1. **เปิดไฟล์ใน Browser:** [`Game/index.html`](file:///G:/ไดรฟ์ของฉัน/SecondBrain/Second%20Brain/04_PROJECTS/Kingdom/Game/index.html) หรือเล่นออนไลน์ผ่าน GitHub Pages
2. **การควบคุม (Controls):**
   - **คลิกซ้าย (Left Click):** เลือกเผ่า, เลือกอาคารเพื่อวาง, มอบหมายคนงาน (Worker Assignment)
   - **คลิกขวา (Right Click) / ESC:** ยกเลิกการสร้าง / ปิดหน้าต่าง
   - **ลากเมาส์ (Drag Mouse):** เลื่อนมุมมองแผนที่ (Pan Camera)
   - **หมุนลูกกลิ้งเมาส์ (Mouse Wheel Zoom) / ปุ่ม `+` `-` `1x`:** ซูมดูตัวละครพิกเซลอาร์ตแบบคมชัดระดับ 250%
   - **F1 / ปุ่ม Dashboard:** เปิดหน้ารายงานเศรษฐกิจและกราฟคลังหลวง (Treasury & Stockpile)
   - **ปุ่ม Diplomacy (การทูต):** เจรจากับ AI Faction ส่งของขวัญ (+ความสัมพันธ์), ทำสัญญาการค้า, หรือประกาศสงคราม
   - **ปุ่ม Tech Tree (วิจัย):** ปลดล็อกเทคโนโลยีการเกษตร, กำแพงหิน, การหลอมเหล็ก, กิลด์คนงาน, กองทัพประจำการ
   - **ปุ่ม Save (บันทึก):** เซฟความก้าวหน้าลง LocalStorage โหลดต่อได้ตลอดเวลา

---

## 🏰 ภาพรวม 4 มหาเผ่าพันธุ์ (The 4 Factions)

| เผ่าพันธุ์ | จุดเด่นหลัก | อาคารเฉพาะเผ่า (Wonder) | จุดอ่อน | เงื่อนไขชัยชนะ |
|---|---|---|---|---|
| **Human Kingdom** | ค้าขายเก่งที่สุด, รายได้ทองคำสูง | **Grand Embassy** (เพิ่มอิทธิพล & ค้าขาย) | ทหารราบพลังโจมตีน้อยกว่า | **Diplomatic Victory** |
| **Orc Warclan** | ผลิตทหารเร็ว 2x, พลังรบดุดัน | **War Totem** (ขวัญกำลังใจ +40%) | ค่าการทูตติดลบ สินค้าแพง | **Conquest Victory** |
| **Elven Conclave** | ฟื้นฟูป่าไม้, อาหารยั่งยืน | **Ancient Grove** (ผลิตอาหาร & สมุนไพรฟรี) | ประชากรเติบโตช้า | **Prosperity Victory** |
| **Dwarf Stronghold** | ขุดแร่หินและเหล็กเร็ว 3x | **Deep Forge** (แปรรูปแร่เหล็ก & อาวุธ) | อัตราเกิดต่ำ ต้องการเสบียงสูง | **Industrial Victory** |

---

## 🛠️ ระบบที่พัฒนาเสร็จสมบูรณ์แล้วใน Master Prototype v1.0

- [x] **Procedural World Generation:** แผนที่สุ่มทุ่งหญ้า, ป่าทึบ, แหล่งน้ำ, แนวเทือกเขาหิน
- [x] **Fog of War (หมอกแห่งสงคราม):** ระบบการมองเห็นแบบสำรวจรอบอาคารและยูนิต, หอคอยสังเกตการณ์ (Watchtower) ส่องสว่างไกลขึ้น
- [x] **Tiny Builders Simulation:** ประชากรเดินจริงตามถนนและพื้นที่, ระบบจัดสรรคนงาน (Worker Slot Assignment) เพื่อเพิ่มผลผลิต
- [x] **Dynamic Economy & Resource Ticks:** บริหาร Gold, Food, Wood, Stone, Iron พร้อมค่าบำรุงรักษา (Upkeep)
- [x] **Web Audio SFX Synthesizer:** เสียงคลิก, เสียงเหรียญทอง, เสียงวางอาคาร, เสียงแตรสงคราม, เสียงชัยชนะ (ไม่ต้องพึ่งไฟล์เสียงภายนอก)
- [x] **Interactive Diplomacy Modal:** เจรจาผู้นำ AI, อัตราความสัมพันธ์ (Relation 0-100), สนธิสัญญาพันธมิตรการค้า
- [x] **Tech Tree (Era I):** ปลดล็อก Advanced Agriculture, Masonry, Metallurgy, Logistics, Standing Army
- [x] **Mini-Map Overview:** แผนที่ย่อมุมขวาล่าง แสดงตำแหน่งสิ่งปลูกสร้าง, กองทัพ, และกรอบ Viewport (คลิกเพื่อกระโดดข้ามมุมมองได้)
- [x] **Real Asset Integration:** ดึงภาพ Character Sheets, Unique Buildings (Grand Embassy, War Totem, Ancient Grove, Deep Forge), Mounts จากโฟลเดอร์ Assets
- [x] **Seasons & Weather Visual FX:** หมุนเวียน 4 ฤดูกาล (ใบไม้ผลิ, ร้อน, ใบไม้ร่วง-ฝนตก, หนาว-หิมะตก)
- [x] **Save & Load Engine:** เซฟข้อมูลสถานะทั้งแผนที่, เทคโนโลยี, คลังทรัพยากรลง LocalStorage พร้อมระบบ Auto-save ทุกสิ้นปี

---

## 📚 โครงสร้างเอกสาร Game Design Document (GDD Links)

- 📜 GDD Index สารบัญหลัก
- 🏛 Vision & Core Pillars
- 🔄 Gameplay Loop
- ⚖ Race Balance Overview
- 👥 Population & Worker Logistics
- 💰 Economy & Supply-Demand
- 🤖 AI Behavior & Faction Strategy
- 🤝 Diplomacy & Treaties
- ⚔ Combat & Unit Tactics
- 🔬 Tech Tree Specification
- 🚀 MVP Roadmap & Version Plans
- 🖼 Asset Gallery คลังภาพของโปรเจกต์

---

## 🎯 Next Development Milestones (ก้าวต่อไปสู่ Unity v1.0)

1. **Unity Engine Porting:** นำโครงสร้าง Game Loop, Grid Logic, และ Data Architecture จาก Prototype นี้ไปขึ้นโครงสร้าง C# ใน Unity 2D Tilemap
2. **Extended Asset Slicing:** สับ Sprite Sheet จาก Character Sheets & Mount Sheets เพื่อทำ Sprite Animation (Walk, Attack, Idle)
3. **Audio BGM Track Integration:** เพิ่มเพลงประกอบแนว Medieval Fantasy สำหรับแต่ละฤดูกาล
4. **Naval & Water Trade (v2.0):** ระบบเรือประมงและเรือขนส่งสินค้าข้ามแม่น้ำ
