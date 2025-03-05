---
title: การส่งออกเลย์เอาต์เฉพาะเป็น PDF - คู่มือ Aspose.CAD
linktitle: การส่งออกเค้าโครงเฉพาะเป็น PDF
second_title: Aspose.CAD .NET - รูปแบบไฟล์ CAD และ BIM
description: เรียนรู้วิธีส่งออกเค้าโครงเฉพาะเป็น PDF โดยใช้ Aspose.CAD สำหรับ .NET คำแนะนำทีละขั้นตอนเพื่อการผสานรวมที่ราบรื่น
type: docs
weight: 13
url: /th/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/
---
## การแนะนำ

ยินดีต้อนรับสู่คำแนะนำทีละขั้นตอนในการส่งออกเค้าโครงเฉพาะเป็น PDF โดยใช้ Aspose.CAD สำหรับ .NET Aspose.CAD เป็นไลบรารีอันทรงพลังที่ช่วยให้นักพัฒนาสามารถทำงานกับรูปแบบไฟล์ CAD ได้อย่างราบรื่น ในบทช่วยสอนนี้ เราจะเน้นที่การส่งออกเค้าโครงเฉพาะจากไฟล์ DWG เป็น PDF โดยใช้ Aspose.CAD ในสภาพแวดล้อม .NET

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเจาะลึกบทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

-  Aspose.CAD สำหรับไลบรารี .NET: ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้งไลบรารี Aspose.CAD แล้ว คุณสามารถดาวน์โหลดได้[ที่นี่](https://releases.aspose.com/cad/net/).

- สภาพแวดล้อมการพัฒนา: ตั้งค่าสภาพแวดล้อมการพัฒนา .NET เช่น Visual Studio

## นำเข้าเนมสเปซ

ในโปรเจ็กต์ .NET ของคุณ ให้นำเข้าเนมสเปซที่จำเป็นสำหรับ Aspose.CAD:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## ขั้นตอนที่ 1: โหลดไฟล์ DWG

```csharp
// เส้นทางไปยังไดเร็กทอรีเอกสาร
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";

using (Image image = Image.Load(sourceFilePath))
{
    // รหัสของคุณสำหรับขั้นตอนต่อไปอยู่ที่นี่
}
```

## ขั้นตอนที่ 2: ตั้งค่า CadRasterizationOptions

```csharp
// สร้างอินสแตนซ์ของ CadRasterizationOptions และตั้งค่าคุณสมบัติต่างๆ
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
```

## ขั้นตอนที่ 3: ระบุชื่อเค้าโครง

```csharp
// ระบุชื่อเค้าโครงที่ต้องการ
rasterizationOptions.Layouts = new string[] { "Layout1" };
```

## ขั้นตอนที่ 4: สร้าง PdfOptions

```csharp
// สร้างอินสแตนซ์ของ PdfOptions
PdfOptions pdfOptions = new PdfOptions();
// ตั้งค่าคุณสมบัติ VectorRasterizationOptions
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## ขั้นตอนที่ 5: ส่งออกเป็น PDF

```csharp
MyDir = MyDir + "ExportSpecificLayoutToPDF_out.pdf";
// ส่งออก DWG เป็น PDF
image.Save(MyDir, pdfOptions);
```

## ขั้นตอนที่ 6: แสดงข้อความแสดงความสำเร็จ

```csharp
// แสดงข้อความแสดงความสำเร็จ
Console.WriteLine("\nThe DWG file with a specific layout exported successfully to PDF.\nFile saved at " + MyDir);
```

## บทสรุป

ยินดีด้วย! คุณได้เรียนรู้วิธีส่งออกเค้าโครงเฉพาะเป็น PDF โดยใช้ Aspose.CAD สำหรับ .NET เรียบร้อยแล้ว คู่มือนี้ให้คำแนะนำโดยละเอียด เพื่อให้มั่นใจว่าคุณสามารถรวมฟังก์ชันการทำงานนี้เข้ากับโปรเจ็กต์ของคุณได้อย่างง่ายดาย

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถส่งออกหลายเค้าโครงพร้อมกันได้หรือไม่

 A1: ใช่ เพียงแค่แก้ไข`Layouts` อาร์เรย์ในขั้นตอนที่ 3 เพื่อรวมชื่อของเค้าโครงที่ต้องการทั้งหมด

### คำถามที่ 2: Aspose.CAD สามารถใช้งานร่วมกับไฟล์ CAD รูปแบบอื่นได้หรือไม่

ตอบ 2: ใช่ Aspose.CAD รองรับรูปแบบ CAD หลากหลาย รวมถึง DWG, DXF, DWF และอื่นๆ

### คำถามที่ 3: ฉันจะปรับการตั้งค่าเอาต์พุต PDF ได้อย่างไร

 A3: สำรวจคุณสมบัติของ`CadRasterizationOptions` ในขั้นตอนที่ 2 สำหรับตัวเลือกการปรับแต่ง

### คำถามที่ 4: ฉันจะหาเอกสารประกอบ Aspose.CAD เพิ่มเติมได้จากที่ไหน

 A4: เยี่ยมชม[เอกสารประกอบ](https://reference.aspose.com/cad/net/) เพื่อข้อมูลเชิงลึก

### คำถามที่ 5: มีการทดลองใช้ฟรีหรือไม่?

 A5: ได้ คุณสามารถเข้าถึงรุ่นทดลองใช้ฟรีได้[ที่นี่](https://releases.aspose.com/).