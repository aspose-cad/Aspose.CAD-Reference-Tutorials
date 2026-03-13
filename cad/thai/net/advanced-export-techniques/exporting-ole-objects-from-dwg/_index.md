---
description: เรียนรู้วิธีแปลง DWG เป็น PNG และดึงวัตถุ OLE จากไฟล์ DWG ด้วย Aspose.CAD
  สำหรับ .NET – คู่มือสั้น ๆ ที่เน้นโค้ด
linktitle: Exporting OLE Objects from DWG Files
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: แปลง DWG เป็น PNG และส่งออกวัตถุ OLE - บทเรียน Aspose.CAD
url: /th/net/advanced-export-techniques/exporting-ole-objects-from-dwg/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# การส่งออกวัตถุ OLE จากไฟล์ DWG - บทแนะนำ Aspose.CAD

## Introduction

หากคุณต้องการ **convert DWG to PNG** พร้อมดึงวัตถุ OLE ที่ฝังอยู่ คุณมาถูกที่แล้ว Aspose.CAD for .NET ทำให้กระบวนการสองขั้นตอนนี้ง่ายดาย ช่วยให้คุณอัตโนมัติการสกัดและการเรสเตอร์ไลซ์ด้วยเพียงไม่กี่บรรทัดของ C# ในไม่กี่นาทีต่อไป เราจะพาคุณผ่านขั้นตอนทั้งหมด ตั้งแต่การตั้งค่าสภาพแวดล้อมจนถึงการบันทึกแต่ละ DWG เป็น PNG ที่บรรจุข้อมูล OLE ที่สกัดออกมา

## Quick Answers
- **บทเรียนนี้ครอบคลุมอะไรบ้าง?** การแปลง DWG เป็น PNG และการสกัดวัตถุ OLE ด้วย Aspose.CAD for .NET.  
- **ฉันต้องการไลเซนส์หรือไม่?** เวอร์ชันทดลองฟรีใช้ได้สำหรับการพัฒนา; ต้องมีไลเซนส์เชิงพาณิชย์สำหรับการใช้งานจริง.  
- **เวอร์ชัน .NET ที่รองรับคืออะไร?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **ฉันสามารถประมวลผลไฟล์ DWG หลายไฟล์พร้อมกันได้หรือไม่?** ได้ – ตัวอย่างจะวนลูปผ่านอาเรย์ของชื่อไฟล์.  
- **ฉันสามารถหา ตัวอย่างเพิ่มเติมได้ที่ไหน?** ดูเอกสารและลิงก์ฟอรั่มอย่างเป็นทางการของ Aspose.CAD ด้านล่าง.

## What is **convert DWG to PNG**?
การแปลง DWG (ไฟล์ AutoCAD) เป็นภาพ PNG จะทำให้ข้อมูลเวกเตอร์ถูกเรสเตอร์ไลซ์ ทำให้ดูหรือฝังในหน้าเว็บ รายงาน หรือแอปพลิเคชันอื่น ๆ ที่ไม่รองรับ DWG โดยตรงได้ง่ายขึ้น เมื่อมีวัตถุ OLE อยู่ การแปลงนี้สามารถสกัดและบันทึกเป็นไฟล์แยกได้ในระหว่างกระบวนการ

## Why extract OLE objects from CAD files?
ไฟล์ DWG จำนวนมากฝังสเปรดชีต แผนภูมิ หรือเอกสาร Office อื่น ๆ เป็นวัตถุ OLE การสกัดเหล่านี้ทำให้คุณสามารถนำข้อมูลเดิมกลับมาใช้ใหม่ อัตโนมัติการรายงาน หรือย้ายเนื้อหาไปยังรูปแบบใหม่โดยไม่สูญเสียข้อมูลที่ฝังอยู่

## Prerequisites

- Aspose.CAD for .NET Library: ตรวจสอบว่าคุณได้ติดตั้งไลบรารีแล้ว คุณสามารถดาวน์โหลดได้จาก [Aspose.CAD for .NET download page](https://releases.aspose.com/cad/net/).
- Document Directory: ตั้งค่าโฟลเดอร์ที่เก็บไฟล์ DWG ของคุณ แทนที่ `"Your Document Directory"` ในโค้ดตัวอย่างด้วยพาธจริงของคุณ

## Import Namespaces

ในโปรเจกต์ .NET ของคุณ ให้นำเข้า namespace ที่จำเป็น:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Step‑by‑Step Guide

### Step 1: Set the Document Directory

```csharp
string MyDir = "Your Document Directory";
```

แทนที่ `"Your Document Directory"` ด้วยพาธที่ไฟล์ DWG ของคุณตั้งอยู่

### Step 2: List the DWG files you want to process

```csharp
string[] files = new string[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

### Step 3: Configure export options for PNG conversion

```csharp
PngOptions pngOptions = new PngOptions { };
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.VectorRasterizationOptions = rasterizationOptions;
rasterizationOptions.Layouts = new string[] { "Layout1" };
```

คุณสามารถปรับ `CadRasterizationOptions` (เช่น `PageWidth`, `PageHeight`, `BackgroundColor`) ให้ตรงกับความละเอียดที่ต้องการได้

### Step 4: Iterate through each DWG and perform the conversion

```csharp
foreach (string file in files)
{
    using (CadImage cadImage = (CadImage)Image.Load(MyDir + file))
    {
        cadImage.Save(MyDir + file + "_out.png", pngOptions);
    }
}
```

ในลูปนี้ไลบรารีจะ **extracts OLE objects** ที่ฝังอยู่ในแต่ละภาพวาดโดยอัตโนมัติและใส่ไว้ใน PNG ที่สร้างขึ้น หากคุณต้องการสตรีม OLE ดิบ คุณสามารถเข้าถึงคอลเลกชัน `cadImage.OleObjects` – วิธีที่สะดวกในการ **how to extract ole** ข้อมูลโดยโปรแกรม

## Common Issues & Troubleshooting

- **Missing layout name** – ตรวจสอบให้แน่ใจว่าเลย์เอาต์ที่คุณระบุ (`"Layout1"` ในตัวอย่าง) มีอยู่ใน DWG ต้นทาง; หากไม่มี rasterizer จะใช้โมเดลสเปซเริ่มต้นแทน
- **Large files cause memory pressure** – ประมวลผลไฟล์ทีละไฟล์ (ตามที่แสดง) และทำลายอ็อบเจ็กต์ `CadImage` ทันทีด้วย `using`
- **Unexpected colors** – ตั้งค่า `rasterizationOptions.BackgroundColor` ให้ตรงกับพื้นหลังของภาพวาดหากต้องการความโปร่งใส

## Frequently Asked Questions

### Q1: Is Aspose.CAD for .NET suitable for both junior and senior CAD files?
A1: ใช่, Aspose.CAD for .NET มีความยืดหยุ่นและสามารถจัดการไฟล์ CAD ชนิดต่าง ๆ รวมถึงไฟล์ระดับ junior และ senior ได้

### Q2: Can I customize export options for different layouts?
A2: แน่นอน! ตามที่แสดงในบทแนะนำ คุณสามารถปรับแต่งตัวเลือกการส่งออก รวมถึงเลย์เอาต์ เพื่อให้ตรงกับความต้องการของคุณ

### Q3: Where can I find detailed documentation for Aspose.CAD for .NET?
A3: สำรวจ [Aspose.CAD for .NET documentation](https://reference.aspose.com/cad/net/) เพื่อรับข้อมูลเชิงลึกและตัวอย่างเพิ่มเติม

### Q4: Is there a free trial available?
A4: มี, คุณสามารถทดลองใช้ความสามารถของ Aspose.CAD for .NET ได้ฟรี เยี่ยมชม [this link](https://releases.aspose.com/) เพื่อเริ่มต้น

### Q5: How can I get support or connect with the community?
A5: สำหรับการสนับสนุนและการมีส่วนร่วมกับชุมชน ให้เยี่ยมชม [Aspose.CAD forum](https://forum.aspose.com/c/cad/19)

### Q6: How do I **extract OLE from CAD** files without converting to PNG?
A6: ใช้คอลเลกชัน `CadImage.OleObjects` หลังจากโหลด DWG; คุณสามารถวนลูปผ่านแต่ละ `OleObject` แล้วบันทึกข้อมูลดิบลงไฟล์ได้

## Conclusion

คุณได้เรียนรู้วิธี **convert DWG to PNG** พร้อมกับ **extracting OLE objects** อย่างราบรื่นด้วย Aspose.CAD for .NET วิธีนี้ช่วยประหยัดเวลา ลดขั้นตอนคัดลอก‑วางด้วยมือ และสามารถรวมเข้ากับกระบวนการอัตโนมัติได้อย่างลงตัว อย่าลังเลที่จะทดลองใช้รูปแบบเรสเตอร์อื่น ๆ (JPEG, BMP) หรือสำรวจคุณสมบัติการจัดการ CAD ที่หลากหลายของ Aspose

---

**Last Updated:** 2026-03-13  
**Tested With:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}