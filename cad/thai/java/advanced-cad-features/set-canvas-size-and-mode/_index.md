---
date: 2026-08-29
description: เรียนรู้วิธีตั้งค่าขนาดหน้ากระดาษ pdf และแปลง CAD เป็น PDF ด้วย Aspose.CAD
  สำหรับ Java พร้อมการปรับสเกลเลย์เอาต์อัตโนมัติและการส่งออกเป็น TIFF
keywords:
- set pdf page size
- convert cad to pdf
- canvas size java
- high resolution tiff
- change pdf dimensions
lastmod: 2026-08-29
linktitle: ตั้งค่าขนาดหน้ากระดาษ pdf – แปลง cad เป็น pdf
og_description: เรียนรู้วิธีตั้งค่าขนาดหน้ากระดาษ pdf ขณะแปลงภาพวาด CAD เป็น PDF ใน
  Java ด้วย Aspose.CAD คู่มือนี้ครอบคลุม canvas dimensions, automatic layout scaling,
  และการส่งออกเป็น high‑resolution TIFF
og_image_alt: Tutorial showing how to set pdf page size and convert CAD to PDF in
  Java
og_title: ตั้งค่าขนาดหน้ากระดาษ pdf – แปลง CAD เป็น PDF ด้วย Aspose ใน Java
schemas:
- author: Aspose
  dateModified: '2026-08-29'
  description: Learn how to set pdf page size and convert CAD to PDF using Aspose.CAD
    for Java, with automatic layout scaling and TIFF export.
  headline: Set pdf page size – convert cad to pdf (Java)
  type: TechArticle
- questions:
  - answer: No. Canvas size controls page dimensions; vector data remains resolution‑independent,
      ensuring crisp rendering at any zoom level.
    question: does the canvas size affect vector quality in the PDF?
  - answer: Yes. Adjust `rasterizationOptions.setResolution(dpiValue)` before creating
      `TiffOptions`.
    question: can I set a different DPI for the TIFF output?
  - answer: Use Aspose.PDF to load the generated PDF and call `pdf.getPages().setPageSize(PageSize.A4)`
      or a custom size.
    question: how can I change PDF dimensions for an existing PDF without re‑rendering
      the CAD?
  - answer: Keep `setAutomaticLayoutsScaling(true)` and avoid `setNoScaling(true)`;
      this retains layer visibility and layout fidelity.
    question: what is the best way to convert dxf to pdf while preserving layers?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- set pdf page size
- convert cad
- Aspose.CAD
- Java
- high resolution tiff
title: ตั้งค่าขนาดหน้ากระดาษ pdf – แปลง cad เป็น pdf (Java)
url: /th/java/advanced-cad-features/set-canvas-size-and-mode/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# กำหนดขนาดหน้ PDF – แปลง CAD เป็น PDF (Java)

## บทนำ

หากคุณต้องการ **set pdf page size** ขณะแปลงภาพวาด CAD เป็น PDF คุณมาถูกที่แล้ว ในบทเรียนนี้เราจะแสดงวิธีใช้ Aspose.CAD for Java เพื่อกำหนดขนาดแคนวาสอย่างแม่นยำ เปิดใช้งานการปรับสเกลเลย์เอาต์อัตโนมัติ แล้วส่งออกผลลัพธ์เป็นทั้ง PDF และ TIFF ไม่ว่าคุณจะเตรียมแผนผังวิศวกรรมสำหรับการพิมพ์หรือสร้างภาพย่อสำหรับแกลเลอรีเว็บ การควบคุมขนาดหน้าและความละเอียดของผลลัพธ์เป็นสิ่งสำคัญ

## คำตอบเร็ว
- **หมายความว่า “convert CAD to PDF” คืออะไร?** การแปลงภาพวาด CAD (เช่น DXF, DWG) ให้เป็นเอกสาร PDF ที่สามารถดูได้บนทุกแพลตฟอร์ม.  
- **ฉันสามารถส่งออกเป็น TIFF ได้หรือไม่?** ได้—ใช้ `TiffOptions` เพื่อสร้างภาพเรสเตอร์ความละเอียดสูง.  
- **ตัวเลือกใดที่ควบคุมขนาดแคนวาสใน Java?** `CadRasterizationOptions.setPageWidth/Height`.  
- **การปรับสเกลเลย์เอาต์อัตโนมัติคืออะไร?** เป็นแฟล็ก (`setAutomaticLayoutsScaling(true)`) ที่รักษาสัดส่วนของเลย์เอาต์เดิมเมื่อขนาดแคนวาสเปลี่ยนแปลง.  
- **ฉันต้องการไลเซนส์สำหรับ Aspose.CAD หรือไม่?** จำเป็นต้องมีไลเซนส์ชั่วคราวหรือถาวรสำหรับการใช้งานในผลิตภัณฑ์.

## วิธีตั้งขนาดหน้ PDF ขณะแปลง CAD เป็น PDF ใน Java

โหลดไฟล์ CAD ของคุณ, กำหนดค่า `CadRasterizationOptions` ด้วยความกว้างและความสูงที่ต้องการ, เปิดใช้งานการปรับสเกลเลย์เอาต์อัตโนมัติ, แล้วบันทึกผลลัพธ์เป็น PDF วิธีการสองขั้นตอนนี้ทำให้คุณควบคุมขนาดที่แน่นอนของหน้าผลลัพธ์โดยไม่สูญเสียคุณภาพเวกเตอร์

## convert CAD to PDF คืออะไร?

การแปลง CAD เป็น PDF หมายถึงการนำภาพวาดวิศวกรรมแบบเวกเตอร์มาสร้างเป็นหน้าต่าง PDF โดยคงรักษาเส้น, ชั้น, และรูปทรงไว้ขณะทำให้ไฟล์เข้าถึงได้ทั่วโลก กระบวนการจะเรสเตอร์ภาพวาดตามตัวเลือกที่กำหนด ทำให้ได้ PDF ที่สามารถเปิดได้บนอุปกรณ์ใดก็ได้โดยไม่ต้องใช้ซอฟต์แวร์ CAD และยังคงความแม่นยำของการออกแบบต้นฉบับ

## ทำไมต้องตั้งขนาดแคนวาสใน Java?

การตั้งค่าขนาดแคนวาสใน Java ช่วยให้คุณกำหนดความละเอียดของผลลัพธ์และขนาดหน้า ทำให้ PDF หรือ TIFF ที่ได้ตรงกับความต้องการการพิมพ์หรือการแสดงผลของคุณ นอกจากนี้ยังให้คุณควบคุมพฤติกรรมการสเกล ซึ่งสำคัญสำหรับภาพวาดขนาดใหญ่

## ข้อกำหนดเบื้องต้น

ก่อนเริ่มบทเรียน โปรดตรวจสอบว่าคุณมีข้อกำหนดต่อไปนี้พร้อมใช้งาน:

- Aspose.CAD for Java: ตรวจสอบว่าคุณได้ติดตั้งไลบรารี Aspose.CAD ในสภาพแวดล้อม Java ของคุณแล้ว คุณสามารถดาวน์โหลดไลบรารี Aspose.CAD for Java ได้จาก [here](https://releases.aspose.com/cad/java/).
- Document directory: ตั้งค่าไดเรกทอรีเอกสารเพื่อเก็บไฟล์ CAD ของคุณ ไดเรกทอรีนี้จะถูกอ้างอิงในขั้นตอนของบทเรียน

ตอนนี้เรามาเริ่มต้นกับคู่มือแบบขั้นตอนกันเลย

## นำเข้าเนมสเปซ

ในขั้นตอนนี้ เราจะนำเข้าเนมสเปซที่จำเป็นเพื่อเริ่มต้นโครงการ Aspose.CAD ของคุณ

`Image` คือคลาสหลักที่ใช้โหลดไฟล์ CAD

```java
import java.awt.Image;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## ขั้นตอนที่ 1: นำเข้าคลาส Aspose.CAD

คลาส `Image` มีเมธอดสำหรับโหลดและบันทึกภาพวาด CAD

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
com.aspose.cad.Image objImage = com.aspose.cad.Image.load(srcFile);
```

ในโค้ดนี้ เราตั้งค่าเส้นทางไปยังไดเรกทอรีทรัพยากรและโหลดไฟล์ DXF ด้วยคลาส `Image` ของ Aspose.CAD

## ขั้นตอนที่ 2: ตั้งค่าคุณสมบัติ CadRasterizationOptions (set canvas size java)

`CadRasterizationOptions` ระบุการตั้งค่าการเรสเตอร์ เช่น ขนาดหน้าและการสเกลสำหรับการแปลง CAD เป็นเรสเตอร์

```java
// Create an instance of CadRasterizationOptions and set its various properties
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

ที่นี่ เราสร้างอินสแตนซ์ของ `CadRasterizationOptions` และกำหนดค่าคุณสมบัติต่าง ๆ เช่น ความกว้างหน้า, ความสูงหน้า, และ **automatic layout scaling** นี่คือหัวใจของ **configure canvas mode** สำหรับการแปลงของคุณ

## ขั้นตอนที่ 3: สร้าง PdfOptions และตั้งค่า vectorRasterizationOptions

`PdfOptions` กำหนดการตั้งค่าการส่งออก PDF สำหรับการแปลง

```java
// Create an instance of PdfOptions
PdfOptions pdfOptions = new PdfOptions();

// Set the VectorRasterizationOptions property
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

ต่อไป เราสร้างอินสแตนซ์ของ `PdfOptions` และตั้งค่าคุณสมบัติ `VectorRasterizationOptions` ของมันให้เป็น `CadRasterizationOptions` ที่กำหนดไว้ก่อนหน้า

## ขั้นตอนที่ 4: ส่งออกเป็น PDF (convert CAD to PDF)

```java
// Export CAD to PDF
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

สุดท้าย เราบันทึกภาพ CAD เป็นไฟล์ PDF ด้วยตัวเลือกที่ระบุ ทำให้กระบวนการ **convert CAD to PDF** เสร็จสมบูรณ์

## ขั้นตอนที่ 5: สร้าง TiffOptions และตั้งค่า vectorRasterizationOptions (export CAD to TIFF)

`TiffOptions` กำหนดพารามิเตอร์การส่งออก TIFF เช่น การบีบอัดและความละเอียด

```java
// Create an instance of TiffOptions
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);

// Set the VectorRasterizationOptions property
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## ขั้นตอนที่ 6: ส่งออกเป็น TIFF

```java
// Export CAD to TIFF
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

สุดท้าย เราบันทึกภาพ CAD เป็นไฟล์ TIFF ด้วยตัวเลือกที่ระบุ แสดงวิธี **export CAD to TIFF** หลังจากตั้งค่าขนาดแคนวาส

## ปัญหาทั่วไปและวิธีแก้

| ปัญหา | สาเหตุ | วิธีแก้ |
|-------|-------|-----|
| PDF ที่ส่งออกเป็นไฟล์เปล่า | `setNoScaling(true)` ปิดการเรนเดอร์สำหรับบางภาพวาด | ลบ `setNoScaling(true)` หรือตั้งค่าเป็น `false`. |
| ความละเอียดของ TIFF ดูต่ำ | ความกว้าง/ความสูงของหน้าเล็กเกินไป | เพิ่มค่าของ `setPageWidth` / `setPageHeight`. |
| เลย์เอาต์ดูบิดเบี้ยว | การปรับสเกลเลย์เอาต์อัตโนมัติถูกปิด | ตรวจสอบว่าได้เปิด `setAutomaticLayoutsScaling(true)` |

## ทำไมต้องปรับขนาดแคนวาสและ DPI?

การเปลี่ยนขนาดแคนวาสมีผลโดยตรงต่อความละเอียดการเรสเตอร์ของผลลัพธ์ หากคุณต้องการ **increase TIFF resolution** เพียงเพิ่มค่าของ `setPageWidth` / `setPageHeight` หรือเรียก `rasterizationOptions.setResolution(300)` ก่อนสร้าง `TiffOptions` จะทำให้คุณได้ภาพเรสเตอร์คุณภาพสูงที่เหมาะสำหรับการพิมพ์หรือการตรวจสอบรายละเอียด

## คำถามที่พบบ่อย

**Q1: ฉันสามารถใช้ Aspose.CAD for Java กับเฟรมเวิร์ก Java อื่น ๆ ได้หรือไม่?**  
A: ใช่, Aspose.CAD ถูกออกแบบให้ผสานรวมกับเฟรมเวิร์ก Java ต่าง ๆ อย่างราบรื่น  

**Q2: มีไลเซนส์ชั่วคราวสำหรับ Aspose.CAD หรือไม่?**  
A: มี, คุณสามารถรับไลเซนส์ชั่วคราวได้จากหน้า [here](https://purchase.aspose.com/temporary-license/).  

**Q3: ฉันจะหาแหล่งสนับสนุนจากชุมชนสำหรับ Aspose.CAD ได้จากที่ไหน?**  
A: เยี่ยมชมฟอรั่ม Aspose.CAD ที่ [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) เพื่อรับการสนับสนุนและการสนทนาจากชุมชน.  

**Q4: ฉันสามารถลอง Aspose.CAD ฟรีได้หรือไม่?**  
A: แน่นอน! ดาวน์โหลดรุ่นทดลองฟรีได้จากหน้า [here](https://releases.aspose.com/).  

**Q5: ฉันจะซื้อ Aspose.CAD for Java ได้อย่างไร?**  
A: ซื้อ Aspose.CAD for Java ได้จาก [here](https://purchase.aspose.com/buy).  

**Q: ขนาดแคนวาสมีผลต่อคุณภาพเวกเตอร์ใน PDF หรือไม่?**  
A: ไม่. ขนาดแคนวาสควบคุมมิติของหน้า; ข้อมูลเวกเตอร์ยังคงเป็นอิสระจากความละเอียด ทำให้การเรนเดอร์คมชัดที่ระดับการซูมใด ๆ  

**Q: ฉันสามารถตั้งค่า DPI ที่แตกต่างสำหรับการส่งออก TIFF ได้หรือไม่?**  
A: ได้. ปรับ `rasterizationOptions.setResolution(dpiValue)` ก่อนสร้าง `TiffOptions`.  

**Q: ฉันจะเปลี่ยนขนาด PDF ของไฟล์ที่มีอยู่แล้วโดยไม่ต้องเรนเดอร์ CAD ใหม่ได้อย่างไร?**  
A: ใช้ Aspose.PDF โหลด PDF ที่สร้างแล้วและเรียก `pdf.getPages().setPageSize(PageSize.A4)` หรือขนาดที่กำหนดเอง  

**Q: วิธีที่ดีที่สุดในการแปลง dxf เป็น pdf พร้อมคงเลเยอร์คืออะไร?**  
A: รักษา `setAutomaticLayoutsScaling(true)` และหลีกเลี่ยง `setNoScaling(true)`; จะทำให้มองเห็นเลเยอร์และรักษาความถูกต้องของเลย์เอาต์  

## สรุป

ขอแสดงความยินดี! คุณได้ทำการ **convert CAD to PDF** และ **export CAD to TIFF** สำเร็จพร้อมกับ **set canvas size java**, เปิดใช้งาน **automatic layout scaling**, และเรียนรู้วิธี **configure canvas mode** เพื่อให้ได้ผลลัพธ์คุณภาพสูง บทเรียนนี้เป็นพื้นฐานที่มั่นคงสำหรับโครงการแปลง CAD ของคุณ ค้นพบคุณลักษณะและความเป็นไปได้เพิ่มเติมใน [Aspose.CAD documentation](https://reference.aspose.com/cad/java/).

---

**อัปเดตล่าสุด:** 2026-08-29  
**ทดสอบด้วย:** Aspose.CAD for Java 24.12  
**ผู้เขียน:** Aspose

## บทเรียนที่เกี่ยวข้อง

- [ตั้งขนาดแคนวาส – คุณลักษณะ CAD ขั้นสูงกับ Aspose.CAD for Java](/cad/java/advanced-cad-features/)
- [ส่งออก DWG เป็น PDF ใน Java – ตั้งขนาดหน้ PDF ด้วย Aspose.CAD](/cad/java/cad-export-options/export-to-pdf/)
- [ตั้งขนาดหน้ากำหนดเอง – PDF จาก CAD ด้วย Auto Layout Scaling](/cad/java/advanced-cad-features/setting-auto-layout-scaling/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}