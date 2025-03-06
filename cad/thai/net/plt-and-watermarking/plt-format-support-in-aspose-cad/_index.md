---
title: รองรับรูปแบบ PLT ใน Aspose.CAD - บทช่วยสอนที่ครอบคลุม
linktitle: รองรับรูปแบบ PLT ใน Aspose.CAD - บทช่วยสอน
second_title: Aspose.CAD .NET - รูปแบบไฟล์ CAD และ BIM
description: ค้นพบการสนับสนุนรูปแบบ PLT ที่ไร้รอยต่อใน Aspose.CAD สำหรับ .NET ปฏิบัติตามคำแนะนำทีละขั้นตอนของเราเพื่อรวมไฟล์ PLT เข้ากับแอปพลิเคชัน .NET ของคุณได้อย่างง่ายดาย
weight: 10
url: /th/net/plt-and-watermarking/plt-format-support-in-aspose-cad/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# รองรับรูปแบบ PLT ใน Aspose.CAD - บทช่วยสอนที่ครอบคลุม

## การแนะนำ

ยินดีต้อนรับสู่บทช่วยสอนเชิงลึกของเราเกี่ยวกับการรองรับรูปแบบ PLT ใน Aspose.CAD สำหรับ .NET! หากคุณเป็นนักพัฒนาที่ต้องการทำงานกับไฟล์ PLT และใช้ประโยชน์จากประสิทธิภาพของ Aspose.CAD แสดงว่าคุณมาถูกที่แล้ว ในคู่มือนี้ เราจะอธิบายขั้นตอนสำคัญ ข้อกำหนดเบื้องต้น และให้ตัวอย่างโดยละเอียดเพื่อให้แน่ใจว่าคุณสามารถรวมการสนับสนุน PLT เข้ากับแอปพลิเคชัน .NET ของคุณได้อย่างราบรื่น

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเข้าสู่บทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:
-  Aspose.CAD สำหรับ .NET: ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้งไลบรารี Aspose.CAD แล้ว หากไม่ใช่คุณสามารถดาวน์โหลดได้จาก[ที่นี่](https://releases.aspose.com/cad/net/).
- สภาพแวดล้อมการพัฒนา: ตั้งค่าสภาพแวดล้อมการพัฒนา .NET ของคุณด้วยเครื่องมือที่จำเป็น
เมื่อคุณตั้งค่าทุกอย่างเรียบร้อยแล้ว มาเริ่มกันเลย!

## นำเข้าเนมสเปซ

ในโปรเจ็กต์ .NET ของคุณ ให้เริ่มด้วยการนำเข้าเนมสเปซที่จำเป็น ขั้นตอนนี้มีความสำคัญอย่างยิ่งในการเข้าถึงฟังก์ชัน Aspose.CAD
```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## ขั้นตอนที่ 1: ตั้งค่าโครงการของคุณ

เริ่มต้นด้วยการสร้างโครงการ .NET ใหม่ในสภาพแวดล้อมการพัฒนาที่คุณต้องการ

## ขั้นตอนที่ 2: เพิ่มการอ้างอิง Aspose.CAD

 อ้างอิงไลบรารี Aspose.CAD ในโปรเจ็กต์ของคุณ คุณสามารถทำได้โดยใช้ NuGet Package Manager หรือดาวน์โหลดไลบรารีจาก[เว็บไซต์กำหนด](https://purchase.aspose.com/buy).

## ขั้นตอนที่ 3: รวมเนมสเปซ Aspose.CAD

รวมเนมสเปซ Aspose.CAD ที่จำเป็นไว้ที่ตอนต้นของไฟล์โค้ดของคุณ ดังที่แสดงไว้ในส่วน "นำเข้าเนมสเปซ" ด้านบน

## ขั้นตอนที่ 4: โหลดไฟล์ PLT

 ระบุเส้นทางไปยังไฟล์ PLT ของคุณและโหลดโดยใช้นามสกุลไฟล์`Image.Load` วิธี.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "themepark.plt";
Image image = Image.Load((sourceFilePath));
```

## ขั้นตอนที่ 5: กำหนดค่าตัวเลือกการแรสเตอร์

กำหนดตัวเลือกการแรสเตอร์สำหรับไฟล์ PLT เช่น ความสูงของหน้า ความกว้างของหน้า ฯลฯ

```csharp
ImageOptionsBase imageOptions = new JpegOptions();
CadRasterizationOptions options = new CadRasterizationOptions
{
    PageHeight = 500,
    PageWidth = 1000,
};
imageOptions.VectorRasterizationOptions = options;
```

## ขั้นตอนที่ 6: บันทึกเป็น JPEG

บันทึกไฟล์ PLT ที่แรสเตอร์เป็นรูปภาพ JPEG

```csharp
image.Save((MyDir+"themepark.jpg"), imageOptions);
```

## ขั้นตอนที่ 7: รหัสสุดท้าย

ตรวจสอบให้แน่ใจว่าโค้ดของคุณดูเหมือนตัวอย่างที่ให้ไว้ในส่วน "บทช่วยสอน" ด้านบน นี่เป็นข้อมูลโค้ดที่สมบูรณ์สำหรับการรองรับรูปแบบ PLT

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "themepark.plt";
Image image = Image.Load((sourceFilePath));
ImageOptionsBase imageOptions = new JpegOptions();
CadRasterizationOptions options = new CadRasterizationOptions
{
    PageHeight = 500,
    PageWidth = 1000,
};
imageOptions.VectorRasterizationOptions = options;
image.Save((MyDir+"themepark.jpg"), imageOptions);
```

ยินดีด้วย! คุณได้รวมการสนับสนุนรูปแบบ PLT โดยใช้ Aspose.CAD สำหรับ .NET เรียบร้อยแล้ว

## บทสรุป

ในบทช่วยสอนนี้ เราได้กล่าวถึงขั้นตอนสำคัญในการทำงานกับไฟล์ PLT โดยใช้ Aspose.CAD สำหรับ .NET ด้วยการทำตามขั้นตอนเหล่านี้ คุณสามารถปรับปรุงแอปพลิเคชัน .NET ของคุณด้วยการสนับสนุนรูปแบบ PLT ที่มีประสิทธิภาพ

## คำถามที่พบบ่อย

### คำถามที่ 1: Aspose.CAD เข้ากันได้กับรูปแบบ CAD อื่นๆ หรือไม่

ตอบ 1: ใช่ Aspose.CAD รองรับรูปแบบ CAD ที่หลากหลาย ทำให้มีความเป็นไปได้ในการบูรณาการที่หลากหลาย

### คำถามที่ 2: ฉันสามารถปรับแต่งตัวเลือกการแรสเตอร์สำหรับรูปแบบเอาต์พุตต่างๆ ได้หรือไม่

A2: แน่นอน! ดังที่แสดงในบทช่วยสอน คุณสามารถปรับแต่งตัวเลือกการแรสเตอร์ได้ตามความต้องการเฉพาะของคุณ

### คำถามที่ 3: ฉันจะรับการสนับสนุนเพิ่มเติมหรือการสนทนาในชุมชนได้จากที่ไหน

 A3: เยี่ยมชม[ฟอรั่ม Aspose.CAD](https://forum.aspose.com/c/cad/19) สำหรับการสนับสนุนและการมีปฏิสัมพันธ์กับชุมชน

### คำถามที่ 4: มีการทดลองใช้ฟรีหรือไม่?

 A4: ได้ คุณสามารถทดลองใช้งานฟรีได้[ที่นี่](https://releases.aspose.com/) เพื่อสัมผัสความสามารถของ Aspose.CAD

### คำถามที่ 5: ฉันจะขอรับใบอนุญาตชั่วคราวได้อย่างไร

 A5: สำหรับใบอนุญาตชั่วคราว โปรดไปที่[ลิงค์นี้](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
