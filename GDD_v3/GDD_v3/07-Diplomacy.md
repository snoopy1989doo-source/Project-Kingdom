---
tags: [gdd, diplomacy, casus-belli]
version: "3.0"
related:
  - "[[00-Index]]"
  - "[[06-AI-Design]]"
  - "[[08-Combat-Design]]"
---

# 🤝 Diplomacy Design — Casus Belli System

> ตัดสินใจแล้วว่าต้องมี **Casus Belli ครบทั้ง 4 ประเภท** ตั้งแต่ MVP — สำคัญทั้งหมด, ไม่ตัดออก
> **Trade Default** เป็นตัวที่ Priority สูงสุดสำหรับการทดสอบ MVP ก่อน

## Casus Belli Triggers

| ประเภท | เงื่อนไข | MVP Priority |
|---|---|---|
| Trade Default | ศัตรูขึ้นภาษีเกินกว่าสัญญา | ⭐ สูงสุด — ทำก่อน |
| Supply Raid Claim | ตรวจพบหน่วยศัตรูโจมตีเกวียนสินค้า | สำคัญ |
| Espionage Exposure | จับสายลับศัตรูได้ในเมือง | สำคัญ |
| Enclave Annexation | ศัตรูยึด Enclave โดยไม่ประกาศสงคราม | สำคัญ |

## Casus Belli Rules (ป้องกัน War Spam)
- **Expiry:** หมดอายุใน 5 ปีในเกมถ้าไม่ใช้
- **War Exhaustion:** หลังสงคราม ต้องรอ 2 ปีในเกม
- **Reparations Treaty:** ชดเชยเพื่อล้าง Casus Belli — **เป็นข้อตกลงชั่วคราวเท่านั้น** ไม่ใช่การแก้ปัญหาถาวร
- **Garrison Requirement:** ต้องมีทหาร >20 นายใน Enclave ก่อน Raid Claim จะใช้ได้

## Diplomacy Actions ทั่วไป
- เมืองเป็นมิตร / เป็นศัตรู
- พันธมิตร (Alliance)
- สนธิสัญญา (Treaty)
- เปิด/ปิดการค้า
- ช่วยรบ (War Support)
- แลกเปลี่ยนทรัพยากร
- ส่งของขวัญ (Gift — เพิ่ม Relation)
- เจรจา (Negotiation)
- สอดแนม (Espionage)

## เชื่อมโยงกับ Victory Condition
- Human Diplomatic Victory ต้องใช้ระบบนี้เป็นหลัก — ดู 03-Races/Human
- Envoy Guard (Human Unique Unit) ลด Casus Belli จากศัตรูรอบข้าง 10%

## เชื่อมโยง
- ผลจาก Casus Belli → นำไปสู่สงคราม → [[08-Combat-Design]]
- AI ตัดสินใจประกาศสงคราม → [[06-AI-Design]]
