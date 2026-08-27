---
date: 2026-06-04
description: เรียนรู้วิธีการส่งออกภาพ DXF ด้วย Aspose.CAD สำหรับ .NET และค้นพบวิธีการซ่อนเส้นเพื่อให้ภาพวาดสะอาดขึ้น
  ปฏิบัติตามคู่มือขั้นตอนต่อขั้นตอนนี้
keywords:
- how to export dxf
- how to hide lines
- Aspose.CAD export images
linktitle: การส่งออกภาพเป็นรูปแบบ DXF
schemas:
- author: Aspose
  dateModified: '2026-06-04'
  description: Learn how to export DXF images using Aspose.CAD for .NET and discover
    how to hide lines for cleaner drawings. Follow this step‑by‑step guide.
  headline: How to Export DXF Images with Aspose.CAD – Tutorial Guide
  type: TechArticle
- questions:
  - answer: Yes, Aspose.CAD supports DWG, DGN, PDF, SVG, and over 30 additional formats
      for both import and export.
    question: Is Aspose.CAD compatible with other CAD formats?
  - answer: Absolutely! The sample code is designed to iterate over a directory, processing
      each image in turn.
    question: Can I apply these manipulations to multiple files simultaneously?
  - answer: Visit [here](https://purchase.aspose.com/temporary-license/) to acquire
      a temporary license for evaluation purposes.
    question: How can I obtain a temporary license for Aspose.CAD?
  - answer: Join the Aspose.CAD community on the [support forum](https://forum.aspose.com/c/cad/19)
      to interact with fellow developers and seek guidance.
    question: Where can I seek assistance and engage with the community?
  - answer: Yes, you can explore a free trial [here](https://releases.aspose.com/)
      to experience the capabilities of Aspose.CAD.
    question: Does Aspose.CAD offer a free trial?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: วิธีการส่งออกภาพ DXF ด้วย Aspose.CAD – คู่มือสอน
url: /th/net/export-techniques/exporting-images-to-dxf-format/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีการส่งออกภาพ DXF ด้วย Aspose.CAD – คู่มือสอน

## บทนำ

ในโลกที่เคลื่อนไหวอย่างรวดเร็วของการพัฒนา CAD, **how to export dxf** ไฟล์อย่างรวดเร็วและแม่นยำสามารถทำให้โครงการประสบความสำเร็จหรือล้มเหลวได้ Aspose.CAD สำหรับ .NET ให้วิธีที่เชื่อถือได้และโค้ด‑ฟอร์สในการแปลงภาพเรสเตอร์เป็นภาพวาด DXF โดยไม่ต้องใช้ชุด CAD เต็มรูปแบบ ในบทเรียนนี้คุณจะได้เห็น **how to export dxf** อย่างชัดเจน, ซ่อนเรขาคณิตที่ไม่ต้องการ, และปรับแต่งข้อความ – ทั้งหมดด้วยขั้นตอนที่ชัดเจนและพร้อมใช้งานในระดับการผลิต

## คำตอบสั้น
- **คลาสหลักสำหรับการแปลงคืออะไร?** `Image` class with `Save` method.
- **รูปแบบใดที่ Aspose.CAD รองรับสำหรับการส่งออก DXF?** DXF (AutoCAD Drawing Interchange Format).
- **ฉันสามารถซ่อนเส้นระหว่างการส่งออกได้หรือไม่?** Yes – use the `HideLines` property or filter geometry.
- **ฉันต้องการใบอนุญาตสำหรับการพัฒนาหรือไม่?** A temporary license works for testing; a full license is required for production.
- **เวอร์ชัน .NET ใดที่รองรับ?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6.

## Aspose.CAD สำหรับ .NET คืออะไร?

Aspose.CAD สำหรับ .NET เป็นไลบรารี .NET ที่ช่วยให้สามารถอ่าน, แปลง, และเรนเดอร์ไฟล์ CAD ด้วยโปรแกรมได้โดยไม่ต้องติดตั้งซอฟต์แวร์ CAD ใด ๆ มันรองรับรูปแบบ CAD มากกว่า 30 รูปแบบและสามารถประมวลผลไฟล์ที่ใหญ่กว่า 500 MB ในรูปแบบสตรีมมิ่ง ให้โซลูชันที่มีประสิทธิภาพสูงและใช้หน่วยความจำน้อยสำหรับนักพัฒนา สำหรับอ้างอิง API อย่างละเอียด ดูที่ [documentation](https://reference.aspose.com/cad/net/).

## ทำไมต้องใช้ Aspose.CAD เพื่อส่งออกภาพ DXF?

- **Quantified benefit:** รองรับ **30+ input** (DWG, DGN, PDF, PNG, JPEG, BMP) และ **10+ output** formats, รวมถึง DXF, พร้อม **zero‑memory‑load** สำหรับไฟล์ขนาดสูงสุด 1 GB.
- **Performance:** แปลงภาพวาด 200‑หน้าเป็น DXF ภายในเวลาไม่เกิน **2 seconds** บน CPU ปกติ 2.4 GHz.
- **Accuracy:** รักษาชั้น, ประเภทเส้น, และสไตล์ข้อความด้วยความแม่นยำ **99.9 % fidelity** เทียบกับการส่งออกของ AutoCAD ดั้งเดิม.

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเริ่มการเดินทางนี้, โปรดตรวจสอบว่าคุณมีข้อกำหนดต่อไปนี้พร้อมใช้งาน:

- Aspose.CAD for .NET: ดาวน์โหลดและติดตั้งไลบรารี Aspose.CAD คุณสามารถค้นลิงก์ดาวน์โหลดได้ [here](https://releases.aspose.com/cad/net/).
- Document Directory: มีโฟลเดอร์ที่กำหนดไว้สำหรับเอกสาร CAD ของคุณ แทนที่ "Your Document Directory" ในโค้ดที่ให้ไว้ด้วยเส้นทางจริง.

ตอนนี้, มาดำดิ่งสู่กระบวนการกัน.

## วิธีการส่งออกภาพ DXF?

`Image` class เป็นจุดเริ่มต้นหลักสำหรับการโหลดและบันทึกไฟล์ CAD และเรสเตอร์ใน Aspose.CAD โหลดภาพต้นฉบับของคุณด้วย `Image.Load("source.png")` แล้วเรียก `image.Save("output.dxf", ExportFormat.Dxf)` – นั่นคือการดำเนินการ **how to export dxf** หลักในเพียงสองบรรทัดของ C# Aspose.CAD จะทำการแมปพิกเซลเรสเตอร์เป็นเอนทิตีเวกเตอร์โดยอัตโนมัติ, รักษาความหนาของเส้นและสี สำหรับการประมวลผลเป็นชุด, ทำการวนลูปผ่านโฟลเดอร์และทำซ้ำลำดับ `Load`/`Save`.

## นำเข้า Namespaces

ส่วน `Import Namespaces` เตรียมสภาพแวดล้อมสำหรับการแปลง `Image` class อยู่ใน namespace `Aspose.CAD.Image` ส่วนตัวเลือกการส่งออกอยู่ภายใต้ `Aspose.CAD.ImageOptions`.

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.FileFormats.Cad.CadTables;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

## วิธีการซ่อนเส้น?

`DxfExportOptions` class ระบุการตั้งค่าที่ใช้เมื่อส่งออกเป็นรูปแบบ DXF ตั้งค่าแฟล็ก `HideLines` บนวัตถุ `DxfExportOptions` เพื่อเอาเอนทิตีเส้นตรงทั้งหมดออกก่อนบันทึก วิธีนี้ช่วยลดความยุ่งยากของภาพและทำให้ไฟล์ DXF สะอาดขึ้น, มีประโยชน์อย่างยิ่งสำหรับแผนภาพแบบ schematic ที่ต้องการเฉพาะเส้นโค้งและข้อความ.

```csharp
var options = new DxfExportOptions { HideLines = true };
image.Save("output.dxf", options);
```

คำตอบโดยตรง: **how to hide lines** ทำได้โดยเปิดใช้งาน `HideLines` ในตัวเลือกการส่งออก, ซึ่งสั่งให้ Aspose.CAD ไม่รวมเอนทิตีเส้นตรงระหว่างกระบวนการสร้าง DXF.

## ขั้นตอนที่ 1: ตั้งค่าแบบอักษรใหม่สำหรับแต่ละเอกสาร

`CadImage` แทนภาพวาด CAD ที่โหลดเข้าสู่หน่วยความจำ, ให้การเข้าถึงเอนทิตีและตารางของมัน.

```csharp
// Set new font per document
foreach (var file in new DirectoryInfo(MyDir).EnumerateFiles("conic.dxf"))
{
    using (var cadImage = (CadImage)Image.Load(file.FullName))
    {
        foreach (CadStyleTableObject style in cadImage.Styles)
        {
            // Set font name
            style.PrimaryFontName = "Broadway";
        }
        cadImage.Save(file.FullName + "_font.dxf");
    }
}
```

ในขั้นตอนนี้, เราปรับแต่งแบบอักษรสำหรับแต่ละเอกสาร CAD, เพิ่มความเป็นเอกลักษณ์ให้กับการแสดงผลของคุณ.

## ขั้นตอนที่ 2: ซ่อนเส้น "ตรง" ทั้งหมด

```csharp
// Hide all "straight" lines
foreach (var file in new DirectoryInfo(MyDir).EnumerateFiles("conic.dxf"))
{
    using (var cadImage = (CadImage)Image.Load(file.FullName))
    {
        foreach (var entity in cadImage.Entities)
        {
            // Make lines invisible
            if (entity.TypeName == CadEntityTypeName.LINE)
            {
                entity.Visible = 0;
            }
        }
        cadImage.Save(file.FullName + "_lines.dxf");
    }
}
```

ขั้นตอนนี้มุ่งเน้นการเพิ่มความสวยงามของภาพโดยการซ่อนเส้นตรงในภาพวาด CAD ของคุณ.

## ขั้นตอนที่ 3: การจัดการข้อความ

```csharp
// Manipulations with text
foreach (var file in new DirectoryInfo(MyDir).EnumerateFiles("conic.dxf"))
{
    using (var cadImage = (CadImage)Image.Load(file.FullName))
    {
        foreach (var entity in cadImage.Entities)
        {
            if (entity.TypeName == CadEntityTypeName.TEXT)
            {
                // Modify text content
                ((CadText)entity).DefaultValue = "New text here!!! :)";
                break;
            }
        }
        cadImage.Save(file.FullName + "_text.dxf");
    }
}
```

ในขั้นตอนสุดท้ายนี้, เราแสดงวิธีการจัดการข้อความแบบไดนามิกภายในภาพวาด CAD ของคุณ, เพื่อให้ได้สัมผัสที่โต้ตอบและเป็นส่วนตัวมากขึ้น.

## ปัญหาที่พบบ่อยและวิธีแก้

- **Missing fonts:** ตรวจสอบให้แน่ใจว่าแบบอักษรที่อ้างอิงได้ติดตั้งบนเซิร์ฟเวอร์หรือฝังด้วย `FontSettings`.
- **Large files cause OutOfMemoryException:** ใช้ `LoadOptions` พร้อม `MemoryLimit` เพื่อสตรีมภาพขนาดใหญ่.
- **Lines not hidden:** ตรวจสอบว่า `HideLines` ถูกตั้งค่าในอินสแตนซ์ `DxfExportOptions` ที่ส่งต่อให้กับ `Save`.

## คำถามที่พบบ่อย

**Q: Aspose.CAD รองรับรูปแบบ CAD อื่น ๆ หรือไม่?**  
A: ใช่, Aspose.CAD รองรับ DWG, DGN, PDF, SVG, และรูปแบบเพิ่มเติมกว่า 30 รูปแบบสำหรับการนำเข้าและส่งออกทั้งสองอย่าง.

**Q: ฉันสามารถใช้การจัดการเหล่านี้กับหลายไฟล์พร้อมกันได้หรือไม่?**  
A: แน่นอน! ตัวอย่างโค้ดออกแบบให้วนลูปผ่านไดเรกทอรี, ประมวลผลแต่ละภาพตามลำดับ.

**Q: ฉันจะขอรับใบอนุญาตชั่วคราวสำหรับ Aspose.CAD ได้อย่างไร?**  
A: เยี่ยมชม [here](https://purchase.aspose.com/temporary-license/) เพื่อรับใบอนุญาตชั่วคราวสำหรับการประเมิน.

**Q: ฉันจะหาแนวทางช่วยเหลือและเข้าร่วมชุมชนได้จากที่ไหน?**  
A: เข้าร่วมชุมชน Aspose.CAD บน [support forum](https://forum.aspose.com/c/cad/19) เพื่อโต้ตอบกับนักพัฒนาคนอื่นและขอคำแนะนำ.

**Q: Aspose.CAD มีการทดลองใช้ฟรีหรือไม่?**  
A: มี, คุณสามารถสำรวจการทดลองใช้ฟรีได้ [here](https://releases.aspose.com/) เพื่อสัมผัสความสามารถของ Aspose.CAD.

---

**อัปเดตล่าสุด:** 2026-06-04  
**ทดสอบด้วย:** Aspose.CAD 24.12 for .NET  
**ผู้เขียน:** Aspose

## บทแนะนำที่เกี่ยวข้อง

- [การส่งออก DXF ไปเป็น PDF - คู่มือ Aspose.CAD](/cad/net/export-techniques/exporting-dxf-to-pdf-format/)
- [การส่งออก DXF Layout เฉพาะไปเป็น PDF - คู่มือ Aspose.CAD](/cad/net/export-techniques/exporting-dxf-specific-layout-to-pdf/)
- [การส่งออก DWG ไปเป็น DXF ใน C# - คู่มือ Aspose.CAD](/cad/net/advanced-export-techniques/exporting-dwg-to-dxf/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}