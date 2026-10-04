---
date: 2026-10-04
description: เรียนรู้วิธีแปลง dwg เป็น png อย่างรวดเร็วและส่งออก cad เป็น png หรือรูปแบบเรสเตอร์อื่น
  ๆ ด้วย Aspose.CAD for Java รับผลลัพธ์คุณภาพสูงได้อย่างเร็ว
keywords:
- convert dwg to png
- dwg to raster image
- convert cad to pdf
- export cad as png
- convert dwg to jpeg
lastmod: 2026-10-04
linktitle: แปลงเลเอาต์ CAD เป็นรูปแบบภาพเรสเตอร์
og_description: แปลง DWG เป็น PNG อย่างรวดเร็วด้วย Aspose.CAD for Java เรียนรู้ขั้นตอนต่อขั้นตอนว่าการส่งออก
  CAD เป็น PNG, JPEG, TIFF และอื่น ๆ ทำอย่างไร
og_image_alt: 'Developer guide: Convert DWG to PNG and other raster formats using
  Aspose.CAD for Java'
og_title: แปลง DWG เป็น PNG และรูปแบบเรสเตอร์อื่น ๆ ด้วย Aspose.CAD for Java
schemas:
- author: Aspose
  dateModified: '2026-10-04'
  description: Learn how to quickly convert dwg to png and export cad as png or other
    raster formats using Aspose.CAD for Java. Get high‑quality results fast.
  headline: Convert DWG to PNG and other raster formats using Aspose.CAD for Java
  type: TechArticle
- description: Learn how to quickly convert dwg to png and export cad as png or other
    raster formats using Aspose.CAD for Java. Get high‑quality results fast.
  name: Convert DWG to PNG and other raster formats using Aspose.CAD for Java
  steps:
  - name: set up the resource directory
    text: Replace `"Your Document Directory"` with the absolute path where your CAD
      files reside. This directory will be used for both input and output files.
  - name: load the CAD file
    text: '`Image.load` parses the source file and creates an in‑memory representation
      that you can rasterize. You can load any supported format (DWG, DXF, DGN, etc.)
      – this is the **how to convert cad** part.'
  - name: configure rasterization options
    text: '`CadRasterizationOptions` defines how the vector data is turned into pixels.
      `setPageWidth` and `setPageHeight` control output resolution (larger values
      = higher DPI). `setLayouts` lets you **convert CAD to raster** for specific
      layouts; omit it to rasterize the whole drawing.'
  - name: set image options
    text: '`TiffOptions` (or `PngOptions` for PNG) tells Aspose which raster format
      to generate and lets you fine‑tune compression, color depth, and other format‑specific
      settings. Choose the options class that matches your desired output.'
  - name: save the resultant image
    text: Call `save` on the `Image` instance, passing the output file name and the
      options object. Change the file extension to `.png` (and use `PngOptions`) to
      **save CAD as PNG**. The same pattern works for JPEG, BMP, or PDF. > **Common
      pitfall:** Forgetting to match the file extension with the options cla
  type: HowTo
- questions:
  - answer: Yes, it supports over 30 CAD and raster formats, including DWG, DXF, DGN,
      and SVG.
    question: Is Aspose.CAD compatible with different CAD file formats?
  - answer: Absolutely. Adjust `setPageWidth`, `setPageHeight`, or `setResolution`
      in `CadRasterizationOptions` to achieve the desired DPI.
    question: Can I customize the resolution of the output raster image?
  - answer: Provide an array with all layout names to `setLayouts`, e.g., `new String[]{"Model","Layout1","Layout2"}`.
    question: How can I convert multiple CAD layouts in a single run?
  - answer: Yes—PNG, JPEG, BMP, PDF, and more are available via their respective `*Options`
      classes.
    question: Are there output formats besides TIFF supported?
  - answer: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for community
      support and official assistance.
    question: Where can I get help or share my experience with Aspose.CAD?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- convert dwg
- Aspose.CAD
- Java raster conversion
- CAD image processing
title: แปลง DWG เป็น PNG และรูปแบบเรสเตอร์อื่น ๆ ด้วย Aspose.CAD for Java
url: /th/java/cad-drawing-conversion/convert-cad-layout-to-raster-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# แปลง DWG เป็น PNG และรูปแบบราสเตอร์อื่น ๆ ด้วย Aspose.CAD for Java

## บทนำ

`Aspose.CAD for Java` เป็นไลบรารีที่ช่วยให้สามารถแปลงไฟล์ CAD เป็นภาพราสเตอร์เช่น PNG, JPEG และ TIFF ได้โดยโปรแกรม การแปลง DWG เป็น PNG (หรือรูปแบบภาพราสเตอร์อื่น) เป็นความต้องการทั่วไปเมื่อคุณต้องการแชร์แบบ CAD ให้กับทีมที่ไม่มีโปรแกรมดู CAD, ฝังการออกแบบในเอกสาร, หรือสร้างภาพย่อสำหรับแกลเลอรีเว็บ ในคู่มือนี้คุณจะได้เรียนรู้วิธีแปลง dwg เป็น png อย่างรวดเร็วและเชื่อถือได้ ไม่ว่าคุณจะทำงานกับไฟล์แบบเต็มหรือเฉพาะเลย์เอาต์ คุณอาจต้อง **convert CAD to raster** สำหรับการพรีวิวเว็บ, เครื่องมือรายงาน, หรือแอปมือถือ

## คำตอบอย่างรวดเร็ว
- **ไลบรารีใดจัดการการแปลง DWG เป็น PNG?** Aspose.CAD for Java provides the conversion engine.  
- **รูปแบบราสเตอร์ใดบ้างที่ฉันสามารถส่งออกได้?** PNG, JPEG, TIFF, PDF, BMP, and more than 30 additional formats.  
- **ฉันต้องการใบอนุญาตสำหรับการทดสอบหรือไม่?** A free trial works for development; a commercial license is required for production.  
- **ฉันสามารถเลือกเลย์เอาต์เฉพาะได้หรือไม่?** Yes – use `setLayouts` to target “Model”, “Layout1”, etc.  
- **สามารถสร้างผลลัพธ์ความละเอียดสูงได้หรือไม่?** Absolutely – adjust `setPageWidth` and `setPageHeight` (or `setResolution`) to control DPI.

## อะไรคือ “convert dwg to png”?

Convert dwg to png หมายถึงการแปลงภาพวาดเวกเตอร์ DWG ให้เป็นภาพ PNG แบบพิกเซลที่สามารถแสดงผลได้โดยโปรแกรมดูภาพมาตรฐาน กระบวนการนี้ทำให้เวกเตอร์เป็นราสเตอร์โดยคงความหนาของเส้น, สี, และเลเยอร์ไว้ขณะแปลงเป็นบิตแมพความละเอียดคงที่ ผลลัพธ์เหมาะสำหรับการฝังใน PDF, เอกสาร Word, หรือหน้าเว็บที่รองรับเวกเตอร์จำกัด

## ทำไมต้องส่งออก CAD เป็น PNG (หรือรูปแบบราสเตอร์อื่น)?

การส่งออก CAD เป็น PNG ให้ความเข้ากันได้ทั่วโลก, การโหลดที่รวดเร็ว, และการฝังที่ง่ายบนแพลตฟอร์มหลักทั้งหมด ภาพราสเตอร์โหลดทันทีเมื่อเทียบกับการเปิดไฟล์ DWG ขนาดใหญ่, และการบีบอัดแบบ loss‑less ของ PNG ทำให้คงความคมชัดของภาพ การควบคุมความละเอียด, สีพื้นหลัง, และเลย์เอาต์ช่วยให้ทุกผู้มีส่วนได้ส่วนเสียเห็นภาพเดียวกัน ไม่ว่าจะดูบนเดสก์ท็อป, อุปกรณ์มือถือ, หรือในเบราว์เซอร์

## กรณีการใช้งานทั่วไป

| สถานการณ์ | เหตุผลที่ผลลัพธ์ราสเตอร์ช่วยได้ |
|----------|------------------------|
| **เอกสารโครงการ** | การฝัง PNG ใน PDF หรือเอกสาร Word ช่วยหลีกเลี่ยงการต้องใช้ซอฟต์แวร์ CAD สำหรับผู้ตรวจสอบ. |
| **พอร์ทัลเว็บ** | ภาพย่อที่สร้างจากไฟล์ DWG โหลดทันทีและปรับปรุงประสบการณ์ผู้ใช้. |
| **แอปมือถือ** | ภาพราสเตอร์แสดงผลอย่างถูกต้องบนอุปกรณ์ที่ไม่มีโปรแกรมดู CAD. |
| **การรายงานอัตโนมัติ** | แปลงหลายเลย์เอาต์เป็น PNG/JPEG เป็นชุดเพื่อใส่ในแผนภูมิหรือแดชบอร์ด. |

## ข้อกำหนดเบื้องต้น

ก่อนเริ่ม, ตรวจสอบว่าคุณมี:

1. **สภาพแวดล้อมการพัฒนา Java** – JDK 8 หรือใหม่กว่า ที่ติดตั้งและกำหนดค่าแล้ว.  
2. **Aspose.CAD for Java** – ดาวน์โหลด JAR ล่าสุดจาก [Aspose.CAD for Java documentation](https://reference.aspose.com/cad/java/).  

## นำเข้าเนมสเปซ

`com.aspose.cad.Image` เป็นคลาสหลักที่แสดงถึงไฟล์ CAD ใด ๆ ในหน่วยความจำ `com.aspose.cad.imageoptions.*` ให้วัตถุตัวเลือกสำหรับแต่ละรูปแบบราสเตอร์ นำเข้าคลาสที่คุณต้องการเพื่อโหลดแบบวาด, กำหนดค่าการราสเตอร์, และบันทึกผลลัพธ์.

> **เคล็ดลับ:** หากคุณวางแผนที่จะ **export CAD as PNG** แทน TIFF, ให้เปลี่ยน `TiffOptions` เป็น `PngOptions` (พบใน `com.aspose.cad.imageoptions.PngOptions`).

## คู่มือขั้นตอนต่อขั้นตอน

### ขั้นตอนที่ 1: ตั้งค่าไดเรกทอรีทรัพยากร

Replace `"Your Document Directory"` with the absolute path where your CAD files reside. This directory will be used for both input and output files.

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

### ขั้นตอนที่ 2: โหลดไฟล์ CAD

`Image.load` parses the source file and creates an in‑memory representation that you can rasterize. You can load any supported format (DWG, DXF, DGN, etc.) – this is the **how to convert cad** part.

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";
```

### ขั้นตอนที่ 3: กำหนดค่าตัวเลือกการราสเตอร์

`CadRasterizationOptions` defines how the vector data is turned into pixels. `setPageWidth` and `setPageHeight` control output resolution (larger values = higher DPI). `setLayouts` lets you **convert CAD to raster** for specific layouts; omit it to rasterize the whole drawing.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

### ขั้นตอนที่ 4: ตั้งค่าตัวเลือกภาพ

`TiffOptions` (or `PngOptions` for PNG) tells Aspose which raster format to generate and lets you fine‑tune compression, color depth, and other format‑specific settings. Choose the options class that matches your desired output.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1200);
rasterizationOptions.setPageHeight(1200);
rasterizationOptions.setLayouts(new String[] {"Model", "Layout1"});
```

### ขั้นตอนที่ 5: บันทึกภาพที่ได้

Call `save` on the `Image` instance, passing the output file name and the options object. Change the file extension to `.png` (and use `PngOptions`) to **save CAD as PNG**. The same pattern works for JPEG, BMP, or PDF.

```java
ImageOptionsBase options = new TiffOptions(TiffExpectedFormat.Default);
options.setVectorRasterizationOptions(rasterizationOptions);
```

> **ข้อผิดพลาดทั่วไป:** การลืมให้ส่วนขยายไฟล์ตรงกับคลาสตัวเลือกจะทำให้เกิด `UnsupportedFormatException`. ควรทำให้ตรงกันเสมอ.

## ปัญหาทั่วไปและวิธีแก้

| ปัญหา | วิธีแก้ |
|-------|----------|
| **ภาพผลลัพธ์เป็นสีขาว** | Verify that the layout names in `setLayouts` exactly match those in the source CAD file. |
| **PNG ความละเอียดต่ำ** | Increase `setPageWidth` / `setPageHeight` or set `setResolution` on the rasterization options. |
| **เวอร์ชัน DWG ที่ไม่รองรับ** | Ensure you are using the latest Aspose.CAD version; older releases may not support newer DWG releases. |
| **ข้อผิดพลาดหน่วยความจำกับไฟล์ขนาดใหญ่** | Process pages one at a time or increase JVM heap (`-Xmx2g`). |

## คำถามที่พบบ่อย

**Q: Aspose.CAD รองรับรูปแบบไฟล์ CAD ต่าง ๆ หรือไม่?**  
A: Yes, it supports over 30 CAD and raster formats, including DWG, DXF, DGN, and SVG.

**Q: ฉันสามารถปรับความละเอียดของภาพราสเตอร์ที่ส่งออกได้หรือไม่?**  
A: Absolutely. Adjust `setPageWidth`, `setPageHeight`, or `setResolution` in `CadRasterizationOptions` to achieve the desired DPI.

**Q: ฉันจะทำอย่างไรเพื่อแปลงหลายเลย์เอาต์ของ CAD ในการรันเดียว?**  
A: Provide an array with all layout names to `setLayouts`, e.g., `new String[]{"Model","Layout1","Layout2"}`.

**Q: มีรูปแบบผลลัพธ์อื่นนอกจาก TIFF ที่รองรับหรือไม่?**  
A: Yes—PNG, JPEG, BMP, PDF, and more are available via their respective `*Options` classes.

**Q: ฉันจะหาแหล่งช่วยเหลือหรือแบ่งปันประสบการณ์กับ Aspose.CAD ได้จากที่ไหน?**  
A: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for community support and official assistance.

## สรุป

By following these steps you can **convert DWG to PNG**, **export CAD as PNG**, **save CAD as JPEG**, or generate any other raster format you need. Aspose.CAD for Java handles the heavy lifting, letting you focus on integrating high‑quality images into your applications, documentation, or web portals. The library’s support for 30+ formats and its ability to render multi‑hundred‑page drawings without loading the entire file into memory make it a robust choice for enterprise‑grade CAD rasterization.

---

**อัปเดตล่าสุด:** 2026-10-04  
**ทดสอบกับ:** Aspose.CAD for Java 24.12  
**ผู้เขียน:** Aspose  







```java
image.save(dataDir + "conic_pyramid_layoutstorasterimage_out_.tiff", options);
```

```bash
java -jar aspose-cad.jar -i input.dwg -o output.png -w 1200 -h 1200
```

## บทแนะนำที่เกี่ยวข้อง

- [ส่งออก DWG ไปเป็น PDF หรือราสเตอร์อย่างรวดเร็วโดยใช้ไลบรารี java cad Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [แปลง DWG เป็น BMP ด้วย Aspose.CAD for Java](/cad/java/cad-export-options/export-to-bmp/)
- [ส่งออก DWG ไปเป็น PDF: เลย์เอ็ตเฉพาะโดยใช้ Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}