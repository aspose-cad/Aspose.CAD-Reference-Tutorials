---
title: การแปลง STL เป็น PNG เป็นเรื่องง่ายด้วย Aspose.CAD สำหรับ .NET
linktitle: การส่งออกไฟล์ STL เป็น PNG
second_title: Aspose.CAD .NET - รูปแบบไฟล์ CAD และ BIM
description: แปลงไฟล์ STL เป็น PNG ได้อย่างง่ายดายโดยใช้ Aspose.CAD สำหรับ .NET ปฏิบัติตามคำแนะนำทีละขั้นตอนของเราเพื่อการบูรณาการที่ราบรื่น ดาวน์โหลดเดี๋ยวนี้!
weight: 10
url: /th/net/stl-file-export/exporting-stl-files-to-png/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# การแปลง STL เป็น PNG เป็นเรื่องง่ายด้วย Aspose.CAD สำหรับ .NET

## การแนะนำ
ในโลกแบบไดนามิกของการออกแบบโดยใช้คอมพิวเตอร์ช่วย (CAD) การแปลงไฟล์อย่างมีประสิทธิภาพถือเป็นสิ่งสำคัญ Aspose.CAD สำหรับ .NET เป็นชุดเครื่องมืออันทรงพลังที่ทำให้กระบวนการส่งออกไฟล์ STL ไปยัง PNG ง่ายขึ้น ช่วยให้นักพัฒนามีความยืดหยุ่นและฟังก์ชันการทำงานที่ต้องการ บทช่วยสอนนี้จะแนะนำคุณตลอดกระบวนการทีละขั้นตอน เพื่อให้มั่นใจว่าการเปลี่ยนจาก STL เป็น PNG เป็นไปอย่างราบรื่นโดยใช้ Aspose.CAD
## ข้อกำหนดเบื้องต้น
ก่อนที่เราจะเจาะลึกบทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีสิ่งต่อไปนี้:
1.  Aspose.CAD สำหรับ .NET: ดาวน์โหลดและติดตั้งไลบรารี Aspose.CAD คุณสามารถหามันได้[ที่นี่](https://releases.aspose.com/cad/net/).
2. สภาพแวดล้อมการพัฒนา: ตั้งค่าสภาพแวดล้อมการพัฒนา .NET ที่คุณต้องการ
3. ไฟล์ STL: เตรียมไฟล์ STL ให้พร้อมสำหรับการแปลง สำหรับบทช่วยสอนนี้ เราจะใช้ไฟล์ตัวอย่างชื่อ "galeon.stl"
## นำเข้าเนมสเปซ
ในการเริ่มต้นกระบวนการ ให้นำเข้าเนมสเปซที่จำเป็นในแอปพลิเคชัน .NET ของคุณ เพื่อให้แน่ใจว่าคุณจะสามารถเข้าถึงคลาสและวิธีการที่จำเป็นสำหรับการแปลง STL เป็น PNG
```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```
## ขั้นตอนที่ 1: กำหนดไดเรกทอรีและเส้นทางไฟล์ต้นฉบับ
```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "galeon.stl";
```
ตรวจสอบให้แน่ใจว่าคุณแทนที่ "Your Document Directory" ด้วยเส้นทางไดเรกทอรีจริงที่มีไฟล์ STL ของคุณอยู่
## ขั้นตอนที่ 2: โหลดอิมเมจ CAD
```csharp
using (var cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // ขั้นตอนต่อไปจะดำเนินการภายในบล็อกนี้
}
```
ขั้นตอนนี้จะโหลดไฟล์ STL เป็นอิมเมจ CAD ซึ่งช่วยให้คุณสามารถจัดการและส่งออกไฟล์ได้
## ขั้นตอนที่ 3: ตั้งค่าตัวเลือกการแรสเตอร์
```csharp
var rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 100;
rasterizationOptions.PageHeight = 100;
```
ปรับความกว้างและความสูงของหน้าตามความต้องการและความต้องการของคุณ การตั้งค่าเหล่านี้จะกำหนดขนาดของ PNG ที่ส่งออก
## ขั้นตอนที่ 4: กำหนดค่าตัวเลือก PNG
```csharp
PngOptions pngOptions = new PngOptions();
pngOptions.VectorRasterizationOptions = rasterizationOptions;
```
สร้างตัวเลือก PNG โดยผสมผสานการตั้งค่าแรสเตอร์ที่กำหนดไว้ในขั้นตอนก่อนหน้า
## ขั้นตอนที่ 5: บันทึกไฟล์ PNG
```csharp
string outPath = sourceFilePath + ".png";
cadImage.Save(outPath, pngOptions);
```
ระบุเส้นทางเอาต์พุตสำหรับไฟล์ PNG และบันทึกรูปภาพ CAD ในรูปแบบ PNG โดยใช้ตัวเลือกที่ให้ไว้
ทำซ้ำขั้นตอนเหล่านี้ตามที่จำเป็นสำหรับกรณีการใช้งานเฉพาะของคุณ และคุณจะส่งออกไฟล์ STL เป็น PNG ด้วย Aspose.CAD สำหรับ .NET ได้สำเร็จ
## บทสรุป
Aspose.CAD สำหรับ .NET ช่วยให้งานที่ซับซ้อนในการแปลงไฟล์ STL เป็น PNG ง่ายขึ้น ช่วยให้นักพัฒนามีชุดเครื่องมือที่เชื่อถือได้ ด้วยการทำตามคำแนะนำทีละขั้นตอนนี้ คุณสามารถรวมฟังก์ชันการทำงานนี้เข้ากับแอปพลิเคชันของคุณได้อย่างราบรื่น
## คำถามที่พบบ่อย
### ถาม: ฉันสามารถกำหนดขนาดของ PNG ที่ส่งออกได้หรือไม่
 อย่างแน่นอน! ในขั้นตอนที่ 3 ให้ปรับ`PageWidth` และ`PageHeight` คุณค่าเพื่อตอบสนองความต้องการเฉพาะของคุณ
### ถาม: มีใบอนุญาตชั่วคราวสำหรับการทดสอบหรือไม่
 ใช่ คุณสามารถขอรับใบอนุญาตชั่วคราวได้[ที่นี่](https://purchase.aspose.com/temporary-license/) เพื่อการทดสอบและประเมินผล
### ถาม: ฉันจะรับการสนับสนุนเพิ่มเติมหรือการสนทนาในชุมชนได้จากที่ไหน
 เยี่ยมชม[ฟอรั่ม Aspose.CAD](https://forum.aspose.com/c/cad/19) เพื่อสนับสนุนและหารือร่วมกัน
### ถาม: มีไฟล์รูปแบบอื่นที่รองรับการแปลงหรือไม่
 ใช่ Aspose.CAD รองรับรูปแบบ CAD ที่หลากหลายนอกเหนือจาก STL อ้างถึง[เอกสารประกอบ](https://reference.aspose.com/cad/net/) สำหรับรายการที่ครอบคลุม
### ถาม: ฉันสามารถประมวลผลไฟล์ STL หลายไฟล์เป็นชุดได้หรือไม่
แน่นอน! ใช้การวนซ้ำตามขั้นตอนที่ให้ไว้เพื่อประมวลผลไฟล์ STL หลายไฟล์เป็นชุด
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
