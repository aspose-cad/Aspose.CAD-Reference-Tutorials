---
title: การเพิ่มลายน้ำให้กับแบบร่าง CAD - คู่มือ Aspose.CAD
linktitle: การเพิ่มลายน้ำให้กับแบบร่าง CAD
second_title: Aspose.CAD .NET - รูปแบบไฟล์ CAD และ BIM
description: ปรับปรุงภาพวาด CAD ของคุณด้วยลายน้ำระดับมืออาชีพโดยใช้ Aspose.CAD สำหรับ .NET ปฏิบัติตามคำแนะนำทีละขั้นตอนของเราเพื่อการออกแบบส่วนบุคคลและน่าดึงดูด
type: docs
weight: 11
url: /th/net/plt-and-watermarking/adding-watermarks-to-cad-drawings/
---
## การแนะนำ

คุณต้องการปรับปรุงแบบร่าง CAD ของคุณด้วยการเพิ่มลายน้ำแบบมืออาชีพหรือไม่? Aspose.CAD สำหรับ .NET มอบโซลูชันที่มีประสิทธิภาพในการรวมลายน้ำเข้ากับไฟล์ CAD ของคุณได้อย่างราบรื่น ในคำแนะนำทีละขั้นตอนนี้ เราจะแนะนำคุณตลอดกระบวนการเพิ่มลายน้ำโดยใช้ Aspose.CAD เพื่อให้มั่นใจว่าภาพวาดของคุณไม่เพียงแต่สื่อถึงข้อมูลที่สำคัญเท่านั้น แต่ยังมีเครื่องหมายที่เป็นเอกลักษณ์ของคุณอีกด้วย

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเข้าสู่บทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีสิ่งต่อไปนี้:
-  Aspose.CAD สำหรับ .NET: ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้งไลบรารี Aspose.CAD แล้ว คุณสามารถดาวน์โหลดได้[ที่นี่](https://releases.aspose.com/cad/net/).
- ไดเร็กทอรีเอกสารของคุณ: ตั้งค่าไดเร็กทอรีเพื่อจัดเก็บแบบร่าง CAD ของคุณ
ตอนนี้ เรามาเริ่มต้นด้วยการเพิ่มลายน้ำให้กับแบบร่าง CAD ของคุณกัน!

## นำเข้าเนมสเปซ

เริ่มต้นด้วยการนำเข้าเนมสเปซที่จำเป็นลงในโปรเจ็กต์ .NET ของคุณ:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## ขั้นตอนที่ 1: โหลดแบบร่าง CAD

```csharp
// เส้นทางไปยังไดเร็กทอรีเอกสาร
string MyDir = "Your Document Directory";
using (CadImage cadImage = (CadImage)Image.Load(MyDir + "Drawing11.dwg")) {
```

## ขั้นตอนที่ 2: เพิ่มลายน้ำเป็น MTEXT

```csharp
// เพิ่ม MTEXT ใหม่
CadMText watermark = new CadMText();
watermark.Text = "Watermark message";
watermark.InitialTextHeight = 40;
watermark.InsertionPoint = new Cad3DPoint(300, 40);
watermark.LayerName = "0";
cadImage.BlockEntities["*Model_Space"].AddEntity(watermark);
```

## ขั้นตอนที่ 3: หรือเพิ่มลายน้ำเป็นข้อความ

```csharp
// หรือเพิ่มเอนทิตีที่เรียบง่ายกว่า เช่น ข้อความ
CadText text = new CadText();
text.DefaultValue = "Watermark text";
text.TextHeight = 40;
text.FirstAlignment = new Cad3DPoint(300, 40);
text.LayerName = "0";
cadImage.BlockEntities["*Model_Space"].AddEntity(text);
```

## ขั้นตอนที่ 4: ส่งออกเป็น PDF

```csharp
// ส่งออกแบบร่าง CAD ที่มีลายน้ำเป็น PDF
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.Layouts = new[] { "Model" };
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
cadImage.Save(MyDir + "AddWatermark_out.pdf", pdfOptions);
```

ทำซ้ำขั้นตอนเหล่านี้สำหรับภาพวาดต่างๆ แล้วคุณจะมีไฟล์ CAD ลายน้ำที่ดูเป็นมืออาชีพในเวลาอันรวดเร็ว!

## บทสรุป

ยินดีด้วย! คุณได้เรียนรู้วิธีเพิ่มลายน้ำให้กับแบบร่าง CAD ของคุณโดยใช้ Aspose.CAD สำหรับ .NET เรียบร้อยแล้ว กระบวนการที่เรียบง่ายแต่ทรงพลังนี้ช่วยให้คุณปรับแต่งการออกแบบในแบบของคุณ ในขณะเดียวกันก็รักษาความสมบูรณ์ของแบบทางเทคนิคของคุณ

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถปรับแต่งลักษณะที่ปรากฏของลายน้ำได้หรือไม่

A1: ได้ คุณสามารถปรับแต่งข้อความ แบบอักษร ขนาด และตำแหน่งของลายน้ำได้ตามความต้องการของคุณ

### คำถามที่ 2: Aspose.CAD สามารถใช้งานร่วมกับไฟล์ CAD ในรูปแบบต่างๆ ได้หรือไม่

A2: Aspose.CAD รองรับไฟล์ CAD หลากหลายรูปแบบ รวมถึง DWG และ DXF เพื่อให้มั่นใจถึงความเข้ากันได้ในวงกว้าง

### คำถามที่ 3: ฉันสามารถเพิ่มลายน้ำหลายลายลงในแบบ CAD เดียวได้หรือไม่

A3: แน่นอน! คุณสามารถเพิ่มลายน้ำได้มากเท่าที่ต้องการ โดยให้ความยืดหยุ่นสำหรับกรณีการใช้งานที่แตกต่างกัน

### คำถามที่ 4: Aspose.CAD ให้ทดลองใช้ฟรีหรือไม่

A4: ได้ คุณสามารถสำรวจคุณสมบัติของ Aspose.CAD ได้ด้วยการทดลองใช้ฟรี รับมัน[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 5: ฉันจะรับการสนับสนุนสำหรับ Aspose.CAD ได้ที่ไหน

 A5: หากมีข้อสงสัยหรือความช่วยเหลือ โปรดไปที่[ฟอรั่ม Aspose.CAD](https://forum.aspose.com/c/cad/19).