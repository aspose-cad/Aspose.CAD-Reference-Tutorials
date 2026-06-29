---
date: 2026-06-29
description: เรียนรู้วิธีสร้าง PDF จาก DWG และปรับแต่งเค้าโครง PDF ด้วย Aspose.CAD
  for Java. การบูรณาการที่ง่ายสำหรับนักพัฒนา Java.
keywords:
- create pdf from dwg
- convert cad to pdf
- pdf different page sizes
- export dwg to pdf
- customize pdf layout
linktitle: PDF เดียวกับเค้าโครงที่แตกต่างกัน
schemas:
- author: Aspose
  dateModified: '2026-06-29'
  description: Learn how to create PDF from DWG and customize PDF layout using Aspose.CAD
    for Java. Easy integration for Java developers.
  headline: Create PDF from DWG with Aspose.CAD for Java
  type: TechArticle
- questions:
  - answer: Yes, Aspose.CAD for Java integrates seamlessly with libraries such as
      Apache POI, Jackson, or Spring Boot.
    question: Can I use Aspose.CAD for Java with other Java libraries?
  - answer: Absolutely! You can access a free trial version [here](https://releases.aspose.com/).
    question: Is there a trial version available?
  - answer: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for community
      support and discussions.
    question: Where can I find additional support?
  - answer: You can obtain a temporary license [here](https://purchase.aspose.com/temporary-license/).
    question: How do I obtain a temporary license?
  - answer: Purchase the full version of Aspose.CAD for Java [here](https://purchase.aspose.com/buy).
    question: Where can I purchase the full version?
  type: FAQPage
second_title: Aspose.CAD Java API
title: สร้าง PDF จาก DWG ด้วย Aspose.CAD for Java
url: /th/java/other-cad-operations/single-pdf-different-layouts/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# สร้าง PDF จาก DWG ด้วย Aspose.CAD สำหรับ Java

## บทนำ

ในบทแนะนำนี้คุณจะ **create PDF from DWG** ไฟล์และใช้เค้าโครงหลายขนาดหน้าโดยใช้ Aspose.CAD สำหรับ Java ไม่ว่าคุณจะต้องการสร้างแบบแปลนการก่อสร้าง, แผนผังวิศวกรรม, หรือ PDF ที่พร้อมสำหรับการตลาด ขั้นตอนต่อไปนี้จะแสดงวิธีแปลงภาพวาด CAD เป็น PDF, ปรับแต่งขนาดของแต่ละเค้าโครง, และสร้างเอกสารหลายหน้าเป็นไฟล์เดียว — ทั้งหมดโดยไม่ต้องออกจากสภาพแวดล้อม Java ของคุณ.

## คำตอบอย่างรวดเร็ว
- **What does the tutorial cover?** การแปลงภาพวาด DWG เป็น PDF เดียวที่มีหลายขนาดหน้า.  
- **Which library is required?** Aspose.CAD for Java (latest version).  
- **Do I need a license?** การทดลองใช้ฟรีทำงานได้สำหรับการพัฒนา; จำเป็นต้องมีใบอนุญาตเชิงพาณิชย์สำหรับการใช้งานจริง.  
- **Can I export other formats?** ใช่ – API ยังรองรับการส่งออกเป็น PNG, JPEG, และ SVG.  
- **Is Java 8 sufficient?** ไลบรารีทำงานได้กับ Java 8 และรันไทม์ที่ใหม่กว่า.

## “create pdf from dwg” คืออะไร?

**Create PDF from DWG** หมายถึงการแปลงไฟล์ AutoCAD DWG ดั้งเดิมเป็นเอกสาร PDF พร้อมคงความแม่นยำของเวกเตอร์, ชั้น, และความหนาของเส้น, และอนุญาตให้ปรับแต่งเค้าโครงได้. Aspose.CAD ทำการแปลงนี้ทั้งหมดในหน่วยความจำ, ดังนั้นไม่จำเป็นต้องใช้ซอฟต์แวร์ CAD ภายนอก, และ PDF ที่ได้สามารถแก้ไขหรือพิมพ์ได้โดยตรง.

## ทำไมต้องปรับแต่งเค้าโครง PDF จาก DWG?

Aspose.CAD รองรับ **30+ รูปแบบ CAD** และสามารถสร้าง PDF ได้ถึง **500 MB** โดยไม่ต้องโหลดไฟล์ทั้งหมดเข้าสู่หน่วยความจำ. โดยการกำหนดขนาดหน้าต่างๆ สำหรับแต่ละเค้าโครง, คุณสามารถสร้างแผ่นพิมพ์ที่ตรงกับมาตรฐาน ISO, ANSI, หรือขนาดที่กำหนดเอง – ประโยชน์ที่วัดได้ซึ่งช่วยประหยัดเวลาและขจัดการประมวลผลหลังจากการแปลงด้วยตนเอง.

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเริ่มการเดินทางนี้, โปรดตรวจสอบว่าคุณมีข้อกำหนดต่อไปนี้พร้อมแล้ว:
- Java Environment: ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง Java บนเครื่องของคุณ.  
- Aspose.CAD Library: ดาวน์โหลดและติดตั้งไลบรารี Aspose.CAD สำหรับ Java จาก [download link](https://releases.aspose.com/cad/java/).  
- Document Directory: ตั้งค่าไดเรกทอรีสำหรับไฟล์ DWG ของคุณ.

## นำเข้าแพ็กเกจ

คลาส `CadImage` เป็นอ็อบเจ็กต์หลักของ Aspose.CAD ที่แสดงภาพวาด CAD ในหน่วยความจำ. นำเข้าชื่อเนมสเปซที่จำเป็นก่อนเริ่มทำงาน:

```java
import com.aspose.cad.Image;
import com.aspose.cad.SizeF;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.VectorRasterizationOptions;
```

## ขั้นตอนที่ 1: โหลดภาพวาด CAD

`CadImage` โหลดไฟล์ DWG และให้เข้าถึงข้อมูลเวกเตอร์ของมัน. เริ่มต้นโดยโหลดภาพวาด CAD ของคุณเข้าสู่วัตถุ `CadImage`:

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
CadImage cadImage = (CadImage)Image.load(dataDir + "City skyway map.dwg");
```

## ขั้นตอนที่ 2: กำหนดค่าตัวเลือกการเรสเตอร์ไลเซชัน

`RasterizationOptions` กำหนดวิธีการแปลงเวกเตอร์ CAD เป็นภาพราสเตอร์ก่อนนำไปใส่ใน PDF. ตั้งค่าตัวเลือกการเรสเตอร์ไลเซชันสำหรับภาพ CAD:

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1000);
rasterizationOptions.setPageHeight(1000);
```

## ขั้นตอนที่ 3: ปรับขนาดหน้าของเค้าโครง

`PdfOptions` ให้คุณกำหนดขนาดหน้าที่แตกต่างกันสำหรับแต่ละเค้าโครงภายใน DWG. กำหนดขนาดที่กำหนดเองสำหรับหลายเค้าโครงในภาพวาด CAD:

```java
rasterizationOptions.getLayoutPageSizes().addItem("ANSI C Plot", new SizeF(500, 1000));
rasterizationOptions.getLayoutPageSizes().addItem("8.5 x 11 Plot", new SizeF(1000, 100));
```

## ขั้นตอนที่ 4: ตั้งค่าตัวเลือก PDF

`PdfOptions` เป็นคอนเทนเนอร์ที่รวมการตั้งค่าการเรสเตอร์ไลเซชันและการกำหนดเค้าโครง. ตั้งค่าตัวเลือก PDF โดยรวมการตั้งค่าการเรสเตอร์ไลเซชัน:

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## ขั้นตอนที่ 5: บันทึกเป็น PDF

`PdfSaveOptions` สรุปการแปลงและเขียนไฟล์ผลลัพธ์. บันทึกภาพ CAD ที่ประมวลผลเป็น PDF:

```java
cadImage.save(dataDir + "singlePDF_out.pdf", pdfOptions);
```

ยินดีด้วย! คุณได้ทำการ **create pdf from dwg** สำเร็จด้วยขนาดหน้าต่างๆ โดยใช้ Aspose.CAD สำหรับ Java.

## ปัญหาที่พบบ่อยและวิธีแก้

- **Blank pages in the output PDF** – ตรวจสอบให้ค่า `PageSize` ตรงกับขนาดเค้าโครงจริงในไฟล์ DWG.  
- **Memory‑out errors on large drawings** – ใช้ `CadImage.load(..., LoadOptions)` กับ `LoadOptions.setLoadMode(LoadMode.Memory)` เพื่อสตรีมไฟล์แทนการโหลดทั้งหมด.  
- **Incorrect scaling** – ปรับ `RasterizationOptions.setPageWidth` และ `setPageHeight` ให้ตรงกับ DPI ที่ต้องการ (จุดต่อหนึ่งนิ้ว).

## คำถามที่พบบ่อย

**Q: ฉันสามารถใช้ Aspose.CAD สำหรับ Java ร่วมกับไลบรารี Java อื่นได้หรือไม่?**  
**A:** ใช่, Aspose.CAD สำหรับ Java ผสานรวมอย่างราบรื่นกับไลบรารีเช่น Apache POI, Jackson, หรือ Spring Boot.

**Q: มีเวอร์ชันทดลองใช้งานหรือไม่?**  
**A:** แน่นอน! คุณสามารถเข้าถึงเวอร์ชันทดลองฟรีได้ [ที่นี่](https://releases.aspose.com/).

**Q: ฉันจะหาแหล่งสนับสนุนเพิ่มเติมได้จากที่ไหน?**  
**A:** เยี่ยมชม [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) เพื่อรับการสนับสนุนจากชุมชนและการสนทนา.

**Q: ฉันจะขอรับใบอนุญาตชั่วคราวได้อย่างไร?**  
**A:** คุณสามารถรับใบอนุญาตชั่วคราวได้ [ที่นี่](https://purchase.aspose.com/temporary-license/).

**Q: ฉันจะซื้อเวอร์ชันเต็มได้จากที่ไหน?**  
**A:** ซื้อเวอร์ชันเต็มของ Aspose.CAD สำหรับ Java [ที่นี่](https://purchase.aspose.com/buy).

---

**อัปเดตล่าสุด:** 2026-06-29  
**ทดสอบกับ:** Aspose.CAD for Java 24.10  
**ผู้เขียน:** Aspose

## บทแนะนำที่เกี่ยวข้อง

- [ส่งออก DWG เป็น PDF หรือ Raster ด้วย Aspose.CAD สำหรับ Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [ส่งออกเค้าโครง CAD เป็น PDF ด้วย Aspose.CAD สำหรับ Java](/cad/java/cad-export-options/export-cad-layouts-to-pdf/)
- [ส่งออกเค้าโครง DWG เฉพาะเป็น PDF ด้วย Aspose.CAD สำหรับ Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< blocks/products/products-backtop-button >}}
{{< /blocks/products/pf/main-wrap-class >}}