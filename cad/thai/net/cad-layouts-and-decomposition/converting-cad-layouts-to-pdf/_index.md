---
title: การแปลงเค้าโครง CAD เป็น PDF - บทช่วยสอน Aspose.CAD
linktitle: การแปลงเค้าโครง CAD เป็น PDF
second_title: Aspose.CAD .NET - รูปแบบไฟล์ CAD และ BIM
description: แปลงเค้าโครง CAD เป็น PDF ได้อย่างง่ายดายด้วย Aspose.CAD สำหรับ .NET ปฏิบัติตามคำแนะนำทีละขั้นตอนของเราเพื่อการบูรณาการที่ราบรื่น
weight: 10
url: /th/net/cad-layouts-and-decomposition/converting-cad-layouts-to-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# การแปลงเค้าโครง CAD เป็น PDF - บทช่วยสอน Aspose.CAD

## การแนะนำ

คุณต้องการแปลงเค้าโครง CAD ของคุณเป็น PDF ได้อย่างราบรื่นหรือไม่? Aspose.CAD สำหรับ .NET มอบโซลูชันที่แข็งแกร่งเพื่อทำให้กระบวนการนี้มีประสิทธิภาพและตรงไปตรงมา ในบทช่วยสอนนี้ เราจะแนะนำคุณตลอดขั้นตอนต่างๆ โดยใช้ Aspose.CAD ซึ่งเป็น API อันทรงพลังที่ช่วยให้นักพัฒนาทำงานกับไฟล์ CAD ได้อย่างง่ายดาย

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเข้าสู่บทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

-  Aspose.CAD สำหรับ .NET: ดาวน์โหลดและติดตั้งไลบรารี คุณสามารถหามันได้[ที่นี่](https://releases.aspose.com/cad/net/).

- สภาพแวดล้อม .NET: ตรวจสอบให้แน่ใจว่าคุณมีสภาพแวดล้อมการพัฒนา .NET ที่ใช้งานได้

- ไฟล์ CAD ตัวอย่าง: เตรียมไฟล์ CAD ตัวอย่างให้พร้อมสำหรับการแปลง สำหรับบทช่วยสอนนี้ เราจะใช้ "conic_pyramid.dxf"

## นำเข้าเนมสเปซ

เริ่มต้นด้วยการนำเข้าเนมสเปซที่จำเป็นลงในโปรเจ็กต์ .NET ของคุณ ขั้นตอนนี้ช่วยให้แน่ใจว่าคุณสามารถเข้าถึงฟังก์ชัน Aspose.CAD ได้

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
using Aspose.CAD.FileFormats.Cad;
```

## ขั้นตอนที่ 1: ตั้งค่าโครงการของคุณ

เริ่มต้นด้วยการตั้งค่าโครงการ .NET ของคุณ สร้างโปรเจ็กต์ใหม่หรือเปิดโปรเจ็กต์ที่มีอยู่ซึ่งคุณต้องการใช้การแปลง CAD เป็น PDF

## ขั้นตอนที่ 2: กำหนดเส้นทางไฟล์ CAD ต้นทาง

ระบุเส้นทางไปยังไฟล์ CAD ของคุณ ในตัวอย่างของเรา ไฟล์ต้นฉบับคือ "conic_pyramid.dxf"

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";
```

## ขั้นตอนที่ 3: โหลดไฟล์ CAD

สร้างอินสแตนซ์ของคลาส CadImage และโหลดไฟล์ CAD ลงในแอปพลิเคชัน

```csharp
using (Aspose.CAD.Image cadImage = (Aspose.CAD.Image)Image.Load(sourceFilePath))
```

## ขั้นตอนที่ 4: กำหนดค่าตัวเลือกการแรสเตอร์

กำหนดค่าตัวเลือกการแรสเตอร์เพื่อปรับแต่งเอาต์พุต PDF ตั้งค่าขนาดหน้า มาตราส่วนเค้าโครง และพารามิเตอร์อื่นๆ ที่เกี่ยวข้อง

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
// ตัวเลือกการกำหนดค่าอื่นๆ...
```

## ขั้นตอนที่ 5: ตั้งค่าเค้าโครง

ระบุเค้าโครงที่คุณต้องการรวมไว้ใน PDF ในตัวอย่างนี้ เราใช้เค้าโครง "แบบจำลอง"

```csharp
rasterizationOptions.Layouts = new string[] { "Model" };
```

## ขั้นตอนที่ 6: กำหนดตัวเลือก PDF

สร้างอินสแตนซ์ของคลาส PdfOptions และเชื่อมโยงกับตัวเลือกการแรสเตอร์

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## ขั้นตอนที่ 7: ตั้งค่าตัวเลือกกราฟิก

กำหนดค่าตัวเลือกกราฟิกสำหรับ PDF รวมถึงโหมดการปรับให้เรียบ การแสดงข้อความ และการแก้ไข

```csharp
rasterizationOptions.GraphicsOptions.SmoothingMode = SmoothingMode.HighQuality;
rasterizationOptions.GraphicsOptions.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
rasterizationOptions.GraphicsOptions.InterpolationMode = InterpolationMode.HighQualityBicubic;
```

## ขั้นตอนที่ 8: บันทึกเป็น PDF

ระบุเส้นทางเอาต์พุตสำหรับไฟล์ PDF และบันทึกเค้าโครง CAD เป็น PDF

```csharp
MyDir = MyDir + "CADLayoutsToPDF_out.pdf";
cadImage.Save(MyDir, pdfOptions);
```

## บทสรุป

ยินดีด้วย! คุณได้แปลงเค้าโครง CAD เป็น PDF โดยใช้ Aspose.CAD สำหรับ .NET สำเร็จแล้ว บทช่วยสอนนี้ให้คำแนะนำที่ครอบคลุมสำหรับนักพัฒนาที่ต้องการปรับปรุงกระบวนการนี้ในแอปพลิเคชันของตน

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถแปลงเค้าโครง CAD หลายรายการพร้อมกันได้หรือไม่

 A1: ได้ คุณสามารถระบุหลายเค้าโครงในไฟล์ได้`Layouts` อาร์เรย์เพื่อรวมไว้ใน PDF

### คำถามที่ 2: รองรับรูปแบบไฟล์ CAD หรือไม่

A2: Aspose.CAD สำหรับ .NET รองรับรูปแบบ CAD หลากหลาย รวมถึง DWG และ DXF

### คำถามที่ 3: ฉันจะปรับแต่งลักษณะที่ปรากฏของเอาต์พุต PDF ได้อย่างไร

A3: ใช้ตัวเลือกแรสเตอร์และกราฟิกที่มีให้เพื่อปรับแต่งเอาต์พุต PDF ตามความต้องการของคุณ

### คำถามที่ 4: มี Aspose.CAD สำหรับ .NET รุ่นทดลองใช้งานหรือไม่

 A4: ใช่ คุณสามารถสำรวจคุณลักษณะต่างๆ ได้ด้วย[รุ่นทดลองใช้ฟรี](https://releases.aspose.com/).

### คำถามที่ 5: ฉันสามารถขอความช่วยเหลือหรือถามคำถามได้ที่ไหน?

A5: เยี่ยมชม[ฟอรั่ม Aspose.CAD](https://forum.aspose.com/c/cad/19) เพื่อขอความช่วยเหลือและหารือ
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
