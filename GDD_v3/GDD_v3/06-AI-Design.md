---
tags: [gdd, ai, personality]
version: "3.0"
related:
  - "[[00-Index]]"
  - "[[05-Economy-Design]]"
priority: core-pillar
---

# 🤖 AI Design

> ตัดสินใจให้ AI เป็นแบบ **Simple แต่มีบุคลิก (Option C)** — ไม่ต้องมี Deep Planning Tree ซับซ้อน แต่ต้องคงบุคลิก 4 แบบไว้ตามเดิมใน GDD v2.0 เพื่อให้การค้าขายมีสีสัน

## Hybrid Architecture

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

## AI Personality (สุ่มต่อ Session)
- **Aggressive:** สร้างทหารก่อน, Hostility Weight สูง, ซื้ออาหาร+อาวุธเยอะ
- **Merchant:** ค้าขายก่อน, ประกาศสงครามยาก, ซื้อ/ขายดุเดือด
- **Expansionist:** ส่ง Enclave เร็ว, Defend น้อย
- **Isolationist:** ปิดพรมแดน, แข็งแกร่งแต่ไม่โต, ซื้อน้อยขายแพง

## หลักการสำคัญ: ผู้เล่นต้อง "เห็น" AI ทำการค้า
- AI ไม่ใช่แค่ตัวเลขเบื้องหลัง — ต้องมี Visual Caravan เดินจริงบน Grid เหมือนของผู้เล่น
- Dashboard ควรแสดงว่า AI เมืองไหนกำลังซื้อ-ขายอะไร เพื่อให้ผู้เล่นวางแผนแข่งขันได้

## AI Trading ตาม Personality (ตัวอย่างพฤติกรรม)
| บุคลิก | พฤติกรรมซื้อขาย |
|---|---|
| Aggressive (มักเป็น Orc) | ซื้ออาหาร+อาวุธเยอะ (ต้องเงินฝึกทหาร), ขายสินค้าถูกเพื่อรีบได้เงินสด |
| Merchant (มักเป็น Human) | ซื้อ/ขายดุเดือดตาม Supply-Demand, ไม่ยอมให้เมืองอื่นตัดราคา |
| Expansionist (มักเป็น Elf) | ซื้อไม้+วัตถุดิบเยอะสำหรับตั้ง Enclave, ขายยา/สมุนไพรแพง |
| Isolationist (มักเป็น Dwarf) | ซื้อน้อย เน้น Self-sufficient, ขายเหล็ก/Steel แพงมาก (ผูกขาด) |

> หมายเหตุ: บุคลิกสุ่มต่อ Session ไม่ผูกตายตัวกับเผ่า แต่มีแนวโน้มบางเผ่าจะสุ่มบุคลิกที่เข้ากับ Lore ได้บ่อยกว่า

## เชื่อมโยง
- Casus Belli trigger จากพฤติกรรม AI → [[07-Diplomacy]]
- Combat behavior → [[08-Combat-Design]]
- Trading logic ผูกกับ Market House → [[05-Economy-Design]]
