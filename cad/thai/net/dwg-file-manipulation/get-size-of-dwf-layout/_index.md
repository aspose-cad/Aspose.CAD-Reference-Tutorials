---
date: 2026-04-06
description: เรียนรู้วิธีแปลง DWF เป็น JPG ใน C# ด้วย Aspose.CAD และค้นพบวิธีดึงขนาดเลย์เอาต์
  DWF จากไฟล์ DWG.
keywords:
- convert dwf to jpg
- how to extract dwf
- convert dwg to jpg
linktitle: ทำงานกับไฟล์ DWG ใน C# - รับขนาดของเลย์เอาต์ DWF
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: แปลง DWF เป็น JPG ด้วย C# – รับขนาด Layout ของ DWF จาก DWG
url: /th/net/dwg-file-manipulation/get-size-of-dwf-layout/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# แปลง DWF เป็น JPG ใน C# – รับขนาด Layout ของ DWF จาก DWG

## บทนำ

หากคุณต้องการ **แปลง DWF เป็น JPG** พร้อมกับหาขนาด Layout ที่แม่นยำ คุณมาถูกที่แล้ว ในบทเรียนนี้เราจะพาคุณผ่านตัวอย่างครบวงจรจากต้นจนจบโดยใช้ Aspose.CAD for .NET เพื่อเปิดไฟล์ DWF ที่ได้มาจาก DWG, อ่านขนาดของแต่ละ Layout, และบันทึก Layout เป็นภาพ JPG คุณภาพสูง เมื่อเสร็จคุณจะไม่เพียงรู้วิธีดึงข้อมูล Layout ของ DWF เท่านั้น แต่ยังมีโค้ดสแนปช็อตที่นำไปใช้ได้ในโปรเจกต์ C# ใด ๆ

## คำตอบสั้น
- **“แปลง DWF เป็น JPG” หมายความว่าอย่างไร?** หมายถึงการแรสเตอร์ไลซ์ Layout เวกเตอร์ DWF ให้เป็นภาพบิตแมพ JPEG  
- **ทำไมต้องอ่านขนาด Layout ก่อน?** การรู้ขอบเขตที่แน่นอนช่วยให้ตั้งค่าขนาดหน้าที่ถูกต้อง หลีกเลี่ยงการยืดหรือคลิปภาพออกมา  
- **ไลบรารีใดจัดการเรื่องนี้?** Aspose.CAD for .NET ให้การสนับสนุนเต็มรูปแบบสำหรับ DWG, DWF และการแปลงเป็นภาพแรสเตอร์  
- **ต้องมีไลเซนส์หรือไม่?** ไลเซนส์ชั่วคราวใช้ได้สำหรับการประเมินผล; ไลเซนส์เต็มจำเป็นสำหรับการใช้งานในโปรดักชัน  
- **เวอร์ชัน .NET ที่รองรับคืออะไร?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7

## “แปลง DWF เป็น JPG” คืออะไรและทำไมจึงสำคัญ?

การแปลงไฟล์ DWF (Design Web Format) เป็น JPG สร้างภาพพกพาที่สามารถแสดงในเบราว์เซอร์ ฝังในรายงาน หรือแชร์กับผู้มีส่วนได้ส่วนเสียที่ไม่มีซอฟต์แวร์ CAD การแปลงนี้ยังให้ความยืดหยุ่นในการจัดการภาพ (ปรับขนาด, บีบอัด, ใส่ลายน้ำ) ด้วยเครื่องมือประมวลผลภาพมาตรฐาน

## ทำไมต้องดึงขนาด Layout ของ DWF?

ไฟล์ DWF สามารถมีหลาย Layout แต่ละ Layout มีระบบพิกัดและหน่วยของตนเอง (นิ้ว, มิลลิเมตร ฯลฯ) การดึงขนาด Layout ช่วยให้คุณ:

1. รักษาอัตราส่วนเดิมเมื่อทำการแรสเตอร์ไลซ์  
2. เลือก DPI ที่เหมาะสมสำหรับผลลัพธ์ความละเอียดสูง  
3. ทำการประมวลผลหลาย Layout อัตโนมัติโดยไม่ต้องปรับด้วยมือ  

## ข้อกำหนดเบื้องต้น

เพื่อทำตามบทเรียนนี้อย่างราบรื่น โปรดตรวจสอบว่าคุณมีสิ่งต่อไปนี้พร้อมใช้งาน:

- Aspose.CAD for .NET: ตรวจสอบว่าคุณได้ติดตั้ง Aspose.CAD for .NET แล้ว คุณสามารถดาวน์โหลดได้จาก [Aspose.CAD for .NET download page](https://releases.aspose.com/cad/net/)

การมีไลบรารีพร้อมหมายความว่าคุณสามารถมุ่งเน้นที่โค้ดได้โดยไม่ต้องตามหา dependencies

## นำเข้า Namespaces

ก่อนเริ่มเขียนโค้ด ให้นำเข้า Namespaces ที่จำเป็น ซึ่งจะให้คลาสที่ต้องใช้สำหรับทำงานกับไฟล์ CAD, ตัวเลือกการแรสเตอร์ไลซ์, และการทำ I/O ของไฟล์

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Dwf;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

## ขั้นตอนที่ 1: ตั้งค่าสภาพแวดล้อมของคุณ

สร้างโปรเจกต์คอนโซลหรือคลาส‑ไลบรารี C# ใหม่ เพิ่มการอ้างอิงไปยัง **Aspose.CAD.dll** และตรวจสอบว่าโปรเจกต์ตั้งค่าเป้าหมายเป็นเวอร์ชัน .NET ที่เข้ากันได้

## ขั้นตอนที่ 2: กำหนดเส้นทางไฟล์ (วิธีดึง DWF)

ระบุตำแหน่งที่ไฟล์ DWF ต้นฉบับอยู่และที่ที่ไฟล์ JPG ที่สร้างขึ้นจะถูกเขียนออกไป

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "blocks_and_tables.dwf";
```

> **เคล็ดลับ:** ใช้ `Path.Combine(MyDir, "blocks_and_tables.dwf")` เพื่อจัดการเส้นทางอย่างปลอดภัยบนระบบปฏิบัติการต่าง ๆ

## ขั้นตอนที่ 3: โหลดภาพ DWF

โหลดไฟล์ DWF เข้าไปในอ็อบเจ็กต์ `Aspose.CAD.Image` เราจะทำการคาสท์เป็น `DwfImage` เพื่อเข้าถึงคุณสมบัติเฉพาะของหน้า

```csharp
using (DwfImage image = (DwfImage)Aspose.CAD.Image.Load(sourceFilePath))
{
    // Code for further steps will go here
}
```

## ขั้นตอนที่ 4: วนลูปผ่านหน้า

DWF สามารถมีหลายหน้า (Layout) ลูปผ่านแต่ละหน้าเพื่อประมวลผลแยกกัน

```csharp
foreach (var page in image.Pages)
{
    // Code for further steps will go here
}
```

## ขั้นตอนที่ 5: รับข้อมูล Layout

ภายในลูป ดึงชื่อ Layout ชื่อนี้จะใช้ทั้งสำหรับบันทึกล็อกและตั้งชื่อไฟล์ JPG ที่จะสร้าง

```csharp
var layout = page.Name;
System.Console.WriteLine("Layout= " + layout);
```

## ขั้นตอนที่ 6: ตั้งค่า JPG Options

สร้างอินสแตนซ์ `JpegOptions` และกำหนดตัวเลือกการแรสเตอร์ไลซ์ property `Layouts` จะบอก Aspose.CAD ว่าจะเรนเดอร์ Layout ใด

```csharp
using (FileStream fs = new FileStream(MyDir + "layout_" + layout + ".jpg", FileMode.Create))
{
    JpegOptions jpegOptions = new JpegOptions();
    CadRasterizationOptions options = new CadRasterizationOptions();
    options.Layouts = new string[] { layout };
    // Code for further steps will go here
}
```

## ขั้นตอนที่ 7: กำหนดขนาดหน้า (แปลง dwg เป็น jpg)

คำนวณความกว้างและความสูงของ Layout ในหน่วยดั้งเดิม ข้อมูลนี้สำคัญสำหรับการตั้งค่าขนาดหน้าการแรสเตอร์อย่างถูกต้อง

```csharp
double sizeExtX = page.MaxPoint.X - page.MinPoint.X;
double sizeExtY = page.MaxPoint.Y - page.MinPoint.Y;
// Code for further steps will go here
```

## ขั้นตอนที่ 8: ตั้งค่าขนาดหน้า

แปลงหน่วยดั้งเดิม (นิ้วหรือมิลลิเมตร) เป็นพิกเซลโดยใช้เมธอดช่วยของ Aspose.CAD หากประเภทหน่วยไม่ใช่สองแบบนี้ เราจะใช้ค่าดิบเป็นค่าเริ่มต้น

```csharp
if (page.UnitType == UnitType.Inch)
{
    options.PageHeight = CommonHelper.INtoPixels(sizeExtY, CommonHelper.DPI);
    options.PageWidth = CommonHelper.INtoPixels(sizeExtX, CommonHelper.DPI);
}
else if (page.UnitType == UnitType.Millimeter)
{
    options.PageHeight = CommonHelper.MMtoPixels(sizeExtY, CommonHelper.DPI);
    options.PageWidth = CommonHelper.MMtoPixels(sizeExtX, CommonHelper.DPI);
}
else
{
    options.PageHeight = (float)sizeExtY;
    options.PageWidth = (float)sizeExtX;
}
```

## ขั้นตอนที่ 9: บันทึกไฟล์ JPG

สุดท้าย ผูกตัวเลือกการแรสเตอร์ไลซ์เข้ากับ JPEG options แล้วบันทึกภาพลงดิสก์

```csharp
jpegOptions.VectorRasterizationOptions = options;
image.Save(fs, jpegOptions);
}
```

เมื่อวนลูปเสร็จสิ้น คุณจะมีไฟล์ JPG สำหรับแต่ละ Layout โดยแต่ละไฟล์มีขนาดตรงกับมิติของ DWF ดั้งเดิม

## ปัญหาที่พบบ่อยและวิธีแก้

| อาการ | สาเหตุที่เป็นไปได้ | วิธีแก้ |
|---------|--------------|-----|
| ไฟล์ JPG ว่างเปล่า | `options.Layouts` ไม่ได้ตั้งค่าอย่างถูกต้อง | ตรวจสอบให้แน่ใจว่าชื่อ Layout ตรงกับ `page.Name`. |
| ภาพบิดเบี้ยว | การแปลง DPI ผิดพลาด | ใช้ `CommonHelper.DPI = 300` (หรือ DPI ที่ต้องการ) ก่อนทำการแปลง. |
| ไม่พบไฟล์ | เส้นทาง `MyDir` ไม่ถูกต้อง | ใช้เส้นทางแบบเต็มหรือ `Path.Combine`. |
| ข้อยกเว้นใบอนุญาต | ไม่ได้โหลดใบอนุญาต | โหลดใบอนุญาตชั่วคราวหรือถาวรก่อนเรียก `Image.Load`. |

## คำถามที่พบบ่อย

### Q1: Aspose.CAD รองรับรูปแบบไฟล์ DWG ล่าสุดหรือไม่?

A1: Aspose.CAD รองรับรูปแบบไฟล์ DWG ต่าง ๆ รวมถึงเวอร์ชันล่าสุด ดูรายละเอียดความเข้ากันได้ใน [documentation](https://reference.aspose.com/cad/net/)

### Q2: สามารถใช้ Aspose.CAD สำหรับโครงการเชิงพาณิชย์และส่วนบุคคลได้หรือไม่?

A2: ใช่, Aspose.CAD มีตัวเลือกการให้ลิขสิทธิ์ที่ยืดหยุ่นสำหรับการใช้งานเชิงพาณิชย์และส่วนบุคคล เยี่ยมชม [purchase page](https://purchase.aspose.com/buy) เพื่อดูรายละเอียด

### Q3: จะขอรับไลเซนส์ชั่วคราวสำหรับ Aspose.CAD ได้อย่างไร?

A3: คุณสามารถรับไลเซนส์ชั่วคราวได้จาก [here](https://purchase.aspose.com/temporary-license/) เพื่อการประเมินผล

### Q4: จะหาการสนับสนุนสำหรับ Aspose.CAD ได้จากที่ไหน?

A4: สำหรับคำถามหรือความช่วยเหลือใด ๆ เยี่ยมชม [Aspose.CAD forum](https://forum.aspose.com/c/cad/19)

### Q5: มีเวอร์ชันทดลองใช้ฟรีสำหรับ Aspose.CAD หรือไม่?

A5: มี, คุณสามารถเข้าถึงเวอร์ชันทดลองฟรีของ Aspose.CAD ได้ [here](https://releases.aspose.com/)

### Q6: จะทำอย่างไรให้แปลงไฟล์ DWG เป็น JPG โดยตรงโดยไม่ต้องดึง DWF ก่อน?

A6: คุณสามารถโหลดไฟล์ DWG ด้วย `Aspose.CAD.Image.Load` แล้วใช้กระบวนการแรสเตอร์ไลซ์เดียวกัน; เพียงตั้งค่า `options.Layouts` ให้เป็นชื่อ Layout ที่ต้องการจาก DWG

### Q7: การแปลงนี้รักษาคุณภาพเวกเตอร์ไว้หรือไม่?

A7: หลังจากแรสเตอร์ไลซ์เป็น JPG ภาพจะเป็นบิตแมพ จึงสูญเสียความสามารถในการสเกลแบบเวกเตอร์ หากต้องการสเกลโดยไม่มีการสูญเสียคุณภาพ ควรส่งออกเป็น PNG หรือ SVG แทน

---

**อัปเดตล่าสุด:** 2026-04-06  
**ทดสอบด้วย:** Aspose.CAD 24.11 for .NET  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}