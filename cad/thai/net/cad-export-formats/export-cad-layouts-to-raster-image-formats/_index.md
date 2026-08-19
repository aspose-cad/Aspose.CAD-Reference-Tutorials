---
date: 2026-03-21
description: เรียนรู้วิธีแปลงไฟล์ DXF เป็น PNG และรูปแบบเรสเตอร์อื่น ๆ ด้วย Aspose.CAD
  สำหรับ .NET. ปฏิบัติตามคู่มือขั้นตอนต่อขั้นตอนของเราเพื่อการส่งออกชั้น CAD อย่างราบรื่น.
linktitle: Export CAD Layouts to Raster Image Formats
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: แปลง DXF เป็น PNG ด้วย Aspose.CAD สำหรับ .NET
url: /th/net/cad-export-formats/export-cad-layouts-to-raster-image-formats/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ส่งออกเค้าโครง CAD เป็นรูปแบบภาพเรสเตอร์ใน Aspose.CAD สำหรับ .NET

## คำแนะนำ

คุณกำลังมองหาวิธี **convert dxf to png** อย่างมีประสิทธิภาพและรูปแบบภาพเรสเตอร์อื่น ๆ ด้วย Aspose.CAD สำหรับ .NET หรือไม่? คู่มือขั้นตอนต่อขั้นตอนนี้จะพาคุณผ่านกระบวนการทั้งหมด พร้อมคำแนะนำโดยละเอียดและโค้ดตัวอย่างเพื่อให้การทำงานเป็นไปอย่างราบรื่น ไม่ว่าคุณจะเป็นนักพัฒนาที่มีประสบการณ์หรือเพิ่งเริ่มต้นกับ Aspose.CAD คู่มือนี้เหมาะกับทุกระดับความเชี่ยวชาญ

### คำตอบอย่างรวดเร็ว
- **ไลบรารีที่จัดการการแปลงคืออะไร?** Aspose.CAD for .NET  
- **รูปแบบหลักที่สนับสนุนโดยตรงคืออะไร?** JPEG, PNG, BMP, และ TIFF raster images  
- **ฉันสามารถส่งออกชั้น CAD เฉพาะได้หรือไม่?** ใช่ – ใช้ `CadRasterizationOptions.Layers` เพื่อกำหนดเป้าหมายแต่ละชั้น  
- **ฉันต้องการใบอนุญาตสำหรับการใช้งานจริงหรือไม่?** จำเป็นต้องมีใบอนุญาต Aspose.CAD ที่ถูกต้องสำหรับการใช้งานที่ไม่ใช่รุ่นทดลอง  
- **เวอร์ชัน .NET ที่รองรับ?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7  

## **convert dxf to png** คืออะไร?

การแปลงไฟล์ DXF (Drawing Exchange Format) เป็น PNG หมายถึงการทำให้ข้อมูล CAD ที่เป็นเวกเตอร์กลายเป็นภาพพิกเซล การทำเช่นนี้มีประโยชน์เมื่อคุณต้องการฝังภาพวาด CAD ลงในหน้าเว็บ รายงาน หรือสภาพแวดล้อมใด ๆ ที่รองรับเฉพาะกราฟิกเรสเตอร์เท่านั้น

## ทำไมต้องส่งออกชั้น CAD แยกกัน?

การส่งออกชั้น CAD แยกกันช่วยให้คุณควบคุมผลลัพธ์ภาพได้อย่างละเอียด ลดขนาดไฟล์ของแต่ละภาพ และทำให้คุณสามารถปรับสไตล์หรือทำการประมวลผลต่อเนื่องตามชั้นได้ การทำเช่นนี้เป็นประโยชน์อย่างยิ่งสำหรับภาพวาดวิศวกรรมขนาดใหญ่ที่มีเพียงบางชั้นเท่านั้นที่เกี่ยวข้องกับผู้ชมเฉพาะกลุ่ม

## ข้อกำหนดเบื้องต้น

ก่อนเริ่มทำตามบทเรียนนี้ โปรดตรวจสอบว่าคุณมีสิ่งต่อไปนี้พร้อมแล้ว:

- **Aspose.CAD for .NET Library** – ดาวน์โหลดจาก [Aspose.CAD website](https://releases.aspose.com/cad/net/)  
- **ไฟล์วาด CAD** – ไฟล์ DXF (เช่น `conic_pyramid.dxf`) ที่คุณต้องการแปลงเป็นรูปแบบเรสเตอร์  

## นำเข้า Namespaces

ในโปรเจกต์ .NET ของคุณ ให้นำเข้า namespaces ที่จำเป็นเพื่อใช้ฟังก์ชันของ Aspose.CAD รวม namespaces ต่อไปนี้ที่ส่วนเริ่มต้นของโค้ดของคุณ:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## วิธี **convert dxf to png** – คู่มือขั้นตอนต่อขั้นตอน

### ขั้นตอนที่ 1: โหลดภาพวาด CAD

ก่อนอื่น โหลดไฟล์ DXF เข้าไปในอ็อบเจกต์ `Image` ซึ่งอ็อบเจกต์นี้แทนภาพวาด CAD ทั้งหมดในหน่วยความจำ

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

// Load a CAD drawing in an instance of Image
using (var image = Image.Load(sourceFilePath))
{
    // Your code for loading the CAD drawing goes here
}
```

### ขั้นตอนที่ 2: สร้าง `CadRasterizationOptions`

กำหนดค่าการเรสเตอร์ไลซ์ เช่น ขนาดเอาต์พุตและความละเอียด ตัวเลือกเหล่านี้จะควบคุมวิธีการแปลงข้อมูลเวกเตอร์เป็นพิกเซล

```csharp
// Create an instance of CadRasterizationOptions
var rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
```

### ขั้นตอนที่ 3: ระบุชั้น (ส่งออกชั้น CAD)

หากคุณต้องการเพียงชั้นใดชั้นหนึ่ง ให้ระบุชื่อชั้นที่นี่ ตัวอย่างนี้แสดงการ **export cad layers** แยกตามชั้น

```csharp
// Add the layer name to the CadRasterizationOptions's layer list
rasterizationOptions.Layers = new string[] { "LayerA" };
```

### ขั้นตอนที่ 4: เลือกรูปแบบภาพ – บันทึก CAD เป็น PNG (หรือ JPEG)

สร้างอ็อบเจกต์ตัวเลือกเฉพาะรูปแบบภาพ แทนที่ `JpegOptions` ด้วย `PngOptions` เมื่อคุณต้องการ **save cad as png**

```csharp
// Create an instance of JpegOptions (or any ImageOptions for raster formats)
var options = new JpegOptions();
options.VectorRasterizationOptions = rasterizationOptions;
```

> **Pro tip:** เพื่อสร้างไฟล์ PNG เพียงแค่สร้าง `new PngOptions()` แทน `JpegOptions`

### ขั้นตอนที่ 5: ส่งออกเป็นรูปแบบ JPEG (หรือ PNG)

สุดท้าย ให้บันทึกภาพที่เรสเตอร์ไลซ์ลงดิสก์ ส่วนขยายไฟล์จะกำหนดรูปแบบเอาต์พุตโดยอัตโนมัติ

```csharp
// Export each layer to Jpeg format
MyDir = MyDir + "CADLayersToRasterImageFormats_out.jpg";
image.Save(MyDir, options);
```

เมื่อคุณเปลี่ยนจาก `JpegOptions` เป็น `PngOptions` โค้ดเดียวกันนี้จะ **convert dxf to png** และสร้างไฟล์ `.png`

### ขั้นตอนเพิ่มเติม: แปลงทุกชั้น

หากคุณต้องการ **convert cad to raster** สำหรับทุกชั้นในภาพวาด ให้เรียกใช้เมธอดช่วยเหลือด้านล่าง ซึ่งจะวนลูปผ่านทุกชั้นและบันทึกแต่ละชั้นเป็นภาพแยกกัน

```csharp
ConvertAllLayersToRasterImageFormats();
```

> *Note:* การทำงานของ `ConvertAllLayersToRasterImageFormats` เป็นส่วนหนึ่งของชุดตัวอย่างเต็มของ Aspose.CAD และแสดงการประมวลผลแบบแบตช์ของชั้นต่าง ๆ

## ปัญหาที่พบบ่อยและการแก้ไขปัญหา

| อาการ | สาเหตุที่เป็นไปได้ | วิธีแก้ |
|---------|--------------|-----|
| ภาพสีขาวหรือสีเปล่า | ไม่ได้ตั้งค่า Rasterization options (เช่น `PageWidth`/`PageHeight` = 0) | ตรวจสอบให้แน่ใจว่า `PageWidth` และ `PageHeight` มีค่าบวก |
| ไม่มีชั้น | ชื่อชั้นไม่ถูกต้องในอาร์เรย์ `Layers` | ตรวจสอบชื่อชั้นที่แน่นอนในไฟล์ CAD (แยกแยะตัวพิมพ์ใหญ่‑เล็ก) |
| PNG คุณภาพต่ำ | ค่า DPI เริ่มต้นต่ำ | ตั้งค่า `rasterizationOptions.Resolution = 300;` เพื่อคุณภาพที่สูงขึ้น |

## คำถามที่พบบ่อย (Original)

### Q1: ฉันสามารถใช้รูปแบบภาพอื่นสำหรับการส่งออกได้หรือไม่?
A1: ใช่, คุณทำได้ เพียงแทนที่ `JpegOptions` ด้วยตัวเลือกของรูปแบบที่ต้องการ เช่น `PngOptions` หรือ `BmpOptions`.

### Q2: มีเวอร์ชันทดลองหรือไม่?
A2: ใช่, คุณสามารถสำรวจฟังก์ชันของ Aspose.CAD ได้โดยดาวน์โหลดเวอร์ชันทดลอง [ที่นี่](https://releases.aspose.com/).

### Q3: ฉันจะรับการสนับสนุนสำหรับ Aspose.CAD ได้อย่างไร?
A3: เยี่ยมชม [forum](https://forum.aspose.com/c/cad/19) ของ Aspose.CAD เพื่อรับการสนับสนุนจากชุมชน หรือพิจารณาซื้อใบอนุญาตเพื่อรับการสนับสนุนโดยตรง

### Q4: มีใบอนุญาตชั่วคราวหรือไม่?
A4: มี, คุณสามารถรับใบอนุญาตชั่วคราว [ที่นี่](https://purchase.aspose.com/temporary-license/).

### Q5: ฉันสามารถหาเอกสารได้จากที่ไหน?
A5: ดูเอกสารโดยละเอียด [ที่นี่](https://reference.aspose.com/cad/net/).

## คำถามเพิ่มเติม

**Q: ฉันสามารถส่งออกทุกชั้นในคำสั่งเดียวได้หรือไม่?**  
A: ใช่, ใช้เมธอด `ConvertAllLayersToRasterImageFormats` ที่แสดงด้านบน

**Q: Aspose.CAD รองรับรูปแบบเวกเตอร์เช่น SVG หรือไม่?**  
A: มันมุ่งเน้นที่รูปแบบเรสเตอร์เป็นหลัก แต่คุณสามารถส่งออกเป็น PDF ที่ยังคงรักษาข้อมูลเวกเตอร์ได้

**Q: ฉันจะควบคุมสีพื้นหลังของ PNG ที่ส่งออกได้อย่างไร?**  
A: ตั้งค่า `rasterizationOptions.BackgroundColor` เป็น `Color` ที่ต้องการก่อนบันทึก

**Q: สามารถส่งออกเฉพาะเลย์เอาต์เดียวแทนการส่งออกทั้งหมดได้หรือไม่?**  
A: ได้, ตั้งค่า `rasterizationOptions.Layouts` เพื่อระบุชื่อเลย์เอาต์ที่ต้องการเรสเตอร์ไลซ์

## สรุป

คุณได้เรียนรู้วิธี **convert dxf to png**, **export cad layers**, และ **save cad as png** หรือ JPEG ด้วย Aspose.CAD สำหรับ .NET โดยการปรับ `CadRasterizationOptions` และสลับตัวเลือกรูปแบบภาพ คุณสามารถปรับแต่งการแปลงให้ตรงกับความต้องการของรูปแบบเรสเตอร์ใด ๆ ที่ต้องการได้ สำรวจตัวเลือกรูปแบบอื่น ๆ ใน Aspose.CAD API เพื่อขยายการทำงาน CAD‑to‑raster ของคุณต่อไป

---

**Last Updated:** 2026-03-21  
**Tested With:** Aspose.CAD for .NET 24.11 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}