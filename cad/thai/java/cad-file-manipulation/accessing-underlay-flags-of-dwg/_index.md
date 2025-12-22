---
date: 2025-12-22
description: เรียนรู้วิธีโหลดไฟล์ DWG และดึงข้อมูลอันเดอร์เลย์ด้วย Aspose.CAD for
  Java – คู่มือแบบขั้นตอนต่อขั้นตอนที่ครอบคลุมแฟล็กอันเดอร์เลย์
linktitle: Accessing Underlay Flags of DWG
second_title: Aspose.CAD Java API
title: โหลดไฟล์ DWG และเข้าถึงแฟล็ก Underlay – Aspose.CAD สำหรับ Java
url: /th/java/cad-file-manipulation/accessing-underlay-flags-of-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# โหลดไฟล์ DWG & เข้าถึง Underlay Flags – Aspose.CAD for Java

ในกระบวนการทำงาน CAD สมัยใหม่ การ **โหลดไฟล์ DWG** อย่างรวดเร็วและดึงข้อมูล underlay เป็นความต้องการที่พบบ่อย ไม่ว่าคุณจะสร้าง viewer, ทำการประมวลผลเป็นชุดอัตโนมัติ, หรือสกัด metadata เพื่อการบูรณาการกับ GIS, Aspose.CAD for Java ให้วิธีที่สะอาดและเป็นโค้ด‑first ในการทำสิ่งเหล่านี้ ในบทแนะนำนี้เราจะเดินผ่านขั้นตอนที่แม่นยำเพื่อ **โหลดไฟล์ DWG**, วนลูป entity ต่าง ๆ, และอ่าน underlay flags ที่หลาย ๆ นักพัฒนามักมองข้าม

## คำตอบอย่างรวดเร็ว
- **คลาสหลักที่ใช้เปิด DWG คืออะไร?** `com.aspose.cad.Image.load()` จะคืนค่าเป็น `CadImage`
- **อ็อบเจกต์ใดเก็บข้อมูล underlay?** `CadUnderlay` (หรือชนิดที่สืบทอดเช่น `CadDgnUnderlay`)
- **ต้องการไลเซนส์สำหรับการพัฒนาไหม?** เวอร์ชันทดลองฟรีใช้ได้สำหรับการทดสอบ; ต้องมีไลเซนส์เชิงพาณิชย์สำหรับการใช้งานจริง
- **สามารถประมวลผลหลายไฟล์ DWG ในลูปได้หรือไม่?** ได้ – เพียงทำซ้ำรูปแบบการโหลด‑และ‑วนลูป
- **วิธีนี้เข้ากันได้กับ Java 11+ หรือไม่?** แน่นอน, Aspose.CAD รองรับ Java 8 จนถึงรุ่น LTS ล่าสุด

## “load dwg file” ใน Aspose.CAD คืออะไร?
`Image.load()` อ่านข้อมูลไบนารีของ DWG และสร้างอ็อบเจกต์ `CadImage` ในหน่วยความจำ จากนั้นคุณสามารถสำรวจ layers, blocks, และ underlay entities ได้โดยไม่ต้องจัดการกับรูปแบบไฟล์ DWG ด้วยตนเอง

## ทำไมต้องสกัด underlay flags จาก DWG?
Underlay flags บอกว่าการอ้างอิงภายนอก (เช่น DGN หรือ PDF underlay) ถูกวางตำแหน่ง, ปรับสเกล, และหมุนอย่างไรภายใน drawing การรู้ค่าดังกล่าวทำให้คุณสามารถ:

- สร้างเลย์เอาต์ภาพที่ตรงกันใน viewer ที่กำหนดเอง
- แปลง underlay ให้เป็น entity CAD ต้นฉบับเพื่อการแก้ไขต่อไป
- สร้างรายงานที่รวม metadata ของ underlay เพื่อการปฏิบัติตามหรือเอกสาร

## สิ่งที่ต้องเตรียม
- **Aspose.CAD Library** – ดาวน์โหลดจากหน้า [releases](https://releases.aspose.com/cad/java/)
- **Java Development Kit** – JDK 8 หรือใหม่กว่า
- **โฟลเดอร์** ที่มีไฟล์ DWG ที่คุณต้องการวิเคราะห์ แทนที่ `"Your Document Directory"` ในโค้ดด้วยพาธจริงของคุณ

## นำเข้า Namespaces

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadBaseEntity;
import com.aspose.cad.fileformats.cad.cadobjects.CadDgnUnderlay;
import com.aspose.cad.fileformats.cad.cadobjects.CadUnderlay;
import com.aspose.cad.fileformats.cad.cadobjects.UnderlayFlags;
```

## คู่มือขั้นตอน‑โดย‑ขั้นตอน

### ขั้นตอนที่ 1: ตั้งค่า Resource Directory
```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DWGDrawings/";
```
กำหนดตำแหน่งที่ไฟล์ DWG ของคุณอยู่ การใช้โฟลเดอร์เฉพาะทำให้ตัวอย่างสะอาดและพกพาได้ง่าย

### ขั้นตอนที่ 2: โหลดไฟล์ DWG
```java
// Input file name and path
String fileName = dataDir + "BlockRefDgn.dwg";

// Load an existing DWG file and convert it into CadImage 
CadImage image = (CadImage)Image.load(fileName);
```
ที่นี่เราจะ **load dwg file** `BlockRefDgn.dwg` เข้าไปในอินสแตนซ์ `CadImage` เพื่อพร้อมตรวจสอบ

### ขั้นตอนที่ 3: วนลูป Entity ของ DWG
```java
// Go through each entity inside the DWG file
for(CadBaseEntity entity : image.getEntities())
```
ลูปนี้จะเดินผ่านทุก entity—lines, circles, blocks, และ underlays—เพื่อให้เราสามารถเลือกเอาเฉพาะที่ต้องการได้

### ขั้นตอนที่ 4: ระบุ CadDgnUnderlay Entities
```java
// Check if entity is of CadDgnUnderlay type
if (entity instanceof CadDgnUnderlay)
```
เฉพาะอ็อบเจกต์ `CadDgnUnderlay` เท่านั้นที่มี underlay flags ที่เราต้องการ จึงทำการกรองเฉพาะอันนี้

### ขั้นตอนที่ 5: เข้าถึงข้อมูล Underlay
```java
// Access different underlay flags 
CadUnderlay underlay = (CadUnderlay) entity;
System.out.println(underlay.getUnderlayPath());
System.out.println(underlay.getUnderlayName());
// ... (Additional underlay properties)
break;
```
เมื่อเรามี `CadUnderlay` แล้ว เราสามารถอ่านพาธ, ชื่อ, จุดแทรก, การหมุน, ปัจจัยสเกล, และ enum `UnderlayFlags` ที่บ่งบอกการมองเห็น, การคลิป, และตัวเลือกการเรนเดอร์อื่น ๆ

## ปัญหาที่พบบ่อย & เคล็ดลับ
- **พาธ underlay เป็น null** – ตรวจสอบให้แน่ใจว่า DWG อ้างอิงไฟล์ภายนอกจริง; มิฉะนั้นพาธจะว่างเปล่า
- **ประเภท underlay ไม่รองรับ** – ปัจจุบัน Aspose.CAD รองรับ DGN underlays; PDF underlays ยังไม่เปิดให้ใช้ผ่าน API
- **ข้อยกเว้นไลเซนส์** – การรันโค้ดโดยไม่มีไลเซนส์ที่ถูกต้องจะทำให้ภาพที่ส่งออกมีลายน้ำ

## คำถามที่พบบ่อย

**ถาม: สามารถใช้ Aspose.CAD for Java กับรูปแบบไฟล์ CAD อื่นได้หรือไม่?**  
ตอบ: Aspose.CAD มุ่งเน้นที่รูปแบบ DWG เป็นหลัก, แต่ยังรองรับ DXF, DWF, และรูปแบบ CAD อื่น ๆ

**ถาม: มีเวอร์ชันทดลองสำหรับ Aspose.CAD for Java หรือไม่?**  
ตอบ: มี, คุณสามารถสำรวจคุณสมบัติต่าง ๆ ได้ฟรีจาก [ที่นี่](https://releases.aspose.com/)

**ถาม: จะขอรับการสนับสนุนหรือความช่วยเหลือสำหรับ Aspose.CAD for Java ได้อย่างไร?**  
ตอบ: เยี่ยมชม [ฟอรั่ม Aspose.CAD](https://forum.aspose.com/c/cad/19) เพื่อรับการสนับสนุนจากชุมชนและการสนทนา

**ถาม: มีไลเซนส์ชั่วคราวสำหรับ Aspose.CAD for Java หรือไม่?**  
ตอบ: มี, คุณสามารถรับไลเซนส์ชั่วคราวได้จาก [ที่นี่](https://purchase.aspose.com/temporary-license/)

**ถาม: จะหาเอกสารประกอบที่ครบถ้วนสำหรับ Aspose.CAD for Java ได้จากที่ไหน?**  
ตอบ: ดูที่ [documentation](https://reference.aspose.com/cad/java/) สำหรับข้อมูลรายละเอียด

---

**อัปเดตล่าสุด:** 2025-12-22  
**ทดสอบด้วย:** Aspose.CAD 24.12 for Java  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}