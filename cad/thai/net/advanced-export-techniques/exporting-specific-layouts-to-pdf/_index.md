---
date: 2026-03-13
description: เรียนรู้วิธีตั้งค่าตัวเลือกการเรสเตอร์ไลซ์ของ CAD และส่งออกเลย์เอาต์
  DWG เฉพาะเป็น PDF ด้วย Aspose.CAD สำหรับ .NET – คู่มือฉบับสมบูรณ์ในการสร้าง PDF
  จากไฟล์ CAD.
linktitle: Exporting Specific Layouts to PDF
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: ตั้งค่าตัวเลือกการเรสเตอร์ไลซ์ CAD – ส่งออกเลย์เอาต์เฉพาะเป็น PDF - คู่มือ
  Aspose.CAD
url: /th/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# การส่งออก Layout เฉพาะเป็น PDF - คู่มือ Aspose.CAD

## บทนำ

ในบทแนะนำนี้คุณจะได้ค้นพบ **วิธีตั้งค่า CAD rasterization options** เพื่อให้คุณสามารถส่งออก layout เดียวหรือหลาย layout จากไฟล์ DWG ไปยัง PDF ได้โดยตรง Aspose.CAD สำหรับ .NET ทำให้กระบวนการ *dwg to pdf conversion c#* เป็นเรื่องง่าย ให้คุณควบคุมขนาดหน้า ความละเอียด และการเลือก layout ได้อย่างเต็มที่ เมื่อจบคู่มือคุณจะสามารถ **สร้าง PDF จากไฟล์ CAD** ด้วยเพียงไม่กี่บรรทัดของโค้ด

## คำตอบสั้น
- **“set cad rasterization options” ทำอะไร?**  
  มันบอก Aspose.CAD ว่าจะเรนเดอร์ข้อมูลเวกเตอร์ (layout, layer, line weight) ไปเป็นหน้า PDF ที่แรสเตอร์ไลซ์  
- **เมธอดใดที่ใช้ส่งออก DWG layout ไปเป็น PDF?**  
  ใช้ `Image.Save` พร้อมกับ `PdfOptions` ที่กำหนด `CadRasterizationOptions` ไว้แล้ว  
- **ฉันสามารถส่งออกหลาย layout พร้อมกันได้หรือไม่?**  
  ได้ – เพียงใส่อาร์เรย์ของชื่อ layout ในคุณสมบัติ `Layouts`  
- **ต้องมีลิขสิทธิ์สำหรับการใช้งานในผลิตภัณฑ์หรือไม่?**  
  ต้องมีลิขสิทธิ์เชิงพาณิชย์; มีรุ่นทดลองฟรีสำหรับการประเมินผล  
- **รองรับ .NET เวอร์ชันใดบ้าง?**  
  .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6 และรุ่นต่อไป

## “set cad rasterization options” คืออะไร?
`CadRasterizationOptions` คือคลาสที่ควบคุมวิธีการแรสเตอร์ไลซ์เอนทิตี CAD เมื่อแปลงเป็นรูปแบบที่ใช้แรสเตอร์เช่น PDF โดยการกำหนดคุณสมบัติต่าง ๆ – ขนาดหน้า, การเลือก layout, สีพื้นหลัง ฯลฯ – คุณจะกำหนดผลลัพธ์ภาพของการ **export dwg layout to pdf** ได้ตามต้องการ

## ทำไมต้องตั้งค่า CAD rasterization options?
- **ความแม่นยำ** – รักษา line weight และสเกลให้ตรงกับที่แสดงในแบบ CAD ดั้งเดิม  
- **ประสิทธิภาพ** – เรนเดอร์เฉพาะ layout ที่ต้องการ ลดขนาดไฟล์และเวลาในการประมวลผล  
- **ความยืดหยุ่น** – ปรับความกว้าง/สูงของหน้า, DPI, และสีพื้นหลังให้สอดคล้องกับมาตรฐานรายงานของคุณ  

## สิ่งที่ต้องเตรียม

ก่อนจะลงมือเขียนโค้ด ให้ตรวจสอบว่าคุณมี:

- **Aspose.CAD for .NET** ติดตั้งแล้ว คุณสามารถดาวน์โหลดได้ [ที่นี่](https://releases.aspose.com/cad/net/)  
- สภาพแวดล้อมการพัฒนา .NET (Visual Studio, VS Code หรือ IDE ใดก็ได้ที่คุณชอบ)  
- ไฟล์ DWG ที่มีอย่างน้อยหนึ่ง layout (ไฟล์ตัวอย่างที่ใช้ในที่นี้คือ `visualization_-_conference_room.dwg`)

## นำเข้า Namespaces

ในโปรเจกต์ .NET ของคุณ ให้นำเข้า namespaces ที่จำเป็นสำหรับ Aspose.CAD:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## คู่มือแบบขั้นตอน

### ขั้นตอนที่ 1: โหลดไฟล์ DWG

แรกเริ่มให้ชี้ Aspose.CAD ไปยังไฟล์ DWG ต้นทางที่คุณต้องการแปลง

```csharp
// The path to the documents directory.
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";

using (Image image = Image.Load(sourceFilePath))
{
    // Your code for further steps goes here.
}
```

### ขั้นตอนที่ 2: ตั้งค่า **CadRasterizationOptions**

ที่นี่เราจะกำหนดค่าการแรสเตอร์ไลซ์ที่กำหนดขนาดหน้า PDF และความละเอียด

```csharp
// Create an instance of CadRasterizationOptions and set its various properties
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
```

> **เคล็ดลับ:** ปรับ `PageWidth` และ `PageHeight` ให้ตรงกับมิติของ layout PDF ที่คุณต้องการ ค่าที่ใหญ่ขึ้นจะเพิ่มรายละเอียดแต่ก็ทำให้ไฟล์ใหญ่ขึ้นด้วย

### ขั้นตอนที่ 3: ระบุชื่อ layout

บอก Aspose.CAD ว่าจะเรนเดอร์ layout ใดบ้าง แทนที่ `"Layout1"` ด้วยชื่อ layout ที่ตรงกับไฟล์ DWG ของคุณ

```csharp
// Specify desired layout name
rasterizationOptions.Layouts = new string[] { "Layout1" };
```

> **ทำไมต้องทำเช่นนี้:** การจำกัดอาร์เรย์ `Layouts` จะช่วยหลีกเลี่ยงการส่งออกแผ่นที่ไม่ต้องการ ทำให้การ **dwg to pdf conversion c#** เร็วขึ้นและ PDF ที่ได้สะอาดกว่า

### ขั้นตอนที่ 4: สร้าง `PdfOptions`

เชื่อมการตั้งค่าแรสเตอร์ไลซ์เข้ากับตัวเลือกการส่งออก PDF

```csharp
// Create an instance of PdfOptions
PdfOptions pdfOptions = new PdfOptions();
// Set the VectorRasterizationOptions property
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

### ขั้นตอนที่ 5: ส่งออกเป็น PDF

สุดท้ายให้บันทึก layout ที่เรนเดอร์เป็นไฟล์ PDF

```csharp
MyDir = MyDir + "ExportSpecificLayoutToPDF_out.pdf";
// Export the DWG to PDF
image.Save(MyDir, pdfOptions);
```

### ขั้นตอนที่ 6: แสดงข้อความสำเร็จ

การแสดงผลบนคอนโซลสั้น ๆ จะยืนยันว่าการดำเนินการสำเร็จ

```csharp
// Display success message
Console.WriteLine("\nThe DWG file with a specific layout exported successfully to PDF.\nFile saved at " + MyDir);
```

## ปัญหาที่พบบ่อยและวิธีแก้

| ปัญหา | สาเหตุ | วิธีแก้ |
|-------|-------|--------|
| **ไม่มี PDF สร้างขึ้น** | อาร์เรย์ `Layouts` ไม่ตรงกับชื่อ layout ใดใน DWG | ตรวจสอบชื่อ layout ด้วยโปรแกรมดู CAD แล้วอัปเดตคุณสมบัติ `Layouts` |
| **หน้าเปล่า** | `PageWidth`/`PageHeight` ตั้งเป็น 0 หรือค่าที่เล็กเกินไป | ใช้มิติที่เป็นจริง (เช่น 1600 × 1600) หรือให้ Aspose คำนวนอัตโนมัติโดยไม่กำหนดคุณสมบัตินี้ |
| **สเกลไม่ถูกต้อง** | ไม่ได้ตั้ง DPI เมื่อจำเป็นต้องได้ผลลัพธ์ความละเอียดสูง | ตั้ง `rasterizationOptions.Resolution = 300;` (หรือ DPI ที่ต้องการ) ก่อนส่งออก |

## คำถามที่พบบ่อย

**ถาม: ฉันสามารถส่งออกหลาย layout พร้อมกันได้หรือไม่?**  
ตอบ: ได้ เพียงแก้ไขอาร์เรย์ `Layouts` ในขั้นตอนที่ 3 ให้รวมชื่อ layout ทั้งหมดที่ต้องการ เช่น `new string[] { "Layout1", "Layout2" }`

**ถาม: Aspose.CAD รองรับรูปแบบไฟล์ CAD อื่น ๆ หรือไม่?**  
ตอบ: รองรับอย่างแน่นอน รวมถึง DWG, DXF, DWF, DGN และรูปแบบอื่น ๆ อีกหลายชนิด

**ถาม: ฉันจะปรับตั้งค่า PDF เพิ่มเติมนอกจากขนาดหน้าได้อย่างไร?**  
ตอบ: สำรวจคุณสมบัติเพิ่มเติมของ `CadRasterizationOptions` เช่น `Resolution`, `BackgroundColor`, และ `DrawType` เพื่อปรับแต่งผลลัพธ์ให้ตรงตามต้องการ

**ถาม: จะหาเอกสารเพิ่มเติมของ Aspose.CAD ได้ที่ไหน?**  
ตอบ: เยี่ยมชม [documentation](https://reference.aspose.com/cad/net/) เพื่อดูรายละเอียด API และตัวอย่างเพิ่มเติม

**ถาม: มีรุ่นทดลองฟรีหรือไม่?**  
ตอบ: มี คุณสามารถเข้าถึงรุ่นทดลองฟรีได้ [ที่นี่](https://releases.aspose.com/)

## สรุป

คุณได้เรียนรู้วิธี **ตั้งค่า CAD rasterization options** และใช้มันเพื่อ **ส่งออก DWG layout เฉพาะเป็น PDF** ด้วย Aspose.CAD สำหรับ .NET วิธีนี้ให้การควบคุมที่แม่นยำต่อกระบวนการแปลง ทำให้คุณสามารถรวมฟังก์ชัน CAD‑to‑PDF เข้าในแอปพลิเคชัน C# ใดก็ได้อย่างรวดเร็วและเชื่อถือได้

---

**อัปเดตล่าสุด:** 2026-03-13  
**ทดสอบกับ:** Aspose.CAD 24.11 for .NET  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}