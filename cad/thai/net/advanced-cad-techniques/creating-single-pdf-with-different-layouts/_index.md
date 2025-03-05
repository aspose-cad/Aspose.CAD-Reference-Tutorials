---
title: การสร้าง PDF ไฟล์เดียวด้วยเลย์เอาต์ที่แตกต่างกัน - คู่มือ Aspose.CAD
linktitle: การสร้าง PDF เดียวด้วยเลย์เอาต์ที่แตกต่างกัน
second_title: Aspose.CAD .NET - รูปแบบไฟล์ CAD และ BIM
description: สร้าง PDF ไฟล์เดียวด้วยเลย์เอาต์ที่แตกต่างกันโดยใช้ Aspose.CAD สำหรับ .NET ปฏิบัติตามคำแนะนำทีละขั้นตอนของเราเพื่อการบูรณาการที่ราบรื่นและการสร้าง PDF ที่มีประสิทธิภาพ
type: docs
weight: 13
url: /th/net/advanced-cad-techniques/creating-single-pdf-with-different-layouts/
---
## การแนะนำ

คุณต้องการสร้างเอกสาร PDF ไฟล์เดียวจากแบบร่าง CAD ที่มีเลย์เอาต์ที่แตกต่างกันโดยใช้ Aspose.CAD สำหรับ .NET หรือไม่? คำแนะนำทีละขั้นตอนนี้จะแนะนำคุณตลอดกระบวนการ ช่วยให้คุณบูรณาการได้อย่างราบรื่นและการสร้าง PDF ที่มีประสิทธิภาพ Aspose.CAD สำหรับ .NET มอบคุณสมบัติอันทรงพลังในการจัดการภาพวาด CAD โดยทางโปรแกรม และในบทช่วยสอนนี้ เราจะเน้นที่การสร้าง PDF ไฟล์เดียวที่มีเค้าโครงที่แตกต่างกัน

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเข้าสู่บทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

-  Aspose.CAD สำหรับ .NET: ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง Aspose.CAD สำหรับ .NET แล้ว คุณสามารถดาวน์โหลดได้จาก[ที่นี่](https://releases.aspose.com/cad/net/).

- สภาพแวดล้อมการพัฒนา: ตั้งค่าสภาพแวดล้อมการพัฒนา .NET และมีความเข้าใจพื้นฐานเกี่ยวกับการเขียนโปรแกรม C#

## นำเข้าเนมสเปซ

ในโปรเจ็กต์ C# ของคุณ ให้รวมเนมสเปซที่จำเป็นเพื่อใช้ประโยชน์จากฟังก์ชันการทำงานของ Aspose.CAD สำหรับ .NET:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## ขั้นตอนที่ 1: โหลดอิมเมจ CAD

```csharp
// เส้นทางไปยังไดเร็กทอรีเอกสาร
string MyDir = "Your Document Directory";

using (CadImage cadImage = (CadImage)Image.Load(MyDir + "City skyway map.dwg"))
{
    // รหัสของคุณสำหรับขั้นตอนที่ 1 อยู่ที่นี่
}
```

## ขั้นตอนที่ 2: ปรับแต่งตัวเลือกการแรสเตอร์

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1000;
rasterizationOptions.PageHeight = 1000;

// ขนาดที่กำหนดเองสำหรับหลายเค้าโครง
rasterizationOptions.LayoutPageSizes.Add("ANSI C Plot", new SizeF(500, 1000));
rasterizationOptions.LayoutPageSizes.Add("8.5 x 11 Plot", new SizeF(1000, 100));
```

## ขั้นตอนที่ 3: กำหนดตัวเลือก PDF

```csharp
PdfOptions pdfOptions = new PdfOptions() { VectorRasterizationOptions = rasterizationOptions };
```

## ขั้นตอนที่ 4: บันทึกเป็น PDF

```csharp
cadImage.Save(MyDir + "singlePDF_out.pdf", pdfOptions);
```

ตอนนี้คุณได้สร้างเอกสาร PDF เดียวที่มีเค้าโครงที่แตกต่างกันโดยใช้ Aspose.CAD สำหรับ .NET เรียบร้อยแล้ว สำรวจคุณสมบัติเพิ่มเติมและปรับแต่งโค้ดได้ตามความต้องการเฉพาะของคุณ

## บทสรุป

ในบทช่วยสอนนี้ เราได้กล่าวถึงกระบวนการสร้าง PDF ไฟล์เดียวจากแบบร่าง CAD ที่มีเลย์เอาต์ที่แตกต่างกันโดยใช้ Aspose.CAD สำหรับ .NET ไลบรารีอันทรงพลังนี้ทำให้งานการจัดการ CAD ง่ายขึ้น และมอบความยืดหยุ่นสำหรับสถานการณ์ต่างๆ

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถใช้ Aspose.CAD สำหรับ .NET กับรูปแบบ CAD อื่นๆ ได้หรือไม่

ตอบ 1: ใช่ Aspose.CAD สำหรับ .NET รองรับรูปแบบ CAD หลากหลาย เช่น DWG, DXF, DGN และอื่นๆ

### คำถามที่ 2: มีการทดลองใช้ฟรีหรือไม่?

 A2: ได้ คุณสามารถทดลองใช้งานฟรีได้[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 3: ฉันจะรับการสนับสนุนสำหรับ Aspose.CAD สำหรับ .NET ได้อย่างไร

 A3: เยี่ยมชม[ฟอรั่ม Aspose.CAD](https://forum.aspose.com/c/cad/19) เพื่อสนับสนุนชุมชน

### Q4: ฉันจะหาเอกสารโดยละเอียดได้จากที่ไหน?

 A4: โปรดดูเอกสารประกอบ[ที่นี่](https://reference.aspose.com/cad/net/).

### คำถามที่ 5: ฉันสามารถซื้อใบอนุญาตสำหรับ Aspose.CAD สำหรับ .NET ได้หรือไม่

 A5: ได้ คุณสามารถซื้อใบอนุญาตได้[ที่นี่](https://purchase.aspose.com/buy).