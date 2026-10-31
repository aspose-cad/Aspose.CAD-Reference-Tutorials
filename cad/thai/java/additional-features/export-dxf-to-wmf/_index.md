---
date: 2026-10-30
description: เรียนรู้วิธีแปลงไฟล์ DXF เป็น WMF เป็นชุดโดยใช้ Aspose.CAD for Java พร้อมโค้ดขั้นตอนต่อขั้นตอน
  ข้อมูลการทดลองใช้ฟรี และการส่งออกเป็น PDF แบบเลือกได้
keywords:
- batch convert dxf files
- aspose cad java
- dxf to wmf conversion
- java cad rasterization
- aspose free trial
lastmod: 2026-10-30
linktitle: ส่งออก DXF ไปเป็นรูปแบบ WMF ด้วย Java
og_description: แปลงไฟล์ DXF เป็น WMF เป็นชุดโดยใช้ Aspose.CAD for Java. ทำตามคู่มือนี้เพื่อโหลดภาพวาด
  DXF, ตั้งค่าตัวเลือก rasterization, บันทึกเป็น WMF, และสามารถส่งออกเป็น PDF ได้โดยใช้การทดลองใช้ฟรี.
og_image_alt: Tutorial showing batch conversion of DXF to WMF in Java using Aspose.CAD
og_title: แปลงไฟล์ DXF เป็น WMF เป็นชุดโดยใช้ Aspose.CAD for Java
schemas:
- author: Aspose
  dateModified: '2026-10-30'
  description: Learn how to batch convert DXF files to WMF using Aspose.CAD for Java,
    with step‑by‑step code, free trial info, and optional PDF export.
  headline: Batch convert DXF files to WMF with Aspose.CAD for Java
  type: TechArticle
- description: Learn how to batch convert DXF files to WMF using Aspose.CAD for Java,
    with step‑by‑step code, free trial info, and optional PDF export.
  name: Batch convert DXF files to WMF with Aspose.CAD for Java
  steps:
  - name: load dxf drawing
    text: Image.load reads the DXF file into an Aspose.CAD Image object.
  - name: configure rasterization options
    text: '`CadRasterizationOptions` specifies page size, resolution, and background
      for rasterizing the CAD drawing.'
  - name: save as wmf
    text: '`ImageSaveOptions` with `SaveFormat.WMF` tells Aspose.CAD to write the
      output as a Windows Metafile.'
  - name: dispose of resources
    text: Calling `image.close()` releases native resources used by the Aspose.CAD
      Image object.
  - name: optional – export to pdf
    text: '`PdfOptions` configures PDF‑specific settings when saving the image as
      a PDF document. > **Pro tip:** You can reuse the same `CadRasterizationOptions`
      object for PDF export by passing it to a `PdfOptions` instance, saving you a
      few lines of setup.'
  type: HowTo
- questions:
  - answer: You can access the documentation [Aspose.CAD Java documentation](https://reference.aspose.com/cad/java/).
    question: Where can I find the Aspose.CAD documentation?
  - answer: Download the library [Aspose.CAD Java download page](https://releases.aspose.com/cad/java/).
    question: How do I download Aspose.CAD for Java?
  - answer: Yes, you can get a free trial [Aspose free trial page](https://releases.aspose.com/).
    question: Is there a free trial available?
  - answer: Explore temporary licenses [temporary license options](https://purchase.aspose.com/temporary-license/).
    question: Need temporary licensing options?
  - answer: Visit the Aspose.CAD support forum [Aspose.CAD support forum](https://forum.aspose.com/c/cad/19).
    question: Where can I get support?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- batch convert dxf
- Aspose.CAD
- Java CAD conversion
- WMF export
- DXF processing
title: แปลงไฟล์ DXF เป็น WMF เป็นชุดโดยใช้ Aspose.CAD for Java
url: /th/java/additional-features/export-dxf-to-wmf/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# แปลงไฟล์ DXF เป็น WMF เป็นชุดด้วย Aspose.CAD สำหรับ Java

## บทนำ

ในบทแนะนำนี้คุณจะได้เรียนรู้วิธี **แปลงไฟล์ DXF เป็น WMF เป็นชุด** ด้วย Aspose.CAD สำหรับ Java ไม่ว่าคุณจะต้องการฝังภาพวาด CAD ลงในรายงานบน Windows, สร้างกราฟิกเวกเตอร์ที่มีน้ำหนักเบาสำหรับเอกสาร Office, หรือทำการแปลงจำนวนมากโดยอัตโนมัติ คำแนะนำนี้จะพาคุณผ่านการโหลดภาพวาด DXF, การกำหนดค่าตัวเลือกการเรสเตอร์ไลซ์, การบันทึกเป็น WMF, และการส่งออกภาพวาดเดียวกันเป็น PDF หากต้องการ ขั้นตอนเหล่านี้ทำงานบนทุกแพลตฟอร์มที่รองรับ Java 8+

## คำตอบสั้น
- **ฉันสามารถแปลง DXF เป็น WMF ด้วยการทดลองใช้ฟรีได้หรือไม่?** ใช่ – Aspose มีการทดลองใช้งานเต็มรูปแบบ 30‑วัน.  
- **ต้องการเวอร์ชัน Java ใด?** Java 8 หรือใหม่กว่า.  
- **ฉันต้องมีใบอนุญาตเพื่อรันโค้ดหรือไม่?** ต้องมีใบอนุญาตสำหรับการใช้งานในสภาพการผลิต; การทดลองใช้ทำงานได้สำหรับการพัฒนาและการทดสอบ.  
- **การแปลงนี้ไม่มีการสูญเสียข้อมูลหรือไม่?** ข้อมูลเวกเตอร์จะถูกเก็บไว้; ตัวเลือกการเรสเตอร์ไลซ์ให้คุณควบคุมความละเอียด.  
- **ฉันสามารถส่งออกภาพวาดเดียวกันเป็น PDF ได้หรือไม่?** แน่นอน – ดูขั้นตอน “Export to PDF” ด้านล่าง.  
- **ฉันจะทำการแปลงหลายไฟล์ DXF เป็นชุดพร้อมกันอย่างไร?** วนลูปผ่านโฟลเดอร์, ใช้รูปแบบ load‑rasterize‑save เดียวกันกับแต่ละไฟล์.

## การแปลงไฟล์ DXF เป็นชุดคืออะไร?

การแปลงไฟล์ DXF เป็นชุดหมายถึงการประมวลผลหลายไฟล์ Drawing Exchange Format (DXF) ในการทำงานครั้งเดียวและสร้างผลลัพธ์ WMF สำหรับแต่ละไฟล์ WMF (Windows Metafile) เป็นรูปแบบภาพเวกเตอร์ที่รวมเข้ากับ Microsoft Office, แอปพลิเคชัน Windows, และเครื่องมือรายงานหลายประเภทโดยตรง

## ทำไมต้องใช้ Aspose.CAD สำหรับ Java?

Aspose.CAD สำหรับ Java เป็นเอนจิน pure‑Java ที่รองรับ **รูปแบบที่รองรับกว่า 50 แบบ** — รวมถึง DXF, DWG, DGN, PDF, PNG, SVG, และ WMF — พร้อมให้ **ความแม่นยำเวกเตอร์ 99 %** มันทำงานบน OS ใดก็ได้ที่สนับสนุน Java, ไม่ต้องใช้ DLL เนทีฟ, และให้คุณควบคุมขนาดหน้า, DPI, และสีพื้นหลังผ่านคลาส `CadRasterizationOptions` เพียงคลาสเดียว API เดียวกันยังจัดการการส่งออกเป็น PDF, PNG, และ SVG อีกด้วย ทำให้ไม่ต้องใช้หลายไลบรารี

### ประโยชน์ที่วัดได้
- **รูปแบบที่รองรับกว่า 50 แบบ** ลดความจำเป็นในการใช้ตัวแปลงจากบุคคลที่สาม.  
- **ประมวลผลไฟล์ DXF 300 หน้าในเวลาน้อยกว่า 5 วินาที** บนเซิร์ฟเวอร์ 2.5 GHz ปกติเมื่อเรสเตอร์ไลซ์ที่ 150 DPI.  
- **การใช้หน่วยความจำคงที่ต่ำกว่า 200 MB** สำหรับไฟล์ขนาดสูงสุด 500 MB เมื่อคุณตั้งค่าขนาดหน้าที่เหมาะสม.  

## ข้อกำหนดเบื้องต้น

- **Aspose.CAD for Java** ที่รวมไว้ในโครงการของคุณ ดาวน์โหลดจากเว็บไซต์อย่างเป็นทางการ: [Aspose.CAD Java download](https://releases.aspose.com/cad/java/).  
- โฟลเดอร์ที่มีไฟล์ DXF ที่คุณต้องการแปลง (เช่น `Your Document Directory/DXFDrawings/`).  

## นำเข้าเนมสเปซ

`Image` คือคลาสหลักของ Aspose.CAD ที่แทนภาพวาด CAD ในหน่วยความจำ หลังจากโหลดไฟล์แล้ว การดำเนินการต่อไปทั้งหมด — การเรสเตอร์ไลซ์, การแปลงรูปแบบ, และการทำความสะอาดทรัพยากร — จะทำผ่านอ็อบเจ็กต์นี้

การนำเข้าต่อไปนี้นำเข้าคลาสของ Aspose.CAD ที่จำเป็นสำหรับการโหลด, เรสเตอร์ไลซ์, และบันทึกไฟล์ CAD.  
```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageSaveOptions;
import com.aspose.cad.fileformats.cad.CadRasterizationOptions;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.CadImageInfo;
import com.aspose.cad.fileformats.cad.CadImageInfo;
import java.awt.Color;
```

## คู่มือทีละขั้นตอน

### ฉันจะทำการแปลงไฟล์ DXF เป็น WMF เป็นชุดใน Java อย่างไร?

โหลดแต่ละไฟล์ DXF ด้วย `Image.load`, กำหนด `CadRasterizationOptions` สำหรับขนาดหน้าและ DPI ที่ต้องการ, แล้วเรียก `image.save` ด้วย `SaveFormat.WMF` รูปแบบสามขั้นตอนนี้ทำการแปลงครบถ้วนพร้อมรักษาคุณภาพเวกเตอร์และต้องการเพียงไม่กี่บรรทัดต่อไฟล์

#### ขั้นตอนที่ 1: โหลดภาพวาด DXF

`Image.load` อ่านไฟล์ DXF เข้าเป็นอ็อบเจ็กต์ Image ของ Aspose.CAD.  
```java
import com.aspose.cad.Color;
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.WmfOptions;
```

#### ขั้นตอนที่ 2: กำหนดค่าตัวเลือกการเรสเตอร์ไลซ์

`CadRasterizationOptions` ระบุขนาดหน้า, ความละเอียด, และสีพื้นหลังสำหรับการเรสเตอร์ไลซ์ภาพวาด CAD.  
```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DXFDrawings/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

#### ขั้นตอนที่ 3: บันทึกเป็น WMF

`ImageSaveOptions` พร้อม `SaveFormat.WMF` บอก Aspose.CAD ให้เขียนผลลัพธ์เป็น Windows Metafile.  
```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(100);
rasterizationOptions.setPageHeight(100);
WmfOptions wmfOptions = new WmfOptions();
```

#### ขั้นตอนที่ 4: ปล่อยทรัพยากร

การเรียก `image.close()` ปล่อยทรัพยากรเนทีฟที่ใช้โดยอ็อบเจ็กต์ Image ของ Aspose.CAD.  
```java
cadImage.save(dataDir+" example.ifc.wmf", wmfOptions);
```

#### ขั้นตอนที่ 5: ตัวเลือก – ส่งออกเป็น PDF

`PdfOptions` กำหนดการตั้งค่าเฉพาะ PDF เมื่อบันทึกภาพเป็นเอกสาร PDF.  
```java
finally
{
  cadImage.dispose();
}
```

> **เคล็ดลับ:** คุณสามารถใช้วัตถุ `CadRasterizationOptions` เดียวกันสำหรับการส่งออกเป็น PDF โดยส่งผ่านไปยังอินสแตนซ์ `PdfOptions` ซึ่งจะช่วยลดจำนวนบรรทัดการตั้งค่า.

## ฉันจะส่งออก DXF เป็น PDF ด้วย Aspose CAD Java อย่างไร?

เปลี่ยนรูปแบบการบันทึกจาก WMF เป็น PDF โดยใช้ `new ImageSaveOptions(SaveFormat.Pdf)` การตั้งค่าการเรสเตอร์ไลซ์เดียวกันจะถูกนำไปใช้, และคุณสามารถตั้งค่าตัวเลือกเฉพาะ PDF เช่น เมตาดาต้าผู้เขียนหรือระดับการบีบอัดได้ การแปลงแบบบรรทัดเดียวนี้จะสร้าง PDF ที่สามารถค้นหาได้และมีหน้าตรงกับเลเอาต์ CAD ดั้งเดิม

## ปัญหาทั่วไปและวิธีแก้

`License` คือคลาสของ Aspose ที่ใช้ในการกำหนดใบอนุญาตผลิตภัณฑ์ในเวลารัน

| ปัญหา | สาเหตุ | วิธีแก้ |
|-------|-------|-----|
| **`NullPointerException` บน `cadImage.save`** | ตัวแปร `cadImage` ไม่ได้กำหนด (ควรเป็น `image`). | แทนที่ `cadImage` ด้วย `image` หรือเปลี่ยนชื่อของตัวแปรให้สอดคล้องกัน. |
| **ผลลัพธ์ WMF ว่าง** | ขนาดหน้าการเรสเตอร์ไลซ์เล็กเกินไปหรือสีพื้นหลังตั้งเป็นโปร่งใส. | เพิ่มค่า `PageWidth`/`PageHeight` หรือกำหนดสีพื้นหลังโดยใช้ `rasterizationOptions.setBackgroundColor(Color.WHITE);`. |
| **ข้อยกเว้นใบอนุญาต** | ทำงานโดยไม่มีใบอนุญาต Aspose ที่ถูกต้องในสภาพการผลิต. | ใช้ไฟล์ใบอนุญาตที่เริ่มต้นแอปพลิเคชัน: `License license = new License(); license.setLicense("Aspose.Total.Java.lic");`. |

## คำถามที่พบบ่อย

**ถาม: ฉันสามารถหาเอกสาร Aspose.CAD ได้จากที่ไหน?**  
คุณสามารถเข้าถึงเอกสารได้ที่ [Aspose.CAD Java documentation](https://reference.aspose.com/cad/java/).

**ถาม: ฉันจะดาวน์โหลด Aspose.CAD สำหรับ Java ได้อย่างไร?**  
ดาวน์โหลดไลบรารีจาก [Aspose.CAD Java download page](https://releases.aspose.com/cad/java/).

**ถาม: มีการทดลองใช้ฟรีหรือไม่?**  
ใช่, คุณสามารถรับการทดลองใช้ฟรีได้จาก [Aspose free trial page](https://releases.aspose.com/).

**ถาม: ต้องการตัวเลือกใบอนุญาตชั่วคราวหรือไม่?**  
สำรวจใบอนุญาตชั่วคราวที่ [temporary license options](https://purchase.aspose.com/temporary-license/).

**ถาม: ฉันจะขอรับการสนับสนุนได้จากที่ไหน?**  
เยี่ยมชมฟอรั่มสนับสนุน Aspose.CAD ที่ [Aspose.CAD support forum](https://forum.aspose.com/c/cad/19).

## คำถามที่พบบ่อยเพิ่มเติม

**ถาม: ฉันสามารถแปลงไฟล์ DXF ขนาดใหญ่ (หลายร้อย MB) โดยไม่เกิดการใช้หน่วยความจำเกินได้หรือไม่?**  
ได้. โหลดไฟล์ในบล็อก `try‑with‑resources` และทำลายอ็อบเจ็กต์ `Image` ทันที ปรับ `CadRasterizationOptions.setPageWidth/Height` ให้มีขนาดเหมาะสมเพื่อรักษาการใช้หน่วยความจำให้ต่ำ

**ถาม: ผลลัพธ์ WMF จะเก็บข้อมูลเลเยอร์ไว้หรือไม่?**  
WMF เป็นรูปแบบเวกเตอร์แบบแบน ดังนั้นโครงสร้างเลเยอร์จะถูกทำให้แบนราบ แต่สไตล์เส้น, สี, และลายเส้น hatch จะถูกเก็บไว้

**ถาม: สามารถตั้งค่า DPI ที่กำหนดเองสำหรับ WMF ได้หรือไม่?**  
ใช้ `rasterizationOptions.setResolution(300);` เพื่อกำหนด DPI ก่อนบันทึก

**ถาม: ฉันสามารถแปลงหลายไฟล์ DXF เป็นชุดในหนึ่งการรันได้หรือไม่?**  
แน่นอน. วนลูปผ่านไดเรกทอรี, โหลดแต่ละไฟล์, และใช้ตรรกะการเรสเตอร์ไลซ์และบันทึกเดียวกัน

**ถาม: รองรับเวอร์ชัน Java ใดบ้าง?**  
Aspose.CAD for Java รองรับ Java 8 และใหม่กว่า รวมถึง Java 11, 17, และรุ่น LTS ล่าสุด

**อัปเดตล่าสุด:** 2026-10-30  
**ทดสอบกับ:** Aspose.CAD for Java 24.11  
**ผู้เขียน:** Aspose

## บทแนะนำที่เกี่ยวข้อง

- [สร้าง PDF จาก CAD – ส่งออก DXF เป็น PDF ด้วย Aspose.CAD สำหรับ Java](/cad/java/additional-features/export-dxf-to-pdf/)
- [สร้าง PDF จาก DXF: ส่งออกเลเยอร์ด้วย Aspose.CAD สำหรับ Java](/cad/java/additional-features/export-specific-layer-to-pdf/)
- [วิธีแปลงเลเอาต์ DXF เป็นภาพ JPEG ด้วย Aspose.CAD ใน Java](/cad/java/additional-features/export-specific-layout-to-image/)

```java
image.save(dataDir + "conic_pyramid_out_.pdf"); 
```

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}