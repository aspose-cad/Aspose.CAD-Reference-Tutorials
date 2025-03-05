---
title: ส่งออก DGN เป็น PDF ใน Aspose.CAD สำหรับ .NET
linktitle: ส่งออก DGN เป็น PDF
second_title: Aspose.CAD .NET - รูปแบบไฟล์ CAD และ BIM
description: เรียนรู้วิธีส่งออกไฟล์ DGN เป็น PDF ได้อย่างง่ายดายด้วย Aspose.CAD สำหรับ .NET คำแนะนำทีละขั้นตอนสำหรับการจัดการไฟล์ CAD ได้อย่างราบรื่น
type: docs
weight: 12
url: /th/net/cad-export-formats/export-dgn-to-pdf/
---
## การแนะนำ

ในโลกของการพัฒนา .NET Aspose.CAD เป็นไลบรารีที่มีประสิทธิภาพซึ่งอำนวยความสะดวกในการจัดการและแปลงไฟล์ CAD งานทั่วไปอย่างหนึ่งที่นักพัฒนามักพบคือการส่งออกไฟล์ DGN เป็นรูปแบบ PDF ในบทช่วยสอนนี้ เราจะอธิบายกระบวนการทีละขั้นตอนโดยใช้ Aspose.CAD สำหรับ .NET

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเข้าสู่บทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีสิ่งต่อไปนี้:

- ความรู้เกี่ยวกับการทำงานของ C# และ .NET framework
-  ติดตั้ง Aspose.CAD สำหรับไลบรารี .NET แล้ว คุณสามารถดาวน์โหลดได้[ที่นี่](https://releases.aspose.com/cad/net/).
- ตัวอย่างไฟล์ DGN เช่น "Nikon_D90_Camera.dgn" สำหรับบทช่วยสอนนี้

## นำเข้าเนมสเปซ

ในโปรเจ็กต์ C# ของคุณ ให้เริ่มต้นด้วยการนำเข้าเนมสเปซที่จำเป็น:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## ขั้นตอนที่ 1: โหลดไฟล์ DGN

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage cadImage = (DgnImage)Image.Load(sourceFilePath))
{
    // รหัสของคุณที่นี่...
}
```

## ขั้นตอนที่ 2: กำหนดค่าตัวเลือกการแรสเตอร์

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 600;
rasterizationOptions.PageHeight = 300;
rasterizationOptions.NoScaling = true;
rasterizationOptions.AutomaticLayoutsScaling = false;
```

## ขั้นตอนที่ 3: สร้างตัวเลือก PDF

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## ขั้นตอนที่ 4: บันทึกเป็น PDF

```csharp
cadImage.Save(MyDir + "ExportDGNToPdf_out.pdf", pdfOptions);
```

## บทสรุป

ยินดีด้วย! คุณได้ส่งออกไฟล์ DGN เป็น PDF โดยใช้ Aspose.CAD สำหรับ .NET สำเร็จแล้ว บทช่วยสอนนี้ครอบคลุมขั้นตอนสำคัญต่างๆ ตั้งแต่การโหลดไฟล์ DGN ไปจนถึงการกำหนดค่าตัวเลือกการแรสเตอร์และบันทึกเอาต์พุตเป็น PDF

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถใช้ Aspose.CAD สำหรับ .NET โดยไม่ต้องมีความรู้ CAD มาก่อนได้หรือไม่

A1: แน่นอน! Aspose.CAD ลดความซับซ้อนของงาน CAD ที่ซับซ้อน ทำให้นักพัฒนาที่มีภูมิหลังหลากหลายสามารถเข้าถึงได้

### คำถามที่ 2: ฉันจะหาตัวอย่างและเอกสารประกอบเพิ่มเติมสำหรับ Aspose.CAD ได้ที่ไหน

 A2: สำรวจ[เอกสารประกอบ](https://reference.aspose.com/cad/net/) สำหรับคำแนะนำและตัวอย่างที่ครอบคลุม

### คำถามที่ 3: Aspose.CAD มีรุ่นทดลองใช้ฟรีหรือไม่

A3: ใช่ คุณสามารถทดลองใช้ฟรีได้[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 4: ฉันจะรับใบอนุญาตชั่วคราวสำหรับ Aspose.CAD ได้อย่างไร

 A4: รับใบอนุญาตชั่วคราว[ที่นี่](https://purchase.aspose.com/temporary-license/).

### Q5: ต้องการความช่วยเหลือหรือมีคำถาม?

A5: เยี่ยมชม[ฟอรั่ม Aspose.CAD](https://forum.aspose.com/c/cad/19) เพื่อสนับสนุนชุมชน