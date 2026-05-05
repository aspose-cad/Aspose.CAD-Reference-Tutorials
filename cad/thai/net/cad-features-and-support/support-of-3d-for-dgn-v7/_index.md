---
date: 2026-03-29
description: เรียนรู้วิธีกำหนดค่าตัวเลือกการเรสเตอร์ไลซ์ของ CAD และส่งออกไฟล์ DGN
  เป็น PDF พร้อมการสนับสนุน 3 มิติโดยใช้ Aspose.CAD สำหรับ .NET
linktitle: Support of 3D for DGN V7
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: กำหนดค่าตัวเลือกการเรสเตอร์ไลซ์ CAD สำหรับ DGN V7 3D
url: /th/net/cad-features-and-support/support-of-3d-for-dgn-v7/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# กำหนดค่าตัวเลือกการเรสเตอร์ไอซ์ CAD สำหรับ DGN V7 3D

## บทนำ

ในบทแนะนำเชิงลึกนี้คุณจะได้เรียนรู้ **วิธีกำหนดค่าตัวเลือกการเรสเตอร์ไอซ์ CAD** เพื่อส่งออกไฟล์ DGN V7 แบบ 3‑D ไปเป็น PDF ด้วย Aspose.CAD for .NET ไม่ว่าคุณจะกำลังสร้างตัวดู CAD, เครื่องมือรายงาน, หรือสายการแปลงอัตโนมัติ การเข้าใจการตั้งค่าเหล่านี้จะทำให้คุณควบคุมขนาดหน้า, การสเกลเลย์เอาต์, สีพื้นหลัง, และมุมมองที่ต้องการเรนเดอร์ได้อย่างแม่นยำ มาดูขั้นตอนกันทีละขั้นตอน

## คำตอบสั้น
- **“กำหนดค่าตัวเลือกการเรสเตอร์ไอซ์ CAD” หมายถึงอะไร?**  
  หมายถึงการตั้งค่าคุณสมบัติต่าง ๆ เช่น ขนาดหน้า, การสเกล, สีพื้นหลัง, และการเลือกเลย์เอาต์ ก่อนแปลงไฟล์ CAD เป็นรูปแบบเรสเตอร์ (เช่น PDF)
- **วิธีส่งออก DGN ไปเป็น PDF พร้อมรองรับ 3‑D?**  
  โหลด DGN ด้วย `DgnImage`, กำหนด `PdfOptions` + `CadRasterizationOptions`, แล้วเรียก `Save`
- **ต้องใช้ไลเซนส์สำหรับการใช้งานในผลิตภัณฑ์หรือไม่?**  
  ใช่ – ต้องมีไลเซนส์เชิงพาณิชย์สำหรับการปรับใช้; มีรุ่นทดลองฟรีให้ใช้
- **รองรับเวอร์ชัน .NET ใดบ้าง?**  
  .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7
- **สามารถเลือกมุมมองเฉพาะเพื่อส่งออกได้หรือไม่?**  
  ได้ – เพียงตั้งค่าอาร์เรย์ `Layouts` ในตัวเลือกการเรสเตอร์ไอซ์

## “กำหนดค่าตัวเลือกการเรสเตอร์ไอซ์ CAD” คืออะไร?

การกำหนดค่าตัวเลือกการเรสเตอร์ไอซ์ CAD หมายถึงการปรับแต่งวิธีที่ภาพวาด CAD ถูกแปลงจากเวกเตอร์เป็นบิตแมพหรือ PDF โดยการปรับตั้งค่าเหล่านี้คุณจะควบคุมผลลัพธ์ภาพ, ประสิทธิภาพ, และขนาดไฟล์ของเอกสารที่ได้

## ทำไมต้องใช้ Aspose.CAD สำหรับการส่งออก DGN V7 3‑D?

- **การบูรณาการเต็มรูปแบบกับ .NET** – ไม่ต้องใช้ COM หรือ DLL เนทีฟ  
- **รองรับเรขาคณิต 3‑D** – คงข้อมูลความลึกเมื่อเรนเดอร์เป็น PDF  
- **การควบคุมระดับละเอียด** – เลือกเลย์เอาต์, การสเกล, และสีพื้นหลังได้ตามต้องการ  
- **ข้ามแพลตฟอร์ม** – ทำงานบน Windows, Linux, และ macOS ด้วย .NET Core

## ข้อกำหนดเบื้องต้น

ก่อนเริ่มทำตามขั้นตอนให้ตรวจสอบว่าคุณมี:

- **Aspose.CAD for .NET** – ดาวน์โหลดได้จาก [here](https://releases.aspose.com/cad/net/)  
- **Visual Studio** หรือ IDE .NET ที่เข้ากันได้  
- **ไฟล์ DGN ตัวอย่าง** – ในคู่มือนี้เราจะใช้ `Nikon_D90_Camera.dgn` (รวมอยู่ในแพ็คตัวอย่างของ Aspose)

เมื่อทุกอย่างพร้อมแล้ว ไปที่โค้ดกันเลย

## นำเข้า Namespaces

ในโครงการ .NET ของคุณ ให้นำเข้า namespaces ที่จำเป็น:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Dgn;
using Aspose.CAD.ImageOptions;
```

## ขั้นตอนที่ 1: ตั้งค่าไดเรกทอรีเอกสารของคุณ

สร้างตัวแปรที่ชี้ไปยังโฟลเดอร์ที่เก็บไฟล์ DGN ต้นฉบับและไฟล์ผลลัพธ์

```csharp
string MyDir = "Your Document Directory";
```

## ขั้นตอนที่ 2: โหลดไฟล์ DGN

โหลดไฟล์ DGN เป็น `DgnImage` ซึ่งออบเจกต์นี้ให้คุณเข้าถึงข้อมูล CAD และไพป์ไลน์การเรสเตอร์ไอซ์

```csharp
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";
string outFile = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Your code for further processing goes here
}
```

## ขั้นตอนที่ 3: กำหนดค่าตัวเลือกการส่งออก PDF (กำหนดค่าตัวเลือกการเรสเตอร์ไอซ์ CAD)

ที่นี่เราจะ **กำหนดค่าตัวเลือกการเรสเตอร์ไอซ์ CAD** เพื่อควบคุมวิธีที่โมเดล 3‑D ถูกเรนเดอร์เป็น PDF คุณสามารถปรับขนาดหน้า, เปิดการสเกลเลย์เอาต์อัตโนมัติ, ตั้งค่าสีพื้นหลัง, และเลือกเลย์เอาต์ (มุมมอง) ที่ต้องการส่งออกได้

```csharp
var options = new PdfOptions
{
    VectorRasterizationOptions = new CadRasterizationOptions
    {
        PageWidth = 1500,
        PageHeight = 1500,
        AutomaticLayoutsScaling = true,
        BackgroundColor = Color.Black,
        Layouts = new string[] { "1", "2", "3", "9" } // Only export specified views
    }
};
```

## ขั้นตอนที่ 4: บันทึกภาพเรสเตอร์

สุดท้ายให้ส่งออก DGN ไปเป็นไฟล์ PDF โดยใช้ตัวเลือกที่คุณกำหนดไว้

```csharp
dgnImage.Save(outFile, options);
```

## ปัญหาทั่วไปและวิธีแก้

| Issue | Solution |
|-------|----------|
| **Blank PDF output** | Verify that the `Layouts` array contains the correct view identifiers present in the DGN file. |
| **Incorrect colors** | Ensure `BackgroundColor` is set to the desired value; use `Color.White` for light background. |
| **Performance bottleneck on large files** | Enable `AutomaticLayoutsScaling` and consider reducing `PageWidth/PageHeight` for a smaller raster resolution. |
| **License exception** | Install a valid Aspose.CAD license before loading the image to avoid trial watermarks. |

## คำถามที่พบบ่อย

**Q: สามารถใช้ Aspose.CAD for .NET กับรูปแบบไฟล์ CAD อื่นได้หรือไม่?**  
A: ใช่, Aspose.CAD รองรับ DWG, DXF, DWF, DGN และรูปแบบอื่น ๆ อีกหลายประเภท

**Q: จะจัดการกับข้อยกเว้นเมื่อใช้ Aspose.CAD อย่างไร?**  
A: ห่อโค้ดของคุณด้วยบล็อก `try‑catch` และตรวจสอบ `Aspose.CAD.CADException` เพื่อดูรายละเอียดข้อผิดพลาด

**Q: Aspose.CAD เหมาะกับโครงการเชิงพาณิชย์หรือไม่?**  
A: แน่นอน คุณสามารถซื้อไลเซนส์ได้จาก [here](https://purchase.aspose.com/buy)

**Q: สามารถทดลองใช้ Aspose.CAD for .NET ก่อนซื้อได้หรือไม่?**  
A: ได้, มีรุ่นทดลองฟรีที่ [here](https://releases.aspose.com/)

**Q: จะหาแหล่งสนับสนุนจากชุมชนสำหรับ Aspose.CAD ได้จากที่ไหน?**  
A: เข้าร่วมฟอรั่มสนทนาได้ที่ [here](https://forum.aspose.com/c/cad/19)

---

**Last Updated:** 2026-03-29  
**Tested With:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}