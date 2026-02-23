---
date: 2026-02-23
description: เรียนรู้วิธีโหลดไฟล์ DWG ด้วย Aspose CAD DWG สำหรับ Java และสกัดแฟล็ก
  Underlay – คู่มือแบบขั้นตอนต่อขั้นตอนสำหรับนักพัฒนา
linktitle: Accessing Underlay Flags of DWG
second_title: Aspose.CAD Java API
title: aspose cad dwg – โหลด DWG และเข้าถึงแฟล็ก Underlay (Java)
url: /th/java/cad-file-manipulation/accessing-underlay-flags-of-dwg/
weight: 11
---

 answer.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# โหลดไฟล์ DWG และเข้าถึง Underlay Flags – Aspose.CAD for Java

ในกระบวนการทำงาน CAD สมัยใหม่, **with aspose cad dwg you can quickly load a DWG file** และดึงรายละเอียด underlay ที่มักจะซ่อนจากผู้ชมทั่วไป ไม่ว่าคุณจะกำลังสร้าง Java DWG viewer, ทำอัตโนมัติ batch process dwg pipeline, หรือสกัด metadata สำหรับการบูรณาการ GIS, Aspose.CAD for Java จะให้วิธีที่สะอาดและเน้นโค้ดในการทำเช่นนั้น ในบทเรียนนี้เราจะอธิบายขั้นตอนที่แน่นอนเพื่อ **load a DWG file**, iterate its entities, และอ่าน underlay flags ที่นักพัฒนาหลายคนมักมองข้าม.

## คำตอบอย่างรวดเร็ว
- **คลาสหลักที่ใช้เปิด DWG คืออะไร?** `com.aspose.cad.Image.load()` returns a `CadImage`.
- **วัตถุใดที่เก็บข้อมูล underlay?** `CadUnderlay` (or its derived types like `CadDgnUnderlay`).
- **ฉันต้องใช้ไลเซนส์สำหรับการพัฒนาหรือไม่?** A free trial works for testing; a commercial license is required for production.
- **ฉันสามารถประมวลผลไฟล์ DWG หลายไฟล์ในลูปได้หรือไม่?** Yes – just repeat the load‑and‑iterate pattern.
- **วิธีนี้เข้ากันได้กับ Java 11+ หรือไม่?** Absolutely, Aspose.CAD supports Java 8 through the latest LTS releases.

## aspose cad dwg – การโหลดไฟล์ DWG (Java)

`Image.load()` อ่านเนื้อหา DWG แบบไบนารีและสร้างอ็อบเจ็กต์ `CadImage` ในหน่วยความจำ จากนั้นคุณสามารถสำรวจเลเยอร์, บล็อก, และเอนทิตี้ underlay ได้โดยไม่ต้องจัดการกับรูปแบบไฟล์ DWG ด้วยตนเอง.

## ทำไมต้องสกัด underlay flags จาก DWG?

Underlay flags บอกวิธีที่อ้างอิงภายนอก (เช่น DGN หรือ PDF underlay) ถูกวางตำแหน่ง, ปรับสเกล, และหมุนภายในภาพวาด การรู้ค่าต่าง ๆ เหล่านี้ทำให้คุณสามารถ:

- สร้างเลย์เอาต์ภาพที่แม่นยำใน **java dwg viewer** ที่กำหนดเอง
- แปลง underlay ไปเป็นเอนทิตี้ CAD แบบดั้งเดิมเพื่อการแก้ไขต่อไป
- สร้างรายงานที่รวม metadata ของ underlay เพื่อการปฏิบัติตามหรือเอกสาร
- **Batch process dwg** ไฟล์และเก็บ metadata ของ underlay ไว้ในฐานข้อมูลเพื่อการวิเคราะห์ในภายหลัง

## ข้อกำหนดเบื้องต้น
- **Aspose.CAD Library** – ดาวน์โหลดจากหน้า [releases](https://releases.aspose.com/cad/java/)  
- **Java Development Kit** – JDK 8 หรือใหม่กว่า.  
- **โฟลเดอร์** ที่บรรจุไฟล์ DWG ที่คุณต้องการวิเคราะห์ แทนที่ `"Your Document Directory"` ในโค้ดด้วยพาธจริงของคุณ.

## นำเข้า Namespaces

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadBaseEntity;
import com.aspose.cad.fileformats.cad.cadobjects.CadDgnUnderlay;
import com.aspose.cad.fileformats.cad.cadobjects.CadUnderlay;
import com.aspose.cad.fileformats.cad.cadobjects.UnderlayFlags;
```

## คู่มือขั้นตอนต่อขั้นตอน

### ขั้นตอนที่ 1: ตั้งค่า Resource Directory
```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DWGDrawings/";
```
กำหนดตำแหน่งที่ไฟล์ DWG ของคุณอยู่ การใช้โฟลเดอร์เฉพาะช่วยให้ตัวอย่างสะอาดและพกพาได้ง่าย.

### ขั้นตอนที่ 2: โหลดไฟล์ DWG
```java
// Input file name and path
String fileName = dataDir + "BlockRefDgn.dwg";

// Load an existing DWG file and convert it into CadImage 
CadImage image = (CadImage)Image.load(fileName);
```
ที่นี่เราจะ **load dwg file** `BlockRefDgn.dwg` เข้าไปในอินสแตนซ์ `CadImage` พร้อมสำหรับการตรวจสอบ.

### ขั้นตอนที่ 3: วนลูปผ่านเอนทิตี้ DWG
```java
// Go through each entity inside the DWG file
for(CadBaseEntity entity : image.getEntities())
```
ลูปนี้จะเดินผ่านทุกเอนทิตี้—เส้น, วงกลม, บล็อก, และ underlay—เพื่อให้เราสามารถเลือกสิ่งที่ต้องการได้.

### ขั้นตอนที่ 4: ระบุเอนทิตี้ CadDgnUnderlay
```java
// Check if entity is of CadDgnUnderlay type
if (entity instanceof CadDgnUnderlay)
```
เฉพาะอ็อบเจ็กต์ `CadDgnUnderlay` เท่านั้นที่มี underlay flags ที่เราต้องการ ดังนั้นเราจึงกรองหาอ็อบเจ็กต์เหล่านั้น.

### ขั้นตอนที่ 5: เข้าถึงข้อมูล Underlay
```java
// Access different underlay flags 
CadUnderlay underlay = (CadUnderlay) entity;
System.out.println(underlay.getUnderlayPath());
System.out.println(underlay.getUnderlayName());
// ... (Additional underlay properties)
break;
```
เมื่อเรามี `CadUnderlay` แล้ว เราสามารถอ่านพาธ, ชื่อ, จุดแทรก, การหมุน, ปัจจัยสเกล, และ enum `UnderlayFlags` ที่บ่งบอกการมองเห็น, การคลิป, และตัวเลือกการเรนเดอร์อื่น ๆ.

## วิธีโหลดไฟล์ dwg ในกระบวนการ batch process

หากคุณต้องการ **batch process dwg** ไฟล์ ให้ใส่ขั้นตอนข้างต้นในลูป `for` ง่าย ๆ ที่วนผ่านไฟล์ทั้งหมดใน `dataDir` การเรียก `Image.load()` เดียวกันทำงานกับแต่ละไฟล์ได้ และคุณสามารถเก็บ flags ที่สกัดออกมาในไฟล์ CSV หรือฐานข้อมูลเพื่อการรายงานต่อไป.

## ปัญหาทั่วไป & เคล็ดลับ
- **Null underlay path** – ตรวจสอบให้แน่ใจว่า DWG อ้างอิงไฟล์ภายนอกจริง; มิฉะนั้นพาธจะว่างเปล่า.
- **Unsupported underlay type** – ปัจจุบัน Aspose.CAD รองรับ DGN underlays; PDF underlays ยังไม่เปิดให้ใช้ผ่าน API.
- **License exceptions** – การรันโค้ดโดยไม่มีไลเซนส์ที่ถูกต้องจะเพิ่มลายน้ำให้กับภาพที่ส่งออกทั้งหมด.
- **Performance tip:** ใช้อ็อบเจ็กต์ `Image` ตัวเดียวเมื่อประมวลผลหลายไฟล์ใน batch เพื่อ ลดภาระการทำงานของ GC.

## คำถามที่พบบ่อย

**Q: ฉันสามารถใช้ Aspose.CAD for Java กับรูปแบบไฟล์ CAD อื่นได้หรือไม่?**  
A: Aspose.CAD มุ่งเน้นที่รูปแบบ DWG เป็นหลัก แต่ยังรองรับ DXF, DWF, และรูปแบบ CAD อื่น ๆ

**Q: มีเวอร์ชันทดลองสำหรับ Aspose.CAD for Java หรือไม่?**  
A: มี, คุณสามารถสำรวจคุณสมบัติต่าง ๆ ด้วยการทดลองฟรีจาก [here](https://releases.aspose.com/).

**Q: ฉันจะขอรับการสนับสนุนหรือขอความช่วยเหลือเกี่ยวกับ Aspose.CAD for Java ได้อย่างไร?**  
A: เยี่ยมชม [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) เพื่อรับการสนับสนุนจากชุมชนและการสนทนา.

**Q: มีไลเซนส์ชั่วคราวสำหรับ Aspose.CAD for Java หรือไม่?**  
A: มี, คุณสามารถรับไลเซนส์ชั่วคราวได้จาก [here](https://purchase.aspose.com/temporary-license/).

**Q: ฉันจะหาเอกสารครบถ้วนสำหรับ Aspose.CAD for Java ได้จากที่ไหน?**  
A: ดูที่ [documentation](https://reference.aspose.com/cad/java/) เพื่อข้อมูลโดยละเอียด.

---

**อัปเดตล่าสุด:** 2026-02-23  
**ทดสอบกับ:** Aspose.CAD 24.12 for Java  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}