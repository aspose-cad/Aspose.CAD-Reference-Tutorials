---
title: การส่งออกแบบร่าง CAD เป็นรูปแบบ SVG - คู่มือ Aspose.CAD
linktitle: การส่งออกแบบร่าง CAD เป็นรูปแบบ SVG
second_title: Aspose.CAD .NET - รูปแบบไฟล์ CAD และ BIM
description: สำรวจกระบวนการที่ราบรื่นในการส่งออกแบบร่าง CAD ไปยัง SVG โดยใช้ Aspose.CAD สำหรับ .NET ปรับปรุงการพัฒนา CAD ของคุณด้วยความยืดหยุ่นและการปรับแต่ง
weight: 15
url: /th/net/advanced-export-techniques/exporting-cad-drawings-to-svg/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# การส่งออกแบบร่าง CAD เป็นรูปแบบ SVG - คู่มือ Aspose.CAD

## การแนะนำ

ในโลกที่มีการเปลี่ยนแปลงตลอดเวลาของ CAD (Computer-Aided Design) ความสามารถในการส่งออกภาพวาดเป็นรูปแบบต่างๆ ถือเป็นทักษะที่สำคัญ SVG (Scalable Vector Graphics) เป็นรูปแบบหนึ่งที่ได้รับความนิยมเนื่องจากความสามารถในการปรับขนาดและความสามารถรอบด้าน ในบทช่วยสอนนี้ เราจะสำรวจวิธีการส่งออกแบบร่าง CAD ไปยัง SVG โดยใช้ไลบรารี Aspose.CAD สำหรับ .NET อันทรงพลัง

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเข้าสู่บทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

-  Aspose.CAD สำหรับไลบรารี .NET: ดาวน์โหลดและติดตั้ง Aspose.CAD สำหรับไลบรารี .NET คุณสามารถค้นหาห้องสมุด[ที่นี่](https://releases.aspose.com/cad/net/).

- สภาพแวดล้อมการพัฒนา: ตั้งค่าสภาพแวดล้อมการพัฒนาที่เหมาะสมด้วย Visual Studio หรือเครื่องมือพัฒนา .NET อื่นๆ

## นำเข้าเนมสเปซ

ในการเริ่มต้น ให้นำเข้าเนมสเปซที่จำเป็นลงในโปรเจ็กต์ของคุณ:

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## ขั้นตอนที่ 1: ตั้งค่าไดเร็กทอรีเอกสาร

```csharp
// เส้นทางไปยังไดเร็กทอรีเอกสาร
string MyDir = "Your Document Directory";
```

## ขั้นตอนที่ 2: โหลดแบบร่าง CAD

```csharp
using (Image image = Image.Load(MyDir + "sample.dwg"))
{
```

## ขั้นตอนที่ 3: กำหนดค่าตัวเลือกการส่งออก SVG

```csharp
    var options = new SvgOptions();
    options.ColorType = SvgColorMode.Grayscale;
    options.TextAsShapes = true;
```

## ขั้นตอนที่ 4: บันทึกไฟล์ SVG

```csharp
    image.Save(MyDir + "sample.svg", options);
}
```

ด้วยการทำตามขั้นตอนง่ายๆ เหล่านี้ คุณสามารถส่งออกแบบร่าง CAD ไปยัง SVG ได้อย่างราบรื่นโดยใช้ Aspose.CAD สำหรับ .NET ไลบรารีมีตัวเลือกความยืดหยุ่นและการปรับแต่ง ช่วยให้คุณสามารถปรับแต่งผลลัพธ์ตามความต้องการของคุณ

## บทสรุป

โดยสรุป Aspose.CAD สำหรับ .NET ช่วยให้กระบวนการส่งออกแบบร่าง CAD ไปยัง SVG ง่ายขึ้น API ที่ใช้งานง่ายและฟีเจอร์ที่แข็งแกร่งทำให้เป็นเครื่องมืออันมีค่าสำหรับนักพัฒนาที่ทำงานกับแอปพลิเคชัน CAD

## คำถามที่พบบ่อย

### คำถามที่ 1: Aspose.CAD เข้ากันได้กับรูปแบบ CAD ทั้งหมดหรือไม่

A1: Aspose.CAD รองรับรูปแบบ CAD หลากหลาย รวมถึง DWG และ DXF เพื่อให้มั่นใจถึงความเข้ากันได้ในวงกว้าง

### คำถามที่ 2: ฉันสามารถปรับแต่งโหมดสีเมื่อส่งออกเป็น SVG ได้หรือไม่

A2: ได้ Aspose.CAD ให้คุณเลือกโหมดสีได้ โดยให้ความยืดหยุ่นในเอาท์พุต

### คำถามที่ 3: มีใบอนุญาตชั่วคราวสำหรับการทดสอบหรือไม่

 A3: ได้ คุณสามารถขอรับใบอนุญาตชั่วคราวได้[ที่นี่](https://purchase.aspose.com/temporary-license/) สำหรับการประเมินผล

### คำถามที่ 4: ฉันจะหาเอกสารโดยละเอียดสำหรับ Aspose.CAD ได้ที่ไหน

 A4: มีเอกสารประกอบให้[ที่นี่](https://reference.aspose.com/cad/net/).

### คำถามที่ 5: ฉันจะรับการสนับสนุนหรือถามคำถามที่เกี่ยวข้องกับ Aspose.CAD ได้อย่างไร

 A5: เยี่ยมชมฟอรั่มชุมชน[ที่นี่](https://forum.aspose.com/c/cad/19) สำหรับการสนับสนุนและการอภิปราย
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
