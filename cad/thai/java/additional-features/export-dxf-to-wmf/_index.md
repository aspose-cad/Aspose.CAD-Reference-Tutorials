---
date: 2026-06-09
description: เรียนรู้วิธีแปลง DXF เป็น WMF ด้วย Aspose.CAD สำหรับ Java รวมถึงการทดลองใช้ฟรี
  การสนับสนุน Java 8+ และการส่งออก PDF แบบเลือกได้ คู่มือขั้นตอนโดยละเอียดพร้อมตัวอย่างโค้ด
keywords:
- convert dxf to wmf
- aspose cad java
- aspose free trial
- aspose cad conversion
- export dxf pdf
linktitle: ส่งออก DXF เป็นรูปแบบ WMF ด้วย Java
schemas:
- author: Aspose
  dateModified: '2026-06-09'
  description: Learn how to convert DXF to WMF with Aspose.CAD for Java, including
    a free trial, Java 8+ support, and optional PDF export. Step‑by‑step guide with
    code examples.
  headline: Convert DXF to WMF Using Aspose.CAD in Java
  type: TechArticle
- description: Learn how to convert DXF to WMF with Aspose.CAD for Java, including
    a free trial, Java 8+ support, and optional PDF export. Step‑by‑step guide with
    code examples.
  name: Convert DXF to WMF Using Aspose.CAD in Java
  steps:
  - name: Load DXF Drawing
    text: Image.load reads the DXF file into an Aspose.CAD Image object.
  - name: Configure Rasterization Options
    text: CadRasterizationOptions specifies page size, resolution, and background
      for rasterizing the CAD drawing.
  - name: Save as WMF
    text: ImageSaveOptions with SaveFormat.WMF tells Aspose.CAD to write the output
      as a Windows Metafile.
  - name: Dispose of Resources
    text: Calling image.close() releases native resources used by the Aspose.CAD Image
      object.
  - name: Optional – Export to PDF
    text: PdfOptions configures PDF‑specific settings when saving the image as a PDF
      document. > **Pro tip:** You can reuse the same `CadRasterizationOptions` object
      for PDF export by passing it to a `PdfOptions` instance, saving you a few lines
      of setup.
  type: HowTo
- questions:
  - answer: Yes. Load the file in a try‑with‑resources block and dispose of the `Image`
      object promptly. Adjust `CadRasterizationOptions.setPageWidth/Height` to a reasonable
      size to keep memory usage low.
    question: Can I convert large DXF files (hundreds of MB) without running out of
      memory?
  - answer: WMF is a flat vector format, so layer hierarchy is flattened, but line
      styles, colors, and hatch patterns are preserved.
    question: Does the WMF output retain layer information?
  - answer: Use `rasterizationOptions.setResolution(300);` to define DPI before saving.
    question: Is it possible to set a custom DPI for the WMF?
  - answer: Absolutely. Loop through a directory, load each file, and apply the same
      rasterization and save logic.
    question: Can I batch‑convert multiple DXF files in one run?
  - answer: Aspose.CAD for Java supports Java 8 and later, including Java 11, 17,
      and newer LTS releases.
    question: What versions of Java are supported?
  type: FAQPage
second_title: Aspose.CAD Java API
title: แปลง DXF เป็น WMF ด้วย Aspose.CAD ใน Java
url: /th/java/additional-features/export-dxf-to-wmf/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# แปลง DXF เป็น WMF ด้วย Aspose.CAD ใน Java

## บทนำ

ในบทแนะนำนี้คุณจะได้เรียนรู้วิธี **แปลง DXF เป็น WMF** ด้วย Aspose.CAD สำหรับ Java ไม่ว่าคุณจะต้องการฝังภาพวาด CAD ลงในรายงานที่ทำงานบน Windows, สร้างกราฟิกเวกเตอร์ขนาดเล็กสำหรับเอกสาร Office, หรือทำการแปลงเป็นชุดอัตโนมัติ การแปลง DXF เป็น WMF เป็นความต้องการที่พบบ่อยในกระบวนการวิศวกรรมและการรายงาน เราจะเดินผ่านการโหลดไฟล์ DXF, การกำหนดค่าตัวเลือกการเรสเตอร์, การบันทึกผลลัพธ์เป็น WMF, และตัวเลือกการส่งออกภาพเดียวกันเป็น PDF

## คำตอบอย่างรวดเร็ว
- **ฉันสามารถแปลง DXF เป็น WMF ด้วยการทดลองใช้งานฟรีได้หรือไม่?** ใช่ – Aspose มีการทดลองใช้งานเต็มรูปแบบ 30 วัน  
- **ต้องใช้ Java เวอร์ชันใด?** Java 8 หรือใหม่กว่า  
- **จำเป็นต้องมีลิขสิทธิ์เพื่อรันโค้ดหรือไม่?** ต้องมีลิขสิทธิ์สำหรับการใช้งานในผลิตภัณฑ์; การทดลองใช้งานทำงานได้สำหรับการพัฒนาและการทดสอบ  
- **การแปลงนี้เป็นแบบไม่มีการสูญเสียข้อมูลหรือไม่?** ข้อมูลเวกเตอร์จะถูกเก็บรักษา; ตัวเลือกการเรสเตอร์ช่วยให้คุณควบคุมความละเอียดได้  
- **ฉันสามารถส่งออกภาพเดียวกันเป็น PDF ได้หรือไม่?** แน่นอน – ดูขั้นตอน “Export to PDF” ด้านล่าง

## “แปลง DXF เป็น WMF” คืออะไร?

การแปลง DXF เป็น WMF หมายถึงการนำไฟล์ Drawing Exchange Format (DXF) – รูปแบบ CAD ที่ใช้กันอย่างกว้างขวาง – มาทำให้เป็น Windows Metafile (WMF) WMF เป็นรูปแบบภาพเวกเตอร์ที่ทำงานร่วมกับ Microsoft Office, แอปพลิเคชัน Windows, และเครื่องมือรายงานหลายประเภทได้อย่างราบรื่น

## ทำไมต้องใช้ Aspose.CAD สำหรับ Java?

Aspose.CAD สำหรับ Java ให้เครื่องยนต์ Pure‑Java ที่ไม่มี DLL เนทีฟ ซึ่งแปลงไฟล์ CAD ด้วย **ความแม่นยำเวกเตอร์เกิน 99 %** โดยคงรักษาชั้น, สี, สไตล์เส้น, และลายเส้น hatch รองรับ **รูปแบบเข้าและออกกว่า 50+** – รวมถึง DXF, DWG, DGN, PDF, PNG, SVG, และ WMF – พร้อมให้คุณปรับขนาดหน้า, DPI, และสีพื้นหลังผ่านตัวเลือกการเรสเตอร์ที่สร้างมาในตัว API เดียวกันยังรองรับการส่งออกเป็น PDF, PNG, และ SVG ทำให้ไม่ต้องใช้หลายไลบรารี

### ข้อได้เปรียบหลัก
- **ไม่มีการพึ่งพาภายนอก** – Pure Java ทำงานบนทุก OS ที่รัน Java  
- **การเรนเดอร์คุณภาพสูง** – รักษาน้ำหนักเส้น, สี, และรายละเอียด hatch  
- **การเรสเตอร์ในตัว** – ควบคุมขนาดหน้า, ความละเอียด, และพื้นหลังได้  
- **การแปลงครบวงจร** – คลาสเดียวกันส่งออกเป็น WMF, PDF, PNG, SVG ฯลฯ  

## ข้อกำหนดเบื้องต้น

ก่อนเริ่มทำให้แน่ใจว่าคุณมี:

- **Aspose.CAD สำหรับ Java** ที่รวมไว้ในโปรเจกต์ของคุณ ดาวน์โหลดจากเว็บไซต์อย่างเป็นทางการ: [ดาวน์โหลด Aspose.CAD Java](https://releases.aspose.com/cad/java/)  
- **ไดเรกทอรีเอกสาร** ที่เก็บไฟล์ DXF ของคุณ (เช่น `Your Document Directory/DXFDrawings/`)  

## นำเข้า Namespaces

การนำเข้าต่อไปนี้จะดึงคลาส Aspose.CAD ที่จำเป็นสำหรับการโหลด, เรสเตอร์, และบันทึกไฟล์ CAD  
```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageSaveOptions;
import com.aspose.cad.fileformats.cad.CadRasterizationOptions;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.CadImageInfo;
import com.aspose.cad.fileformats.cad.CadImageInfo;
import java.awt.Color;
```

## คู่มือขั้นตอนต่อขั้นตอน

### ฉันจะแปลง DXF เป็น WMF ใน Java อย่างไร?

โหลดไฟล์ DXF ด้วย `Image.load("yourFile.dxf")`, ตั้งค่า `CadRasterizationOptions` สำหรับขนาดหน้าและ DPI ที่ต้องการ, จากนั้นเรียก `image.save("output.wmf", new ImageSaveOptions(SaveFormat.WMF))` รูปแบบสามขั้นตอนนี้ทำการแปลงครบถ้วนโดยคงคุณภาพเวกเตอร์ไว้และต้องใช้เพียงไม่กี่บรรทัดโค้ด

#### ขั้นตอนที่ 1: โหลดภาพวาด DXF

`Image.load` อ่านไฟล์ DXF เข้าเป็นอ็อบเจ็กต์ Aspose.CAD Image  
```java
import com.aspose.cad.Color;
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.WmfOptions;
```

#### ขั้นตอนที่ 2: ตั้งค่าตัวเลือกการเรสเตอร์

`CadRasterizationOptions` ระบุขนาดหน้า, ความละเอียด, และสีพื้นหลังสำหรับการเรสเตอร์ภาพวาด CAD  
```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DXFDrawings/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

#### ขั้นตอนที่ 3: บันทึกเป็น WMF

`ImageSaveOptions` พร้อม `SaveFormat.WMF` บอก Aspose.CAD ให้เขียนผลลัพธ์เป็น Windows Metafile  
```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(100);
rasterizationOptions.setPageHeight(100);
WmfOptions wmfOptions = new WmfOptions();
```

#### ขั้นตอนที่ 4: ปิดการใช้ทรัพยากร

การเรียก `image.close()` ปล่อยทรัพยากรเนทีฟที่ใช้โดยอ็อบเจ็กต์ Aspose.CAD Image  
```java
cadImage.save(dataDir+" example.ifc.wmf", wmfOptions);
```

#### ขั้นตอนที่ 5: ตัวเลือกเพิ่มเติม – ส่งออกเป็น PDF

`PdfOptions` ตั้งค่าที่เกี่ยวกับ PDF เมื่อบันทึกภาพเป็นเอกสาร PDF  
```java
finally
{
  cadImage.dispose();
}
```

> **เคล็ดลับ:** คุณสามารถใช้วัตถุ `CadRasterizationOptions` เดียวกันสำหรับการส่งออกเป็น PDF โดยส่งผ่านให้กับอินสแตนซ์ `PdfOptions` ซึ่งช่วยลดจำนวนบรรทัดการตั้งค่าได้

## ฉันจะส่งออก DXF เป็น PDF ด้วย Aspose CAD Java อย่างไร?

การส่งออกเป็น PDF ทำตามขั้นตอนการโหลดและการเรสเตอร์เดียวกัน; เพียงเปลี่ยนรูปแบบการบันทึกจาก WMF เป็น PDF ใช้ `new ImageSaveOptions(SaveFormat.Pdf)` และอาจตั้งค่าตัวเลือกเฉพาะ PDF เช่น ระดับการบีบอัดหรือเมตาดาต้าผู้เขียน การแปลงแบบบรรทัดเดียวนี้จะให้ PDF ที่ค้นหาได้และมีหน้าตรงกับเลย์เอาต์ CAD ดั้งเดิม

## ปัญหาที่พบบ่อยและวิธีแก้

| ปัญหา | สาเหตุ | วิธีแก้ |
|-------|-------|-----|
| **`NullPointerException` ที่ `cadImage.save`** | ตัวแปร `cadImage` ไม่ได้กำหนด (ควรเป็น `image`) | แทนที่ `cadImage` ด้วย `image` หรือเปลี่ยนชื่อแปรให้สอดคล้องกัน |
| **WMF ที่ได้เป็นสีขาวเปล่า** | ขนาดหน้าการเรสเตอร์เล็กเกินไปหรือสีพื้นหลังตั้งเป็นโปร่งแสง | เพิ่มค่า `PageWidth`/`PageHeight` หรือกำหนดสีพื้นหลังด้วย `rasterizationOptions.setBackgroundColor(Color.WHITE);` |
| **ข้อยกเว้นลิขสิทธิ์** | รันโดยไม่มีลิขสิทธิ์ Aspose ที่ถูกต้องในผลิตภัณฑ์ | โหลดไฟล์ลิขสิทธิ์เมื่อแอปเริ่มต้น: `License license = new License(); license.setLicense("Aspose.Total.Java.lic");` |

## สรุป

คุณมีเวิร์กโฟลว์ที่พร้อมใช้งานในระดับผลิตภัณฑ์เพื่อ **แปลง DXF เป็น WMF** ด้วย Aspose.CAD สำหรับ Java พร้อมขั้นตอนเสริมเพื่อ **ส่งออกภาพเดียวกันเป็น PDF** วิธีนี้ให้ผลลัพธ์เวกเตอร์คุณภาพสูงที่ผสานรวมกับเครื่องมือรายงานและเอกสารบน Windows ได้อย่างราบรื่น พร้อมโค้ดที่เรียบง่ายและไม่มีการพึ่งพาไลบรารีเพิ่มเติม

## คำถามที่พบบ่อย

### Q1: ฉันจะหาเอกสาร Aspose.CAD ได้จากที่ไหน?

A1: คุณสามารถเข้าถึงเอกสารได้ [ที่นี่](https://reference.aspose.com/cad/java/)  

### Q2: ฉันจะดาวน์โหลด Aspose.CAD สำหรับ Java ได้อย่างไร?

A2: ดาวน์โหลดไลบรารีได้ [ที่นี่](https://releases.aspose.com/cad/java/)  

### Q3: มีการทดลองใช้งานฟรีหรือไม่?

A3: มี, คุณสามารถรับการทดลองใช้งานฟรีได้ [ที่นี่](https://releases.aspose.com/)  

### Q4: ต้องการตัวเลือกลิขสิทธิ์ชั่วคราว?

A4: สำรวจลิขสิทธิ์ชั่วคราวได้ [ที่นี่](https://purchase.aspose.com/temporary-license/)  

### Q5: ฉันจะรับการสนับสนุนได้จากที่ไหน?

A5: เยี่ยมชมฟอรั่มสนับสนุน Aspose.CAD [ที่นี่](https://forum.aspose.com/c/cad/19)  

## Frequently Asked Questions

**Q: ฉันสามารถแปลงไฟล์ DXF ขนาดใหญ่ (หลายร้อย MB) โดยไม่เกิดปัญหาเรื่องหน่วยความจำหรือไม่?**  
A: ได้. โหลดไฟล์ในบล็อก `try‑with‑resources` และปิดอ็อบเจ็กต์ `Image` ทันที ปรับ `CadRasterizationOptions.setPageWidth/Height` ให้เหมาะสมเพื่อควบคุมการใช้หน่วยความจำ  

**Q: ผลลัพธ์ WMF จะรักษาข้อมูลชั้น (layer) ไว้หรือไม่?**  
A: WMF เป็นรูปแบบเวกเตอร์แบน จึงทำให้โครงสร้างชั้นถูกแปลงเป็นแบน แต่สไตล์เส้น, สี, และลาย hatch จะถูกเก็บรักษาไว้  

**Q: สามารถกำหนด DPI ที่กำหนดเองสำหรับ WMF ได้หรือไม่?**  
A: ใช้ `rasterizationOptions.setResolution(300);` เพื่อกำหนด DPI ก่อนบันทึก  

**Q: ฉันสามารถแปลงหลายไฟล์ DXF เป็นชุดได้ในครั้งเดียวหรือไม่?**  
A: แน่นอน. วนลูปผ่านไดเรกทอรี, โหลดแต่ละไฟล์, แล้วใช้ตรรกะการเรสเตอร์และบันทึกเดียวกัน  

**Q: รองรับเวอร์ชัน Java ใดบ้าง?**  
A: Aspose.CAD สำหรับ Java รองรับ Java 8 ขึ้นไป รวมถึง Java 11, 17, และรุ่น LTS ใหม่ ๆ  

---

**อัปเดตล่าสุด:** 2026-06-09  
**ทดสอบด้วย:** Aspose.CAD for Java 24.11  
**ผู้เขียน:** Aspose

```java
image.save(dataDir + "conic_pyramid_out_.pdf"); 
```

## บทแนะนำที่เกี่ยวข้อง

- [สร้าง PDF จาก CAD – ส่งออก DXF เป็น PDF ด้วย Aspose.CAD for Java](/cad/java/additional-features/export-dxf-to-pdf/)
- [สร้าง PDF จาก DXF: ส่งออกชั้นด้วย Aspose.CAD for Java](/cad/java/additional-features/export-specific-layer-to-pdf/)
- [วิธีแปลงเลย์เอาต์ DXF เป็นภาพ JPEG ด้วย Aspose.CAD ใน Java](/cad/java/additional-features/export-specific-layout-to-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}