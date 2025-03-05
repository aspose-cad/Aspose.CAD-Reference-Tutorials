---
title: การส่งออกเค้าโครง DXF เฉพาะไปยังรูปภาพ - บทช่วยสอน Aspose.CAD
linktitle: การส่งออกเค้าโครง DXF เฉพาะไปยังรูปภาพ
second_title: Aspose.CAD .NET - รูปแบบไฟล์ CAD และ BIM
description: สำรวจคำแนะนำทีละขั้นตอนเกี่ยวกับการใช้ Aspose.CAD สำหรับ .NET เพื่อส่งออกเค้าโครง DXF เฉพาะไปยังรูปภาพ เพิ่มประสิทธิภาพการพัฒนา .NET ของคุณให้สูงสุดด้วยบทช่วยสอนอันทรงพลังนี้
type: docs
weight: 10
url: /th/net/layout-and-object-handling/exporting-specific-dxf-layout-to-image/
---
## การแนะนำ

ในขอบเขตของการพัฒนา .NET นั้น Aspose.CAD มีความโดดเด่นในฐานะเครื่องมืออันทรงพลังสำหรับการจัดการไฟล์ Computer-Aided Design (CAD) โดยเฉพาะอย่างยิ่ง มีฟังก์ชันการทำงานที่ครอบคลุมสำหรับการส่งออกเค้าโครง DXF เฉพาะไปยังรูปภาพ บทช่วยสอนนี้จะแนะนำคุณตลอดกระบวนการทีละขั้นตอน ช่วยให้คุณสามารถควบคุมความสามารถของ Aspose.CAD ได้อย่างง่ายดาย

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเข้าสู่บทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

-  ไลบรารี Aspose.CAD: ดาวน์โหลดและติดตั้งไลบรารี Aspose.CAD จากไฟล์[หน้าปล่อย](https://releases.aspose.com/cad/net/).

- สภาพแวดล้อมการพัฒนา: ตรวจสอบให้แน่ใจว่าคุณได้ตั้งค่าสภาพแวดล้อมการพัฒนา .NET บนเครื่องของคุณ

## นำเข้าเนมสเปซ

ในโปรเจ็กต์ .NET ของคุณ ให้เริ่มต้นด้วยการนำเข้าเนมสเปซที่จำเป็นเพื่อเข้าถึงฟังก์ชันการทำงานที่ Aspose.CAD มอบให้:

```csharp
using System;
```

## ขั้นตอนที่ 1: ตั้งค่าโครงการของคุณ

สร้างโปรเจ็กต์ .NET ใหม่หรือเปิดโปรเจ็กต์ที่มีอยู่ซึ่งคุณวางแผนจะใช้ฟังก์ชัน Aspose.CAD

## ขั้นตอนที่ 2: โหลดอิมเมจ CAD

ใช้รหัสต่อไปนี้เพื่อโหลดภาพ CAD จากเส้นทางไฟล์ที่คุณระบุ:

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "for_layers_test.dwf";

using (var image = (Aspose.CAD.FileFormats.Cad.CadImage)Aspose.CAD.Image.Load(sourceFilePath))
{
    // รหัสของคุณสำหรับขั้นตอนต่อไปจะอยู่ที่นี่
}
```

## ขั้นตอนที่ 3: กำหนดค่าตัวเลือกการแรสเตอร์

ตั้งค่าตัวเลือกการแรสเตอร์โดยระบุความกว้างและความสูงของหน้า:

```csharp
var rasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
```

## ขั้นตอนที่ 4: วนซ้ำเลเยอร์

ดึงเลเยอร์จากอิมเมจ CAD และวนซ้ำเลเยอร์เหล่านั้น:

```csharp
var layersList = image.Layers;
foreach (var layerName in layersList.GetLayersNames())
{
    // รหัสของคุณสำหรับขั้นตอนต่อไปจะอยู่ที่นี่
}
```

## ขั้นตอนที่ 5: ส่งออกเลเยอร์ไปยังรูปภาพ

สำหรับแต่ละเลเยอร์ ให้ส่งออกเป็นภาพ JPEG โดยใช้ตัวเลือกที่กำหนดค่าไว้:

```csharp
rasterizationOptions.Layers = new string[] { layerName };
var options = new Aspose.CAD.ImageOptions.JpegOptions();
options.VectorRasterizationOptions = rasterizationOptions;
image.Save(layerName + "_out.jpg", options);
```

ทำซ้ำขั้นตอนเหล่านี้สำหรับแต่ละเลเยอร์ในภาพ CAD

## บทสรุป

ยินดีด้วย! คุณได้เรียนรู้วิธีส่งออกเค้าโครง DXF เฉพาะไปยังรูปภาพโดยใช้ Aspose.CAD ในสภาพแวดล้อม .NET เรียบร้อยแล้ว บทช่วยสอนนี้ได้จัดเตรียมขั้นตอนที่จำเป็นเพื่อให้คุณได้รับประโยชน์สูงสุดจากไลบรารีอันทรงพลังนี้

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถใช้ Aspose.CAD กับเฟรมเวิร์ก .NET อื่นๆ ได้หรือไม่

ตอบ 1: ใช่ Aspose.CAD เข้ากันได้กับเฟรมเวิร์ก .NET ต่างๆ ซึ่งให้ความยืดหยุ่นสำหรับความต้องการในการพัฒนาของคุณ

### คำถามที่ 2: Aspose.CAD มีใบอนุญาตชั่วคราวหรือไม่

 A2: ได้ คุณสามารถขอรับใบอนุญาตชั่วคราวสำหรับ Aspose.CAD ได้จาก[ที่นี่](https://purchase.aspose.com/temporary-license/).

### คำถามที่ 3: ฉันจะรับการสนับสนุนสำหรับ Aspose.CAD ได้อย่างไร

 A3: เยี่ยมชม[ฟอรั่ม Aspose.CAD](https://forum.aspose.com/c/cad/19) เพื่อรับการสนับสนุนและความช่วยเหลือจากชุมชน

### คำถามที่ 4: Aspose.CAD มีรุ่นทดลองใช้ฟรีหรือไม่

 A4: ได้ คุณสามารถทดลองใช้ Aspose.CAD ได้ฟรี[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 5: ฉันจะหาเอกสารโดยละเอียดสำหรับ Aspose.CAD ได้ที่ไหน

 A5: อ้างถึงเนื้อหาที่ครอบคลุม[เอกสาร Aspose.CAD](https://reference.aspose.com/cad/net/) เพื่อข้อมูลเชิงลึก