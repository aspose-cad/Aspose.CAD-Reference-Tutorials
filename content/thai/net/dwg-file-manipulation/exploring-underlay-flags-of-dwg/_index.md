---
title: การสำรวจ Underlay Flags ของไฟล์ DWG - บทช่วยสอน Aspose.CAD
linktitle: การสำรวจ Underlay Flags ของไฟล์ DWG
second_title: Aspose.CAD .NET - รูปแบบไฟล์ CAD และ BIM
description: ปลดล็อกพลังของ Aspose.CAD สำหรับ .NET ในการสำรวจแฟล็กการซ้อนทับไฟล์ DWG ปฏิบัติตามคำแนะนำทีละขั้นตอนของเรา
type: docs
weight: 13
url: /th/net/dwg-file-manipulation/exploring-underlay-flags-of-dwg/
---
## การแนะนำ

หากคุณกำลังเจาะลึกโลกที่ซับซ้อนของไฟล์ CAD โดยเฉพาะไฟล์ DWG และต้องการปลดล็อกความลึกลับของธงด้านล่าง แสดงว่าคุณมาถูกที่แล้ว บทช่วยสอนนี้จะแนะนำคุณตลอดกระบวนการสำรวจแฟล็กอันเดอร์เลย์ในไฟล์ DWG โดยใช้ไลบรารี Aspose.CAD สำหรับ .NET อันทรงพลัง

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเจาะลึกบทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีสิ่งต่อไปนี้:

- ความเข้าใจพื้นฐานเกี่ยวกับการเขียนโปรแกรม C# และ .NET
-  ติดตั้ง Aspose.CAD สำหรับไลบรารี .NET แล้ว ถ้าไม่คุณสามารถดาวน์โหลดได้[ที่นี่](https://releases.aspose.com/cad/net/).
- ไฟล์ DWG สำหรับการทดสอบ คุณสามารถใช้ไฟล์ตัวอย่าง "BlockRefDgn.dwg" ที่ให้ไว้ในบทช่วยสอน

## นำเข้าเนมสเปซ

ในการเริ่มต้น คุณต้องนำเข้าเนมสเปซที่จำเป็น นี่เป็นตัวอย่างเพื่อช่วยคุณ:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;

```

## ขั้นตอนที่ 1: โหลดไฟล์ DWG และแปลงเป็น CadImage

เริ่มต้นด้วยการโหลดไฟล์ DWG ที่มีอยู่แล้วแปลงเป็น CadImage:

```csharp
string fileName = MyDir + "BlockRefDgn.dwg";

// โหลดไฟล์ DWG และแปลงเป็น CadImage
using (CadImage image = (CadImage)Image.Load(fileName))
{
    // รหัสของคุณสำหรับขั้นตอนต่อไปจะอยู่ที่นี่
}
```

## ขั้นตอนที่ 2: วนซ้ำผ่านเอนทิตี

จากนั้น วนซ้ำแต่ละเอนทิตีภายในไฟล์ DWG:

```csharp
foreach (CadBaseEntity entity in image.Entities)
{
    // รหัสของคุณสำหรับขั้นตอนต่อไปจะอยู่ที่นี่
}
```

## ขั้นตอนที่ 3: ตรวจสอบประเภท CadDgnUnderlay

ตรวจสอบว่าเอนทิตีเป็นประเภท CadDgnUnderlay หรือไม่:

```csharp
if (entity is CadDgnUnderlay)
{
    // รหัสของคุณสำหรับขั้นตอนต่อไปจะอยู่ที่นี่
}
```

## ขั้นตอนที่ 4: เข้าถึง Underlay Flags

เข้าถึงแฟล็กอันเดอร์เลย์ต่างๆ และดึงข้อมูลที่เกี่ยวข้อง:

```csharp
CadUnderlay underlay = entity as CadUnderlay;

Console.WriteLine(underlay.UnderlayPath);
Console.WriteLine(underlay.UnderlayName);
Console.WriteLine(underlay.InsertionPoint.X);
Console.WriteLine(underlay.InsertionPoint.Y);
Console.WriteLine(underlay.RotationAngle);
Console.WriteLine(underlay.ScaleX);
Console.WriteLine(underlay.ScaleY);
Console.WriteLine(underlay.ScaleZ);
Console.WriteLine((underlay.Flags & UnderlayFlags.UnderlayIsOn) == UnderlayFlags.UnderlayIsOn);
Console.WriteLine((underlay.Flags & UnderlayFlags.ClippingIsOn) == UnderlayFlags.ClippingIsOn);
Console.WriteLine((underlay.Flags & UnderlayFlags.Monochrome) != UnderlayFlags.Monochrome);
```

## บทสรุป

ยินดีด้วย! คุณได้สำรวจแฟล็กด้านล่างของไฟล์ DWG โดยใช้ Aspose.CAD สำหรับ .NET สำเร็จแล้ว บทช่วยสอนนี้ช่วยให้คุณมีความรู้ในการไปยังส่วนต่างๆ ของเอนทิตีและดึงข้อมูลที่สำคัญเกี่ยวกับอันเดอร์เลย์

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถใช้ Aspose.CAD สำหรับ .NET กับไฟล์ CAD รูปแบบอื่นได้หรือไม่

A1: Aspose.CAD รองรับรูปแบบ CAD หลากหลาย รวมถึง DWG, DXF, DGN และอื่นๆ ตรวจสอบเอกสารเพื่อดูรายการทั้งหมด

### คำถามที่ 2: Aspose.CAD สำหรับ .NET มีใบอนุญาตชั่วคราวหรือไม่

 A2: ได้ คุณสามารถขอรับใบอนุญาตชั่วคราวได้[ที่นี่](https://purchase.aspose.com/temporary-license/).

### คำถามที่ 3: ฉันจะรับการสนับสนุนสำหรับ Aspose.CAD สำหรับ .NET ได้ที่ไหน

 A3: เยี่ยมชมฟอรั่มการสนับสนุน[ที่นี่](https://forum.aspose.com/c/cad/19) สำหรับความช่วยเหลือ.

### คำถามที่ 4: ฉันจะซื้อ Aspose.CAD สำหรับ .NET ได้อย่างไร

A4: ซื้อห้องสมุด[ที่นี่](https://purchase.aspose.com/buy).

### คำถามที่ 5: มีการทดลองใช้ฟรีหรือไม่?

 A5: ได้ คุณสามารถเข้าถึงรุ่นทดลองใช้ฟรีได้[ที่นี่](https://releases.aspose.com/).
