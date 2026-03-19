---
date: 2026-03-19
description: เรียนรู้วิธีแปลง CAD เป็น PNG ใน .NET ด้วย Aspose.CAD, บันทึก CAD เป็น
  PNG อย่างมีประสิทธิภาพ, และทำให้กระบวนการทำงานกับภาพราสเตอร์ของคุณเป็นระเบียบและรวดเร็วขึ้น.
linktitle: Convert CAD Drawing to Raster Image
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: แปลง CAD เป็น PNG ใน Aspose.CAD สำหรับ .NET
url: /th/net/cad-drawing-manipulation/convert-cad-drawing-to-raster-image/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# แปลง CAD เป็น PNG ด้วย Aspose.CAD สำหรับ .NET

## บทนำ

ในแอปพลิเคชันที่เน้น CAD สมัยใหม่ การ **แปลง CAD เป็น PNG** เป็นความต้องการทั่วไป—ไม่ว่าจะต้องการสร้างภาพย่อ ฝังแบบวาดในหน้าเว็บ หรือเก็บบันทึกการออกแบบเป็นภาพเรสเตอร์ บทเรียนนี้จะพาคุณผ่านกระบวนการเต็มรูปแบบของการแปลงแบบ CAD (DXF, DWG ฯลฯ) ไปเป็นไฟล์ PNG คุณภาพสูงโดยใช้ไลบรารี Aspose.CAD สำหรับ .NET เมื่อเสร็จสิ้น คุณจะสามารถ **บันทึก CAD เป็น PNG** พร้อมการควบคุมเต็มที่ของการตั้งค่าการเรสเตอร์ไลซ์ ทำให้กระบวนการทำงานของคุณเร็วขึ้นและเชื่อถือได้มากขึ้น.

## คำตอบสั้น

- **ไลบรารีที่ดีที่สุดสำหรับการแปลง CAD‑to‑PNG คืออะไร?** Aspose.CAD for .NET.  
- **รูปแบบไฟล์ใดบ้างที่สามารถส่งออกเป็น PNG?** DWG, DXF, DGN and other supported CAD formats.  
- **ฉันต้องใช้ไลเซนส์สำหรับการใช้งานในผลิตภัณฑ์หรือไม่?** Yes, a commercial license is required; a free trial is available.  
- **ฉันสามารถปรับขนาดและคุณภาพของภาพได้หรือไม่?** Absolutely—rasterization options let you set page width, height, background color, and more.  
- **โค้ดนี้เข้ากันได้กับ .NET Core / .NET 6 หรือไม่?** Yes, the same API works across .NET Framework, .NET Core, and .NET 5/6.

## “การแปลง CAD เป็น PNG” คืออะไร?

การแปลง CAD เป็น PNG หมายถึงการเรสเตอร์ไลซ์แบบวาด CAD ที่เป็นเวกเตอร์ให้เป็นรูปแบบภาพพิกเซล (PNG) กระบวนการนี้รักษาความถูกต้องของภาพไว้ในขณะที่ทำให้ไฟล์ง่ายต่อการแสดงผลในเบราว์เซอร์ แอปมือถือ หรือสภาพแวดล้อมใด ๆ ที่ไม่รองรับรูปแบบ CAD โดยตรง.

## ทำไมต้องใช้ Aspose.CAD เพื่อแปลง CAD เป็น PNG?

- **ไม่มีการพึ่งพาภายนอก** – .NET แท้ ๆ ไม่ต้องใช้เอนจิน CAD แบบเนทีฟ  
- **รองรับรูปแบบเต็ม** – จัดการ DWG, DXF, DGN และอื่น ๆ  
- **การควบคุมการเรสเตอร์ไลซ์ละเอียด** – ขนาดหน้า ความละเอียด พื้นหลัง ความหนาของเส้น ฯลฯ  
- **ประสิทธิภาพสูง** – ปรับให้เหมาะกับการประมวลผลแบบแบตช์บนเซิร์ฟเวอร์  

## ข้อกำหนดเบื้องต้น

ก่อนเริ่มต้น ให้แน่ใจว่าคุณมี:

1. **Aspose.CAD for .NET** – ดาวน์โหลดจาก [download page](https://releases.aspose.com/cad/net/).  
2. IDE ที่เข้ากันได้กับ .NET (Visual Studio, Rider หรือ VS Code) พร้อมโครงการที่ตั้งเป้าหมายเป็น .NET Framework 4.6+ หรือ .NET Core 3.1+.

## นำเข้า Namespaces

ในโครงการ .NET ของคุณ ให้นำเข้า namespaces ที่จำเป็นเพื่อเข้าถึงฟังก์ชันของ Aspose.CAD เพิ่มโค้ดต่อไปนี้ที่ส่วนต้นของไฟล์โค้ดของคุณ:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## คู่มือขั้นตอนต่อขั้นตอน

### ขั้นตอนที่ 1: กำหนดเส้นทางไฟล์

กำหนดไฟล์ CAD ต้นทางและเส้นทาง PNG ปลายทาง แทนที่ตัวแสดงตำแหน่งด้วยไดเรกทอรีจริงบนเครื่องของคุณ.

```csharp
// The path to the documents directory.
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";
```

### ขั้นตอนที่ 2: โหลดแบบ CAD

เปิดไฟล์ CAD ด้วย `Aspose.CAD.Image.Load` ซึ่งจะสร้างการแสดงผลของแบบในหน่วยความจำที่คุณสามารถเรสเตอร์ไลซ์ได้.

```csharp
using (Aspose.CAD.Image image = Aspose.CAD.Image.Load(sourceFilePath))
{
```

### ขั้นตอนที่ 3: กำหนดค่าตัวเลือกการเรสเตอร์ไลซ์  

กำหนดวิธีการแปลงข้อมูลเวกเตอร์เป็นพิกเซล ที่นี่เราตั้งค่าแคนวาสขนาด 1200 × 1200 พิกเซล แต่คุณสามารถปรับ `PageWidth` และ `PageHeight` ให้ตรงกับความต้องการของคุณ (เช่น สำหรับ **convert dwg to png** ที่ DPI เฉพาะ).

```csharp
// Create an instance of CadRasterizationOptions
Aspose.CAD.ImageOptions.CadRasterizationOptions rasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
// Set page width & height
rasterizationOptions.PageWidth = 1200;
rasterizationOptions.PageHeight = 1200;
```

> **เคล็ดลับ:** เพื่อเพิ่มความเร็วการเรนเดอร์สำหรับแบบที่ใหญ่ คุณสามารถตั้งค่า `rasterizationOptions.BackgroundColor` เป็นสีทึบหรือเปิดใช้งาน `rasterizationOptions.DrawType` เพื่อการแปลงเวกเตอร์ที่เร็วขึ้น.

### ขั้นตอนที่ 4: สร้าง PNG Options สำหรับภาพผลลัพธ์  

ห่อหุ้มการตั้งค่าการเรสเตอร์ไลซ์ภายในอ็อบเจกต์ `PngOptions` ซึ่งบอกให้ Aspose.CAD ส่งออกไฟล์ PNG.

```csharp
// Create an instance of PngOptions for the resultant image
ImageOptionsBase options = new Aspose.CAD.ImageOptions.PngOptions();
// Set rasterization options
options.VectorRasterizationOptions = rasterizationOptions;
```

### ขั้นตอนที่ 5: บันทึก PNG ผลลัพธ์  

รวมเส้นทางไดเรกทอรีกับชื่อไฟล์ที่ต้องการและเขียนภาพที่เรสเตอร์ไลซ์ลงดิสก์ ขั้นตอนนี้ **บันทึก CAD เป็น PNG**.

```csharp
MyDir = MyDir + "conic_pyramid_raster_image_out.png";
// Save resultant image
image.Save(MyDir, options);
```

### ขั้นตอนที่ 6: แสดงข้อความสำเร็จ  

ยืนยันว่าการแปลงสำเร็จและแสดงตำแหน่งที่ไฟล์ถูกบันทึก.

```csharp
//ExEnd:ConvertDrawingToRasterImage            
Console.WriteLine("\nCAD drawing converted successfully to raster image format.\nFile saved at " + MyDir);
```

> **หมายเหตุ:** บล็อก `using` จากขั้นตอนที่ 2 จะทำการปล่อยอ็อบเจกต์ `Image` โดยอัตโนมัติ เพื่อให้แน่ใจว่าทรัพยากรทั้งหมดถูกปล่อยออก.

## ปัญหาที่พบบ่อยและวิธีแก้

| ปัญหา | สาเหตุ | วิธีแก้ |
|-------|-------|-----|
| **ผลลัพธ์ PNG ว่าง** | ไม่ได้ตั้งค่าตัวเลือกการเรสเตอร์ไลซ์ (เช่น ขาด `PageWidth`/`PageHeight`). | ตรวจสอบให้แน่ใจว่า `CadRasterizationOptions` กำหนดขนาดแคนวาสที่ไม่เป็นศูนย์. |
| **สีไม่ถูกต้อง** | สีพื้นหลังตั้งค่าเป็นสีขาวโดยค่าเริ่มต้น; แบบต้นฉบับใช้เลเยอร์โปร่งใส. | ตั้งค่า `rasterizationOptions.BackgroundColor = Color.Transparent;` |
| **ความล่าช้าของประสิทธิภาพกับไฟล์ DWG ขนาดใหญ่** | ความละเอียดสูงโดยไม่มีการแบ่งเป็นแผ่น. | ใช้ `rasterizationOptions.LayoutOptions` เพื่อลดพื้นที่การเรนเดอร์หรือปรับ DPI ให้ต่ำลง. |
| **ข้อยกเว้นไลเซนส์** | ทำงานโดยไม่มีไลเซนส์ที่ถูกต้องในสภาพการผลิต. | กำหนดไลเซนส์โดยใช้ `License license = new License(); license.SetLicense("Aspose.CAD.lic");` ก่อนโหลดภาพ. |

## คำถามที่พบบ่อย

### Q1: Aspose.CAD รองรับรูปแบบไฟล์ CAD ทั้งหมดหรือไม่?

A1: Aspose.CAD รองรับรูปแบบไฟล์ CAD หลากหลายรวมถึง DWG, DXF, DGN และอื่น ๆ ดูที่ [documentation](https://reference.aspose.com/cad/net/) เพื่อดูรายการอย่างครบถ้วน.

### Q2: ฉันสามารถปรับแต่งตัวเลือกการเรสเตอร์ไลซ์สำหรับโครงการต่าง ๆ ได้หรือไม่?

A2: ได้, Aspose.CAD อนุญาตให้ปรับแต่งตัวเลือกการเรสเตอร์ไลซ์อย่างละเอียด ทำให้ผู้พัฒนาสามารถปรับผลลัพธ์ให้ตรงตามความต้องการของโครงการ.

### Q3: มีรุ่นทดลองใช้ฟรีสำหรับ Aspose.CAD หรือไม่?

A3: มี, คุณสามารถทดลองใช้คุณสมบัติของ Aspose.CAD ด้วยรุ่นทดลองฟรี เยี่ยมชม [here](https://releases.aspose.com/) เพื่อเริ่มต้น.

### Q4: ฉันจะขอรับการสนับสนุนสำหรับ Aspose.CAD ได้อย่างไร?

A4: สำหรับความช่วยเหลือหรือคำถามใด ๆ ให้เยี่ยมชม [support forum](https://forum.aspose.com/c/cad/19) ของ Aspose.CAD.

### Q5: มีไลเซนส์ชั่วคราวสำหรับ Aspose.CAD หรือไม่?

A5: มี, นักพัฒนาสามารถรับไลเซนส์ชั่วคราวสำหรับ Aspose.CAD ได้จาก [this link](https://purchase.aspose.com/temporary-license/).

### Q6: ฉันสามารถใช้วิธีนี้เพื่อ **แปลง DWG เป็น PNG** ได้หรือไม่?

A6: แน่นอน. โค้ดเดียวกันทำงานกับไฟล์ DWG; เพียงเปลี่ยนนามสกุลไฟล์ต้นทางเป็น `.dwg`.

### Q7: ฉันจะ **ส่งออก DXF เป็นภาพ** พร้อมพื้นหลังโปร่งใสอย่างไร?

A7: ตั้งค่า `rasterizationOptions.BackgroundColor = Color.Transparent;` ก่อนบันทึกเป็น PNG.

---

**อัปเดตล่าสุด:** 2026-03-19  
**ทดสอบกับ:** Aspose.CAD 24.11 for .NET (latest release)  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}