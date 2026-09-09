---
date: 2026-09-09
description: เรียนรู้วิธีใช้ Aspose CAD export เพื่อแปลงเลเอาต์ DXF เฉพาะเป็น JPEG
  หรือ PNG ใน .NET. ทำตามคำแนะนำทีละขั้นตอนเพื่อผลลัพธ์ที่รวดเร็ว.
keywords:
- aspose cad export
- how to export dxf
- convert dxf to jpeg
- batch export dxf
- convert dwf to jpeg
lastmod: 2026-09-09
linktitle: การส่งออกเลเอาต์ DXF เฉพาะเป็นภาพ
og_description: เรียนรู้วิธีใช้ Aspose CAD export เพื่อแปลงเลเอาต์ DXF เฉพาะเป็น JPEG
  หรือ PNG ใน .NET. ทำตามคำแนะนำทีละขั้นตอนเพื่อผลลัพธ์ที่รวดเร็ว.
og_image_alt: Tutorial showing Aspose CAD export of DXF layout to JPEG image in .NET
og_title: Aspose CAD export – การส่งออกเลเอาต์ DXF เฉพาะเป็นภาพ
schemas:
- author: Aspose
  dateModified: '2026-09-09'
  description: Learn how to use Aspose CAD export to convert a specific DXF layout
    to JPEG or PNG in .NET. Follow step‑by‑step instructions for fast results.
  headline: Aspose CAD export – exporting a specific DXF layout to an image
  type: TechArticle
- description: Learn how to use Aspose CAD export to convert a specific DXF layout
    to JPEG or PNG in .NET. Follow step‑by‑step instructions for fast results.
  name: Aspose CAD export – exporting a specific DXF layout to an image
  steps:
  - name: set up your project
    text: Create a new .NET project or open an existing one where you plan to implement
      the Aspose.CAD functionality.
  - name: load CAD image
    text: 'Use the following code to load a CAD image from your specified file path:'
  - name: configure rasterization options
    text: 'Set up the rasterization options, specifying the page width and height:'
  - name: iterate over layers
    text: 'Retrieve the layers from the CAD image and iterate through them:'
  - name: export layers to images
    text: For each layer, export it to a JPEG image using the configured options.
      The `JpegOptions` class defines JPEG‑specific settings such as quality and compression
      level. Repeat these steps for each layer in the CAD image.
  type: HowTo
- questions:
  - answer: Yes – you can script a folder scan and call the same export routine for
      each file; the library is optimized for high‑throughput scenarios.
    question: Does Aspose CAD export support batch processing of thousands of files?
  - answer: Absolutely – set the `JpegQuality` property in `RasterizationOptions`
      to a value between 0 and 100.
    question: Can I control the JPEG quality level?
  - answer: Yes – change the `Save` format to `SaveFormat.Png` and adjust any transparency
      settings as needed.
    question: Is it possible to export a layout as a PNG instead of JPEG?
  - answer: Aspose.CAD supports .NET Framework 4.5+, .NET Core 3.1+, .NET 5, .NET
      6 and later.
    question: What .NET versions are officially supported?
  - answer: The engine streams pages to disk and never loads the full document into
      memory, allowing processing of multi‑gigabyte files on modest hardware.
    question: How does Aspose CAD export handle very large drawings?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- aspose cad
- dxf export
- cad to image
- c# cad processing
- cad conversion
title: Aspose CAD export – การส่งออกเลเอาต์ DXF เฉพาะเป็นภาพ
url: /th/net/layout-and-object-handling/exporting-specific-dxf-layout-to-image/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# การส่งออก Aspose CAD – ส่งออกเลเอาต์ DXF เฉพาะเป็นภาพ

## บทนำ

Aspose CAD export ช่วยให้คุณแปลงภาพวาด CAD รวมถึงเลเอาต์ DXF แยกแต่ละอันโดยตรงเป็นภาพเรสเตอร์ เช่น JPEG หรือ PNG โดยไม่ต้องใช้ซอฟต์แวร์ CAD ของบุคคลที่สาม ในบทแนะนำนี้คุณจะได้เรียนรู้วิธีโหลดไฟล์ DXF เลือกเลเอาต์ที่ต้องการ และส่งออกเป็นภาพด้วยโค้ด .NET เพียงไม่กี่บรรทัด

## คำตอบอย่างรวดเร็ว
- **ต้องการไลบรารีอะไร?** Aspose.CAD for .NET (ส่วนประกอบการส่งออก Aspose CAD).  
- **ฉันสามารถส่งออกเพียงเลเอาต์เดียวได้หรือไม่?** ได้ – คุณสามารถเลือกเลเอาต์เฉพาะก่อนทำ rasterizing.  
- **รูปแบบผลลัพธ์ที่รองรับ?** JPEG, PNG, BMP, TIFF และอื่น ๆ.  
- **ต้องการใบอนุญาตสำหรับการใช้งานจริงหรือไม่?** จำเป็นต้องมีใบอนุญาต Aspose.CAD ที่ถูกต้องสำหรับการใช้งานที่ไม่ใช่แบบทดลอง.  
- **จะทำงานบน .NET 6+ หรือไม่?** แน่นอน – ไลบรารีรองรับ .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## Aspose CAD export คืออะไร?

Aspose CAD export เป็นส่วนหนึ่งของไลบรารี Aspose.CAD ที่แปลงไฟล์ CAD และ BIM ให้เป็นภาพเรสเตอร์หรือเวกเตอร์ มันให้ API แบบเรียกครั้งเดียวเพื่อเรนเดอร์เลเอาต์ หน้า หรือเลเยอร์ใด ๆ โดยไม่ต้องติดตั้ง AutoCAD ส่วนประกอบนี้ยังรองรับการประมวลผลเป็นชุด ผลลัพธ์ความละเอียดสูง และตัวเลือกการเรนเดอร์ขั้นสูง เช่น การทำ anti‑aliasing และการควบคุมสีพื้นหลัง

## ทำไมต้องใช้ Aspose CAD export สำหรับการแปลง DXF?

Aspose CAD export รองรับ **รูปแบบ CAD/BIM มากกว่า 30 รูปแบบ** และสามารถเรนเดอร์ไฟล์ที่มีถึง **10 000 หน้า** พร้อมคงการใช้หน่วยความจำต่ำกว่า **50 MB** ด้วยการสตรีมข้อมูล เอนจินจะรักษาน้ำหนักเส้น สี และลวดลาย hatch อย่างแม่นยำ ส่งออก JPEG ที่พิกเซลสมบูรณ์แบบตรงกับภาพวาดต้นฉบับ อีกทั้งยังขจัดความจำเป็นในการติดตั้ง CAD บนเดสก์ท็อป ทำให้การสร้างสายงานแปลงอัตโนมัติง่ายและคุ้มค่า

## ข้อกำหนดเบื้องต้น

- Aspose.CAD Library: ดาวน์โหลดและติดตั้งไลบรารี Aspose.CAD จาก [release page](https://releases.aspose.com/cad/net/).  
- Development Environment: ตรวจสอบให้แน่ใจว่าคุณมีสภาพแวดล้อมการพัฒนา .NET ตั้งค่าไว้บนเครื่องของคุณ

## นำเข้า namespace

ในโครงการ .NET ของคุณ ให้เริ่มต้นด้วยการนำเข้า namespace ที่จำเป็นเพื่อเข้าถึงฟังก์ชันของ Aspose.CAD:

```csharp
using System;
```

## วิธีส่งออกเลเอาต์ DXF เฉพาะเป็นภาพ?

โหลดไฟล์ DXF เลือกเลเอาต์ที่ต้องการ ตั้งค่าตัวเลือกการ rasterization แล้วบันทึกผลลัพธ์เป็นภาพ กระบวนการทั้งหมดใช้เพียงไม่กี่การเรียกเมธอดและทำงานภายในไม่กี่วินาทีสำหรับภาพวาดทั่วไป คลาส `CadImage` แสดงภาพวาด CAD ที่โหลดเข้าสู่หน่วยความจำ ให้เข้าถึงเลเยอร์ เลเอาต์ และตัวเลือกการเรนเดอร์ได้

### ขั้นตอนที่ 1: ตั้งค่าโปรเจกต์ของคุณ
สร้างโปรเจกต์ .NET ใหม่หรือเปิดโปรเจกต์ที่มีอยู่ซึ่งคุณต้องการนำฟังก์ชัน Aspose.CAD ไปใช้

### ขั้นตอนที่ 2: โหลดภาพ CAD
ใช้โค้ดต่อไปนี้เพื่อโหลดภาพ CAD จากเส้นทางไฟล์ที่ระบุ:

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "for_layers_test.dwf";

using (var image = (Aspose.CAD.FileFormats.Cad.CadImage)Aspose.CAD.Image.Load(sourceFilePath))
{
    // Your code for further steps will go here.
}
```

### ขั้นตอนที่ 3: กำหนดค่าตัวเลือกการ rasterization
ตั้งค่าตัวเลือกการ rasterization โดยระบุความกว้างและความสูงของหน้า:

```csharp
var rasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
```

### ขั้นตอนที่ 4: วนซ้ำผ่านเลเยอร์
ดึงเลเยอร์จากภาพ CAD แล้ววนลูปผ่านแต่ละเลเยอร์:

```csharp
var layersList = image.Layers;
foreach (var layerName in layersList.GetLayersNames())
{
    // Your code for further steps will go here.
}
```

### ขั้นตอนที่ 5: ส่งออกเลเยอร์เป็นภาพ
สำหรับแต่ละเลเยอร์ ให้ส่งออกเป็นภาพ JPEG โดยใช้ตัวเลือกที่กำหนดไว้ คลาส `JpegOptions` กำหนดการตั้งค่าเฉพาะ JPEG เช่น คุณภาพและระดับการบีบอัด

```csharp
rasterizationOptions.Layers = new string[] { layerName };
var options = new Aspose.CAD.ImageOptions.JpegOptions();
options.VectorRasterizationOptions = rasterizationOptions;
image.Save(layerName + "_out.jpg", options);
```

ทำซ้ำขั้นตอนเหล่านี้สำหรับแต่ละเลเยอร์ในภาพ CAD

## วิธีส่งออกเลเอาต์ DXF เป็นภาพแบบชุด

คุณสามารถวางไฟล์ DXF ทั้งหมดในโฟลเดอร์หนึ่ง ลูปผ่านแต่ละไฟล์ เลือกเลเอาต์ที่ต้องการ แล้วเรียกใช้ตรรกะการส่งออกเดียวกัน วิธีนี้ช่วยให้คุณแปลงหลายสิบภาพวาดในรอบเดียว เหมาะสำหรับสายงานอัตโนมัติ โดยการใช้การตั้งค่า rasterization และการบันทึกเดียวกัน คุณจะได้คุณภาพผลลัพธ์ที่สม่ำเสมอทั่วทั้งชุด

## วิธีแปลง DWF เป็น JPEG ด้วย Aspose CAD?

Aspose CAD export ยังรองรับไฟล์ DWF อีกด้วย โหลด DWF ด้วย `CadImage.Load` ตั้งค่าตัวเลือกการ rasterization เหมือนกับ DXF แล้วเรียก `Save` ด้วยรูปแบบ JPEG API เหมือนกันกับกระบวนการ DXF ทำให้คุณสามารถใช้โค้ดฐานเดียวกันสำหรับคอลเลกชันไฟล์ CAD ที่หลากหลายโดยไม่ต้องเพิ่มโค้ดสาขา

## ปัญหาที่พบบ่อยและวิธีแก้

- **Missing layout name:** ตรวจสอบให้แน่ใจว่าอัตลักษณ์ของเลเอาต์ตรงกับชื่อที่แสดงในตัวจัดการเลเยอร์ของไฟล์ CAD.  
- **Large file memory spikes:** ใช้ `CadImage.Load` พร้อม `LoadOptions` ที่เปิดใช้งานการสตรีมเพื่อรักษาหน่วยความจำให้ต่ำ.  
- **Incorrect colors:** ตรวจสอบให้แน่ใจว่า property `BackgroundColor` ใน `RasterizationOptions` ถูกตั้งค่าเป็น `Color.White` หากคุณต้องการพื้นหลังสีขาว.

## คำถามที่พบบ่อย

### คำถาม 1: ฉันสามารถใช้ Aspose.CAD กับเฟรมเวิร์ก .NET อื่น ๆ ได้หรือไม่?
A1: ใช่, Aspose.CAD เข้ากันได้กับเฟรมเวิร์ก .NET ต่าง ๆ ให้ความยืดหยุ่นตามความต้องการของการพัฒนาของคุณ

### คำถาม 2: มีใบอนุญาตชั่วคราวสำหรับ Aspose.CAD หรือไม่?
A2: มี, คุณสามารถรับใบอนุญาตชั่วคราวสำหรับ Aspose.CAD ได้จาก [temporary license page](https://purchase.aspose.com/temporary-license/)

### คำถาม 3: ฉันจะขอรับการสนับสนุนสำหรับ Aspose.CAD ได้อย่างไร?
A3: เยี่ยมชม [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) เพื่อรับการสนับสนุนจากชุมชนและความช่วยเหลือ

### คำถาม 4: มีการทดลองใช้งานฟรีสำหรับ Aspose.CAD หรือไม่?
A4: มี, คุณสามารถสำรวจการทดลองใช้งานฟรีของ Aspose.CAD ได้ที่ [Aspose.CAD free trial page](https://releases.aspose.com/)

### คำถาม 5: ฉันสามารถหาเอกสารรายละเอียดของ Aspose.CAD ได้ที่ไหน?
A5: ดูเอกสารที่ครอบคลุมของ [Aspose.CAD documentation](https://reference.aspose.com/cad/net/) สำหรับข้อมูลเชิงลึก

## คำถามที่พบบ่อย

**Q: Aspose CAD export รองรับการประมวลผลเป็นชุดของไฟล์หลายพันไฟล์หรือไม่?**  
A: ใช่ – คุณสามารถเขียนสคริปต์สแกนโฟลเดอร์และเรียกใช้ฟังก์ชันส่งออกเดียวกันสำหรับแต่ละไฟล์; ไลบรารีถูกปรับให้ทำงานได้อย่างมีประสิทธิภาพในสถานการณ์ที่ต้องประมวลผลจำนวนมาก

**Q: ฉันสามารถควบคุมระดับคุณภาพของ JPEG ได้หรือไม่?**  
A: แน่นอน – ตั้งค่า property `JpegQuality` ใน `RasterizationOptions` เป็นค่าระหว่าง 0 ถึง 100

**Q: สามารถส่งออกเลเอาต์เป็น PNG แทน JPEG ได้หรือไม่?**  
A: ได้ – เปลี่ยนรูปแบบใน `Save` เป็น `SaveFormat.Png` และปรับการตั้งค่าความโปร่งใสตามต้องการ

**Q: .NET เวอร์ชันใดที่รองรับอย่างเป็นทางการ?**  
A: Aspose.CAD รองรับ .NET Framework 4.5+, .NET Core 3.1+, .NET 5, .NET 6 และรุ่นต่อไป

**Q: Aspose CAD export จัดการกับภาพวาดขนาดใหญ่มากอย่างไร?**  
A: เอนจินสตรีมหน้าไปยังดิสก์และไม่โหลดเอกสารเต็มลงในหน่วยความจำ ทำให้สามารถประมวลผลไฟล์หลายกิกะไบต์บนฮาร์ดแวร์ที่มีสเปคปานกลางได้

---

**Last Updated:** 2026-09-09  
**Tested With:** Aspose.CAD 24.12 for .NET  
**Author:** Aspose

## บทแนะนำที่เกี่ยวข้อง

- [แปลง DXF เป็น PNG ด้วย Aspose.CAD สำหรับ .NET](/cad/net/cad-export-formats/export-cad-layouts-to-raster-image-formats/)
- [ตัวอย่าง Aspose CAD: แปลงเลเอาต์เป็นภาพ Raster ใน .NET](/cad/net/cad-drawing-manipulation/convert-layouts-to-raster-image/)
- [เรียนรู้การตั้งค่า CAD Rasterization Options – ส่งออกเลเอาต์เฉพาะเป็น PDF ด้วย Aspose.CAD](/cad/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}