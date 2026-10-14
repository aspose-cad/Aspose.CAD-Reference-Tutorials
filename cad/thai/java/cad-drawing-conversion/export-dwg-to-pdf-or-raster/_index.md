---
date: 2026-10-14
description: เรียนรู้วิธีที่ Java CAD library Aspose.CAD for Java สามารถส่งออก DWG
  ไปเป็น PDF หรือภาพแรสเตอร์ได้อย่างรวดเร็วและแม่นยำ
keywords:
- export dwg pdf
- high quality pdf
- dwg to pdf tutorial
- aspose cad java
- java cad library
lastmod: 2026-10-14
linktitle: ส่งออก DWG PDF และภาพแรสเตอร์
og_description: ส่งออก DWG PDF อย่างรวดเร็วด้วย Aspose.CAD for Java. เรียนรู้การแปลง
  PDF คุณภาพสูง, ตัวเลือกแรสเตอร์, และการให้ลิขสิทธิ์ในคู่มือขั้นตอนต่อขั้นตอนนี้
og_image_alt: Tutorial showing Java code to convert DWG drawings to PDF and raster
  formats with Aspose.CAD
og_title: ส่งออก DWG PDF และภาพแรสเตอร์โดยใช้ Java CAD library Aspose.CAD
schemas:
- author: Aspose
  dateModified: '2026-10-14'
  description: Learn how the Java CAD library Aspose.CAD for Java can export DWG to
    PDF or raster images quickly and accurately.
  headline: Export DWG PDF and raster images using Java CAD library Aspose.CAD
  type: TechArticle
- description: Learn how the Java CAD library Aspose.CAD for Java can export DWG to
    PDF or raster images quickly and accurately.
  name: Export DWG PDF and raster images using Java CAD library Aspose.CAD
  steps:
  - name: Load the DWG file
    text: First, load your DWG drawing using the `Image` class. This creates an in‑memory
      representation that Aspose.CAD can work with.
  - name: Determine unit type
    text: Understanding whether the drawing uses metric or imperial units is essential
      for correct scaling. The helper method `IsMetric` (implementation omitted for
      brevity) returns a boolean flag.
  - name: Set rasterization options
    text: The `CadRasterizationOptions` class defines rasterization parameters such
      as DPI, page size, and unit conversion. Based on the unit system, configure
      page size, scaling, and the target unit type. These options drive how the DWG
      is rasterized before being wrapped into a PDF.
  - name: Configure PDF options (pdf options cad)
    text: The `PdfOptions` class specifies PDF‑specific settings, including compression
      and metadata. Create a `PdfOptions` instance and attach the rasterization settings.
      This tells Aspose.CAD how to embed the rasterized content into the final PDF.
  - name: Save as PDF
    text: The `save` method writes the image to the given file path using the supplied
      options. Finally, export the drawing to a PDF file. The `save` method takes
      the output path and the configured `PdfOptions`. When the code finishes, you’ll
      find **Saved.pdf** in your `DWGDrawings` folder, ready for distribu
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD for Java seamlessly integrates with popular Java frameworks
      such as Spring, Jakarta EE, and Android.
    question: Can I use Aspose.CAD for Java with other Java frameworks?
  - answer: Yes, you can obtain a temporary license **[obtain a temporary license](https://purchase.aspose.com/temporary-license/)**.
    question: Is a temporary license available for Aspose.CAD for Java?
  - answer: Visit the **[Aspose.CAD forum](https://forum.aspose.com/c/cad/19)** for
      assistance from the community and Aspose engineers.
    question: Where can I find support for Aspose.CAD for Java?
  - answer: You can purchase a license **[purchase a license](https://purchase.aspose.com/buy)**.
    question: How can I purchase a license for Aspose.CAD for Java?
  - answer: Aspose.CAD for Java supports both metric and imperial units, automatically
      detecting the drawing’s unit system.
    question: What units does Aspose.CAD for Java support?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- export dwg
- aspose.cad
- java cad conversion
title: ส่งออก DWG PDF และภาพแรสเตอร์โดยใช้ Java CAD library Aspose.CAD
url: /th/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ส่งออก DWG PDF และภาพเรสเตอร์โดยใช้ไลบรารี Java CAD Aspose.CAD

## บทนำ

การส่งออก DWG เป็น PDF เป็นความต้องการที่พบบ่อยสำหรับวิศวกร สถาปนิก และผู้ที่ต้องการแชร์แบบ CAD โดยไม่เปิดเผยรูปแบบไฟล์ดั้งเดิม ด้วย **Aspose.CAD for Java** คุณสามารถ **export dwg pdf** — หรือภาพเรสเตอร์ — ได้ด้วยเพียงไม่กี่บรรทัดของโค้ด Java โดยคงความแม่นยำของเวกเตอร์และการจัดวาง การสอนนี้จะพาคุณผ่านขั้นตอนการโหลดไฟล์ DWG การกำหนดค่าการเรสเตอร์ไลซ์ และการบันทึกผลลัพธ์เป็น PDF หรือภาพคุณภาพสูง คุณจะได้เห็นว่าทำไม Aspose.CAD จึงเป็นไลบรารี Java CAD ที่ได้รับความนิยมสำหรับการแปลงที่เชื่อถือได้และข้ามแพลตฟอร์ม

สำหรับคู่มือที่มุ่งเน้นการแปลงเป็น PDF เท่านั้น ดูที่ [Export DWG to PDF tutorial](/java/cad-drawing-conversion/export-dwg-to-pdf/).

## คำตอบเร็ว
- **บทเรียนนี้ครอบคลุมอะไร?** Exporting DWG files to PDF or raster images using Aspose.CAD for Java.  
- **ฉันต้องการไลเซนส์หรือไม่?** A free temporary license is available for evaluation; a full license is required for production.  
- **เวอร์ชัน Java ที่รองรับคืออะไร?** Any Java 8+ runtime works with the latest Aspose.CAD Java API.  
- **ฉันสามารถแปลง DWG ไปเป็นรูปแบบภาพอื่นได้หรือไม่?** Yes – the same rasterization options let you output PNG, JPEG, BMP, etc.  
- **การแปลงใช้เวลานานเท่าไหร่?** Typically under a second for standard drawings; larger files may take a few seconds.

## ทำไมไลบรารี Java CAD จึงเป็นตัวเลือกที่ดีที่สุดสำหรับการแปลง DWG?

Aspose.CAD for Java เป็นตัวเลือกที่ดีที่สุดเพราะให้การทำงานแบบ pure‑Java ที่ไม่ต้องอาศัย DLL เนทีฟ ตรวจจับหน่วยเมตริกหรืออิมพีเรียลโดยอัตโนมัติ ให้ผลลัพธ์เรสเตอร์ที่ความละเอียดสูงสุดถึง 1200 DPI และสร้าง PDF ที่คงเวกเตอร์ไว้โดยไม่มีการพึ่งพาไลบรารีภายนอก ไลบรารียังมีโมเดลไลเซนส์ที่ยืดหยุ่นให้คุณเริ่มต้นด้วยไลเซนส์ชั่วคราวและขยายไปสู่การใช้งานระดับองค์กรได้

## “export dwg to pdf” คืออะไร?

`Export dwg pdf` คือกระบวนการแปลงไฟล์แบบ DWG ดั้งเดิมให้เป็นเอกสาร PDF พร้อมคงข้อมูลเวกเตอร์ ชั้น และสเกล การแปลงนี้สร้างไฟล์ที่อิสระต่ออุปกรณ์ซึ่งสามารถดูได้บนทุกแพลตฟอร์มโดยไม่ต้องใช้ AutoCAD เนื่องจาก PDF รักษาข้อมูลเวกเตอร์ ข้อความจึงสามารถค้นหาได้และกราฟิกคมชัดที่ระดับการซูมใด ๆ ทำให้เหมาะสำหรับเอกสาร การตรวจสอบโดยลูกค้า และการเก็บรักษาในระยะยาว

## ทำไมต้องใช้ Aspose.CAD Java สำหรับการแปลงนี้?

คุณควรใช้ Aspose.CAD Java เพราะไลบรารีจัดการการแปลงหน่วย การเรสเตอร์ไลซ์ และการฝัง PDF ภายในโดยอัตโนมัติ ไม่ต้องพึ่งพาเครื่องมือของบุคคลที่สามหรือไพพ์ไลน์บรรทัดคำสั่งที่ซับซ้อน API ของมันออกแบบมาสำหรับนักพัฒนา: วัตถุ `Image` ตัวเดียวแทนแบบร่าง และอ็อบเจกต์การกำหนดค่าจำนวนไม่กี่ตัวช่วยให้คุณปรับ DPI ขนาดหน้าและการบีบอัดได้อย่างละเอียด ผลลัพธ์คือการส่งออกที่สม่ำเสมอและทำซ้ำได้บน Windows, Linux และ macOS

## ข้อกำหนดเบื้องต้น

ก่อนเริ่มเขียนโค้ด ตรวจสอบให้คุณมี:

- ความรู้พื้นฐานเกี่ยวกับการเขียนโปรแกรม Java.  
- Aspose.CAD for Java library installed. If you haven’t downloaded it yet, get it **[download Aspose.CAD for Java](https://releases.aspose.com/cad/java/)**.  
- ไฟล์ DWG สำหรับการทดสอบ – ตัวอย่าง **Bottom_plate.dwg** จะถูกใช้ในคู่มือนี้.  

## นำเข้าเนมสเปซ

ในโปรเจกต์ Java ของคุณ ให้นำเข้าคลาสที่จำเป็นเพื่อเริ่มต้นการแปลง:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.UnitType;
```

## คู่มือทีละขั้นตอน

### ขั้นตอน 1: โหลดไฟล์ DWG

แรกเริ่ม โหลดแบบร่าง DWG ของคุณโดยใช้คลาส `Image` ซึ่งจะสร้างการแสดงผลในหน่วยความจำที่ Aspose.CAD สามารถทำงานได้

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Bottom_plate.dwg";
Image objImage = Image.load(srcFile);
```

### ขั้นตอน 2: กำหนดประเภทหน่วย

การเข้าใจว่าแบบร่างใช้หน่วยเมตริกหรืออิมพีเรียลเป็นสิ่งสำคัญสำหรับการสเกลที่ถูกต้อง วิธีช่วย `IsMetric` (การทำงานถูกละเว้นเพื่อความกระชับ) จะคืนค่า boolean

```java
Boolean currentUnitIsMetric = IsMetric(objImage.getUnitType());
int currentUnitCoefficient = objImage.getUnitType();
```

### ขั้นตอน 3: ตั้งค่าตัวเลือกการเรสเตอร์ไลซ์

คลาส `CadRasterizationOptions` กำหนดพารามิเตอร์การเรสเตอร์ไลซ์ เช่น DPI, ขนาดหน้า, และการแปลงหน่วย ตามระบบหน่วยที่ใช้ ให้ตั้งค่าขนาดหน้า, การสเกล, และประเภทหน่วยเป้าหมาย ตัวเลือกเหล่านี้กำหนดวิธีที่ DWG จะถูกเรสเตอร์ไลซ์ก่อนบรรจุเป็น PDF

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();

if (currentUnitIsMetric) {
    // Metric units
    double metersCoeff = 1 / 1000.0;
    double scaleFactor = metersCoeff / currentUnitCoefficient;
    rasterizationOptions.setPageWidth((float)(210 * scaleFactor));
    rasterizationOptions.setPageHeight((float)(297 * scaleFactor));
    rasterizationOptions.setUnitType(UnitType.Millimeter);
} else {
    // Imperial units
    rasterizationOptions.setPageWidth((float)(8.27f / currentUnitCoefficient));
    rasterizationOptions.setPageHeight((float)(11.69f / currentUnitCoefficient));
    rasterizationOptions.setUnitType(UnitType.Inch);
}
```

### ขั้นตอน 4: ตั้งค่าตัวเลือก PDF (pdf options cad)

คลาส `PdfOptions` ระบุการตั้งค่าเฉพาะ PDF รวมถึงการบีบอัดและเมตาดาต้า สร้างอินสแตนซ์ `PdfOptions` แล้วผูกกับการตั้งค่าการเรสเตอร์ไลซ์ นี้บอก Aspose.CAD ว่าจะฝังเนื้อหาเรสเตอร์ไลซ์ลงใน PDF สุดท้ายอย่างไร

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());
```

### ขั้นตอน 5: บันทึกเป็น PDF

เมธอด `save` จะเขียนภาพไปยังเส้นทางไฟล์ที่ระบุโดยใช้ตัวเลือกที่กำหนดไว้ สุดท้ายให้ส่งออกแบบร่างเป็นไฟล์ PDF เมธอด `save` รับพาธเอาต์พุตและ `PdfOptions` ที่กำหนดไว้

```java
objImage.save(dataDir + "Saved.pdf", pdfOptions);
```

เมื่อโค้ดทำงานเสร็จ คุณจะพบ **Saved.pdf** ในโฟลเดอร์ `DWGDrawings` ของคุณ พร้อมสำหรับการแจกจ่ายหรือเก็บรักษา

## วิธีแปลงภาพเรสเตอร์ DWG ด้วยไลบรารี Java CAD?

คุณสามารถแปลง DWG ไปเป็นรูปแบบเรสเตอร์โดยเปลี่ยน `PdfOptions` เป็นคลาสตัวเลือกเรสเตอร์เฉพาะเช่น `PngOptions` หรือ `JpegOptions` ใช้ `CadRasterizationOptions` เดิม ปรับรูปแบบเอาต์พุต แล้วเรียกเมธอด `save` ด้วยอ็อบเจกต์ตัวเลือกใหม่ วิธีนี้ทำให้คุณสร้างไฟล์ PNG, JPEG, BMP หรือ TIFF ได้ด้วยการเปลี่ยนบรรทัดเดียวเดียวกัน

## วิธีสร้าง PDF DWG ด้วย PDF options CAD?

ตัวอย่างข้างต้นได้ **generates pdf dwg** แล้ว หากต้องการปรับขนาด PDF ให้เปิดการบีบอัดโดยเรียก `pdfOptions.setCompress(true)` คุณยังสามารถฝังเมตาดาต้ากำหนดเวอร์ชัน PDF หรือเพิ่มการป้องกันด้วยรหัสผ่านผ่านคุณสมบัติ `PdfOptions` เพิ่มเติม การปรับแต่งเหล่านี้ให้คุณควบคุม PDF สุดท้ายได้อย่างเต็มที่โดยไม่ต้องออกจากโค้ด Java

## ปัญหาที่พบบ่อยและเคล็ดลับ

- **Incorrect page size** – ตรวจสอบตรรกะการแปลงหน่วยอีกครั้ง; ค่าสัมประสิทธิ์ที่ไม่ตรงกันอาจทำให้หน้ามีขนาดใหญ่เกินไป.  
- **Missing fonts or lineweights** – ตรวจสอบให้แน่ใจว่า DWG อ้างอิงทรัพยากรภายนอกทั้งหมดก่อนทำการแปลง.  
- **Performance on large drawings** – เพิ่มค่าการตั้งค่า `DPI` ใน `CadRasterizationOptions` เฉพาะเมื่อจำเป็นต้องการคุณภาพสูง; ลด DPI จะช่วยเร่งการประมวลผล.  
- **License concerns** – สำหรับการประเมินคุณสามารถใช้ **temporary license Aspose**; จำเป็นต้องมีไลเซนส์เต็มสำหรับการใช้งานในสภาพแวดล้อมการผลิต.

## คำถามที่พบบ่อย

**Q: Can I use Aspose.CAD for Java with other Java frameworks?**  
A: Yes, Aspose.CAD for Java seamlessly integrates with popular Java frameworks such as Spring, Jakarta EE, and Android.

**Q: Is a temporary license available for Aspose.CAD for Java?**  
A: Yes, you can obtain a temporary license **[obtain a temporary license](https://purchase.aspose.com/temporary-license/)**.

**Q: Where can I find support for Aspose.CAD for Java?**  
A: Visit the **[Aspose.CAD forum](https://forum.aspose.com/c/cad/19)** for assistance from the community and Aspose engineers.

**Q: How can I purchase a license for Aspose.CAD for Java?**  
A: You can purchase a license **[purchase a license](https://purchase.aspose.com/buy)**.

**Q: What units does Aspose.CAD for Java support?**  
A: Aspose.CAD for Java supports both metric and imperial units, automatically detecting the drawing’s unit system.

**Q: Can I convert DWG to other image formats (e.g., PNG, JPEG) using the same API?**  
A: Absolutely. Replace `PdfOptions` with the appropriate raster image options (e.g., `PngOptions`) and reuse the same `CadRasterizationOptions`.

## สรุป

บทเรียนนี้ได้สาธิตวิธี **export dwg pdf** และภาพเรสเตอร์โดยใช้ **java cad library** Aspose.CAD for Java โดยทำตามคู่มือทีละขั้นตอน คุณสามารถผสานการแปลง CAD ที่เชื่อถือได้เข้าไปในแอปพลิเคชัน Java ใดก็ได้ ไม่ว่าจะต้องการ PDF สำหรับเอกสารหรือภาพเรสเตอร์สำหรับแสดงบนเว็บ ไลบรารีที่เป็น pure‑Java, ผลลัพธ์คุณภาพสูง, และโมเดลไลเซนส์ที่ยืดหยุ่นทำให้เป็นตัวเลือกที่มั่นคงสำหรับเครื่องมือขนาดเล็กและโครงการระดับองค์กร

---

**อัปเดตล่าสุด:** 2026-10-14  
**ทดสอบกับ:** Aspose.CAD for Java 24.10  
**ผู้เขียน:** Aspose

## บทแนะนำที่เกี่ยวข้อง

- [Export DWG to PDF: Specific Layout Using Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [Export DWG to PDF in Java – Set PDF Page Size with Aspose.CAD](/cad/java/cad-export-options/export-to-pdf/)
- [Export DWG to PDF with Hidden Lines – Aspose.CAD for Java](/cad/java/cad-text-and-formatting/support-hidden-lines-in-dwg/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}