---
tags: [gdd, ui, ux]
version: "3.0"
related:
  - "[[00-Index]]"
  - "[[17-Tech-Stack-Dev-Environment]]"
---

# 🖥️ UI Flow — PC-Only (Keyboard & Mouse)

> Localization-Ready: ต้องออกแบบ UI ให้รองรับ Text ยาว (สเปน) และ Font พิเศษ (ไทย/เกาหลี/ญี่ปุ่น) ตั้งแต่เริ่ม

## HUD (Always Visible)
```
มุมบนซ้าย: Gold | Food | Population | Happiness | Season/Time
มุมบนขวา:  Alert Log (โรคระบาด, กบฏ, สงคราม)
มุมล่าง:   Quick Action Bar (Build, Military, Diplomacy, Research)
```

## Floating Dashboard Windows
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

## Pre-Game Setup Screen (เพิ่มใหม่ v3.0)
ก่อนเริ่มเกม ผู้เล่นต้องตั้งค่า:
- ขนาดแผนที่ (เล็ก/กลาง/ใหญ่)
- จำนวนเมือง (สูงสุด 20)
- โหมด: Scenario vs Free Play
- Save Slot ที่จะใช้ (3-5 slots)
- ภาษา (Localization)

## Localization Considerations
| ประเด็น | แนวทาง |
|---|---|
| Font ไทย/เกาหลี/ญี่ปุ่น | ต้องเลือก Font ที่รองรับ Unicode ครบ ตั้งแต่ต้น |
| Text ยาว (สเปน) | UI ต้อง Responsive/Dynamic Width ไม่ Fix ขนาด |
| String Key System | ใช้ Key-based String Table (ไม่ Hardcode ข้อความในโค้ด) เพื่อรองรับ Phased Localization |

## เชื่อมโยง
- Localization Rollout Plan → [[14-MVP-Roadmap-Versions]]
