---
date: 2026-03-21
description: เรียนรู้วิธีดึงขนาดเลย์เอาต์ของ CAD ใน .NET ด้วย Aspose.CAD ปฏิบัติตามคู่มือขั้นตอนต่อขั้นตอนของเราเพื่อการจัดการไฟล์
  CAD อย่างมีประสิทธิภาพ
linktitle: Get Size of CAD Layout
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: รับขนาดเลย์เอาต์ CAD ใน Aspose.CAD สำหรับ .NET
url: /th/net/cad-drawing-manipulation/get-size-of-cad-layout/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# รับขนาด Layout CAD ใน Aspose.CAD สำหรับ .NET

## บทนำ

ในบทแนะนำที่ครอบคลุมนี้คุณจะได้เรียนรู้ **วิธีรับขนาด layout CAD** โดยใช้ไลบรารี Aspose.CAD สำหรับ .NET ไม่ว่าคุณจะกำลังสร้างตัวดู CAD, สร้างภาพย่อ, หรือจำเป็นต้องมีขนาด layout ที่แม่นยำสำหรับการประมวลผลต่อเนื่อง การรู้ขนาดที่แน่นอนของแต่ละ layout เป็นสิ่งสำคัญ เราจะเดินผ่านขั้นตอนทั้งหมด—from การโหลดไฟล์วาดไปจนถึงการสกัดขนาด layout และอาจบันทึกเป็นภาพ—เพื่อให้คุณสามารถผสานความสามารถนี้เข้าไปในแอปพลิเคชันของคุณได้อย่างมั่นใจ

## คำตอบอย่างรวดเร็ว
- **“get CAD layout size” หมายถึงอะไร?** หมายถึงการดึงความกว้างและความสูง (ในหน่วยของการวาด) ของแต่ละ layout ที่ไม่ว่างเปล่าในไฟล์ CAD  
- **ไลบรารีใดรองรับสิ่งนี้?** Aspose.CAD สำหรับ .NET มี API ที่ง่ายต่อการเข้าถึงข้อมูล layout  
- **ต้องมีลิขสิทธิ์หรือไม่?** สามารถใช้รุ่นทดลองฟรีสำหรับการประเมิน; ต้องมีลิขสิทธิ์เชิงพาณิชย์สำหรับการใช้งานในผลิตภัณฑ์  
- **รูปแบบที่รองรับ?** DWG, DXF และรูปแบบ CAD/BIM อื่น ๆ มากมายที่รองรับเต็มรูปแบบ  
- **เวลาการทำงานโดยประมาณ?** ประมาณ 10‑15 นาทีสำหรับการสร้างฟังก์ชันดึงขนาดพื้นฐาน  

## “get CAD layout size” คืออะไร?
การรับขนาด layout CAD หมายถึงการสกัดขอบเขตเชิงเรขาคณิตของแต่ละ layout (paper space) ที่กำหนดในไฟล์ CAD ขอบเขตเหล่านี้แสดงเป็นหน่วยดั้งเดิมของการวาด (โดยทั่วไปเป็นมิลลิเมตรหรืออินช์) และมีประโยชน์สำหรับงานเช่นการสเกล, การพิมพ์, หรือการสร้างภาพตัวอย่าง

## ทำไมต้องดึงขนาด layout CAD ด้วย Aspose.CAD?
- **ไม่ต้องใช้ซอฟต์แวร์ CAD** – ทำงานได้เต็มที่บนเซิร์ฟเวอร์  
- **ข้ามแพลตฟอร์ม** – รองรับ .NET Framework, .NET Core, และ .NET 5/6+  
- **การวัดที่แม่นยำ** – คืนค่าขอบเขตที่ตรงกับที่เก็บในไฟล์, หลีกเลี่ยงการพาร์สด้วยตนเอง  
- **การผสานที่ง่าย** – การเรียก API อย่างง่ายเข้ากับโปรเจกต์ C# ที่มีอยู่ได้อย่างเป็นธรรมชาติ  

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะลงลึกในโค้ด, โปรดตรวจสอบว่าคุณมีสิ่งต่อไปนี้:

- ติดตั้ง Aspose.CAD สำหรับ .NET แล้ว คุณสามารถดาวน์โหลดได้จาก [Aspose.CAD for .NET download page](https://releases.aspose.com/cad/net/)  
- ไฟล์ CAD หนึ่งไฟล์หรือหลายไฟล์ (DWG, DXF ฯลฯ) ที่ต้องการวิเคราะห์ คู่มือฉบับนี้ใช้ `conic_pyramid.dxf` และ `Bottom_plate.dwg` เป็นไฟล์ตัวอย่าง  

## นำเข้า Namespaces

ในโปรเจกต์ .NET ของคุณ, เริ่มต้นด้วยการนำเข้า namespace ที่จำเป็น:

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

## ขั้นตอนที่ 1: ตั้งค่าโฟลเดอร์เอกสาร

กำหนดโฟลเดอร์ที่บรรจุไฟล์ CAD ของคุณ แทนที่ตัวแปร placeholder ด้วยพาธจริงบนเครื่องของคุณ

```csharp
string MyDir = "Your Document Directory";
```

## ขั้นตอนที่ 2: ระบุพาธไฟล์ CAD

สร้างอาเรย์ที่ชี้ไปยังไฟล์ CAD แต่ละไฟล์ที่ต้องการประมวลผล

```csharp
string[] sourceFilePaths = new[]
{
    MyDir + "conic_pyramid.dxf",
    MyDir + "Bottom_plate.dwg"
};
```

## ขั้นตอนที่ 3: วนลูปผ่านไฟล์ CAD

โหลดแต่ละไฟล์, ตรวจจับรูปแบบ, และเตรียมดึงข้อมูล layout

```csharp
foreach (var sourceFilePath in sourceFilePaths)
{
    string extension = Path.GetExtension(sourceFilePath);
    using (CadImage cadImage = (CadImage)Aspose.CAD.Image.Load(sourceFilePath))
    {
        // ... (continue to the next step)
    }
}
```

## ขั้นตอนที่ 4: ดึง Layout ที่ไม่ว่างเปล่า

เราต้องการเมธอดช่วยเหลือที่คืนค่าเฉพาะ layout ที่มีเอนทิตีการวาดอยู่จริง Layout ที่ว่างเปล่าจะถูกละเว้นเพราะไม่มีขนาดให้รายงาน

```csharp
private static List<string> GetNotEmptyLayouts(Image cadImage, string extension)
{
    // ... (continue to the next step)
}
```

## ขั้นตอนที่ 5: ดึง Layout สำหรับไฟล์ DWG

ไฟล์ DWG เก็บข้อมูล layout ไว้ในตาราง `HeaderVariables` เมธอดต่อไปนี้สกัดชื่อของทุก layout ที่ไม่ว่างเปล่าสำหรับการวาด DWG

```csharp
private static List<string> GetNotEmptyLayoutsForDwg(CadImage cadImage)
{
    // ... (continue to the next step)
}
```

## ขั้นตอนที่ 6: ดึง Layout สำหรับไฟล์ DXF

ไฟล์ DXF ใช้โครงสร้างที่แตกต่างกัน เมธอดนี้พาร์สคอลเลกชัน `Tables` เพื่อค้นหา layout paper space ที่มีเอนทิตีอยู่

```csharp
private static List<string> GetNotEmptyLayoutsForDxf(CadImage cadImage)
{
    // ... (continue to the next step)
}
```

## ขั้นตอนที่ 7: ดึงขนาด Layout และบันทึกเป็นภาพ

สุดท้าย, วนลูปผ่านแต่ละ layout ที่ค้นพบ, อ่านขอบเขต, และอาจเรนเดอร์ layout ไปเป็นไฟล์ภาพเพื่อการตรวจสอบด้วยสายตา

```csharp
foreach (string layout in layouts)
{
    // ... (continue to the next step)
}
```

## ปัญหาที่พบบ่อย & เคล็ดลับ

- **Missing layout names:** ตรวจสอบให้แน่ใจว่าไฟล์ CAD มี layout paper space อยู่จริง; บางไฟล์อาจมีเฉพาะ model space เท่านั้น  
- **Incorrect units:** ขนาดจะถูกคืนค่าในหน่วยดั้งเดิมของการวาด; แปลงเป็นมิลลิเมตรหรืออินช์หากต้องการ  
- **Performance:** การโหลดไฟล์ DWG/DXF ขนาดใหญ่มากอาจใช้หน่วยความจำสูง; พิจารณาประมวลผลแบบอะซิงโครนัสหรือเป็นชุด  

## คำถามที่พบบ่อย

**Q: Aspose.CAD รองรับรูปแบบไฟล์ CAD ทั้งหมดหรือไม่?**  
A: รองรับ, Aspose.CAD รองรับรูปแบบหลากหลายรวมถึง DWG, DXF, DGN, และหลายประเภทไฟล์ BIM  

**Q: ฉันสามารถปรับแต่งตัวเลือกการบันทึกภาพได้หรือไม่?**  
A: แน่นอน! คุณสามารถปรับ `CadRasterizationOptions` (รูปแบบ, ความละเอียด, สีพื้นหลัง ฯลฯ) ให้ตรงกับความต้องการของคุณ  

**Q: จะหาเอกสารเพิ่มเติมได้จากที่ไหน?**  
A: ดูที่ [Aspose.CAD documentation](https://reference.aspose.com/cad/net/) สำหรับอ้างอิง API รายละเอียดและตัวอย่างเพิ่มเติม  

**Q: มีรุ่นทดลองฟรีหรือไม่?**  
A: มี, คุณสามารถสำรวจ Aspose.CAD ด้วย [free trial](https://releases.aspose.com/)  

**Q: จะขอรับการสนับสนุนทางเทคนิคได้อย่างไร?**  
A: สำหรับการสนับสนุนทางเทคนิค, เยี่ยมชม [Aspose.CAD forum](https://forum.aspose.com/c/cad/19)  

**อัปเดตล่าสุด:** 2026-03-21  
**ทดสอบด้วย:** Aspose.CAD 24.11 สำหรับ .NET  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}