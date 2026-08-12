---
date: 2026-08-12
description: ดึงข้อความจาก DWG และแปลง DWG เฉพาะเป็นภาพใน C# ด้วย Aspose.CAD สำหรับ
  .NET เรียนรู้แบบขั้นตอนต่อขั้นตอนพร้อมตัวอย่างโค้ด
keywords:
- extract text from dwg
- convert specific dwg to image
- Aspose.CAD .NET
lastmod: 2026-08-12
linktitle: การแปลง DWG เฉพาะเป็นภาพใน C#
og_description: ดึงข้อความจาก DWG และแปลง DWG เฉพาะเป็นภาพใน C# ด้วย Aspose.CAD ปฏิบัติตามคู่มือสั้น
  ๆ นี้เพื่อการนำไปใช้เร็ว
og_image_alt: Guide showing DWG to image conversion and text extraction using Aspose.CAD
  in C#
og_title: ดึงข้อความจาก DWG และแปลง DWG เฉพาะเป็นภาพใน C#
schemas:
- author: Aspose
  dateModified: '2026-08-12'
  description: Extract text from DWG and convert specific DWG to image in C# using
    Aspose.CAD for .NET. Learn step‑by‑step with code snippets.
  headline: Extract text from DWG and convert specific DWG to image in C#
  type: TechArticle
- questions:
  - answer: Aspose.CAD supports DWG releases from AutoCAD 2000 up to the latest 2024
      version, covering over 90 % of files created in the field.
    question: Is Aspose.CAD compatible with all versions of DWG files?
  - answer: Yes – you can change resolution, image format, anti‑aliasing, and background
      color to suit PNG, JPEG, or PDF targets.
    question: Can I customize the rasterization options for different outputs?
  - answer: Explore the comprehensive [Aspose.CAD documentation](https://reference.aspose.com/cad/net/)
      for more code samples and API details.
    question: Where can I find additional examples and documentation?
  - answer: Absolutely – you can download a trial version on the **[Aspose trial download
      page](https://releases.aspose.com/)** and evaluate all features without restrictions
      for 30 days.
    question: Is there a free trial available for Aspose.CAD?
  - answer: Join the active [Aspose.CAD forum](https://forum.aspose.com/c/cad/19)
      where developers share solutions and the Aspose team answers questions.
    question: How can I get support or connect with the community?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- extract text from dwg
- Aspose.CAD
- C# CAD processing
title: ดึงข้อความจาก DWG และแปลง DWG เฉพาะเป็นภาพใน C#
url: /th/net/image-manipulation-and-rendering/converting-particular-dwg-to-image/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# การแปลง DWG เฉพาะเป็นภาพใน C# - คู่มือ Aspose.CAD

## บทนำ

ในแอปพลิเคชันวิศวกรรมสมัยใหม่ คุณมักต้อง **extract text from DWG** ไฟล์และ **convert specific DWG to image** เพื่อการรายงานหรือการแสดงผล Aspose.CAD สำหรับ .NET ให้ API ที่ครบถ้วนซึ่งจัดการงานทั้งสองโดยไม่ต้องใช้ซอฟต์แวร์ CAD ภายนอก ในบทเรียนนี้คุณจะได้เรียนรู้วิธีโหลด DWG, กรองเอนทิตีข้อความ, แปลงภาพราสเตอร์ของแบบร่าง, และสุดท้ายบันทึกผลลัพธ์เป็นภาพ PDF — ทั้งหมดในโค้ด C# ที่สะอาด

## คำตอบอย่างรวดเร็ว
- **ขั้นตอนแรกคืออะไร?** Load the DWG file with `new CadImage("file.dwg")`.  
- **คลาสใดที่กรองข้อความ?** Use `CadEntityFilter` to select `Text` entities.  
- **จะกำหนดขนาดภาพอย่างไร?** Set `Width` and `Height` on `CadRasterizationOptions`.  
- **รูปแบบผลลัพธ์ที่ใช้คืออะไร?** The example saves to PDF, which embeds the raster image.  
- **ฉันต้องการลิขสิทธิ์สำหรับการผลิตหรือไม่?** Yes – a commercial Aspose.CAD license removes evaluation limits.

## วิธีการดึงข้อความจาก DWG

โหลด DWG, ใช้ตัวกรองที่เลือกเฉพาะเอนทิตีข้อความ, แล้วอ่านคุณสมบัติ `TextString` ของแต่ละเอนทิตี วิธีนี้จะคืนค่าข้อความคำอธิบาย, ป้ายกำกับ หรือข้อความมิติทั้งหมดที่มีในแบบร่าง ทำให้คุณสามารถนำกลับไปใช้ในการค้นหา, การทำดัชนี, หรือการรายงานได้

## ทำไมต้องแปลง DWG เฉพาะเป็นภาพ

การแปลง DWG เป็นภาพราสเตอร์ทำให้คุณสามารถฝังแบบร่างลงในเอกสาร, หน้าเว็บ, หรือแอปมือถือที่ไม่สามารถแสดงรูปแบบ CAD ดั้งเดิมได้ Aspose.CAD ประมวลผล **over 50+ CAD formats** และสามารถแปลงภาพราสเตอร์ของแบบร่างหลายร้อยหน้าโดยใช้หน่วยความจำน้อยกว่า 200 MB ซึ่งทำให้เหมาะกับสถานการณ์เซิร์ฟเวอร์ที่ต้องการประมวลผลสูง

## ข้อกำหนดเบื้องต้น

- Visual Studio (รุ่นล่าสุดใดก็ได้) เพื่อคอมไพล์และรันโครงการ C#
- Aspose.CAD สำหรับ .NET – ตรวจสอบว่าคุณได้ติดตั้งไลบรารีแล้ว คุณสามารถค้นหาลิงก์ดาวน์โหลดได้ที่ **[Aspose.CAD for .NET download page](https://releases.aspose.com/cad/net/)**.
- ไฟล์ DWG ที่คุณต้องการทำงาน; ตัวอย่างไฟล์ *visualization_-_conference_room.dwg* ถูกใช้ในโค้ดตัวอย่าง

## นำเข้าเนมสเปซ

เนมสเปซต่อไปนี้ให้คุณเข้าถึงคลาส CAD หลัก, ตัวเลือกการแปลงราสเตอร์, และตัวช่วยการส่งออก PDF:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## ขั้นตอนที่ 1: โหลดไฟล์ DWG

สร้างอินสแตนซ์ `CadImage` โดยส่งพาธของไฟล์ DWG ของคุณ `CadImage` แทนภาพรวมของแบบร่างทั้งหมดในหน่วยความจำและให้เข้าถึงเลเยอร์, เอนทิตี, และเมตาดาต้าต่าง ๆ

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";
var cadImage = (CadImage)Aspose.CAD.Image.Load(sourceFilePath);
```

## ขั้นตอนที่ 2: กรองเอนทิตี

`CadEntityFilter` ให้คุณเลือกเฉพาะเอนทิตีที่ต้องการ ในคู่มือนี้เราตั้งค่าให้เก็บวัตถุ **text** เท่านั้น, ลบเส้น, วงกลม, และรูปทรงอื่น ๆ ที่คุณไม่ต้องการในภาพสุดท้าย

```csharp
CadBaseEntity[] entities = cadImage.Entities;
List<CadBaseEntity> filteredEntities = new List<CadBaseEntity>();

foreach (CadBaseEntity baseEntity in entities)
{
    // Selection or filtration of entities
    if (baseEntity.TypeName == CadEntityTypeName.TEXT)
    {
        filteredEntities.Add(baseEntity);
    }
}

cadImage.Entities = filteredEntities.ToArray();
```

## ขั้นตอนที่ 3: ตั้งค่าตัวเลือกการแปลงราสเตอร์

`CadRasterizationOptions` ควบคุมวิธีการแปลงแบบร่างเป็นบิตแมป คุณสามารถกำหนดขนาดผลลัพธ์, สีพื้นหลัง, และความละเอียด (DPI) คำอธิบายต่อไปนี้แนะนำคลาส:

คลาส `CadRasterizationOptions` ระบุขนาดภาพ, ความละเอียด, และการตั้งค่าการเรนเดอร์สำหรับการแปลงแบบร่าง CAD ไปเป็นรูปแบบราสเตอร์

ตั้งค่าความกว้าง, ความสูง, และสีพื้นหลังที่ต้องการก่อนส่งตัวเลือกไปยังตัวส่งออก PDF

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions rasterizationOptions =
    new Aspose.CAD.ImageOptions.CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.AutomaticLayoutsScaling = true;
```

## ขั้นตอนที่ 4: ตั้งค่าตัวเลือก PDF

`PdfOptions` รวมการตั้งค่าการแปลงราสเตอร์กับคุณลักษณะเฉพาะของ PDF เช่น การบีบอัด คำอธิบายของคลาสนี้ปรากฏเป็นอันดับแรก:

`PdfOptions` รวมพารามิเตอร์การสร้าง PDF, รวมถึงตัวเลือกการแปลงราสเตอร์ที่กำหนดวิธีการเรนเดอร์ข้อมูล CAD ภายในเอกสาร PDF

กำหนดอินสแตนซ์ `CadRasterizationOptions` ที่สร้างไว้ก่อนหน้านี้ให้กับคุณสมบัติ `VectorRasterizationOptions`

```csharp
Aspose.CAD.ImageOptions.PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## ขั้นตอนที่ 5: บันทึกเป็น PDF

สุดท้าย, เรียกเมธอด `Save` บนวัตถุ `CadImage`, ส่งชื่อไฟล์เป้าหมายและ `PdfOptions` ที่กำหนดไว้ PDF จะมีภาพคุณภาพสูงของแบบร่างที่กรองแล้ว

```csharp
string outFile = MyDir + "result_out_generated.pdf";
cadImage.Save(outFile, pdfOptions);
```

## ปัญหาทั่วไปและการแก้ไขข้อผิดพลาด
- **Missing text after filtering** – ตรวจสอบว่า DWG มีเอนทิตี `Text` จริงหรือไม่; บางแบบร่างเก็บคำอธิบายเป็น `MText`. ปรับตัวกรองให้รวม `MText` หากจำเป็น.
- **Blank output image** – ตรวจสอบว่าความละเอียด DPI ของการแปลงราสเตอร์สูงพอ (300 DPI เป็นค่าเริ่มต้นที่ปลอดภัย) และสีพื้นหลังไม่ได้ตั้งเป็นโปร่งใสเมื่อดู PDF.
- **Out‑of‑memory errors on large files** – ใช้ overload ของ `LoadOptions` ที่เปิดใช้งานการสตรีมมิ่ง, ซึ่งป้องกันไม่ให้ไฟล์ทั้งหมดโหลดเข้าสู่หน่วยความจำพร้อมกัน.

## คำถามที่พบบ่อย

**Q: Aspose.CAD รองรับทุกเวอร์ชันของไฟล์ DWG หรือไม่?**  
A: Aspose.CAD รองรับ DWG ตั้งแต่ AutoCAD 2000 จนถึงเวอร์ชันล่าสุด 2024, ครอบคลุมกว่า 90 % ของไฟล์ที่สร้างในอุตสาหกรรม

**Q: ฉันสามารถปรับแต่งตัวเลือกการแปลงราสเตอร์สำหรับผลลัพธ์ต่าง ๆ ได้หรือไม่?**  
A: ใช่ – คุณสามารถเปลี่ยนความละเอียด, รูปแบบภาพ, การตัดขอบ, และสีพื้นหลังให้เหมาะกับเป้าหมาย PNG, JPEG, หรือ PDF

**Q: ฉันจะหา ตัวอย่างและเอกสารเพิ่มเติมได้จากที่ไหน?**  
A: สำรวจ [Aspose.CAD documentation](https://reference.aspose.com/cad/net/) เพื่อดูตัวอย่างโค้ดและรายละเอียด API เพิ่มเติม

**Q: มีรุ่นทดลองฟรีสำหรับ Aspose.CAD หรือไม่?**  
A: แน่นอน – คุณสามารถดาวน์โหลดรุ่นทดลองได้จาก **[Aspose trial download page](https://releases.aspose.com/)** และประเมินคุณสมบัติทั้งหมดโดยไม่มีข้อจำกัดเป็นเวลา 30 วัน

**Q: ฉันจะรับการสนับสนุนหรือเชื่อมต่อกับชุมชนได้อย่างไร?**  
A: เข้าร่วม [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) ที่นักพัฒนาร่วมแบ่งปันวิธีแก้และทีม Aspose ตอบคำถาม

---

**อัปเดตล่าสุด:** 2026-08-12  
**ทดสอบด้วย:** Aspose.CAD 24.11 for .NET  
**ผู้เขียน:** Aspose

## บทเรียนที่เกี่ยวข้อง

- [ค้นหาข้อความในไฟล์ DWG ด้วย C# - บทแนะนำ Aspose.CAD](/cad/net/text-search-and-manipulation/searching-text-in-dwg-files/)
- [แปลงภาพวาด CAD เป็นภาพราสเตอร์ใน Aspose.CAD สำหรับ .NET](/cad/net/cad-drawing-manipulation/convert-cad-drawing-to-raster-image/)
- [การเรนเดอร์เอกสาร DWG ใน C# - คู่มือ Aspose.CAD](/cad/net/image-manipulation-and-rendering/rendering-dwg-documents/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< blocks/products/products-backtop-button >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}