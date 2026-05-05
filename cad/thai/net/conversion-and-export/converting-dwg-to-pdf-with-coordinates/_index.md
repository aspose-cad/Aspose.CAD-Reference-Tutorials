---
date: 2026-04-03
description: เรียนรู้วิธีตั้งค่า viewport และแปลง DWG เป็น PDF ด้วย C# โดยใช้ Aspose.CAD.
  บทเรียนการแปลง DWG เป็น PDF นี้แสดงการส่งออกที่แม่นยำพร้อมพิกัด.
keywords:
- how to set viewport
- dwg to pdf tutorial
- convert dwg to pdf c#
linktitle: การแปลง DWG เป็น PDF พร้อมพิกัดใน C#
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: วิธีตั้ง Viewport ขณะแปลง DWG เป็น PDF พร้อมพิกัดใน C# - บทแนะนำ Aspose.CAD
url: /th/net/conversion-and-export/converting-dwg-to-pdf-with-coordinates/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# การแปลง DWG เป็น PDF พร้อมพิกัดใน C# - บทแนะนำ Aspose.CAD

## บทนำ

ยินดีต้อนรับสู่บทแนะนำที่ครอบคลุมนี้เกี่ยวกับ **วิธีตั้ง viewport** ขณะแปลงไฟล์ DWG เป็น PDF พร้อมพิกัดที่ระบุโดยใช้ Aspose.CAD สำหรับ .NET การควบคุม viewport จะทำให้คุณได้ PDF ที่พิกเซลแม่นยำตรงกับพื้นที่ที่ต้องการ—เหมาะสำหรับแบบแปลนการก่อสร้าง, ตัวอย่างแผนผังชั้น, หรือกระบวนการทำงาน BIM ใด ๆ

## คำตอบอย่างรวดเร็ว
- **การตั้ง viewport** หมายความว่าอะไร? มันกำหนดพื้นที่ที่มองเห็นและการสเกลของการวาด CAD ระหว่างการเรสเตอร์ไลซ์  
- **ไลบรารีใดจัดการการแปลง?** Aspose.CAD for .NET.  
- **ฉันต้องการไลเซนส์หรือไม่?** เวอร์ชันทดลองฟรีใช้ได้สำหรับการประเมิน; ต้องมีไลเซนส์เชิงพาณิชย์สำหรับการใช้งานจริง.  
- **แพลตฟอร์มที่รองรับ?** Windows, Linux, macOS พร้อม .NET 5/6/7 หรือ .NET Framework 4.6+.  
- **เวลาในการดำเนินการโดยทั่วไป?** ประมาณ 10‑15 นาทีสำหรับการแปลงพื้นฐาน.

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเริ่ม, โปรดตรวจสอบว่าคุณมีข้อกำหนดต่อไปนี้:

- **Aspose.CAD Library** – ดาวน์โหลดและติดตั้งไลบรารี Aspose.CAD สำหรับ .NET คุณสามารถหาไลบรารีได้จาก [ที่นี่](https://releases.aspose.com/cad/net/).  
- **สภาพแวดล้อมการพัฒนา** – Visual Studio, Rider หรือ IDE ใด ๆ ที่รองรับการพัฒนา .NET.  
- **ไฟล์ DWG** – มีไฟล์ DWG พร้อมสำหรับการแปลง คุณสามารถใช้ไฟล์ตัวอย่างที่ให้ไว้หรือไฟล์ DWG ของคุณเอง.

## วิธีตั้ง Viewport สำหรับการส่งออก PDF อย่างแม่นยำ

การตั้ง viewport เป็นขั้นตอนหลักที่ให้คุณกำหนดพื้นที่ที่ต้องการเรนเดอร์ของการวาด เราในโค้ดด้านล่างจะสร้าง `CadVportTableObject` ใหม่, กำหนดตำแหน่งด้วยพิกัดบน‑ซ้าย, และคำนวณความกว้าง, ความสูง, และอัตราส่วน นี่คือการทำ **วิธีตั้ง viewport** ที่เป็นพื้นฐานของการแปลงทั้งหมด.

## นำเข้า Namespaces

ในโปรเจกต์ C# ของคุณ, ให้นำเข้า namespaces ที่จำเป็น:

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

มาทำความเข้าใจโค้ดทีละขั้นตอนเพื่อความเข้าใจที่ดีขึ้น:

## ขั้นตอนที่ 1: กำหนดไดเรกทอรีเอกสาร

```csharp
string MyDir = "Your Document Directory";
```

## ขั้นตอนที่ 2: ตั้งค่าพาธไฟล์ DWG แหล่งที่มา

```csharp
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";
```

## ขั้นตอนที่ 3: โหลดไฟล์ DWG และกำหนดตัวเลือกการเรสเตอร์ไลซ์

```csharp
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
    rasterizationOptions.Layouts = new string[] { "Model" };
    rasterizationOptions.NoScaling = true;
```

## ขั้นตอนที่ 4: กำหนดพิกัดและ Viewport  

ที่นี่เราจริง ๆ **ตั้ง viewport** (วิธีตั้ง viewport) โดยระบุมุมบน‑ซ้าย, ความกว้าง, และความสูงของพื้นที่ที่ต้องการส่งออก.

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

## ขั้นตอนที่ 5: ใช้การตั้งค่า Viewport

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

## ขั้นตอนที่ 6: กำหนดตัวเลือก PDF และส่งออก  

ตอนนี้เราจะรวมทุกอย่างและ **แปลง DWG เป็น PDF** โดยใช้ตัวเลือกการเรสเตอร์ไลซ์ที่เตรียมไว้.

```csharp
    Aspose.CAD.ImageOptions.PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions();
    pdfOptions.VectorRasterizationOptions = rasterizationOptions;

    MyDir = MyDir + "ConvertDWGToPDFBySupplyingCoordinates_out.pdf";
    cadImage.Save(MyDir, pdfOptions);
}
```

## ขั้นตอนที่ 7: แสดงข้อความสำเร็จ

```csharp
Console.WriteLine("\nThe DWG file exported successfully to PDF.\nFile saved at " + MyDir);
```

## กรณีการใช้งานทั่วไป

- **เอกสารการก่อสร้าง** – สร้าง PDF ที่พิมพ์ได้ของส่วนแผนผังชั้นที่ระบุ.  
- **การประสานงาน BIM** – ส่งออกเฉพาะพื้นที่ที่สนใจสำหรับการตรวจสอบการชนกัน.  
- **การนำเสนอให้ลูกค้า** – ให้ PDF ที่สะอาดของห้องหรือมุมมองที่เลือกโดยไม่เปิดเผยการวาดทั้งหมด.

## สรุป

ยินดีด้วย! คุณได้ **แปลง DWG เป็น PDF** อย่างแม่นยำด้วยพิกัดและเรียนรู้ **วิธีตั้ง viewport** ด้วย Aspose.CAD สำหรับ .NET บทแนะนำ **dwg to pdf tutorial** นี้แสดงวิธี **สร้าง pdf จาก dwg** และ **ส่งออก dwg เป็น pdf c#** พร้อมควบคุมพื้นที่ผลลัพธ์อย่างเต็มที่.

## คำถามที่พบบ่อย

### Q1: ฉันสามารถใช้ Aspose.CAD กับรูปแบบไฟล์ CAD อื่นได้หรือไม่?

A1: ใช่, Aspose.CAD รองรับรูปแบบ CAD ต่าง ๆ รวมถึง DWG, DXF, DWF, และอื่น ๆ

### Q2: ฉันจะจัดการข้อผิดพลาดระหว่างกระบวนการแปลงอย่างไร?

A2: ใช้กลไกการจัดการข้อผิดพลาดด้วยบล็อก try‑catch เพื่อจับและจัดการข้อยกเว้น.

### Q3: Aspose.CAD เหมาะกับสภาพแวดล้อม Windows และ Linux หรือไม่?

A3: ใช่, Aspose.CAD เข้ากันได้กับทั้งแพลตฟอร์ม Windows และ Linux.

### Q4: ฉันสามารถปรับแต่งผลลัพธ์ PDF เพิ่มเติมได้หรือไม่?

A4: แน่นอน! สำรวจตัวเลือกที่หลากหลายที่ Aspose.CAD มีให้เพื่อปรับผลลัพธ์ PDF ให้ตรงกับความต้องการของคุณ.

### Q5: ฉันจะหาแหล่งสนับสนุนเพิ่มเติมหรือการสนทนาชุมชนได้ที่ไหน?

A5: Visit the [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19) for community support and discussions.

## คำถามที่พบบ่อยเพิ่มเติม

**ถาม: วิธีนี้ทำงานกับไฟล์ DWG ขนาดใหญ่ (หลายร้อย MB) หรือไม่?**  
**ตอบ:** ใช่. การเรสเตอร์ไลซ์ทำเป็นหน้า‑ต่อหน้า, และคุณสามารถปรับ `rasterizationOptions` (เช่น `Resolution`) เพื่อสมดุลคุณภาพและการใช้หน่วยความจำ.

**ถาม: ฉันสามารถส่งออกหลาย viewport ไปยังหน้า PDF แยกกันได้หรือไม่?**  
**ตอบ:** คุณสามารถวนลูป `cadImage.ViewPorts`, ตั้งแต่ละอันเป็น active, แล้วเรียก `Save` สำหรับแต่ละหน้า, จากนั้นรวม PDF ด้วย Aspose.PDF.

**ถาม: สามารถเพิ่มลายน้ำลงใน PDF ที่สร้างขึ้นได้หรือไม่?**  
**ตอบ:** หลังจากบันทึก PDF, คุณสามารถเปิดใหม่ด้วย Aspose.PDF และใส่ลายน้ำข้อความหรือรูปภาพก่อนส่งให้ผู้ใช้.

---

**Last Updated:** 2026-04-03  
**Tested With:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}