---
title: การทำงานกับไฟล์ DWG ใน C # - รับขนาดของเค้าโครง DWF
linktitle: การทำงานกับไฟล์ DWG ใน C # - รับขนาดของเค้าโครง DWF
second_title: Aspose.CAD .NET - รูปแบบไฟล์ CAD และ BIM
description: สำรวจพลังของ Aspose.CAD สำหรับ .NET ในการจัดการไฟล์ DWG เรียนรู้การแยกขนาดเค้าโครง DWF ได้อย่างง่ายดายโดยใช้ C#
type: docs
weight: 10
url: /th/net/dwg-file-manipulation/get-size-of-dwf-layout/
---
## การแนะนำ

ในขอบเขตของการออกแบบโดยใช้คอมพิวเตอร์ช่วย (CAD) และการพัฒนา .NET นั้น Aspose.CAD ถือเป็นเครื่องมืออันทรงพลังสำหรับการจัดการไฟล์ DWG บทช่วยสอนนี้จะแนะนำคุณตลอดกระบวนการทำงานกับไฟล์ DWG ใน C# และการแยกขนาดของเค้าโครง DWF ก่อนที่เราจะเจาะลึกโค้ด เรามาตรวจสอบให้แน่ใจว่าคุณได้เตรียมทุกอย่างไว้แล้วเพื่อเริ่มต้นการเดินทางครั้งนี้

## ข้อกำหนดเบื้องต้น

หากต้องการปฏิบัติตามบทช่วยสอนนี้อย่างราบรื่น ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

-  Aspose.CAD สำหรับ .NET: ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง Aspose.CAD สำหรับ .NET แล้ว คุณสามารถดาวน์โหลดได้จาก[หน้าดาวน์โหลด Aspose.CAD สำหรับ .NET](https://releases.aspose.com/cad/net/).

ตอนนี้คุณมีเครื่องมือที่จำเป็นแล้ว เรามาเข้าสู่เวทีการเขียนโค้ดกันดีกว่า

## นำเข้าเนมสเปซ

ก่อนที่เราจะเริ่มทำงานกับโค้ด เรามานำเข้าเนมสเปซที่จำเป็นก่อน:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Dwf;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

เนมสเปซเหล่านี้จะจัดเตรียมคลาสและวิธีการที่จำเป็นสำหรับการจัดการไฟล์ CAD ด้วย Aspose.CAD ในแอปพลิเคชัน C# ของคุณ

## ขั้นตอนที่ 1: ตั้งค่าสภาพแวดล้อมของคุณ

เริ่มต้นด้วยการตรวจสอบให้แน่ใจว่าคุณได้ตั้งค่าสภาพแวดล้อมที่ถูกต้องสำหรับโปรเจ็กต์ของคุณ อ้างอิงไลบรารี Aspose.CAD ในโปรเจ็กต์ C# ของคุณ

## ขั้นตอนที่ 2: กำหนดเส้นทางไฟล์

กำหนดเส้นทางสำหรับไฟล์ DWG ของคุณและไดเร็กทอรีเอาต์พุตสำหรับไฟล์ JPG ที่สร้างขึ้น:

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "blocks_and_tables.dwf";
```

## ขั้นตอนที่ 3: โหลดอิมเมจ DWF

โหลดอิมเมจ DWF โดยใช้ Aspose.CAD:

```csharp
using (DwfImage image = (DwfImage)Aspose.CAD.Image.Load(sourceFilePath))
{
    // รหัสสำหรับขั้นตอนต่อไปจะอยู่ที่นี่
}
```

## ขั้นตอนที่ 4: วนซ้ำผ่านหน้าต่างๆ

วนซ้ำหน้าต่างๆ ของอิมเมจ DWF:

```csharp
foreach (var page in image.Pages)
{
    // รหัสสำหรับขั้นตอนต่อไปจะอยู่ที่นี่
}
```

## ขั้นตอนที่ 5: รับข้อมูลเค้าโครง

รับข้อมูลเค้าโครงจากแต่ละหน้า:

```csharp
var layout = page.Name;
System.Console.WriteLine("Layout= " + layout);
```

## ขั้นตอนที่ 6: ตั้งค่าตัวเลือก JPG

ตั้งค่าตัวเลือกสำหรับการบันทึกเค้าโครงเป็นไฟล์ JPG:

```csharp
using (FileStream fs = new FileStream(MyDir + "layout_" + layout + ".jpg", FileMode.Create))
{
    JpegOptions jpegOptions = new JpegOptions();
    CadRasterizationOptions options = new CadRasterizationOptions();
    options.Layouts = new string[] { layout };
    // รหัสสำหรับขั้นตอนต่อไปจะอยู่ที่นี่
}
```

## ขั้นตอนที่ 7: กำหนดขนาดหน้า

กำหนดขนาดของโครงร่าง DWF:

```csharp
double sizeExtX = page.MaxPoint.X - page.MinPoint.X;
double sizeExtY = page.MaxPoint.Y - page.MinPoint.Y;
// รหัสสำหรับขั้นตอนต่อไปจะอยู่ที่นี่
```

## ขั้นตอนที่ 8: ตั้งค่าขนาดหน้า

ตั้งค่าขนาดหน้าตามประเภทหน่วย:

```csharp
if (page.UnitType == UnitType.Inch)
{
    options.PageHeight = CommonHelper.INtoPixels(sizeExtY, CommonHelper.DPI);
    options.PageWidth = CommonHelper.INtoPixels(sizeExtX, CommonHelper.DPI);
}
else if (page.UnitType == UnitType.Millimeter)
{
    options.PageHeight = CommonHelper.MMtoPixels(sizeExtY, CommonHelper.DPI);
    options.PageWidth = CommonHelper.MMtoPixels(sizeExtX, CommonHelper.DPI);
}
else
{
    options.PageHeight = (float)sizeExtY;
    options.PageWidth = (float)sizeExtX;
}
```

## ขั้นตอนที่ 9: บันทึกไฟล์ JPG

บันทึกไฟล์ JPG ด้วยตัวเลือกที่ระบุ:

```csharp
jpegOptions.VectorRasterizationOptions = options;
image.Save(fs, jpegOptions);
}
```

ตอนนี้ คุณได้แยกขนาดของโครงร่าง DWF จากไฟล์ DWG โดยใช้ Aspose.CAD ใน C# สำเร็จแล้ว รู้สึกอิสระที่จะสำรวจคุณสมบัติและฟังก์ชันการทำงานเพิ่มเติมที่ Aspose.CAD นำเสนอสำหรับการพัฒนา .NET

## บทสรุป

ในบทช่วยสอนนี้ เราได้อธิบายกระบวนการทำงานกับไฟล์ DWG ใน C# โดยใช้ Aspose.CAD แล้ว ด้วยการทำตามขั้นตอนเหล่านี้ คุณไม่เพียงแต่จะได้ขนาดของเค้าโครง DWF เท่านั้น แต่ยังใช้ประโยชน์จากความสามารถของ Aspose.CAD สำหรับงานที่เกี่ยวข้องกับ CAD ต่างๆ ในโปรเจ็กต์ .NET ของคุณได้อีกด้วย

## คำถามที่พบบ่อย

### คำถามที่ 1: Aspose.CAD เข้ากันได้กับรูปแบบไฟล์ DWG ล่าสุดหรือไม่

 A1: Aspose.CAD รองรับไฟล์ DWG หลากหลายรูปแบบ รวมถึงเวอร์ชันล่าสุดด้วย อ้างถึง[เอกสารประกอบ](https://reference.aspose.com/cad/net/) สำหรับรายละเอียดความเข้ากันได้เฉพาะ

### คำถามที่ 2: ฉันสามารถใช้ Aspose.CAD สำหรับทั้งโครงการเชิงพาณิชย์และโครงการส่วนตัวได้หรือไม่

 ตอบ 2: ใช่ Aspose.CAD เสนอตัวเลือกสิทธิ์การใช้งานที่ยืดหยุ่นสำหรับการใช้งานเชิงพาณิชย์และส่วนบุคคล เยี่ยมชม[หน้าซื้อ](https://purchase.aspose.com/buy) สำหรับรายละเอียดเพิ่มเติม

### คำถามที่ 3: ฉันจะขอรับใบอนุญาตชั่วคราวสำหรับ Aspose.CAD ได้อย่างไร

 A3: คุณสามารถขอรับใบอนุญาตชั่วคราวได้จาก[ที่นี่](https://purchase.aspose.com/temporary-license/) เพื่อวัตถุประสงค์ในการประเมินผล

### คำถามที่ 4: ฉันจะรับการสนับสนุนสำหรับ Aspose.CAD ได้ที่ไหน

A4: หากมีข้อสงสัยหรือความช่วยเหลือ โปรดไปที่[ฟอรั่ม Aspose.CAD](https://forum.aspose.com/c/cad/19).

### คำถามที่ 5: Aspose.CAD มีรุ่นทดลองใช้ฟรีหรือไม่

 A5: ได้ คุณสามารถเข้าถึง Aspose.CAD เวอร์ชันทดลองใช้ฟรีได้[ที่นี่](https://releases.aspose.com/).