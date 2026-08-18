---
tags: [gdd, economy, market]
version: "3.0"
related:
  - "[[00-Index]]"
  - "[[06-AI-Design]]"
priority: core-pillar
---

# 💰 Economy Design

> ระบบที่ผู้ออกแบบ (Snoopy) "ตื่นตัวมากที่สุด" — ต้องทำให้สมจริงและลึก (Medium Complexity — Option B)

## Multi-Tier Resource Chain
```
Tier 1 (Raw):       Wood, Stone, Iron Ore, Gold Ore, Water
Tier 2 (Processed): Firewood, Charcoal, Iron Ingot, Flour, Cloth
Tier 3 (Advanced):  Steel*, Bread, Tools, Weapons, Armor, Medicine, Horses
(* Steel ผลิตได้เฉพาะ Dwarf Deep Forge เท่านั้น — ดู [[03-Races/Dwarf]])
```

## Dynamic Price System
- ตลาดคำนวณราคาทุก "วัน" ในเกม ตาม Supply-Demand
- Supply มาก → ราคาตก | Supply ขาด → ราคาพุ่ง
- **ราคาแตกต่างกันในแต่ละเมือง** (Medium Complexity — ตัดสินใจแล้ว)
- ผู้เล่นคำนวณ Profit Margin เพื่อให้คุ้มทำการค้า

## กลไกการตั้งราคา — Market House System
ตัดสินใจใช้ **Option C: Market House (อาคารพิเศษ)**

```
สร้าง "Market House" ในเมือง
  → ผู้เล่นคลิกเข้าไปดู Dashboard
  → ระบบแสดง: "ปลายทางไหนราคาสูงสุด?"
  → ผู้เล่นตั้งราคา Auto-sell
  → Caravan (เกวียน) ส่งสินค้าไปเองบน Grid
```
- ให้ความรู้สึก "ตั้งเส้นทางการค้า" มากกว่าการเลื่อน Slider เฉย ๆ
- ต้องมี Visual Caravan เดินบน Grid จริง (เชื่อมกับ [[04-Population-System]])

## Money Sink (แก้ปัญหา Late Game Gold Glut)
| Money Sink | รายละเอียด |
|---|---|
| Building Upkeep | ค่าบำรุงรักษาอาคารรายปี (หลักสำคัญที่สุด) |
| Skilled Worker Wages | Tiny Tier 3 เรียกเงินเดือนสูงขึ้น |
| Tribute | ค่าบรรณาการให้พันธมิตรตามสนธิสัญญา |
| Disaster Relief | Random Event บังคับจ่ายเงินฉุกเฉิน |
| Military Upkeep | ทหารทุกหน่วยมีค่า Wage รายสัปดาห์ |

## AI Cities ในตลาด
- เริ่มต้น MVP: **3 AI Cities** (รวมผู้เล่นเป็น 4 เมือง) — ตลาดวุ่นวายพอดี ไม่ซับซ้อนเกินไป
- อนาคต: ขยายรองรับได้ถึง 20 เมือง (ตามที่ผู้เล่นกำหนดขนาดแผนที่)
- ผู้เล่น**ต้องเห็น AI กำลังทำการค้า** (Visual Caravan ของ AI เดินบน Grid ด้วย ไม่ใช่แค่ Log ข้อความ)

## เชื่อมโยง
- AI Trading Logic → [[06-AI-Design]]
- Resource Flow เต็มรูปแบบ → [[11-Building-Resource-Flow]]
- Casus Belli จาก Trade Default → [[07-Diplomacy]]
