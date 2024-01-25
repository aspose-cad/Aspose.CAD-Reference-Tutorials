---
title: การส่งออกเป็นรูปแบบ BMP - บทช่วยสอน Aspose.CAD
linktitle: ส่งออกเป็นรูปแบบ BMP
second_title: Aspose.CAD .NET - รูปแบบไฟล์ CAD และ BIM
description: สำรวจโลกที่ไร้รอยต่อของการส่งออกภาพ 3 มิติไปยัง BMP โดยใช้ Aspose.CAD สำหรับ .NET ปฏิบัติตามบทช่วยสอนของเราเพื่อรับประสบการณ์ที่ไม่ยุ่งยาก
type: docs
weight: 11
url: /th/net/file-format-conversion/exporting-to-bmp-format/
---
## การแนะนำ

ในโลกแบบไดนามิกของการพัฒนาซอฟต์แวร์ Aspose.CAD สำหรับ .NET มีความโดดเด่นในฐานะเครื่องมืออันทรงพลังสำหรับการจัดการไฟล์ Computer-Aided Design (CAD) หากคุณต้องการส่งออกรูปภาพ CAD เป็นรูปแบบ BMP ที่ใช้กันอย่างแพร่หลาย บทช่วยสอนนี้คือแนวทางปฏิบัติของคุณ ในคำแนะนำแบบทีละขั้นตอนนี้ เราจะสำรวจกระบวนการส่งออกรูปภาพ 3 มิติไปยัง BMP โดยใช้ Aspose.CAD สำหรับ .NET มาดำน้ำกันเถอะ!

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเริ่มบทช่วยสอนนี้ ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

-  Aspose.CAD สำหรับ .NET: ดาวน์โหลดและติดตั้งไลบรารี Aspose.CAD จาก[ที่นี่](https://releases.aspose.com/cad/net/).
- สภาพแวดล้อมการพัฒนา: ตั้งค่าสภาพแวดล้อมการพัฒนา .NET
- ไฟล์ CAD: เตรียมไฟล์ CAD ให้พร้อมสำหรับการส่งออก สำหรับตัวอย่างนี้ เราจะใช้ "18-12-11 9644 - site.dwf"

## นำเข้าเนมสเปซ

ในโปรเจ็กต์ .NET ของคุณ ตรวจสอบให้แน่ใจว่าได้นำเข้าเนมสเปซที่จำเป็น:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
```

## ขั้นตอนที่ 1: โหลดอิมเมจ CAD

เริ่มต้นด้วยการโหลดอิมเมจ CAD ลงในโปรเจ็กต์ของคุณ แทนที่ "Your Document Directory" ด้วยเส้นทางไดเรกทอรีจริง

```csharp
string MyDir = "Your Document Directory";
string inputFile = MyDir + "18-12-11 9644 - site.dwf";

using (Image image = Image.Load(inputFile))
{
    // รหัสของคุณสำหรับการโหลดภาพอยู่ที่นี่
}
```

## ขั้นตอนที่ 2: กำหนดค่าตัวเลือกการส่งออก BMP

ตั้งค่าตัวเลือกการส่งออก BMP รวมถึงตัวเลือกการแรสเตอร์เวกเตอร์สำหรับไฟล์ CAD

```csharp
BmpOptions bmpOptions = new BmpOptions();
var dwfRasterizationOptions = new CadRasterizationOptions();
bmpOptions.VectorRasterizationOptions = dwfRasterizationOptions;

dwfRasterizationOptions.PageHeight = 500;
dwfRasterizationOptions.PageWidth = 500;
```

## ขั้นตอนที่ 3: ส่งออกเป็น BMP

ดำเนินการกระบวนการส่งออก โดยระบุเส้นทางเอาต์พุตสำหรับไฟล์ BMP

```csharp
string outPath = MyDir + "18-12-11 9644 - site.bmp";
image.Save(outPath, bmpOptions);
```

## บทสรุป

ยินดีด้วย! คุณได้ส่งออกรูปภาพ 3 มิติไปยัง BMP โดยใช้ Aspose.CAD สำหรับ .NET สำเร็จแล้ว บทช่วยสอนนี้ให้ข้อมูลเชิงลึกเกี่ยวกับความอเนกประสงค์ของ Aspose.CAD ซึ่งทำให้งานที่ซับซ้อนรู้สึกเหมือนเป็นเรื่องง่าย

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถใช้ Aspose.CAD สำหรับ .NET กับไฟล์ CAD ทุกรูปแบบได้หรือไม่

ตอบ 1: ใช่ Aspose.CAD รองรับไฟล์ CAD หลากหลายรูปแบบ ซึ่งให้ความยืดหยุ่นในโครงการของคุณ

### คำถามที่ 2: มีใบอนุญาตชั่วคราวสำหรับการทดสอบหรือไม่

 A2: แน่นอน! คุณสามารถขอรับใบอนุญาตชั่วคราวได้[ที่นี่](https://purchase.aspose.com/temporary-license/) สำหรับการประเมินผล

### คำถามที่ 3: ฉันจะหาเอกสารประกอบสำหรับ Aspose.CAD ได้ที่ไหน

 A3: โปรดดูเอกสารประกอบ[ที่นี่](https://reference.aspose.com/cad/net/) สำหรับข้อมูลโดยละเอียดและตัวอย่าง

### คำถามที่ 4: ฉันจะขอรับการสนับสนุนหรือเชื่อมต่อกับชุมชนได้อย่างไร

 A4: เยี่ยมชมฟอรั่ม Aspose.CAD[ที่นี่](https://forum.aspose.com/c/cad/19) เพื่อถามคำถามและมีส่วนร่วมกับชุมชน

### คำถามที่ 5: ฉันสามารถซื้อ Aspose.CAD สำหรับ .NET ได้หรือไม่

 A5: ได้ คุณสามารถซื้อ Aspose.CAD ได้[ที่นี่](https://purchase.aspose.com/buy) เพื่อปลดล็อกศักยภาพสูงสุดสำหรับโครงการของคุณ
