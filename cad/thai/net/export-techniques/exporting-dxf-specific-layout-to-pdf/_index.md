---
title: การส่งออกเค้าโครงเฉพาะของ DXF เป็น PDF - คู่มือ Aspose.CAD
linktitle: การส่งออกเค้าโครงเฉพาะ DXF เป็น PDF
second_title: Aspose.CAD .NET - รูปแบบไฟล์ CAD และ BIM
description: เรียนรู้วิธีส่งออกเค้าโครงเฉพาะของ DXF เป็น PDF โดยใช้ Aspose.CAD สำหรับ .NET ปฏิบัติตามคำแนะนำทีละขั้นตอนของเราเพื่อการแปลงที่มีประสิทธิภาพและมีคุณภาพสูง
type: docs
weight: 11
url: /th/net/export-techniques/exporting-dxf-specific-layout-to-pdf/
---
## การแนะนำ

ยินดีต้อนรับสู่บทช่วยสอน Aspose.CAD เกี่ยวกับการส่งออกเค้าโครงเฉพาะของ DXF ไปเป็น PDF โดยใช้คุณสมบัติอันทรงพลังของ Aspose.CAD สำหรับ .NET คำแนะนำทีละขั้นตอนนี้จะแนะนำคุณตลอดขั้นตอนการแปลงไฟล์ DXF เป็น PDF โดยเน้นไปที่เค้าโครงเฉพาะที่ชื่อว่า "Model" Aspose.CAD มอบเครื่องมือและฟังก์ชันที่มีประสิทธิภาพในการปรับปรุงกระบวนการแปลง ทำให้มั่นใจได้ถึงผลลัพธ์คุณภาพสูงสำหรับแบบร่าง CAD ของคุณ

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเข้าสู่บทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

- Aspose.CAD สำหรับ .NET: ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้งไลบรารี Aspose.CAD ในโปรเจ็กต์ .NET ของคุณ คุณสามารถดาวน์โหลดได้[ที่นี่](https://releases.aspose.com/cad/net/) และปฏิบัติตามคำแนะนำในการติดตั้งที่ให้ไว้ในเอกสารประกอบ

- สภาพแวดล้อมการพัฒนา: ตั้งค่าสภาพแวดล้อมการพัฒนา .NET ที่ใช้งานได้ รวมถึง Visual Studio หรือ IDE ที่ต้องการอื่นๆ

- ไฟล์ DXF: เตรียมไฟล์ DXF ที่คุณต้องการแปลงเป็น PDF สำหรับคำแนะนำนี้ เราจะใช้ไฟล์ตัวอย่างชื่อ "conic_pyramid.dxf"

## นำเข้าเนมสเปซ

ในโปรเจ็กต์ .NET ของคุณ ให้รวมเนมสเปซที่จำเป็นเพื่อใช้ประโยชน์จากฟังก์ชันการทำงานของ Aspose.CAD เพิ่มบรรทัดต่อไปนี้ที่จุดเริ่มต้นของโค้ดของคุณ:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
namespace Aspose.CAD.Examples.CSharp.DXF_Drawings

```

## ขั้นตอนที่ 1: โหลดไฟล์ DXF

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (Image image = Image.Load(sourceFilePath))
{
    //รหัสของคุณสำหรับขั้นตอนต่อไปจะอยู่ที่นี่
}
```

## ขั้นตอนที่ 2: ตั้งค่าตัวเลือกการแรสเตอร์

```csharp
// สร้างอินสแตนซ์ของ CadRasterizationOptions และตั้งค่าคุณสมบัติต่างๆ
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
// ระบุชื่อเค้าโครงที่ต้องการ
rasterizationOptions.Layouts = new string[] { "Model" };
```

## ขั้นตอนที่ 3: ตั้งค่าตัวเลือก PDF

```csharp
// สร้างอินสแตนซ์ของ PdfOptions
PdfOptions pdfOptions = new PdfOptions();
// ตั้งค่าคุณสมบัติ VectorRasterizationOptions
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## ขั้นตอนที่ 4: กำหนดเส้นทางเอาต์พุต

```csharp
MyDir = MyDir + "conic_pyramid_layout_out.pdf";
```

## ขั้นตอนที่ 5: ส่งออก DXF เป็น PDF

```csharp
// ส่งออก DXF เป็น PDF
image.Save(MyDir, pdfOptions);
```

## ขั้นตอนที่ 6: แสดงข้อความแสดงความสำเร็จ

```csharp
// แสดงข้อความแสดงความสำเร็จ
Console.WriteLine("\nThe DXF file with the specific layout exported successfully to PDF.\nFile saved at " + MyDir);
```

## บทสรุป

ยินดีด้วย! คุณได้เรียนรู้วิธีส่งออกไฟล์ DXF ด้วยเลย์เอาต์เฉพาะเป็น PDF โดยใช้ Aspose.CAD สำหรับ .NET เรียบร้อยแล้ว คู่มือนี้ครอบคลุมขั้นตอนสำคัญต่างๆ ตั้งแต่การโหลดไฟล์ DXF ไปจนถึงการตั้งค่าตัวเลือกการแรสเตอร์และการส่งออกเป็น PDF

## คำถามที่พบบ่อย

### คำถามที่ 1: Aspose.CAD เข้ากันได้กับไฟล์ DXF ทุกเวอร์ชันหรือไม่

 A1: Aspose.CAD รองรับไฟล์ DXF เวอร์ชันต่างๆ อ้างถึง[เอกสารประกอบ](https://reference.aspose.com/cad/net/) สำหรับรายการเวอร์ชันที่รองรับ

### คำถามที่ 2: ฉันสามารถปรับแต่งการตั้งค่าเอาต์พุต PDF ได้หรือไม่

A2: ได้ คุณสามารถปรับแต่งการตั้งค่าเอาต์พุต PDF ได้โดยการปรับคุณสมบัติของ`CadRasterizationOptions` และ`PdfOptions` ตามความต้องการของคุณ

### คำถามที่ 3: Aspose.CAD มีรุ่นทดลองใช้ฟรีหรือไม่

 A3: ได้ คุณสามารถสำรวจ Aspose.CAD ด้วยการทดลองใช้ฟรีโดยไปที่[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 4: ฉันจะรับการสนับสนุนสำหรับ Aspose.CAD ได้อย่างไร

 A4: สำหรับการสนับสนุนหรือข้อสงสัยใด ๆ โปรดไปที่[ฟอรั่ม Aspose.CAD](https://forum.aspose.com/c/cad/19).

### คำถามที่ 5: ฉันจะซื้อใบอนุญาตสำหรับ Aspose.CAD ได้ที่ไหน

 A5: คุณสามารถซื้อใบอนุญาตสำหรับ Aspose.CAD ได้[ที่นี่](https://purchase.aspose.com/buy).