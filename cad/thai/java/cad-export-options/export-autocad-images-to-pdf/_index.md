---
date: 2026-10-19
description: เรียนรู้วิธีส่งออกแบบร่าง AutoCAD ไปเป็น PDF ด้วยขนาดหน้ากระดาษ PDF แบบกำหนดเองโดยใช้
  Aspose.CAD for Java คู่มือขั้นตอนต่อขั้นตอนนี้ครอบคลุมการแปลง DWG to PDF, ตัวเลือก
  rasterization, และ licensing
keywords:
- custom pdf page size
- export autocad to pdf
- save cad as pdf
- generate pdf from dwg
- dwg to pdf java
lastmod: 2026-10-19
linktitle: ส่งออกภาพ AutoCAD เป็น PDF
og_description: ตั้งค่าขนาดหน้ากระดาษ PDF แบบกำหนดเองเมื่อส่งออกแบบร่าง AutoCAD ไปเป็น
  PDF โดยใช้ Aspose.CAD for Java เรียนรู้การแปลง DWG to PDF, การตั้งค่า rasterization,
  และ licensing ในไม่กี่นาที
og_image_alt: Guide showing how to export AutoCAD drawings to PDF with custom page
  dimensions using Aspose.CAD for Java
og_title: ตั้งค่าขนาดหน้ากระดาษ PDF แบบกำหนดเองสำหรับการส่งออก AutoCAD ด้วย Aspose.CAD
schemas:
- author: Aspose
  dateModified: '2026-10-19'
  description: Learn how to export AutoCAD drawings to PDF with a custom PDF page
    size using Aspose.CAD for Java. This step‑by‑step guide covers converting DWG
    to PDF, rasterization options, and licensing.
  headline: Set custom PDF page size for AutoCAD export with Aspose.CAD
  type: TechArticle
- description: Learn how to export AutoCAD drawings to PDF with a custom PDF page
    size using Aspose.CAD for Java. This step‑by‑step guide covers converting DWG
    to PDF, rasterization options, and licensing.
  name: Set custom PDF page size for AutoCAD export with Aspose.CAD
  steps:
  - name: set the resource directory path
    text: '> **Pro tip:** Replace `"Your Document Directory"` with the absolute path
      to the folder you created in the prerequisites.'
  - name: load the CAD image
    text: The `Image` class loads the CAD file and gives you access to Aspose.CAD’s
      rasterization engine. > **Why this matters:** Once the CAD file is loaded, you
      can manipulate rasterization options before rendering to PDF.
  - name: set rasterization options
    text: The `CadRasterizationOptions` class specifies how the CAD drawing is rasterized
      before being saved as PDF. Adjust `pageWidth` and `pageHeight` to define a **custom
      PDF page size**. You can also enable 3‑D rendering by uncommenting the `setTypeOfEntities`
      line. - `pageWidth` / `pageHeight` – measured
  - name: configure PDF options
    text: The `PdfOptions` class holds PDF‑specific settings and links the rasterization
      options to the output file, ensuring the custom page dimensions are applied
      correctly.
  - name: save the PDF
    text: The `save` method writes the rendered image to the specified PDF file. The
      resulting file, `Export3DImagestoPDF_out_.pdf`, is a **save cad as pdf** representation
      of your original AutoCAD drawing with the exact page dimensions you specified.
  type: HowTo
- questions:
  - answer: Yes, the library supports DWG, DXF, DWF, DGN, and many more, giving you
      flexibility across projects.
    question: Can I use Aspose.CAD for Java with other CAD file formats?
  - answer: Visit the [temporary license page](https://purchase.aspose.com/temporary-license/)
      to request a time‑limited license for evaluation.
    question: How do I obtain a temporary license for Aspose.CAD for Java?
  - answer: Absolutely. Use `setLayouts("Model")` or specify other layout names to
      control which view is rendered.
    question: Are there layout options for rasterization?
  - answer: Yes – modify `pageWidth` and `pageHeight` in the rasterization options
      to any dimensions you need.
    question: Can I customize the size of the output PDF file?
  - answer: The dedicated [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) offers
      community support and official responses from the Aspose team.
    question: Where can I get help or discuss issues related to Aspose.CAD for Java?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- custom pdf page size
- Aspose.CAD
- Java CAD conversion
- PDF generation
- DWG export
title: ตั้งค่าขนาดหน้ากระดาษ PDF แบบกำหนดเองสำหรับการส่งออก AutoCAD ด้วย Aspose.CAD
url: /th/java/cad-export-options/export-autocad-images-to-pdf/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ส่งออก AutoCAD PDF - ส่งออกภาพ AutoCAD เป็น PDF ด้วย Aspose.CAD for Java

## บทนำ

หากคุณต้องการ **แปลง DWG เป็น PDF** และควบคุมขนาดที่แน่นอนของไฟล์ผลลัพธ์ คุณมาถูกที่แล้ว คู่มือนี้จะแสดงวิธีตั้ง **ขนาดหน้ PDF แบบกำหนดเอง** ขณะส่งออกภาพ AutoCAD เป็น PDF ด้วย Aspose.CAD for Java เมื่อคุณอ่านจนจบ คุณจะรู้วิธีโหลดไฟล์ DWG, กำหนดค่าตัวเลือกการเรสเตอร์ไลซ์เช่น DPI และความกว้าง/ความสูงของหน้า, ใช้ไลเซนส์, และสร้าง PDF ที่พร้อมสำหรับการผลิต

## คำตอบด่วน

- **ฉันสามารถแปลง DWG เป็น PDF ด้วย Java ได้หรือไม่?** ใช่ – Aspose.CAD for Java รองรับ DWG, DXF, DWF และรูปแบบ CAD อื่น ๆ อย่างเนทีฟ  
- **ฉันต้องการไลเซนส์สำหรับการใช้งานในผลิตภัณฑ์หรือไม่?** ไลเซนส์ Aspose.CAD เต็มรูปแบบจะลบข้อจำกัดการประเมินทั้งหมด; มีไลเซนส์ชั่วคราวสำหรับการทดสอบ  
- **เวอร์ชัน Java ใดที่เข้ากันได้?** ไลบรารีทำงานกับ Java 8 และ JDK เวอร์ชันถัดไปทั้งหมด  
- **ฉันจะเปลี่ยนขนาดหน้าของ PDF ได้อย่างไร?** ตั้งค่า `pageWidth` และ `pageHeight` บน `PdfOptions.getRasterizationOptions()` ให้เป็นขนาดที่คุณต้องการ  
- **การเรนเดอร์ 3‑D รองรับหรือไม่?** ใช่ – เปิดใช้งาน `TypeOfEntities.Entities3D` เพื่อเรสเตอร์ไลซ์เอนทิตี 3‑D  

## Export AutoCAD PDF คืออะไร?

การส่งออก AutoCAD PDF หมายถึงการแปลงภาพวาด CAD แบบเวกเตอร์ (DWG, DXF, DWF ฯลฯ) ให้เป็นเอกสาร PDF พกพา พร้อมคงรักษาชั้น, ความหนาของเส้น, และเรขาคณิต 3‑D ทางเลือก ซึ่งช่วยให้คุณสามารถแชร์แบบออกแบบกับลูกค้า, เก็บถาวรภาพวาด, หรือพิมพ์โดยไม่ต้องติดตั้งซอฟต์แวร์ CAD

## ทำไมต้องใช้ Aspose.CAD for Java เพื่อแปลง DWG เป็น PDF?

Aspose.CAD for Java เหมาะอย่างยิ่งสำหรับการแปลง DWG เป็น PDF เนื่องจากให้การสนับสนุนรูปแบบที่กว้างขวาง, ทำงานบน Java บริสุทธิ์โดยไม่มีการพึ่งพาเนทีฟ, ให้การเรสเตอร์ไลซ์ความละเอียดสูงพร้อมการควบคุม DPI และขนาดหน้าอย่างเต็มที่, และมีระบบไลเซนส์ที่ยืดหยุ่นซึ่งทำให้คุณเริ่มต้นด้วยรุ่นทดลองและขยายไปสู่การผลิตได้

- **การครอบคลุมรูปแบบที่กว้างขวาง** – รองรับรูปแบบเข้าและออกกว่า 50 รูปแบบ รวมถึง DWG, DXF, DWF, DGN, และ PDF.  
- **การนำไปใช้ด้วย Java บริสุทธิ์** – ไม่มี DLL เนทีฟหรือการพึ่งพาภายนอก ทำให้การปรับใช้บนแพลตฟอร์มใดก็ง่ายดาย  
- **การเรสเตอร์ไลซ์ความละเอียดสูง** – คุณสามารถกำหนด DPI, ขนาดหน้า, และเลย์เอาต์, ให้คุณควบคุม **ขนาดหน้ PDF แบบกำหนดเอง** ของผลลัพธ์ได้อย่างเต็มที่  
- **ไลเซนส์ที่ขยายได้** – เริ่มต้นด้วยรุ่นทดลองฟรี, จากนั้นอัปเกรดเป็น **ไลเซนส์ Aspose CAD** ถาวร  

## ข้อกำหนดเบื้องต้น

- **Java Development Kit** – JDK 8 หรือใหม่กว่า ติดตั้งบนเครื่องของคุณ  
- **Aspose.CAD for Java** – ดาวน์โหลด JAR ล่าสุดจาก [download link](https://releases.aspose.com/cad/java/).  
- **Working directory** – โฟลเดอร์ที่บรรจุไฟล์ DWG ต้นฉบับและจะรับไฟล์ PDF ที่สร้างขึ้น  

## นำเข้าเนมสเปซ

`Image` class คืออ็อบเจ็กต์หลักของ Aspose.CAD ที่แสดงภาพวาด CAD ในหน่วยความจำ นำเข้าแพ็กเกจที่จำเป็นก่อนเริ่มเขียนโค้ด

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

ตอนนี้เรามาเดินผ่านโค้ดทีละขั้นตอนกัน

## วิธีตั้งขนาดหน้ PDF แบบกำหนดเองเมื่อส่งออก DWG เป็น PDF?

โหลดไฟล์ DWG ของคุณ, กำหนดความกว้างและความสูงของหน้าที่ต้องการ, แล้วบันทึกผลลัพธ์เป็น PDF – นั่นคือทั้งหมดที่คุณต้องการเพื่อสร้าง PDF ที่มีขนาดหน้ากำหนดเอง ขั้นตอนต่อไปนี้จะแสดงลำดับที่แน่นอนและโค้ดขั้นต่ำที่จำเป็น

### ขั้นตอนที่ 1: ตั้งค่าพาธไดเรกทอรีทรัพยากร

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
```

> **เคล็ดลับ:** แทนที่ `"Your Document Directory"` ด้วยพาธเต็มของโฟลเดอร์ที่คุณสร้างในข้อกำหนดเบื้องต้น.

### ขั้นตอนที่ 2: โหลดภาพ CAD

`Image` class โหลดไฟล์ CAD และให้คุณเข้าถึงเอนจินการเรสเตอร์ไลซ์ของ Aspose.CAD

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

> **ทำไมเรื่องนี้สำคัญ:** เมื่อไฟล์ CAD ถูกโหลดแล้ว คุณสามารถปรับตัวเลือกการเรสเตอร์ไลซ์ก่อนทำการเรนเดอร์เป็น PDF

### ขั้นตอนที่ 3: ตั้งค่าตัวเลือกการเรสเตอร์ไลซ์

`CadRasterizationOptions` class ระบุวิธีการเรสเตอร์ไลซ์ภาพวาด CAD ก่อนบันทึกเป็น PDF ปรับ `pageWidth` และ `pageHeight` เพื่อกำหนด **ขนาดหน้ PDF แบบกำหนดเอง** คุณยังสามารถเปิดการเรนเดอร์ 3‑D ได้โดยการยกเลิกคอมเมนต์บรรทัด `setTypeOfEntities`

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setPageHeight(500);
// rasterizationOptions.setTypeOfEntities(TypeOfEntities.Entities3D);

rasterizationOptions.setLayouts(new String[] {"Model"});
```

- `pageWidth` / `pageHeight` – วัดเป็นพิกเซล; เปลี่ยนค่าตามขนาด A4, Letter, หรือขนาดกำหนดเองใด ๆ  
- `setTypeOfEntities(TypeOfEntities.Entities3D)` – เรนเดอร์เอนทิตี 3‑D เมื่อจำเป็น  
- `setLayouts` – เลือกเลย์เอาต์ (Model, Layout1, ฯลฯ) ที่จะทำการเรสเตอร์ไลซ์  

### ขั้นตอนที่ 4: กำหนดค่า PDF options

`PdfOptions` class เก็บการตั้งค่าเฉพาะ PDF และเชื่อมตัวเลือกการเรสเตอร์ไลซ์กับไฟล์ผลลัพธ์ เพื่อให้แน่ใจว่าขนาดหน้าที่กำหนดเองถูกนำไปใช้อย่างถูกต้อง

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### ขั้นตอนที่ 5: บันทึก PDF

เมธอด `save` จะเขียนภาพที่เรสเตอร์ไลซ์ลงในไฟล์ PDF ที่ระบุ

```java
cadImage.save(dataDir + "Export3DImagestoPDF_out_.pdf", pdfOptions);
```

ไฟล์ที่ได้, `Export3DImagestoPDF_out_.pdf`, เป็นการแสดงผล **save cad as pdf** ของภาพวาด AutoCAD ดั้งเดิมของคุณพร้อมขนาดหน้าที่คุณระบุอย่างแม่นยำ

## ปัญหาทั่วไป & วิธีแก้

| อาการ | สาเหตุที่เป็นไปได้ | วิธีแก้ |
|---------|--------------|-----|
| PDF ว่าง | ตัวเลือกการเรสเตอร์ไลซ์ไม่ได้ตั้งค่า หรือเลย์เอาต์ไม่ตรงกัน | ตรวจสอบว่า `setLayouts` ตรงกับชื่อเลย์เอาต์ในไฟล์ CAD ของคุณ. |
| ภาพความละเอียดต่ำ | `pageWidth`/`pageHeight` เล็กเกินไปหรือ DPI ต่ำ | เพิ่มขนาดหรือเรียก `rasterizationOptions.setResolution(...)` ด้วย DPI ที่สูงขึ้น. |
| ข้อยกเว้นไลเซนส์ | ไม่มีไลเซนส์ที่ถูกต้องถูกนำไปใช้ | ใช้ไลเซนส์ Aspose.CAD ถาวรหรือใช้ไลเซนส์ชั่วคราวสำหรับการทดสอบ. |

## คำถามที่พบบ่อย

**ถาม: ฉันสามารถใช้ Aspose.CAD for Java กับรูปแบบไฟล์ CAD อื่น ๆ ได้หรือไม่?**  
**ตอบ:** ใช่, ไลบรารีรองรับ DWG, DXF, DWF, DGN และอื่น ๆ อีกมากมาย, ให้ความยืดหยุ่นในการทำงานหลายโครงการ  

**ถาม: ฉันจะขอไลเซนส์ชั่วคราวสำหรับ Aspose.CAD for Java ได้อย่างไร?**  
**ตอบ:** เยี่ยมชม [temporary license page](https://purchase.aspose.com/temporary-license/) เพื่อขอไลเซนส์ที่มีระยะเวลาจำกัดสำหรับการประเมิน  

**ถาม: มีตัวเลือกเลย์เอาต์สำหรับการเรสเตอร์ไลซ์หรือไม่?**  
**ตอบ:** มีแน่นอน ใช้ `setLayouts("Model")` หรือระบุชื่อเลย์เอาต์อื่นเพื่อควบคุมว่ามุมมองใดจะถูกเรนเดอร์  

**ถาม: ฉันสามารถปรับขนาดไฟล์ PDF ผลลัพธ์ได้หรือไม่?**  
**ตอบ:** ใช่ – ปรับ `pageWidth` และ `pageHeight` ในตัวเลือกการเรสเตอร์ไลซ์ให้เป็นขนาดที่คุณต้องการ  

**ถาม: ฉันจะหาแนวทางช่วยเหลือหรือหารือเกี่ยวกับปัญหา Aspose.CAD for Java ได้จากที่ไหน?**  
**ตอบ:** ฟอรั่ม [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) ให้การสนับสนุนจากชุมชนและการตอบจากทีม Aspose อย่างเป็นทางการ  

## FAQ เพิ่มเติม (รูปแบบเป็นมิตรกับ AI)

**ถาม: Aspose.CAD ต้องการไลบรารีเนทีฟบน Windows หรือ Linux หรือไม่?**  
**ตอบ:** ไม่. Aspose.CAD for Java เป็นไลบรารี Java บริสุทธิ์ จึงทำงานบนแพลตฟอร์มใดก็ได้ที่รองรับ JDK โดยไม่มี DLL เนทีฟเพิ่มเติม  

**ถาม: ไลบรารีสามารถประมวลผลไฟล์ DWG ขนาดเท่าใด?**  
**ตอบ:** ไลบรารีสามารถจัดการภาพวาดหลายร้อยหน้า (สูงสุด 500 MB) โดยไม่ต้องโหลดไฟล์ทั้งหมดเข้าสู่หน่วยความจำ เนื่องจากสถาปัตยกรรมสตรีมมิง  

**ถาม: สามารถแปลงไฟล์ DWG จำนวนหลายไฟล์เป็น PDF เป็นชุดได้หรือไม่?**  
**ตอบ:** ได้. วนลูปผ่านไดเรกทอรี, โหลดแต่ละไฟล์ด้วย `Image.load()`, ใช้ตัวเลือกการเรสเตอร์ไลซ์เดียวกัน, แล้วเรียก `save()` สำหรับ PDF แต่ละไฟล์  

**ถาม: ฉันคาดหวังประสิทธิภาพอย่างไรบนเซิร์ฟเวอร์ทั่วไป?**  
**ตอบ:** การแปลง DWG 100 หน้า ที่ 300 DPI บน CPU 2.5 GHz ปกติใช้เวลาประมาณ 12 วินาที ตามการทดสอบเบนช์มาร์คของ Aspose  

**ถาม: ไลบรารีคงข้อมูลชั้นใน PDF ไว้หรือไม่?**  
**ตอบ:** แม้ว่าผลลัพธ์จะเป็นการเรสเตอร์ไลซ์ แต่ลักษณะการแสดงผลของชั้น, ความหนาของเส้น, และสีจะถูกทำซ้ำอย่างแม่นยำ  

---

**อัปเดตล่าสุด:** 2026-10-19  
**ทดสอบด้วย:** Aspose.CAD for Java 24.10  
**ผู้เขียน:** Aspose

## บทแนะนำที่เกี่ยวข้อง

- [ส่งออก DWG เป็น PDF และเปิดใช้งานการติดตามด้วย Aspose.CAD Java](/cad/java/additional-features/enable-tracking/)
- [ส่งออก DWG เป็น PDF: เลย์เอาต์เฉพาะโดยใช้ Aspose.CAD Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [ส่งออก DWG เป็น BMP และปรับขนาด CAD ด้วยประเภทหน่วยโดยใช้ Aspose.CAD for Java](/cad/java/cad-file-manipulation/adjusting-cad-drawing-size-using-unit-type/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}