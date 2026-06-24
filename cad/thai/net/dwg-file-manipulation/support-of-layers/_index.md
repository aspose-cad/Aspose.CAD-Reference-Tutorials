---
date: 2026-04-09
description: เรียนรู้วิธีส่งออกชั้น DWG, แปลงภาพ DWG และบันทึก DWG เป็น JPEG ด้วย
  C# และ Aspose.CAD สำหรับ .NET คู่มือขั้นตอนต่อขั้นตอนสำหรับการจัดการไฟล์ CAD อย่างมีประสิทธิภาพ
keywords:
- export dwg layers
- convert dwg image
- dwg layer visibility
- save dwg jpeg
linktitle: การจัดการเลเยอร์ในไฟล์ DWG ด้วย C#
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: ส่งออกชั้น DWG ด้วย C# – บทแนะนำ Aspose.CAD
url: /th/net/dwg-file-manipulation/support-of-layers/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ส่งออกชั้น DWG ด้วย C# – บทแนะนำ Aspose.CAD

## บทนำ

ในคู่มือฉบับครอบคลุมนี้ คุณจะได้เรียนรู้ **วิธีส่งออกชั้น DWG** ด้วย C# และไลบรารี Aspose.CAD ไม่ว่าคุณจะต้องการ **แปลงรูปภาพ DWG** รูปแบบต่าง ๆ ควบคุม **การมองเห็นชั้น DWG** หรือเพียงแค่ **บันทึกไฟล์ DWG JPEG** ขั้นตอนต่อไปนี้จะแสดงให้คุณเห็นวิธีทำอย่างมีประสิทธิภาพ เมื่อจบบทแนะนำคุณจะมีโค้ดสั้นที่พร้อมรันซึ่งแยกชั้นเฉพาะและเรนเดอร์เป็น JPEG คุณภาพสูง

## คำตอบสั้น
- **การส่งออกชั้น dwg หมายถึงอะไร?** หมายถึงการแปลงเป็นภาพ (rasterizing) ชั้นที่เลือกจากไฟล์ DWG ไปเป็นรูปแบบภาพ เช่น JPEG หรือ PNG.  
- **ไลบรารีใดที่ดีที่สุดสำหรับงานนี้?** Aspose.CAD สำหรับ .NET ให้การสนับสนุนเต็มรูปแบบโดยไม่ต้องใช้ AutoCAD.  
- **ฉันสามารถส่งออกหลายชั้นพร้อมกันได้หรือไม่?** ได้ – ส่งอาร์เรย์ของชื่อชั้นไปยังตัวเลือกการเรสเตอร์ไลซ์.  
- **ฉันต้องการไลเซนส์สำหรับการใช้งานในผลิตภัณฑ์หรือไม่?** จำเป็นต้องมีไลเซนส์เชิงพาณิชย์; มีรุ่นทดลองฟรีสำหรับการประเมินผล.  
- **รูปแบบผลลัพธ์ที่รองรับมีอะไรบ้าง?** JPEG, PNG, BMP, TIFF และรูปแบบอื่น ๆ อีกหลายรูปแบบผ่านคลาส ImageOptions.

## การส่งออกชั้น DWG คืออะไร?
การส่งออกชั้น DWG หมายถึงการนำข้อมูลเวกเตอร์ที่อยู่ในหนึ่งหรือหลายชั้นภายในภาพวาด DWG ไปแปลงเป็นภาพบิตแมป การทำเช่นนี้เป็นประโยชน์เมื่อคุณต้องการแชร์มุมมองของส่วนเฉพาะของภาพวาดโดยไม่ต้องเปิดเผยไฟล์ CAD ทั้งหมด

## ทำไมต้องควบคุมการมองเห็นชั้น DWG?
การควบคุมการมองเห็นชั้นทำให้คุณ:

- สร้างสื่อภาพที่สะอาดสำหรับการนำเสนอหรือเอกสาร.  
- ลดขนาดไฟล์โดยส่งออกเฉพาะเรขาคณิตที่ต้องการ.  
- ปกป้องรายละเอียดการออกแบบที่เป็นกรรมสิทธิ์โดยซ่อนชั้นที่เป็นความลับ.  

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเริ่ม ตรวจสอบว่าคุณมี:

- ความรู้พื้นฐานของภาษาโปรแกรม C#.  
- Visual Studio ติดตั้งบนเครื่องของคุณ.  
- ไลบรารี Aspose.CAD สำหรับ .NET ซึ่งคุณสามารถดาวน์โหลดได้จาก [Aspose.CAD website](https://releases.aspose.com/cad/net/).

## นำเข้า Namespaces

เริ่มต้นโดยการนำเข้า namespaces ที่ให้คุณเข้าถึงคุณลักษณะการเรสเตอร์ไลซ์และการส่งออกภาพ

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

## ขั้นตอนที่ 1: โหลดไฟล์ DWG

โหลดไฟล์ DWG (หรือ DWF) ต้นฉบับเข้าสู่วัตถุ `Image` วัตถุนี้แทนภาพวาดทั้งหมดในหน่วยความจำ

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "for_layers_test.dwf";

using (Aspose.CAD.Image image = Aspose.CAD.Image.Load(sourceFilePath))
{
    // Your code for subsequent steps goes here
}
```

*ทำไมเรื่องนี้ถึงสำคัญ:* การโหลดไฟล์เพียงครั้งเดียวทำให้คุณสามารถใช้อินสแตนซ์ `image` เดียวกันสำหรับการส่งออกหลายชั้นได้ ซึ่งช่วยเพิ่มประสิทธิภาพ

## ขั้นตอนที่ 2: กำหนดค่าตัวเลือกการเรสเตอร์ไลซ์

สร้างอินสแตนซ์ `CadRasterizationOptions` เพื่อบอก Aspose.CAD วิธีการเรนเดอร์ภาพวาด ในที่นี้เราตั้งความละเอียดสูง (1600 × 1600) เพื่อให้ JPEG ที่ส่งออกคมชัด

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions rasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
```

คุณยังสามารถปรับสีพื้นหลัง, การสเกลความหนาของเส้น, หรือการตั้งค่า anti‑aliasing หากต้องการ

## ขั้นตอนที่ 3: ระบุชั้น (การมองเห็นชั้น DWG)

เพิ่มชั้นที่คุณต้องการ **export dwg layers** ในที่นี้เราส่งออกเฉพาะ “LayerA” หากต้องการส่งออกหลายชั้น เพียงระบุชื่อในอาร์เรย์

```csharp
rasterizationOptions.Layers = new string[] { "LayerA" };
```

*เคล็ดลับ:* ใช้ชื่อชั้นที่ตรงกับที่ปรากฏในภาพวาด; ชื่อชั้นแยกแยะตัวพิมพ์ใหญ่‑เล็ก

## ขั้นตอนที่ 4: กำหนดค่าตัวเลือกการส่งออกภาพ

เลือกรูปแบบภาพที่ต้องการสร้าง เราจะใช้ `JpegOptions` เนื่องจาก JPEG ให้สมดุลที่ดีระหว่างคุณภาพและขนาดไฟล์ ซึ่งเหมาะเมื่อคุณต้องการ **save dwg jpeg** สำหรับการแสดงตัวอย่างบนเว็บ

```csharp
JpegOptions jpegOptions = new JpegOptions();
jpegOptions.VectorRasterizationOptions = rasterizationOptions;
```

หากคุณต้องการ **convert dwg image** เป็น PNG หรือ TIFF ให้เปลี่ยน `JpegOptions` เป็นคลาสตัวเลือกที่สอดคล้องกัน

## ขั้นตอนที่ 5: บันทึกรูปภาพที่ส่งออก

กำหนดเส้นทางไฟล์ผลลัพธ์และเรียก `Save` เอนจินการเรสเตอร์ไลซ์จะเคารพรายการชั้นที่คุณระบุ ดังนั้นใน JPEG สุดท้ายจะมีเฉพาะ “LayerA” เท่านั้น

```csharp
MyDir = MyDir + "for_layers_test.jpg";
image.Save(MyDir, jpegOptions);
```

หลังจากบรรทัดนี้ทำงาน คุณจะพบไฟล์ `for_layers_test.jpg` ในไดเรกทอรีของเอกสารของคุณ ซึ่งมีเฉพาะชั้นที่เลือกเท่านั้น

## ปัญหาที่พบบ่อยและวิธีแก้

| ปัญหา | วิธีแก้ |
|-------|------------|
| **ไม่พบชื่อชั้น** | ตรวจสอบการสะกดและตัวพิมพ์ใหญ่‑เล็กของชื่อชั้นใน DWG ต้นฉบับ ใช้โปรแกรมดู CAD เพื่อแสดงรายการชื่อชั้น |
| **ภาพผลลัพธ์เป็นสีขาว** | ตรวจสอบว่าตัวเลือกการเรสเตอร์ไลซ์มีพื้นหลังที่ไม่โปร่งแสงและชั้นที่เลือกมีเรขาคณิตจริง |
| **ผลลัพธ์ความละเอียดต่ำ** | เพิ่มค่า `PageWidth` และ `PageHeight` หรือกำหนด `Resolution` ใน `CadRasterizationOptions` |
| **เวอร์ชัน DWG ไม่รองรับ** | อัปเดตเป็นเวอร์ชันล่าสุดของ Aspose.CAD; จะเพิ่มการสนับสนุนเวอร์ชัน AutoCAD ใหม่ |

## คำถามที่พบบ่อย

### Q1: ฉันสามารถจัดการหลายชั้นพร้อมกันได้หรือไม่?
A1: ได้ คุณเพียงเพิ่มชื่อชั้นลงในอาร์เรย์ `rasterizationOptions.Layers`

### Q2: มีเวอร์ชันทดลองของ Aspose.CAD หรือไม่?
A2: มี คุณสามารถรับเวอร์ชันทดลองฟรีได้จาก [here](https://releases.aspose.com/)

### Q3: ฉันสามารถหาเอกสารอ้างอิงได้ที่ไหน?
A3: เอกสารอ้างอิงมีให้ที่ [here](https://reference.aspose.com/cad/net/)

### Q4: ฉันจะขอรับการสนับสนุนสำหรับ Aspose.CAD ได้อย่างไร?
A4: คุณสามารถขอรับการสนับสนุนได้ใน [Aspose.CAD forum](https://forum.aspose.com/c/cad/19)

### Q5: ตัวเลือกการให้ลิขสิทธิ์สำหรับ Aspose.CAD มีอะไรบ้าง?
A5: คุณสามารถสำรวจตัวเลือกการให้ลิขสิทธิ์และรายละเอียดการซื้อได้ที่ [here](https://purchase.aspose.com/buy)

**คำถามเพิ่มเติม**

**Q: ฉันสามารถส่งออกภาพวาดเป็น PNG แทน JPEG ได้หรือไม่?**  
A: ได้เลย แค่เปลี่ยน `JpegOptions` เป็น `PngOptions` และปรับนามสกุลไฟล์ให้สอดคล้อง

**Q: ไลบรารีนี้รักษารูปแบบเส้นและสีไว้หรือไม่?**  
A: ใช่ คุณสมบัติเวกเตอร์ทั้งหมดจะถูกเรนเดอร์อย่างถูกต้องระหว่างการเรสเตอร์ไลซ์

**อัปเดตล่าสุด:** 2026-04-09  
**ทดสอบด้วย:** Aspose.CAD for .NET (latest release)  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}