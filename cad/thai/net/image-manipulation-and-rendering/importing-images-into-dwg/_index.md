---
title: การนำเข้ารูปภาพไปยังไฟล์ DWG ด้วย C# - Aspose.CAD Guide
linktitle: การนำเข้ารูปภาพไปยังไฟล์ DWG ด้วย C#
second_title: Aspose.CAD .NET - รูปแบบไฟล์ CAD และ BIM
description: เรียนรู้วิธีนำเข้ารูปภาพลงในไฟล์ DWG โดยใช้ C# กับ Aspose.CAD สำหรับ .NET ปฏิบัติตามคำแนะนำทีละขั้นตอนของเราเพื่อการบูรณาการที่ราบรื่น
weight: 11
url: /th/net/image-manipulation-and-rendering/importing-images-into-dwg/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# การนำเข้ารูปภาพไปยังไฟล์ DWG ด้วย C# - Aspose.CAD Guide

## การแนะนำ

ในขอบเขตของการออกแบบโดยใช้คอมพิวเตอร์ช่วย (CAD) การรวมรูปภาพลงในไฟล์ DWG ถือเป็นงานทั่วไปและสำคัญ Aspose.CAD สำหรับ .NET มอบชุดเครื่องมืออันทรงพลังเพื่อปรับปรุงกระบวนการนี้ ทำให้นักพัฒนา C# สามารถเข้าถึงได้ ในบทช่วยสอนนี้ เราจะสำรวจวิธีการนำเข้ารูปภาพลงในไฟล์ DWG ทีละขั้นตอน

## ข้อกำหนดเบื้องต้น

ก่อนที่จะศึกษาคู่มือนี้ ตรวจสอบให้แน่ใจว่าคุณมีสิ่งต่อไปนี้:

- ความรู้พื้นฐานเกี่ยวกับการเขียนโปรแกรม C#
-  ติดตั้ง Aspose.CAD สำหรับ .NET แล้ว คุณสามารถดาวน์โหลดได้[ที่นี่](https://releases.aspose.com/cad/net/).
- สภาพแวดล้อมการพัฒนาที่จัดตั้งขึ้น

## นำเข้าเนมสเปซ

ตรวจสอบให้แน่ใจว่าได้รวมเนมสเปซที่จำเป็นในโครงการ C# ของคุณ:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## ขั้นตอนที่ 1: ตั้งค่าไดเร็กทอรีเอกสารของคุณ

```csharp
string MyDir = "Your Document Directory";
```

## ขั้นตอนที่ 2: โหลดไฟล์ DWG

```csharp
string dwgPathToFile = MyDir + "Drawing11.dwg";
CadImage cadImage1 = (CadImage)Image.Load(dwgPathToFile);
```

## ขั้นตอนที่ 3: กำหนดคุณสมบัติของรูปภาพ

```csharp
CadRasterImageDef cadRasterImageDef = new CadRasterImageDef("road-sign-custom.png", 640, 562);
cadRasterImageDef.ObjectHandle = "A3B4";
```

## ขั้นตอนที่ 4: ตั้งค่าจุดแทรกและเวกเตอร์

```csharp
Cad3DPoint insertionPoint = new Cad3DPoint(26.77, 22.35);
Cad3DPoint uVector = new Cad3DPoint(0.0061565450840500831, 0);
Cad3DPoint vVector = new Cad3DPoint(0, 0.0061565450840500822);
```

## ขั้นตอนที่ 5: สร้างและกำหนดค่าภาพแรสเตอร์

```csharp
CadRasterImage cadRasterImage = new CadRasterImage(cadRasterImageDef, insertionPoint, uVector, vVector);
cadRasterImage.ImageDefReference = "A3B4";
cadRasterImage.DisplayFlags = 7;
cadRasterImage.ClippingState = 0;
cadRasterImage.ClipBoundaryVertexList.Add(new Cad2DPoint(-0.5, 0.5));
cadRasterImage.ClipBoundaryVertexList.Add(new Cad2DPoint(639.5, 561.5));
```

## ขั้นตอนที่ 6: เพิ่มรูปภาพลงในไฟล์ DWG

```csharp
CadImage cadImage = (CadImage)cadImage1;
cadImage.BlockEntities["*Model_Space"].AddEntity(cadRasterImage);

List<CadBaseObject> list = new List<CadBaseObject>(cadImage.Objects);
list.Add(cadRasterImageDef);
cadImage.Objects = list.ToArray();
```

## ขั้นตอนที่ 7: บันทึกเป็น PDF

```csharp
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.VectorRasterizationOptions = cadRasterizationOptions;
cadRasterizationOptions.DrawType = CadDrawTypeMode.UseObjectColor;

cadRasterizationOptions.PageHeight = 1600;
cadRasterizationOptions.PageWidth = 1600;
cadRasterizationOptions.Layouts = new string[] { "Model" };
cadImage1.Save(MyDir + "export2.pdf", pdfOptions);
```

## บทสรุป

การรวมรูปภาพลงในไฟล์ DWG โดยใช้ C# และ Aspose.CAD สำหรับ .NET เป็นกระบวนการที่ราบรื่น ช่วยให้นักพัฒนาปรับปรุงโครงการ CAD ของตนด้วยองค์ประกอบภาพได้อย่างง่ายดาย

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถใช้ Aspose.CAD สำหรับ .NET กับภาษาการเขียนโปรแกรมอื่นได้หรือไม่

ตอบ 1: Aspose.CAD ได้รับการออกแบบมาเพื่อ .NET เป็นหลัก แต่ Aspose มีไลบรารีสำหรับภาษาการเขียนโปรแกรมต่างๆ

### คำถามที่ 2: Aspose.CAD สำหรับ .NET มีให้ทดลองใช้ฟรีหรือไม่

 A2: ได้ คุณสามารถทดลองใช้งานฟรีได้[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 3: ฉันจะหาเอกสารโดยละเอียดสำหรับ Aspose.CAD ได้ที่ไหน

 A3: มีเอกสารประกอบให้[ที่นี่](https://reference.aspose.com/cad/net/).

### คำถามที่ 4: ฉันจะขอรับใบอนุญาตชั่วคราวสำหรับ Aspose.CAD สำหรับ .NET ได้อย่างไร

 A4: เยี่ยมเลย[ลิงค์นี้](https://purchase.aspose.com/temporary-license/) เพื่อรับใบอนุญาตชั่วคราว

### คำถามที่ 5: มีฟอรัมชุมชนสำหรับการสนับสนุน Aspose.CAD หรือไม่

 A5: ได้ คุณสามารถขอการสนับสนุนและมีส่วนร่วมกับชุมชนได้[ที่นี่](https://forum.aspose.com/c/cad/19).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
