---
title: การแสดงผลเอกสาร DWG ใน C# - คู่มือ Aspose.CAD
linktitle: การแสดงผลเอกสาร DWG ใน C #
second_title: Aspose.CAD .NET - รูปแบบไฟล์ CAD และ BIM
description: เรียนรู้วิธีเรนเดอร์เอกสาร DWG ใน C# โดยใช้ Aspose.CAD คำแนะนำทีละขั้นตอนนี้ครอบคลุมถึงการนำเข้า การกำหนดค่า และการบันทึกพร้อมตัวอย่างโค้ด
weight: 17
url: /th/net/image-manipulation-and-rendering/rendering-dwg-documents/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# การแสดงผลเอกสาร DWG ใน C# - คู่มือ Aspose.CAD

## การแนะนำ

ยินดีต้อนรับสู่คำแนะนำที่ครอบคลุมเกี่ยวกับการเรนเดอร์เอกสาร DWG ใน C# โดยใช้ Aspose.CAD ไม่ว่าคุณจะเป็นนักพัฒนาที่มีประสบการณ์หรือเพิ่งเริ่มต้นด้วย .NET บทช่วยสอนนี้จะแนะนำคุณตลอดกระบวนการใช้ประโยชน์จาก Aspose.CAD เพื่อเรนเดอร์ไฟล์ DWG อย่างมีประสิทธิภาพ Aspose.CAD เป็น API ที่ทรงพลังซึ่งมีฟังก์ชันการทำงานที่มีประสิทธิภาพสำหรับการทำงานกับรูปแบบไฟล์ CAD ทำให้เป็นตัวเลือกสำหรับนักพัฒนาที่เกี่ยวข้องกับไฟล์ DWG

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเข้าสู่บทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

- ความรู้พื้นฐานเกี่ยวกับภาษาการเขียนโปรแกรม C#
- ติดตั้ง Visual Studio บนเครื่องของคุณแล้ว
-  ไลบรารี Aspose.CAD รวมอยู่ในโปรเจ็กต์ของคุณ คุณสามารถดาวน์โหลดได้จาก[ที่นี่](https://releases.aspose.com/cad/net/).
- ไฟล์ DWG ตัวอย่าง เช่น "Bottom_plate.dwg" ที่ต้องติดตามพร้อมกับตัวอย่าง

## นำเข้าเนมสเปซ

ในการเริ่มต้น ตรวจสอบให้แน่ใจว่าได้นำเข้าเนมสเปซที่จำเป็นที่จุดเริ่มต้นของโค้ด C# ของคุณ:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.FileFormats.Cad;
```

ตอนนี้ เรามาแบ่งตัวอย่างที่ให้ไว้ออกเป็นหลายขั้นตอน:

## ขั้นตอนที่ 1: โหลดไฟล์ DWG

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // รหัสของคุณสำหรับการโหลดไฟล์ DWG อยู่ที่นี่
}
```

## ขั้นตอนที่ 2: กำหนดค่าตัวเลือกการแรสเตอร์

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new string[] { "Model" };
rasterizationOptions.NoScaling = true;
//คุณสามารถเพิ่มการกำหนดค่าแรสเตอร์เพิ่มเติมได้ที่นี่
```

## ขั้นตอนที่ 3: กำหนดภูมิภาคที่จะวาด

```csharp
Point topLeft = new Point(6156, 7053);
double width = 3108;
double height = 2489;
```

## ขั้นตอนที่ 4: สร้างวิวพอร์ตใหม่

```csharp
CadVportTableObject newView = new CadVportTableObject();
newView.Name.Value = "*Active";
newView.CenterPoint.X = topLeft.X + width / 2f;
newView.CenterPoint.Y = topLeft.Y - height / 2f;
newView.ViewHeight.Value = height;
newView.ViewAspectRatio.Value = width / height;
```

## ขั้นตอนที่ 5: แทนที่ Active Viewport

```csharp
for (int i = 0; i < cadImage.ViewPorts.Count; i++)
{
    CadVportTableObject currentView = (CadVportTableObject)(cadImage.ViewPorts[i]);
    if ((currentView.Name.Value == null && cadImage.ViewPorts.Count == 1) ||
    string.Equals(currentView.Name.Value.ToLowerInvariant(), "*active"))
    {
        cadImage.ViewPorts[i] = newView;
        break;
    }
}
```

## ขั้นตอนที่ 6: กำหนดค่าตัวเลือก PDF

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## ขั้นตอนที่ 7: บันทึก DWG ที่เรนเดอร์เป็น PDF

```csharp
cadImage.Save(MyDir, pdfOptions);
```

## บทสรุป

ยินดีด้วย! คุณได้เรนเดอร์เอกสาร DWG เป็น PDF โดยใช้ Aspose.CAD ใน C# สำเร็จแล้ว สำรวจคุณสมบัติเพิ่มเติมและปรับแต่งโค้ดตามความต้องการเฉพาะของคุณได้อย่างอิสระ

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถใช้ Aspose.CAD กับไฟล์ CAD รูปแบบอื่นได้หรือไม่

A1: ใช่ Aspose.CAD รองรับรูปแบบ CAD หลากหลาย รวมถึง DWG, DXF, DWF และอื่นๆ

### คำถามที่ 2: Aspose.CAD เข้ากันได้กับ .NET Core หรือไม่

A2: ใช่ Aspose.CAD เข้ากันได้กับทั้ง .NET Framework และ .NET Core

### คำถามที่ 3: ฉันจะจัดการเลย์เอาต์ต่างๆ ในไฟล์ DWG ได้อย่างไร

 A3: คุณสามารถระบุเค้าโครงที่ต้องการได้ใน`Layouts` ทรัพย์สินของ`CadRasterizationOptions`.

### คำถามที่ 4: มีข้อควรพิจารณาในการอนุญาตให้ใช้งาน Aspose.CAD หรือไม่

 A4: สำหรับรายละเอียดใบอนุญาต โปรดไปที่[ที่นี่](https://purchase.aspose.com/buy).

### คำถามที่ 5: ฉันจะรับการสนับสนุนเพิ่มเติมได้จากที่ไหน

A5: เยี่ยมชม[ฟอรั่ม Aspose.CAD](https://forum.aspose.com/c/cad/19) สำหรับการสนับสนุนและการอภิปรายของชุมชน
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
