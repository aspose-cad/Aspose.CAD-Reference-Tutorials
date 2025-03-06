---
title: ยกระดับการส่งออก CAD ด้วยตัวเลือกปากกาแบบกำหนดเองใน Aspose.CAD สำหรับ .NET
linktitle: รองรับปากกาในการส่งออก
second_title: Aspose.CAD .NET - รูปแบบไฟล์ CAD และ BIM
description: เรียนรู้วิธีปรับปรุงการส่งออกรูปภาพ CAD ของคุณโดยใช้ Aspose.CAD สำหรับ .NET ปรับแต่งตัวเลือกปากกาเพื่อภาพที่น่าทึ่งในรูปแบบ PDF, PNG, BMP และอื่นๆ
weight: 12
url: /th/net/cad-features-and-support/pen-support-in-export/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ยกระดับการส่งออก CAD ด้วยตัวเลือกปากกาแบบกำหนดเองใน Aspose.CAD สำหรับ .NET

## การแนะนำ

Aspose.CAD สำหรับ .NET มอบชุดเครื่องมืออันทรงพลังสำหรับการทำงานกับไฟล์ Computer-Aided Design (CAD) ช่วยให้นักพัฒนาจัดการและส่งออกอิมเมจ CAD ได้อย่างราบรื่น คุณสมบัติเด่นอย่างหนึ่งคือการรองรับปากกาในระหว่างการส่งออก ทำให้ผู้ใช้สามารถกำหนดการตั้งค่าเริ่มต้นและฝาปิดท้ายสำหรับปากกาได้เมื่อส่งออกภาพ CAD เป็นรูปแบบต่างๆ เช่น PDF, PNG, BMP, GIF, JPEG2000, JPEG, PSD, TIFF และ WMF

ในบทช่วยสอนนี้ เราจะเจาะลึกข้อมูลเฉพาะของการรองรับปากกาในการส่งออกโดยใช้ Aspose.CAD สำหรับ .NET เราจะแจกแจงรายละเอียดแต่ละขั้นตอนโดยให้คำอธิบายและตัวอย่างที่ชัดเจนเพื่อแนะนำคุณตลอดกระบวนการ

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเจาะลึกบทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

- ติดตั้ง Aspose.CAD สำหรับ .NET ในสภาพแวดล้อมการพัฒนาของคุณ คุณสามารถดาวน์โหลดได้จาก[หน้าปล่อย](https://releases.aspose.com/cad/net/).

- ความเข้าใจพื้นฐานเกี่ยวกับรูปแบบไฟล์ CAD โดยเฉพาะ DXF (รูปแบบการแลกเปลี่ยนรูปวาด)

- ความรู้การทำงานของภาษาการเขียนโปรแกรม C #

## นำเข้าเนมสเปซ

ในการเริ่มต้น ตรวจสอบให้แน่ใจว่าคุณนำเข้าเนมสเปซที่จำเป็นในโปรเจ็กต์ C# ของคุณ:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Drawing;
using System.Drawing.Drawing2D;
```

## ขั้นตอนที่ 1: ตั้งค่าไดเร็กทอรีเอกสารของคุณ

กำหนดไดเร็กทอรีที่มีเอกสาร CAD ของคุณ:

```csharp
string MyDir = "Your Document Directory";
```

## ขั้นตอนที่ 2: โหลดอิมเมจ CAD

โหลดอิมเมจ CAD โดยใช้ Aspose.CAD:

```csharp
string sourceFilePath = MyDir + "conic_pyramid.dxf";
CadImage cadImage = (CadImage)Image.Load(sourceFilePath);
```

## ขั้นตอนที่ 3: กำหนดค่าตัวเลือกการแรสเตอร์

สร้างตัวเลือกการแรสเตอร์และ PDF เพื่อปรับแต่งกระบวนการส่งออก:

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
PdfOptions pdfOptions = new PdfOptions();
```

## ขั้นตอนที่ 4: ปรับแต่งตัวเลือกปากกา

ตั้งค่าตัวเลือกเริ่มต้นและปิดท้ายสำหรับปากกา:

```csharp
rasterizationOptions.PenOptions = new PenOptions
{
   StartCap = LineCap.Flat,
   EndCap = LineCap.Flat
};
```

## ขั้นตอนที่ 5: ใช้ตัวเลือกการแรสเตอร์แบบเวกเตอร์

ใช้ตัวเลือกการแรสเตอร์กับตัวเลือก PDF:

```csharp
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## ขั้นตอนที่ 6: บันทึก PDF ที่ส่งออก

บันทึกภาพ CAD ด้วยตัวเลือกปากกาที่ปรับแต่งเป็นไฟล์ PDF:

```csharp
cadImage.Save(MyDir + "9LHATT-A56_generated.pdf", pdfOptions);
```

## บทสรุป

ในบทช่วยสอนนี้ เราได้สำรวจการรองรับปากกาในฟีเจอร์การส่งออกของ Aspose.CAD สำหรับ .NET ด้วยการทำตามคำแนะนำทีละขั้นตอน คุณสามารถปรับแต่งการตั้งค่าเริ่มต้นและฝาปิดท้ายสำหรับปากกาได้อย่างง่ายดาย เพิ่มความยืดหยุ่นในการส่งออกรูปภาพ CAD ของคุณ

ทดลองใช้ตัวเลือกปากกาต่างๆ ได้อย่างอิสระเพื่อให้ได้เอฟเฟ็กต์ภาพที่ต้องการในรูปภาพที่คุณส่งออก

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถใช้ตัวเลือกปากกาเหล่านี้กับรูปแบบรูปภาพอื่นนอกเหนือจาก PDF ได้หรือไม่

A1: ได้ ตัวเลือกปากกาสามารถใช้ได้กับรูปแบบภาพต่างๆ เช่น PNG, BMP, GIF, JPEG และอื่นๆ

### คำถามที่ 2: ฉันจะหาเอกสารเพิ่มเติมสำหรับ Aspose.CAD สำหรับ .NET ได้ที่ไหน

 A2: โปรดดูที่[เอกสารประกอบ](https://reference.aspose.com/cad/net/) สำหรับข้อมูลและตัวอย่างที่ครอบคลุม

### คำถามที่ 3: Aspose.CAD สำหรับ .NET มีรุ่นทดลองใช้ฟรีหรือไม่

 A3: ได้ คุณสามารถทดลองใช้ฟรีได้[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 4: ฉันจะรับใบอนุญาตชั่วคราวสำหรับ Aspose.CAD สำหรับ .NET ได้อย่างไร

 A4: เยี่ยมชม[หน้าใบอนุญาตชั่วคราว](https://purchase.aspose.com/temporary-license/) สำหรับตัวเลือกการออกใบอนุญาตชั่วคราว

### คำถามที่ 5: ฉันจะขอการสนับสนุนจากชุมชนสำหรับ Aspose.CAD สำหรับ .NET ได้ที่ไหน

 A5: มีส่วนร่วมกับชุมชนบน[ฟอรั่ม Aspose.CAD](https://forum.aspose.com/c/cad/19).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
