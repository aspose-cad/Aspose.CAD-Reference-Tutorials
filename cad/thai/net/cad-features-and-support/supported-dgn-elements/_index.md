---
title: รองรับองค์ประกอบ DGN ใน Aspose.CAD สำหรับ .NET
linktitle: องค์ประกอบ DGN ที่รองรับ
second_title: Aspose.CAD .NET - รูปแบบไฟล์ CAD และ BIM
description: สำรวจ Aspose.CAD สำหรับคุณสมบัติอันทรงพลังของ .NET สำหรับการจัดการไฟล์ DGN ปฏิบัติตามคำแนะนำทีละขั้นตอนของเราเพื่อทำงานกับองค์ประกอบ 2D และ 3D ได้อย่างราบรื่น
weight: 18
url: /th/net/cad-features-and-support/supported-dgn-elements/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# รองรับองค์ประกอบ DGN ใน Aspose.CAD สำหรับ .NET

## การแนะนำ

คุณเป็นนักพัฒนา .NET ที่ต้องการทำงานกับไฟล์ DGN ได้อย่างราบรื่นหรือไม่? Aspose.CAD สำหรับ .NET มอบโซลูชันที่แข็งแกร่งในการจัดการไฟล์ DGN ได้อย่างมีประสิทธิภาพ ในบทช่วยสอนนี้ เราจะเจาะลึกองค์ประกอบ DGN ที่รองรับ ซึ่งจะแนะนำคุณตลอดกระบวนการทำงานกับ Aspose.CAD สำหรับ .NET

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเริ่ม ตรวจสอบให้แน่ใจว่าคุณมีสิ่งต่อไปนี้:

- ความรู้พื้นฐานเกี่ยวกับการเขียนโปรแกรม .NET
- ติดตั้ง Visual Studio บนเครื่องของคุณแล้ว
-  Aspose.CAD สำหรับไลบรารี .NET ซึ่งคุณสามารถดาวน์โหลดได้[ที่นี่](https://releases.aspose.com/cad/net/).

## นำเข้าเนมสเปซ

หากต้องการเริ่มต้นโปรเจ็กต์ของคุณ ให้นำเข้าเนมสเปซที่จำเป็นลงในแอปพลิเคชัน .NET ของคุณ ขั้นตอนนี้ช่วยให้แน่ใจว่าคุณสามารถเข้าถึงฟังก์ชันการทำงานที่ Aspose.CAD สำหรับ .NET มอบให้

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Dgn;
using Aspose.CAD.FileFormats.Dgn.DgnElements;
```

## ขั้นตอนที่ 1: โหลดไฟล์ DGN

เริ่มต้นด้วยการโหลดไฟล์ DGN ที่มีอยู่เป็น CadImage ในแอปพลิเคชัน .NET ของคุณ

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // รหัสของคุณที่นี่
}
```

## ขั้นตอนที่ 2: วนซ้ำผ่านองค์ประกอบ DGN

วนซ้ำองค์ประกอบ DGN โดยใช้ foreach loop Aspose.CAD สำหรับ .NET มีองค์ประกอบ DGN หลากหลายประเภทที่คุณสามารถใช้งานได้

```csharp
foreach (DgnDrawingElementBase element in dgnImage.Elements)
{
    // รหัสของคุณที่นี่
}
```

## ขั้นตอนที่ 3: จัดการเอนทิตีที่ได้รับการสนับสนุนก่อนหน้านี้

จัดการเอนทิตี 2D ที่รองรับก่อนหน้านี้ ซึ่งขณะนี้รองรับ 3D ด้วยเช่นกัน

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.Line:
    case DgnElementType.Ellipse:
    case DgnElementType.Curve:
    // กรณีเพิ่มเติม
        {
            // รหัสของคุณที่นี่
            break;
        }
}
```

## ขั้นตอนที่ 4: จัดการเอนทิตี 3 มิติที่รองรับ

จัดการเอนทิตี 3 มิติที่รองรับโดย Aspose.CAD สำหรับ .NET

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.SolidHeader3D:
    case DgnElementType.Cone:
    case DgnElementType.CellHeader:
        {
            // รหัสของคุณที่นี่
            break;
        }
}
```

## ขั้นตอนที่ 5: ส่งออกและบันทึก

สุดท้าย ส่งออกไฟล์ DGN ที่แก้ไขแล้วไปยังอิมเมจแรสเตอร์ และบันทึกลงในไดเร็กทอรีที่ระบุ

```csharp
Console.WriteLine("\nThe DGN file exported successfully to raster image.\nFile saved at " + MyDir);
```

## บทสรุป

ในบทช่วยสอนนี้ เราได้สำรวจความสามารถของ Aspose.CAD สำหรับ .NET ในการจัดการและจัดการไฟล์ DGN ด้วยการทำตามคำแนะนำทีละขั้นตอน คุณสามารถทำงานกับองค์ประกอบ DGN ที่รองรับได้อย่างมีประสิทธิภาพ ไม่ว่าจะเป็นเอนทิตี 2 มิติหรือ 3 มิติ Aspose.CAD สำหรับ .NET ช่วยให้คุณสามารถรวมการประมวลผลไฟล์ DGN เข้ากับแอปพลิเคชัน .NET ของคุณได้อย่างราบรื่น

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันจะหาเอกสารสำหรับ Aspose.CAD สำหรับ .NET ได้ที่ไหน

 A1: คุณสามารถค้นหาเอกสารประกอบได้[ที่นี่](https://reference.aspose.com/cad/net/).

### คำถามที่ 2: ฉันจะดาวน์โหลด Aspose.CAD สำหรับ .NET ได้อย่างไร

 A2: คุณสามารถดาวน์โหลดห้องสมุดได้[ที่นี่](https://releases.aspose.com/cad/net/).

### คำถามที่ 3: Aspose.CAD สำหรับ .NET มีรุ่นทดลองใช้ฟรีหรือไม่

 A3: ได้ คุณสามารถเข้าถึงรุ่นทดลองใช้ฟรีได้[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 4: ฉันจะรับใบอนุญาตชั่วคราวสำหรับ Aspose.CAD สำหรับ .NET ได้ที่ไหน

 A4: มีใบอนุญาตชั่วคราว[ที่นี่](https://purchase.aspose.com/temporary-license/).

### Q5: ต้องการความช่วยเหลือหรือมีคำถาม?

 A5: เยี่ยมชมชุมชน Aspose.CAD สำหรับ .NET[ฟอรั่มการสนับสนุน](https://forum.aspose.com/c/cad/19).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
