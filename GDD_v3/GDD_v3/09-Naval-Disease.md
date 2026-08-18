---
tags: [gdd, naval, disease]
version: "3.0"
related:
  - "[[00-Index]]"
  - "[[08-Combat-Design]]"
---

# ⚓ Naval System — Tile-Based V1.0

## หลักการ
- เรือเคลื่อนที่เป็น Grid บน Water Tile
- Deterministic โดยธรรมชาติ — รองรับ Multiplayer Lockstep ในอนาคต
- ไม่มี Physics Engine (Physics Naval → ย้ายไป DLC 1 หรือ v2.0)

## Naval Actions
| Action | วิธีทำงาน |
|---|---|
| Naval Blockade | วางเรือ Tile หน้าท่าเรือ → ปิด Trade Route |
| Boarding | เรือชิด → ทหาร Deck เข้า Melee บน Grid |
| Transport | รับทหารจาก Dock → ย้ายข้ามทะเล |
| Patrol | กำหนด Patrol Route บน Water Tile |

---

# 🦠 Disease System — Hybrid C

## 3 ระยะ

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

## เชื่อมโยง
- Disease กระทบ Population → [[04-Population-System]]
- Quarantine Gate → [[11-Building-Resource-Flow]]
