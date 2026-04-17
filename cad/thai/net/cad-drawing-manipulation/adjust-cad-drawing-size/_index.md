---
date: 2026-03-19
description: เรียนรู้วิธีปรับขนาดภาพวาด CAD ใน .NET ด้วย Aspose.CAD รวมถึงวิธีสเกลหน่วยของภาพวาด
  CAD และปรับขนาดเลย์เอาต์ ตามคู่มือขั้นตอนของเรา.
linktitle: Adjusting CAD Drawing Size
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: วิธีปรับขนาดภาพวาด CAD ด้วย Aspose.CAD สำหรับ .NET
url: /th/net/cad-drawing-manipulation/adjust-cad-drawing-size/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีปรับขนาดการวาด CAD ด้วย Aspose.CAD สำหรับ .NET

## บทนำ

หากคุณต้องการ **how to resize CAD** ไฟล์โดยตรงจากแอปพลิเคชัน .NET ของคุณ คุณมาถูกที่แล้ว ในบทเรียนนี้เราจะแสดงวิธีเปลี่ยนการตั้งค่า unit ของ CAD, ปรับขนาดมิติการวาด CAD, และปรับขนาด CAD อย่างโปรแกรมโดยใช้ Aspose.CAD สำหรับ .NET เมื่อจบคู่มือคุณจะมีโซลูชันที่พร้อมใช้งานในผลิตภัณฑ์สำหรับการปรับขนาดรูปแบบ CAD ที่รองรับทั้งหมด

## คำตอบสั้น
- **ต้องใช้ไลบรารีอะไร?** Aspose.CAD for .NET  
- **ฉันสามารถเปลี่ยนประเภทหน่วยได้หรือไม่?** Yes – set `UnitType` in `CadRasterizationOptions`  
- **ต้องการใบอนุญาตสำหรับการใช้งานจริงหรือไม่?** A valid Aspose.CAD license is required for non‑trial use  
- **รูปแบบภาพที่ตัวอย่างส่งออกเป็นอะไร?** BMP (but any supported raster format works)  
- **จำนวนบรรทัดของโค้ดเท่าไหร่?** Less than 30 lines for a complete resize operation  

## “how to resize CAD” คืออะไรในทางปฏิบัติ?
การปรับขนาดการวาด CAD หมายถึงการแปลงข้อมูลเวกเตอร์เป็นภาพ raster ที่สเกลหรือหน่วยเฉพาะ (เช่น เซนติเมตร, นิ้ว) ซึ่งมีประโยชน์เมื่อคุณต้องการฝังการวาดลงในรายงาน, สร้างรูปย่อ, หรือรวมภาพ CAD เข้าในหน้าเว็บ

## ทำไมต้องปรับขนาด CAD ด้วย Aspose.CAD?
- **ไม่มีซอฟต์แวร์ CAD ภายนอก** – ทุกอย่างทำงานภายในโค้ด .NET ของคุณ  
- **การควบคุมระดับละเอียด** over units, layouts, and rasterization options.  
- **รองรับหลายรูปแบบ** – โค้ดเดียวทำงานได้กับ DWG, DXF, DWF, และอื่น ๆ  

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเริ่ม ให้ตรวจสอบว่าคุณมี:

- Aspose.CAD for .NET Library: ดาวน์โหลดและติดตั้งไลบรารีจาก [Aspose.CAD for .NET download page](https://releases.aspose.com/cad/net/).  
- Sample CAD Drawing: ไฟล์เช่น `sample.dwg` ที่วางในไดเรกทอรีเอกสารของโปรเจกต์ของคุณ  

## นำเข้า Namespaces

ก่อนอื่น ให้นำเข้า namespaces ที่ให้คุณเข้าถึงคลาสต่าง ๆ ของ Aspose.CAD

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## ขั้นตอนที่ 1: โหลดการวาด CAD

โหลดไฟล์ต้นทางเข้าสู่วัตถุ `Image` วัตถุนี้แทนการวาด CAD ในหน่วยความจำและจะเป็นพื้นฐานสำหรับการดำเนินการต่อไปทั้งหมด

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "sample.dwg";

// Load a CAD drawing in an instance of Image
using (var image = Aspose.CAD.Image.Load(sourceFilePath))
{
    // Your code here...
}
```

## ขั้นตอนที่ 2: สร้าง BmpOptions (หรือรูปแบบ raster อื่นใดก็ได้)

`BmpOptions` บอก Aspose.CAD ว่าจะเรนเดอร์ข้อมูลเวกเตอร์อย่างไรเมื่อบันทึกเป็น bitmap คุณสามารถสลับเป็น `PngOptions`, `JpegOptions` ฯลฯ ตามรูปแบบเป้าหมายที่ต้องการ

```csharp
Aspose.CAD.ImageOptions.BmpOptions bmpOptions = new Aspose.CAD.ImageOptions.BmpOptions();
```

## ขั้นตอนที่ 3: ตั้งค่า CadRasterizationOptions

`CadRasterizationOptions` เก็บการตั้งค่าหลักสำหรับการสเกล, การแปลงหน่วย, และการเลือก layout การเชื่อมโยงกับ property `VectorRasterizationOptions` ของ `BmpOptions` ทำให้ rasterizer ใช้การตั้งค่าที่กำหนดเองของคุณ

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions cadRasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
bmpOptions.VectorRasterizationOptions = cadRasterizationOptions;
```

## ขั้นตอนที่ 4: ตั้งค่า UnitType (เปลี่ยนหน่วย CAD)

ที่นี่เราจะเปลี่ยนหน่วย CAD จากค่าเริ่มต้นเป็นเซนติเมตร นี่คือจุดที่คีย์เวิร์ด **change cad unit** ปรากฏและมีผลโดยตรงต่อขนาดภาพสุดท้าย

```csharp
cadRasterizationOptions.UnitType = Aspose.CAD.ImageOptions.UnitType.Centimeter;
```

## ขั้นตอนที่ 5: เลือก Layouts (ตั้งค่า CAD layouts)

หากการวาดของคุณมีหลาย layout (เช่น Model, Sheet1) ให้ระบุว่า layout ใดที่ต้องการ rasterize การเลือก layout ที่ถูกต้องเป็นสิ่งสำคัญเมื่อคุณ **set cad layouts** สำหรับผลลัพธ์ที่ปรับขนาดแล้ว

```csharp
cadRasterizationOptions.Layouts = new string[] { "Model" };
```

## ขั้นตอนที่ 6: ส่งออกเป็น BMP (ปรับขนาดการวาด CAD)

สุดท้ายบันทึกภาพที่ rasterized ไฟล์ผลลัพธ์จะแสดงขนาด, หน่วย, และ layout ใหม่ที่คุณกำหนด – เสร็จสิ้นการดำเนินการ **resize CAD drawing**

```csharp
string outPath = sourceFilePath + ".bmp";
image.Save(outPath, bmpOptions);
```

คุณจะได้ไฟล์ BMP ที่เป็นตัวแทนของการวาด CAD ที่ปรับขนาดแล้ว พร้อมสำหรับการประมวลผลหรือแสดงต่อไป

## ปัญหาที่พบบ่อยและวิธีแก้ไข

| ปัญหา | สาเหตุ | วิธีแก้ |
|-------|--------|----------|
| ผลลัพธ์เบลอ | ค่า DPI ต่ำ (จุดต่อนิ้ว) เป็นค่าเริ่มต้น | ตั้งค่า `cadRasterizationOptions.Resolution = 300;` ก่อนบันทึก |
| แสดง Layout ผิด | ชื่อ Layout พิมพ์ผิด | ตรวจสอบชื่อ Layout ที่ถูกต้องโดยใช้ CAD viewer หรือคอลเลกชัน `Layouts` |
| การแปลงหน่วยดูไม่ตรง | ผสมหน่วยเมตริกและอิมพีเรียล | ตรวจสอบให้แน่ใจว่า `UnitType` ตรงกับระบบการวัดที่ต้องการ |

## คำถามที่พบบ่อย

### Q1: Aspose.CAD สำหรับ .NET รองรับรูปแบบ CAD ทั้งหมดหรือไม่?
**A1:** Aspose.CAD for .NET รองรับรูปแบบ CAD มากมาย รวมถึง DWG, DXF, DWF และอื่น ๆ ตรวจสอบ [documentation](https://reference.aspose.com/cad/net/) เพื่อดูรายการทั้งหมด

### Q2: ฉันสามารถปรับขนาดหลาย layout พร้อมกันได้หรือไม่?
**A2:** ได้ คุณสามารถปรับขนาดหลาย layout ได้โดยปรับอาร์เรย์ `Layouts` ใน `CadRasterizationOptions`

### Q3: ฉันจะหาแหล่งสนับสนุนสำหรับ Aspose.CAD สำหรับ .NET ได้จากที่ไหน?
**A3:** เยี่ยมชม [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) เพื่อรับการสนับสนุนจากชุมชนและความช่วยเหลือ

### Q4: มีการทดลองใช้ฟรีหรือไม่?
**A4:** มี คุณสามารถสำรวจ [free trial](https://releases.aspose.com/) เพื่อประเมินคุณสมบัติของ Aspose.CAD สำหรับ .NET

### Q5: ฉันจะขอรับใบอนุญาตชั่วคราวสำหรับ Aspose.CAD สำหรับ .NET ได้อย่างไร?
**A5:** รับใบอนุญาตชั่วคราวสำหรับการทดสอบได้ที่ [here](https://purchase.aspose.com/temporary-license/)

## Frequently Asked Questions

**Q: ฉันจะสเกลการวาด CAD โดยไม่เปลี่ยนประเภทหน่วยได้อย่างไร?**  
**A:** ปรับ property `Zoom` ของ `CadRasterizationOptions` (เช่น `cadRasterizationOptions.Zoom = 2.0;`) เพื่อเพิ่มขนาดเป็นสองเท่าโดยคงหน่วยเดิม

**Q: ฉันสามารถส่งออกเป็นรูปแบบอื่นนอกจาก BMP ได้หรือไม่?**  
**A:** แน่นอน แค่เปลี่ยน `BmpOptions` เป็น `PngOptions`, `JpegOptions` หรือคลาส raster format ที่รองรับอื่น ๆ

**Q: สามารถประมวลผลหลายไฟล์ในโฟลเดอร์พร้อมกันได้หรือไม่?**  
**A:** ได้ ลูปผ่านไฟล์ในไดเรกทอรี ใช้ตรรกะ rasterization เดียวกัน แล้วบันทึกแต่ละผลลัพธ์ด้วยชื่อที่ไม่ซ้ำกัน

---

**อัปเดตล่าสุด:** 2026-03-19  
**ทดสอบด้วย:** Aspose.CAD for .NET 24.11 (latest at time of writing)  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}