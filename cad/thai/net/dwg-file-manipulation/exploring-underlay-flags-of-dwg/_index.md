---
date: 2026-04-09
description: เรียนรู้วิธีแปลง DWG เป็นภาพและวิธีอ่านแฟล็ก underlay ด้วย Aspose.CAD
  สำหรับ .NET ในคู่มือแบบขั้นตอนต่อขั้นตอนนี้
keywords:
- convert dwg to image
- how to read underlay
- Aspose.CAD DWG underlay flags
linktitle: สำรวจธง Underlay ของไฟล์ DWG
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: แปลง DWG เป็นภาพ – สำรวจแฟล็ก Underlay ของไฟล์ DWG - บทแนะนำ Aspose.CAD
url: /th/net/dwg-file-manipulation/exploring-underlay-flags-of-dwg/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# สำรวจแฟล็ก Underlay ของไฟล์ DWG - บทแนะนำ Aspose.CAD

## บทนำ

หากคุณกำลังสำรวจโลกซับซ้อนของไฟล์ CAD โดยเฉพาะไฟล์ DWG และต้องการ **แปลง DWG เป็นภาพ** พร้อมกับค้นหา **วิธีอ่านแฟล็ก underlay** คุณมาถูกที่แล้ว บทแนะนำนี้จะพาคุณผ่านทุกขั้นตอนโดยใช้ไลบรารี Aspose.CAD for .NET ที่ทรงพลัง เพื่อให้คุณสามารถดึงข้อมูล underlay และเรนเดอร์ภาพวาดเป็นรูปภาพได้อย่างมั่นใจ

## คำตอบอย่างรวดเร็ว
- **อะไรหมายถึง “convert DWG to image”?**  
  หมายความว่าการเรนเดอร์ภาพวาด DWG ไปเป็นรูปแบบเรสเตอร์ (PNG, JPEG ฯลฯ) โดยใช้ Aspose.CAD.
- **วิธีใดที่เปิดเผยแฟล็ก underlay?**  
  เข้าถึงคุณสมบัติ `Flags` ของอ็อบเจ็กต์ `CadUnderlay` หลังจากโหลด DWG.
- **ฉันต้องการไลเซนส์สำหรับ Aspose.CAD หรือไม่?**  
  มีไลเซนส์ชั่วคราวสำหรับการประเมิน; จำเป็นต้องมีไลเซนส์เต็มสำหรับการใช้งานจริง.
- **เวอร์ชัน .NET ใดที่รองรับ?**  
  .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6 และรุ่นต่อไป.
- **ฉันสามารถดึงเรขาคณิตของ underlay ได้หรือไม่?**  
  ได้ – สามารถเข้าถึงเส้นทาง underlay, จุดแทรก, การสเกล, การหมุน, และสถานะของแฟล็กทั้งหมด

## “convert DWG to image” คืออะไรและทำไมจึงสำคัญ?

การแปลงไฟล์ DWG เป็นภาพทำให้คุณสามารถแสดงภาพวาด CAD ในเบราว์เซอร์ ฝังลงในรายงาน หรือแชร์ให้กับผู้มีส่วนได้ส่วนเสียที่ไม่มีโปรแกรมดู CAD ได้ ในขณะเรนเดอร์ คุณมักต้องตรวจสอบอ็อบเจ็กต์ **underlay** (เช่น การอ้างอิง DGN) เพื่อให้แน่ใจว่าปรากฏอย่างถูกต้อง การเข้าใจแฟล็กของ underlay จะช่วยให้คุณแก้ไขปัญหาการคลิป, การเรนเดอร์แบบสีเดียว, และปัญหาการมองเห็นก่อนสร้างภาพสุดท้าย

## ข้อกำหนดเบื้องต้น

- ความเข้าใจพื้นฐานเกี่ยวกับ C# และการเขียนโปรแกรม .NET.  
- **Aspose.CAD for .NET** library installed. หากคุณยังไม่มี สามารถดาวน์โหลดได้จาก **[here](https://releases.aspose.com/cad/net/)**.  
- ไฟล์ DWG สำหรับการทดสอบ – ไฟล์ตัวอย่าง **“BlockRefDgn.dwg”** จะใช้ตลอดคู่มือนี้.

## นำเข้า Namespaces

To get started, import the necessary namespaces:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## ขั้นตอนที่ 1: โหลดไฟล์ DWG และแปลงเป็น `CadImage`

แรกสุด โหลดไฟล์ DWG แล้วแคสต์เป็น `CadImage` วัตถุนี้ให้คุณเข้าถึงเอนทิตีทั้งหมดของภาพวาด รวมถึง underlay

```csharp
string fileName = MyDir + "BlockRefDgn.dwg";

// Load DWG file and convert to CadImage
using (CadImage image = (CadImage)Image.Load(fileName))
{
    // Your code for subsequent steps will go here
}
```

## ขั้นตอนที่ 2: วนลูปผ่านเอนทิตี

ต่อไป วนลูปผ่านเอนทิตีทั้งหมดในภาพวาด ที่นี่คุณจะค้นหาอ็อบเจ็กต์ underlay

```csharp
foreach (CadBaseEntity entity in image.Entities)
{
    // Your code for subsequent steps will go here
}
```

## ขั้นตอนที่ 3: ตรวจสอบประเภท `CadDgnUnderlay`

ระบุเอนทิตี underlay โดยตรวจสอบประเภทเวลารันของมัน คลาส `CadDgnUnderlay` แทน underlay ประเภท DGN ที่ฝังอยู่ใน DWG

```csharp
if (entity is CadDgnUnderlay)
{
    // Your code for subsequent steps will go here
}
```

## ขั้นตอนที่ 4: เข้าถึงแฟล็ก Underlay

เมื่อคุณมี `CadDgnUnderlay` แล้ว ให้แคสต์เป็น `CadUnderlay` เพื่ออ่านคุณสมบัติและสถานะของแฟล็ก แฟล็กบ่งบอกว่า underlay ปรากฏ, ถูกคลิป, หรือเรนเดอร์เป็นสีเดียวหรือไม่

```csharp
CadUnderlay underlay = entity as CadUnderlay;

Console.WriteLine(underlay.UnderlayPath);
Console.WriteLine(underlay.UnderlayName);
Console.WriteLine(underlay.InsertionPoint.X);
Console.WriteLine(underlay.InsertionPoint.Y);
Console.WriteLine(underlay.RotationAngle);
Console.WriteLine(underlay.ScaleX);
Console.WriteLine(underlay.ScaleY);
Console.WriteLine(underlay.ScaleZ);
Console.WriteLine((underlay.Flags & UnderlayFlags.UnderlayIsOn) == UnderlayFlags.UnderlayIsOn);
Console.WriteLine((underlay.Flags & UnderlayFlags.ClippingIsOn) == UnderlayFlags.ClippingIsOn);
Console.WriteLine((underlay.Flags & UnderlayFlags.Monochrome) != UnderlayFlags.Monochrome);
```

### สิ่งที่ผลลัพธ์บอกคุณ

- **UnderlayPath / UnderlayName** – ที่ตั้งของไฟล์ DGN ภายนอก.  
- **InsertionPoint (X, Y)** – พิกัดที่ underlay ถูกวางในพื้นที่ DWG.  
- **RotationAngle** – การหมุนที่ใช้กับ underlay.  
- **ScaleX / ScaleY / ScaleZ** – ตัวคูณสเกลสำหรับแต่ละแกน.  
- **Flags** – ค่าบูลีนที่บ่งบอกการมองเห็น (`UnderlayIsOn`), การคลิป (`ClippingIsOn`), และการเรนเดอร์สีเดียว (`Monochrome`).

## ปัญหาทั่วไป & วิธีแก้ไข

| ปัญหา | สาเหตุ | วิธีแก้ |
|-------|--------|-----|
| ไม่มีผลลัพธ์สำหรับการตรวจสอบแฟล็ก | แฟล็กของ underlay จะเป็นค่าเริ่มต้น 0 เมื่อ underlay ถูกปิด | ตรวจสอบให้แน่ใจว่า DWG มี underlay ที่ทำงานอยู่หรือสลับการมองเห็นในไฟล์ CAD ต้นฉบับ |
| `Invalid cast` exception | เอนทิตีไม่ใช่ `CadDgnUnderlay` | ตรวจสอบเงื่อนไข `if (entity is CadDgnUnderlay)` ก่อนทำการแคสต์ |
| การเรนเดอร์ภาพล้มเหลวหลังจากดึงแฟล็ก | underlay อาจถูกคลิปหรือปิดทำให้เกิดพื้นที่ว่าง | ปรับค่าแฟล็ก (`UnderlayIsOn = true`, `ClippingIsOn = false`) ก่อนเรนเดอร์ภาพสุดท้าย |

## คำถามที่พบบ่อย

### Q1: ฉันสามารถใช้ Aspose.CAD for .NET กับรูปแบบไฟล์ CAD อื่นได้หรือไม่?

A1: Aspose.CAD รองรับรูปแบบ CAD หลากหลาย รวมถึง DWG, DXF, DGN และอื่น ๆ ตรวจสอบเอกสารสำหรับรายการเต็ม

### Q2: มีไลเซนส์ชั่วคราวสำหรับ Aspose.CAD for .NET หรือไม่?

A2: มี คุณสามารถรับไลเซนส์ชั่วคราวได้จาก **[here](https://purchase.aspose.com/temporary-license/)**.

### Q3: ฉันจะหาแหล่งสนับสนุนสำหรับ Aspose.CAD for .NET ได้ที่ไหน?

A3: เยี่ยมชมฟอรั่มสนับสนุน **[here](https://forum.aspose.com/c/cad/19)** เพื่อขอความช่วยเหลือ.

### Q4: ฉันจะซื้อ Aspose.CAD for .NET ได้อย่างไร?

A4: ซื้อไลบรารีได้จาก **[here](https://purchase.aspose.com/buy)**.

### Q5: มีการทดลองใช้ฟรีหรือไม่?

A5: มี คุณสามารถเข้าถึงการทดลองใช้ฟรีได้จาก **[here](https://releases.aspose.com/)**.

## สรุป

ขอแสดงความยินดี! คุณได้เรียนรู้ **วิธีแปลง DWG เป็นภาพ** พร้อมกับเชี่ยวชาญ **วิธีอ่านแฟล็ก underlay** ด้วย Aspose.CAD for .NET ด้วยความรู้นี้คุณสามารถ:

- เรนเดอร์ภาพวาด DWG เป็นรูปภาพเรสเตอร์สำหรับเว็บหรือการรายงาน  
- ตรวจสอบและจัดการคุณสมบัติของ underlay เพื่อให้แสดงผลถูกต้อง  
- แก้ไขปัญหาการมองเห็น, การคลิป, และการเรนเดอร์สีเดียวก่อนสร้างภาพสุดท้าย

คุณสามารถสำรวจคุณสมบัติอื่น ๆ ของ Aspose.CAD เช่น การจัดการเลเยอร์, การสกัดข้อความ, และการแปลงเป็นชุด เพื่อขยายการทำงานอัตโนมัติของ CAD ของคุณต่อไป.

---

**อัปเดตล่าสุด:** 2026-04-09  
**ทดสอบด้วย:** Aspose.CAD for .NET 24.11  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}