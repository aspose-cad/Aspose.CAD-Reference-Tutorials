---
date: 2025-12-19
description: เรียนรู้วิธีส่งออก PDF ของ AutoCAD ด้วย Aspose.CAD สำหรับ Java คู่มือขั้นตอนนี้จะแสดงวิธีแปลง
  DWG เป็น PDF, บันทึก CAD เป็น PDF, และจัดการการให้สิทธิ์ใช้งาน.
linktitle: Export AutoCAD Images to PDF
second_title: Aspose.CAD Java API
title: ส่งออก PDF จาก AutoCAD - ส่งออกภาพ AutoCAD เป็น PDF ด้วย Aspose.CAD สำหรับ
  Java (บทเรียน)
url: /th/java/cad-export-options/export-autocad-images-to-pdf/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ส่งออก AutoCAD PDF - ส่งออกภาพ AutoCAD เป็น PDF ด้วย Aspose.CAD สำหรับ Java

## บทนำ

คุณกำลังมองหาแนวทางการ **export AutoCAD PDF** ด้วย Java อย่างราบรื่นหรือไม่? ไม่ต้องหาเพิ่มเติม! ในบทแนะนำนี้เราจะพาคุณผ่านขั้นตอนการแปลงภาพ AutoCAD เป็น PDF ด้วย Aspose.CAD สำหรับ Java ซึ่งเป็นไลบรารีที่ทรงพลังที่ทำให้กระบวนการ **convert DWG to PDF** เป็นเรื่องง่าย สุดท้ายคุณจะเข้าใจวิธี **save CAD as PDF**, ปรับตั้งค่าการเรสเตอร์ไลซ์แบบกำหนดเอง, และทำงานกับใบอนุญาต Aspose.CAD สำหรับการใช้งานในผลิตภัณฑ์

## คำตอบด่วน
- **ฉันสามารถแปลง DWG เป็น PDF ด้วย Java ได้หรือไม่?** ใช่, Aspose.CAD สำหรับ Java รองรับ DWG, DXF และรูปแบบอื่น ๆ มากมาย.  
- **ฉันต้องการใบอนุญาตหรือไม่?** จำเป็นต้องมี **Aspose CAD license** เพื่อการใช้งานไม่จำกัด; มีใบอนุญาตชั่วคราวสำหรับการประเมิน.  
- **เวอร์ชัน Java ที่รองรับคืออะไร?** Java 8+ (ไลบรารีเข้ากันได้กับ JDK สมัยใหม่ทั้งหมด).  
- **ฉันสามารถปรับขนาดหน้าของ PDF ได้หรือไม่?** แน่นอน – ปรับ `pageWidth` และ `pageHeight` ในตัวเลือกการเรสเตอร์ไลซ์.  
- **การเรสเตอร์ไลซ์ 3‑D เป็นไปได้หรือไม่?** ใช่, เปิดใช้งาน `TypeOfEntities.Entities3D` เพื่อการเรนเดอร์ 3‑D เต็มรูปแบบ.

## อะไรคือ **export autocad pdf**?
การส่งออก AutoCAD PDF หมายถึงการแปลงภาพวาด CAD แบบเวกเตอร์ (DWG, DXF, DWF ฯลฯ) ให้เป็นเอกสาร PDF พกพาได้โดยคงรักษาชั้น, ความหนาของเส้น, และโดยออปชัน 3‑D geometry ซึ่งเป็นประโยชน์สำหรับการแชร์แบบกับลูกค้า, การเก็บถาวร, หรือการพิมพ์โดยไม่ต้องใช้ซอฟต์แวร์ CAD

## ทำไมต้องใช้ Aspose.CAD สำหรับ Java เพื่อ **export autocad pdf**?
- **รองรับรูปแบบเต็ม** – ทำงานกับ DWG, DXF, DWF และอื่น ๆ อีกมาก.  
- **ไม่มีการพึ่งพาภายนอก** – ไลบรารี Java แท้, ไม่มี DLL แบบเนทีฟ.  
- **การเรสเตอร์ไลซ์คุณภาพสูง** – ควบคุม DPI, ขนาดหน้า, และเลย์เอาต์.  
- **ความยืดหยุ่นของใบอนุญาต** – เริ่มต้นด้วยการทดลองใช้ฟรี, จากนั้นอัปเกรดเป็น **Aspose CAD license** ถาวร.  

## ข้อกำหนดเบื้องต้น

ก่อนเริ่มทำงาน โปรดตรวจสอบว่าคุณมี:

- **สภาพแวดล้อมการพัฒนา Java** – ติดตั้ง JDK 8 หรือใหม่กว่า.  
- **ไลบรารี Aspose.CAD สำหรับ Java** – ดาวน์โหลดจาก [download link](https://releases.aspose.com/cad/java/).  
- **ไดเรกทอรีเอกสาร** – โฟลเดอร์บนเครื่องของคุณที่เก็บไฟล์ CAD ต้นฉบับและ PDF ที่สร้างขึ้น.

## นำเข้า Namespaces

ในโปรเจกต์ Java ของคุณ ให้นำเข้าคลาสที่จำเป็นเพื่อทำงานกับ Aspose.CAD:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

ตอนนี้เราจะเดินผ่านโค้ดทีละขั้นตอน.

## คู่มือขั้นตอนต่อขั้นตอน

### ขั้นตอนที่ 1: ตั้งค่าพาธไดเรกทอรีทรัพยากร

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
```

> **เคล็ดลับ**: แทนที่ `"Your Document Directory"` ด้วยพาธเต็มของโฟลเดอร์ที่คุณสร้างในข้อกำหนดเบื้องต้น.

### ขั้นตอนที่ 2: โหลดภาพ CAD

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

> **ทำไมจึงสำคัญ**: การโหลดไฟล์ CAD เข้าไปในอ็อบเจกต์ `Image` ให้คุณเข้าถึงเครื่องยนต์การเรสเตอร์ไลซ์ของ Aspose.CAD อย่างเต็มที่.

### ขั้นตอนที่ 3: ตั้งค่าตัวเลือกการเรสเตอร์ไลซ์

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setPageHeight(500);
// rasterizationOptions.setTypeOfEntities(TypeOfEntities.Entities3D);

rasterizationOptions.setLayouts(new String[] {"Model"});
```

- ปรับ `pageWidth` และ `pageHeight` เพื่อเปลี่ยนขนาดของ PDF ที่ส่งออก.  
- ยกเลิกการคอมเมนต์บรรทัด `setTypeOfEntities` หากคุณต้องการ **java convert cad pdf** สำหรับเอนทิตี้ 3‑D.  
- คำสั่ง `setLayouts` เลือกเลย์เอาต์ (Model, Layout1 ฯลฯ) ที่จะเรนเดอร์.

### ขั้นตอนที่ 4: ตั้งค่าตัวเลือก PDF

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

นี่ทำให้การตั้งค่าการเรสเตอร์ไลซ์เชื่อมต่อกับการส่งออก PDF, ทำให้ข้อมูลเวกเตอร์แปลงอย่างถูกต้อง.

### ขั้นตอนที่ 5: บันทึก PDF

```java
cadImage.save(dataDir + "Export3DImagestoPDF_out_.pdf", pdfOptions);
```

ไฟล์ที่ได้, `Export3DImagestoPDF_out_.pdf`, เป็นการแสดงผล **save cad as pdf** ของการวาด AutoCAD ดั้งเดิมของคุณ.

## ปัญหาทั่วไปและวิธีแก้

| อาการ | สาเหตุที่เป็นไปได้ | วิธีแก้ |
|-------|-------------------|--------|
| PDF ว่างเปล่า | ตัวเลือกการเรสเตอร์ไลซ์ไม่ได้ตั้งค่าหรือเลย์เอาต์ไม่ตรงกัน | ตรวจสอบว่า `setLayouts` ตรงกับชื่อเลย์เอาต์ในไฟล์ CAD ของคุณ. |
| ภาพความละเอียดต่ำ | `pageWidth`/`pageHeight` เล็กเกินไป | เพิ่มขนาดหรือกำหนด DPI สูงกว่าโดยใช้ `rasterizationOptions.setResolution(...)`. |
| ข้อยกเว้นใบอนุญาต | ไม่มีใบอนุญาตที่ถูกต้องถูกนำไปใช้ | ใช้ **Aspose CAD license** หรือใช้ใบอนุญาตชั่วคราวสำหรับการทดสอบ. |

## คำถามที่พบบ่อย

### Q1: ฉันสามารถใช้ Aspose.CAD สำหรับ Java กับรูปแบบไฟล์ CAD อื่นได้หรือไม่?
**A1:** ใช่, Aspose.CAD รองรับรูปแบบหลากหลายรวมถึง DWG, DWF, DGN และอื่น ๆ ให้ความยืดหยุ่นในโครงการของคุณ.

### Q2: ฉันจะขอรับใบอนุญาตชั่วคราวสำหรับ Aspose.CAD สำหรับ Java อย่างไร?
**A2:** เยี่ยมชม [here](https://purchase.aspose.com/temporary-license/) เพื่อรับใบอนุญาตชั่วคราวสำหรับการประเมิน.

### Q3: มีตัวเลือกเลย์เอาต์สำหรับการเรสเตอร์ไลซ์หรือไม่?
**A3:** ใช่, คุณสามารถปรับแต่งเลย์เอาต์ (เช่น `"Model"`, `"Layout1"`) ผ่านเมธอด `setLayouts` เพื่อควบคุมว่ามุมมองใดจะถูกเรนเดอร์.

### Q4: ฉันสามารถปรับขนาดไฟล์ PDF ที่ส่งออกได้หรือไม่?
**A4:** แน่นอน! ปรับพารามิเตอร์ `pageWidth` และ `pageHeight` ในตัวเลือกการเรสเตอร์ไลซ์ให้ตรงกับขนาดที่ต้องการ.

### Q5: ฉันจะหาความช่วยเหลือหรือหารือเกี่ยวกับปัญหา Aspose.CAD สำหรับ Java ได้ที่ไหน?
**A5:** ไปที่ [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) เพื่อรับการสนับสนุนและการสนทนาชุมชน.

**Last Updated:** 2025-12-19  
**Tested With:** Aspose.CAD for Java 24.10  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}