---
date: 2026-10-04
description: เรียนรู้วิธีค้นหาข้อความในไฟล์ DWG ด้วย C# และ Aspose.CAD สำหรับ .NET.
  ดึงข้อความ, อ่านไฟล์ DWG, และเพิ่มประสิทธิภาพแอปพลิเคชัน CAD ของคุณ.
keywords:
- search text in dwg
- extract text from dwg
- c# read dwg file
- how to search dwg files
lastmod: 2026-10-04
linktitle: การค้นหาและจัดการข้อความ
og_description: ค้นหาข้อความในไฟล์ DWG ด้วย C# และ Aspose.CAD สำหรับ .NET. ดึงข้อความ,
  อ่านไฟล์ DWG, และปรับปรุงประสิทธิภาพของแอป CAD.
og_image_alt: Guide showing C# code searching text in DWG files with Aspose.CAD
og_title: ค้นหาข้อความในไฟล์ DWG ด้วย C# โดยใช้ Aspose.CAD
schemas:
- author: Aspose
  dateModified: '2026-10-04'
  description: Learn how to search text in DWG files using C# and Aspose.CAD for .NET.
    Extract text, read DWG files, and boost your CAD applications.
  headline: Search text in DWG files with C# using Aspose.CAD
  type: TechArticle
- description: Learn how to search text in DWG files using C# and Aspose.CAD for .NET.
    Extract text, read DWG files, and boost your CAD applications.
  name: Search text in DWG files with C# using Aspose.CAD
  steps:
  - name: install the Aspose.CAD NuGet package
    text: 'Open the NuGet Package Manager console and run: This adds the required
      assemblies and updates your project file.'
  - name: open the DWG file
    text: Create a `CadImage` instance by calling `Image.Load`. The method automatically
      detects the file format and prepares an in‑memory representation.
  - name: enumerate text fragments
    text: '`image.TextFragments` returns a collection of `TextFragment` objects, each
      exposing `Text`, `Location`, `Height`, and `LayerName`. You can iterate or LINQ‑filter
      this collection.'
  - name: apply your search criteria
    text: Use `String.Contains`, `Regex.IsMatch`, or any custom predicate to locate
      the exact text you need. For case‑insensitive searches, call `ToLowerInvariant()`
      on both sides.
  - name: handle the results
    text: Typical actions include logging the fragment’s coordinates, exporting to
      CSV, or highlighting the entity in a viewer. Because the API gives you the exact
      `Location`, you can feed it into any downstream CAD visualization component.
  type: HowTo
- questions:
  - answer: Yes. Provide the password via `CadLoadOptions.Password` when calling `Image.Load`.
    question: Can I search for text in password‑protected DWG files?
  - answer: Absolutely. Loop through a directory, load each file, and reuse the same
      LINQ filter – the library is thread‑safe for parallel processing.
    question: Does the API support searching across multiple DWG files at once?
  - answer: Aspose.CAD reports a **99 % success rate** on industry‑standard test sets,
      handling MTEXT, attribute definitions, and even embedded Unicode characters.
    question: How accurate is the text extraction for complex annotations?
  - answer: After obtaining the `Location` of each `TextFragment`, you can draw a
      temporary overlay using any CAD viewer that accepts geometry primitives.
    question: Is there a way to highlight found text in a viewer?
  - answer: The product uses a per‑developer or per‑server license model; a free evaluation
      license is available for 30 days.
    question: What licensing model applies to Aspose.CAD?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- CAD processing
- Aspose.CAD
- .NET
- DWG text search
title: ค้นหาข้อความในไฟล์ DWG ด้วย C# โดยใช้ Aspose.CAD
url: /th/net/text-search-and-manipulation/
weight: 28
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ค้นหาข้อความในไฟล์ DWG ด้วย C# โดยใช้ Aspose.CAD

## บทนำ

ในบทแนะนำนี้คุณจะได้เรียนรู้วิธี **search text in DWG** ไฟล์ด้วย C# โดยใช้ไลบรารี Aspose.CAD for .NET ที่มีประสิทธิภาพ ไม่ว่าคุณจะต้องการค้นหาคำอธิบาย, ดึงค่าคุณลักษณะ, หรือสร้างดัชนีที่ค้นหาได้ ขั้นตอนต่อไปนี้จะนำคุณผ่านโซลูชันที่เชื่อถือได้และมีประสิทธิภาพสูงซึ่งทำงานได้ทั้งบน .NET Framework และ .NET Core.

## คำตอบอย่างรวดเร็ว
- **ไลบรารีใดที่จัดการการค้นหาข้อความ DWG?** Aspose.CAD for .NET.
- **ฉันสามารถดึงข้อความจาก DWG ได้หรือไม่?** Yes – the API returns plain‑text strings for any found entity.
- **เวอร์ชัน .NET ใดที่รองรับ?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.
- **ฉันต้องการใบอนุญาตสำหรับการพัฒนาหรือไม่?** A free temporary license works for evaluation; a full license is required for production.
- **การดำเนินการนี้มีประสิทธิภาพด้านหน่วยความจำหรือไม่?** Yes, Aspose.CAD processes files stream‑wise, allowing multi‑hundred‑page DWG handling without loading the entire file into RAM.

## การค้นหาข้อความใน DWG คืออะไร

CadImage คืออ็อบเจ็กต์ของ Aspose.CAD ที่แสดงถึงการวาด CAD ที่โหลดแล้ว โดยเปิดเผยเอนทิตีต่าง ๆ เช่น ชิ้นส่วนข้อความ  
TextFragment แสดงถึงส่วนย่อยของข้อความที่ดึงออกมาแต่ละส่วน รวมถึงเนื้อหาและตำแหน่งเชิงเรขาคณิต

วลี *search text in DWG* หมายถึงการค้นหาข้อมูลสตริงโดยโปรแกรม เช่น ชื่อเลเยอร์, ค่าคุณลักษณะ, หรือข้อความอธิบาย ภายในไฟล์วาด DWG Aspose.CAD เปิดเผยความสามารถนี้ผ่านอ็อบเจ็กต์ `CadImage` และคอลเลกชัน `TextFragment` ทำให้ผู้พัฒนาสามารถดึงและจัดการข้อความได้อย่างมีประสิทธิภาพ

## ทำไมต้องใช้ Aspose.CAD สำหรับการค้นหาข้อความใน DWG

Aspose.CAD รองรับ **30+ CAD and BIM formats** (รวมถึง DWG, DXF, DGN, DWF) และสามารถประมวลผลไฟล์ได้ถึง **500 MB** โดยไม่ต้องโหลดทั้งหมดเข้าสู่หน่วยความจำ ไลบรารีรับประกัน **99 % text‑extraction accuracy** บนภาพวาดที่ซับซ้อน ซึ่งเป็นการปรับปรุงเชิงปริมาณเมื่อเทียบกับพาร์เซอร์โอเพนซอร์สหลายตัวที่มักพลาด MTEXT หรือคุณลักษณะบล็อกที่ฝังอยู่

## วิธีการค้นหาข้อความในไฟล์ DWG ด้วย C#?

Image.Load เป็นเมธอดแบบ static ที่อ่านไฟล์ CAD และคืนค่าเป็นอ็อบเจ็กต์ CadImage

โหลด DWG ด้วย `Image.Load`, ดึงคอลเลกชัน `TextFragments` แล้วกรองด้วย LINQ ตามคำค้นของคุณ รูปแบบที่กระชับนี้ทำงานในเวลาเชิงเส้นสัมพันธ์กับจำนวนเอนทิตีข้อความ ไม่ต้องใช้ไลบรารีเพิ่มเติม และทำงานสอดคล้องกันในสภาพแวดล้อม .NET Framework และ .NET Core

### ขั้นตอนที่ 1: ติดตั้งแพคเกจ Aspose.CAD NuGet
เปิดคอนโซล NuGet Package Manager แล้วรัน:

```
Install-Package Aspose.CAD
```

### ขั้นตอนที่ 2: เปิดไฟล์ DWG
สร้างอ็อบเจ็กต์ `CadImage` โดยเรียก `Image.Load` เมธอดจะตรวจจับรูปแบบไฟล์โดยอัตโนมัติและเตรียมการแสดงผลในหน่วยความจำ

### ขั้นตอนที่ 3: แสดงรายการชิ้นส่วนข้อความ
`image.TextFragments` คืนค่าคอลเลกชันของอ็อบเจ็กต์ `TextFragment` แต่ละอ็อบเจ็กต์มี `Text`, `Location`, `Height` และ `LayerName` คุณสามารถวนลูปหรือกรองด้วย LINQ ได้

### ขั้นตอนที่ 4: ใช้เกณฑ์การค้นหาของคุณ
ใช้ `String.Contains`, `Regex.IsMatch` หรือพรีดิเกตใด ๆ ที่กำหนดเองเพื่อค้นหาข้อความที่ต้องการอย่างแม่นยำ สำหรับการค้นหาแบบไม่สนใจตัวพิมพ์ใหญ่‑เล็ก ให้เรียก `ToLowerInvariant()` ทั้งสองด้าน

### ขั้นตอนที่ 5: จัดการผลลัพธ์
การกระทำทั่วไปรวมถึงการบันทึกพิกัดของชิ้นส่วน, การส่งออกเป็น CSV, หรือการไฮไลท์เอนทิตีในตัวดู คุณสามารถใช้ `Location` ที่ API ให้ได้อย่างแม่นยำเพื่อส่งต่อไปยังคอมโพเนนต์การแสดงผล CAD ใด ๆ

## วิธีการดึงข้อความจาก DWG?

TextFragment คืออ็อบเจ็กต์ที่เก็บข้อความที่ดึงออกมาและเมตาดาต้าที่เกี่ยวข้อง เช่น ตำแหน่งและเลเยอร์

การดึงข้อความเหมือนกับการค้นหา; เพียงแค่แสดงรายการคอลเลกชัน `TextFragment` และอ่านคุณสมบัติ `TextFragment.Text` ของแต่ละอ็อบเจ็กต์ คุณสามารถต่อข้อความเป็นเอกสารเดียว, เขียนลงไฟล์ CSV, หรือส่งต่อไปยังดัชนีการค้นหาเพื่อการดึงข้อมูลอย่างรวดเร็วในหลายภาพวาด

## ข้อผิดพลาดทั่วไปและการแก้ไขปัญหา
- **Missing MTEXT:** บางเวอร์ชัน DWG เก่าจะเก็บข้อความหลายบรรทัดในแอตทริบิวต์ของบล็อก ตรวจสอบให้แน่ใจว่าคุณได้ตรวจสอบ `image.Blocks` สำหรับอ็อบเจ็กต์ `Attribute` ด้วย
- **Encoding issues:** ไฟล์ DWG อาจใช้โค้ดเพจที่ไม่ใช่ Unicode ตั้งค่า `image.LoadOptions.Encoding` ให้เป็น `System.Text.Encoding` ที่เหมาะสมก่อนทำการโหลด
- **Large files:** สำหรับไฟล์ที่ใหญ่กว่า 200 MB ให้เปิดใช้งาน `image.LoadOptions.Streaming = true` เพื่อรักษาการใช้หน่วยความจำให้อยู่ต่ำกว่า 100 MB

## คำถามที่พบบ่อย

**Q: ฉันสามารถค้นหาข้อความในไฟล์ DWG ที่ป้องกันด้วยรหัสผ่านได้หรือไม่?**  
A: Yes. Provide the password via `CadLoadOptions.Password` when calling `Image.Load`.

**Q: API รองรับการค้นหาในหลายไฟล์ DWG พร้อมกันหรือไม่?**  
A: Absolutely. Loop through a directory, load each file, and reuse the same LINQ filter – the library is thread‑safe for parallel processing.

**Q: ความแม่นยำของการดึงข้อความสำหรับคำอธิบายที่ซับซ้อนเป็นเท่าใด?**  
A: Aspose.CAD reports a **99 % success rate** on industry‑standard test sets, handling MTEXT, attribute definitions, and even embedded Unicode characters.

**Q: มีวิธีใดในการไฮไลท์ข้อความที่พบในตัวดูหรือไม่?**  
A: After obtaining the `Location` of each `TextFragment`, you can draw a temporary overlay using any CAD viewer that accepts geometry primitives.

**Q: โมเดลการให้ลิขสิทธิ์ของ Aspose.CAD เป็นแบบใด?**  
A: The product uses a per‑developer or per‑server license model; a free evaluation license is available for 30 days.

---

**อัปเดตล่าสุด:** 2026-10-04  
**ทดสอบด้วย:** Aspose.CAD 24.11 for .NET  
**ผู้เขียน:** Aspose  

## การสอนการค้นหาและจัดการข้อความ
### [การค้นหาข้อความในไฟล์ DWG ด้วย C# - บทแนะนำ Aspose.CAD](./searching-text-in-dwg-files/)

```csharp
using Aspose.CAD;
using Aspose.CAD.ImageOptions;

// Load the DWG file
using var image = (CadImage)Image.Load("sample.dwg");

// Retrieve all text fragments
var fragments = image.TextFragments;

// Filter fragments that contain the target string
var matches = fragments.Where(t => t.Text.Contains("TargetString"));
```

## บทแนะนำที่เกี่ยวข้อง

- [แปลง DWG เป็น PDF และเพิ่มข้อความใน C# – บทแนะนำ Aspose.CAD](/cad/net/dwg-file-manipulation/adding-text-to-dwg/)
- [วิธีแปลง DWG เป็น PDF และภาพ Raster ด้วย Aspose.CAD for .NET](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)
- [วิธีเรนเดอร์ CAD และแปลง DWG – Aspose.CAD .NET](/cad/net/conversion-and-export/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}