---
tags: [gdd, save-system, multiplayer, live-service]
version: "3.0"
related:
  - "[[00-Index]]"
  - "[[17-Tech-Stack-Dev-Environment]]"
---

# 💾 Save System — Partitioned JSON

```
save_slot_1/
├── meta.json      → Profile, Age, Influence (เซฟทุก Action)
├── world_map.json → Grid, Roads, Buildings (เซฟเมื่อกด Save)
├── citizens.json  → Tiny State, Skill, Disease (Async ทุก 5 นาที)
└── economy.json   → Prices, Treasury, Trade (Auto-save ทุก 10 นาที)
```

- รองรับ **3-5 Save Slots** ตามที่ผู้เล่นกำหนด
- ออกแบบให้ Modular ตั้งแต่ต้น เพื่อรองรับ Mod Support ในอนาคต (แยกไฟล์ตามระบบ ไม่ผูกทุกอย่างไว้ที่เดียว)

---

# 🌐 Multiplayer Possibility (v2.0)

**สถานะ: เลื่อนไป v2.0 — ไม่ทำใน v1.0**

**Architecture: Deterministic Lockstep**
- ส่งเฉพาะ Event Command ผ่านเครือข่าย ไม่ส่ง State
- Tile-Based Naval รองรับ Lockstep โดยธรรมชาติ (ดู [[09-Naval-Disease]])
- รองรับ 2–4 ผู้เล่น

---

# 📡 Live Service

- Seasonal Chronicles (ความท้าทายประจำซีซัน)
- Cosmetic Packs (สกิน Palace / เรือ / UI — ไม่กระทบ Balance)

## เชื่อมโยง
- Mod Support ต้องออกแบบ Save System ให้รองรับตั้งแต่ต้น → [[15-Risks-Scope-Reduction]]
