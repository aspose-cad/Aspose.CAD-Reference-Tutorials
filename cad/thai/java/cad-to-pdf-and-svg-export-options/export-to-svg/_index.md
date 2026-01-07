---
date: 2026-01-07
description: เรียนรู้วิธีส่งออก CAD เป็น SVG ด้วย Aspose.CAD สำหรับ Java คู่มือขั้นตอนต่อขั้นตอนนี้จะแสดงวิธีแปลง
  DWG เป็น SVG ตั้งค่าโหมดสีของ SVG และรวมไลบรารีเข้ากับโปรเจกต์ Java ของคุณ
linktitle: Export to SVG
second_title: Aspose.CAD Java API
title: ส่งออก CAD ไปเป็น SVG ด้วย Aspose.CAD สำหรับ Java
url: /th/java/cad-to-pdf-and-svg-export-options/export-to-svg/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ส่งออก CAD เป็น SVG ด้วย Aspose.CAD สำหรับ Java

## บทนำ

ยินดีต้อนรับสู่โลกของ Aspose.CAD สำหรับ Java ไลบรารีที่ทรงพลังซึ่งช่วยให้นักพัฒนาสามารถจัดการกับภาพวาด CAD ได้อย่างง่ายดาย ไม่ว่าคุณจะเป็นนักพัฒนาที่มีประสบการณ์หรือเพิ่งเริ่มต้นในด้าน CAD คู่มือฉบับสมบูรณ์นี้จะพาคุณผ่านขั้นตอน **การส่งออก CAD เป็น SVG** อย่างละเอียด แสดงวิธีแปลง DWG เป็น SVG ตั้งค่าโหมดสีของ SVG และรวม API เข้ากับโปรเจกต์ Java ของคุณ

## คำตอบสั้น ๆ
- **“การส่งออก CAD เป็น SVG” หมายถึงอะไร?** จะทำการแปลงภาพวาด CAD (เช่น DWG) ให้เป็นไฟล์ Scalable Vector Graphics ที่สามารถแสดงในเบราว์เซอร์ได้  
- **ไลบรารีใดรับหน้าที่แปลง?** Aspose.CAD สำหรับ Java มี API ที่เรียบง่ายสำหรับงานนี้  
- **ต้องมีลิขสิทธิ์สำหรับการพัฒนาหรือไม่?** สามารถใช้รุ่นทดลองฟรีสำหรับการทดสอบ; ต้องมีลิขสิทธิ์เชิงพาณิชย์สำหรับการใช้งานจริง  
- **สามารถควบคุมสีของ SVG ได้หรือไม่?** ได้, คุณสามารถตั้งค่าโหมดสีของ SVG (เช่น grayscale)  
- **ต้องการซอฟต์แวร์เพิ่มเติมหรือไม่?** เพียงแค่มี Java runtime และไฟล์ JAR ของ Aspose.CAD

## ข้อกำหนดเบื้องต้น

ก่อนจะเริ่มทำตามบทเรียนนี้ โปรดตรวจสอบว่าคุณมีสิ่งต่อไปนี้แล้ว:

- สภาพแวดล้อมการพัฒนา Java: ตรวจสอบให้แน่ใจว่ามีการติดตั้ง Java บนระบบของคุณ  
- ไลบรารี Aspose.CAD: ดาวน์โหลดและติดตั้ง Aspose.CAD สำหรับ Java จาก [download link](https://releases.aspose.com/cad/java/)  
- โฟลเดอร์เอกสาร: สร้างโฟลเดอร์สำหรับเก็บไฟล์ CAD ของคุณและจดบันทึกตำแหน่งของมันไว้

## นำเข้า Namespaces

ในขั้นตอนนี้ เราจะนำเข้า namespaces ที่จำเป็นเพื่อเริ่มต้นการทำงานกับ Aspose.CAD ทำตามขั้นตอนต่อไปนี้:

### ขั้นตอนที่ 1: เปิดโปรเจกต์ Java ของคุณ
เปิดโปรเจกต์ Java ของคุณใน IDE ที่คุณใช้งาน

### ขั้นตอนที่ 2: เพิ่มไลบรารี Aspose.CAD
เพิ่มไลบรารี Aspose.CAD เข้าไปในโปรเจกต์ของคุณ โดยใส่ไฟล์ JAR ลงใน dependencies ของโปรเจกต์

### ขั้นตอนที่ 3: นำเข้า Namespaces
ในคลาส Java ของคุณ ให้นำเข้า namespaces ที่ต้องการ:

```java
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.SvgOptions;
import com.aspose.cad.imageoptions.SvgColorMode;
```

## ส่งออก CAD เป็น SVG

เมื่อเตรียมพร้อมแล้ว เราจะดำเนินการตามขั้นตอน **การส่งออก CAD เป็น SVG** ด้วย Aspose.CAD สำหรับ Java

### ขั้นตอนที่ 1: ระบุโฟลเดอร์ Resource
กำหนดพาธไปยังโฟลเดอร์ resource ที่เก็บไฟล์ CAD ของคุณ:

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

### ขั้นตอนที่ 2: โหลดภาพวาด CAD
โหลดภาพวาด CAD ด้วยไลบรารี Aspose.CAD:

```java
Image image = Image.load(dataDir + "meshes.dwg");
```

### ขั้นตอนที่ 3: ตั้งค่าตัวเลือกการส่งออก SVG
กำหนดตัวเลือกการส่งออก SVG เพื่อปรับแต่งผลลัพธ์ ที่นี่เราจะ **ตั้งค่าโหมดสีของ SVG** เป็น grayscale และบอกให้ตัวแปลงแปลงข้อความเป็นรูปทรง:

```java
SvgOptions options = new SvgOptions();
options.setColorType(SvgColorMode.Grayscale);
options.setTextAsShapes(true);
```

### ขั้นตอนที่ 4: บันทึกเป็น SVG
บันทึกภาพวาด CAD เป็นไฟล์ SVG:

```java
image.save(dataDir + "meshes.svg");
```

> **เคล็ดลับ:** หากต้องการ **แปลง DWG เป็น SVG** พร้อมคงสีไว้ ให้เปลี่ยน `SvgColorMode.Grayscale` เป็น `SvgColorMode.FullColor`

ยินดีด้วย! คุณได้ส่งออกภาพวาด CAD เป็น SVG สำเร็จด้วย Aspose.CAD สำหรับ Java

## ทำไมต้องใช้ Aspose.CAD เพื่อส่งออก CAD เป็น SVG?
- **ความแม่นยำสูง:** ข้อมูลเวกเตอร์ถูกเก็บรักษาไว้ ทำให้ SVG มีลักษณะเหมือนต้นฉบับ CAD อย่างเต็มที่  
- **ไม่มีการพึ่งพาเครื่องมือภายนอก:** การแปลงทำงานทั้งหมดภายใน Java ไม่ต้องใช้เครื่องมือเพิ่มเติม  
- **ผลลัพธ์ที่ปรับแต่งได้:** ตัวเลือกเช่น `setColorType` ให้คุณควบคุมว่า SVG จะเป็น grayscale หรือสีเต็ม

## ปัญหาที่พบบ่อยและวิธีแก้
- **ไฟล์ไม่พบ:** ตรวจสอบให้ `dataDir` ชี้ไปยังโฟลเดอร์ที่ถูกต้องและชื่อไฟล์ DWG ตรงกัน  
- **SVG ว่างเปล่า:** ตรวจสอบว่าคุณได้ตั้งค่า `options.setTextAsShapes(true)` หากภาพวาดมีข้อความที่ต้องการแสดงเป็นรูปทรง  
- **รูปแบบ CAD ไม่รองรับ:** Aspose.CAD รองรับ DWG, DXF, DWF และหลายรูปแบบอื่น; ตรวจสอบเอกสารสำหรับรายการเต็ม

## สรุป

ในบทเรียนนี้ เราได้สำรวจกระบวนการที่ราบรื่นของการใช้ Aspose.CAD สำหรับ Java เพื่อ **ส่งออก CAD เป็น SVG** ด้วย API ที่ใช้งานง่ายและฟีเจอร์ที่แข็งแกร่ง Aspose.CAD ทำให้การทำงานที่ซับซ้อนกลายเป็นเรื่องง่ายสำหรับนักพัฒนา

## คำถามที่พบบ่อย

### Q1: สามารถใช้ Aspose.CAD สำหรับ Java กับรูปแบบ CAD อื่นได้หรือไม่?

A1: ได้, Aspose.CAD รองรับรูปแบบ CAD หลากหลาย รวมถึง DWG, DXF, DWF และอื่น ๆ

### Q2: Aspose.CAD เหมาะกับทั้งผู้เริ่มต้นและนักพัฒนาที่มีประสบการณ์หรือไม่?

A2: แน่นอน! Aspose.CAD มี API ที่เป็นมิตรกับผู้ใช้ ทำให้ผู้เริ่มต้นเข้าถึงได้ง่าย พร้อมฟีเจอร์ขั้นสูงสำหรับนักพัฒนาที่ชำนาญ

### Q3: จะหาการสนับสนุนเพิ่มเติมหรือชุมชนได้จากที่ไหน?

A3: เยี่ยมชม [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19) เพื่อรับการสนับสนุนและเข้าร่วมการสนทนา

### Q4: มีรุ่นทดลองฟรีหรือไม่?

A4: มี, คุณสามารถสำรวจ Aspose.CAD ด้วย [free trial](https://releases.aspose.com/)

### Q5: จะซื้อไลเซนส์สำหรับ Aspose.CAD สำหรับ Java ได้อย่างไร?

A5: สามารถซื้อไลเซนส์ได้จาก [purchase page](https://purchase.aspose.com/buy)

## Frequently Asked Questions

**Q: สามารถแปลงไฟล์ DXF เป็น SVG ด้วยโค้ดเดียวกันได้หรือไม่?**  
A: ได้, เพียงเปลี่ยนชื่อไฟล์เป็น DXF; API จะจัดการได้ทั้งสองรูปแบบ

**Q: จะเปลี่ยนผลลัพธ์เป็น SVG สีเต็มได้อย่างไร?**  
A: ตั้งค่า `options.setColorType(SvgColorMode.FullColor);` ก่อนบันทึก

**Q: สามารถฝังฟอนต์ใน SVG ที่สร้างขึ้นได้หรือไม่?**  
A: Aspose.CAD ปัจจุบันแปลงข้อความเป็นรูปทรง; การฝังฟอนต์ไม่จำเป็น

**Q: ไลบรารีทำงานบน Linux และ macOS หรือไม่?**  
A: ไลบรารี Java เป็นแบบ platform‑independent ทำงานได้ทุกที่ที่มี JVM ที่รองรับ

**Q: เวอร์ชันของ Aspose.CAD ที่ใช้ในบทเรียนนี้คืออะไร?**  
A: ตัวอย่างทดสอบกับ Aspose.CAD สำหรับ Java 24.10

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**อัปเดตล่าสุด:** 2026-01-07  
**ทดสอบด้วย:** Aspose.CAD สำหรับ Java 24.10  
**ผู้เขียน:** Aspose  

---