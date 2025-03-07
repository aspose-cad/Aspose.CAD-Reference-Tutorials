---
title: การแสดงสีในไฟล์ CAD - คู่มือ Aspose.CAD
linktitle: การแสดงสีในไฟล์ CAD
second_title: Aspose.CAD .NET - รูปแบบไฟล์ CAD และ BIM
description: การเรนเดอร์ไฟล์ Master CAD ใน .NET ด้วย Aspose.CAD ปฏิบัติตามคำแนะนำทีละขั้นตอนของเราเพื่อสีสันสดใส
weight: 10
url: /th/net/conversion-and-export/rendering-colors-in-cad-files/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# การแสดงสีในไฟล์ CAD - คู่มือ Aspose.CAD

## การแนะนำ

คุณกำลังเผชิญกับความท้าทายในการเรนเดอร์สีในไฟล์ CAD โดยใช้ .NET หรือไม่? ไม่ต้องมองอีกต่อไป! ในคู่มือที่ครอบคลุมนี้ เราจะแนะนำคุณตลอดกระบวนการทีละขั้นตอนโดยใช้ไลบรารี Aspose.CAD อันทรงพลัง เมื่อสิ้นสุดบทช่วยสอนนี้ คุณจะได้รับความรู้ในการเรนเดอร์สีในไฟล์ CAD ของคุณอย่างง่ายดาย

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเจาะลึกบทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

-  ไลบรารี Aspose.CAD: ดาวน์โหลดและติดตั้งไลบรารี Aspose.CAD จาก[ที่นี่](https://releases.aspose.com/cad/net/).

- สภาพแวดล้อมการพัฒนา: ตรวจสอบให้แน่ใจว่าคุณได้ตั้งค่าสภาพแวดล้อมการพัฒนา .NET แล้ว

- ไฟล์ CAD: เตรียมไฟล์ CAD ตัวอย่างให้พร้อมสำหรับการทดสอบ คุณสามารถใช้ "test1.dwg" สำหรับบทช่วยสอนนี้

## นำเข้าเนมสเปซ

ในโปรเจ็กต์ .NET ของคุณ ให้นำเข้าเนมสเปซที่จำเป็นเพื่อเข้าถึงฟังก์ชัน Aspose.CAD เพิ่มบรรทัดต่อไปนี้ที่จุดเริ่มต้นของโค้ดของคุณ:

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

## ขั้นตอนที่ 1: ตั้งค่าโครงการของคุณ

สร้างโปรเจ็กต์ .NET ใหม่และตั้งค่าไดเร็กทอรีที่จำเป็น ตรวจสอบให้แน่ใจว่าไลบรารี Aspose.CAD ถูกอ้างอิงในโปรเจ็กต์ของคุณ

## ขั้นตอนที่ 2: กำหนดเส้นทางไฟล์

ระบุเส้นทางสำหรับไฟล์ CAD อินพุตและไฟล์ PNG เอาต์พุตของคุณ อัปเดตบรรทัดต่อไปนี้ในโค้ดของคุณ:

```csharp
string MyDir = "Your Document Directory";
string inputFile = MyDir + "test1.dwg";
string outputFile = MyDir + "test1.png";
```

## ขั้นตอนที่ 3: โหลดไฟล์ CAD

ใช้รหัสต่อไปนี้เพื่อเปิดและโหลดไฟล์ CAD:

```csharp
using (FileStream fs = new FileStream(inputFile, FileMode.Open))
{
    using (FileStream output = new FileStream(outputFile, FileMode.Create))
    {
        Image document = Image.Load(fs);
```

## ขั้นตอนที่ 4: กำหนดค่าตัวเลือกการแรสเตอร์

กำหนดค่าตัวเลือกการแรสเตอร์เพื่อปรับแต่งกระบวนการเรนเดอร์ อัพเดตบรรทัดต่อไปนี้:

```csharp
PngOptions saveOptions = new PngOptions();

CadRasterizationOptions options = new CadRasterizationOptions();
options.NoScaling = false;
options.PageHeight = document.Height * 10;
options.PageWidth = document.Width * 10;
options.DrawType = Aspose.CAD.FileFormats.Cad.CadDrawTypeMode.UseObjectColor;
saveOptions.VectorRasterizationOptions = options;
```

## ขั้นตอนที่ 5: บันทึกภาพที่แสดงผล

บันทึกภาพที่แสดงผลโดยใช้ตัวเลือกที่ระบุ:

```csharp
document.Save(output, saveOptions);
```

## บทสรุป

ยินดีด้วย! คุณเรนเดอร์สีในไฟล์ CAD ได้สำเร็จโดยใช้ Aspose.CAD สำหรับ .NET คำแนะนำทีละขั้นตอนนี้ช่วยให้คุณมีทักษะในการปรับปรุงความสามารถในการเรนเดอร์ CAD ของคุณ

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถใช้ Aspose.CAD ได้ฟรีหรือไม่

 A1: Aspose.CAD มีเวอร์ชันทดลองใช้ฟรีให้ใช้งาน[ที่นี่](https://releases.aspose.com/)คุณสามารถสำรวจคุณสมบัติต่างๆ ได้ก่อนตัดสินใจซื้อ

### คำถามที่ 2: ฉันจะหาเอกสารโดยละเอียดสำหรับ Aspose.CAD ได้ที่ไหน

 A2: โปรดดูเอกสารประกอบ[ที่นี่](https://reference.aspose.com/cad/net/) สำหรับข้อมูลเชิงลึกเกี่ยวกับฟังก์ชันการทำงานของ Aspose.CAD

### คำถามที่ 3: ฉันจะได้รับใบอนุญาตชั่วคราวสำหรับ Aspose.CAD ได้อย่างไร

 A3: รับใบอนุญาตชั่วคราว[ที่นี่](https://purchase.aspose.com/temporary-license/) เพื่อวัตถุประสงค์ในการทดสอบ

### Q4: ต้องการความช่วยเหลือหรือมีคำถาม?

 A4: เยี่ยมชมชุมชน Aspose.CAD[ฟอรั่ม](https://forum.aspose.com/c/cad/19) สำหรับการสนับสนุนและการอภิปราย

### คำถามที่ 5: ฉันจะซื้อไลบรารี Aspose.CAD ได้ที่ไหน

 A5: ซื้อ Aspose.CAD[ที่นี่](https://purchase.aspose.com/buy) เพื่อปลดล็อกศักยภาพอันเต็มเปี่ยม
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
