---
title: รับขนาดของเค้าโครง CAD ใน Aspose.CAD สำหรับ .NET
linktitle: รับขนาดของเค้าโครง CAD
second_title: Aspose.CAD .NET - รูปแบบไฟล์ CAD และ BIM
description: เรียนรู้วิธีดึงข้อมูลขนาดเค้าโครง CAD ใน .NET โดยใช้ Aspose.CAD ปฏิบัติตามคำแนะนำทีละขั้นตอนของเราเพื่อการจัดการไฟล์ CAD ที่มีประสิทธิภาพ
type: docs
weight: 14
url: /th/net/cad-drawing-manipulation/get-size-of-cad-layout/
---
## การแนะนำ

ยินดีต้อนรับสู่คำแนะนำที่ครอบคลุมเกี่ยวกับการกำหนดขนาดของเค้าโครง CAD โดยใช้ Aspose.CAD สำหรับ .NET Aspose.CAD เป็นไลบรารีอันทรงพลังที่ช่วยให้นักพัฒนาสามารถทำงานกับไฟล์ CAD ได้อย่างราบรื่น ในบทช่วยสอนนี้ เราจะแนะนำคุณตลอดกระบวนการดึงขนาดของเค้าโครง CAD โดยใช้ตัวอย่างที่ใช้งานได้จริงและคำแนะนำทีละขั้นตอน

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเจาะลึกบทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

-  Aspose.CAD สำหรับ .NET: ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้งไลบรารี Aspose.CAD แล้ว คุณสามารถดาวน์โหลดได้จาก[หน้าดาวน์โหลด Aspose.CAD สำหรับ .NET](https://releases.aspose.com/cad/net/).

- ไฟล์เอกสาร: เตรียมไฟล์ CAD ที่คุณต้องการใช้งาน บทช่วยสอนนี้ใช้ "conic_pyramid.dxf" และ "Bottom_plate.dwg" เป็นตัวอย่าง

เอาล่ะ มาเริ่มกันเลย!

## นำเข้าเนมสเปซ

ในโปรเจ็กต์ .NET ของคุณ ให้เริ่มด้วยการนำเข้าเนมสเปซที่จำเป็น:

```csharp
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.ImageOptions;
```

## ขั้นตอนที่ 1: ตั้งค่าไดเร็กทอรีเอกสาร

 กำหนดเส้นทางไปยังไดเร็กทอรีเอกสารของคุณ แทนที่`"Your Document Directory"` กับเส้นทางที่แท้จริง

```csharp
string MyDir = "Your Document Directory";
```

## ขั้นตอนที่ 2: ระบุเส้นทางไฟล์ CAD

กำหนดอาร์เรย์ของเส้นทางไฟล์ CAD ที่คุณต้องการวิเคราะห์ ในตัวอย่างนี้ เราใช้ "conic_pyramid.dxf" และ "Bottom_plate.dwg"

```csharp
string[] sourceFilePaths = new[]
{
    MyDir + "conic_pyramid.dxf",
    MyDir + "Bottom_plate.dwg"
};
```

## ขั้นตอนที่ 3: วนซ้ำผ่านไฟล์ CAD

วนซ้ำไฟล์ CAD แต่ละไฟล์และดึงข้อมูลเค้าโครง

```csharp
foreach (var sourceFilePath in sourceFilePaths)
{
    string extension = Path.GetExtension(sourceFilePath);
    using (CadImage cadImage = (CadImage)Aspose.CAD.Image.Load(sourceFilePath))
    {
        // ... (ไปยังขั้นตอนต่อไป)
    }
}
```

## ขั้นตอนที่ 4: รับเลย์เอาต์ที่ไม่ว่างเปล่า

กำหนดวิธีการช่วยเหลือเพื่อรับเค้าโครงที่ไม่ว่างเปล่าตามประเภทไฟล์ CAD

```csharp
private static List<string> GetNotEmptyLayouts(Image cadImage, string extension)
{
    // ... (ไปยังขั้นตอนต่อไป)
}
```

## ขั้นตอนที่ 5: รับเลย์เอาต์สำหรับไฟล์ DWG

ใช้ตรรกะเพื่อดึงข้อมูลเค้าโครงที่ไม่ว่างเปล่าสำหรับไฟล์ DWG

```csharp
private static List<string> GetNotEmptyLayoutsForDwg(CadImage cadImage)
{
    // ... (ไปยังขั้นตอนต่อไป)
}
```

## ขั้นตอนที่ 6: รับเลย์เอาต์สำหรับไฟล์ DXF

ใช้ตรรกะเพื่อดึงข้อมูลเค้าโครงที่ไม่ว่างเปล่าสำหรับไฟล์ DXF

```csharp
private static List<string> GetNotEmptyLayoutsForDxf(CadImage cadImage)
{
    // ... (ไปยังขั้นตอนต่อไป)
}
```

## ขั้นตอนที่ 7: ดึงขนาดเค้าโครงและบันทึกเป็นรูปภาพ

เสร็จสิ้นขั้นตอนการรับขนาดเค้าโครงและบันทึกเป็นรูปภาพ

```csharp
foreach (string layout in layouts)
{
    // ... (ไปยังขั้นตอนต่อไป)
}
```

## บทสรุป

ยินดีด้วย! คุณได้เรียนรู้วิธีเพิ่มขนาดของเค้าโครง CAD โดยใช้ Aspose.CAD สำหรับ .NET เรียบร้อยแล้ว บทช่วยสอนนี้ครอบคลุมขั้นตอนที่สำคัญ ตั้งแต่การตั้งค่าโปรเจ็กต์ของคุณไปจนถึงการดึงข้อมูลเลย์เอาต์และบันทึกเป็นรูปภาพ ตอนนี้คุณสามารถรวมความรู้นี้เข้ากับแอปพลิเคชัน .NET ของคุณเพื่อการจัดการไฟล์ CAD ที่มีประสิทธิภาพ

## คำถามที่พบบ่อย

### คำถามที่ 1: Aspose.CAD เข้ากันได้กับไฟล์ CAD ทุกรูปแบบหรือไม่

A1: ใช่ Aspose.CAD รองรับไฟล์ CAD หลากหลายรูปแบบ รวมถึง DWG และ DXF

### คำถามที่ 2: ฉันสามารถปรับแต่งตัวเลือกการบันทึกรูปภาพได้หรือไม่

A2: แน่นอน! คุณสามารถปรับตัวเลือกรูปภาพ เช่น รูปแบบและความละเอียด เพื่อให้ตรงตามความต้องการเฉพาะของคุณได้

### คำถามที่ 3: ฉันจะหาเอกสารเพิ่มเติมได้จากที่ไหน?

 A3: โปรดดูที่[เอกสาร Aspose.CAD](https://reference.aspose.com/cad/net/) สำหรับข้อมูลโดยละเอียดและตัวอย่าง

### คำถามที่ 4: มีการทดลองใช้ฟรีหรือไม่?

 A4: ได้ คุณสามารถสำรวจ Aspose.CAD ได้ด้วย[ทดลองฟรี](https://releases.aspose.com/).

### ไตรมาสที่ 5; ฉันจะได้รับการสนับสนุนทางเทคนิคได้อย่างไร?

 A5: สำหรับการสนับสนุนด้านเทคนิค โปรดไปที่[ฟอรั่ม Aspose.CAD](https://forum.aspose.com/c/cad/19).