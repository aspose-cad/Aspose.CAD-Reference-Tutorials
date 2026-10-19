---
date: 2026-10-19
description: เรียนรู้วิธีแปลง DWG เป็น PDF ใน Java ด้วย Aspose.CAD คู่มือขั้นตอนต่อขั้นตอนนี้จะแสดงวิธีส่งออก
  AutoCAD PDF, บันทึก CAD เป็น PDF, และใช้ไลเซนส์
keywords:
- dwg to pdf java
- export autocad pdf
- java pdf export library
- aspose cad license
- save cad pdf
- customize pdf page size
lastmod: 2026-10-19
linktitle: ส่งออกภาพ AutoCAD เป็น PDF
og_description: เรียนรู้วิธีแปลง DWG เป็น PDF ใน Java ด้วย Aspose.CAD คู่มือนี้จะพาคุณผ่านการส่งออก
  AutoCAD PDF, การบันทึก CAD เป็น PDF, และการจัดการไลเซนส์
og_image_alt: 'Tutorial: convert DWG to PDF in Java with Aspose.CAD'
og_title: แปลง DWG เป็น PDF ใน Java ด้วย Aspose.CAD
schemas:
- author: Aspose
  dateModified: '2026-10-19'
  description: Learn how to convert DWG to PDF in Java with Aspose.CAD. This step‑by‑step
    guide shows you how to export AutoCAD PDF, save CAD as PDF, and apply a license.
  headline: Convert DWG to PDF in Java using Aspose.CAD
  type: TechArticle
- description: Learn how to convert DWG to PDF in Java with Aspose.CAD. This step‑by‑step
    guide shows you how to export AutoCAD PDF, save CAD as PDF, and apply a license.
  name: Convert DWG to PDF in Java using Aspose.CAD
  steps:
  - name: set the resource directory path
    text: Replace `"Your Document Directory"` with the absolute path to the folder
      you created in the prerequisites. > **Pro tip:** Use `Paths.get(...).toAbsolutePath()`
      to avoid path‑related errors on different operating systems.
  - name: load the CAD image
    text: Loading the CAD file into an `Image` object gives you full access to Aspose.CAD’s
      rasterization engine. The `Image` class loads the DWG file and prepares it for
      conversion. > **Why this matters:** Once the drawing is in memory, you can query
      its layouts, layers, and metadata before rasterizing.
  - name: set rasterization options
    text: Adjust `pageWidth` and `pageHeight` to **customize PDF page size**. Enabling
      `setTypeOfEntities(TypeOfEntities.Entities3D)` allows full 3‑D rendering when
      needed. The `RasterizationOptions` object controls DPI, page dimensions, and
      entity types for the output. - `pageWidth` / `pageHeight` are measur
  - name: configure PDF options
    text: Tie the rasterization settings to the PDF output, ensuring the vector data
      is correctly transformed. The `PdfOptions` class links the rasterization configuration
      with the final PDF file.
  - name: save the PDF
    text: The resulting file, `Export3DImagestoPDF_out_.pdf`, is a **save cad as pdf**
      representation of your original AutoCAD drawing. The `save` method writes the
      rasterized image to a PDF file on disk.
  type: HowTo
- questions:
  - answer: Yes – the library supports DWG, DXF, DWF, DGN, and over 30 additional
      formats, giving you flexibility across projects.
    question: Can I use Aspose.CAD for Java with other CAD file formats?
  - answer: Visit the [temporary license page](https://purchase.aspose.com/temporary-license/)
      to request a time‑limited license for evaluation.
    question: How do I obtain a temporary license for Aspose.CAD for Java?
  - answer: Absolutely. Use `setLayouts("Model")`, `setLayouts("Layout1")`, etc.,
      to choose which view is rendered into the PDF.
    question: Are there layout options for rasterization?
  - answer: Yes – modify `pageWidth` and `pageHeight` in the rasterization options
      to match any required page dimensions.
    question: Can I change the size of the output PDF file?
  - answer: The dedicated community is available at the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19)
      where you can ask questions and share solutions.
    question: Where can I get help if I run into problems?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- dwg to pdf
- aspose.cad
- java cad conversion
- export autocad pdf
title: แปลง DWG เป็น PDF ใน Java ด้วย Aspose.CAD
url: /th/java/cad-export-options/export-autocad-images-to-pdf/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ส่งออก AutoCAD PDF – ส่งออกภาพ AutoCAD เป็น PDF ด้วย Aspose.CAD for Java

## บทนำ

หากคุณต้องการ **แปลง DWG เป็น PDF ใน Java** คุณมาถูกที่แล้ว บทแนะนำนี้จะแสดงวิธีส่งออกภาพ AutoCAD เป็น PDF ด้วย Aspose.CAD for Java ซึ่งเป็นไลบรารี pure‑Java ที่จัดการกับ DWG, DXF, DWF และรูปแบบ CAD อื่น ๆ อีกหลายรูปแบบโดยไม่ต้องพึ่งพาไลบรารีเนทีฟ เมื่อเสร็จสิ้นคุณจะสามารถ **บันทึก CAD เป็น PDF** ปรับแต่งตัวเลือกการเรสเตอร์ไลเซชันเช่นขนาดหน้า และใช้ **Aspose CAD license** อย่างถูกต้องสำหรับการใช้งานในผลิตภัณฑ์

## คำตอบอย่างรวดเร็ว
- **ฉันสามารถแปลง DWG เป็น PDF ด้วย Java ได้หรือไม่?** ใช่ – Aspose.CAD for Java รองรับ DWG, DXF และหลายสิบรูปแบบ CAD อื่น ๆ โดยเนทีฟ  
- **ฉันต้องการไลเซนส์หรือไม่?** ไลเซนส์ **Aspose CAD license** ถาวรจะลบข้อจำกัดการประเมินทั้งหมด; ไลเซนส์ชั่วคราวพร้อมให้ใช้สำหรับการทดสอบ  
- **เวอร์ชัน Java ไหนที่รองรับ?** Java 8 และสูงกว่าได้รับการสนับสนุนเต็มรูปแบบ  
- **ฉันสามารถควบคุมขนาดหน้ากระดาษ PDF ได้หรือไม่?** แน่นอน – ตั้งค่า `pageWidth` และ `pageHeight` ในตัวเลือกการเรสเตอร์ไลเซชัน  
- **การเรนเดอร์ 3‑D เป็นไปได้หรือไม่?** ใช่ – เปิดใช้งาน `TypeOfEntities.Entities3D` เพื่อเรสเตอร์ไลซ์เอนทิตี 3‑D  

## การส่งออก AutoCAD PDF คืออะไร?
การส่งออก AutoCAD PDF คือกระบวนการแปลงภาพวาด CAD เวกเตอร์ให้เป็นเอกสาร PDF พกพา ซึ่งจะคงรักษาชั้น, ความหนาของเส้น, สี และอาจรวมถึงเรขาคณิต 3‑D ทำให้สามารถแชร์แบบออกแบบกับลูกค้า หรือเก็บเป็นเอกสารโดยไม่ต้องใช้ซอฟต์แวร์ CAD

## ทำไมต้องแปลง DWG เป็น PDF ด้วย Aspose.CAD for Java?
Aspose.CAD รองรับ **50+ input and output formats** ประมวลผลภาพวาดหลายร้อยหน้าโดยไม่ต้องโหลดไฟล์ทั้งหมดเข้าสู่หน่วยความจำ และทำงานบนแพลตฟอร์มใด ๆ ที่รองรับ Java 8+ ไลบรารีให้คุณควบคุม DPI, ขนาดหน้า, และเลย์เอาต์อย่างเต็มที่ เพื่อให้คุณ **customize PDF page size** ให้ตรงกับสเปคโครงการโดยไม่ต้องติดตั้ง DLL เนทีฟ

## ข้อกำหนดเบื้องต้น

- **Java Development Kit** – JDK 8 หรือใหม่กว่า ติดตั้งบนเครื่องของคุณ  
- **Aspose.CAD for Java** – ดาวน์โหลด JAR ล่าสุดจาก [download link](https://releases.aspose.com/cad/java/)  
- **Working directory** – โฟลเดอร์ที่ไฟล์ DWG ต้นฉบับและ PDF ที่สร้างขึ้นจะถูกเก็บไว้  

## นำเข้าเนมสเปซ

คลาส `Image` แทนภาพ CAD ที่สามารถเรสเตอร์ไลซ์ได้ ส่วน `RasterizationOptions` และ `PdfOptions` ให้คุณปรับแต่งการแปลงอย่างละเอียด

คลาส `Image` เป็นอ็อบเจ็กต์ระดับบนของ Aspose.CAD ที่เก็บภาพวาด CAD ในหน่วยความจำ  
คลาส `RasterizationOptions` กำหนดวิธีการเรสเตอร์ไลซ์ข้อมูลเวกเตอร์ก่อนเขียนเป็น PDF  
คลาส `PdfOptions` รวมการตั้งค่าการเรสเตอร์ไลซ์กับพารามิเตอร์การส่งออก PDF  

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

ตอนนี้เราจะเดินผ่านโค้ดทีละขั้นตอน

## วิธีแปลง DWG เป็น PDF ด้วย Aspose.CAD for Java?

เพื่อแปลงไฟล์ DWG เป็น PDF ด้วย Aspose.CAD for Java ให้โหลดภาพวาดโดยใช้คลาส Image ตั้งค่า CadRasterizationOptions (เช่น DPI, ขนาดหน้า, ประเภทเอนทิตี) ห่ออ็อบเจ็กต์เหล่านั้นใน PdfOptions แล้วเรียกเมธอด save พร้อมระบุชื่อไฟล์ .pdf ลำดับนี้ทำให้ข้อมูลเวกเตอร์ถูกเรสเตอร์ไลซ์อย่างถูกต้องและ PDF ที่ได้ตรงกับการจัดวางที่คุณต้องการ

### ขั้นตอนที่ 1: ตั้งค่าพาธไดเรกทอรีทรัพยากร

แทนที่ `"Your Document Directory"` ด้วยพาธเต็มของโฟลเดอร์ที่คุณสร้างตามข้อกำหนดเบื้องต้น  

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
```

> **เคล็ดลับ:** ใช้ `Paths.get(...).toAbsolutePath()` เพื่อหลีกเลี่ยงข้อผิดพลาดที่เกี่ยวกับพาธบนระบบปฏิบัติการต่าง ๆ  

### ขั้นตอนที่ 2: โหลดภาพ CAD

การโหลดไฟล์ CAD ลงในอ็อบเจ็กต์ `Image` ให้คุณเข้าถึงเอนจินการเรสเตอร์ไลซ์ของ Aspose.CAD อย่างเต็มที่  

คลาส `Image` โหลดไฟล์ DWG และเตรียมพร้อมสำหรับการแปลง  

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

> **ทำไมเรื่องนี้สำคัญ:** เมื่อภาพวาดอยู่ในหน่วยความจำ คุณสามารถสอบถามเลย์เอาต์, ชั้น, และเมตาดาต้าก่อนทำการเรสเตอร์ไลซ์  

### ขั้นตอนที่ 3: ตั้งค่าตัวเลือกการเรสเตอร์ไลเซชัน

ปรับ `pageWidth` และ `pageHeight` เพื่อ **customize PDF page size** การเปิดใช้งาน `setTypeOfEntities(TypeOfEntities.Entities3D)` จะทำให้เรนเดอร์ 3‑D อย่างเต็มที่เมื่อจำเป็น  

อ็อบเจ็กต์ `RasterizationOptions` ควบคุม DPI, ขนาดหน้า, และประเภทเอนทิตีสำหรับผลลัพธ์  

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setPageHeight(500);
// rasterizationOptions.setTypeOfEntities(TypeOfEntities.Entities3D);

rasterizationOptions.setLayouts(new String[] {"Model"});
```

- `pageWidth` / `pageHeight` มีหน่วยเป็นพอยต์ (1 pt = 1/72 in)  
- ยกเลิกคอมเมนต์บรรทัด `setTypeOfEntities` เพื่อทำการเรสเตอร์ไลซ์ 3‑D  
- `setLayouts` เลือกเลย์เอาต์ที่ต้องการ (Model, Layout1, ฯลฯ) เพื่อเรนเดอร์  

### ขั้นตอนที่ 4: ตั้งค่าตัวเลือก PDF

เชื่อมการตั้งค่าการเรสเตอร์ไลซ์กับผลลัพธ์ PDF เพื่อให้ข้อมูลเวกเตอร์ถูกแปลงอย่างถูกต้อง  

คลาส `PdfOptions` เชื่อมการกำหนดค่าการเรสเตอร์ไลซ์กับไฟล์ PDF สุดท้าย  

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### ขั้นตอนที่ 5: บันทึก PDF

ไฟล์ที่ได้ `Export3DImagestoPDF_out_.pdf` เป็นการ **save cad as pdf** ของภาพวาด AutoCAD ดั้งเดิมของคุณ  

เมธอด `save` เขียนภาพที่เรสเตอร์ไลซ์ลงไฟล์ PDF บนดิสก์  

```java
cadImage.save(dataDir + "Export3DImagestoPDF_out_.pdf", pdfOptions);
```

## ปัญหาทั่วไปและวิธีแก้

| อาการ | สาเหตุที่เป็นไปได้ | วิธีแก้ |
|---------|--------------|-----|
| PDF ว่างเปล่า | ตัวเลือกการเรสเตอร์ไลเซชันไม่ได้ตั้งค่า หรือเลย์เอาต์ไม่ตรงกัน | ตรวจสอบว่า `setLayouts` ตรงกับชื่อเลย์เอาต์ในไฟล์ CAD ของคุณ |
| ภาพความละเอียดต่ำ | `pageWidth`/`pageHeight` เล็กเกินไป | เพิ่มขนาดหรือกำหนด DPI สูงขึ้นโดยใช้ `rasterizationOptions.setResolution(...)` |
| ข้อยกเว้นไลเซนส์ | ไม่ได้ใช้ไลเซนส์ที่ถูกต้อง | ใช้ **Aspose CAD license** หรือใช้ไลเซนส์ชั่วคราวสำหรับการทดสอบ |

## คำถามที่พบบ่อย

**Q: ฉันสามารถใช้ Aspose.CAD for Java กับรูปแบบไฟล์ CAD อื่นได้หรือไม่?**  
A: ใช่ – ไลบรารีรองรับ DWG, DXF, DWF, DGN, และรูปแบบเพิ่มเติมกว่า 30 รูปแบบ ให้ความยืดหยุ่นในหลายโครงการ  

**Q: ฉันจะขอรับไลเซนส์ชั่วคราวสำหรับ Aspose.CAD for Java ได้อย่างไร?**  
A: เยี่ยมชม [temporary license page](https://purchase.aspose.com/temporary-license/) เพื่อขอไลเซนส์แบบจำกัดเวลาเพื่อการประเมิน  

**Q: มีตัวเลือกเลย์เอาต์สำหรับการเรสเตอร์ไลเซชันหรือไม่?**  
A: แน่นอน ใช้ `setLayouts("Model")`, `setLayouts("Layout1")` ฯลฯ เพื่อเลือกมุมมองที่ต้องการเรนเดอร์เป็น PDF  

**Q: ฉันสามารถเปลี่ยนขนาดไฟล์ PDF ที่ได้ได้หรือไม่?**  
A: ใช่ – ปรับ `pageWidth` และ `pageHeight` ในตัวเลือกการเรสเตอร์ไลเซชันให้ตรงกับขนาดหน้าที่ต้องการ  

**Q: จะหาแหล่งช่วยเหลือเมื่อเจอปัญหาได้จากที่ไหน?**  
A: ชุมชนเฉพาะด้านพร้อมให้บริการที่ [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) คุณสามารถถามคำถามและแชร์วิธีแก้ได้  

---

**อัปเดตล่าสุด:** 2026-10-19  
**ทดสอบด้วย:** Aspose.CAD for Java 24.10  
**ผู้เขียน:** Aspose

## บทแนะนำที่เกี่ยวข้อง

- [ส่งออก DWG เป็น PDF ใน Java – ตั้งค่าขนาดหน้ากระดาษ PDF ด้วย Aspose.CAD](/cad/java/cad-export-options/export-to-pdf/)
- [ส่งออก DWG เป็น PDF: เลย์เอาต์เฉพาะโดยใช้ Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [ส่งออก DWG เป็น PDF และเปิดใช้งานการติดตามด้วย Aspose.CAD Java](/cad/java/additional-features/enable-tracking/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}