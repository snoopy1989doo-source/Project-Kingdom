---
tags: [gdd, art, prompts, pixel-art]
version: "3.0"
related:
  - "[[00-Index]]"
  - "[[15-Risks-Scope-Reduction]]"
---

# 🎨 คลังคำสั่งสร้างภาพ (Image Generation Prompts)

## หลักการใช้ไฟล์นี้
- ทุก Prompt เขียนเป็น **2 ภาษา**: คำอธิบายภาษาไทย (เพื่อความเข้าใจ) + Prompt ภาษาอังกฤษ (สำหรับ Copy ไปใช้จริงกับ AI Generator เพราะแม่นยำกว่า)
- โมเดล AI ส่วนใหญ่เทรนด้วยข้อมูล Caption ภาษาอังกฤษเป็นหลัก การใช้ Prompt อังกฤษโดยตรงจะได้ผลลัพธ์แม่นยำและสม่ำเสมอกว่าการแปลจากไทย
- จัดหมวดหมู่ตาม: **ตัวละคร (Characters) → อาคาร (Buildings) → ภูมิทัศน์ (Landscape) → เอฟเฟกต์ (VFX/Lighting)**

---

## 1️⃣ หมวดตัวละคร (Characters)

> ตาม [[15-Risks-Scope-Reduction]]: Character ควรทำเอง + Krita Touch-up เพื่อคุม Consistency แต่ใช้ AI เป็นจุดเริ่มต้น (Draft/Reference) ได้

### 🏹 Human — Crossbowman (Role ที่ 4, เพิ่มใหม่)

**คำอธิบายไทย:**
- สไตล์ภาพ: Pixel Art 16-bit มุมบนลงล่าง (Top-down) แบบเดียวกับชุด Sprite Sheet ที่มีอยู่แล้ว
- Layout: 4 ช่อง (Idle, Walk 1, Walk 2, Walk 3), หัวข้อ "CROSSBOWMAN" ด้านล่าง, พื้นหลังกล่องสีเทาเหมือนชุดเดิม
- รูปร่าง: มนุษย์ตัวเตี้ยป้อม (Chibi Style) สัดส่วน 2-3 หัวตัว เหมือน Sprite Human อื่น ๆ
- ชุด: เกราะหนังสีน้ำตาล/แทน, หน้าไม้ถือแนวทแยงตอน Idle, ยกขึ้นเล็กน้อยตอนเดิน, ถุงใส่ลูกดอกสะพายหลัง/สะโพก, หมวกผ้าหรือฮู้ดหนังธรรมดา (ไม่ใช่หมวกเหล็กเต็มแบบ Soldier)
- สี: หลักน้ำตาลหนัง, รอง เทาเข้ม (โลหะหน้าไม้), จุดเน้น แดง/ทอง (ให้เข้ากับ Human Merchant)

**English Prompt:**
```
16-bit pixel art, top-down RPG character sprite sheet, matching an existing 
"Kingdom Builder Character Sprites" series style. Layout: 4 columns labeled 
Idle, Walk 1, Walk 2, Walk 3, with header text "CROSSBOWMAN" below, dark gray 
rounded rectangle background boxes per row, black background overall.

Character: short chibi-proportioned human (2-3 heads tall), medium build, 
matching the same art style as existing Human Soldier and Merchant sprites.

Outfit: brown leather chest armor, crossbow held diagonally across body in 
idle pose (raised slightly higher during walk frames), bolt quiver strapped 
to back or hip, simple cloth cap or leather hood (not a full metal helmet).

Color palette: primary brown leather tones (#8B5A2B range), secondary dark 
grey crossbow and metal bolt tips, accent red/gold trim matching the Human 
faction Merchant sprite for consistency.

Animation: Idle = standing, crossbow held ready at chest height. Walk 1-3 = 
walking cycle, crossbow bounces slightly, legs alternate stride, consistent 
with existing walk cycle framing in the reference sheet.
```

---

### 🐴 Mount Units (ทหารม้าแต่ละเผ่า)

**คำอธิบายไทย (โครงสร้างทั่วไป):**
- ต้องสร้างแยก 4 ชุด ตามเผ่า: Human (ม้า), Elf (กวางเขาใหญ่), Orc (หมูป่า), Dwarf (แพะภูเขา)
- แต่ละชุดใช้ Layout เดียวกับ Character Sheet เดิม (Idle, Walk 1-3) แต่เพิ่มขนาดภาพให้รวมสัตว์พาหนะ + ผู้ขี่
- สีสัตว์พาหนะต้องกลมกลืนกับ Palette ของเผ่านั้น ๆ

**English Prompt (Template — เปลี่ยนเผ่า/สัตว์ตามต้องการ):**
```
16-bit pixel art, top-down RPG mounted-unit sprite sheet, matching an existing 
"Kingdom Builder Character Sprites" series style. Layout: 4 columns labeled 
Idle, Walk 1, Walk 2, Walk 3, header text "[RACE] RIDER" below, dark gray 
background boxes per row.

Character: chibi-proportioned [race] rider mounted on [mount animal], 
rider matches existing [race] faction color palette and armor style, 
mount animal sized proportionally larger than a standing character sprite 
but still fitting the same tile grid.

Mount animal details: [insert specific animal description, e.g. "sturdy 
brown horse with simple leather tack" / "large elk with ornate antlers, 
pale grey-white fur" / "muscular wild boar, dark green-brown hide, tusks 
visible" / "shaggy white mountain goat with curved horns, sure-footed pose"]

Color palette: matches existing [race] faction sprites for consistency.

Animation: Idle = mount standing still, rider alert holding weapon. 
Walk 1-3 = galloping/trotting cycle, legs of mount alternate, rider posture 
leans slightly forward.
```

**ตัวอย่างการแทนค่าแต่ละเผ่า:**
- Human: `[mount animal]` = "a sturdy brown horse with simple leather tack and reins"
- Elf: `[mount animal]` = "a large elegant great stag with tall branching antlers, pale grey-white fur, forest green riding gear"
- Orc: `[mount animal]` = "a muscular wild boar with dark green-brown bristled hide, visible tusks, crude leather harness"
- Dwarf: `[mount animal]` = "a shaggy white mountain goat with large curved horns, sure-footed stance, simple rope harness"

---

## 2️⃣ หมวดอาคาร (Buildings)

**คำอธิบายไทย (โครงสร้างทั่วไปสำหรับ Unique Building):**
- แต่ละเผ่ามีอาคาร Unique 1 หลัง: Grand Embassy (Human), Ancient Grove (Elf), War Totem (Orc), Deep Forge (Dwarf)
- สไตล์ต้องตรงกับภาพ Day/Night Town Scene ที่มีอยู่แล้ว (Isometric-ish Top-down, สัดส่วนอาคารในเมือง)

**English Prompt (Template):**
```
16-bit pixel art, top-down/slight isometric building sprite, matching the 
art style of an existing medieval fantasy town scene (day and night versions 
with warm window glow lighting). 

Building: [insert building name and description, e.g. "Grand Embassy - an 
ornate two-story stone building with tall arched windows, blue and gold 
banners, a welcoming open courtyard entrance"]

Color palette: matches [race] faction colors. Include both a day-lit version 
(bright, clear shadows) and optionally a night version (warm glowing windows, 
torches lit, deep blue-purple ambient shadows) consistent with the existing 
day/night town reference image.

Style: consistent stone/wood texture detail level as the reference town scene, 
same pixel density (not more detailed, not less).
```

---

## 3️⃣ หมวดภูมิทัศน์ (Landscape / Tiles) — เหมาะกับ AI Generate เต็มที่

> จุดนี้ AI Generate ได้อย่างอิสระ เพราะ Consistency ไม่กระทบเท่า Character/Building

**คำอธิบายไทย:**
- ใช้สำหรับพื้นหญ้า, ป่า, ภูเขา, น้ำ, ถนน ฯลฯ

**English Prompt (Template):**
```
16-bit pixel art tileset, seamless tile, top-down game map style, 
[insert terrain type e.g. "lush grassland with small flower details" / 
"dense pine forest floor with fallen logs" / "rocky mountain terrain with 
grey stone texture" / "calm blue river water with subtle wave animation frames"].

Color palette: vibrant but not oversaturated, matching a warm medieval 
fantasy kingdom builder game. Must tile seamlessly on all four edges.
```

---

## 4️⃣ หมวดเอฟเฟกต์/แสง (VFX & Lighting)

**English Prompt (Template):**
```
16-bit pixel art lighting effect, top-down view, [insert effect e.g. 
"warm torch flame flicker animation, 4 frames" / "soft moonlight glow 
overlay for night scenes" / "dust cloud effect for marching army units"].

Must be compatible with a medieval fantasy pixel art kingdom-building game, 
transparent background (PNG), consistent pixel scale with existing 
character sprites.
```

---

## 📌 หมายเหตุการใช้งาน
- ทุกครั้งที่ต้องการภาพใหม่ (อาคาร Unique อื่น ๆ, หน่วยพิเศษเพิ่มเติม, ฉากใหม่) ให้ขอ Prompt ในรูปแบบเดียวกันนี้จาก Claude
- เก็บภาพที่ Generate สำเร็จแล้วไว้เป็น Reference สำหรับ Prompt ครั้งต่อไป เพื่อรักษาความสม่ำเสมอของสไตล์
