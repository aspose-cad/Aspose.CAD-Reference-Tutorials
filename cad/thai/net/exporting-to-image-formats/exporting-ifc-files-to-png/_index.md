---
title: การส่งออกไฟล์ IFC เป็น PNG - บทช่วยสอน Aspose.CAD
linktitle: การส่งออกไฟล์ IFC เป็น PNG
second_title: Aspose.CAD .NET - รูปแบบไฟล์ CAD และ BIM
description: สำรวจ Aspose.CAD สำหรับ .NET ซึ่งเป็นโซลูชันที่มีประสิทธิภาพสำหรับการแปลง IFC เป็น PNG ได้อย่างราบรื่น ดาวน์โหลดตอนนี้เพื่อการประมวลผลไฟล์ CAD ที่มีประสิทธิภาพ
weight: 10
url: /th/net/exporting-to-image-formats/exporting-ifc-files-to-png/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# การส่งออกไฟล์ IFC เป็น PNG - บทช่วยสอน Aspose.CAD

## การแนะนำ

ในโลกแบบไดนามิกของการออกแบบโดยใช้คอมพิวเตอร์ช่วย (CAD) การแปลงไฟล์อย่างมีประสิทธิภาพถือเป็นสิ่งสำคัญ Aspose.CAD สำหรับ .NET กลายเป็นเครื่องมืออันทรงพลังที่นำเสนอความสามารถที่ราบรื่นสำหรับการส่งออกไฟล์ IFC (Industry Foundation Classes) เป็นรูปแบบ PNG บทช่วยสอนแบบทีละขั้นตอนนี้จะแนะนำคุณตลอดกระบวนการ เพื่อให้มั่นใจว่าจะได้รับประสบการณ์ที่ราบรื่นกับ Aspose.CAD

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเข้าสู่บทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

### 1. การติดตั้ง Aspose.CAD

 ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง Aspose.CAD สำหรับ .NET แล้ว คุณสามารถดาวน์โหลดได้จากหน้าเผยแพร่[ที่นี่](https://releases.aspose.com/cad/net/).

### 2. ไดเร็กทอรีเอกสาร

 สร้างไดเร็กทอรีที่กำหนดสำหรับเอกสารของคุณ ในตัวอย่างที่ให้มา ตัวแปร`MyDir` แสดงถึงไดเร็กทอรีเอกสาร

## นำเข้าเนมสเปซ

ตอนนี้คุณได้ตั้งค่าข้อกำหนดเบื้องต้นแล้ว เรามานำเข้าเนมสเปซที่จำเป็นในแอปพลิเคชัน .NET ของคุณเพื่อใช้ฟังก์ชัน Aspose.CAD กันดีกว่า

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using Aspose.CAD.FileFormats.Ifc;
```

## ขั้นตอนที่ 1: โหลดไฟล์ IFC

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "example.ifc";
using (IfcImage cadImage = (IfcImage)Image.Load(sourceFilePath))
{
```

 ในขั้นตอนนี้ เราจะเริ่มต้น Aspose.CAD`IfcImage` object และโหลดไฟล์ IFC ลงไป

## ขั้นตอนที่ 2: ตั้งค่าตัวเลือกการแรสเตอร์

```csharp
    CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
   
    rasterizationOptions.PageWidth = 100;
    rasterizationOptions.PageHeight = 100;
```

กำหนดตัวเลือกการแรสเตอร์เพื่อกำหนดค่าความกว้างและความสูงของหน้าสำหรับเอาต์พุต PNG

## ขั้นตอนที่ 3: ตั้งค่าตัวเลือก PNG

```csharp
    PngOptions pngOptions = new PngOptions();
    pngOptions.VectorRasterizationOptions = rasterizationOptions;
```

สร้างตัวเลือก PNG และเชื่อมโยงตัวเลือกการแรสเตอร์ที่กำหนดไว้ก่อนหน้านี้

## ขั้นตอนที่ 4: ระบุเส้นทางเอาต์พุต

```csharp
    // กำหนดเส้นทางเอาต์พุตด้วย
    string outPath = sourceFilePath + ".png";
    cadImage.Save(outPath, pngOptions);
}
```

กำหนดเส้นทางเอาต์พุตสำหรับไฟล์ PNG โดยตรวจสอบให้แน่ใจว่ามีชื่อเดียวกันกับไฟล์ต้นฉบับที่มีนามสกุล ".png" สุดท้าย ให้บันทึกภาพที่แปลงแล้ว

## บทสรุป

ด้วยขั้นตอนที่ไม่ซับซ้อนเหล่านี้ คุณได้ส่งออกไฟล์ IFC ไปยัง PNG โดยใช้ Aspose.CAD สำหรับ .NET ได้สำเร็จ เครื่องมืออเนกประสงค์นี้ทำให้กระบวนการแปลง CAD ง่ายขึ้น ทำให้นักพัฒนาและวิศวกรสามารถเข้าถึงได้

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถใช้ Aspose.CAD สำหรับ .NET บน macOS หรือ Linux ได้หรือไม่

ตอบ 1: ไม่ Aspose.CAD สำหรับ .NET ได้รับการออกแบบมาเป็นพิเศษสำหรับสภาพแวดล้อม Windows

### คำถามที่ 2: มีใบอนุญาตชั่วคราวสำหรับการทดสอบหรือไม่

 A2: ได้ คุณสามารถขอรับใบอนุญาตชั่วคราวได้จาก[ที่นี่](https://purchase.aspose.com/temporary-license/) สำหรับการประเมินผล

### คำถามที่ 3: ฉันจะรับการสนับสนุนสำหรับ Aspose.CAD ได้อย่างไร

 A3: เยี่ยมชม[ฟอรั่ม Aspose.CAD](https://forum.aspose.com/c/cad/19) สำหรับการสนับสนุนและการอภิปรายของชุมชน

### คำถามที่ 4: ฉันจะหาเอกสารประกอบที่ครอบคลุมได้จากที่ไหน?

 A4: โปรดดูที่[เอกสาร Aspose.CAD](https://reference.aspose.com/cad/net/) สำหรับข้อมูลโดยละเอียดและตัวอย่าง

### คำถามที่ 5: จะเกิดอะไรขึ้นหากฉันประสบปัญหาระหว่างการติดตั้ง?

 A5: ตรวจสอบเอกสารหรือขอความช่วยเหลือจาก[ฟอรั่ม Aspose.CAD](https://forum.aspose.com/c/cad/19).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
