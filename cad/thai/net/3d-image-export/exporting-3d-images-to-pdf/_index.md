---
date: 2026-07-04
description: เรียนรู้วิธีตั้งขนาดหน้ากระดาษ PDF และส่งออก PDF จากภาพ 3D CAD โดยใช้
  Aspose.CAD สำหรับ .NET – คู่มือขั้นตอนต่อขั้นตอนในการแปลง DWG เป็น PDF และบันทึก
  CAD เป็น PDF
keywords:
- set pdf page size
- export pdf from cad
- convert dwg to pdf
- save cad as pdf
- cad to pdf tutorial
linktitle: การส่งออกภาพ 3D เป็น PDF
schemas:
- author: Aspose
  dateModified: '2026-07-04'
  description: Learn how to set PDF page size and export PDF from 3D CAD images using
    Aspose.CAD for .NET – a step‑by‑step guide to convert DWG to PDF and save CAD
    as PDF.
  headline: Set PDF page size – Export 3D Images to PDF with Aspose.CAD
  type: TechArticle
- description: Learn how to set PDF page size and export PDF from 3D CAD images using
    Aspose.CAD for .NET – a step‑by‑step guide to convert DWG to PDF and save CAD
    as PDF.
  name: Set PDF page size – Export 3D Images to PDF with Aspose.CAD
  steps:
  - name: Load the CAD Image
    text: '`Image` class represents a CAD drawing loaded into memory, ready for rasterization.'
  - name: Configure Rasterization Options (Save CAD as PDF)
    text: '`RasterizationOptions` class defines how the CAD data is rasterized, including
      page size, DPI, and whether 3‑D entities are rendered.'
  - name: Set PDF Options (Create PDF from CAD)
    text: '`PdfOptions` class holds the output format settings and links the rasterization
      options to PDF generation.'
  - name: Save as PDF (Generate PDF from 3D Model)
    text: '`Save` method on the `Image` object writes the rasterized content to the
      specified PDF file, producing a ready‑to‑share document.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD supports more than 50 input and output formats, including
      DWG, DXF, DGN, STL, and IFC, ensuring flexibility for any project.
    question: Is Aspose.CAD compatible with all CAD file formats?
  - answer: Absolutely. Set `PageWidth` and `PageHeight` in `RasterizationOptions`
      to any size in points, inches, or millimetres before calling `Save`.
    question: Can I customize the page dimensions when exporting to PDF?
  - answer: Yes, you can obtain temporary licenses for Aspose.CAD by visiting [Temporary
      License](https://purchase.aspose.com/temporary-license/).
    question: Are temporary licenses available for Aspose.CAD?
  - answer: Head to the [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19) for
      expert help and peer‑to‑peer advice.
    question: Where can I find additional support or community discussions?
  - answer: Yes, you can explore the features of Aspose.CAD by accessing the [free
      trial](https://releases.aspose.com/).
    question: Is there a free trial version of Aspose.CAD?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: ตั้งขนาดหน้ากระดาษ PDF – ส่งออกภาพ 3D เป็น PDF ด้วย Aspose.CAD
url: /th/net/3d-image-export/exporting-3d-images-to-pdf/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# การส่งออกภาพ 3 มิติเป็น PDF - บทแนะนำ Aspose.CAD

## บทนำ

หากคุณต้องการ **ตั้งขนาดหน้ากระดาษ PDF** ขณะแปลงภาพวาด CAD 3‑D เป็น PDF คุณมาถูกที่แล้ว บทแนะนำนี้จะแสดงให้คุณเห็นขั้นตอนต่อขั้นตอนว่าจะโหลดไฟล์ CAD อย่างไร ตั้งค่าตัวเลือกการเรสเตอร์ไลซ์รวมถึงขนาดหน้ากระดาษที่กำหนดเอง และสร้าง PDF คุณภาพสูงโดยใช้ Aspose.CAD สำหรับ .NET เมื่อเสร็จคุณจะสามารถ **ส่งออก PDF จาก CAD**, **บันทึก CAD เป็น PDF**, และควบคุมรายละเอียดการจัดวางทุกอย่างโดยไม่ต้องติดตั้ง AutoCAD.

## คำตอบเร็ว
- **อะไรหมายถึง “export PDF from CAD”?** มันแปลงภาพวาด CAD (DWG, DXF, DGN ฯลฯ) ให้เป็นไฟล์ PDF ที่สามารถเปิดได้บนอุปกรณ์ใดก็ได้.  
- **ไลบรารีใดทำการแปลง?** Aspose.CAD สำหรับ .NET ให้การเรสเตอร์ไลซ์และการส่งออก PDF โดยไม่มีการพึ่งพาไลบรารีภายนอก.  
- **ฉันต้องการไลเซนส์หรือไม่?** จำเป็นต้องมีไลเซนส์ชั่วคราวหรือเต็มสำหรับการใช้งานจริง; มีรุ่นทดลองฟรีให้ใช้.  
- **ฉันสามารถตั้งขนาดหน้ากระดาษแบบกำหนดเองได้หรือไม่?** ได้—ใช้ `PageWidth` และ `PageHeight` ใน `RasterizationOptions`.  
- **รูปทรง 3‑D จะถูกเก็บไว้หรือไม่?** เอนทิตี 3‑D จะถูกเรสเตอร์ไลซ์; เปิดใช้งาน `TypeOfEntities.Entities3D` เพื่อรับการสนับสนุน 3‑D อย่างเต็มที่.

## “export PDF” หมายถึงอะไรในบริบทของ CAD?

การส่งออก PDF จาก CAD หมายถึงการนำภาพวาด CAD (DWG, DXF, DGN ฯลฯ) มาแปลงเป็นไฟล์ PDF ที่สามารถบรรจุกราฟิกเวกเตอร์, มุมมอง 3‑D ที่เรสเตอร์ไลซ์, และข้อมูลการจัดหน้าอย่างแม่นยำ ทำให้สามารถแชร์กับผู้ที่ไม่มีซอฟต์แวร์ CAD ได้ง่าย.

## ทำไมต้องใช้ Aspose.CAD เพื่อส่งออก PDF?

Aspose.CAD ให้คุณ **ตั้งขนาดหน้ากระดาษ PDF** และส่งออก PDF ทั้งหมดด้วยโค้ด .NET ที่จัดการได้เอง รองรับรูปแบบ CAD มากกว่า 50 แบบ, ประมวลผลไฟล์ขนาดถึง 2 GB โดยไม่ต้องโหลดเอกสารทั้งหมดเข้าสู่หน่วยความจำ, และคงรักษาน้ำหนักเส้น, สี, และการเรนเดอร์เอนทิตี 3‑D แบบเลือกได้ด้วย DPI การเรสเตอร์ไลซ์สูงสุดถึง 1200 ไลบรารีทำงานบน Windows, Linux, และ macOS ทำให้ PDF ที่สร้างขึ้นทำงานได้บนทุกแพลตฟอร์ม.

## ข้อกำหนดเบื้องต้น

- **Aspose.CAD for .NET** ติดตั้งแล้ว ดาวน์โหลดได้จาก [หน้าดาวน์โหลด Aspose.CAD for .NET](https://releases.aspose.com/cad/net/).  
- โฟลเดอร์ที่มีไฟล์ CAD ที่คุณต้องการแปลง (เช่น `C:\CAD\`).  
- .NET 6.0 หรือใหม่กว่า (หรือ .NET Framework 4.7.2).  

## นำเข้า Namespaces

คำสั่ง `using` นำเข้า namespaces ของ Aspose.CAD ที่จำเป็นสำหรับการทำงานกับตัวเลือกการเรสเตอร์ไลซ์และ PDF.  

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
```

## คู่มือขั้นตอนต่อขั้นตอน

### วิธีตั้งขนาดหน้ากระดาษ PDF เมื่อส่งออก CAD เป็น PDF?

โหลดไฟล์ CAD ของคุณ, ตั้งค่าขนาดหน้ากระดาษใน `RasterizationOptions`, แนบตัวเลือกเหล่านั้นไปยังอินสแตนซ์ของ `PdfOptions`, แล้วเรียก `Save`. กระบวนการสี่ขั้นตอนนี้ให้คุณควบคุมขนาดและคุณภาพของผลลัพธ์ได้เต็มที่พร้อมโค้ดที่กระชับ.

### ขั้นตอนที่ 1: โหลดภาพ CAD

คลาส `Image` แสดงภาพวาด CAD ที่โหลดเข้าสู่หน่วยความจำ พร้อมสำหรับการเรสเตอร์ไลซ์.  

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";
using (Image cadImage = Image.Load(sourceFilePath))
{
    // Your code for loading the CAD image goes here
}
```

### ขั้นตอนที่ 2: ตั้งค่าตัวเลือกการเรสเตอร์ไลซ์ (บันทึก CAD เป็น PDF)

คลาส `RasterizationOptions` กำหนดวิธีการเรสเตอร์ไลซ์ข้อมูล CAD รวมถึงขนาดหน้า, DPI, และการเรนเดอร์เอนทิตี 3‑D หรือไม่.  

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
// rasterizationOptions.TypeOfEntities = TypeOfEntities.Entities3D;

rasterizationOptions.Layouts = new string[] { "Model" };
```

### ขั้นตอนที่ 3: ตั้งค่าตัวเลือก PDF (สร้าง PDF จาก CAD)

คลาส `PdfOptions` เก็บการตั้งค่ารูปแบบผลลัพธ์และเชื่อมต่อตัวเลือกการเรสเตอร์ไลซ์กับการสร้าง PDF.  

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

### ขั้นตอนที่ 4: บันทึกเป็น PDF (สร้าง PDF จากโมเดล 3D)

เมธอด `Save` ของอ็อบเจ็กต์ `Image` เขียนเนื้อหาที่เรสเตอร์ไลซ์ลงในไฟล์ PDF ที่ระบุ ทำให้ได้เอกสารพร้อมแชร์.  

```csharp
MyDir = MyDir + "Export3DImagestoPDF_out.pdf";
cadImage.Save(MyDir, pdfOptions);
```

## ปัญหาทั่วไปและวิธีแก้

| ปัญหา | สาเหตุ | วิธีแก้ |
|-------|--------|-----|
| **PDF ที่ส่งออกเป็นไฟล์เปล่า** | ชื่อเลเอาต์ผิดหรือไม่มีเลเอาต์ `Model`. | ตรวจสอบว่า `rasterizationOptions.Layouts` ตรงกับเลเอาต์ที่มีอยู่ในไฟล์ CAD. |
| **ความละเอียดต่ำ** | ค่า DPI การเรสเตอร์ไลซ์เริ่มต้นต่ำ. | ตั้งค่า `rasterizationOptions.Resolution = 300;` ก่อนบันทึก. |
| **เอนทิตี 3‑D ไม่แสดง** | `TypeOfEntities` ถูกคอมเมนต์ออก. | ยกเลิกคอมเมนต์ `rasterizationOptions.TypeOfEntities = TypeOfEntities.Entities3D;`. |
| **ข้อยกเว้นไลเซนส์** | ใช้รุ่นทดลองโดยไม่มีไลเซนส์. | ใช้ไลเซนส์ชั่วคราวหรือถาวรโดยเรียก `License license = new License(); license.SetLicense("Aspose.CAD.lic");`. |

## คำถามที่พบบ่อย

**ถาม: Aspose.CAD รองรับรูปแบบไฟล์ CAD ทั้งหมดหรือไม่?**  
ตอบ: ใช่, Aspose.CAD รองรับรูปแบบไฟล์เข้าและออกมากกว่า 50 รูปแบบ รวมถึง DWG, DXF, DGN, STL, และ IFC ทำให้มีความยืดหยุ่นสำหรับโครงการใด ๆ  

**ถาม: ฉันสามารถกำหนดขนาดหน้ากระดาษได้เองเมื่อส่งออกเป็น PDF หรือไม่?**  
ตอบ: แน่นอน. ตั้งค่า `PageWidth` และ `PageHeight` ใน `RasterizationOptions` ให้เป็นขนาดใดก็ได้ในหน่วย points, inches หรือ millimetres ก่อนเรียก `Save`.  

**ถาม: มีไลเซนส์ชั่วคราวสำหรับ Aspose.CAD หรือไม่?**  
ตอบ: มี, คุณสามารถรับไลเซนส์ชั่วคราวสำหรับ Aspose.CAD ได้โดยไปที่ [Temporary License](https://purchase.aspose.com/temporary-license/).  

**ถาม: ฉันจะหาแหล่งสนับสนุนเพิ่มเติมหรือการสนทนาชุมชนได้ที่ไหน?**  
ตอบ: ไปที่ [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19) เพื่อรับความช่วยเหลือจากผู้เชี่ยวชาญและคำแนะนำจากชุมชน.  

**ถาม: มีเวอร์ชันทดลองฟรีของ Aspose.CAD หรือไม่?**  
ตอบ: มี, คุณสามารถสำรวจคุณสมบัติของ Aspose.CAD ได้โดยเข้าที่ [free trial](https://releases.aspose.com/).  

## สรุป

ตอนนี้คุณมีวิธีที่ครบถ้วนและพร้อมใช้งานในระดับการผลิตเพื่อ **ตั้งขนาดหน้ากระดาษ PDF** และ **ส่งออก PDF จากภาพ CAD 3D** ด้วย Aspose.CAD สำหรับ .NET โดยการปรับตัวเลือกการเรสเตอร์ไลซ์คุณสามารถปรับความละเอียด, การจัดหน้า, และการเรนเดอร์เอนทิตี 3‑D ให้ตรงตามความต้องการของเอกสารใด ๆ ทดลองเปลี่ยนค่าการตั้ง DPI และขนาดหน้ากระดาษต่าง ๆ เพื่อหาสมดุลที่สมบูรณ์ระหว่างขนาดไฟล์และความคมชัดของภาพ.

{{< blocks/products/products-backtop-button >}}

## บทแนะนำที่เกี่ยวข้อง

- [ส่งออกเลเอาต์เฉพาะเป็น PDF - คู่มือ Aspose.CAD](/cad/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/)
- [ส่งออก DWG เป็น PDF หรือภาพเรสเตอร์ - คู่มือ Aspose.CAD](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)
- [ส่งออก DGN เป็น PDF ใน Aspose.CAD สำหรับ .NET](/cad/net/cad-export-formats/export-dgn-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

--- 

**อัปเดตล่าสุด:** 2026-07-04  
**ทดสอบด้วย:** Aspose.CAD 24.11 for .NET  
**ผู้เขียน:** Aspose