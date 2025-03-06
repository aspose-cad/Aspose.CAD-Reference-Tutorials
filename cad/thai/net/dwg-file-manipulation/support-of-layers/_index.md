---
title: การจัดการเลเยอร์ในไฟล์ DWG ด้วย C# - บทช่วยสอน Aspose.CAD
linktitle: การจัดการเลเยอร์ในไฟล์ DWG ด้วย C#
second_title: Aspose.CAD .NET - รูปแบบไฟล์ CAD และ BIM
description: เรียนรู้วิธีจัดการเลเยอร์ในไฟล์ DWG โดยใช้ C# กับ Aspose.CAD สำหรับ .NET คำแนะนำทีละขั้นตอนสำหรับการจัดการไฟล์ CAD ที่มีประสิทธิภาพ
weight: 11
url: /th/net/dwg-file-manipulation/support-of-layers/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# การจัดการเลเยอร์ในไฟล์ DWG ด้วย C# - บทช่วยสอน Aspose.CAD

## การแนะนำ

ยินดีต้อนรับสู่บทช่วยสอนเชิงลึกเกี่ยวกับการจัดการเลเยอร์ในไฟล์ DWG โดยใช้ C# กับ Aspose.CAD สำหรับ .NET Aspose.CAD เป็นไลบรารีอันทรงพลังที่ช่วยให้นักพัฒนาสามารถทำงานกับรูปแบบไฟล์ CAD ได้อย่างราบรื่น ในบทช่วยสอนนี้ เราจะแนะนำคุณตลอดกระบวนการจัดการเลเยอร์ในไฟล์ DWG ทีละขั้นตอน

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเจาะลึกบทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

- ความรู้พื้นฐานเกี่ยวกับภาษาการเขียนโปรแกรม C#
- ติดตั้ง Visual Studio บนเครื่องของคุณแล้ว
-  Aspose.CAD สำหรับไลบรารี .NET ซึ่งคุณสามารถดาวน์โหลดได้จากไฟล์[เว็บไซต์ Aspose.CAD](https://releases.aspose.com/cad/net/).

## นำเข้าเนมสเปซ

ในการเริ่มต้น ให้นำเข้าเนมสเปซที่จำเป็นลงในโปรเจ็กต์ C# ของคุณ เนมสเปซเหล่านี้มีฟังก์ชันที่จำเป็นสำหรับการทำงานกับไฟล์ CAD

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

## ขั้นตอนที่ 1: โหลดไฟล์ DWG

เริ่มต้นด้วยการโหลดไฟล์ DWG ลงในแอปพลิเคชัน C# ของคุณโดยใช้ไลบรารี Aspose.CAD

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "for_layers_test.dwf";

using (Aspose.CAD.Image image = Aspose.CAD.Image.Load(sourceFilePath))
{
    // รหัสของคุณสำหรับขั้นตอนต่อไปอยู่ที่นี่
}
```

## ขั้นตอนที่ 2: กำหนดค่าตัวเลือกการแรสเตอร์

 สร้างอินสแตนซ์ของ`CadRasterizationOptions` และตั้งค่าคุณสมบัติเพื่อกำหนดวิธีการแรสเตอร์ไฟล์ DWG

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions rasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
```

## ขั้นตอนที่ 3: ระบุเลเยอร์

เพิ่มเลเยอร์ที่ต้องการลงในตัวเลือกแรสเตอร์ ในตัวอย่างนี้ เราได้เพิ่ม "LayerA"

```csharp
rasterizationOptions.Layers = new string[] { "LayerA" };
```

## ขั้นตอนที่ 4: กำหนดค่าตัวเลือกการส่งออกรูปภาพ

 สร้างตัวเลือกการส่งออกรูปภาพที่จำเป็น นี่เราใช้อยู่.`JpegOptions` เพื่อส่งออกเป็น JPEG

```csharp
JpegOptions jpegOptions = new JpegOptions();
jpegOptions.VectorRasterizationOptions = rasterizationOptions;
```

## ขั้นตอนที่ 5: บันทึกภาพที่ส่งออก

ระบุเส้นทางเอาต์พุตและบันทึกไฟล์ DWG ที่แรสเตอร์เป็น JPEG

```csharp
MyDir = MyDir + "for_layers_test.jpg";
image.Save(MyDir, jpegOptions);
```

ตอนนี้ คุณได้จัดการเลเยอร์ในไฟล์ DWG โดยใช้ C# กับ Aspose.CAD สำหรับ .NET เรียบร้อยแล้ว

## บทสรุป

ในบทช่วยสอนนี้ เราได้อธิบายขั้นตอนการจัดการเลเยอร์ในไฟล์ DWG โดยใช้ C# และไลบรารี Aspose.CAD เมื่อทำตามขั้นตอนเหล่านี้ คุณจะทำงานกับไฟล์ CAD ในแอปพลิเคชัน .NET ของคุณได้อย่างมีประสิทธิภาพ

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถจัดการหลายเลเยอร์พร้อมกันได้หรือไม่

 A1: ใช่คุณทำได้ เพียงเพิ่มชื่อเลเยอร์ลงใน`rasterizationOptions.Layers` อาร์เรย์

### คำถามที่ 2: Aspose.CAD เวอร์ชันทดลองใช้งานมีให้ใช้งานหรือไม่

 A2: ได้ คุณสามารถดาวน์โหลดเวอร์ชันทดลองใช้ฟรีได้จาก[ที่นี่](https://releases.aspose.com/).

### Q3: ฉันจะหาเอกสารได้จากที่ไหน?

 A3: มีเอกสารประกอบให้[ที่นี่](https://reference.aspose.com/cad/net/).

### คำถามที่ 4: ฉันจะได้รับการสนับสนุนสำหรับ Aspose.CAD ได้อย่างไร

 A4: คุณสามารถขอรับการสนับสนุนได้ที่[ฟอรั่ม Aspose.CAD](https://forum.aspose.com/c/cad/19).

### คำถามที่ 5: Aspose.CAD มีตัวเลือกการอนุญาตให้ใช้สิทธิอะไรบ้าง

 A5: คุณสามารถสำรวจตัวเลือกใบอนุญาตและรายละเอียดการซื้อได้[ที่นี่](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
