---
tags: [gdd, buildings, resources]
version: "3.0"
related:
  - "[[00-Index]]"
  - "[[05-Economy-Design]]"
---

# 🏗️ Building Tree & Resource Flow

## Civil & Palace
| อาคาร | ฟังก์ชัน |
|---|---|
| Housing | แหล่งกำเนิดแรงงาน |
| Royal Palace | ศูนย์บริหาร, ผลิต Influence Points |
| Royal Prison | ควบคุมโจร → แรงงาน (มี Oppression Meter) |

## Production & Logistics
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
| Stable | Hay + Water → Horses/Mounts (ดู 03-Races/Race-Balance-Overview) |
| Herbalist | Plants → Medicine |
| **Market House** | ศูนย์กลางตั้งราคา + ส่ง Caravan (ดู [[05-Economy-Design]]) |

## Roads
```
Dirt Path → Stone Road → Iron-Plated Highway
Speed:  1x → 1.5x → 2.5x
```

## Military & Security
| อาคาร | ฟังก์ชัน |
|---|---|
| Barracks | ฝึก Squad |
| Arsenal | เก็บ Weapons/Armor |
| Watchtower | แผ่ Visibility |
| Signal Beacon | แจ้งเตือน Alert ทั่วแผนที่ |
| Quarantine Gate | ปิดถนน Node ป้องกันโรค |
| Maritime Dock | สร้างเรือ Tile-Based |

## Unique Buildings ตามเผ่า
| เผ่า | อาคาร |
|---|---|
| Human | Grand Embassy |
| Elf | Ancient Grove |
| Orc | War Totem |
| Dwarf | Deep Forge |

## Resource Flow Diagram
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

## เชื่อมโยง
- Tech Tree ปลดล็อกอาคาร → [[10-Tech-Tree]]
- Population ทำงานในอาคาร → [[04-Population-System]]
