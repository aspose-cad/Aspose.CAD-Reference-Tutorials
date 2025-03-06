---
title: ส่งออก DGN เป็นภาพแรสเตอร์ใน Aspose.CAD สำหรับ .NET
linktitle: ส่งออก DGN เป็นภาพแรสเตอร์
second_title: Aspose.CAD .NET - รูปแบบไฟล์ CAD และ BIM
description: แปลง DGN เป็นภาพแรสเตอร์ได้อย่างง่ายดายโดยใช้ Aspose.CAD สำหรับ .NET สำรวจคำแนะนำทีละขั้นตอนและปลดปล่อยพลังของ .NET ในการจัดการไฟล์ CAD
weight: 13
url: /th/net/cad-export-formats/export-dgn-to-raster-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ส่งออก DGN เป็นภาพแรสเตอร์ใน Aspose.CAD สำหรับ .NET

## การแนะนำ

ในขอบเขตแบบไดนามิกของการพัฒนา .NET Aspose.CAD กลายเป็นเครื่องมืออันทรงพลังสำหรับการจัดการไฟล์ Computer-Aided Design (CAD) บทช่วยสอนนี้จะเจาะลึกเกี่ยวกับกระบวนการส่งออกไฟล์ DGN ไปเป็นภาพแรสเตอร์โดยใช้ Aspose.CAD สำหรับ .NET หากคุณกระตือรือร้นที่จะแปลงไฟล์ DGN ของคุณให้เป็นภาพแรสเตอร์ที่สวยงามน่าดึงดูดได้อย่างราบรื่น แสดงว่าคุณมาถูกที่แล้ว

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเริ่มต้นการเดินทางนี้ ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

-  Aspose.CAD สำหรับ .NET: ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้งไลบรารี Aspose.CAD ในโปรเจ็กต์ .NET ของคุณ คุณสามารถค้นหาห้องสมุดและเอกสารที่เกี่ยวข้องได้ที่[เว็บไซต์](https://reference.aspose.com/cad/net/).

- ไฟล์ DGN ตัวอย่าง: เตรียมไฟล์ DGN พร้อมสำหรับการแปลง ในตัวอย่างของเรา เราจะใช้ "Nikon_D90_Camera.dgn"

ตอนนี้ เรามาดูรายละเอียดคำแนะนำทีละขั้นตอนกันดีกว่า

## นำเข้าเนมสเปซ

ในโปรเจ็กต์ .NET ของคุณ ให้เริ่มด้วยการนำเข้าเนมสเปซที่จำเป็นสำหรับ Aspose.CAD ขั้นตอนนี้ช่วยให้คุณเข้าถึงคลาสและวิธีการที่จำเป็นสำหรับ DGN เพื่อการแปลงภาพแรสเตอร์

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## ขั้นตอนที่ 1: โหลดไฟล์ DGN

 เริ่มต้นด้วยการโหลดไฟล์ DGN ลงในไฟล์`CadImage` วัตถุ. นี่เป็นรากฐานสำหรับการดำเนินงานครั้งต่อไป

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // รหัสของคุณสำหรับการประมวลผลเพิ่มเติมอยู่ที่นี่
}
```

## ขั้นตอนที่ 2: กำหนดตัวเลือกการแรสเตอร์

 สร้างก`CadRasterizationOptions` object และตั้งค่าคุณสมบัติต่างๆ เพื่อปรับแต่งกระบวนการแรสเตอร์ไรซ์ตามความต้องการของคุณ

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 600;
rasterizationOptions.PageHeight = 300;
rasterizationOptions.NoScaling = true;
rasterizationOptions.AutomaticLayoutsScaling = false;
```

## ขั้นตอนที่ 3: สร้างวัตถุ JpegOptions

 เนื่องจากเรามุ่งมั่นที่จะแปลงไฟล์ DGN เป็น JPEG ให้สร้างไฟล์`JpegOptions` วัตถุและกำหนดที่กำหนดไว้ก่อนหน้านี้`CadRasterizationOptions` ถึงมัน

```csharp
ImageOptionsBase options = new JpegOptions();
options.VectorRasterizationOptions = rasterizationOptions;
```

## ขั้นตอนที่ 4: บันทึกภาพแรสเตอร์

 ใช้`Save` วิธีการของ`CadImage` เพื่อส่งออกไฟล์ DGN ไปยังภาพแรสเตอร์ในรูปแบบที่ต้องการ ในกรณีนี้คือ JPEG

```csharp
cadImage.Save(MyDir + "ExportDGNToRasterImage_out.jpg", options);
```

## บทสรุป

ยินดีด้วย! คุณได้ทำตามขั้นตอนในการส่งออกไฟล์ DGN ไปยังอิมเมจแรสเตอร์โดยใช้ Aspose.CAD สำหรับ .NET สำเร็จแล้ว บทช่วยสอนนี้ช่วยให้คุณมีความรู้ที่จำเป็นในการรวมฟังก์ชันนี้เข้ากับโปรเจ็กต์ .NET ของคุณได้อย่างง่ายดาย

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถส่งออกไฟล์ DGN ไปเป็นรูปแบบอื่นที่ไม่ใช่ JPEG ได้หรือไม่

A1: ใช่ Aspose.CAD สำหรับ .NET รองรับรูปแบบเอาต์พุตที่หลากหลาย คุณสามารถแก้ไขตัวเลือกได้ตามขั้นตอนที่ 3

### Q2 ฉันจะจัดการกับข้อยกเว้นในระหว่างกระบวนการแปลงได้อย่างไร

A2: ตรวจสอบให้แน่ใจว่าคุณมีการจัดการข้อยกเว้นที่เหมาะสม ดังที่แสดงในโค้ดที่ให้มา เพื่อแก้ไขปัญหาที่อาจเกิดขึ้น

### คำถามที่ 3: มี Aspose.CAD สำหรับ .NET รุ่นทดลองใช้งานหรือไม่

 A3: ได้ คุณสามารถสำรวจผลิตภัณฑ์ได้ด้วยการทดลองใช้ฟรี เยี่ยม[ที่นี่](https://releases.aspose.com/) สำหรับข้อมูลเพิ่มเติม.

### คำถามที่ 4: ฉันจะขอความช่วยเหลือหรือหารือเกี่ยวกับปัญหาที่เกี่ยวข้องกับ Aspose.CAD สำหรับ .NET ได้ที่ไหน

 A4: ตรงไปที่[ฟอรั่ม Aspose.CAD](https://forum.aspose.com/c/cad/19) สำหรับการสนับสนุนและการอภิปรายของชุมชน

### คำถามที่ 5: ฉันจะขอรับใบอนุญาตชั่วคราวสำหรับ Aspose.CAD สำหรับ .NET ได้อย่างไร

 A5: เยี่ยมเลย[ลิงค์นี้](https://purchase.aspose.com/temporary-license/)เพื่อรับใบอนุญาตชั่วคราวสำหรับความต้องการในการพัฒนาของคุณ
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
