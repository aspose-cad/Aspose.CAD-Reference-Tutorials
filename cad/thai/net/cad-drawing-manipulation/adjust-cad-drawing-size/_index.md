---
title: การปรับขนาดการเขียนแบบ CAD ใน Aspose.CAD สำหรับ .NET
linktitle: การปรับขนาดการวาด CAD
second_title: Aspose.CAD .NET - รูปแบบไฟล์ CAD และ BIM
description: เรียนรู้วิธีปรับขนาดการวาด CAD ใน .NET ได้อย่างง่ายดายโดยใช้ Aspose.CAD ปฏิบัติตามคำแนะนำทีละขั้นตอนของเราเพื่อการปรับขนาดที่ราบรื่น
type: docs
weight: 10
url: /th/net/cad-drawing-manipulation/adjust-cad-drawing-size/
---
## การแนะนำ

คุณกำลังมองหาการปรับขนาดภาพวาด CAD ในแอปพลิเคชัน .NET ของคุณได้อย่างราบรื่นหรือไม่? Aspose.CAD สำหรับ .NET มอบโซลูชันที่มีประสิทธิภาพ ซึ่งช่วยให้คุณจัดการการปรับขนาดการวาด CAD ได้อย่างง่ายดาย ในบทช่วยสอนนี้ เราจะแนะนำคุณตลอดกระบวนการ โดยแจกแจงแต่ละขั้นตอนเพื่อให้แน่ใจว่าคุณเข้าใจความซับซ้อนของการปรับขนาดแบบร่าง CAD โดยใช้ Aspose.CAD

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเจาะลึกบทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

- Aspose.CAD สำหรับ .NET Library: ดาวน์โหลดและติดตั้งไลบรารีจาก[หน้าดาวน์โหลด Aspose.CAD สำหรับ .NET](https://releases.aspose.com/cad/net/).
- ตัวอย่างการเขียนแบบ CAD: ตรวจสอบให้แน่ใจว่าคุณมีไฟล์เขียนแบบ CAD ตัวอย่าง (เช่น "sample.dwg") ในไดเร็กทอรีเอกสารของคุณ

## นำเข้าเนมสเปซ

เริ่มต้นด้วยการนำเข้าเนมสเปซที่จำเป็นลงในแอปพลิเคชัน .NET ของคุณ ขั้นตอนนี้มีความสำคัญอย่างยิ่งในการเข้าถึงฟังก์ชันการทำงานที่ Aspose.CAD สำหรับ .NET มอบให้

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## ขั้นตอนที่ 1: โหลด CAD Drawing

เริ่มต้นด้วยการโหลดแบบร่าง CAD ลงในอินสแตนซ์ของคลาส Aspose.CAD.Image ตรวจสอบให้แน่ใจว่าคุณมีเส้นทางไฟล์ที่ถูกต้องสำหรับภาพวาดตัวอย่างของคุณ

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "sample.dwg";

// โหลดแบบร่าง CAD ในอินสแตนซ์ของรูปภาพ
using (var image = Aspose.CAD.Image.Load(sourceFilePath))
{
    // รหัสของคุณที่นี่...
}
```

## ขั้นตอนที่ 2: สร้าง BmpOptions

สร้างอินสแตนซ์ของคลาส BmpOptions ซึ่งมีหน้าที่ระบุตัวเลือกเมื่อบันทึกแบบร่าง CAD เป็นไฟล์ BMP

```csharp
Aspose.CAD.ImageOptions.BmpOptions bmpOptions = new Aspose.CAD.ImageOptions.BmpOptions();
```

## ขั้นตอนที่ 3: ตั้งค่า CadRasterizationOptions

สร้างอินสแตนซ์คลาส CadRasterizationOptions และกำหนดค่าคุณสมบัติสำหรับการแรสเตอร์เวกเตอร์

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions cadRasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
bmpOptions.VectorRasterizationOptions = cadRasterizationOptions;
```

## ขั้นตอนที่ 4: ตั้งค่าคุณสมบัติ UnitType

ตั้งค่าคุณสมบัติ UnitType ของ CadRasterizationOptions เพื่อระบุประเภทหน่วยสำหรับการปรับขนาด ในตัวอย่างนี้ กำหนดเป็นเซนติเมตร

```csharp
cadRasterizationOptions.UnitType = Aspose.CAD.ImageOptions.UnitType.Centimeter;
```

## ขั้นตอนที่ 5: ตั้งค่าคุณสมบัติเค้าโครง

ระบุเค้าโครงที่คุณต้องการรวมไว้ในภาพวาดที่ปรับขนาดโดยการตั้งค่าคุณสมบัติเค้าโครง

```csharp
cadRasterizationOptions.Layouts = new string[] { "Model" };
```

## ขั้นตอนที่ 6: ส่งออกเป็น BMP

สุดท้าย ให้บันทึกเค้าโครงที่ปรับขนาดแล้วเป็นไฟล์ BMP โดยใช้วิธีบันทึก

```csharp
string outPath = sourceFilePath + ".bmp";
image.Save(outPath, bmpOptions);
```

ตอนนี้ คุณได้ปรับขนาดการเขียนแบบ CAD ของคุณโดยใช้ Aspose.CAD สำหรับ .NET สำเร็จแล้ว!

## บทสรุป

ในบทช่วยสอนนี้ เราได้อธิบายขั้นตอนการปรับขนาดภาพวาด CAD ใน .NET โดยใช้ Aspose.CAD เมื่อทำตามขั้นตอนเหล่านี้ คุณจะสามารถรวมฟังก์ชันการทำงานนี้เข้ากับแอปพลิเคชันของคุณได้อย่างราบรื่น มอบประสบการณ์ผู้ใช้ที่ราบรื่น

## คำถามที่พบบ่อย

### คำถามที่ 1: Aspose.CAD สำหรับ .NET เข้ากันได้กับรูปแบบ CAD ทั้งหมดหรือไม่

 A1: Aspose.CAD สำหรับ .NET รองรับรูปแบบ CAD ที่หลากหลาย รวมถึง DWG, DXF, DWF และอื่นๆ ตรวจสอบ[เอกสารประกอบ](https://reference.aspose.com/cad/net/) สำหรับรายการทั้งหมด

### คำถามที่ 2: ฉันสามารถปรับขนาดหลายเลย์เอาต์พร้อมกันได้หรือไม่

ตอบ 2: ได้ คุณสามารถปรับขนาดเลย์เอาต์หลาย ๆ อันได้โดยการปรับอาร์เรย์เลย์เอาต์ใน CadRasterizationOptions

### คำถามที่ 3: ฉันจะรับการสนับสนุนสำหรับ Aspose.CAD สำหรับ .NET ได้ที่ไหน

 A3: เยี่ยมชม[ฟอรั่ม Aspose.CAD](https://forum.aspose.com/c/cad/19) สำหรับการสนับสนุนและช่วยเหลือชุมชน

### คำถามที่ 4: มีการทดลองใช้ฟรีหรือไม่?

 A4: ใช่ คุณสามารถสำรวจได้[ทดลองฟรี](https://releases.aspose.com/) เพื่อประเมินคุณสมบัติของ Aspose.CAD สำหรับ .NET

### คำถามที่ 5: ฉันจะขอรับใบอนุญาตชั่วคราวสำหรับ Aspose.CAD สำหรับ .NET ได้อย่างไร

 A5: รับใบอนุญาตชั่วคราวเพื่อการทดสอบ[ที่นี่](https://purchase.aspose.com/temporary-license/).