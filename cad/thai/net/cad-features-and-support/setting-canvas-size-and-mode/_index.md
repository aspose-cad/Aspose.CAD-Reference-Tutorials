---
title: การตั้งค่าขนาดและโหมด Canvas ใน Aspose.CAD สำหรับ .NET
linktitle: การตั้งค่าขนาดและโหมดแคนวาส
second_title: Aspose.CAD .NET - รูปแบบไฟล์ CAD และ BIM
description: สำรวจคำแนะนำทีละขั้นตอนเกี่ยวกับการตั้งค่าขนาดและโหมดแคนวาสใน Aspose.CAD สำหรับ .NET เพิ่มประสิทธิภาพการเรนเดอร์ CAD ของคุณอย่างง่ายดายโดยใช้บทช่วยสอนที่ครอบคลุมนี้
type: docs
weight: 16
url: /th/net/cad-features-and-support/setting-canvas-size-and-mode/
---
## การแนะนำ

คุณพร้อมที่จะปลดล็อกศักยภาพเต็มรูปแบบของ Aspose.CAD สำหรับ .NET และปฏิวัติประสบการณ์การเรนเดอร์ CAD ของคุณแล้วหรือยัง? ในบทช่วยสอนทีละขั้นตอนนี้ เราจะเจาะลึกความซับซ้อนของการตั้งค่าขนาดและโหมดแคนวาสโดยใช้ไลบรารี Aspose.CAD อันทรงพลัง ไม่ว่าคุณจะเป็นนักพัฒนาที่มีประสบการณ์หรือเพิ่งเริ่มต้น คู่มือนี้จะแนะนำคุณตลอดกระบวนการ เพื่อให้มั่นใจว่าคุณจะสามารถควบคุมความสามารถของ Aspose.CAD ได้อย่างมีประสิทธิภาพ

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเจาะลึกบทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

-  ไลบรารี Aspose.CAD: ดาวน์โหลดและติดตั้งไลบรารี Aspose.CAD จากไฟล์[เว็บไซต์ Aspose.CAD](https://releases.aspose.com/cad/net/).

- สภาพแวดล้อมการพัฒนา: ตรวจสอบให้แน่ใจว่าคุณได้ตั้งค่าสภาพแวดล้อมการพัฒนา .NET บนเครื่องของคุณ

-  ตัวอย่างไฟล์ CAD: สำหรับบทช่วยสอนนี้ เราจะใช้ไฟล์ DXF ตัวอย่าง คุณสามารถหาหนึ่งใน[เอกสาร Aspose.CAD](https://reference.aspose.com/cad/net/).

## นำเข้าเนมสเปซ

ในการเริ่มต้น ให้นำเข้าเนมสเปซที่จำเป็นที่จุดเริ่มต้นของแอปพลิเคชัน .NET ของคุณ:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## ขั้นตอนที่ 1: โหลดไฟล์ CAD

เริ่มต้นด้วยการโหลดไฟล์ CAD โดยใช้รหัสต่อไปนี้:

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (Image image = Image.Load(sourceFilePath))
{
    //รหัสของคุณสำหรับขั้นตอนต่อไปจะอยู่ที่นี่
}
```

## ขั้นตอนที่ 2: สร้าง CadRasterizationOptions

 สร้างอินสแตนซ์ของ`CadRasterizationOptions` และกำหนดคุณสมบัติของมัน:

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.AutomaticLayoutsScaling = true;
rasterizationOptions.NoScaling = false;
```

## ขั้นตอนที่ 3: สร้าง PdfOptions

 สร้างอินสแตนซ์ของ`PdfOptions` และตั้งค่าของมัน`VectorRasterizationOptions` คุณสมบัติ:

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## ขั้นตอนที่ 4: ส่งออกเป็น PDF

ส่งออกไฟล์ CAD เป็น PDF โดยใช้ตัวเลือกที่กำหนดค่าไว้:

```csharp
image.Save(MyDir + "result_out.pdf", pdfOptions);
```

## ขั้นตอนที่ 5: สร้าง TiffOptions

 สร้างอินสแตนซ์ของ`TiffOptions` และตั้งค่าของมัน`VectorRasterizationOptions` คุณสมบัติ:

```csharp
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.VectorRasterizationOptions = rasterizationOptions;
```

## ขั้นตอนที่ 6: ส่งออกเป็น TIFF

ส่งออกไฟล์ CAD เป็น TIFF โดยใช้ตัวเลือกที่กำหนดค่าไว้:

```csharp
image.Save(MyDir + "result_out.tiff", tiffOptions);
```

## บทสรุป

ยินดีด้วย! คุณได้ตั้งค่าขนาดและโหมดแคนวาสใน Aspose.CAD สำหรับ .NET เรียบร้อยแล้ว คุณสมบัติอันทรงพลังนี้เปิดโลกแห่งความเป็นไปได้สำหรับการเรนเดอร์ CAD ทดลองใช้ตัวเลือกต่างๆ และค้นพบศักยภาพทั้งหมดของ Aspose.CAD ในแอปพลิเคชัน .NET ของคุณ

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถใช้ Aspose.CAD กับไลบรารี .NET อื่นๆ ได้หรือไม่

ตอบ 1: ใช่ Aspose.CAD ทำงานร่วมกับไลบรารี .NET อื่นๆ ได้อย่างราบรื่น โดยให้ความสามารถที่ได้รับการปรับปรุงสำหรับการจัดการ CAD

### คำถามที่ 2: Aspose.CAD มีให้ทดลองใช้ฟรีหรือไม่

 ตอบ 2: ได้ คุณสามารถสำรวจคุณสมบัติของ Aspose.CAD ได้ด้วยการทดลองใช้ฟรี เยี่ยม[ที่นี่](https://releases.aspose.com/) ที่จะเริ่มต้น.

### คำถามที่ 3: ฉันจะรับการสนับสนุนสำหรับ Aspose.CAD ได้อย่างไร

 A3: สำหรับการสนับสนุนและการสนทนา โปรดไปที่[ฟอรั่ม Aspose.CAD](https://forum.aspose.com/c/cad/19).

### คำถามที่ 4: ฉันจะหาเอกสารประกอบสำหรับ Aspose.CAD ได้ที่ไหน

 A4: โปรดดูที่[เอกสาร Aspose.CAD](https://reference.aspose.com/cad/net/) สำหรับข้อมูลโดยละเอียดและตัวอย่าง

### คำถามที่ 5: ฉันจะซื้อ Aspose.CAD สำหรับ .NET ได้อย่างไร

 A5: หากต้องการซื้อ Aspose.CAD โปรดไปที่[หน้าซื้อ](https://purchase.aspose.com/buy).