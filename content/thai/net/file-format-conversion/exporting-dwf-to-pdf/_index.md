---
title: การส่งออก DWF เป็น PDF - คู่มือ Aspose.CAD
linktitle: ส่งออก DWF เป็น PDF
second_title: Aspose.CAD .NET - รูปแบบไฟล์ CAD และ BIM
description: สำรวจคำแนะนำที่ราบรื่นเกี่ยวกับการส่งออก DWF เป็น PDF โดยใช้ Aspose.CAD สำหรับ .NET ปรับปรุงความสามารถในการจัดการไฟล์ CAD ของคุณได้อย่างง่ายดาย
type: docs
weight: 10
url: /th/net/file-format-conversion/exporting-dwf-to-pdf/
---
## การแนะนำ

ในโลกของการพัฒนา .NET นั้น Aspose.CAD มีความโดดเด่นในฐานะไลบรารีที่ทรงพลังสำหรับการจัดการไฟล์ Computer-Aided Design (CAD) ในบทช่วยสอนนี้ เราจะเน้นไปที่งานเฉพาะ: การส่งออกไฟล์ DWF (Design Web Format) เป็น PDF โดยใช้ Aspose.CAD สำหรับ .NET ไม่ว่าคุณจะเป็นนักพัฒนาที่มีประสบการณ์หรือเพิ่งเริ่มต้น ให้ปฏิบัติตามเพื่อผสานรวมฟังก์ชันการทำงานนี้เข้ากับแอปพลิเคชันของคุณได้อย่างราบรื่น

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเข้าสู่บทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

-  Aspose.CAD สำหรับ .NET: ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง Aspose.CAD สำหรับ .NET แล้ว คุณสามารถดาวน์โหลดได้จาก[ที่นี่](https://releases.aspose.com/cad/net/).

- สภาพแวดล้อมการพัฒนา: ตั้งค่าสภาพแวดล้อมการพัฒนา .NET ที่ใช้งานได้ รวมถึง Visual Studio หรือ IDE ที่ต้องการอื่นๆ

## นำเข้าเนมสเปซ

เริ่มต้นด้วยการนำเข้าเนมสเปซที่จำเป็นลงในโปรเจ็กต์ของคุณ ขั้นตอนนี้มีความสำคัญอย่างยิ่งในการเข้าถึงฟังก์ชันการทำงานที่ Aspose.CAD มอบให้

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
```

## ขั้นตอนที่ 1: โหลดไฟล์ DWF

เริ่มต้นด้วยการโหลดไฟล์ DWF ที่คุณต้องการส่งออกเป็น PDF ปรับเส้นทางไฟล์ให้เหมาะสม

```csharp
string MyDir = "Your Document Directory";
string fileName = MyDir + "18-12-11 9644 - site.dwf";

using (Image image = Image.Load(fileName))
{
    // รหัสของคุณที่นี่...
}
```

## ขั้นตอนที่ 2: กำหนดค่าตัวเลือกการแรสเตอร์

ตั้งค่าตัวเลือกการแรสเตอร์สำหรับ DWF เพื่อให้แน่ใจว่าได้ผลลัพธ์ที่ต้องการ ในตัวอย่างนี้ เรากำหนดความสูงและความกว้างของหน้า

```csharp
CadRasterizationOptions dwfRasterizationOptions = new CadRasterizationOptions();
dwfRasterizationOptions.PageHeight = 500;
dwfRasterizationOptions.PageWidth = 500;
```

## ขั้นตอนที่ 3: กำหนดตัวเลือก PDF

สร้างตัวเลือก PDF และเชื่อมโยงกับตัวเลือกการแรสเตอร์ที่กำหนดค่าไว้ก่อนหน้านี้

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = dwfRasterizationOptions;
```

## ขั้นตอนที่ 4: ส่งออกเป็น PDF

ดำเนินการกระบวนการส่งออก โดยระบุเส้นทางเอาต์พุตสำหรับไฟล์ PDF ที่ได้

```csharp
string outPath = MyDir + "18-12-11 9644 - site.pdf";
image.Save(outPath, pdfOptions);
```

## ขั้นตอนที่ 5: ตรวจสอบการส่งออก

รับประกันการส่งออกภาพ 3 มิติเป็น PDF ได้สำเร็จ แสดงข้อความยืนยันพร้อมเส้นทางไฟล์ที่บันทึกไว้

```csharp
Console.WriteLine("\n3D images exported successfully to PDF.\nFile saved at " + MyDir);
```

ตอนนี้คุณได้ปรับใช้ฟังก์ชันการส่งออก DWF เป็น PDF ในแอปพลิเคชัน .NET ของคุณโดยใช้ Aspose.CAD เรียบร้อยแล้ว

## บทสรุป

ในบทช่วยสอนนี้ เราได้สำรวจกระบวนการส่งออกไฟล์ DWF เป็น PDF โดยใช้ Aspose.CAD สำหรับ .NET เมื่อทำตามขั้นตอนเหล่านี้ คุณจะสามารถรวมฟังก์ชันการทำงานนี้เข้ากับโปรเจ็กต์ของคุณได้อย่างราบรื่น ช่วยเพิ่มความสามารถในการจัดการไฟล์ CAD ของคุณ

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถใช้ Aspose.CAD สำหรับ .NET กับไฟล์ CAD รูปแบบอื่นได้หรือไม่

A1: ใช่ Aspose.CAD รองรับไฟล์ CAD หลากหลายรูปแบบ รวมถึง DWG, DXF, DWF และอื่นๆ ตรวจสอบเอกสารเพื่อดูรายการที่ครอบคลุม

### คำถามที่ 2: ฉันจะรับการสนับสนุนเพิ่มเติมสำหรับ Aspose.CAD ได้ที่ไหน

 A2: สำหรับการสนับสนุนเพิ่มเติม โปรดไปที่[ฟอรั่ม Aspose.CAD](https://forum.aspose.com/c/cad/19) ที่ซึ่งคุณสามารถถามคำถามและโต้ตอบกับชุมชนได้

### คำถามที่ 3: Aspose.CAD มีรุ่นทดลองใช้ฟรีหรือไม่

 A3: ได้ คุณสามารถสำรวจ Aspose.CAD เวอร์ชันทดลองใช้ฟรีได้จาก[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 4: ฉันจะขอรับใบอนุญาตชั่วคราวสำหรับ Aspose.CAD ได้อย่างไร

 A4: คุณสามารถขอรับใบอนุญาตชั่วคราวได้จาก[ลิงค์นี้](https://purchase.aspose.com/temporary-license/).

### คำถามที่ 5: ฉันจะซื้อ Aspose.CAD เวอร์ชันเต็มสำหรับ .NET ได้ที่ไหน

 A5: คุณสามารถซื้อ Aspose.CAD สำหรับ .NET เวอร์ชันเต็มได้จาก[ที่นี่](https://purchase.aspose.com/buy).