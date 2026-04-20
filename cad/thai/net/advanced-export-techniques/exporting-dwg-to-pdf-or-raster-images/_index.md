---
date: 2026-03-16
description: เรียนรู้วิธีแปลงไฟล์ DWG เป็น PDF หรือภาพเรสเตอร์ด้วย Aspose.CAD สำหรับ
  .NET บทแนะนำขั้นตอนต่อขั้นตอนการแปลง CAD เป็น PDF นี้ครอบคลุมการส่งออก DWG ไปยังรูปแบบภาพเช่น
  PNG และแสดงวิธีการส่งออก DWG ไปยังไฟล์ภาพอย่างมีประสิทธิภาพ
linktitle: Exporting DWG to PDF or Raster Images
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: วิธีแปลง DWG เป็น PDF และภาพเรสเตอร์โดยใช้ Aspose.CAD สำหรับ .NET
url: /th/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/
weight: 11
---

ผู้เขียน:".

Proceed.

Now produce final content.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# การส่งออก DWG เป็น PDF หรือภาพ Raster - คู่มือ Aspose.CAD

## บทนำ

หากคุณต้องการ **แปลง DWG เป็น PDF** (หรือเป็นรูปแบบ raster เช่น PNG) โดยตรงจากแอปพลิเคชัน .NET คุณมาถูกที่แล้ว ในบทแนะนำนี้เราจะพาคุณผ่านขั้นตอนที่จำเป็นในการใช้ Aspose.CAD for .NET เพื่อทำการแปลง อธิบายว่าทำไมไลบรารีนี้เป็นตัวเลือกที่ดี และแสดงวิธีจัดการทั้งการส่งออกเป็น PDF และภาพด้วยเพียงไม่กี่บรรทัดของโค้ด

## คำตอบสั้น
- **ไลบรารีที่จัดการการแปลง DWG คืออะไร?** Aspose.CAD for .NET  
- **ฉันสามารถส่งออก DWG เป็น PNG ได้เช่นเดียวกับ PDF หรือไม่?** ได้ – ตัวเลือกการ rasterization เดียวกันทำงานสำหรับทั้งสองรูปแบบ  
- **ต้องใช้ไลเซนส์สำหรับการพัฒนาหรือไม่?** เวอร์ชันทดลองฟรีใช้ได้สำหรับการทดสอบ; ต้องมีไลเซนส์เชิงพาณิชย์สำหรับการใช้งานจริง  
- **รองรับเวอร์ชัน .NET ใดบ้าง?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+  
- **การแปลงหน่วยทำโดยอัตโนมัติหรือไม่?** คุณสามารถกำหนดระบบหน่วยเอง (เมตริกหรืออิมพีเรียล) ตามที่แสดงในโค้ดได้  

## “แปลง DWG เป็น PDF” คืออะไร?
การแปลง DWG เป็น PDF หมายถึงการนำแบบ CAD (DWG) มารันเดอร์เป็นเอกสารพกพาแบบอ่าน‑เท่านั้น (PDF) ซึ่งเป็นประโยชน์สำหรับการแชร์แบบออกแบบกับผู้มีส่วนได้ส่วนเสียที่ไม่มีซอฟต์แวร์ CAD, การสร้างเอกสารที่พิมพ์ได้, หรือการเก็บรักษาแบบในรูปแบบที่ทุกคนสามารถอ่านได้

## ทำไมต้องใช้ Aspose.CAD สำหรับการแปลงนี้?
- **ไม่มีการพึ่งพาไลบรารีภายนอก** – ไลบรารีทำงานทั้งหมดในโค้ดที่จัดการโดย .NET  
- **ความแม่นยำสูง** – รักษาชั้น, ความหนาของเส้น, และข้อมูลการจัดวางไว้ครบถ้วน  
- **ตัวเลือก raster ในตัว** – สามารถส่งออกเป็น PNG, JPEG, BMP ฯลฯ ด้วยการกำหนดอ็อบเจกต์การตั้งค่าเดียว  
- **ข้ามแพลตฟอร์ม** – ทำงานบน Windows, Linux, และ macOS ด้วย .NET Core  

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะลงลึกในบทแนะนำ โปรดตรวจสอบว่าคุณมีสิ่งต่อไปนี้พร้อมใช้งาน:

- ความเข้าใจพื้นฐานเกี่ยวกับการเขียนโปรแกรม .NET  
- ไลบรารี Aspose.CAD for .NET ติดตั้งแล้ว หากยังไม่มี ให้ดาวน์โหลดได้จาก [ที่นี่](https://releases.aspose.com/cad/net/)  
- IDE ที่คุณชื่นชอบสำหรับการพัฒนา .NET ตั้งค่าเรียบร้อยแล้ว  

## นำเข้า Namespaces

เริ่มต้นโดยการนำเข้า namespaces ที่จำเป็นในโปรเจกต์ .NET ของคุณ เพื่อให้เข้าถึงฟังก์ชันของ Aspose.CAD ได้

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

โหลดไฟล์ DWG ที่ต้องการแปลง แทนที่ `"Your Document Directory"` ด้วยพาธที่ชี้ไปยังไฟล์ DWG ของคุณ

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Your code for loading DWG goes here
}
```

## ขั้นตอนที่ 2: ตั้งค่า PDF Export (วิธีส่งออก DWG เป็น PDF)

กำหนดค่าการส่งออกเป็น PDF ตัวอย่างนี้แสดงวิธีตั้งค่า layout และจัดการการแปลงหน่วย

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new string[] { "Model" };

// Check and define the unit system
bool currentUnitIsMetric = false;
double currentUnitCoefficient = 1.0;
DefineUnitSystem(cadImage.UnitType, out currentUnitIsMetric, out currentUnitCoefficient);

// Your code for setting up PDF export goes here
```

## ขั้นตอนที่ 3: ส่งออกเป็น PDF

เรียกใช้การส่งออกเป็น PDF ด้วยการตั้งค่าที่กำหนดไว้

```csharp
PdfOptions pdfOptions = new PdfOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath, pdfOptions);
```

## ขั้นตอนที่ 4: ส่งออกเป็นภาพ Raster (export dwg to image)

ขยายฟังก์ชันเพื่อส่งออกเป็นภาพ raster เช่น PNG

```csharp
// A4 size at 300 DPI - 2480 x 3508
rasterizationOptions.PageHeight = 3508;
rasterizationOptions.PageWidth = 2480;

PngOptions pngOptions = new PngOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath.Replace("pdf", "png"), pngOptions);
```

## ปัญหาที่พบบ่อยและวิธีแก้ไข

| ปัญหา | สาเหตุ | วิธีแก้ไข |
|-------|--------|-----------|
| **หน้าเปล่าใน PDF** | ไม่ได้ระบุ layout อย่างถูกต้อง | ตรวจสอบให้ `rasterizationOptions.Layouts` มีชื่อ layout ที่ถูกต้อง (เช่น `"Model"`) |
| **ขนาดไม่ตรง** | ค่า DPI หรือขนาดหน้าไม่ตรงกัน | ปรับค่า `PageHeight`, `PageWidth` และ DPI ใน `CadRasterizationOptions` |
| **หน่วยแสดงผลผิด** | ไม่ได้กำหนดการแปลงหน่วย | ใช้ `DefineUnitSystem` เพื่อกำหนด `currentUnitIsMetric` และ `currentUnitCoefficient` ตาม `cadImage.UnitType` |
| **ข้อยกเว้นไลเซนส์** | เวอร์ชันทดลองมีข้อจำกัด | ใส่ไลเซนส์ชั่วคราวหรือถาวรก่อนเรียก `Image.Load` |

## คำถามที่พบบ่อย

### Q1: ฉันสามารถใช้ Aspose.CAD for .NET ในโครงการเชิงพาณิชย์ของฉันได้หรือไม่?
A1: ได้ คุณสามารถดูรายละเอียดการซื้อไลเซนส์ได้ที่ [purchase.aspose.com/buy](https://purchase.aspose.com/buy)

### Q2: มีเวอร์ชันทดลองฟรีหรือไม่?
A2: มีแน่นอน! ดาวน์โหลดเวอร์ชันทดลองฟรีได้จาก [ที่นี่](https://releases.aspose.com/)

### Q3: ฉันจะขอรับการสนับสนุนสำหรับ Aspose.CAD for .NET ได้อย่างไร?
A3: ไปที่ [ฟอรั่ม Aspose.CAD](https://forum.aspose.com/c/cad/19) เพื่อรับการสนับสนุนจากชุมชน

### Q4: ฉันสามารถขอไลเซนส์ชั่วคราวสำหรับการทดสอบได้หรือไม่?
A4: ได้ คุณสามารถรับไลเซนส์ชั่วคราวได้จาก [ที่นี่](https://purchase.aspose.com/temporary-license/)

### Q5: ฉันจะหาเอกสารรายละเอียดได้จากที่ไหน?
A5: เอกสารพร้อมใช้งานที่ [Aspose.CAD](https://reference.aspose.com/cad/net/)

### Q6: ฉันจะ **บันทึก CAD เป็น PNG** ด้วยคุณภาพสูงอย่างไร?
A6: ตั้งค่า `PageHeight` และ `PageWidth` ให้เป็นขนาดพิกเซลที่ต้องการ และเลือก DPI ที่ 300 หรือสูงกว่าใน `CadRasterizationOptions`

### Q7: วิธีที่ดีที่สุดในการ **แปลง dwg** เมื่อไฟล์ต้นทางมีหลาย layout คืออะไร?
A7: เติมค่า `rasterizationOptions.Layouts` ด้วยชื่อ layout ทั้งหมดที่ต้องการส่งออก แล้ววนลูปแต่ละ layout เพื่อเรียก `Save` สำหรับแต่ละรูปแบบผลลัพธ์

---

**อัปเดตล่าสุด:** 2026-03-16  
**ทดสอบด้วย:** Aspose.CAD 24.11 for .NET  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}