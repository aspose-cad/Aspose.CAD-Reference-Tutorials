---
title: การแปลง DWG เฉพาะเป็นรูปภาพใน C # - คู่มือ Aspose.CAD
linktitle: การแปลง DWG เฉพาะเป็นรูปภาพใน C #
second_title: Aspose.CAD .NET - รูปแบบไฟล์ CAD และ BIM
description: สำรวจ Aspose.CAD สำหรับ .NET แปลง DWG เป็นรูปภาพใน C# ได้อย่างง่ายดาย คู่มือที่ครอบคลุมพร้อมตัวอย่างโค้ด
type: docs
weight: 15
url: /th/net/image-manipulation-and-rendering/converting-particular-dwg-to-image/
---
## การแนะนำ

ในโลกที่มีการเปลี่ยนแปลงตลอดเวลาของการพัฒนาซอฟต์แวร์ การจัดการไฟล์ CAD อย่างมีประสิทธิภาพถือเป็นสิ่งสำคัญ Aspose.CAD สำหรับ .NET กลายเป็นโซลูชันอันทรงพลัง ช่วยให้นักพัฒนามีชุดเครื่องมือที่มีประสิทธิภาพในการจัดการและแปลงไฟล์ CAD ได้อย่างราบรื่น ในบทช่วยสอนนี้ เราจะเจาะลึกขั้นตอนการแปลงไฟล์ DWG ที่เฉพาะเจาะจงไปเป็นรูปภาพโดยใช้ C#

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเริ่มการเดินทางเขียนโค้ดนี้ ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

- Visual Studio: สภาพแวดล้อมการพัฒนาเพื่อเขียนและรันโค้ด C#
-  Aspose.CAD สำหรับ .NET: ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้งไลบรารีแล้ว คุณสามารถค้นหาลิงค์ดาวน์โหลด[ที่นี่](https://releases.aspose.com/cad/net/).
- - ไฟล์ DWG: เตรียมไฟล์ DWG พร้อมสำหรับการแปลง คุณสามารถใช้ไฟล์ตัวอย่าง "visualization_-_conference_room.dwg" สำหรับคำแนะนำนี้

## นำเข้าเนมสเปซ

ในโค้ด C# ของคุณ ตรวจสอบให้แน่ใจว่าได้นำเข้าเนมสเปซที่จำเป็นสำหรับการทำงานกับ Aspose.CAD:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## ขั้นตอนที่ 1: โหลดไฟล์ DWG

เริ่มต้นด้วยการโหลดไฟล์ DWG ลงในเฟรมเวิร์ก Aspose.CAD:

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";
var cadImage = (CadImage)Aspose.CAD.Image.Load(sourceFilePath);
```

## ขั้นตอนที่ 2: กรองเอนทิตี

ถัดไป กรองเอนทิตีในไฟล์ DWG ในตัวอย่างนี้ เราจะเน้นที่การแยกเอนทิตีข้อความ:

```csharp
CadBaseEntity[] entities = cadImage.Entities;
List<CadBaseEntity> filteredEntities = new List<CadBaseEntity>();

foreach (CadBaseEntity baseEntity in entities)
{
    // การเลือกหรือการกรองเอนทิตี
    if (baseEntity.TypeName == CadEntityTypeName.TEXT)
    {
        filteredEntities.Add(baseEntity);
    }
}

cadImage.Entities = filteredEntities.ToArray();
```

## ขั้นตอนที่ 3: ตั้งค่าตัวเลือกการแรสเตอร์

 สร้างอินสแตนซ์ของ`CadRasterizationOptions` และกำหนดคุณสมบัติสำหรับการแปลงรูปภาพ:

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions rasterizationOptions =
    new Aspose.CAD.ImageOptions.CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.AutomaticLayoutsScaling = true;
```

## ขั้นตอนที่ 4: ตั้งค่าตัวเลือก PDF

 สร้างอินสแตนซ์ของ`PdfOptions` และกำหนดตัวเลือกการแรสเตอร์:

```csharp
Aspose.CAD.ImageOptions.PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## ขั้นตอนที่ 5: บันทึกเป็น PDF

สุดท้าย ให้บันทึกภาพที่แปลงแล้วเป็นไฟล์ PDF:

```csharp
string outFile = MyDir + "result_out_generated.pdf";
cadImage.Save(outFile, pdfOptions);
```

## บทสรุป

ยินดีด้วย! คุณได้แปลงไฟล์ DWG เฉพาะเป็นรูปภาพโดยใช้ Aspose.CAD สำหรับ .NET สำเร็จแล้ว บทช่วยสอนนี้ให้ข้อมูลเชิงลึกเกี่ยวกับความสามารถอันทรงพลังของไลบรารี ช่วยให้นักพัฒนาสามารถทำงานกับไฟล์ CAD ในแอปพลิเคชันของตนได้อย่างมีประสิทธิภาพ

## คำถามที่พบบ่อย

### คำถามที่ 1: Aspose.CAD เข้ากันได้กับไฟล์ DWG ทุกเวอร์ชันหรือไม่

A1: Aspose.CAD รองรับไฟล์ DWG หลากหลายเวอร์ชัน จึงรับประกันความเข้ากันได้กับซอฟต์แวร์ CAD หลากหลายประเภท

### คำถามที่ 2: ฉันสามารถปรับแต่งตัวเลือกการแรสเตอร์สำหรับเอาต์พุตต่างๆ ได้หรือไม่

A2: แน่นอน! Aspose.CAD ให้ความยืดหยุ่นในการปรับตัวเลือกการแรสเตอร์เพื่อตอบสนองความต้องการเฉพาะของคุณสำหรับรูปแบบเอาต์พุตที่แตกต่างกัน

### คำถามที่ 3: ฉันจะหาตัวอย่างและเอกสารประกอบเพิ่มเติมได้ที่ไหน

 A3: สำรวจอย่างครอบคลุม[เอกสาร Aspose.CAD](https://reference.aspose.com/cad/net/) สำหรับตัวอย่างเพิ่มเติมและคำแนะนำเชิงลึก

### คำถามที่ 4: Aspose.CAD มีรุ่นทดลองใช้ฟรีหรือไม่

 A4: ได้ คุณสามารถทดลองใช้ฟรีได้[ที่นี่](https://releases.aspose.com/) เพื่อสัมผัสประสบการณ์เต็มศักยภาพของ Aspose.CAD

### คำถามที่ 5: ฉันจะรับการสนับสนุนหรือเชื่อมต่อกับชุมชนเพื่อขอความช่วยเหลือได้อย่างไร

A5: เยี่ยมชม[ฟอรั่ม Aspose.CAD](https://forum.aspose.com/c/cad/19) สำหรับการสนับสนุน การอภิปราย และความร่วมมือกับชุมชน