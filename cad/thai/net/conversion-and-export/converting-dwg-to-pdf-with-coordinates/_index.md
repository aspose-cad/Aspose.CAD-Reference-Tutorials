---
title: การแปลง DWG เป็น PDF ด้วยพิกัดใน C # - บทช่วยสอน Aspose.CAD
linktitle: การแปลง DWG เป็น PDF ด้วยพิกัดใน C #
second_title: Aspose.CAD .NET - รูปแบบไฟล์ CAD และ BIM
description: เรียนรู้วิธีแปลง DWG เป็น PDF ด้วยพิกัดเฉพาะใน C# โดยใช้ Aspose.CAD ปฏิบัติตามคำแนะนำทีละขั้นตอนของเราเพื่อการแปลงไฟล์ CAD ที่แม่นยำและมีประสิทธิภาพ
type: docs
weight: 11
url: /th/net/conversion-and-export/converting-dwg-to-pdf-with-coordinates/
---
## การแนะนำ

ยินดีต้อนรับสู่บทช่วยสอนที่ครอบคลุมเกี่ยวกับการแปลงไฟล์ DWG เป็น PDF ด้วยพิกัดที่ระบุโดยใช้ Aspose.CAD สำหรับ .NET Aspose.CAD เป็นไลบรารีอันทรงพลังที่ช่วยให้นักพัฒนาทำงานกับรูปแบบไฟล์ CAD ในแอปพลิเคชัน .NET ของตนได้อย่างราบรื่น ในบทช่วยสอนนี้ เราจะแนะนำคุณตลอดขั้นตอนการแปลงไฟล์ DWG เป็น PDF พร้อมทั้งระบุพิกัดเฉพาะเพื่อเพิ่มความแม่นยำ

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเริ่มต้น ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นดังต่อไปนี้:

- ไลบรารี Aspose.CAD: ดาวน์โหลดและติดตั้งไลบรารี Aspose.CAD สำหรับ .NET คุณสามารถค้นหาห้องสมุด[ที่นี่](https://releases.aspose.com/cad/net/).

- สภาพแวดล้อมการพัฒนา: ตรวจสอบให้แน่ใจว่าคุณได้ตั้งค่าสภาพแวดล้อมการพัฒนาที่เข้ากันได้ รวมถึง Visual Studio หรือ IDE ที่ต้องการอื่นๆ

- ไฟล์ DWG: เตรียมไฟล์ DWG พร้อมสำหรับการแปลง คุณสามารถใช้ไฟล์ตัวอย่างที่ให้มาหรือไฟล์ DWG ที่คุณกำหนดเองได้

## นำเข้าเนมสเปซ

ในโปรเจ็กต์ C# ของคุณ ให้นำเข้าเนมสเปซที่จำเป็น:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadParameters;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.ImageOptions;
```

มาแบ่งโค้ดออกเป็นคำแนะนำทีละขั้นตอนเพื่อความเข้าใจที่ดีขึ้น:

## ขั้นตอนที่ 1: กำหนดไดเร็กทอรีเอกสาร

```csharp
string MyDir = "Your Document Directory";
```

## ขั้นตอนที่ 2: ตั้งค่าเส้นทางไฟล์ DWG ต้นทาง

```csharp
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";
```

## ขั้นตอนที่ 3: โหลดไฟล์ DWG และกำหนดค่าตัวเลือกการแรสเตอร์

```csharp
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
    rasterizationOptions.Layouts = new string[] { "Model" };
    rasterizationOptions.NoScaling = true;
```

## ขั้นตอนที่ 4: กำหนดพิกัดและวิวพอร์ต

```csharp
    Point topLeft = new Point(500, 1000);
    double width = 3108;
    double height = 2489;

    CadVportTableObject newView = new CadVportTableObject();
    newView.Name = new CadStringParameter();
    newView.Name.Init("*Active");
    newView.CenterPoint.X = topLeft.X + width / 2f;
    newView.CenterPoint.Y = topLeft.Y - height / 2f;
    newView.ViewHeight.Value = height;
    newView.ViewAspectRatio.Value = width / height;
```

## ขั้นตอนที่ 5: ใช้การตั้งค่าวิวพอร์ต

```csharp
    for (int i = 0; i < cadImage.ViewPorts.Count; i++)
    {
        CadVportTableObject currentView = (CadVportTableObject)(cadImage.ViewPorts[i]);
        if (cadImage.ViewPorts.Count == 1 || string.Equals(currentView.Name.Value.ToLowerInvariant(), "*active"))
        {
            cadImage.ViewPorts[i] = newView;
            break;
        }
    }
```

## ขั้นตอนที่ 6: กำหนดค่าตัวเลือก PDF และส่งออก

```csharp
    Aspose.CAD.ImageOptions.PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions();
    pdfOptions.VectorRasterizationOptions = rasterizationOptions;

    MyDir = MyDir + "ConvertDWGToPDFBySupplyingCoordinates_out.pdf";
    cadImage.Save(MyDir, pdfOptions);
}
```

## ขั้นตอนที่ 7: แสดงข้อความแสดงความสำเร็จ

```csharp
Console.WriteLine("\nThe DWG file exported successfully to PDF.\nFile saved at " + MyDir);
```

## บทสรุป

ยินดีด้วย! คุณได้แปลงไฟล์ DWG เป็น PDF ด้วยพิกัดที่ระบุสำเร็จแล้วโดยใช้ Aspose.CAD สำหรับ .NET บทช่วยสอนนี้ครอบคลุมขั้นตอนสำคัญและให้คำแนะนำที่ชัดเจนสำหรับนักพัฒนา

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถใช้ Aspose.CAD กับไฟล์ CAD รูปแบบอื่นได้หรือไม่

A1: ใช่ Aspose.CAD รองรับรูปแบบ CAD หลากหลาย รวมถึง DWG, DXF, DWF และอื่นๆ

### คำถามที่ 2: ฉันจะจัดการกับข้อผิดพลาดระหว่างกระบวนการแปลงได้อย่างไร

ตอบ 2: ใช้กลไกการจัดการข้อผิดพลาดโดยใช้บล็อก try-catch เพื่อจับภาพและจัดการข้อยกเว้น

### คำถามที่ 3: Aspose.CAD เหมาะสำหรับทั้งสภาพแวดล้อม Windows และ Linux หรือไม่

A3: ใช่ Aspose.CAD เข้ากันได้กับทั้งแพลตฟอร์ม Windows และ Linux

### คำถามที่ 4: ฉันสามารถปรับแต่งเอาต์พุต PDF เพิ่มเติมได้หรือไม่

A4: แน่นอน! สำรวจตัวเลือกมากมายจาก Aspose.CAD เพื่อปรับแต่งเอาต์พุต PDF ให้ตรงตามความต้องการเฉพาะของคุณ

### คำถามที่ 5: ฉันจะรับการสนับสนุนเพิ่มเติมหรือการสนทนาในชุมชนได้จากที่ไหน

A5: เยี่ยมชม[ฟอรั่ม Aspose.CAD](https://forum.aspose.com/c/cad/19) สำหรับการสนับสนุนและการอภิปรายของชุมชน