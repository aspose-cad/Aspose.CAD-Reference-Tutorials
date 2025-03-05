---
title: การส่งออกไฟล์ DGN แบบฝัง - บทช่วยสอน Aspose.CAD
linktitle: การส่งออกไฟล์ DGN แบบฝัง
second_title: Aspose.CAD .NET - รูปแบบไฟล์ CAD และ BIM
description: สำรวจพลังของ Aspose.CAD สำหรับ .NET เรียนรู้การส่งออกไฟล์ DGN ที่ฝังไว้เป็น PDF ได้อย่างง่ายดายด้วยบทช่วยสอนทีละขั้นตอนนี้
type: docs
weight: 14
url: /th/net/export-techniques/exporting-embedded-dgn-files/
---
## การแนะนำ

ในโลกแบบไดนามิกของการพัฒนาซอฟต์แวร์ Aspose.CAD สำหรับ .NET มีความโดดเด่นในฐานะเครื่องมืออันทรงพลังสำหรับการจัดการไฟล์ Computer-Aided Design (CAD) บทช่วยสอนนี้จะแนะนำคุณตลอดกระบวนการส่งออกไฟล์ DGN ที่ฝังไว้โดยใช้ Aspose.CAD สำหรับ .NET ไม่ว่าคุณจะเป็นนักพัฒนาที่มีประสบการณ์หรือเป็นมือใหม่ที่อยากรู้อยากเห็น คำแนะนำทีละขั้นตอนนี้จะช่วยให้คุณควบคุมความสามารถของ Aspose.CAD ได้อย่างมีประสิทธิภาพ

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเข้าสู่บทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

1.  Aspose.CAD สำหรับ .NET: ดาวน์โหลดและติดตั้งไลบรารีจาก[Aspose.CAD สำหรับ .NET](https://releases.aspose.com/cad/net/).

2. สภาพแวดล้อมการพัฒนา: ตั้งค่าสภาพแวดล้อมการพัฒนา .NET ด้วย Visual Studio หรือ IDE ที่ต้องการอื่นๆ

3. ตัวอย่างไฟล์ DXF: สำหรับบทช่วยสอนนี้ เราจะใช้ไฟล์ "conic_pyramid.dxf" ตรวจสอบให้แน่ใจว่าคุณมีมันอยู่ในไดเร็กทอรีเอกสารที่คุณกำหนด

## นำเข้าเนมสเปซ

ในโค้ด C# ของคุณ ตรวจสอบให้แน่ใจว่าได้นำเข้าเนมสเปซที่จำเป็น:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
```

## ขั้นตอนที่ 1: โหลดไฟล์ DXF

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    //รหัสของคุณสำหรับขั้นตอนต่อไปจะอยู่ที่นี่
}
```

## ขั้นตอนที่ 2: ตั้งค่าตัวเลือกการแรสเตอร์

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new[] { "Model" };
```

## ขั้นตอนที่ 3: ตั้งค่าตัวเลือก PDF

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## ขั้นตอนที่ 4: บันทึกเป็น PDF

```csharp
cadImage.Save(MyDir + "conic_pyramid.pdf", pdfOptions);
```

## ขั้นตอนที่ 5: แสดงข้อความแสดงความสำเร็จ

```csharp
Console.WriteLine("\nThe DXF drawing exported successfully to PDF.\nFile saved at " + MyDir);
```

## บทสรุป

ยินดีด้วย! คุณได้ส่งออกไฟล์ DGN ที่ฝังไว้เป็น PDF โดยใช้ Aspose.CAD สำหรับ .NET สำเร็จแล้ว บทช่วยสอนนี้ครอบคลุมขั้นตอนที่สำคัญ เพื่อเป็นพื้นฐานในการสำรวจฟังก์ชันการทำงานขั้นสูงเพิ่มเติมที่นำเสนอโดย Aspose.CAD

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถใช้ Aspose.CAD สำหรับ .NET กับภาษาการเขียนโปรแกรมอื่นได้หรือไม่

A1: Aspose.CAD รองรับ .NET เป็นหลัก แต่ Aspose มีไลบรารีสำหรับภาษาต่างๆ รวมถึง Java และ Python

### คำถามที่ 2: Aspose.CAD สำหรับ .NET มีรุ่นทดลองใช้ฟรีหรือไม่

 A2: ได้ คุณสามารถทดลองใช้งานฟรีได้จาก[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 3: ฉันจะหาเอกสารที่ครอบคลุมสำหรับ Aspose.CAD สำหรับ .NET ได้ที่ไหน

 A3: โปรดดูเอกสารประกอบ[ที่นี่](https://reference.aspose.com/cad/net/).

### คำถามที่ 4: ฉันจะได้รับใบอนุญาตชั่วคราวสำหรับ Aspose.CAD สำหรับ .NET ได้อย่างไร

 A4: รับใบอนุญาตชั่วคราว[ที่นี่](https://purchase.aspose.com/temporary-license/).

### คำถามที่ 5: ต้องการความช่วยเหลือหรือต้องการมีส่วนร่วมกับชุมชน?

A5: เยี่ยมชม[ฟอรั่ม Aspose.CAD](https://forum.aspose.com/c/cad/19) สำหรับการสนับสนุนและการอภิปราย