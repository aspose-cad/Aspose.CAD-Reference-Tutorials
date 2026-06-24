---
date: 2026-03-02
description: เรียนรู้วิธีสร้างไฟล์ PDF เดียวที่มีหลายเลย์เอาต์โดยใช้ Aspise.CAD สำหรับ
  .NET – แปลง CAD เป็น PDF, ส่งออก DWG เป็น PDF, และบันทึก CAD เป็น PDF อย่างมีประสิทธิภาพ.
linktitle: Creating Single PDF with Different Layouts
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: วิธีสร้าง PDF เดียวที่มีเลเอาต์ต่างกัน - คู่มือ Aspose.CAD
url: /th/net/advanced-cad-techniques/creating-single-pdf-with-different-layouts/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีสร้าง single pdf ด้วยเลเอาต์ที่แตกต่าง - Aspose.CAD Guide

## บทนำ

หากคุณต้องการ **create single pdf** ที่มีหลายเลเอาต์ของ CAD, คุณมาถูกที่แล้ว. ในบทแนะนำนี้ เราจะอธิบายขั้นตอนที่จำเป็นเพื่อแปลงภาพวาด CAD ให้เป็นเอกสาร PDF เดียว, พร้อมจัดการหลายเลเอาต์ระหว่างทาง. คุณจะได้เห็นว่า Aspose.CAD for .NET ทำให้การ **convert CAD to PDF**, **export DWG to PDF**, และ **save CAD as PDF** ง่ายขึ้นด้วยเพียงไม่กี่บรรทัดของโค้ด C#.

## Quick Answers
- **What does this tutorial cover?** การสร้าง PDF หนึ่งไฟล์ที่รวมหลายเลเอาต์ของ CAD.  
- **Which library is used?** Aspose.CAD for .NET.  
- **Do I need a license?** ทดลองใช้ฟรีสำหรับการประเมิน; ต้องมีลิขสิทธิ์สำหรับการใช้งานจริง.  
- **Supported CAD formats?** DWG, DXF, DGN และอื่น ๆ อีกหลายรูปแบบ.  
- **Typical implementation time?** ประมาณ 10‑15 นาทีสำหรับการแปลงพื้นฐาน.

## อะไรคือ “create single pdf” ในบริบทของ CAD?

การสร้าง single PDF หมายถึงการนำไฟล์ CAD ต้นฉบับหนึ่งไฟล์ที่อาจมีหลายการกำหนดเลเอาต์ (paper spaces) แล้วรวมแต่ละเลเอาต์เป็นหน้าต่าง ๆ ของเอกสาร PDF หนึ่งไฟล์. สิ่งนี้มีประโยชน์เป็นพิเศษสำหรับแผนผังสถาปัตยกรรม, แผนผังวิศวกรรม, หรือสถานการณ์ใด ๆ ที่ลูกค้าต้องการแพ็คเกจ PDF ที่รวมไว้ในหนึ่งไฟล์.

## ทำไมต้องใช้ Aspose.CAD สำหรับงานนี้?

- **No external dependencies** – .NET แท้, ไม่ต้องติดตั้ง AutoCAD.  
- **Full control over rasterization** – คุณสามารถกำหนดขนาดหน้า, DPI, และมิติของเลเอาต์ที่กำหนดเอง.  
- **High‑fidelity rendering** – ข้อมูลเวกเตอร์จะถูกเก็บไว้เมื่อเป็นไปได้, ทำให้ผลลัพธ์คมชัด.  
- **Batch‑ready** – โค้ดเดียวกันสามารถใส่ในลูปเพื่อประมวลผลหลายภาพวาดโดยอัตโนมัติ.

## ข้อกำหนดเบื้องต้น

- Aspose.CAD for .NET: ตรวจสอบว่าคุณได้ติดตั้ง Aspose.CAD for .NET แล้ว. คุณสามารถดาวน์โหลดได้จาก [here](https://releases.aspose.com/cad/net/).  
- Development Environment: ตั้งค่าสภาพแวดล้อมการพัฒนา .NET, และมีความเข้าใจพื้นฐานเกี่ยวกับการเขียนโปรแกรม C#.

## นำเข้า Namespaces

ในโปรเจกต์ C# ของคุณ, ให้รวม Namespaces ที่จำเป็นเพื่อใช้ฟังก์ชันของ Aspose.CAD for .NET:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## คู่มือขั้นตอนต่อขั้นตอน

### ขั้นตอนที่ 1: โหลดภาพ CAD

แรกเริ่มให้โหลดไฟล์ CAD ต้นฉบับ (เช่นไฟล์ DWG). คลาส `CadImage` จะให้คุณเข้าถึงเลเอาต์ทั้งหมดภายในไฟล์.

```csharp
// The path to the documents directory.
string MyDir = "Your Document Directory";

using (CadImage cadImage = (CadImage)Image.Load(MyDir + "City skyway map.dwg"))
{
    // Your code for Step 1 goes here
}
```

### ขั้นตอนที่ 2: ปรับแต่งตัวเลือกการแรสเตอร์ไลเซชัน

กำหนดวิธีการแรสเตอร์ไลเซชันของแต่ละเลเอาต์. คุณสามารถตั้งค่าขนาดหน้าตั้งต้นแล้วทำการแทนที่สำหรับเลเอาต์เฉพาะโดยใช้ `LayoutPageSizes`.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1000;
rasterizationOptions.PageHeight = 1000;

// Custom sizes for several layouts
rasterizationOptions.LayoutPageSizes.Add("ANSI C Plot", new SizeF(500, 1000));
rasterizationOptions.LayoutPageSizes.Add("8.5 x 11 Plot", new SizeF(1000, 100));
```

> **Pro tip:** ปรับ DPI (`rasterizationOptions.Resolution`) หากคุณต้องการผลลัพธ์ความละเอียดสูงสำหรับภาพวาดที่ละเอียด.

### ขั้นตอนที่ 3: กำหนดตัวเลือก PDF

ห่อหุ้มการตั้งค่าการแรสเตอร์ไลเซชันไว้ในอ็อบเจ็กต์ `PdfOptions`. สิ่งนี้บอก Aspose.CAD ให้เรนเดอร์ข้อมูล CAD โดยตรงเป็นสตรีม PDF.

```csharp
PdfOptions pdfOptions = new PdfOptions() { VectorRasterizationOptions = rasterizationOptions };
```

### ขั้นตอนที่ 4: บันทึกเป็น PDF

สุดท้ายให้เรียก `Save` บนอินสแตนซ์ `CadImage`, ส่งชื่อไฟล์ PDF ปลายทางและตัวเลือกที่เตรียมไว้. ไลบรารีจะสร้าง PDF เดียวที่มีหน้าสำหรับแต่ละเลเอาต์ที่คุณกำหนดค่า.

```csharp
cadImage.Save(MyDir + "singlePDF_out.pdf", pdfOptions);
```

หลังจากเรียกนี้แล้ว, คุณจะได้ PDF ที่รวมเลเอาต์ “ANSI C Plot” และ “8.5 x 11 Plot” เข้าเป็นเอกสารเดียวที่ต่อเนื่องกัน.

## ข้อผิดพลาดทั่วไปและการแก้ไขปัญหา

| ปัญหา | สาเหตุ | วิธีแก้ |
|-------|--------|-----|
| Layouts missing in PDF | `LayoutPageSizes` ไม่ได้กำหนดสำหรับชื่อเลเอาต์ | ตรวจสอบชื่อเลเอาต์ที่ถูกต้องในไฟล์ CAD (แยกแยะตัวพิมพ์ใหญ่‑เล็ก). |
| Low‑quality output | DPI เริ่มต้นคือ 96 | ตั้งค่า `rasterizationOptions.Resolution = 300` (หรือสูงกว่า) ก่อนบันทึก. |
| File not found | เส้นทาง `MyDir` ไม่ถูกต้อง | ใช้ `Path.Combine` เพื่อสร้างเส้นทางที่เป็นอิสระต่อแพลตฟอร์ม. |

## คำถามที่พบบ่อย

### Q1: Can I use Aspose.CAD for .NET with other CAD formats?

A1: ใช่, Aspose.CAD for .NET รองรับรูปแบบ CAD ต่าง ๆ เช่น DWG, DXF, DGN และอื่น ๆ อีกหลายรูปแบบ.

### Q2: Is there a free trial available?

A2: ใช่, คุณสามารถสำรวจการทดลองใช้ฟรีได้จาก [here](https://releases.aspose.com/).

### Q3: How can I get support for Aspose.CAD for .NET?

A3: เยี่ยมชม [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) เพื่อรับการสนับสนุนจากชุมชน.

### Q4: Where can I find detailed documentation?

A4: ดูเอกสารรายละเอียดได้ที่ [here](https://reference.aspose.com/cad/net/).

### Q5: Can I purchase a license for Aspose.CAD for .NET?

A5: ใช่, คุณสามารถซื้อไลเซนส์ได้จาก [here](https://purchase.aspose.com/buy).

**Additional Q&A**

**Q:** How do I **export DWG to PDF** with custom page sizes?  
**A:** ใช้ `CadRasterizationOptions.LayoutPageSizes` เพื่อแมปแต่ละเลเอาต์ของ DWG ไปยังขนาดหน้าที่ต้องการใน PDF, ตามที่แสดงในขั้นตอน 2.

**Q:** Is it possible to **save CAD as PDF** without rasterizing vector data?  
**A:** Aspose.CAD จะทำการแรสเตอร์ไลเซชันเสมอเมื่อสร้าง PDF, แต่คุณสามารถเพิ่ม DPI เพื่อรักษาความคมชัดของภาพได้.

## สรุป

ในคู่มือนี้เราได้สาธิตวิธี **create single pdf** จากภาพวาด CAD ที่มีหลายเลเอาต์โดยใช้ Aspose.CAD for .NET. ตอนนี้คุณมีบล็อกพื้นฐานเพื่อ **convert CAD to PDF**, **export DWG to PDF**, และ **save CAD as PDF** ในเวิร์กโฟลว์อัตโนมัติเดียว. ทดลองปรับตั้งค่าการแรสเตอร์ไลเซชันต่าง ๆ เพื่อให้ตรงกับความต้องการคุณภาพของโครงการของคุณ, และผสานโค้ดนี้เข้ากับระบบประมวลผลแบบแบตช์ที่ใหญ่ขึ้นตามต้องการ.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**อัปเดตล่าสุด:** 2026-03-02  
**ทดสอบด้วย:** Aspose.CAD for .NET 24.11  
**ผู้เขียน:** Aspose  

---