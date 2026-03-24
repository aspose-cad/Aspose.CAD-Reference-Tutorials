---
date: 2026-03-24
description: เรียนรู้วิธีแปลง dgn เป็น png และบันทึก cad เป็น jpeg ด้วย Aspose.CAD
  สำหรับ .NET – คู่มือเร็วสำหรับการแปลง CAD เป็นภาพ
linktitle: Export DGN to Raster Image
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: วิธีแปลง DGN เป็น PNG ใน Aspose.CAD สำหรับ .NET
url: /th/net/cad-export-formats/export-dgn-to-raster-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# แปลง DGN เป็น PNG ใน Aspose.CAD สำหรับ .NET

ในการพัฒนา .NET สมัยใหม่, **convert dgn to png** เป็นความต้องการทั่วไปเมื่อคุณต้องการแสดงภาพวาด CAD บนเว็บหรือฝังไว้ในรายงาน Aspose.CAD สำหรับ .NET ทำให้การแปลงนี้ง่ายดาย โดยให้คุณเปลี่ยนไฟล์ DGN เป็นภาพเรสเตอร์คุณภาพสูงได้ด้วยเพียงไม่กี่บรรทัดของโค้ด ในคู่มือนี้เราจะอธิบายขั้นตอนทั้งหมด ตั้งแต่การตั้งค่าโครงการจนถึงการบันทึกไฟล์ PNG (หรือ JPEG) สุดท้าย

## คำตอบสั้น
- **ฉันสามารถแปลง DGN เป็น PNG ด้วย Aspose.CAD ได้หรือไม่?** ใช่ – เพียงกำหนดค่าตัวเลือกการเรสเตอร์ไลซ์และเลือกผลลัพธ์เป็น PNG หรือ JPEG.  
- **ฉันต้องการไลเซนส์สำหรับการใช้งานในผลิตภัณฑ์หรือไม่?** จำเป็นต้องมีไลเซนส์ Aspose.CAD ที่ถูกต้องสำหรับการใช้งานที่ไม่ใช่รุ่นทดลอง.  
- **เวอร์ชัน .NET ใดที่รองรับ?** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6/7.  
- **รูปแบบภาพใดบ้างที่มีให้ใช้?** PNG, JPEG, BMP, GIF, TIFF, and more.  
- **จำเป็นต้องมีการจัดการข้อยกเว้นหรือไม่?** แน่นอน – ให้ใส่โค้ดการแปลงไว้ใน try/catch เพื่อจัดการกับปัญหาการเข้าถึงไฟล์.

## “convert dgn to png” คืออะไร?
การแปลงไฟล์ DGN (MicroStation) เป็น PNG หมายถึงการเรสเตอร์ไลซ์ข้อมูล CAD เวกเตอร์เป็นภาพแบบพิกเซล ซึ่งเป็นประโยชน์สำหรับการสร้างตัวอย่างภาพ, ฝังภาพวาดในอีเมล HTML, หรือสร้างรูปย่อสำหรับระบบจัดการเอกสาร.

## ทำไมต้องใช้ Aspose.CAD สำหรับการแปลง CAD เป็นภาพ?
- **ไม่มีการพึ่งพาภายนอก** – ทำงานโดยใช้โค้ดที่จัดการโดย .NET เท่านั้น.  
- **ความแม่นยำสูง** – รักษาน้ำหนักเส้น, ชั้น, และสี.  
- **ผลลัพธ์ที่ยืดหยุ่น** – สามารถสลับระหว่าง PNG, JPEG, BMP ฯลฯ ได้โดยการเปลี่ยนตัวเลือกเดียว.  
- **ประสิทธิภาพที่ปรับแต่ง** – การเรสเตอร์ไลซ์ทำได้เร็วแม้กับภาพวาดขนาดใหญ่.

## ข้อกำหนดเบื้องต้น

Before we begin, ensure you have:

- **Aspose.CAD for .NET** ติดตั้งในโครงการของคุณ คุณสามารถดาวน์โหลดได้จาก [website](https://reference.aspose.com/cad/net/).  
- ไฟล์ DGN ตัวอย่าง (เช่น `Nikon_D90_Camera.dgn`) วางไว้ในไดเรกทอรีที่รู้จัก.

## นำเข้า Namespace

Start by adding the required `using` statements so you can access Aspose.CAD classes.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## ขั้นตอนที่ 1: โหลดไฟล์ DGN

Load the source DGN into a `CadImage` object. This object represents the CAD drawing in memory and will be the source for rasterization.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Your code for further processing goes here
}
```

## ขั้นตอนที่ 2: กำหนดตัวเลือกการเรสเตอร์ไลซ์

Configure how the CAD drawing should be rasterized. You can control image size, scaling, and background color here.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 600;
rasterizationOptions.PageHeight = 300;
rasterizationOptions.NoScaling = true;
rasterizationOptions.AutomaticLayoutsScaling = false;
```

## ขั้นตอนที่ 3: เลือกรูปแบบผลลัพธ์ (PNG หรือ JPEG)

Although the tutorial focuses on PNG, you might also want to **save cad as jpeg**. Create the appropriate image options object and attach the rasterization settings.

```csharp
ImageOptionsBase options = new JpegOptions();   // Change to PngOptions() for PNG output
options.VectorRasterizationOptions = rasterizationOptions;
```

> **เคล็ดลับ:** เพื่อสร้างไฟล์ PNG ให้เปลี่ยน `new JpegOptions()` เป็น `new PngOptions()`.

## ขั้นตอนที่ 4: บันทึกภาพเรสเตอร์

Finally, call `Save` on the `CadImage` instance, providing the desired file name and the options object you configured.

```csharp
cadImage.Save(MyDir + "ExportDGNToRasterImage_out.jpg", options);
```

If you switched to `PngOptions`, the file will be saved as `ExportDGNToRasterImage_out.png`.

## ปัญหาทั่วไปและวิธีแก้

| Issue | Cause | Fix |
|-------|-------|-----|
| **ภาพผลลัพธ์เป็นสีขาว** | `NoScaling` ตั้งค่าไม่ถูกต้องหรือไม่ได้เลือกเลเอาต์ | ตั้งค่า `AutomaticLayoutsScaling = true` หรือระบุเลเอาต์ที่ต้องการ. |
| **Out‑of‑memory สำหรับไฟล์ขนาดใหญ่** | โหลดไฟล์ DGN ขนาดใหญ่โดยไม่มีการสตรีม | ใช้ `Image.Load(sourceFilePath, new LoadOptions { LoadOnDemand = true })`. |
| **เวอร์ชัน DGN ที่ไม่รองรับ** | เวอร์ชัน MicroStation เก่า | ตรวจสอบว่าคุณมี Aspose.CAD เวอร์ชันล่าสุดที่รองรับรูปแบบเก่า. |

## คำถามที่พบบ่อย

**Q: ฉันสามารถส่งออกไฟล์ DGN ไปยังรูปแบบอื่นนอกจาก JPEG ได้หรือไม่?**  
A: ใช่, Aspose.CAD สำหรับ .NET รองรับ PNG, BMP, GIF, TIFF และอื่น ๆ – เพียงเปลี่ยนคลาสตัวเลือก (เช่น `new PngOptions()`).

**Q: ฉันควรจัดการข้อยกเว้นระหว่างการแปลงอย่างไร?**  
A: ใส่โค้ดการแปลงไว้ในบล็อก `try/catch` และบันทึก `Aspose.CAD.CadException` เพื่อรับข้อมูลข้อผิดพลาดโดยละเอียด.

**Q: มีเวอร์ชันทดลองสำหรับ Aspose.CAD สำหรับ .NET หรือไม่?**  
A: ใช่, คุณสามารถทดลองใช้ผลิตภัณฑ์ได้ฟรี เยี่ยมชม [here](https://releases.aspose.com/) เพื่อดูข้อมูลเพิ่มเติม.

**Q: ฉันสามารถขอความช่วยเหลือหรือหารือเกี่ยวกับปัญหา Aspose.CAD สำหรับ .NET ได้ที่ไหน?**  
A: ไปที่ [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) เพื่อรับการสนับสนุนจากชุมชนและการสนทนา.

**Q: ฉันจะขอรับไลเซนส์ชั่วคราวสำหรับ Aspose.CAD สำหรับ .NET ได้อย่างไร?**  
A: เยี่ยมชม [this link](https://purchase.aspose.com/temporary-license/) เพื่อรับไลเซนส์ชั่วคราวสำหรับความต้องการพัฒนาของคุณ.

## สรุป

คุณได้เรียนรู้วิธี **convert dgn to png** (หรือ JPEG) ด้วย Aspose.CAD สำหรับ .NET แล้ว โดยการปรับตัวเลือกการเรสเตอร์ไลซ์และสลับคลาสตัวเลือกภาพ คุณสามารถปรับผลลัพธ์ให้ตรงกับความต้องการของโครงการใด ๆ อย่าลังเลที่จะทดลองกับขนาดหน้า, การตั้งค่า DPI, และรูปแบบไฟล์ต่าง ๆ เพื่อให้ได้ภาพเรสเตอร์ที่สมบูรณ์แบบสำหรับแอปพลิเคชันของคุณ.

---

**อัปเดตล่าสุด:** 2026-03-24  
**ทดสอบกับ:** Aspose.CAD 24.11 for .NET  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}