---
date: 2026-08-23
description: เรียนรู้วิธีสร้าง viewport dwg c# ด้วย Aspose.CAD คู่มือนี้ครอบคลุมการ
  loading ไฟล์ DWG, การ configuring rasterization, การ defining viewport, และการ saving
  ผลลัพธ์เป็น PDF.
keywords:
- create viewport dwg c#
- render dwg c#
- aspose.cad .net
lastmod: 2026-08-23
linktitle: การ Rendering เอกสาร DWG ด้วย C#
og_description: เรียนรู้วิธีสร้าง viewport dwg c# ด้วย Aspose.CAD ใน .NET คู่มือขั้นตอนนี้แสดงการ
  loading, การ rasterizing, การ defining viewports, และการ saving ไปยัง PDF.
og_image_alt: Guide showing how to create viewport dwg c# with Aspose.CAD in .NET
og_title: วิธีสร้าง viewport dwg c# ด้วย Aspose.CAD สำหรับ .NET
schemas:
- author: Aspose
  dateModified: '2026-08-23'
  description: Learn how to create viewport dwg c# using Aspose.CAD. This guide covers
    loading a DWG file, configuring rasterization, defining a viewport, and saving
    the result as PDF.
  headline: How to create viewport dwg c# with Aspose.CAD for .NET
  type: TechArticle
- questions:
  - answer: Load the DWG file with `CadImage.Load`.
    question: What is the first step?
  - answer: '`Viewport` inside `CadRasterizationOptions`.'
    question: Which class defines the view area?
  - answer: Yes, using `PdfOptions` after rasterization.
    question: Can I output to PDF?
  - answer: A commercial license is required; a free trial works for evaluation.
    question: Do I need a license for production?
  - answer: Absolutely – Aspose.CAD works with .NET Framework, .NET Core, and .NET 5/6.
    question: Is .NET Core supported?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- create viewport dwg c#
- Aspose.CAD
- C# CAD rendering
- DWG to PDF
- CAD viewports
title: วิธีสร้าง viewport dwg c# ด้วย Aspose.CAD สำหรับ .NET
url: /th/net/image-manipulation-and-rendering/rendering-dwg-documents/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# การเรนเดอร์เอกสาร DWG ใน C# – สร้าง viewport dwg c# บทแนะนำ

## บทนำ

ในบทแนะนำที่ครอบคลุมนี้ คุณจะได้เรียนรู้วิธี **create viewport dwg c#** ด้วย Aspose.CAD และเรนเดอร์ไฟล์ DWG เป็น PDF ไม่ว่าคุณจะต้องการสกัดเลย์เอาต์เฉพาะ, สร้างแผ่นพิมพ์ที่พิมพ์ได้, หรือฝังมุมมอง CAD ในรายงาน การควบคุม viewport จะให้การควบคุมการเรนเดอร์ที่แม่นยำ Aspose.CAD รองรับ **20+ CAD formats** และสามารถประมวลผลไฟล์ที่มีพัน ๆ เอนทิตีโดยไม่ต้องโหลดเอกสารทั้งหมดเข้าสู่หน่วยความจำ ทำให้เหมาะสำหรับแอปพลิเคชัน .NET ที่มีประสิทธิภาพสูง

## คำตอบเร็ว
- **ขั้นตอนแรกคืออะไร?** Load the DWG file with `CadImage.Load`.
- **คลาสใดกำหนดพื้นที่มุมมอง?** `Viewport` inside `CadRasterizationOptions`.
- **ฉันสามารถส่งออกเป็น PDF ได้หรือไม่?** Yes, using `PdfOptions` after rasterization.
- **ฉันต้องการใบอนุญาตสำหรับการผลิตหรือไม่?** A commercial license is required; a free trial works for evaluation.
- **.NET Core รองรับหรือไม่?** Absolutely – Aspose.CAD works with .NET Framework, .NET Core, and .NET 5/6.

## ข้อกำหนดเบื้องต้น

- ความรู้พื้นฐานของการเขียนโปรแกรม C#.
- ติดตั้ง Visual Studio (เวอร์ชันล่าสุดใดก็ได้).
- ไลบรารี Aspose.CAD ถูกเพิ่มในโปรเจคของคุณ คุณสามารถดาวน์โหลดได้จาก [Aspose.CAD download page](https://releases.aspose.com/cad/net/).
- ไฟล์ตัวอย่าง DWG เช่น **Bottom_plate.dwg** เพื่อทำตามขั้นตอน.

## นำเข้า namespace

เพิ่มคำสั่ง `using` ที่จำเป็นที่ส่วนบนของไฟล์ C# ของคุณเพื่อให้คอมไพเลอร์สามารถค้นหา type ของ Aspose.CAD ได้.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.FileFormats.Cad;
```

เมื่อสภาพแวดล้อมพร้อมแล้ว เราจะเดินผ่านการทำงานทีละขั้นตอน.

## วิธีสร้าง viewport dwg c#?

เพื่อสร้าง viewport แบบกำหนดเอง ก่อนอื่นให้โหลดไฟล์ DWG เข้าไปในอ็อบเจ็กต์ `CadImage` จากนั้นกำหนดค่า `CadRasterizationOptions` ด้วยเลย์เอาต์และสเกลที่ต้องการ กำหนดพื้นที่ที่ต้องการแสดง, สร้างอ็อบเจ็กต์ `CadVportTableObject` ด้วยศูนย์กลาง, ความสูงและอัตราส่วนที่คำนวณ, แทนที่ viewport ที่ใช้งานอยู่, ตั้งค่า PDF options ตามต้องการ, และสุดท้ายบันทึกผลลัพธ์.

## ขั้นตอนที่ 1: โหลดไฟล์ dwg

`CadImage.Load` โหลดไฟล์ DWG เข้าไปในอ็อบเจ็กต์ `CadImage` ซึ่งเป็นตัวแทนของการวาด CAD ในหน่วยความจำ.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Your code for loading the DWG file goes here.
}
```

## ขั้นตอนที่ 2: กำหนดค่า rasterization options

`CadRasterizationOptions` ระบุวิธีการแปลงภาพ CAD เป็น raster รวมถึงการเลือกเลย์เอาต์, การสเกล, และขนาดผลลัพธ์.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new string[] { "Model" };
rasterizationOptions.NoScaling = true;
// Additional rasterization configurations can be added here.
```

## ขั้นตอนที่ 3: กำหนดพื้นที่ที่จะวาด

`Point` กำหนดพิกัด X และ Y ของมุมบนซ้ายของพื้นที่ที่ต้องการเรนเดอร์.

```csharp
Point topLeft = new Point(6156, 7053);
double width = 3108;
double height = 2489;
```

## ขั้นตอนที่ 4: สร้าง viewport ใหม่

`CadVportTableObject` แสดงถึงอ็อบเจ็กต์ viewport ที่ควบคุมพื้นที่ที่มองเห็นและอัตราส่วนของการเรนเดอร์ภาพวาด.

```csharp
CadVportTableObject newView = new CadVportTableObject();
newView.Name.Value = "*Active";
newView.CenterPoint.X = topLeft.X + width / 2f;
newView.CenterPoint.Y = topLeft.Y - height / 2f;
newView.ViewHeight.Value = height;
newView.ViewAspectRatio.Value = width / height;
```

## ขั้นตอนที่ 5: แทนที่ viewport ที่ใช้งานอยู่

ลูปนี้จะแทนที่ viewport ที่ใช้งานอยู่ด้วย viewport ใหม่ที่สร้างขึ้นเพื่อใช้การตั้งค่ามุมมองที่กำหนดเอง.

```csharp
for (int i = 0; i < cadImage.ViewPorts.Count; i++)
{
    CadVportTableObject currentView = (CadVportTableObject)(cadImage.ViewPorts[i]);
    if ((currentView.Name.Value == null && cadImage.ViewPorts.Count == 1) ||
    string.Equals(currentView.Name.Value.ToLowerInvariant(), "*active"))
    {
        cadImage.ViewPorts[i] = newView;
        break;
    }
}
```

## ขั้นตอนที่ 6: กำหนดค่า PDF options

`PdfOptions` กำหนดพารามิเตอร์การส่งออก PDF เช่น การบีบอัดและเมตาดาต้า.

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## ขั้นตอนที่ 7: บันทึก DWG ที่เรนเดอร์เป็น PDF

`image.Save` เขียนภาพที่เรนเดอร์ลงไฟล์โดยใช้ตัวเลือกรูปแบบที่ระบุ.

```csharp
cadImage.Save(MyDir, pdfOptions);
```

## ทำไมต้องใช้ viewport แบบกำหนดเองเมื่อเรนเดอร์ DWG?

viewport แบบกำหนดเองช่วยให้คุณแยกเลย์เอาต์หรือพื้นที่เฉพาะ ลดขนาดไฟล์และเพิ่มความเร็วการเรนเดอร์ Aspose.CAD สามารถเรนเดอร์ DWG 300 หน้าในเวลาน้อยกว่า 2 วินาทีเมื่อใช้ viewport ที่มุ่งเน้น เมื่อเทียบกับการเรนเดอร์ภาพทั้งหมดที่อาจใช้เวลานานกว่าหลายวินาที.

## ปัญหาทั่วไปและวิธีแก้

- **ผลลัพธ์เป็นสีขาว** – ตรวจสอบให้แน่ใจว่าพิกัดของ viewport อยู่ภายในขอบเขตของการวาด; ใช้ `CadImage.Size` เพื่อตรวจสอบขอบเขต.
- **เลเยอร์หาย** – ตั้งค่า `CadRasterizationOptions.Layouts` ให้เป็นชื่อเลย์เอาต์ที่ถูกต้อง; มิฉะนั้นเลย์เอาต์เริ่มต้นอาจว่างเปล่า.
- **ประสิทธิภาพช้าลง** – ปิดการทำ anti‑aliasing ใน `CadRasterizationOptions` หากคุณต้องการเพียงการพรีวิวอย่างรวดเร็ว.

## คำถามที่พบบ่อย

### Q1: ฉันสามารถใช้ Aspose.CAD กับรูปแบบไฟล์ CAD อื่นได้หรือไม่?
A1: ใช่, Aspose.CAD รองรับรูปแบบต่าง ๆ รวมถึง DWG, DXF, DWF, และประเภท CAD เพิ่มเติมกว่า 20 ประเภท.

### Q2: Aspose.CAD เข้ากันได้กับ .NET Core หรือไม่?
A2: ใช่, Aspose.CAD ทำงานกับ .NET Framework, .NET Core, และรุ่น .NET ล่าสุด.

### Q3: ฉันจะจัดการกับเลย์เอาต์ต่าง ๆ ในไฟล์ DWG อย่างไร?
A3: ระบุเลย์เอาต์ที่ต้องการโดยใช้ property `Layouts` ของ `CadRasterizationOptions` ก่อนทำการเรนเดอร์.

### Q4: มีข้อพิจารณาเรื่องลิขสิทธิ์สำหรับการใช้ Aspose.CAD หรือไม่?
A4: สำหรับรายละเอียดลิขสิทธิ์ โปรดเยี่ยมชม [Aspose.CAD licensing page](https://purchase.aspose.com/buy).

### Q5: ฉันจะหาแหล่งสนับสนุนเพิ่มเติมได้จากที่ไหน?
A5: เยี่ยมชม [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) เพื่อรับความช่วยเหลือจากชุมชนและการสนทนา.

### Q6: ฉันสามารถเรนเดอร์โดยตรงเป็น PNG แทน PDF ได้หรือไม่?
A6: ใช่, เปลี่ยน `PdfOptions` เป็น `PngOptions` และเรียก `image.Save("output.png", pngOptions)`.

### Q7: ฉันจะฝังภาพที่เรนเดอร์ลงในแอปพลิเคชัน Windows Forms อย่างไร?
A7: โหลดภาพที่บันทึกไว้เข้าสู่คอนโทรล `PictureBox` โดยใช้ `Image.FromFile("output.png")`.

## สรุป

คุณตอนนี้รู้วิธี **create viewport dwg c#** และเรนเดอร์ไฟล์ DWG เป็น PDF (หรือรูปแบบ raster อื่น) ด้วย Aspose.CAD การเชี่ยวชาญการจัดการ viewport จะให้การควบคุมผลลัพธ์ภาพอย่างละเอียด ซึ่งจำเป็นสำหรับการสร้างภาพวิศวกรรมที่แม่นยำ, รายงาน, หรือภาพย่อ สำรวจการตั้งค่า rasterization เพิ่มเติม, ทดลองกับรูปแบบผลลัพธ์ต่าง ๆ, และรวมโค้ดเข้ากับบริการ .NET ขนาดใหญ่หรือยูทิลิตี้บนเดสก์ท็อป.

---

**อัปเดตล่าสุด:** 2026-08-23  
**ทดสอบด้วย:** Aspose.CAD 24.11 for .NET  
**ผู้เขียน:** Aspose

## บทแนะนำที่เกี่ยวข้อง

- [วิธีตั้งค่า Viewport ขณะแปลง DWG เป็น PDF พร้อมพิกัดใน C# - บทแนะนำ Aspose.CAD](/cad/net/conversion-and-export/converting-dwg-to-pdf-with-coordinates/)
- [เรียนรู้การตั้งค่า CAD Rasterization Options – ส่งออกเลย์เอาต์เฉพาะเป็น PDF ด้วย Aspose.CAD](/cad/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/)
- [วิธีแปลง DWG เป็น PDF และภาพ Raster ด้วย Aspose.CAD สำหรับ .NET](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}