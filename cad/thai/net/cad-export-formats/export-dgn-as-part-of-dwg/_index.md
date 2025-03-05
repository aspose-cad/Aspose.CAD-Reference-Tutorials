---
title: ส่งออก DGN โดยเป็นส่วนหนึ่งของ DWG ใน Aspose.CAD สำหรับ .NET
linktitle: ส่งออก DGN โดยเป็นส่วนหนึ่งของ DWG
second_title: Aspose.CAD .NET - รูปแบบไฟล์ CAD และ BIM
description: เรียนรู้วิธีส่งออก DGN โดยเป็นส่วนหนึ่งของ DWG ใน Aspose.CAD สำหรับ .NET ปฏิบัติตามคำแนะนำทีละขั้นตอนของเราเพื่อการบูรณาการที่ราบรื่น
type: docs
weight: 11
url: /th/net/cad-export-formats/export-dgn-as-part-of-dwg/
---
## การแนะนำ

ในโลกของการพัฒนา .NET นั้น Aspose.CAD มีความโดดเด่นในฐานะไลบรารีที่ทรงพลังสำหรับการทำงานกับไฟล์ Computer-Aided Design (CAD) บทช่วยสอนนี้จะแนะนำคุณตลอดขั้นตอนการส่งออกไฟล์ DGN (การออกแบบ) โดยเป็นส่วนหนึ่งของไฟล์ DWG (รูปวาด) โดยใช้ Aspose.CAD สำหรับ .NET ไม่ว่าคุณจะเป็นนักพัฒนาที่มีประสบการณ์หรือเพิ่งเริ่มต้น คำแนะนำทีละขั้นตอนนี้จะช่วยให้คุณควบคุมความสามารถของ Aspose.CAD เพื่อให้บรรลุภารกิจเฉพาะนี้ได้อย่างมีประสิทธิภาพ

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเข้าสู่บทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

-  Aspose.CAD สำหรับ .NET: ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้งไลบรารี Aspose.CAD สำหรับ .NET แล้ว คุณสามารถดาวน์โหลดได้[ที่นี่](https://releases.aspose.com/cad/net/).

- สภาพแวดล้อมการพัฒนา: ตั้งค่าสภาพแวดล้อมการพัฒนา .NET ที่คุณต้องการ เช่น Visual Studio

- ความรู้พื้นฐานของ C#: ทำความคุ้นเคยกับภาษาการเขียนโปรแกรม C#

## นำเข้าเนมสเปซ

ในโปรเจ็กต์ C# ของคุณ ให้รวมเนมสเปซที่จำเป็นเพื่อเข้าถึงฟังก์ชัน Aspose.CAD เพิ่มคำสั่งการใช้ต่อไปนี้ที่จุดเริ่มต้นของไฟล์โค้ดของคุณ:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

ตอนนี้ เรามาแบ่งโค้ดที่ให้มาออกเป็นหลายขั้นตอน:

## ขั้นตอนที่ 1: กำหนดเส้นทางไฟล์

```csharp
//เส้นทางไฟล์อินพุตและเอาต์พุต
string fileName = "BlockRefDgn.dwg";
string outPath = fileName + ".pdf";
```

## ขั้นตอนที่ 2: สร้างอินสแตนซ์ PdfOptions

```csharp
// สร้างอินสแตนซ์ของคลาส PdfOptions สำหรับส่งออก DWG เป็น PDF
PdfOptions exportOptions = new PdfOptions();
```

## ขั้นตอนที่ 3: โหลดไฟล์ DWG

```csharp
// โหลดไฟล์ DWG ที่มีอยู่เป็นรูปภาพและแปลงเป็นประเภท CadImage
using (CadImage cadImage = (CadImage)Image.Load(fileName))
```

## ขั้นตอนที่ 4: วนซ้ำผ่านเอนทิตี

```csharp
// วนซ้ำแต่ละเอนทิตีภายในไฟล์ DWG
foreach (CadBaseEntity baseEntity in cadImage.Entities)
```

## ขั้นตอนที่ 5: ตรวจสอบประเภทเอนทิตี

```csharp
// ตรวจสอบว่าเอนทิตีเป็นคำจำกัดความของรูปภาพหรือไม่
if (baseEntity.TypeName == CadEntityTypeName.DGNUNDERLAY)
```

## ขั้นตอนที่ 6: รับเส้นทาง Underlay

```csharp
// หากเป็นคำจำกัดความของรูปภาพ ให้รับการอ้างอิงภายนอกไปยังออบเจ็กต์
CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
Console.WriteLine(dgnFile.UnderlayPath);
```

## ขั้นตอนที่ 7: กำหนดตัวเลือกการแรสเตอร์

```csharp
// กำหนดการตั้งค่าสำหรับวัตถุ CadRasterizationOptions
exportOptions.VectorRasterizationOptions = new CadRasterizationOptions()
{
    PageWidth = 1600,
    PageHeight = 1600,
    Layouts = new string[] { "Model" },
    AutomaticLayoutsScaling = false,
    NoScaling = true,
    BackgroundColor = Color.Black,
    DrawType = CadDrawTypeMode.UseObjectColor
};
```

## ขั้นตอนที่ 8: ส่งออก DWG เป็น PDF

```csharp
// ส่งออก DWG เป็น PDF โดยเรียกวิธีการบันทึก
cadImage.Save(outPath, exportOptions);
```

## บทสรุป

ยินดีด้วย! คุณทำตามขั้นตอนการส่งออกไฟล์ DGN โดยเป็นส่วนหนึ่งของไฟล์ DWG โดยใช้ Aspose.CAD สำหรับ .NET สำเร็จแล้ว บทช่วยสอนนี้ได้จัดเตรียมขั้นตอนพื้นฐานและข้อมูลโค้ดเพื่อให้คุณทำงานเฉพาะด้านนี้ได้อย่างราบรื่น

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถใช้ Aspose.CAD สำหรับ .NET ในโครงการเชิงพาณิชย์ของฉันได้หรือไม่
 A1: ใช่คุณทำได้ เยี่ยม[ที่นี่](https://purchase.aspose.com/buy) เพื่อสำรวจตัวเลือกการออกใบอนุญาต

### คำถามที่ 2: มีข้อจำกัดเกี่ยวกับขนาดของไฟล์ DWG ที่ฉันสามารถประมวลผลได้หรือไม่
ตอบ 2: Aspose.CAD รองรับการจัดการไฟล์ DWG ขนาดใหญ่ แต่อาจมีข้อจำกัดด้านฮาร์ดแวร์

### คำถามที่ 3: มีเวอร์ชันทดลองใช้งานหรือไม่
A3: ใช่ คุณสามารถทดลองใช้ฟรีได้[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 4: ฉันจะรับใบอนุญาตชั่วคราวได้อย่างไร
 A4: สามารถรับใบอนุญาตชั่วคราวได้[ที่นี่](https://purchase.aspose.com/temporary-license/).

### คำถามที่ 5: ฉันจะขอความช่วยเหลือได้ที่ไหนหากฉันประสบปัญหา
 A5: คุณสามารถเยี่ยมชมฟอรัม Aspose.CAD ได้[ที่นี่](https://forum.aspose.com/c/cad/19) สำหรับการสนับสนุน