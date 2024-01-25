---
title: การแปลง DWG เป็น PDF ตามมาตรฐาน - บทช่วยสอน Aspose.CAD
linktitle: การแปลง DWG เป็น PDF การปฏิบัติตามข้อกำหนด
second_title: Aspose.CAD .NET - รูปแบบไฟล์ CAD และ BIM
description: แปลง DWG เป็น PDF ตามมาตรฐานด้วย Aspose.CAD สำหรับ .NET ปฏิบัติตามบทช่วยสอนของเราเพื่อรับคำแนะนำทีละขั้นตอน
type: docs
weight: 13
url: /th/net/conversion-and-export/converting-dwg-to-compliance-pdf/
---
## การแนะนำ

ยินดีต้อนรับสู่บทช่วยสอนทีละขั้นตอนเกี่ยวกับการแปลงไฟล์ DWG เป็น Compliance PDF โดยใช้ Aspose.CAD สำหรับ .NET Aspose.CAD เป็น .NET API อันทรงพลังที่ช่วยให้นักพัฒนาทำงานกับรูปแบบไฟล์ CAD ได้อย่างง่ายดาย ในบทช่วยสอนนี้ เราจะแนะนำคุณตลอดขั้นตอนการแปลงไฟล์ DWG เป็น Compliance PDF พร้อมตัวอย่างและคำอธิบายโดยละเอียด

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเริ่มต้น ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

-  Aspose.CAD สำหรับ .NET: ตรวจสอบให้แน่ใจว่าคุณมีไลบรารี Aspose.CAD ที่รวมอยู่ในโปรเจ็กต์ .NET ของคุณ คุณสามารถดาวน์โหลดได้[ที่นี่](https://releases.aspose.com/cad/net/).

- สภาพแวดล้อมการพัฒนา: ติดตั้งสภาพแวดล้อมการพัฒนา .NET ที่ใช้งานได้ และตรวจสอบให้แน่ใจว่ามีการกำหนดค่าอย่างถูกต้อง

- ไฟล์ DWG ตัวอย่าง: ดาวน์โหลดไฟล์ DWG ตัวอย่างที่คุณต้องการแปลงเป็น PDF การปฏิบัติตามข้อกำหนด

## นำเข้าเนมสเปซ

ในโปรเจ็กต์ .NET ของคุณ ให้นำเข้าเนมสเปซที่จำเป็นเพื่อใช้ฟังก์ชัน Aspose.CAD

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
```

ตอนนี้ เรามาแจกแจงขั้นตอนการแปลงไฟล์ DWG เป็น Compliance PDF ออกเป็นหลายขั้นตอน

## ขั้นตอนที่ 1: โหลดไฟล์ DWG

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";

Aspose.CAD.Image cadImage = Aspose.CAD.Image.Load(sourceFilePath);
```

## ขั้นตอนที่ 2: ตั้งค่าตัวเลือกการแรสเตอร์

 สร้างอินสแตนซ์ของ`CadRasterizationOptions` และกำหนดค่าคุณสมบัติ เช่น สีพื้นหลัง ความกว้างของหน้า และความสูงของหน้า

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions
{
    BackgroundColor = Aspose.CAD.Color.White,
    PageWidth = 1600,
    PageHeight = 1600
};
```

## ขั้นตอนที่ 3: สร้างตัวเลือก PDF

 สร้างอินสแตนซ์ของ`PdfOptions` และตั้งค่าตัวเลือกการแรสเตอร์เวกเตอร์

```csharp
PdfOptions pdfOptions = new PdfOptions
{
    VectorRasterizationOptions = rasterizationOptions,
    CorePdfOptions = new PdfDocumentOptions { Compliance = PdfCompliance.PdfA1a }
};
```

## ขั้นตอนที่ 4: บันทึกเป็น PDF (ตามมาตรฐาน A1a)

บันทึกอิมเมจ CAD เป็น PDF ตามมาตรฐาน A1a

```csharp
cadImage.Save(MyDir + "PDFA1_A.pdf", pdfOptions);
```

## ขั้นตอนที่ 5: บันทึกเป็น PDF (ตามมาตรฐาน A1b)

เปลี่ยนประเภทการปฏิบัติตามข้อกำหนดเป็น A1b และบันทึกอิมเมจ CAD เป็น PDF การปฏิบัติตามข้อกำหนด

```csharp
pdfOptions.CorePdfOptions.Compliance = PdfCompliance.PdfA1b;
cadImage.Save(MyDir + "PDFA1_B.pdf", pdfOptions);
```

## บทสรุป

ยินดีด้วย! คุณได้แปลงไฟล์ DWG เป็น Compliance PDF โดยใช้ Aspose.CAD สำหรับ .NET สำเร็จแล้ว บทช่วยสอนนี้ให้คำแนะนำที่ครอบคลุมสำหรับนักพัฒนาที่ต้องการรวมความสามารถในการแปลง CAD เข้ากับแอปพลิเคชันของตน

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถแปลงรูปแบบ CAD อื่นๆ เป็น Compliance PDF โดยใช้ Aspose.CAD ได้หรือไม่

A1: ใช่ Aspose.CAD รองรับรูปแบบ CAD ที่หลากหลาย ทำให้สามารถแปลงเป็น Compliance PDF ได้

### คำถามที่ 2: Aspose.CAD เข้ากันได้กับ .NET Core หรือไม่

A2: ใช่ Aspose.CAD เข้ากันได้กับทั้ง .NET Framework และ .NET Core

### คำถามที่ 3: มีตัวเลือกสิทธิ์การใช้งานสำหรับ Aspose.CAD หรือไม่

 A3: ได้ คุณสามารถสำรวจตัวเลือกใบอนุญาตได้[ที่นี่](https://purchase.aspose.com/buy).

### คำถามที่ 4: มีการทดลองใช้ฟรีหรือไม่?

 A4: ใช่ คุณสามารถทดลองใช้ฟรีได้[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 5: ฉันจะรับการสนับสนุนสำหรับ Aspose.CAD ได้ที่ไหน

A5: เยี่ยมชม[ฟอรั่ม Aspose.CAD](https://forum.aspose.com/c/cad/19) สำหรับคำถามที่เกี่ยวข้องกับการสนับสนุน