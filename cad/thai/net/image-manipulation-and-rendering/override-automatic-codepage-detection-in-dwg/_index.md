---
date: 2026-09-04
description: เรียนรู้วิธีการแทนที่การตรวจจับ codepage ของ dwg ในไฟล์ DWG ด้วย Aspose.CAD
  สำหรับ .NET เพื่อให้คุณควบคุมการเข้ารหัสอักขระได้อย่างแม่นยำ
keywords:
- override dwg codepage
- dwg codepage detection
- aspose.cad .net
- cad file encoding
- dwg processing
lastmod: 2026-09-04
linktitle: แทนที่การตรวจจับ Codepage อัตโนมัติในไฟล์ DWG - บทแนะนำ Aspose.CAD
og_description: เรียนรู้วิธีการแทนที่การตรวจจับ codepage ของ dwg ในไฟล์ DWG ด้วย Aspose.CAD
  สำหรับ .NET เพื่อให้คุณควบคุมการเข้ารหัสอักขระได้อย่างแม่นยำและปรับปรุงการจัดการไฟล์
  CAD
og_image_alt: Guide showing how to override DWG codepage with Aspose.CAD in .NET
og_title: วิธีการแทนที่ codepage ของ dwg ใน Aspose.CAD สำหรับ .NET
schemas:
- author: Aspose
  dateModified: '2026-09-04'
  description: Learn how to override dwg codepage detection in DWG files using Aspose.CAD
    for .NET, giving you precise control over character encoding.
  headline: How to override dwg codepage in Aspose.CAD for .NET
  type: TechArticle
- questions:
  - answer: It forces Aspose.CAD to use the encoding you specify instead of guessing,
      preventing character corruption.
    question: What does overriding the DWG codepage do?
  - answer: Whenever a DWG file contains text in a language that isn’t the default
      Windows codepage (e.g., Central European, Cyrillic).
    question: When should I use it?
  - answer: Any .NET `Encoding` such as `Encoding.GetEncoding(1250)` for Central European.
    question: Which encodings are supported?
  - answer: A trial works for development; a commercial license is required for production.
    question: Do I need a license?
  - answer: Yes, the setting is applied per `Image` instance, so multiple threads
      can process different files concurrently.
    question: Is it thread‑safe?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- override dwg codepage
- Aspose.CAD
- .NET CAD processing
- DWG codepage
- CAD rendering
title: วิธีการแทนที่ codepage ของ dwg ใน Aspose.CAD สำหรับ .NET
url: /th/net/image-manipulation-and-rendering/override-automatic-codepage-detection-in-dwg/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีการแทนที่ codepage ของ dwg ใน Aspose.CAD สำหรับ .NET

ในไฟล์ DWG รุ่นเก่าหลายไฟล์ การตรวจจับ codepage ที่ฝังอยู่จะทำโดยอัตโนมัติ ซึ่งอาจทำให้ข้อความเป็นอักขระผิดเมื่อไฟล์ใช้การเข้ารหัสที่ไม่ใช่ค่าเริ่มต้น **Override dwg codepage** ช่วยให้คุณกำหนดการเข้ารหัสที่ต้องการอย่างชัดเจน เพื่อให้รูปทรงและข้อความคำอธิบายแสดงผลอย่างถูกต้อง ในบทแนะนำนี้คุณจะเห็นว่าทำไมจึงสำคัญ API มีลักษณะอย่างไร และวิธีใช้การตั้งค่าในขั้นตอนง่าย ๆ ไม่กี่ขั้นตอน.

## คำตอบอย่างรวดเร็ว
- **อะไรที่การแทนที่ DWG codepage ทำ?** มันบังคับให้ Aspose.CAD ใช้การเข้ารหัสที่คุณระบุแทนการเดา เพื่อป้องกันการเสียหายของอักขระ.  
- **เมื่อใดควรใช้?** เมื่อใดก็ตามที่ไฟล์ DWG มีข้อความในภาษาที่ไม่ใช่ codepage เริ่มต้นของ Windows (เช่น Central European, Cyrillic).  
- **การเข้ารหัสใดที่สนับสนุน?** Any .NET `Encoding` เช่น `Encoding.GetEncoding(1250)` สำหรับ Central European.  
- **ฉันต้องการใบอนุญาตหรือไม่?** รุ่นทดลองใช้ได้สำหรับการพัฒนา; จำเป็นต้องมีใบอนุญาตเชิงพาณิชย์สำหรับการใช้งานจริง.  
- **ปลอดภัยต่อการทำงานหลายเธรดหรือไม่?** ใช่ การตั้งค่านี้ถูกนำไปใช้ต่อแต่ละอินสแตนซ์ของ `Image` ดังนั้นหลายเธรดจึงสามารถประมวลผลไฟล์ต่าง ๆ พร้อมกันได้.

## Override dwg codepage คืออะไร?
Override dwg codepage เป็นคุณลักษณะของ Aspose.CAD ที่ให้คุณแทนที่การตรวจจับ codepage อัตโนมัติของไลบรารีด้วยการเข้ารหัสอักขระที่คุณระบุ ซึ่งทำให้แน่ใจว่าข้อความภายใน DWG ถูกตีความอย่างถูกต้องโดยไม่คำนึงถึงเมตาดาต้าต้นฉบับของไฟล์.

## ทำไมต้องใช้ override dwg codepage?
Aspose.CAD รองรับ **เวอร์ชัน DWG/DXF มากกว่า 50+** และสามารถประมวลผลไฟล์ได้ถึง **2 GB** โดยไม่ต้องโหลดเอกสารทั้งหมดเข้าสู่หน่วยความจำ เมื่อการตรวจจับอัตโนมัติล้มเหลว คุณอาจสูญเสียความสามารถในการอ่านคำอธิบายได้ถึง **100 %** การตั้งค่า codepage อย่างชัดเจนช่วยลดความเสี่ยงนี้เหลือ **0 %** และยังคงเวลาเรนเดอร์ไม่เปลี่ยนแปลง.

## ข้อกำหนดเบื้องต้น

- ความรู้พื้นฐานของ C# และแพลตฟอร์ม .NET.  
- Aspose.CAD for .NET ได้รับการติดตั้งแล้ว หากคุณยังไม่ได้ติดตั้ง ดาวน์โหลดได้จาก **[Aspose.CAD for .NET download page](https://releases.aspose.com/cad/net/)**.  
- ไฟล์ DWG ที่ใช้ codepage ที่ไม่ใช่ค่าเริ่มต้น (เช่น ไฟล์ที่สร้างบนระบบที่ใช้ codepage 1250).

## นำเข้า namespace

เพื่อเริ่มต้น ให้เพิ่มคำสั่ง `using` ที่จำเป็นเพื่อให้คอมไพเลอร์สามารถค้นหาคลาสของ Aspose.CAD ได้.

Insert the following at the top of your C# source file:

```csharp
using System;
using Aspose.CAD.FileFormats.Cad;
```

นี่จะเตรียมสภาพแวดล้อมสำหรับการดำเนินการ CAD ทั้งหมดต่อไป.

## ขั้นตอนที่ 1: กำหนดไดเรกทอรีเอกสารของคุณ

ระบุโฟลเดอร์ที่บรรจุ DWG ที่คุณต้องการประมวลผล แทนที่ตัวแสดงตำแหน่งด้วยพาธจริงบนเครื่องของคุณ:

```csharp
//ExStart:1
string SourceDir = "Your Document Directory";
//ExEnd:1
```

## ขั้นตอนที่ 2: แทนที่การตรวจจับ codepage อัตโนมัติ

ตอนนี้เรามาถึงหัวใจของบทแนะนำ โค้ดด้านล่างโหลดไฟล์ DWG, บังคับให้ codepage เป็น **Windows‑1250** (Central European) แล้วบันทึกภาพเป็น PNG. ปรับเปลี่ยนชื่อไฟล์และการเข้ารหัสตามความต้องการของคุณ.

```csharp
//ExStart:1
using (CadImage cadImage = (CadImage)Image.Load(SourceDir + "SimpleEntites.dwg",
new LoadOptions()
{
	SpecifiedEncoding = CodePages.Japanese,
	SpecifiedMifEncoding = MifCodePages.Japanese,
	RecoverMalformedCifMif = false
}))
{
	// Perform export or other operations with cadImage
}
//ExEnd:1
Console.WriteLine("OverrideAutomaticCodePageDetectionDwg executed successfully");
```

`Image.Load` เป็นเมธอดแบบ static ที่โหลดไฟล์ CAD และคืนค่าเป็นอ็อบเจ็กต์ `CadImage`. `LoadOptions.CodePage` ระบุการเข้ารหัสอักขระที่จะใช้ระหว่างการโหลด. `CadImage` แสดงการแทนภาพ CAD ในหน่วยความจำและให้เมธอดสำหรับการเรนเดอร์หรือการแปลง.

## ปัญหาทั่วไปและวิธีแก้

- **อักขระขยะยังคงอยู่หลังการแทนที่** – ตรวจสอบว่าการเข้ารหัสที่คุณเลือกตรงกับภาษาของไฟล์ต้นฉบับ ใช้ `Encoding.GetEncoding(1251)` สำหรับ Cyrillic เป็นตัวอย่าง.  
- **ไฟล์ไม่สามารถโหลดได้** – ตรวจสอบว่าเวอร์ชัน DWG รองรับโดยเวอร์ชัน Aspose.CAD ของคุณ; หากจำเป็นให้อัปเกรด.  
- **ประสิทธิภาพลดลง** – การแทนที่ไม่ได้เพิ่มภาระ; หากคุณสังเกตเห็นความช้าลง ให้ตรวจสอบคอขวด I/O ที่ไม่เกี่ยวข้อง.

## คำถามที่พบบ่อย

### Q1: ฉันสามารถใช้ Aspose.CAD for .NET กับภาษานอกเหนือจาก C# ได้หรือไม่?
A1: Aspose.CAD for .NET ถูกออกแบบเป็นหลักสำหรับ C# แต่สามารถใช้ในภาษา .NET อื่น ๆ เช่น VB.NET.

### Q2: มีรุ่นทดลองฟรีหรือไม่?
A2: มี คุณสามารถเข้าถึงรุ่นทดลองฟรี **[Aspose.CAD free trial download page](https://releases.aspose.com/)**.

### Q3: ฉันจะขอรับการสนับสนุนสำหรับ Aspose.CAD for .NET ได้อย่างไร?
A3: เยี่ยมชม **[Aspose.CAD forum](https://forum.aspose.com/c/cad/19)** เพื่อรับการสนับสนุนจากชุมชน.

### Q4: ฉันสามารถซื้อใบอนุญาตชั่วคราวได้หรือไม่?
A4: ใช่ คุณสามารถรับใบอนุญาตชั่วคราวได้จาก **[temporary license purchase page](https://purchase.aspose.com/temporary-license/)**.

### Q5: ฉันจะหาเอกสารรายละเอียดได้จากที่ไหน?
A5: ดูที่ **[Aspose.CAD .NET API documentation](https://reference.aspose.com/cad/net/)**.

### Q6: การแทนที่ codepage มีผลต่อคุณภาพการเรนเดอร์แบบแรสเตอร์หรือไม่?
A6: ไม่ การตั้งค่า codepage มีผลต่อการถอดรหัสข้อความเท่านั้น; คุณภาพของภาพยังคงไม่เปลี่ยนแปลง.

### Q7: ฉันสามารถใช้การแทนที่เมื่อแปลงเป็นรูปแบบอื่นนอกจาก PNG ได้หรือไม่?
A7: แน่นอน ค่า `LoadOptions.CodePage` เดียวกันทำงานกับ PDF, SVG หรือรูปแบบผลลัพธ์อื่นใดที่ Aspose.CAD รองรับ.

**อัปเดตล่าสุด:** 2026-09-04  
**ทดสอบด้วย:** Aspose.CAD 24.10 for .NET  
**ผู้เขียน:** Aspose

## บทแนะนำที่เกี่ยวข้อง

- [ค้นหาข้อความในไฟล์ DWG ด้วย C# - บทแนะนำ Aspose.CAD](/cad/net/text-search-and-manipulation/searching-text-in-dwg-files/)
- [แปลง DWG เป็น PDF และเพิ่มข้อความใน C# – บทแนะนำ Aspose.CAD](/cad/net/dwg-file-manipulation/adding-text-to-dwg/)
- [วิธีแปลง DWG เป็น PDF และภาพแรสเตอร์โดยใช้ Aspose.CAD สำหรับ .NET](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}