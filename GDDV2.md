# 📜 Game Design Document — Project Kingdom (Working Title)
**เวอร์ชัน:** 2.0 (Final Approved)  
**วันที่:** 2026-07-08  
**แพลตฟอร์มหลัก:** PC (Keyboard & Mouse) → Android (อนาคต)  
**Engine:** Unity (Personal License)  
**ทีม:** Commander (Human) + Antigravity (Dev AI) + Gemini/GPT/Claude (Design AI)

---

## 1. Core Experience Pillars

### Pillar 1 — The Sovereign's Desk
ผู้เล่นคือประมุขที่สั่งการผ่าน Modular Dashboard บน PC  
ข้อมูลคืออาวุธที่ทรงพลังที่สุด — ผู้ที่อ่านกราฟเศรษฐกิจออกเร็วกว่าคือผู้ชนะ

### Pillar 2 — Physical Consequences
ทุกคำสั่งมีต้นทุนกายภาพ Tiny Builders เดินจริงบน Grid ถนน  
คอขวดเกิดจากถนนที่แออัด ไม่ใช่ตัวเลขในสูตร

### Pillar 3 — Geopolitical Friction
อาณาจักรอื่นมีสมองกล มีเป้าหมาย มีเศรษฐกิจของตัวเอง  
โลกเคลื่อนไหวแม้ผู้เล่นไม่ทำอะไร

---

## 2. Gameplay Loop

```
[1. บริหารภายใน - Micro]
   จัดผัง, มอบหมายงาน Tiny, คำนวณ Supply Chain
         ↓
[2. ขยายโครงข่าย - Macro]
   ส่งเกวียนผู้อพยพ, ตั้ง Enclave, สร้างท่าเรือ
         ↓
[3. การทูตและสงคราม - Tactical]
   ส่งสายลับ, สะสม Casus Belli, สั่งกองพัน Squad
         ↓
[4. ผลกระทบย้อนกลับ]
   ภัยพิบัติ, โรคระบาด, กบฏ, AI ประกาศสงคราม
         ↓
   กลับไป [1]
```

**Session Length Target:** 45 นาที – 3 ชั่วโมง/ครั้ง  
**Replay Value:** สูงมาก — แต่ละเผ่าพันธุ์และแผนที่สุ่มให้ประสบการณ์ต่างกันทุก Run

---

## 3. Race Design — Asymmetric 4 Factions

### หลักการ Balance ที่ใช้
- **Rule of 2+1:** ข้อดีหลัก 2 อย่าง + ข้อเสียบังคับ 1 อย่าง
- **Forbidden Action:** สิ่งที่ทำไม่ได้เด็ดขาด (Hard Block)
- **Unique Building:** อาคารที่เผ่าอื่นสร้างไม่ได้
- **Victory Bias:** เส้นทางชนะที่ถนัดกว่าเผ่าอื่น 30%
- **Resource Counter-Chain:** ทุกเผ่าต้องพึ่งพาเผ่าอื่นในบางจุด

---

### Human — นักการทูต
| | รายละเอียด |
|---|---|
| **ข้อดี #1** | ราคาค้าขายดีกว่า +25% ในตลาดกลาง |
| **ข้อดี #2** | สร้างพันธมิตรได้ง่ายกว่า — ต้นทุน Influence -30% |
| **ข้อเสีย** | ทหารอ่อนแอที่สุด (ATK -20%, HP -15%) |
| **Forbidden** | ไม่สามารถเกณฑ์หน่วย Berserker ได้เลย |
| **Unique Building** | Grand Embassy — Influence Points 2x, Diplomatic Options พิเศษ |
| **Victory Bias** | Diplomatic Victory — พันธมิตรครบ 3 เผ่า + ควบคุมตลาดกลาง |
| **วิธีคิด** | ชนะด้วยเครือข่าย ไม่ใช่กำลัง |

---

### Orc — นักรบ
| | รายละเอียด |
|---|---|
| **ข้อดี #1** | ผลิตทหารเร็วกว่า 2x, Barracks Upkeep -20% |
| **ข้อดี #2** | Morale ทหารสูงมาก — War Totem แผ่ Morale +40% |
| **ข้อเสีย** | Reputation ติดลบกับทุกเผ่าตั้งแต่ต้น |
| **Forbidden** | ไม่สามารถลงนามสนธิสัญญาการค้าระยะยาว (> 1 ปีในเกม) |
| **Unique Building** | War Totem — Morale +40% รัศมี 5 Tile แต่กินอาหาร 2x |
| **Victory Bias** | Conquest Victory — ยึดครองดินแดน >60% ของแผนที่ |
| **วิธีคิด** | ชนะด้วยความเร็วและความกลัว |

---

### Elf — นักอนุรักษ์
| | รายละเอียด |
|---|---|
| **ข้อดี #1** | ป่าฟื้นตัวเองได้ ไม่มีวันหมดถ้าตัดแบบ Sustainable |
| **ข้อดี #2** | Medicine + Rare Herb จาก Ancient Grove ฟรีทุกฤดู |
| **ข้อเสีย** | ขยายเมืองช้า — ต้องรักษา Forest Coverage >40% |
| **Forbidden** | ไม่สามารถสร้าง Deep Mine ได้เลย |
| **Unique Building** | Ancient Grove — Medicine + Rare Herb ฟรี, ป่าฟื้น 2x |
| **Victory Bias** | Prosperity Victory — Happiness >80% นาน 10 ปีในเกม |
| **วิธีคิด** | ชนะด้วยความยั่งยืน ไม่ใช่ความเร็ว |

---

### Dwarf — นักอุตสาหกรรม
| | รายละเอียด |
|---|---|
| **ข้อดี #1** | ขุดแร่เร็วกว่า 3x, Deep Mine Tier 3 ปลดล็อกได้เร็ว |
| **ข้อดี #2** | Deep Forge = เดียวที่แปลง Iron → Steel ได้ (Monopoly) |
| **ข้อเสีย** | ประชากรเพิ่มช้าที่สุด Birth Rate -40% |
| **Forbidden** | ไม่สามารถสร้าง Enclave ในพื้นที่ป่าได้ |
| **Unique Building** | Deep Forge — แปลง Iron → Steel, เผ่าอื่นต้องซื้อ Steel จาก Dwarf |
| **Victory Bias** | Industrial Victory — Tier 3 Resource ครบทุกประเภท + Megastructure |
| **วิธีคิด** | ชนะด้วยเทคโนโลยีและการผูกขาด |

---

### Resource Counter-Chain
```
Human  ต้องการ Medicine    จาก Elf
Elf    ต้องการ Tools/Steel จาก Dwarf
Dwarf  ต้องการ ตลาดขาย    จาก Human
Orc    ปล้นได้ทุกคน แต่ถูกทุกคนเกลียด
→ ทุกเผ่าต้องติดต่อกัน ไม่มีใคร Self-Sufficient 100%
```

### Dominant Strategy Prevention
- **Environmental Pressure:** ภัยพิบัติแต่ละอย่างกดเผ่าที่แข็งที่สุดในแมป
- **Coalition AI:** เผ่าที่แข็งกว่าในแมปจะถูก AI อื่นรวมตัวกดดัน
- **Matchup Testing:** ทดสอบทีละ 6 คู่ (4C2) ไม่ใช่ทั้งหมดพร้อมกัน

---

## 4. Population System — Hybrid 1,000/เมือง

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

### Micro Proficiency System
- Tiny สะสม XP ตามงานที่ทำ: Tier 1 → 2 → 3
- Tier 3: ผลผลิต +50% แต่ถ้าเสียชีวิต = Economic Loss ทันที

---

## 5. Economy Design

### Multi-Tier Resource Chain
```
Tier 1 (Raw):     Wood, Stone, Iron Ore, Gold Ore, Water
Tier 2 (Processed): Firewood, Charcoal, Iron Ingot, Flour, Cloth
Tier 3 (Advanced):  Steel*, Bread, Tools, Weapons, Armor, Medicine, Horses
(* Steel ผลิตได้เฉพาะ Dwarf Deep Forge เท่านั้น)
```

### Dynamic Price System
- ตลาดคำนวณราคาทุก "วัน" ในเกม ตาม Supply-Demand
- Supply มาก → ราคาตก | Supply ขาด → ราคาพุ่ง

### Money Sink (แก้ปัญหา Late Game Gold Glut)
| Money Sink | รายละเอียด |
|---|---|
| Building Upkeep | ค่าบำรุงรักษาอาคารรายปี (หลักสำคัญที่สุด) |
| Skilled Worker Wages | Tiny Tier 3 เรียกเงินเดือนสูงขึ้น |
| Tribute | ค่าบรรณาการให้พันธมิตรตามสนธิสัญญา |
| Disaster Relief | Random Event บังคับจ่ายเงินฉุกเฉิน |
| Military Upkeep | ทหารทุกหน่วยมีค่า Wage รายสัปดาห์ |

---

## 6. AI Design — Hybrid Architecture

### High-Level Strategy (Utility AI) — ทุก 5 วินาทีเกม
```
U_food      = 1 - (Current / Target)
U_military  = f(ศัตรูรอบข้าง, กำลังตัวเอง)
U_economy   = f(คลัง, Trade Routes)
U_expansion = f(พื้นที่ว่าง, ประชากร)
```

### Low-Level Execution (Behavior Trees) — รายวินาที
- สั่ง Builder สร้างตึกตาม Build Order
- สั่งเกวียนสินค้าเดินตาม Route
- ควบคุม Squad ในการรบ

### AI Personality (สุ่มต่อ Session)
- **Aggressive:** สร้างทหารก่อน, Hostility Weight สูง
- **Merchant:** ค้าขายก่อน, ประกาศสงครามยาก
- **Expansionist:** ส่ง Enclave เร็ว, Defend น้อย
- **Isolationist:** ปิดพรมแดน, แข็งแกร่งแต่ไม่โต

---

## 7. Diplomacy Design — Casus Belli System

### Casus Belli Triggers
| ประเภท | เงื่อนไข |
|---|---|
| Supply Raid Claim | ตรวจพบหน่วยศัตรูโจมตีเกวียนสินค้า |
| Espionage Exposure | จับสายลับศัตรูได้ในเมือง |
| Trade Default | ศัตรูขึ้นภาษีเกินกว่าสัญญา |
| Enclave Annexation | ศัตรูยึด Enclave โดยไม่ประกาศสงคราม |

### Casus Belli Rules (ป้องกัน War Spam)
- **Expiry:** หมดอายุใน 5 ปีในเกมถ้าไม่ใช้
- **War Exhaustion:** หลังสงคราม ต้องรอ 2 ปีในเกม
- **Reparations Treaty:** ชดเชยเพื่อล้าง Casus Belli
- **Garrison Requirement:** ต้องมีทหาร >20 นายใน Enclave ก่อน Raid Claim จะใช้ได้

---

## 8. Combat Design

### Squad System
- ทหาร 12-16 นาย/Squad ควบคุมผ่าน Commander
- Pathfinding คำนวณเฉพาะ Commander
- ทหารที่เหลือใช้ Local Steering Behaviors

### Army Scale
```
1 เมือง  = ~10 Squad  → ปะทะชายแดน
3 เมือง  = ~30 Squad  → สงครามจริงจัง
5+ เมือง = ~50 Squad  → สงครามมหาภาพ
```

### Tactical Formations
| Formation | ผล | ใช้เมื่อ |
|---|---|---|
| Shield Wall | DEF +50%, SPD -30% | รับการโจมตีหน้า |
| Wedge | ATK +40%, ทำลาย Morale ศัตรู | เจาะแนวรบ |
| Square | ป้องกัน Commander, Morale +30% | ป้องกัน Flanking |

### Morale System
- Morale ดี → สู้นาน, Retreat ช้า
- Morale แตก → Desertion เพิ่ม
- Commander ตาย → Morale ตก -50 ทันที

---

## 9. Naval System — Tile-Based V1.0

### หลักการ
- เรือเคลื่อนที่เป็น Grid บน Water Tile
- Deterministic โดยธรรมชาติ — รองรับ Multiplayer Lockstep
- ไม่มี Physics Engine

### Naval Actions
| Action | วิธีทำงาน |
|---|---|
| Naval Blockade | วางเรือ Tile หน้าท่าเรือ → ปิด Trade Route |
| Boarding | เรือชิด → ทหาร Deck เข้า Melee บน Grid |
| Transport | รับทหารจาก Dock → ย้ายข้ามทะเล |
| Patrol | กำหนด Patrol Route บน Water Tile |

**Physics Naval → ย้ายไป DLC 1 หรือ V2.0**

---

## 10. Disease System — Hybrid C

### 3 ระยะ

**ระยะ 1 — WARNING (สีเหลือง)**
- Dashboard: Sanitation 23% ใน District X
- ผู้เล่นกด "Build Sanitation Well" หรือ "Assign Doctor"
- ง่าย ไม่กดดัน

**ระยะ 2 — OUTBREAK (สีส้ม)**
- โรคลามข้าม District หลายเขต
- ผู้เล่นสั่ง Zone Lockdown (กดปุ่มเดียว)

**ระยะ 3 — CRISIS (สีแดง — เกิดนานๆ ครั้ง)**
- Spawn Patient Zero ตัวจริงบน Grid
- ผู้เล่นสั่ง Guard ไปจับ + ปิด Quarantine Gate
- ตื่นเต้น Memorable แต่ไม่ยากเพราะมีแค่ 1 ตัว

---

## 11. Tech Tree — 4 Ages Asymmetric

```
Age 1: Colonial Age
  Human  → Free Trade License, Merchant Guild
  Orc    → Hunter Camp, Raid Wagon
  Elf    → Sacred Forest Harvest, Herbalist Hut
  Dwarf  → Shallow Tunnel Drill, Basic Forge

Age 2: Strategic Age
  All    → Stone Road, Watchtower, Quarantine Gate
  Human  → Diplomat Corps, Trade Fleet (Tile)
  Orc    → Heavy Armor, Siege Equipment
  Elf    → Ancient Grove Unlock, Forest Road
  Dwarf  → Iron Ingot Production, Logistics Depot

Age 3: Tribunal Age
  All    → Royal Prison, Signal Beacon, Drydock
  Human  → Grand Embassy Unlock, Alliance Treaty
  Orc    → War Totem Unlock, Berserker Squad
  Elf    → Elder Council, Peace Treaty Bonus
  Dwarf  → Deep Mine, Advanced Tools

Age 4: Industrial & Overlord Age
  All    → Iron-Plated Highway, Full Logistics Overlay
  Human  → Megapolis Trade Hub
  Orc    → Fortress Citadel, Siege Engine Fleet
  Elf    → World Tree (Megastructure)
  Dwarf  → Deep Forge Unlock, Steam Ironclad (DLC Preview)
```

### Catch-Up Mechanics
1. **Tech Espionage:** สายลับขโมยเทคโนโลยีศัตรูได้
2. **Crisis Bonus:** ยิ่งอ่อนแอ ยิ่งได้ Research Speed +15%

---

## 12. Building Tree

### Civil & Palace
| อาคาร | ฟังก์ชัน |
|---|---|
| Housing | แหล่งกำเนิดแรงงาน |
| Royal Palace | ศูนย์บริหาร, ผลิต Influence Points |
| Royal Prison | ควบคุมโจร → แรงงาน (มี Oppression Meter) |

### Production & Logistics
| อาคาร | Input → Output |
|---|---|
| Lumber Mill | Wood → Firewood/Planks |
| Quarry | Stone → Cut Stone |
| Mine | Iron Ore → Iron Ore Stack |
| Deep Mine (Dwarf) | → Gold Ore, Rare Minerals |
| Smelter | Iron Ore + Charcoal → Iron Ingot |
| Deep Forge (Dwarf) | Iron Ingot + Charcoal → Steel |
| Windmill | Wheat → Flour |
| Bakery | Flour + Water → Bread |
| Blacksmith | Iron Ingot + Wood → Tools |
| Weaponsmith | Steel/Iron → Weapons/Armor |
| Stable | Hay + Water → Horses |
| Herbalist | Plants → Medicine |

### Roads
```
Dirt Path → Stone Road → Iron-Plated Highway
Speed:  1x → 1.5x → 2.5x
```

### Military & Security
| อาคาร | ฟังก์ชัน |
|---|---|
| Barracks | ฝึก Squad |
| Arsenal | เก็บ Weapons/Armor |
| Watchtower | แผ่ Visibility |
| Signal Beacon | แจ้งเตือน Alert ทั่วแผนที่ |
| Quarantine Gate | ปิดถนน Node ป้องกันโรค |
| Maritime Dock | สร้างเรือ Tile-Based |

---

## 13. Resource Flow

```
[Extraction: Mine / Farm / Forest / Fishing]
         ↓ (Tiny Builders เดินแบกจริง)
[Logistics Depot]
         ↓ (เกวียนขนส่ง)
[Processing: Smelter / Bakery / Weaponsmith]
         ↓
    ┌────┴────┐
[Military]  [Commerce]
 เกณฑ์ทหาร  ส่งออกตลาด → Gold → Treasury
                               ↓
                         [Money Sinks]
                    Upkeep / Wages / Events
```

---

## 14. UI Flow — PC-Only (Keyboard & Mouse)

### HUD (Always Visible)
```
มุมบนซ้าย: Gold | Food | Population | Happiness | Season/Time
มุมบนขวา:  Alert Log (โรคระบาด, กบฏ, สงคราม)
มุมล่าง:   Quick Action Bar (Build, Military, Diplomacy, Research)
```

### Floating Dashboard Windows
```
F1 → Economy Dashboard
     ราคาสินค้า Real-time / กราฟ รายรับ-รายจ่าย / Inflation Meter

F2 → War Cabinet
     Squad List + Morale / Naval Fleet / Casus Belli Tracker

F3 → Crisis & Health
     Disease Heatmap Overlay / Prisoner List / Disaster Log

F4 → Diplomacy
     Relation Matrix / Active Treaties / Influence Balance

F5 → Research
     Tech Tree Web (4 Ages x 4 Races)
```

---

## 15. Save System — Partitioned JSON

```
save_slot_1/
├── meta.json      → Profile, Age, Influence (เซฟทุก Action)
├── world_map.json → Grid, Roads, Buildings (เซฟเมื่อกด Save)
├── citizens.json  → Tiny State, Skill, Disease (Async ทุก 5 นาที)
└── economy.json   → Prices, Treasury, Trade (Auto-save ทุก 10 นาที)
```

---

## 16. Multiplayer Possibility

**Architecture: Deterministic Lockstep**
- ส่งเฉพาะ Event Command ผ่านเครือข่าย ไม่ส่ง State
- Tile-Based Naval รองรับ Lockstep โดยธรรมชาติ
- รองรับ 2–4 ผู้เล่น

---

## 17. Live Service

- Seasonal Chronicles (ความท้าทายประจำซีซัน)
- Cosmetic Packs (สกิน Palace / เรือ / UI — ไม่กระทบ Balance)

---

## 18. Future DLC

**DLC 1 — Abyssal Waters**
- Physics Naval System (Wind, Broadside, Boarding)
- Volcanic Island Biome / Sea Monster Events

**DLC 2 — Steam & Clockwork Revolution**
- Crude Oil + Steam Engine
- Physical Railway Supply Chains
- Dwarf Steam-Ironclad

---

## 19. MVP — Minimum Viable Product

| ระบบ | MVP Scope |
|---|---|
| เผ่า | Human เท่านั้น |
| แผนที่ | Grassland + Forest |
| ทรัพยากร | Wood, Stone, Iron, Food, Gold |
| ประชากร | Physical Simulation <= 300 คน |
| สงคราม | Squad-Based บกเท่านั้น |
| Naval | ไม่มี |
| Disease | Phase 1-2 เท่านั้น |
| AI | 1 เมือง (Aggressive) |
| Tech Tree | Age 1-2 |
| UI | HUD + F1 + F2 |
| Save | meta.json + world_map.json |

**เวลาพัฒนา MVP:** 8–12 สัปดาห์

---

## 20. Version 1.0 — Official Launch

- 4 เผ่าครบ พร้อม Asymmetric Balance Framework
- Hybrid Population 1,000 คน/เมือง
- Tile-Based Naval ครบ
- Disease Hybrid C ครบ 3 ระยะ
- Casus Belli + War Exhaustion + Reparations
- Tech Tree ครบ 4 Ages
- AI 4 บุคลิก
- PC UI ครบ F1–F5
- Multiplayer Foundation (Lockstep)

---

## 21. Version 2.0 — Major Update

- Steam Workshop + Level Editor
- Multiplayer 2–4 ผู้เล่น
- Geopolitical Megastructures
- Physics Naval System
- Mobile Port (UI Redesign)

---

## 22. Development Roadmap

| สัปดาห์ | งาน |
|---|---|
| 1–3 | Core Foundation: Grid, Pathfinding, Tiny Movement, Save Architecture |
| 4–6 | Economy & Simulation: Resources, Workers, Market, Buildings |
| 7–9 | Military & AI: Squad, Combat, Utility AI, Fog of War |
| 10–12 | Crisis & UI Polish: Disease Phase 1-2, Casus Belli Basic, F1-F2 UI, Balancing |

---

## 23. Project Risks & Mitigation

| ความเสี่ยง | ระดับ | มาตรการ |
|---|---|---|
| Balance 4 เผ่า | สูง | ทดสอบทีละ 6 Matchup, Community Feedback |
| Performance Tiny > 300 | กลาง | Hybrid Abstract ตั้งแต่ต้น, Job System |
| Feature Creep | สูง | ล็อก MVP Scope เข้มงวด |
| Oppression Exploit | กลาง | Oppression Meter + Negative Feedback Loop |
| Casus Belli Exploit | กลาง | Garrison Requirement + Verification Layer |

---

## 24. Scope Reduction (ถ้าจำเป็น)

ลำดับการตัดโดยไม่ทำลาย Core Loop:
1. ตัด Naval ออก → สงครามบกยังครบ
2. ลด Race เหลือ 2 (Human + Dwarf)
3. Disease เหลือ Phase 1–2 เท่านั้น
4. Diplomacy เหลือแค่ Trade + War
5. Tech Tree เหลือ Age 1–2

---

*GDD Version 2.0 — Final Approved for Development*  
*ระบบทุกอย่างผ่านการ Critique และ Q&A Session ครบถ้วนแล้ว*
