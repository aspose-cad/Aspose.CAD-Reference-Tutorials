---
title: การส่งออก DWG เป็น PDF หรือรูปภาพแรสเตอร์ - คู่มือ Aspose.CAD
linktitle: ส่งออก DWG เป็น PDF หรือรูปภาพแรสเตอร์
second_title: Aspose.CAD .NET - รูปแบบไฟล์ CAD และ BIM
description: สำรวจคำแนะนำที่ครอบคลุมเกี่ยวกับการส่งออก DWG เป็น PDF หรือรูปภาพแรสเตอร์โดยใช้ Aspose.CAD สำหรับ .NET เรียนรู้ขั้นตอน ข้อกำหนดเบื้องต้น และลงมือปฏิบัติจริงด้วยไลบรารีที่มีประสิทธิภาพนี้
weight: 11
url: /th/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# การส่งออก DWG เป็น PDF หรือรูปภาพแรสเตอร์ - คู่มือ Aspose.CAD

## การแนะนำ

คุณต้องการแปลงไฟล์ DWG เป็น PDF หรือรูปภาพแรสเตอร์ในแอปพลิเคชัน .NET ของคุณได้อย่างราบรื่นหรือไม่? ไม่ต้องมองอีกต่อไป! คำแนะนำทีละขั้นตอนนี้จะแนะนำคุณตลอดกระบวนการโดยใช้ไลบรารี Aspose.CAD สำหรับ .NET อันทรงพลัง ไม่ว่าคุณจะเป็นนักพัฒนาที่มีประสบการณ์หรือเพิ่งเริ่มต้น บทช่วยสอนนี้เหมาะสำหรับทุกระดับทักษะ

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเจาะลึกบทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีสิ่งต่อไปนี้:

- ความเข้าใจพื้นฐานเกี่ยวกับการเขียนโปรแกรม .NET
-  ติดตั้ง Aspose.CAD สำหรับไลบรารี .NET แล้ว ถ้าไม่เช่นนั้นให้ดาวน์โหลด[ที่นี่](https://releases.aspose.com/cad/net/).
- สภาพแวดล้อมการพัฒนาแบบรวม (IDE) ที่คุณชื่นชอบซึ่งตั้งค่าไว้สำหรับการพัฒนา .NET

## นำเข้าเนมสเปซ

มาเริ่มกันด้วยการนำเข้าเนมสเปซที่จำเป็นในโปรเจ็กต์ .NET ของคุณ สิ่งนี้ทำให้แน่ใจได้ว่าคุณจะสามารถเข้าถึงฟังก์ชัน Aspose.CAD ในโค้ดของคุณได้

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
```

## ขั้นตอนที่ 1: โหลดไฟล์ DWG

เริ่มต้นด้วยการโหลดไฟล์ DWG ที่คุณต้องการแปลง แทนที่ "Your Document Directory" ด้วยเส้นทางไปยังไฟล์ DWG ของคุณ

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // รหัสของคุณสำหรับการโหลด DWG อยู่ที่นี่
}
```

## ขั้นตอนที่ 2: ตั้งค่าการส่งออก PDF

ตอนนี้ เรามากำหนดการตั้งค่าการส่งออก PDF กัน ตัวอย่างนี้สาธิตวิธีการตั้งค่าโครงร่างและจัดการการแปลงหน่วย

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new string[] { "Model" };

// ตรวจสอบและกำหนดระบบหน่วย
bool currentUnitIsMetric = false;
double currentUnitCoefficient = 1.0;
DefineUnitSystem(cadImage.UnitType, out currentUnitIsMetric, out currentUnitCoefficient);

// รหัสของคุณสำหรับการตั้งค่าการส่งออก PDF อยู่ที่นี่
```

## ขั้นตอนที่ 3: ส่งออกเป็น PDF

ดำเนินการส่งออกเป็น PDF โดยใช้การตั้งค่าที่กำหนดไว้

```csharp
PdfOptions pdfOptions = new PdfOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath, pdfOptions);
```

## ขั้นตอนที่ 4: ส่งออกเป็นรูปภาพแรสเตอร์

ขยายฟังก์ชันการทำงานเพื่อส่งออกไปยังรูปภาพแรสเตอร์ เช่น PNG

```csharp
// ขนาด A4 ที่ 300 DPI - 2480 x 3508
rasterizationOptions.PageHeight = 3508;
rasterizationOptions.PageWidth = 2480;

PngOptions pngOptions = new PngOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath.Replace("pdf", "png"), pngOptions);
```

## บทสรุป

ยินดีด้วย! คุณได้เรียนรู้วิธีใช้ Aspose.CAD สำหรับ .NET เพื่อส่งออกไฟล์ DWG เป็นทั้ง PDF และรูปภาพแรสเตอร์เรียบร้อยแล้ว ไลบรารีอันทรงพลังนี้ปรับปรุงกระบวนการให้มีประสิทธิภาพและเป็นมิตรต่อนักพัฒนา

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถใช้ Aspose.CAD สำหรับ .NET ในโครงการเชิงพาณิชย์ของฉันได้หรือไม่

 A1: ใช่คุณทำได้ เยี่ยม[buy.aspose.com/buy](https://purchase.aspose.com/buy) สำหรับรายละเอียดใบอนุญาต

### คำถามที่ 2: มีการทดลองใช้ฟรีหรือไม่?

 A2: แน่นอน! ทดลองใช้ฟรี[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 3: ฉันจะรับการสนับสนุนสำหรับ Aspose.CAD สำหรับ .NET ได้อย่างไร

 A3: ตรงไปที่[ฟอรั่ม Aspose.CAD](https://forum.aspose.com/c/cad/19) เพื่อสนับสนุนชุมชน

### คำถามที่ 4: ฉันสามารถขอรับใบอนุญาตชั่วคราวเพื่อการทดสอบได้หรือไม่

 A4: ได้ คุณสามารถขอรับใบอนุญาตชั่วคราวได้[ที่นี่](https://purchase.aspose.com/temporary-license/).

### Q5: ฉันจะหาเอกสารโดยละเอียดได้ที่ไหน?

 A5: เอกสารมีอยู่ที่[Aspose.CAD](https://reference.aspose.com/cad/net/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
