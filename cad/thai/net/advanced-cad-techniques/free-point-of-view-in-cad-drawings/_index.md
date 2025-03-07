---
title: มุมมองฟรีในแบบร่าง CAD - คู่มือ Aspose.CAD
linktitle: มุมมองฟรีในแบบร่าง CAD
second_title: Aspose.CAD .NET - รูปแบบไฟล์ CAD และ BIM
description: สำรวจอิสรภาพของการแสดงภาพ CAD ด้วย Aspose.CAD สำหรับ .NET ปฏิบัติตามคำแนะนำทีละขั้นตอนของเราเพื่อรับมุมมองที่ไม่เหมือนใคร
weight: 11
url: /th/net/advanced-cad-techniques/free-point-of-view-in-cad-drawings/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# มุมมองฟรีในแบบร่าง CAD - คู่มือ Aspose.CAD

ในขอบเขตของการออกแบบโดยใช้คอมพิวเตอร์ช่วย (CAD) การได้รับมุมมองอิสระในการวาดภาพเป็นส่วนสำคัญในการแสดงภาพและนำเสนอการออกแบบที่ซับซ้อน Aspose.CAD สำหรับ .NET มอบโซลูชันที่แข็งแกร่งเพื่อให้บรรลุอิสรภาพนี้ ทำให้ผู้ใช้สามารถจัดการและปรับแต่งแบบร่าง CAD ได้อย่างง่ายดาย ในคำแนะนำทีละขั้นตอนนี้ เราจะสำรวจกระบวนการรับมุมมองฟรีในแบบร่าง CAD โดยใช้ Aspose.CAD สำหรับ .NET

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเข้าสู่บทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

1. การติดตั้ง Aspose.CAD
 ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง Aspose.CAD สำหรับ .NET ในสภาพแวดล้อมการพัฒนาของคุณ ถ้าไม่เช่นนั้นคุณสามารถดาวน์โหลดได้จาก[เว็บไซต์ Aspose.CAD](https://releases.aspose.com/cad/net/).

2. ไฟล์เขียนแบบ CAD
เตรียมไฟล์รูปวาด CAD ที่คุณต้องการจัดการ สำหรับคำแนะนำนี้ เราจะใช้ไฟล์ตัวอย่างชื่อ "conic_pyramid.dxf"

3. การพัฒนาสภาพแวดล้อม
มีสภาพแวดล้อมการพัฒนา .NET ที่ใช้งานได้ซึ่งตั้งค่าด้วย Visual Studio หรือ IDE ที่ต้องการ

## นำเข้าเนมสเปซ

ในโปรเจ็กต์ .NET ของคุณ ให้นำเข้าเนมสเปซที่จำเป็นสำหรับฟังก์ชัน Aspose.CAD เพิ่มข้อมูลโค้ดต่อไปนี้ที่ด้านบนของไฟล์:

```csharp
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
```


## ขั้นตอนที่ 1: กำหนดไดเร็กทอรีเอกสาร

```csharp
// เส้นทางไปยังไดเร็กทอรีเอกสาร
string MyDir = "Your Document Directory";
```

ตรวจสอบให้แน่ใจว่าได้แทนที่ "Your Document Directory" ด้วยเส้นทางจริงไปยังไดเร็กทอรีเอกสารของคุณ

## ขั้นตอนที่ 2: ระบุไฟล์ต้นฉบับ

```csharp
string sourceFilePath = MyDir + "conic_pyramid.dxf";
```

ระบุเส้นทางไปยังไฟล์รูปวาด CAD ของคุณ

## ขั้นตอนที่ 3: ตั้งค่าเส้นทางเอาต์พุต

```csharp
var outPath = Path.Combine(MyDir, "FreePointOfView_out.jpg");
```

กำหนดเส้นทางที่จะบันทึกแบบร่าง CAD ที่ถูกจัดการ

## ขั้นตอนที่ 4: โหลดอิมเมจ CAD

```csharp
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
```

โหลดแบบร่าง CAD โดยใช้ Aspose.CAD

## ขั้นตอนที่ 5: กำหนดค่าตัวเลือก JPEG

```csharp
JpegOptions options = new JpegOptions
{
    VectorRasterizationOptions = new CadRasterizationOptions
    {
        PageWidth = 1500, PageHeight = 1500
    }
};
```

กำหนดค่าตัวเลือกสำหรับการส่งออกแบบร่าง CAD เป็นรูปแบบ JPEG

## ขั้นตอนที่ 6: ตั้งค่ามุมการหมุน

```csharp
float xAngle = 10; //มุมการหมุนตามแนวแกน X
float yAngle = 30; //มุมการหมุนตามแนวแกน Y
float zAngle = 40; //มุมการหมุนตามแนวแกน Z
((CadRasterizationOptions)(options.VectorRasterizationOptions)).ObserverPoint = new ObserverPoint(xAngle, yAngle, zAngle);
```

ระบุมุมการหมุนตามแกน X, Y และ Z เพื่อให้ได้มุมมองที่ต้องการ

## ขั้นตอนที่ 7: บันทึกการวาด CAD ที่ปรับแต่งแล้ว

```csharp
cadImage.Save(outPath, options);
}
```

บันทึกแบบร่าง CAD ที่ถูกจัดการไปยังเส้นทางเอาต์พุตที่ระบุ

## ขั้นตอนที่ 8: แสดงข้อความแสดงความสำเร็จ

```csharp
Console.WriteLine("\n3D images exported successfully to JPEG.\nFile saved at " + outPath);
```

แจ้งให้ผู้ใช้ทราบเกี่ยวกับการส่งออกภาพ 3 มิติได้สำเร็จ

## บทสรุป

ในบทช่วยสอนนี้ เราได้สำรวจกระบวนการรับมุมมองฟรีในแบบร่าง CAD โดยใช้ Aspose.CAD สำหรับ .NET ด้วยการทำตามคำแนะนำทีละขั้นตอนเหล่านี้ คุณจะสามารถเพิ่มความสามารถในการแสดงภาพ CAD ของคุณและนำเสนอการออกแบบของคุณด้วยมุมมองที่ค้นพบใหม่


## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถใช้ Aspose.CAD สำหรับ .NET กับไฟล์ CAD รูปแบบอื่นได้หรือไม่

A1: ใช่ Aspose.CAD สำหรับ .NET รองรับไฟล์ CAD หลากหลายรูปแบบ รวมถึง DWG และ DXF

### คำถามที่ 2: Aspose.CAD มีเวอร์ชันทดลองใช้งานหรือไม่

 A2: ได้ คุณสามารถดาวน์โหลดเวอร์ชันทดลองใช้ฟรีได้จาก[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 3: ฉันจะขอรับใบอนุญาตชั่วคราวสำหรับ Aspose.CAD ได้อย่างไร

 A3: คุณสามารถขอรับใบอนุญาตชั่วคราวได้จาก[ที่นี่](https://purchase.aspose.com/temporary-license/).

### คำถามที่ 4: ฉันจะรับการสนับสนุนเพิ่มเติมสำหรับ Aspose.CAD ได้ที่ไหน

 A4: เยี่ยมชม[ฟอรั่ม Aspose.CAD](https://forum.aspose.com/c/cad/19) สำหรับการสนับสนุนและการอภิปรายของชุมชน

### คำถามที่ 5: ฉันสามารถปรับแต่งตัวเลือกการส่งออกสำหรับรูปแบบรูปภาพต่างๆ ได้หรือไม่

A5: แน่นอน! Aspose.CAD มีตัวเลือกมากมายสำหรับการปรับแต่ง ซึ่งช่วยให้คุณปรับแต่งกระบวนการส่งออกให้ตรงกับความต้องการเฉพาะของคุณได้
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
