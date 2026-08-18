---
tags: [gdd, risks, scope]
version: "3.0"
related:
  - "[[00-Index]]"
  - "[[14-MVP-Roadmap-Versions]]"
---

# ⚠️ Project Risks & Scope Reduction

## จุดเสี่ยงของโปรเจกต์

| ความเสี่ยง | ระดับ | มาตรการ |
|---|---|---|
| Balance 4 เผ่า | สูง | ทดสอบทีละ 6 Matchup (4C2), Community Feedback |
| Performance Tiny > 300 ตัว/เมือง | กลาง | Hybrid Abstract ตั้งแต่ต้น, Job System, Object Pooling |
| Feature Creep | สูง | ล็อก MVP Scope ให้ชัดเจนในแต่ละช่วง แม้ไม่มี Deadline บังคับ |
| Oppression Exploit | กลาง | Oppression Meter + Negative Feedback Loop |
| Casus Belli Exploit | กลาง | Garrison Requirement + Verification Layer |
| **Solo Dev Burnout** | สูง | ใช้ AI Generate Art เพื่อลดภาระ, พัก/สลับงานเมื่อรู้สึกล้า, ไม่ผูกตัวเองกับ Deadline |
| **AI-Generated Art Consistency** | กลาง | จำกัดการใช้ AI Art เฉพาะ Landscape/Background/Tile เท่านั้น, Character/Building ทำเอง+Krita เพื่อคุม Consistency |
| **Localization 7 ภาษา พร้อมกัน** | กลาง | ใช้ String Key System ตั้งแต่ต้น + Phased Rollout (ไม่ทำพร้อมกันทั้งหมด) |
| **Mod Support ต้อง Clean Architecture** | กลาง | ออกแบบ Save System แบบ Modular (Partitioned JSON) ตั้งแต่ต้น |

## วิธีลด Scope (ถ้าจำเป็น — เรียงลำดับการตัดโดยไม่ทำลาย Core Loop)

1. ตัด Naval ออก → สงครามบกยังครบ
2. ลด Race เหลือ 2 (Human + Dwarf) ชั่วคราวเพื่อทดสอบ Balance ก่อนขยาย
3. Disease เหลือ Phase 1–2 เท่านั้น
4. Diplomacy เหลือแค่ Trade + War (ตัด Casus Belli ประเภทอื่นชั่วคราว)
5. Tech Tree เหลือ Age 1–2
6. ลด Session/Map ให้เล็กลง เพื่อลดภาระ Performance ระหว่างทดสอบ

> หมายเหตุ: ลำดับนี้ใช้เฉพาะกรณี**จำเป็นจริง ๆ** เท่านั้น — เนื่องจากโปรเจกต์นี้ไม่มีข้อจำกัดเวลา ควรพยายามคง Full Scope ให้นานที่สุดก่อนตัดสินใจลด

## AI Art Strategy (ตัดสินใจ: Option C — Smart Split)
```
AI Generate (GPT/Gemini):
  ✅ Landscape Tiles (หญ้า, ป่า, ภูเขา)
  ✅ Background (ท้องฟ้า, เมฆ)

ทำเอง + Krita:
  ❌ Character Sprite (ต้อง Consistency สูง)
  ❌ Building (ต้อง Consistency สูง)
```
เหตุผล: AI-Generated Character/Building มักมี Quality ไม่สม่ำเสมอ (ขนาด, มุมกล้อง, สไตล์เพี้ยน) การแก้ไขทีหลังอาจใช้เวลาเท่าทำเองตั้งแต่ต้น จึงประหยัดเวลาแค่ส่วน Landscape/Background ที่ Consistency ไม่สำคัญเท่า

## เชื่อมโยง
- Image Generation Prompts → [[16-Art-Asset-Prompts]]
