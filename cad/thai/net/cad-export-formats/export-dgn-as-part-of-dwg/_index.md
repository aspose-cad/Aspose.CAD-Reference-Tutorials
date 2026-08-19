---
date: 2026-03-21
description: เรียนรู้วิธีสร้าง PDF จาก DWG และส่งออก DGN เป็นส่วนหนึ่งของ DWG ด้วย
  Aspose.CAD สำหรับ .NET คู่มือนี้ยังแสดงวิธีแปลง DWG เป็น PDF และตั้งค่าตัวเลือก
  PDF
linktitle: Export DGN as Part of DWG
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: สร้าง PDF จาก DWG และส่งออก DGN เป็นส่วนหนึ่งของ DWG – Aspose.CAD สำหรับ .NET
url: /th/net/cad-export-formats/export-dgn-as-part-of-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# สร้าง PDF จาก DWG และส่งออก DGN เป็นส่วนหนึ่งของ DWG – Aspose.CAD for .NET

## บทนำ

หากคุณต้องการ **สร้าง PDF จากไฟล์ DWG** พร้อมกับฝังการออกแบบ DGN เป็นส่วนหนึ่งของ DWG, Aspose.CAD for .NET ทำให้ขั้นตอนนี้ง่ายดาย ในบทแนะนำนี้เราจะเดินผ่านขั้นตอนทั้งหมด: โหลด DWG, ค้นหา DGN underlay ที่ฝังอยู่, ตั้งค่าตัวเลือกการเรสเตอร์ไลซ์, และสุดท้ายส่งออกผลลัพธ์เป็นเอกสาร PDF ไม่ว่าคุณจะสร้างเครื่องมือแปลงแบบแบตช์, ระบบรายงาน, หรือบริการการบูรณาการ CAD‑BIM ขั้นตอนต่อไปนี้จะให้พื้นฐานที่มั่นคงและพร้อมใช้งานในระดับผลิตจริง

## คำตอบสั้น
- **ไลบรารีใดที่จัดการการแปลง DWG → PDF?** Aspose.CAD for .NET  
- **ฉันสามารถส่งออก DGN underlay ขณะสร้าง PDF ได้หรือไม่?** ได้ – สามารถเข้าถึง underlay ผ่าน `CadDgnUnderlay`  
- **เมธอดใดที่ตั้งค่าตัวเลือก PDF?** `PdfOptions` ร่วมกับ `CadRasterizationOptions`  
- **ต้องมีลิขสิทธิ์สำหรับการใช้งานเชิงพาณิชย์หรือไม่?** ต้องมีลิขสิทธิ์ Aspose.CAD ที่ถูกต้อง  
- **รองรับเวอร์ชัน .NET ใดบ้าง?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7

## “สร้าง PDF จาก DWG” คืออะไร?

การสร้าง PDF จากไฟล์ DWG หมายถึงการเรนเดอร์ภาพเวกเตอร์ของการวาดเป็นเอกสาร PDF แบบเรสเตอร์หรือเวกเตอร์ กระบวนการนี้มีประโยชน์สำหรับการแชร์แบบร่างกับผู้ที่ไม่มีซอฟต์แวร์ CAD, การเก็บถาวร, หรือการสร้างรายงานที่พิมพ์ได้ Aspose.CAD ทำให้การทำงานนี้ง่ายขึ้นโดยจัดการการพาร์สเอนทิตีของ DWG และให้การควบคุมละเอียดผ่าน `PdfOptions`

## ทำไมต้องส่งออก DGN เป็นส่วนหนึ่งของ DWG?

DGN underlay มักเป็นการอ้างอิงเรขาคณิตจากโครงการ MicroStation การส่งออก DGN พร้อมกับ DWG จะช่วยรักษาบริบทการออกแบบเดิมไว้ ทำให้ผู้รับต่อไปเห็นชุดแบบร่างครบถ้วน สิ่งนี้มีคุณค่าอย่างยิ่งในโครงการหลายสาขาที่มีไฟล์ DWG และ DGN อยู่ร่วมกัน

## ข้อกำหนดเบื้องต้น

- **Aspose.CAD for .NET** – ดาวน์โหลดได้ [ที่นี่](https://releases.aspose.com/cad/net/)  
- **สภาพแวดล้อมการพัฒนา** – Visual Studio (เวอร์ชันล่าสุดใดก็ได้) หรือ IDE .NET ที่คุณชื่นชอบ  
- **ความรู้พื้นฐาน C#** – ควรคุ้นเคยกับไวยากรณ์ C# และโครงสร้างโครงการ .NET

## นำเข้า Namespaces

เพิ่ม `using` directives ที่จำเป็นไว้ด้านบนของไฟล์ C# ของคุณ:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## คู่มือแบบขั้นตอน

### ขั้นตอนที่ 1: กำหนดเส้นทางไฟล์

ตั้งค่าไฟล์ DWG อินพุตและชื่อไฟล์ PDF เอาต์พุต

```csharp
// Input and Output file paths
string fileName = "BlockRefDgn.dwg";
string outPath = fileName + ".pdf";
```

### ขั้นตอนที่ 2: สร้างอินสแตนซ์ `PdfOptions` (ตั้งค่าตัวเลือก PDF)

`PdfOptions` ให้คุณควบคุมวิธีการสร้าง PDF เช่น ขนาดหน้า, การบีบอัด, และเมตาดาต้า

```csharp
// Create an instance of PdfOptions class for exporting DWG to PDF
PdfOptions exportOptions = new PdfOptions();
```

### ขั้นตอนที่ 3: โหลดไฟล์ DWG

โหลด DWG เป็น `CadImage` เพื่อให้คุณตรวจสอบเอนทิตีต่าง ๆ

```csharp
// Load the existing DWG file as an image and convert it to CadImage type
using (CadImage cadImage = (CadImage)Image.Load(fileName))
```

### ขั้นตอนที่ 4: วนลูปผ่านเอนทิตีทั้งหมด

เดินผ่านทุกเอนทิตีในแบบร่างเพื่อค้นหา DGN underlay

```csharp
// Iterate through each entity inside the DWG file
foreach (CadBaseEntity baseEntity in cadImage.Entities)
```

### ขั้นตอนที่ 5: ตรวจสอบประเภทเอนทิตี (วิธีส่งออก dgn)

ระบุว่าเอนทิตีปัจจุบันเป็น DGN underlay หรือไม่

```csharp
// Check if the entity is an image definition
if (baseEntity.TypeName == CadEntityTypeName.DGNUNDERLAY)
```

### ขั้นตอนที่ 6: รับเส้นทาง Underlay

ดึงเส้นทางอ้างอิงภายนอกของไฟล์ DGN

```csharp
// If it's an image definition, get the external reference to the object
CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
Console.WriteLine(dgnFile.UnderlayPath);
```

### ขั้นตอนที่ 7: กำหนดตัวเลือกการเรสเตอร์ไลซ์ (แปลง dwg เป็น pdf)

ตั้งค่าการเรสเตอร์ไลซ์ DWG ก่อนนำไปวางใน PDF

```csharp
// Define settings for CadRasterizationOptions object
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

### ขั้นตอนที่ 8: ส่งออก DWG เป็น PDF

สุดท้ายบันทึกภาพที่เรนเดอร์เป็นไฟล์ PDF

```csharp
// Export the DWG to PDF by calling Save method
cadImage.Save(outPath, exportOptions);
```

## ปัญหาที่พบบ่อยและวิธีแก้

| ปัญหา | สาเหตุ | วิธีแก้ |
|-------|--------|-----|
| **`Image.Load` ขว้าง “File not found”** | เส้นทางไม่ถูกต้องหรือไฟล์หาย | ใช้เส้นทางแบบ absolute หรือให้แน่ใจว่า DWG ถูกคัดลอกไปยังโฟลเดอร์เอาต์พุต |
| **เส้นทาง Underlay ว่าง** | DGN underlay ไม่ได้ฝังหรืออ้างอิงเสีย | ตรวจสอบว่า DWG มี DGN underlay จริง ๆ และไฟล์ DGN ภายนอกเข้าถึงได้ |
| **ผลลัพธ์ PDF เป็นสีขาว** | ตัวเลือกการเรสเตอร์ไลซ์ตั้งค่าเป็นขนาดศูนย์ | ปรับ `PageWidth`/`PageHeight` หรือตั้งค่า `NoScaling = false` |
| **ข้อยกเว้นลิขสิทธิ์** | รันโดยไม่มีลิขสิทธิ์ Aspose.CAD ที่ถูกต้อง | ใส่ลิขสิทธิ์ก่อนโหลดภาพ: `License lic = new License(); lic.SetLicense("Aspose.CAD.lic");` |

## คำถามที่พบบ่อย

### Q1: ฉันสามารถใช้ Aspose.CAD for .NET ในโครงการเชิงพาณิชย์ของฉันได้หรือไม่?
A1: ใช่ คุณสามารถทำได้ เยี่ยมชม [ที่นี่](https://purchase.aspose.com/buy) เพื่อดูตัวเลือกการให้ลิขสิทธิ์

### Q2: มีข้อจำกัดใดเกี่ยวกับขนาดไฟล์ DWG ที่ฉันสามารถประมวลผลได้หรือไม่?
A2: Aspose.CAD รองรับการจัดการไฟล์ DWG ขนาดใหญ่ แต่ข้อจำกัดของฮาร์ดแวร์อาจมีผล

### Q3: มีเวอร์ชันทดลองใช้งานหรือไม่?
A3: มี คุณสามารถรับเวอร์ชันทดลองฟรี [ที่นี่](https://releases.aspose.com/)

### Q4: ฉันจะขอรับลิขสิทธิ์ชั่วคราวได้อย่างไร?
A4: สามารถขอรับลิขสิทธิ์ชั่วคราวได้ [ที่นี่](https://purchase.aspose.com/temporary-license/)

### Q5: ฉันจะหาความช่วยเหลือได้จากที่ไหนหากเจอปัญหา?
A5: คุณสามารถเยี่ยมชมฟอรั่ม Aspose.CAD [ที่นี่](https://forum.aspose.com/c/cad/19) เพื่อรับการสนับสนุน

**Q: จะตั้งค่าเมตาดาต้า PDF เพิ่มเติม (author, title, ฯลฯ) อย่างไร?**  
A: ใช้คุณสมบัติ `exportOptions.Metadata` ก่อนเรียก `Save`

**Q: สามารถส่งออกหลาย layout ไปยังหน้า PDF แยกกันได้หรือไม่?**  
A: ได้ – ตั้งค่า `Layouts = new string[] { "Layout1", "Layout2" }` ใน `CadRasterizationOptions`

**Q: Aspose.CAD รองรับการแปลง DWG ไปเป็นรูปแบบภาพอื่นหรือไม่?**  
A: แน่นอน คุณสามารถส่งออกเป็น PNG, JPEG, SVG และอื่น ๆ โดยใช้ overload ของ `Image.Save` ที่สอดคล้องกัน

---

**อัปเดตล่าสุด:** 2026-03-21  
**ทดสอบกับ:** Aspose.CAD 24.11 for .NET  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}