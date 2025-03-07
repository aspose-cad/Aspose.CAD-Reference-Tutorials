---
title: การส่งออกวัตถุ OLE จากไฟล์ DWG - บทช่วยสอน Aspose.CAD
linktitle: การส่งออกวัตถุ OLE จากไฟล์ DWG
second_title: Aspose.CAD .NET - รูปแบบไฟล์ CAD และ BIM
description: สำรวจคำแนะนำทีละขั้นตอนในการส่งออกออบเจ็กต์ OLE จากไฟล์ DWG โดยใช้ Aspose.CAD สำหรับ .NET เสริมทักษะการจัดการไฟล์ CAD ของคุณได้อย่างง่ายดาย
weight: 12
url: /th/net/advanced-export-techniques/exporting-ole-objects-from-dwg/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# การส่งออกวัตถุ OLE จากไฟล์ DWG - บทช่วยสอน Aspose.CAD

## การแนะนำ

คุณต้องการแยกวัตถุ OLE ออกจากไฟล์ DWG อย่างง่ายดายหรือไม่? Aspose.CAD สำหรับ .NET พร้อมที่จะปรับปรุงกระบวนการให้กับคุณ ในบทช่วยสอนนี้ เราจะแนะนำคุณตลอดขั้นตอนการส่งออกออบเจ็กต์ OLE ทีละขั้นตอน เพื่อให้มั่นใจว่าคุณจะได้ประโยชน์สูงสุดจากไลบรารี .NET อันทรงพลังนี้ 

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเจาะลึกบทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

-  Aspose.CAD สำหรับ .NET Library: ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้งไลบรารีแล้ว คุณสามารถดาวน์โหลดได้จาก[หน้าดาวน์โหลด Aspose.CAD สำหรับ .NET](https://releases.aspose.com/cad/net/).

-  ไดเร็กทอรีเอกสาร: ตั้งค่าไดเร็กทอรีที่เก็บไฟล์ DWG ของคุณ แทนที่`"Your Document Directory"` ในข้อมูลโค้ดที่ให้มาพร้อมกับเส้นทางจริง

## นำเข้าเนมสเปซ

ในโปรเจ็กต์ .NET ของคุณ คุณจะต้องนำเข้าเนมสเปซที่จำเป็นเพื่อใช้ประโยชน์จากฟังก์ชัน Aspose.CAD ใช้ข้อมูลโค้ดต่อไปนี้:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## ขั้นตอนที่ 1: ตั้งค่าไดเร็กทอรีเอกสาร

```csharp
string MyDir = "Your Document Directory";
```

 แทนที่`"Your Document Directory"` ด้วยเส้นทางที่มีไฟล์ DWG ของคุณอยู่

## ขั้นตอนที่ 2: ระบุไฟล์ DWG

```csharp
string[] files = new string[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

แสดงรายการไฟล์ DWG ที่คุณต้องการประมวลผลภายในอาร์เรย์

## ขั้นตอนที่ 3: กำหนดค่าตัวเลือกการส่งออก

```csharp
PngOptions pngOptions = new PngOptions { };
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.VectorRasterizationOptions = rasterizationOptions;
rasterizationOptions.Layouts = new string[] { "Layout1" };
```

ปรับแต่งตัวเลือกการส่งออกตามความต้องการของคุณ ในตัวอย่างนี้ เรากำหนดค่าการส่งออก PNG ด้วยเค้าโครงที่ระบุ

## ขั้นตอนที่ 4: วนซ้ำไฟล์และส่งออก

```csharp
foreach (string file in files)
{
    using (CadImage cadImage = (CadImage)Image.Load(MyDir + file))
    {
        cadImage.Save(MyDir + file + "_out.png", pngOptions);
    }
}
```

วนซ้ำไฟล์ DWG ที่ระบุ โหลดแต่ละไฟล์ และบันทึกไฟล์ PNG ที่ส่งออกด้วยตัวเลือกที่กำหนดไว้

## บทสรุป

ยินดีด้วย! คุณได้ส่งออกวัตถุ OLE จากไฟล์ DWG โดยใช้ Aspose.CAD สำหรับ .NET เรียบร้อยแล้ว ไลบรารีอันทรงพลังนี้ทำให้งานที่ซับซ้อนง่ายขึ้น โดยให้ประสิทธิภาพและความยืดหยุ่นในการจัดการไฟล์ CAD

## คำถามที่พบบ่อย

### คำถามที่ 1: Aspose.CAD สำหรับ .NET เหมาะสำหรับไฟล์ CAD ระดับจูเนียร์และระดับสูงหรือไม่

ตอบ 1: ใช่ Aspose.CAD สำหรับ .NET มีความหลากหลายและสามารถจัดการไฟล์ CAD ได้หลากหลาย รวมถึงรุ่นรองและรุ่นอาวุโส

### คำถามที่ 2: ฉันสามารถปรับแต่งตัวเลือกการส่งออกสำหรับเลย์เอาต์ต่างๆ ได้หรือไม่

A2: แน่นอน! ดังที่แสดงในบทช่วยสอน คุณสามารถปรับแต่งตัวเลือกการส่งออก รวมถึงเค้าโครง เพื่อให้เหมาะกับความต้องการเฉพาะของคุณได้

### คำถามที่ 3: ฉันจะหาเอกสารโดยละเอียดสำหรับ Aspose.CAD สำหรับ .NET ได้ที่ไหน

 A3: สำรวจ[Aspose.CAD สำหรับเอกสาร .NET](https://reference.aspose.com/cad/net/) สำหรับข้อมูลเชิงลึกและตัวอย่าง

### คำถามที่ 4: มีการทดลองใช้ฟรีหรือไม่?

 ตอบ 4: ได้ คุณสามารถสัมผัสประสบการณ์ความสามารถของ Aspose.CAD สำหรับ .NET ได้ด้วยการทดลองใช้ฟรี เยี่ยม[ลิงค์นี้](https://releases.aspose.com/) ที่จะเริ่มต้น.

### คำถามที่ 5: ฉันจะรับการสนับสนุนหรือเชื่อมต่อกับชุมชนได้อย่างไร

 A5: สำหรับการสนับสนุนและการมีส่วนร่วมของชุมชน โปรดไปที่[ฟอรั่ม Aspose.CAD](https://forum.aspose.com/c/cad/19).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
