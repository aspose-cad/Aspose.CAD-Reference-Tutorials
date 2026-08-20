---
date: 2026-03-29
description: เรียนรู้วิธีแปลง DGN เป็น PNG ด้วย Aspose.CAD สำหรับ .NET คู่มือนี้ยังครอบคลุมการสนับสนุนรูปแบบไฟล์
  CAD และชุดเต็มขององค์ประกอบ DGN ที่รองรับ.
linktitle: Supported DGN Elements
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: แปลง DGN เป็น PNG ด้วย Aspose.CAD สำหรับ .NET
url: /th/net/cad-features-and-support/supported-dgn-elements/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# แปลง DGN เป็น PNG ด้วย Aspose.CAD สำหรับ .NET

## บทนำ

คุณเป็นนักพัฒนา .NET ที่กำลังมองหา **การแปลง DGN เป็น PNG** อย่างราบรื่นหรือไม่? Aspose.CAD สำหรับ .NET ให้โซลูชันที่แข็งแกร่งในการจัดการไฟล์ DGN อย่างมีประสิทธิภาพ ในบทแนะนำนี้ เราจะเจาะลึกองค์ประกอบ DGN ที่รองรับ แนะนำขั้นตอนการทำงานกับ Aspose.CAD สำหรับ .NET พร้อมแสดงวิธีการส่งออกองค์ประกอบเหล่านั้นเป็นภาพ PNG อย่างละเอียด

## คำตอบสั้น
- **Aspose.CAD ทำอะไร?** มันอ่าน, แก้ไข, และแปลงไฟล์ CAD/BIM (รวมถึง DGN) ไปเป็นรูปแบบเรสเตอร์เช่น PNG.  
- **ฉันสามารถแปลงองค์ประกอบ DGN 2D และ 3D ได้หรือไม่?** ได้ – ทั้งเอนทิตี้ 2‑D และ 3‑D ได้รับการสนับสนุน.  
- **ต้องการเวอร์ชัน .NET ใด?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **ต้องการไลเซนส์สำหรับการทดสอบหรือไม่?** มีการทดลองใช้ฟรี; จำเป็นต้องมีไลเซนส์สำหรับการใช้งานจริง.  
- **จะดาวน์โหลดไลบรารีได้จากที่ไหน?** ดาวน์โหลดจากเว็บไซต์อย่างเป็นทางการของ Aspose (ลิงก์ด้านล่าง).

## “การแปลง DGN เป็น PNG” คืออะไร
การแปลง DGN เป็น PNG หมายถึงการเรนเดอร์ภาพวาด DGN ที่เป็นเวกเตอร์ (2‑D หรือ 3‑D) ให้เป็นรูปแบบภาพเรสเตอร์ (PNG) ซึ่งมีประโยชน์เมื่อคุณต้องการแสดงภาพวาด CAD บนเว็บ, ฝังในรายงาน, หรือสร้างรูปย่อโดยไม่ต้องใช้โปรแกรมดู CAD.

## ทำไมต้องใช้ Aspose.CAD สำหรับ .NET เพื่อสนับสนุนรูปแบบไฟล์ CAD
- **สนับสนุนรูปแบบไฟล์ CAD ครบ** – DGN, DWG, DXF, DWF, และอื่น ๆ.  
- **ไม่มีการพึ่งพาภายนอก** – ไลบรารี .NET แท้, ไม่ต้องติดตั้ง CAD แบบเนทีฟ.  
- **การเรนเดอร์ความละเอียดสูง** – รักษาน้ำหนักเส้น, สี, และเรขาคณิต 3‑D.  
- **การประมวลผลแบบชุด** – สามารถวนลูปไฟล์จำนวนมากในแอปพลิเคชันฝั่งเซิร์ฟเวอร์ได้อย่างง่ายดาย.

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเริ่ม, โปรดตรวจสอบว่าคุณมีสิ่งต่อไปนี้:

- ความรู้พื้นฐานการเขียนโปรแกรม .NET.  
- ติดตั้ง Visual Studio บนเครื่องของคุณ.  
- ไลบรารี Aspose.CAD สำหรับ .NET, คุณสามารถดาวน์โหลดได้จาก [ที่นี่](https://releases.aspose.com/cad/net/).

## นำเข้า Namespaces

เพื่อเริ่มต้นโครงการของคุณ, ให้นำเข้า namespaces ที่จำเป็นเข้าสู่แอปพลิเคชัน .NET ของคุณ ขั้นตอนนี้ทำให้คุณเข้าถึงฟังก์ชันที่ Aspose.CAD สำหรับ .NET ให้มา.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Dgn;
using Aspose.CAD.FileFormats.Dgn.DgnElements;
```

## วิธีการแปลง DGN เป็น PNG

ด้านล่างเป็นคู่มือขั้นตอนต่อขั้นตอนที่นำคุณผ่านการโหลดไฟล์ DGN, การวนลูปองค์ประกอบ, การจัดการเอนทิตี้ 2‑D และ 3‑D, และสุดท้ายการส่งออกผลลัพธ์เป็นภาพเรสเตอร์ PNG.

### ขั้นตอนที่ 1: โหลดไฟล์ DGN

เริ่มต้นโดยการโหลดไฟล์ DGN ที่มีอยู่เป็น `DgnImage` ในแอปพลิเคชัน .NET ของคุณ.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Your code here
}
```

### ขั้นตอนที่ 2: วนลูปผ่านองค์ประกอบ DGN

วนลูปผ่านองค์ประกอบ DGN ด้วยลูป `foreach`. Aspose.CAD สำหรับ .NET มีประเภทองค์ประกอบ DGN หลากหลายที่คุณสามารถทำงานได้.

```csharp
foreach (DgnDrawingElementBase element in dgnImage.Elements)
{
    // Your code here
}
```

### ขั้นตอนที่ 3: จัดการเอนทิตี้ 2‑D ที่เคยสนับสนุน

เอนทิตี้เหล่านี้ตอนนี้ยังรองรับการเรนเดอร์ 3‑D ด้วย. คำสั่ง switch ช่วยให้คุณแยกตรรกะตามประเภทขององค์ประกอบ.

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.Line:
    case DgnElementType.Ellipse:
    case DgnElementType.Curve:
    // Additional cases
        {
            // Your code here
            break;
        }
}
```

### ขั้นตอนที่ 4: จัดการเอนทิตี้ 3‑D ที่รองรับ

Aspose.CAD เพิ่มการสนับสนุนเต็มรูปแบบสำหรับหลายเอนทิตี้ DGN 3‑D. ขยายคำสั่ง switch เพื่อประมวลผลตามต้องการ.

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.SolidHeader3D:
    case DgnElementType.Cone:
    case DgnElementType.CellHeader:
        {
            // Your code here
            break;
        }
}
```

### ขั้นตอนที่ 5: ส่งออกและบันทึกเป็น PNG

หลังจากทำการปรับแต่งที่จำเป็นแล้ว, ส่งออกภาพวาด DGN เป็นภาพเรสเตอร์ PNG และบันทึกลงในไดเรกทอรีที่ระบุ.

```csharp
Console.WriteLine("\nThe DGN file exported successfully to raster image.\nFile saved at " + MyDir);
```

> **เคล็ดลับ:** ใช้ `Image.Save` พร้อม `new PngOptions()` เพื่อควบคุมความละเอียด, สีพื้นหลัง, และการตั้งค่าเฉพาะของ PNG อื่น ๆ.

## ภาพรวมการสนับสนุนรูปแบบไฟล์ CAD

Aspose.CAD สำหรับ .NET ไม่ได้จำกัดเพียง DGN เท่านั้น ยังรองรับ DWG, DXF, DWF, และรูปแบบ CAD อื่น ๆ มากมาย ทำให้คุณมี API เดียวสำหรับจัดการภาพวาดวิศวกรรมหลากหลายรูปแบบ ซึ่งเหมาะสำหรับโครงการที่ต้องการ **การสนับสนุนรูปแบบไฟล์ CAD** ข้ามมาตรฐานหลายประเภท.

## ปัญหาทั่วไปและวิธีแก้

| ปัญหา | สาเหตุ | วิธีแก้ |
|-------|--------|-----|
| **ภาพปรากฏว่าง** | ส่งออกด้วย DPI เป็นศูนย์ | ระบุ `ResolutionX` และ `ResolutionY` ใน `PngOptions`. |
| **ขาดเรขาคณิต 3‑D** | ประเภทขององค์ประกอบไม่ได้รับการจัดการใน switch | เพิ่มกรณี `DgnElementType` ที่ขาดและทำการเรนเดอร์ตามนั้น. |
| **หน่วยความจำไม่พอเมื่อไฟล์ขนาดใหญ่** | โหลดไฟล์ทั้งหมดพร้อมกัน | ประมวลผลองค์ประกอบเป็นชุดหรือใช้การสตรีมเมื่อต้องการ. |

## คำถามที่พบบ่อย

### Q1: จะหาเอกสารสำหรับ Aspose.CAD สำหรับ .NET ได้จากที่ไหน?
A1: คุณสามารถหาเอกสารได้จาก [ที่นี่](https://reference.aspose.com/cad/net/).

### Q2: คุณจะดาวน์โหลด Aspose.CAD สำหรับ .NET ได้อย่างไร?
A2: คุณสามารถดาวน์โหลดไลบรารีได้จาก [ที่นี่](https://releases.aspose.com/cad/net/).

### Q3: มีการทดลองใช้ฟรีสำหรับ Aspose.CAD สำหรับ .NET หรือไม่?
A3: มี, คุณสามารถเข้าถึงการทดลองใช้ฟรีได้จาก [ที่นี่](https://releases.aspose.com/).

### Q4: จะหาไลเซนส์ชั่วคราวสำหรับ Aspose.CAD สำหรับ .NET ได้จากที่ไหน?
A4: ไลเซนส์ชั่วคราวมีให้ที่ [ที่นี่](https://purchase.aspose.com/temporary-license/).

### Q5: ต้องการความช่วยเหลือหรือมีคำถาม?
A5: เยี่ยมชมชุมชน Aspose.CAD สำหรับ .NET ที่ [ฟอรั่มสนับสนุน](https://forum.aspose.com/c/cad/19).

---

**Last Updated:** 2026-03-29  
**Tested With:** Aspose.CAD for .NET 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}