---
date: 2026-04-06
description: เรียนรู้วิธีแปลง DWG เป็น PDF และเพิ่มข้อความกำหนดเองโดยใช้ C# และ Aspose.CAD
  คู่มือขั้นตอนนี้ครอบคลุมการสร้าง PDF จาก DWG การแทรกเอนทิตีข้อความ และการเปลี่ยนแบบอักษรของข้อความ
  DWG
keywords:
- convert dwg to pdf
- generate pdf from dwg
- insert text entity
- change dwg text font
- aspose cad dwg pdf
linktitle: การเพิ่มข้อความลงในไฟล์ DWG ด้วย C#
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: แปลง DWG เป็น PDF และเพิ่มข้อความใน C# – บทเรียน Aspose.CAD
url: /th/net/dwg-file-manipulation/adding-text-to-dwg/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# แปลง DWG เป็น PDF และเพิ่มข้อความใน C# – บทแนะนำ Aspose.CAD

## บทนำ

ในโลกที่เคลื่อนที่อย่างรวดเร็วของ CAD และการพัฒนา .NET การ **แปลง DWG เป็น PDF** พร้อมกับการแทรกคำอธิบายกำหนดเองเป็นความต้องการที่พบบ่อย ไม่ว่าคุณจะต้องการสร้างแบบแปลนที่พิมพ์ได้สำหรับลูกค้าหรือฝังโน้ตแบบไดนามิกโดยตรงลงใน DWG, Aspose.CAD ทำให้การทำงานนี้ง่ายดาย ในบทแนะนำนี้คุณจะได้เรียนรู้วิธี **แปลง DWG เป็น PDF**, **เพิ่มเอนทิตีข้อความ**, และแม้กระทั่ง **เปลี่ยนฟอนต์ข้อความใน DWG** ด้วย C#.

## คำตอบสั้น

- **ไลบรารีที่ดีที่สุดสำหรับการแปลง DWG‑to‑PDF คืออะไร?** Aspose.CAD for .NET  
- **ฉันสามารถเพิ่มข้อความกำหนดเองขณะแปลงได้หรือไม่?** ใช่ – สร้างเอนทิตี `CadText` แล้วเพิ่มก่อนบันทึก.  
- **ฉันต้องการใบอนุญาตสำหรับการใช้งานในผลิตภัณฑ์หรือไม่?** จำเป็นต้องมีใบอนุญาตเชิงพาณิชย์; มีรุ่นทดลองฟรีให้ใช้.  
- **เวอร์ชัน .NET ที่รองรับคืออะไร?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **สามารถเปลี่ยนฟอนต์ข้อความได้หรือไม่?** ใช่, ปรับคุณสมบัติของ `CadText` เช่น `StyleType` และ `TextHeight`.

## “การแปลง dwg เป็น pdf” คืออะไร?

การแปลงไฟล์ DWG เป็น PDF จะเปลี่ยนแบบ CAD ที่เป็นเวกเตอร์ให้เป็นเอกสารที่สามารถแชร์ได้อย่างกว้างขวางและไม่ขึ้นกับอุปกรณ์ PDF จะรักษาเรขาคณิตและเลเยอร์เดิมไว้ พร้อมให้คุณฝังคำอธิบาย, ข้อความ หรือเมตาดาต้าอื่น ๆ Aspose.CAD จัดการการเรสเตอร์ไลซ์และการเรนเดอร์เวกเตอร์โดยอัตโนมัติ ดังนั้นคุณไม่จำเป็นต้องมีซอฟต์แวร์ CAD ของบุคคลที่สามบนเซิร์ฟเวอร์.

## ทำไมต้องเพิ่มข้อความลงใน DWG ก่อนการแปลง?

การฝังข้อความโดยตรงลงใน DWG ให้คุณควบคุมการวางตำแหน่ง, การจัดรูปแบบ, และการกำหนดเลเยอร์ได้อย่างเต็มที่ เมื่อไฟล์ถูกแปลงเป็น PDF ภายหลัง ข้อความจะปรากฏตรงตำแหน่งที่คุณกำหนดไว้, รักษาเจตนาการออกแบบและขจัดความจำเป็นในการทำหลังการประมวลผลในโปรแกรมแก้ไข PDF.

## ข้อกำหนดเบื้องต้น

- **Aspose.CAD Library** – ดาวน์โหลดได้จาก [download link](https://releases.aspose.com/cad/net/).  
- **สภาพแวดล้อม .NET ที่ทำงานได้** (Visual Studio 2022, .NET 6, หรือเวอร์ชันที่เข้ากันได้ใด ๆ).  
- **โฟลเดอร์สำหรับไฟล์ทดสอบของคุณ** – เราจะอ้างอิงเป็น `MyDir` ตลอดคู่มือ.

ตอนนี้, เรามาเดินผ่านกระบวนการทีละขั้นตอนกัน.

## นำเข้า Namespaces

เพิ่มคำสั่ง `using` ที่จำเป็นเพื่อให้คุณเข้าถึงคลาสของ Aspose.CAD.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects.AttEntities;
using Aspose.CAD.ImageOptions;
```

## ขั้นตอนที่ 1: โหลดไฟล์ DWG

โหลดไฟล์ DWG ต้นฉบับของคุณเข้าสู่วัตถุ `Image`. วัตถุนี้ให้คุณเข้าถึงเอนทิตี CAD ภายใน.

```csharp
string dwgPathToFile = MyDir + "SimpleEntites.dwg";
using (Image image = Image.Load(dwgPathToFile))
{
    // Subsequent steps will be performed inside this block
}
```

## ขั้นตอนที่ 2: สร้างอ็อบเจ็กต์ CadText (แทรกเอนทิตีข้อความ)

คลาส `CadText` แสดงถึงข้อความบรรทัดเดียวใน DWG. ที่นี่เราตั้งค่าสไตล์, ค่า, สี, เลเยอร์, และตำแหน่งของมัน. ปรับ `StyleType` หรือ `TextHeight` เพื่อ **เปลี่ยนฟอนต์ข้อความใน DWG**.

```csharp
CadText cadText = new CadText();
cadText.StyleType = "Standard";          // Font/style – change to alter DWG text font
cadText.DefaultValue = "Some custom text";
cadText.ColorId = 256;                    // 256 = ByLayer (you can use a specific ACI color)
cadText.LayerName = "0";
cadText.FirstAlignment.X = 47.90;
cadText.FirstAlignment.Y = 5.56;
cadText.TextHeight = 0.8;                 // Height influences visual size
cadText.ScaleX = 0.0;
```

## ขั้นตอนที่ 3: เพิ่มเอนทิตีข้อความลงใน Model Space

Model Space ของ DWG เก็บเอนทิตีการวาดส่วนใหญ่. โดยการเพิ่ม `CadText` ของเราไปยังบล็อก `*Model_Space`, ข้อความจะกลายเป็นส่วนหนึ่งของแบบแปลน.

```csharp
CadImage cadImage = (CadImage)image;
cadImage.BlockEntities["*Model_Space"].AddEntity(cadText);
```

## ขั้นตอนที่ 4: กำหนดค่า PDF Options (สร้าง PDF จาก DWG)

ตั้งค่าตัวเลือกการเรสเตอร์ไลซ์ที่ควบคุมวิธีการเรนเดอร์ DWG เป็น PDF. คุณสามารถปรับขนาดหน้า, ประเภทการวาด, และการจัดวาง.

```csharp
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.VectorRasterizationOptions = cadRasterizationOptions;
cadRasterizationOptions.DrawType = CadDrawTypeMode.UseObjectColor;
cadRasterizationOptions.PageHeight = 1600;
cadRasterizationOptions.PageWidth = 1600;
cadRasterizationOptions.Layouts = new string[] { "Model" };
```

## ขั้นตอนที่ 5: บันทึก DWG ที่แก้ไขเป็น PDF

สุดท้าย, ส่งออกแบบแปลนที่แก้ไข. PDF ที่ได้จะรวมข้อความที่แทรกใหม่.

```csharp
image.Save(MyDir + "SimpleEntites_generated.pdf", pdfOptions);
```

> **เคล็ดลับ:** หากคุณต้องการ PDF ความละเอียดสูงขึ้น, เพิ่มค่า `PageHeight` และ `PageWidth` อย่างสัดส่วน.

## ปัญหาที่พบบ่อยและวิธีแก้

| ปัญหา | สาเหตุ | วิธีแก้ |
|-------|--------|-----|
| ข้อความไม่ปรากฏใน PDF | เลเยอร์หรือรหัสสีผิด | ตรวจสอบว่า `LayerName` มีอยู่และ `ColorId` ตั้งเป็นสีที่มองเห็นได้ (เช่น 7 สำหรับสีขาว). |
| ข้อความอยู่ผิดตำแหน่ง | พิกัดการจัดแนวไม่ถูกต้อง | ตรวจสอบค่าของ `FirstAlignment.X/Y` ตามหน่วยของแบบแปลน. |
| PDF ว่างเปล่า | ไม่ได้ตั้งค่าตัวเลือกการเรสเตอร์ไลซ์ | ตั้งค่า `DrawType` เป็น `UseObjectColor` หรือ `UseObjectLineWeight`. |

## คำถามที่พบบ่อย (เดิม)

### Q1: Aspose.CAD รองรับเวอร์ชันไฟล์ DWG ทั้งหมดหรือไม่?

A1: Aspose.CAD รองรับช่วงเวอร์ชันไฟล์ DWG ที่หลากหลาย, ทำให้เข้ากันได้กับซอฟต์แวร์ CAD ต่าง ๆ.

### Q2: ฉันสามารถเพิ่มหลายเอนทิตีข้อความในไฟล์ DWG เดียวโดยใช้ Aspose.CAD ได้หรือไม่?

A2: ได้, คุณสามารถเพิ่มหลายเอนทิตีข้อความในไฟล์ DWG ได้โดยทำซ้ำขั้นตอนที่อธิบายในบทแนะนำ.

### Q3: ฉันจะเปลี่ยนฟอนต์และสไตล์ของข้อความใน Aspose.CAD อย่างไร?

A3: เพื่อปรับเปลี่ยนฟอนต์และสไตล์ของข้อความ, ปรับคุณสมบัติของอ็อบเจ็กต์ `CadText` ก่อนเพิ่มลงในไฟล์ DWG.

### Q4: มีข้อพิจารณาเรื่องใบอนุญาตในการใช้ Aspose.CAD ในโครงการเชิงพาณิชย์หรือไม่?

A5: ใช่, โปรดตรวจสอบให้สอดคล้องกับเงื่อนไขการให้ใบอนุญาตของ Aspose.CAD. ดูรายละเอียดที่ [Aspose.CAD Purchase](https://purchase.aspose.com/buy).

### Q5: ฉันสามารถขอความช่วยเหลือหรือสนทนาเกี่ยวกับคำถามที่เกี่ยวกับ Aspose.CAD ได้ที่ไหน?

A5: เยี่ยมชม [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) เพื่อเชื่อมต่อกับชุมชนและรับการสนับสนุน.

## คำถามเพิ่มเติม

**Q: ฉันจะสร้าง PDF จาก DWG โดยไม่เพิ่มข้อความได้อย่างไร?**  
A: ข้ามขั้นตอนการสร้าง `CadText` และกำหนดค่า `PdfOptions` โดยตรงก่อนเรียก `image.Save(...)`.

**Q: ฉันสามารถเปลี่ยนสีข้อความโดยโปรแกรมได้หรือไม่?**  
A: ใช่, ตั้งค่า `cadText.ColorId` เป็นหมายเลขสี ACI ที่ต้องการ (เช่น 1 สำหรับสีแดง).

**Q: สามารถแทรกข้อความหลายบรรทัดได้หรือไม่?**  
A: ใช้ `CadMText` สำหรับบล็อกข้อความหลายบรรทัด; วิธีการคล้ายกับ `CadText`.

**Q: Aspose.CAD รองรับการแปลงเป็นชุดของหลายไฟล์ DWG หรือไม่?**  
A: แน่นอน – วนลูปผ่านไดเรกทอรีของไฟล์ DWG, ทำตามขั้นตอนเดียวกัน, แล้วบันทึกแต่ละไฟล์เป็น PDF.

## สรุป

ตอนนี้คุณมีเวิร์กโฟลว์ที่ครบถ้วนและพร้อมใช้งานในผลิตภัณฑ์เพื่อ **แปลง DWG เป็น PDF**, **เพิ่มข้อความกำหนดเอง**, และ **ปรับแต่งลักษณะของข้อความ** ด้วย C# และ Aspose.CAD. เทคนิคนี้เหมาะสำหรับการสร้างแบบแปลนอัตโนมัติ, กระบวนการรายงาน, หรือสถานการณ์ใด ๆ ที่คุณต้องการเสริมข้อมูลในไฟล์ CAD อย่างรวดเร็ว.

---

**Last Updated:** 2026-04-06  
**Tested With:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}