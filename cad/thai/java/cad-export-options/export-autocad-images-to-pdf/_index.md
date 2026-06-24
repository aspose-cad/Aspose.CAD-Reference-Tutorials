---
date: 2026-02-20
description: เรียนรู้วิธีส่งออก PDF ของ AutoCAD ด้วย Aspose.CAD สำหรับ Java คู่มือขั้นตอนต่อขั้นตอนนี้จะแสดงให้คุณเห็นวิธี
  **แปลง DWG เป็น PDF**, **บันทึก CAD เป็น PDF**, และจัดการการให้สิทธิ์ใช้งาน.
linktitle: Export AutoCAD Images to PDF
second_title: Aspose.CAD Java API
title: แปลง DWG เป็น PDF - ส่งออกภาพ AutoCAD เป็น PDF ด้วย Aspose.CAD สำหรับ Java
url: /th/java/cad-export-options/export-autocad-images-to-pdf/
weight: 10
---

 Aspose.CAD for Java" -> "ส่งออก AutoCAD PDF - ส่งออกภาพ AutoCAD เป็น PDF ด้วย Aspose.CAD for Java"

Proceed.

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ส่งออก AutoCAD PDF - ส่งออกภาพ AutoCAD เป็น PDF ด้วย Aspose.CAD for Java

## บทนำ

คุณกำลังมองหา **การแปลง DWG เป็น PDF** ด้วย Java อยู่หรือไม่? ไม่ต้องหาไกล! ในบทแนะนำนี้เราจะพาคุณผ่านขั้นตอนการแปลงภาพ AutoCAD เป็น PDF ด้วย Aspose.CAD for Java ซึ่งเป็นไลบรารีที่ทรงพลังทำให้กระบวนการ **แปลง DWG เป็น PDF** เป็นเรื่องง่าย สุดท้ายคุณจะเข้าใจวิธี **บันทึก CAD เป็น PDF**, ตั้งค่าการเรสเตอร์ไลซ์แบบกำหนดเอง, และทำงานกับใบอนุญาต Aspose.CAD สำหรับการใช้งานในสภาพแวดล้อมการผลิต

## คำตอบสั้น
- **ฉันสามารถแปลง DWG เป็น PDF ด้วย Java ได้หรือไม่?** ได้, Aspose.CAD for Java รองรับ DWG, DXF และรูปแบบอื่น ๆ อีกมากมาย  
- **ฉันต้องการใบอนุญาตหรือไม่?** จำเป็นต้องมี **ใบอนุญาต Aspose CAD** เพื่อใช้งานไม่จำกัด; มีใบอนุญาตชั่วคราวสำหรับการประเมินผล  
- **รองรับเวอร์ชัน Java ใด?** Java 8+ (ไลบรารีเข้ากันได้กับ JDK สมัยใหม่ทั้งหมด)  
- **ฉันสามารถปรับขนาดหน้ PDF ได้หรือไม่?** แน่นอน – ปรับ `pageWidth` และ `pageHeight` ในตัวเลือกการเรสเตอร์ไลซ์  
- **การเรสเตอร์ไลซ์ 3‑D เป็นไปได้หรือไม่?** ใช่, เปิดใช้งาน `TypeOfEntities.Entities3D` เพื่อเรนเดอร์ 3‑D อย่างเต็มรูปแบบ

## **export autocad pdf** คืออะไร?
การส่งออก AutoCAD PDF หมายถึงการแปลงแบบร่าง CAD ที่เป็นเวกเตอร์ (DWG, DXF, DWF ฯลฯ) ให้เป็นเอกสาร PDF พกพาได้พร้อมคงรักษาชั้น, ความหนาของเส้น, และโดยเลือกอาจรวมถึงเรขาคณิต 3‑D ซึ่งเป็นประโยชน์สำหรับการแชร์แบบออกแบบกับลูกค้า, การเก็บถาวร, หรือการพิมพ์โดยไม่ต้องใช้ซอฟต์แวร์ CAD

## ทำไมต้องแปลง DWG เป็น PDF ด้วย Aspose.CAD for Java?
- **รองรับรูปแบบครบวงจร** – ทำงานกับ DWG, DXF, DWF และอื่น ๆ อีกมาก  
- **ไม่มีการพึ่งพาไลบรารีภายนอก** – ไลบรารี Java แท้ ๆ ไม่ต้องใช้ DLL เนทีฟ  
- **เรสเตอร์ไลซ์คุณภาพสูง** – ควบคุม DPI, ขนาดหน้า, และการจัดวาง, ดังนั้นคุณสามารถ **ปรับขนาดหน้ PDF** ให้ตรงกับความต้องการของโครงการได้  
- **ความยืดหยุ่นของใบอนุญาต** – เริ่มต้นด้วยการทดลองใช้งานฟรี, แล้วอัปเกรดเป็น **ใบอนุญาต Aspose CAD** ถาวร  

## ข้อกำหนดเบื้องต้น

ก่อนเริ่มทำงาน, โปรดตรวจสอบว่าคุณมี:

- **สภาพแวดล้อมการพัฒนา Java** – ติดตั้ง JDK 8 หรือใหม่กว่า  
- **Aspose.CAD for Java Library** – ดาวน์โหลดจาก [ลิงก์ดาวน์โหลด](https://releases.aspose.com/cad/java/)  
- **ไดเรกทอรีเอกสาร** – โฟลเดอร์บนเครื่องของคุณที่เก็บไฟล์ CAD ต้นฉบับและ PDF ที่สร้างขึ้น

## นำเข้า Namespaces

ในโปรเจกต์ Java ของคุณ, นำเข้าคลาสที่จำเป็นสำหรับทำงานกับ Aspose.CAD:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

ตอนนี้มาดูโค้ดทีละขั้นตอนกัน

## วิธีแปลง DWG เป็น PDF ด้วย Aspose.CAD for Java

### ขั้นตอนที่ 1: ตั้งค่าเส้นทางไดเรกทอรีทรัพยากร

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
```

> **เคล็ดลับ:** แทนที่ `"Your Document Directory"` ด้วยเส้นทางเต็มของโฟลเดอร์ที่คุณสร้างในขั้นตอนข้อกำหนดเบื้องต้น

### ขั้นตอนที่ 2: โหลดภาพ CAD

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

> **ทำไมถึงสำคัญ:** การโหลดไฟล์ CAD เข้าเป็นอ็อบเจกต์ `Image` ทำให้คุณเข้าถึงเอนจินเรสเตอร์ไลซ์ของ Aspose.CAD ได้เต็มที่

### ขั้นตอนที่ 3: ตั้งค่าตัวเลือกการเรสเตอร์ไลซ์

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setPageHeight(500);
// rasterizationOptions.setTypeOfEntities(TypeOfEntities.Entities3D);

rasterizationOptions.setLayouts(new String[] {"Model"});
```

- ปรับ `pageWidth` และ `pageHeight` เพื่อ **ปรับขนาดหน้ PDF** ตามต้องการ  
- ยกเลิกคอมเมนต์บรรทัด `setTypeOfEntities` หากคุณต้องการ **java convert cad pdf** สำหรับเอนทิตี 3‑D  
- การเรียก `setLayouts` จะเลือกเลเอาต์ (Model, Layout1, ฯลฯ) ที่ต้องการเรนเดอร์

### ขั้นตอนที่ 4: ตั้งค่าตัวเลือก PDF

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

ขั้นตอนนี้เชื่อมการตั้งค่าเรสเตอร์ไลซ์กับการส่งออก PDF, ทำให้ข้อมูลเวกเตอร์ถูกแปลงอย่างถูกต้อง

### ขั้นตอนที่ 5: บันทึกเป็น PDF

```java
cadImage.save(dataDir + "Export3DImagestoPDF_out_.pdf", pdfOptions);
```

ไฟล์ที่ได้, `Export3DImagestoPDF_out_.pdf`, เป็นการ **save cad as pdf** ของภาพวาด AutoCAD ดั้งเดิมของคุณ

## ปัญหาที่พบบ่อย & วิธีแก้

| Symptom | Likely Cause | Fix |
|---------|--------------|-----|
| PDF ว่างเปล่า | ไม่ได้ตั้งค่าตัวเลือกการเรสเตอร์ไลซ์หรือเลเอาต์ไม่ตรง | ตรวจสอบให้ `setLayouts` ตรงกับชื่อเลเอาต์ในไฟล์ CAD ของคุณ |
| ภาพความละเอียดต่ำ | `pageWidth`/`pageHeight` เล็กเกินไป | เพิ่มขนาดหรือกำหนด DPI สูงกว่าโดยใช้ `rasterizationOptions.setResolution(...)` |
| ข้อผิดพลาดใบอนุญาต | ไม่มีการใช้ใบอนุญาตที่ถูกต้อง | ใช้ **ใบอนุญาต Aspose CAD** หรือใบอนุญาตชั่วคราวสำหรับการทดสอบ |

## คำถามที่พบบ่อย

### Q1: ฉันสามารถใช้ Aspose.CAD for Java กับรูปแบบไฟล์ CAD อื่นได้หรือไม่?
A1: ได้, Aspose.CAD รองรับรูปแบบหลากหลายรวมถึง DWG, DWF, DGN และอื่น ๆ อีกมาก ทำให้คุณมีความยืดหยุ่นในโครงการของคุณ

### Q2: ฉันจะขอรับใบอนุญาตชั่วคราวสำหรับ Aspose.CAD for Java ได้อย่างไร?
A2: เยี่ยมชม [ที่นี่](https://purchase.aspose.com/temporary-license/) เพื่อรับใบอนุญาตชั่วคราวสำหรับการประเมินผล

### Q3: มีตัวเลือกเลเอาต์สำหรับการเรสเตอร์ไลซ์หรือไม่?
A3: มี, คุณสามารถกำหนดเลเอาต์ (เช่น `"Model"`, `"Layout1"`) ผ่านเมธอด `setLayouts` เพื่อควบคุมว่ามุมมองใดจะถูกเรนเดอร์

### Q4: ฉันสามารถปรับขนาดไฟล์ PDF ที่ส่งออกได้หรือไม่?
A4: แน่นอน! ปรับพารามิเตอร์ `pageWidth` และ `pageHeight` ในตัวเลือกการเรสเตอร์ไลซ์ให้ตรงกับขนาดที่ต้องการ

### Q5: ฉันจะหาแหล่งช่วยเหลือหรือพูดคุยเกี่ยวกับปัญหา Aspose.CAD for Java ได้จากที่ไหน?
A5: ไปที่ [ฟอรัม Aspose.CAD](https://forum.aspose.com/c/cad/19) เพื่อรับการสนับสนุนเฉพาะด้านและการสนทนากับชุมชน

---

**อัปเดตล่าสุด:** 2026-02-20  
**ทดสอบด้วย:** Aspose.CAD for Java 24.10  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}