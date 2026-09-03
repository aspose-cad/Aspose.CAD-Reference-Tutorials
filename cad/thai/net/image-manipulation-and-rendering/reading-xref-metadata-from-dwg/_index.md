---
date: 2026-08-23
description: เปิดศักยภาพของ Aspose.CAD สำหรับ .NET ด้วยบทแนะนำขั้นตอนที่ละเอียดเกี่ยวกับวิธีอ่านข้อมูลเมตาดาต้า
  xref จากไฟล์ DWG
keywords:
- read xref metadata
- extract dwg xref
- Aspose.CAD
lastmod: 2026-08-23
linktitle: การอ่านข้อมูลเมตาดาต้า XREF จากไฟล์ DWG
og_description: เรียนรู้วิธีอ่านข้อมูลเมตาดาต้า xref จากไฟล์ DWG ด้วย Aspose.CAD สำหรับ
  .NET คู่มือนี้จะพาคุณผ่านข้อกำหนดเบื้องต้น ขั้นตอนโค้ด และข้อผิดพลาดทั่วไปภายในเวลาน้อยกว่า
  สิบนาที
og_image_alt: Screenshot of Aspose.CAD reading XREF metadata in a .NET IDE
og_title: วิธีอ่านข้อมูลเมตาดาต้า xref จากไฟล์ DWG ด้วย Aspose.CAD
schemas:
- author: Aspose
  dateModified: '2026-08-23'
  description: Unlock the potential of Aspose.CAD for .NET with our step‑by‑step tutorial
    on how to read xref metadata from DWG files.
  headline: How to read xref metadata from DWG files using Aspose.CAD
  type: TechArticle
- description: Unlock the potential of Aspose.CAD for .NET with our step‑by‑step tutorial
    on how to read xref metadata from DWG files.
  name: How to read xref metadata from DWG files using Aspose.CAD
  steps:
  - name: load the DWG file
    text: Create an `Image` instance from the DWG file you want to analyze. `Image.Load`
      loads a CAD file and returns a `CadImage` object representing the drawing. Adjust
      the `sourceFilePath` variable to the exact location of your drawing.
  - name: iterate through entities
    text: Loop through the `Image` object’s `Entities` collection. `CadBaseEntity`
      is the base class for all CAD entities in Aspose.CAD. For each entity, check
      whether it is an XREF reference and collect its metadata.
  - name: extract metadata
    text: When you encounter an XREF entity, read its insertion point (X, Y, Z) and
      the path of the referenced drawing. `CadUnderlay` represents an external reference
      (XREF) entity within a DWG drawing.
  - name: process metadata
    text: At this stage you can store the extracted information in a database, write
      it to a CSV file, or feed it into downstream BIM workflows. The sample simply
      prints the values to the console, but you are free to replace that with any
      custom logic.
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD for .NET supports **50+ input and output formats**, including
      DWG, DXF, DGN, and IFC, giving you broad coverage for most engineering workflows.
    question: Is Aspose.CAD for .NET compatible with all CAD file formats?
  - answer: Certainly! You can access the free trial download page [free trial download
      page](https://releases.aspose.com/).
    question: Can I use the free trial before making a purchase decision?
  - answer: The documentation is available [Aspose.CAD .NET documentation](https://reference.aspose.com/cad/net/).
    question: Where can I find comprehensive documentation for Aspose.CAD for .NET?
  - answer: You can get a temporary license [temporary license page](https://purchase.aspose.com/temporary-license/).
    question: How do I obtain a temporary license for Aspose.CAD for .NET?
  - answer: Join the Aspose.CAD community at [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19)
      for expert support and discussions.
    question: Need assistance or have specific queries?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- read xref metadata
- extract dwg xref
- Aspose.CAD
- DWG
- CAD metadata
title: วิธีอ่านข้อมูลเมตาดาต้า xref จากไฟล์ DWG ด้วย Aspose.CAD
url: /th/net/image-manipulation-and-rendering/reading-xref-metadata-from-dwg/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีอ่านข้อมูลเมตาดาต้า xref จากไฟล์ DWG ด้วย Aspose.CAD

## บทนำ

ในบทเรียนนี้คุณจะได้เรียนรู้ **วิธีอ่านข้อมูลเมตาดาต้า xref** จากไฟล์ DWG โดยใช้ไลบรารี Aspose.CAD สำหรับ .NET ไม่ว่าคุณจะต้องการตรวจสอบการอ้างอิงภายนอก, ย้ายภาพวาดเก่า, หรือสร้าง pipeline BIM แบบกำหนดเอง การสกัดข้อมูล XREF เป็นความต้องการทั่วไป เราจะอธิบายทุกขั้นตอน ตั้งแต่การตั้งค่าโครงการจนถึงการประมวลผลเมตาดาต้า และเราจะเน้นเคล็ดลับที่คุณสามารถนำไปใช้ได้ทันที

## คำตอบอย่างรวดเร็ว
- **วัตถุประสงค์หลักคืออะไร?** ดึงจุดแทรกและเส้นทางไฟล์ของการอ้างอิงภายนอก (XREFs) ที่ฝังอยู่ในภาพวาด DWG.  
- **ต้องใช้ไลบรารีอะไร?** Aspose.CAD for .NET (supports 50+ CAD formats).  
- **ต้องการไลเซนส์หรือไม่?** จำเป็นต้องมีไลเซนส์ชั่วคราวหรือเต็มสำหรับการใช้งานในสภาพแวดล้อมการผลิต; มีรุ่นทดลองฟรีให้ใช้.  
- **รองรับเวอร์ชัน .NET ใดบ้าง?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.  
- **โค้ดใช้เวลารันนานเท่าไหร่?** การประมวลผล DWG ขนาดประมาณ 200 หน้า พร้อม XREF จำนวนไม่กี่รายการเสร็จสิ้นภายในไม่ถึงหนึ่งวินาทีบนฮาร์ดแวร์มาตรฐาน.

## read xref metadata คืออะไร?
`read xref metadata` หมายถึงการดำเนินการเข้าถึงคุณสมบัติของเอนทิตี้การอ้างอิงภายนอกที่เก็บอยู่ในไฟล์ DWG เช่น พิกัดการแทรก, เส้นทางไฟล์ต้นทาง, และแฟล็กการมองเห็น การดำเนินการนี้ทำให้คุณสามารถค้นพบว่าไฟล์วาดประกอบด้วยไฟล์อื่นอย่างไรโดยอัตโนมัติ เพื่อการตรวจสอบ, รายงาน, หรือการประมวลผลแบบกลุ่มของทรัพยากรที่เชื่อมโยง

## ทำไมต้องใช้ Aspose.CAD สำหรับงานนี้?
Aspose.CAD รองรับ **มากกว่า 50 รูปแบบไฟล์ CAD** และสามารถอ่านไฟล์ DWG **โดยไม่ต้องใช้ AutoCAD** ไลบรารีประมวลผลภาพวาดขนาดใหญ่ **ด้วยสตรีมที่ใช้หน่วยความจำน้อย** ทำให้คุณจัดการไฟล์หลายร้อยหน้าได้โดยไม่ต้องโหลดไฟล์ทั้งหมดเข้าสู่ RAM ความสามารถที่วัดได้เหล่านี้ทำให้เป็นตัวเลือกที่เชื่อถือได้สำหรับการทำอัตโนมัติ CAD ระดับองค์กร

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะลงลึกในโค้ด, โปรดตรวจสอบว่าคุณมีสิ่งต่อไปนี้:

- Aspose.CAD for .NET ที่ติดตั้งแล้ว ดาวน์โหลดแพคเกจล่าสุดจาก [Aspose.CAD for .NET release page](https://releases.aspose.com/cad/net/).
- โฟลเดอร์ในเครื่องที่มีไฟล์ DWG ที่คุณต้องการตรวจสอบ ปรับค่าตัวแปร `MyDir` ในโค้ดตัวอย่างให้ชี้ไปยังโฟลเดอร์นี้.
- ไลเซนส์ Aspose.CAD ที่ถูกต้อง (หรือรุ่นทดลองฟรี) หากคุณวางแผนรันโค้ดในสภาพแวดล้อมการผลิต.

เมื่อสภาพแวดล้อมพร้อมแล้ว, มาเริ่มเขียนโค้ดกัน.

## นำเข้า namespace

สิ่งแรกที่คุณต้องทำคือการนำเข้า namespace ที่เปิดเผย API ของ Aspose.CAD คำสั่ง `using` จะนำ namespace ของ Aspose.CAD เข้ามาในขอบเขต, ทำให้เข้าถึงคลาส CAD เช่น `Image` และ `CadImage`.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects;
```

## วิธีอ่านข้อมูลเมตาดาต้า xref จากไฟล์ DWG?

โหลดภาพวาด, นับจำนวนเอนทิตี้, กรองออบเจ็กต์ XREF, แล้วดึงคุณสมบัติที่ต้องการ — ทั้งหมดในไม่กี่บรรทัดของโค้ด ส่วนต่อไปนี้จะแบ่งกระบวนการเป็นสี่ขั้นตอนที่คุณสามารถคัดลอกและวางลงในโครงการ .NET console หรือ service ใดก็ได้.

### ขั้นตอนที่ 1: โหลดไฟล์ DWG

สร้างอินสแตนซ์ `Image` จากไฟล์ DWG ที่คุณต้องการวิเคราะห์ `Image.Load` จะโหลดไฟล์ CAD และคืนค่าออบเจ็กต์ `CadImage` ที่แสดงภาพวาด ปรับตัวแปร `sourceFilePath` ให้ชี้ไปยังตำแหน่งที่แน่นอนของไฟล์วาดของคุณ.

```csharp
// The path to the documents directory.
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";
using (CadImage image = (CadImage)Image.Load(sourceFilePath))
{
    // Code for the next steps goes here
}
```

### ขั้นตอนที่ 2: วนลูปผ่านเอนทิตี้

วนลูปผ่านคอลเลกชัน `Entities` ของออบเจ็กต์ `Image`. `CadBaseEntity` เป็นคลาสฐานสำหรับเอนทิตี้ CAD ทั้งหมดใน Aspose.CAD สำหรับแต่ละเอนทิตี้, ตรวจสอบว่ามันเป็นการอ้างอิง XREF หรือไม่และเก็บเมตาดาต้าของมัน.

```csharp
foreach (CadBaseEntity entity in image.Entities)
{
    if (entity is CadUnderlay)
    {
        // Code for the next steps goes here
    }
}
```

### ขั้นตอนที่ 3: สกัดเมตาดาต้า

เมื่อพบเอนทิตี้ XREF, อ่านจุดแทรก (X, Y, Z) และเส้นทางของภาพวาดที่อ้างอิง `CadUnderlay` แทนเอนทิตี้การอ้างอิงภายนอก (XREF) ภายในไฟล์ DWG.

```csharp
//XREF entity with metadata
Cad3DPoint insertionPoint = ((CadUnderlay)entity).InsertionPoint;
string path = ((CadUnderlay)entity).UnderlayPath;
```

### ขั้นตอนที่ 4: ประมวลผลเมตาดาต้า

ในขั้นตอนนี้คุณสามารถเก็บข้อมูลที่สกัดไว้ในฐานข้อมูล, เขียนลงไฟล์ CSV, หรือส่งต่อไปยังกระบวนการ BIM ต่อไป ตัวอย่างนี้แค่พิมพ์ค่าลงคอนโซล, แต่คุณสามารถเปลี่ยนเป็นตรรกะที่กำหนดเองได้ตามต้องการ.

```csharp
// Your custom logic for processing metadata goes here
```

## ปัญหาที่พบบ่อยและการแก้ไขปัญหา

| อาการ | สาเหตุที่เป็นไปได้ | วิธีแก้ไข |
|---------|--------------|-----|
| ไม่มีเอนทิตี้ XREF ถูกส่งคืน | ภาพวาดใช้ประเภทการอ้างอิงที่แตกต่าง (เช่น INSERT) | ตรวจสอบประเภทเอนทิตี้กับ `CadEntityType.Xref` และจัดการ `Insert` หากจำเป็น |
| `Image.Load` ทำให้เกิดข้อยกเว้น | เส้นทางไฟล์ไม่ถูกต้องหรือเวอร์ชัน DWG ไม่รองรับ | ตรวจสอบเส้นทางและให้แน่ใจว่าคุณใช้ Aspose.CAD 24.11 หรือใหม่กว่า |
| ค่ามีเมตาดาต้าเป็นค่าว่าง | XREF ถูกกำหนดแต่ไม่สามารถแก้ไขได้ (ไฟล์ภายนอกหายไป) | ตรวจสอบว่าไฟล์ที่อ้างอิงมีอยู่บนดิสก์หรือให้ตัวแก้ไขระบบไฟล์เสมือน |

## คำถามที่พบบ่อย

**Q: Aspose.CAD for .NET รองรับรูปแบบไฟล์ CAD ทั้งหมดหรือไม่?**  
A: ใช่, Aspose.CAD for .NET รองรับ **มากกว่า 50 รูปแบบการนำเข้าและส่งออก**, รวมถึง DWG, DXF, DGN, และ IFC, ให้คุณครอบคลุมการทำงานด้านวิศวกรรมส่วนใหญ่.

**Q: ฉันสามารถใช้รุ่นทดลองฟรีก่อนตัดสินใจซื้อได้หรือไม่?**  
A: แน่นอน! คุณสามารถเข้าถึงหน้าดาวน์โหลดรุ่นทดลองฟรีได้ที่ [free trial download page](https://releases.aspose.com/).

**Q: ฉันจะหาเอกสารประกอบที่ครอบคลุมสำหรับ Aspose.CAD for .NET ได้จากที่ไหน?**  
A: เอกสารพร้อมให้บริการที่ [Aspose.CAD .NET documentation](https://reference.aspose.com/cad/net/).

**Q: ฉันจะขอรับไลเซนส์ชั่วคราวสำหรับ Aspose.CAD for .NET ได้อย่างไร?**  
A: คุณสามารถรับไลเซนส์ชั่วคราวได้จาก [temporary license page](https://purchase.aspose.com/temporary-license/).

**Q: ต้องการความช่วยเหลือหรือมีคำถามเฉพาะหรือไม่?**  
A: เข้าร่วมชุมชน Aspose.CAD ที่ [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19) เพื่อรับการสนับสนุนจากผู้เชี่ยวชาญและการสนทนา.

## สรุป

ตอนนี้คุณมีรูปแบบที่สมบูรณ์และพร้อมใช้งานในสภาพแวดล้อมการผลิตสำหรับ **การอ่านเมตาดาต้า XREF** จากไฟล์ DWG ด้วย Aspose.CAD for .NET โดยทำตามสี่ขั้นตอน—การโหลดไฟล์, การวนลูปเอนทิตี้, การสกัดจุดแทรกและเส้นทาง underlay, และการประมวลผลผลลัพธ์—คุณสามารถผสานความสามารถนี้เข้าไปในแอปพลิเคชันที่เน้น CAD ใดก็ได้ ไม่ว่าจะเป็นเครื่องมือย้ายข้อมูล, สคริปต์ตรวจสอบคุณภาพ, หรือ pipeline BIM แบบกำหนดเอง.

---

**อัปเดตล่าสุด:** 2026-08-23  
**ทดสอบด้วย:** Aspose.CAD 24.11 for .NET  
**ผู้เขียน:** Aspose

## บทเรียนที่เกี่ยวข้อง

- [วิธีเปลี่ยนเส้นทาง xref และแก้ไขไฮเปอร์ลิงก์ในไฟล์ CAD - บทเรียน Aspose.CAD](/cad/net/advanced-cad-techniques/editing-hyperlinks-in-cad-files/)
- [การดึงคุณลักษณะของบล็อกจากไฟล์ DWG - บทเรียน Aspose.CAD](/cad/net/image-manipulation-and-rendering/getting-block-attributes-from-dwg/)
- [การแปลงไฟล์ DWG ขนาดใหญ่เป็น PDF - บทเรียน Aspose.CAD](/cad/net/image-manipulation-and-rendering/converting-large-dwg-files-to-pdf/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}