---
date: 2026-08-17
description: เรียนรู้วิธีเพิ่ม image ไปยังไฟล์ dwg ด้วย C# และ Aspose.CAD สำหรับ .NET
  คู่มือนี้จะพาคุณผ่านขั้นตอนการนำเข้า images, การกำหนดจุดแทรก, และการส่งออกเป็น PDF
keywords:
- add image to dwg
- convert dwg to pdf
- set insertion point dwg
- embed png in dwg
- save dwg as pdf
lastmod: 2026-08-17
linktitle: การนำเข้า Images ไปยังไฟล์ DWG ด้วย C#
og_description: เรียนรู้วิธีเพิ่ม image ไปยังไฟล์ dwg ด้วย C# บทเรียนนี้ครอบคลุมการนำเข้า
  images, การกำหนดจุดแทรก, และการแปลง dwg เป็น pdf ด้วย Aspose.CAD
og_image_alt: Guide showing C# code to embed an image into a DWG file using Aspose.CAD
og_title: วิธีเพิ่ม image ไปยังไฟล์ dwg ด้วย C# โดยใช้ Aspose.CAD
schemas:
- author: Aspose
  dateModified: '2026-08-17'
  description: Learn how to add image to dwg files using C# and Aspose.CAD for .NET.
    This guide walks you through importing images, setting insertion points, and exporting
    to PDF.
  headline: How to add image to dwg files with C# using Aspose.CAD
  type: TechArticle
- description: Learn how to add image to dwg files using C# and Aspose.CAD for .NET.
    This guide walks you through importing images, setting insertion points, and exporting
    to PDF.
  name: How to add image to dwg files with C# using Aspose.CAD
  steps:
  - name: set up your document directory
    text: Prepare the folder that contains the source DWG and the image you want to
      embed.
  - name: load the dwg file
    text: The `CadImage` class represents a DWG drawing and provides access to its
      entities, layers, and metadata.
  - name: define the image properties
    text: Create an `Image` object that points to the raster file (e.g., PNG) and
      specify its format.
  - name: set insertion point dwg and vectors
    text: Specify where the image should appear inside the drawing and how it should
      be scaled. The insertion point is defined by a 2‑D coordinate, while the vectors
      control width and height.
  - name: create and configure the raster image
    text: Instantiate a `RasterImage` object, assign the image data, and set any additional
      rendering options.
  - name: add image to dwg file
    text: Insert the configured raster image into the DWG’s entities collection so
      it becomes part of the drawing.
  - name: save as pdf (export dwg to pdf)
    text: After embedding the image you can **convert dwg to pdf** or **save dwg as
      pdf** with a single call. This is useful for sharing the drawing with stakeholders
      who don’t have CAD software.
  type: HowTo
- questions:
  - answer: The core library is .NET‑specific, but Aspose offers equivalent APIs for
      Java, Python and other platforms.
    question: Can I use Aspose.CAD for .NET with other programming languages?
  - answer: Yes, you can explore a free trial on the [Aspose free trial page](https://releases.aspose.com/).
    question: Is a free trial available for Aspose.CAD?
  - answer: The documentation is available in the [Aspose.CAD .NET API reference](https://reference.aspose.com/cad/net/).
    question: Where can I find detailed documentation for Aspose.CAD?
  - answer: Visit the [temporary license page](https://purchase.aspose.com/temporary-license/)
      to get a temporary license.
    question: How do I obtain a temporary license for Aspose.CAD?
  - answer: Yes, you can seek support and engage with the community in the [Aspose.CAD
      community forum](https://forum.aspose.com/c/cad/19).
    question: Are there community forums for Aspose.CAD support?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- CAD
- Aspose.CAD
- C# image processing
- DWG manipulation
title: วิธีเพิ่ม image ไปยังไฟล์ dwg ด้วย C# โดยใช้ Aspose.CAD
url: /th/net/image-manipulation-and-rendering/importing-images-into-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีเพิ่มรูปภาพลงในไฟล์ dwg ด้วย C# โดยใช้ Aspose.CAD

## บทนำ

การเพิ่มรูปภาพลงในไฟล์ DWG เป็นความต้องการทั่วไปเมื่อคุณต้องการเสริมภาพวาด CAD ด้วยโลโก้, รูปถ่าย หรือกราฟิกเรสเตอร์ ในบทเรียนนี้คุณจะได้เรียนรู้วิธี **add image to dwg** อย่างโปรแกรมโดยใช้ C# และ Aspose.CAD สำหรับ .NET, จากนั้นอาจแปลงผลลัพธ์เป็น PDF ขั้นตอนต่าง ๆ ถูกแบ่งเป็นส่วนย่อยเพื่อให้คุณสามารถคัดลอก‑วางแต่ละส่วนลงในโปรเจกต์ของคุณได้

## คำตอบอย่างรวดเร็ว
- **ไลบรารีใดที่ทำงานนี้?** Aspose.CAD for .NET.
- **ฉันสามารถฝังไฟล์ PNG ได้หรือไม่?** ใช่ – PNG, JPEG, BMP และรูปแบบเรสเตอร์อื่น ๆ ได้รับการสนับสนุน.
- **ฉันต้องการใบอนุญาตสำหรับการพัฒนาหรือไม่?** รุ่นทดลองฟรีใช้ได้สำหรับการทดสอบ; จำเป็นต้องมีใบอนุญาตเชิงพาณิชย์สำหรับการใช้งานจริง.
- **การส่งออกเป็น PDF รองรับหรือไม่?** แน่นอน – คุณสามารถแปลง DWG ที่อัปเดตเป็น PDF ได้ในบรรทัดเดียว.
- **เวอร์ชัน .NET ใดที่เข้ากันได้?** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6/7.

## DWG คืออะไร?

DWG เป็นรูปแบบไบนารีเนทีฟของไฟล์ Autodesk AutoCAD ที่เก็บข้อมูลเรขาคณิตเวกเตอร์, เลเยอร์, และเมตาดาต้า มันถูกใช้กันอย่างกว้างขวางในสถาปัตยกรรม, วิศวกรรม, และการก่อสร้าง และ Aspose.CAD สามารถอ่านและเขียนรูปแบบนี้ได้โดยไม่ต้องติดตั้ง AutoCAD

## ทำไมต้องเพิ่มรูปภาพลงใน dwg ด้วย Aspose.CAD?

Aspose.CAD รองรับ **50+** รูปแบบอินพุตและเอาต์พุต, สามารถประมวลผลไฟล์ที่ใหญ่กว่า 500 MB โดยไม่ต้องโหลดเอกสารทั้งหมดเข้าสู่หน่วยความจำ, และให้ API ที่กำหนดผลลัพธ์ได้อย่างแน่นอนซึ่งทำงานในสภาพแวดล้อมเซิร์ฟเวอร์แบบไม่มีหัว (headless) สิ่งนี้ทำให้การประมวลผลแบบกลุ่มของภาพวาด DWG เร็วและเชื่อถือได้

## ข้อกำหนดเบื้องต้น
- ความรู้พื้นฐานเกี่ยวกับการเขียนโปรแกรม C#.
- Aspose.CAD for .NET ติดตั้งแล้ว คุณสามารถดาวน์โหลดได้จาก [หน้าโหลด Aspose.CAD สำหรับ .NET](https://releases.aspose.com/cad/net/). คุณยังสามารถสำรวจผลิตภัณฑ์ Aspose อื่น ๆ ได้บน [หน้าเผยแพร่ของ Aspose](https://releases.aspose.com/).
- สภาพแวดล้อมการพัฒนา เช่น Visual Studio 2022 หรือใหม่กว่า.

## วิธีเพิ่มรูปภาพลงใน dwg ด้วย Aspose.CAD?

โหลด DWG เป้าหมาย, สร้างอ็อบเจ็กต์ภาพเรสเตอร์ที่อธิบายรูปภาพที่ต้องการฝัง, ตั้งค่าจุดแทรกและเวกเตอร์สเกล, จากนั้นแนบภาพลงในภาพวาด สุดท้ายบันทึก DWG ที่แก้ไขหรือส่งออกโดยตรงเป็น PDF ทั้งกระบวนการใช้เพียงไม่กี่คำสั่ง API และทำงานได้ภายในไม่กี่วินาทีสำหรับภาพวาด 2‑หน้าแบบทั่วไป

### นำเข้าเนมสเปซ
รวมเนมสเปซที่เปิดเผยคลาส CAD ที่คุณต้องการใช้

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

### ขั้นตอนที่ 1: ตั้งค่าไดเรกทอรีเอกสารของคุณ
เตรียมโฟลเดอร์ที่มีไฟล์ DWG ต้นฉบับและรูปภาพที่คุณต้องการฝัง

```csharp
string MyDir = "Your Document Directory";
```

### ขั้นตอนที่ 2: โหลดไฟล์ dwg
คลาส `CadImage` แสดงถึงการวาด DWG และให้เข้าถึงเอนทิตี้, เลเยอร์, และเมตาดาต้าของมัน

```csharp
string dwgPathToFile = MyDir + "Drawing11.dwg";
CadImage cadImage1 = (CadImage)Image.Load(dwgPathToFile);
```

### ขั้นตอนที่ 3: กำหนดคุณสมบัติของรูปภาพ
สร้างอ็อบเจ็กต์ `Image` ที่ชี้ไปยังไฟล์เรสเตอร์ (เช่น PNG) และระบุรูปแบบของมัน

```csharp
CadRasterImageDef cadRasterImageDef = new CadRasterImageDef("road-sign-custom.png", 640, 562);
cadRasterImageDef.ObjectHandle = "A3B4";
```

### ขั้นตอนที่ 4: ตั้งค่าจุดแทรกใน dwg และเวกเตอร์
ระบุว่ารูปภาพควรปรากฏที่ไหนภายในภาพวาดและควรสเกลอย่างไร จุดแทรกกำหนดด้วยพิกัด 2‑D, ส่วนเวกเตอร์ควบคุมความกว้างและความสูง

```csharp
Cad3DPoint insertionPoint = new Cad3DPoint(26.77, 22.35);
Cad3DPoint uVector = new Cad3DPoint(0.0061565450840500831, 0);
Cad3DPoint vVector = new Cad3DPoint(0, 0.0061565450840500822);
```

### ขั้นตอนที่ 5: สร้างและกำหนดค่ารูปภาพเรสเตอร์
สร้างอ็อบเจ็กต์ `RasterImage`, กำหนดข้อมูลภาพ, และตั้งค่าตัวเลือกการเรนเดอร์เพิ่มเติมตามต้องการ

```csharp
CadRasterImage cadRasterImage = new CadRasterImage(cadRasterImageDef, insertionPoint, uVector, vVector);
cadRasterImage.ImageDefReference = "A3B4";
cadRasterImage.DisplayFlags = 7;
cadRasterImage.ClippingState = 0;
cadRasterImage.ClipBoundaryVertexList.Add(new Cad2DPoint(-0.5, 0.5));
cadRasterImage.ClipBoundaryVertexList.Add(new Cad2DPoint(639.5, 561.5));
```

### ขั้นตอนที่ 6: เพิ่มรูปภาพลงในไฟล์ dwg
แทรกรูปภาพเรสเตอร์ที่กำหนดค่าแล้วลงในคอลเลกชันเอนทิตี้ของ DWG เพื่อให้เป็นส่วนหนึ่งของภาพวาด

```csharp
CadImage cadImage = (CadImage)cadImage1;
cadImage.BlockEntities["*Model_Space"].AddEntity(cadRasterImage);

List<CadBaseObject> list = new List<CadBaseObject>(cadImage.Objects);
list.Add(cadRasterImageDef);
cadImage.Objects = list.ToArray();
```

### ขั้นตอนที่ 7: บันทึกเป็น pdf (ส่งออก dwg เป็น pdf)
หลังจากฝังรูปภาพคุณสามารถ **convert dwg to pdf** หรือ **save dwg as pdf** ด้วยการเรียกครั้งเดียว ซึ่งเป็นประโยชน์สำหรับการแชร์ภาพวาดกับผู้มีส่วนได้ส่วนเสียที่ไม่มีซอฟต์แวร์ CAD

```csharp
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.VectorRasterizationOptions = cadRasterizationOptions;
cadRasterizationOptions.DrawType = CadDrawTypeMode.UseObjectColor;

cadRasterizationOptions.PageHeight = 1600;
cadRasterizationOptions.PageWidth = 1600;
cadRasterizationOptions.Layouts = new string[] { "Model" };
cadImage1.Save(MyDir + "export2.pdf", pdfOptions);
```

## วิธีแปลง dwg เป็น pdf หลังจากฝังรูปภาพ?

เรียกเมธอด `Save` บนอินสแตนซ์ `CadImage`, ส่งผ่าน `SaveFormat.Pdf` และอาจแนบอ็อบเจ็กต์ `PdfOptions` เพื่อควบคุมขนาดหน้า, การเรสเตอร์ไลซ์, และเมตาดาต้า Aspose.CAD จะคงรักษาภาพเรสเตอร์ที่ฝังไว้, เลเยอร์, และน้ำหนักเส้น, สร้างไฟล์ PDF ที่แม่นยำซึ่งสามารถเปิดได้ในโปรแกรมอ่านใด ๆ การแปลงนี้ทำได้ในบรรทัดโค้ดเดียว

## ปัญหาที่พบบ่อยและวิธีแก้ไข
- **Image appears at the wrong location** – ตรวจสอบพิกัดจุดแทรกและเวกเตอร์ทิศทางอีกครั้ง; พิกัดเหล่านี้สัมพันธ์กับจุดกำเนิดของภาพวาด.
- **Large images cause memory spikes** – ใช้ตัวเลือก `Resize` บนภาพเรสเตอร์ก่อนแทรก, หรือทำงานกับสำเนาที่ความละเอียดต่ำกว่า.
- **PDF export loses vector quality** – ตรวจสอบว่าคุณบันทึกด้วย `PdfOptions` ที่รักษาข้อมูลเวกเตอร์; ภาพเรสเตอร์จะถูกฝังไว้ตามที่เป็น.

## คำถามที่พบบ่อย

**Q: ฉันสามารถใช้ Aspose.CAD สำหรับ .NET กับภาษาโปรแกรมอื่นได้หรือไม่?**  
A: ไลบรารีหลักเป็นแบบเฉพาะ .NET, แต่ Aspose มี API ที่เทียบเท่าสำหรับ Java, Python และแพลตฟอร์มอื่น ๆ

**Q: มีรุ่นทดลองฟรีสำหรับ Aspose.CAD หรือไม่?**  
A: มี, คุณสามารถสำรวจรุ่นทดลองฟรีได้บน [หน้า trial ฟรีของ Aspose](https://releases.aspose.com/)

**Q: ฉันจะหาเอกสารรายละเอียดสำหรับ Aspose.CAD ได้จากที่ไหน?**  
A: เอกสารพร้อมใช้งานใน [Aspose.CAD .NET API reference](https://reference.aspose.com/cad/net/)

**Q: ฉันจะขอรับใบอนุญาตชั่วคราวสำหรับ Aspose.CAD ได้อย่างไร?**  
A: เยี่ยมชม [หน้าใบอนุญาตชั่วคราว](https://purchase.aspose.com/temporary-license/) เพื่อรับใบอนุญาตชั่วคราว

**Q: มีฟอรั่มชุมชนสำหรับการสนับสนุน Aspose.CAD หรือไม่?**  
A: มี, คุณสามารถขอความช่วยเหลือและเข้าร่วมชุมชนได้ที่ [ฟอรั่มชุมชน Aspose.CAD](https://forum.aspose.com/c/cad/19)

---

**อัปเดตล่าสุด:** 2026-08-17  
**ทดสอบด้วย:** Aspose.CAD 24.11 for .NET  
**ผู้เขียน:** Aspose

## บทเรียนที่เกี่ยวข้อง

- [การส่งออก DWG เป็น PDF หรือรูปภาพเรสเตอร์ - คู่มือ Aspose.CAD](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)
- [การส่งออก DWG เป็นรูปแบบ DXF ใน C# - บทเรียน Aspose.CAD](/cad/net/advanced-export-techniques/exporting-dwg-to-dxf/)
- [การส่งออกเลย์เอาต์เฉพาะเป็น PDF - คู่มือ Aspose.CAD](/cad/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}