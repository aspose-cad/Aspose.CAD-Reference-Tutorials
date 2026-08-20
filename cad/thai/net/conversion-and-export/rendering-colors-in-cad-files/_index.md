---
date: 2026-04-03
description: เรียนรู้วิธีการเรนเดอร์ไฟล์ CAD และแปลง DWG เป็น PNG ด้วย Aspose.CAD
  สำหรับ .NET คู่มือทีละขั้นตอนในการบันทึก CAD เป็นภาพ
keywords:
- how to render cad
- convert dwg to png
- export cad to png
- save cad as image
- load dwg in .net
linktitle: การเรนเดอร์สีในไฟล์ CAD
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: วิธีเรนเดอร์ไฟล์ CAD ด้วยสี – คู่มือ Aspose.CAD
url: /th/net/conversion-and-export/rendering-colors-in-cad-files/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีการเรนเดอร์ไฟล์ CAD ด้วยสี – คู่มือ Aspose.CAD

## บทนำ

## คำตอบสั้น
- **ไลบรารีใดที่ดีที่สุดสำหรับการเรนเดอร์สี CAD?** Aspose.CAD for .NET  
- **ฉันสามารถแปลง DWG เป็น PNG ในขั้นตอนเดียวได้หรือไม่?** ใช่ – เรนเดอร์ DWG แล้วบันทึกเป็น PNG.  
- **ฉันต้องการไลเซนส์สำหรับการใช้งานในผลิตภัณฑ์หรือไม่?** ไลเซนส์ชั่วคราวใช้ได้สำหรับการทดสอบ; จำเป็นต้องมีไลเซนส์เต็มสำหรับการผลิต.  
- **เวอร์ชัน .NET ใดที่รองรับ?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.  
- **กระบวนการเร็วพอสำหรับการแปลงเป็นชุดหรือไม่?** การเรนเดอร์ทำในหน่วยความจำและเหมาะสำหรับการดำเนินการเป็นจำนวนมาก.

## การเรนเดอร์สีในไฟล์ CAD คืออะไร?
การเรนเดอร์สีหมายถึงการนำข้อมูลเวกเตอร์ที่เก็บไว้ในภาพวาด CAD (DWG, DXF ฯลฯ) มาทำเป็นภาพบิตแมพในขณะที่คงสีของวัตถุต้นฉบับไว้ นี่เป็นสิ่งสำคัญเมื่อคุณต้องการแชร์ภาพ CAD ให้กับผู้มีส่วนได้ส่วนเสียที่ไม่มีซอฟต์แวร์ CAD.

## ทำไมต้องใช้ Aspose.CAD เพื่อแปลง DWG เป็น PNG?
- **ไม่มีการพึ่งพาภายนอก** – ทำงานแบบออฟไลน์ทั้งหมด.  
- **ความแม่นยำเต็มรูปแบบ** – สีของวัตถุ, ความหนาของเส้น, และเลเยอร์จะถูกเก็บไว้.  
- **API ง่าย** – โค้ดบรรทัดเดียวเพื่อโหลด, ตั้งค่า, และบันทึก.  
- **ข้ามแพลตฟอร์ม** – ทำงานบน Windows, Linux, และ macOS .NET runtimes.

## ข้อกำหนดเบื้องต้น
- Aspose.CAD Library: ดาวน์โหลดและติดตั้งไลบรารี Aspose.CAD จาก [ที่นี่](https://releases.aspose.com/cad/net/).  
- Development Environment: ตรวจสอบว่าคุณมีสภาพแวดล้อมการพัฒนา .NET ตั้งค่าไว้แล้ว.  
- CAD File: มีไฟล์ CAD ตัวอย่างพร้อมสำหรับการทดสอบ คุณสามารถใช้ “test1.dwg” สำหรับบทเรียนนี้.

## นำเข้า Namespaces
ในโครงการ .NET ของคุณ ให้นำเข้า namespaces ที่จำเป็นเพื่อเข้าถึงฟังก์ชันของ Aspose.CAD เพิ่มบรรทัดต่อไปนี้ที่ส่วนเริ่มต้นของโค้ดของคุณ:

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

## ขั้นตอนที่ 1: ตั้งค่าโปรเจกต์ของคุณ
สร้างโปรเจกต์ .NET ใหม่และตั้งค่าไดเรกทอรีที่จำเป็น ตรวจสอบให้แน่ใจว่าไลบรารี Aspose.CAD ถูกอ้างอิงในโปรเจกต์ของคุณ.

## ขั้นตอนที่ 2: กำหนดเส้นทางไฟล์
ระบุเส้นทางสำหรับไฟล์ CAD เข้าของคุณและไฟล์ PNG เอาต์พุต ปรับปรุงบรรทัดต่อไปนี้ในโค้ดของคุณ:

```csharp
string MyDir = "Your Document Directory";
string inputFile = MyDir + "test1.dwg";
string outputFile = MyDir + "test1.png";
```

## ขั้นตอนที่ 3: โหลดไฟล์ CAD
ใช้โค้ดต่อไปนี้เพื่อเปิดและโหลดไฟล์ CAD:

```csharp
using (FileStream fs = new FileStream(inputFile, FileMode.Open))
{
    using (FileStream output = new FileStream(outputFile, FileMode.Create))
    {
        Image document = Image.Load(fs);
```

## ขั้นตอนที่ 4: ตั้งค่าตัวเลือกการเรนเดอร์
กำหนดค่าตัวเลือกการเรนเดอร์เพื่อปรับแต่งกระบวนการเรนเดอร์ ปรับปรุงบรรทัดต่อไปนี้:

```csharp
PngOptions saveOptions = new PngOptions();

CadRasterizationOptions options = new CadRasterizationOptions();
options.NoScaling = false;
options.PageHeight = document.Height * 10;
options.PageWidth = document.Width * 10;
options.DrawType = Aspose.CAD.FileFormats.Cad.CadDrawTypeMode.UseObjectColor;
saveOptions.VectorRasterizationOptions = options;
```

## ขั้นตอนที่ 5: บันทึกภาพที่เรนเดอร์
บันทึกภาพที่เรนเดอร์โดยใช้ตัวเลือกที่ระบุ:

```csharp
document.Save(output, saveOptions);
```

## ทำไมเรื่องนี้ถึงสำคัญ
การบันทึก CAD เป็นภาพ (PNG, JPEG, ฯลฯ) เป็นความต้องการทั่วไปเมื่อคุณต้องการฝังภาพวาดในรายงาน, หน้าเว็บ, หรือไฟล์แนบอีเมล โดยการเชี่ยวชาญ **วิธีการเรนเดอร์ CAD** คุณจะไม่ต้องพึ่งพาผู้ชมจากบุคคลที่สามและรับประกันผลลัพธ์ภาพที่สอดคล้องกันบนทุกแพลตฟอร์ม.

## ปัญหาที่พบบ่อยและวิธีแก้
| ปัญหา | สาเหตุ | วิธีแก้ |
|-------|-------|----------|
| ผลลัพธ์ภาพว่าง | `NoScaling` ตั้งค่าเป็น `true` พร้อมมิติศูนย์ | ตรวจสอบให้แน่ใจว่า `PageHeight` และ `PageWidth` คำนวณจากภาพที่โหลด (ตามที่แสดง). |
| สีแสดงผลผิด | `DrawType` ผิด | ใช้ `CadDrawTypeMode.UseObjectColor` เพื่อรักษาสีวัตถุต้นฉบับ. |
| ไม่พบไฟล์ | `MyDir` path ไม่ถูกต้อง | ตรวจสอบว่าเส้นทางไดเรกทอรีลงท้ายด้วยเครื่องหมายทับหรือใช้ `Path.Combine`. |
| หน่วยความจำเต็มเมื่อไฟล์ขนาดใหญ่ | เรนเดอร์ที่ DPI สูงมาก | ลดค่าอัตราสเกล (เช่น `*5` แทน `*10`). |

## สรุป
ขอแสดงความยินดี! คุณได้เรียนรู้ **วิธีการเรนเดอร์ CAD** ไฟล์, แปลง DWG เป็น PNG, และ **บันทึก CAD เป็นภาพ** ด้วย Aspose.CAD สำหรับ .NET อย่างสำเร็จ ความรู้นี้ทำให้คุณสามารถรวมการเรนเดอร์ CAD เข้าไปในแอปพลิเคชันของคุณโดยตรง, อัตโนมัติการสร้างรายงาน, ตัวอย่างเว็บ, และอื่น ๆ

## คำถามที่พบบ่อย

### Q1: ฉันสามารถใช้ Aspose.CAD ได้ฟรีหรือไม่?
A1: Aspose.CAD มีเวอร์ชันทดลองฟรีที่พร้อมให้ดาวน์โหลด [ที่นี่](https://releases.aspose.com/). คุณสามารถสำรวจคุณสมบัติก่อนตัดสินใจซื้อ.

### Q2: ฉันจะหาเอกสารรายละเอียดของ Aspose.CAD ได้จากที่ไหน?
A2: ดูเอกสาร [ที่นี่](https://reference.aspose.com/cad/net/) สำหรับข้อมูลเชิงลึกเกี่ยวกับฟังก์ชันของ Aspose.CAD.

### Q3: ฉันจะขอรับไลเซนส์ชั่วคราวสำหรับ Aspose.CAD ได้อย่างไร?
A3: รับไลเซนส์ชั่วคราว [ที่นี่](https://purchase.aspose.com/temporary-license/) เพื่อการทดสอบ.

### Q4: ต้องการความช่วยเหลือหรือมีคำถาม?
A4: เยี่ยมชม [ฟอรั่ม](https://forum.aspose.com/c/cad/19) ของชุมชน Aspose.CAD เพื่อรับการสนับสนุนและการสนทนา.

### Q5: ฉันจะซื้อไลบรารี Aspose.CAD ได้จากที่ไหน?
A5: ซื้อ Aspose.CAD [ที่นี่](https://purchase.aspose.com/buy) เพื่อเปิดศักยภาพเต็มของมัน.

## คำถามที่พบบ่อยเพิ่มเติม

**ถาม: ฉันจะ **แปลง DWG เป็น PNG** โดยไม่สูญเสียความหนาของเส้นได้อย่างไร?**  
A: รักษาการสเกล `PageHeight` และ `PageWidth` เริ่มต้น (เช่น คูณด้วย 10) และตั้งค่า `options.DrawType` เป็น `UseObjectColor`. วิธีนี้จะรักษาความหนาของเส้นและสี.

**ถาม: สามารถ **ส่งออก CAD เป็น PNG** ในบริการพื้นหลังได้หรือไม่?**  
A: ได้. API ของ Aspose.CAD ปลอดภัยต่อการทำงานหลายเธรดสำหรับการดำเนินการแบบอ่านอย่างเดียว, ดังนั้นคุณสามารถโหลดและเรนเดอร์ไฟล์ภายใน background worker ได้.

**ถาม: ฉันสามารถ **โหลด DWG ใน .NET** จากอาร์เรย์ไบต์แทนไฟล์ได้หรือไม่?**  
A: แน่นอน. ใช้ `Image.Load(byteArray)` แทน `FileStream` และทำตามขั้นตอนการเรนเดอร์เดียวกัน.

**ถาม: ควรเลือกฟอร์แมตใดสำหรับคุณภาพดีที่สุดเมื่อ **บันทึก CAD เป็นภาพ**?**  
A: PNG ให้การบีบอัดแบบไม่มีการสูญเสียและรักษาความแม่นยำของสี, ทำให้เหมาะสำหรับภาพวาดทางเทคนิค.

**ถาม: Aspose.CAD รองรับฟอร์แมตเรสเตอร์อื่น ๆ เช่น JPEG หรือ BMP หรือไม่?**  
A: ใช่ – เพียงเปลี่ยน `PngOptions` เป็น `JpegOptions` หรือ `BmpOptions` และปรับการตั้งค่าที่เฉพาะฟอร์แมตตามต้องการ.

---

**อัปเดตล่าสุด:** 2026-04-03  
**ทดสอบด้วย:** Aspose.CAD 24.11 for .NET  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}