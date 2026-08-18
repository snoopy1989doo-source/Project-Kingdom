---
tags: [gdd, tech-stack, tools]
version: "3.0"
related:
  - "[[00-Index]]"
---

# 🛠️ Tech Stack & Dev Environment

## Engine
- **Unity (C#)** — Personal License
- เหตุผลที่เลือก: รองรับ Pixel Art ดี, Community/Asset Store ใหญ่, Mod Support ทำได้, พื้นฐาน Web Dev เดิมช่วยให้เรียน C# ได้เร็วขึ้น

## Version Control
- **GitHub** — ใช้เก็บ Backup + History + Rollback (มีประสบการณ์จากการทำ Web App มาก่อน)

## Art Pipeline
```
AI Generate (GPT/Gemini)
   → ใช้เฉพาะ: Landscape Tiles, Background
   → Export PNG
       ↓
Krita (Manual Touch-up)
   → ใช้สำหรับ: Character Sprite, Building (ต้อง Consistency สูง)
       ↓
Import เข้า Unity
```

ดู Prompt Library เต็มรูปแบบที่ [[16-Art-Asset-Prompts]]

## Audio
- Snoopy ผลิตเสียงเอง (Sound Production)
- เป้าหมาย: ~10 BGM Tracks, 50-70+ SFX (Medium-Premium Quality)

## Localization Pipeline
- ใช้ String Key System (ไม่ Hardcode ข้อความในโค้ด) เพื่อรองรับ Phased Rollout
- ดูแผน Rollout ที่ [[14-MVP-Roadmap-Versions]]

## Package/Tool Checklist
- [ ] Unity Hub + Unity Editor (LTS version)
- [ ] Git + GitHub Desktop หรือ CLI
- [ ] Krita (ติดตั้งแล้วหรือยัง — ต้องเตรียม)
- [ ] Aseprite (ทางเลือกเสริมสำหรับ Pixel Art เฉพาะทาง ถ้าต้องการในอนาคต)
- [ ] เครื่องมือสร้างเสียง (มีอยู่แล้ว)
- [ ] AI Image Tool: GPT/Gemini (สำหรับ Landscape/Background)

## เชื่อมโยง
- Save System Architecture (Modular, รองรับ Mod) → [[13-Save-Multiplayer-LiveService]]
- Risk เกี่ยวกับ AI Art Consistency → [[15-Risks-Scope-Reduction]]
