---
date: 2026-03-29
description: เรียนรู้วิธีสร้าง PDF จาก CAD ตั้งขนาดแคนวาส และส่งออก CAD เป็น PDF หรือ
  TIFF ด้วย Aspose.CAD สำหรับ .NET ในคู่มือขั้นตอนต่อขั้นตอนนี้
linktitle: Setting Canvas Size and Mode
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: 'วิธีสร้าง PDF จาก CAD: ตั้งค่าขนาดแคนวาสและโหมดใน Aspose.CAD สำหรับ .NET'
url: /th/net/cad-features-and-support/setting-canvas-size-and-mode/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# กำหนดขนาดและโหมดของแคนวาสใน Aspose.CAD สำหรับ .NET

## บทนำ

Ready to **create PDF from CAD** files while controlling the output dimensions? In this tutorial we’ll walk through setting the canvas size and mode, loading a CAD file, and exporting it to PDF or TIFF with Aspose.CAD for .NET. Whether you need to **convert DXF to PDF**, generate high‑resolution drawings, or simply adjust the rasterization area, the steps below will give you a solid, production‑ready solution.

## คำตอบอย่างรวดเร็ว
- **What does “create PDF from CAD” mean?** การแปลงภาพวาด CAD (เช่น DXF, DWG) เป็นเอกสาร PDF ที่คงรายละเอียดเวกเตอร์และเรสเตอร์ไว้  
- **Which option controls the output size?** `CadRasterizationOptions.PageWidth` และ `PageHeight` (ขนาดแคนวาส)  
- **Can I export to TIFF as well?** ใช่ – ใช้ `TiffOptions` พร้อมการตั้งค่า rasterization เดียวกัน  
- **Do I need a license for production?** จำเป็นต้องมีใบอนุญาตเชิงพาณิชย์; มีรุ่นทดลองฟรีให้ใช้  
- **Supported .NET versions?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7  

## “create PDF from CAD” คืออะไร?
Creating a PDF from CAD means rendering the CAD drawing into a page‑oriented format (PDF) that can be viewed, printed, or shared without needing CAD software. Aspose.CAD handles the heavy lifting, letting you define canvas size, scaling, and output format.

## ทำไมต้องกำหนดขนาดแคนวาสเมื่อสร้าง PDF จาก CAD?
Setting the canvas size gives you precise control over the resolution and dimensions of the resulting PDF or TIFF. This is especially useful when:
- Preparing drawings for printing on specific paper sizes.  
- Generating thumbnails or high‑resolution images for web preview.  
- Ensuring consistent layout across multiple documents.

## ข้อกำหนดเบื้องต้น

- Aspose.CAD Library: Download and install the Aspose.CAD library from the [Aspose.CAD website](https://releases.aspose.com/cad/net/).  
- Development Environment: Ensure you have a .NET development environment set up on your machine.  
- Sample CAD File: For this tutorial, we'll use a sample DXF file. You can find one in the [Aspose.CAD documentation](https://reference.aspose.com/cad/net/).

## นำเข้า Namespaces

First, import the namespaces required for CAD processing:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## วิธีสร้าง PDF จาก CAD ด้วยขนาดแคนวาสที่กำหนดเอง

### ขั้นตอนที่ 1: โหลดไฟล์ CAD

We start by **loading the CAD file** (e.g., a DXF) into an `Image` object. This is the point where you **load CAD file** into memory.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (Image image = Image.Load(sourceFilePath))
{
    // Your code for further steps will go here
}
```

### ขั้นตอนที่ 2: สร้าง CadRasterizationOptions

Create a `CadRasterizationOptions` instance and define the canvas size. The `PageWidth` and `PageHeight` properties let you **set canvas size** to the exact dimensions you need.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.AutomaticLayoutsScaling = true;
rasterizationOptions.NoScaling = false;
```

### ขั้นตอนที่ 3: สร้าง PdfOptions (ส่งออก CAD เป็น PDF)

Link the rasterization settings to a `PdfOptions` object. This configuration enables you to **export CAD to PDF** with the custom canvas you defined.

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

### ขั้นตอนที่ 4: ส่งออกเป็น PDF (แปลง DXF เป็น PDF)

Now save the image as a PDF. This step **creates PDF from CAD** using the options we set.

```csharp
image.Save(MyDir + "result_out.pdf", pdfOptions);
```

### ขั้นตอนที่ 5: สร้าง TiffOptions (ส่งออก CAD เป็น TIFF)

If you also need a raster image, configure `TiffOptions`. The same rasterization options are reused, so the **export CAD to TIFF** respects the canvas size.

```csharp
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.VectorRasterizationOptions = rasterizationOptions;
```

### ขั้นตอนที่ 6: ส่งออกเป็น TIFF

Finally, save the drawing as a TIFF file.

```csharp
image.Save(MyDir + "result_out.tiff", tiffOptions);
```

## ปัญหาทั่วไปและวิธีแก้

- **Canvas appears cropped** – ตรวจสอบว่า `AutomaticLayoutsScaling` ตั้งเป็น `true` และ `NoScaling` ตั้งเป็น `false` เพื่อให้ภาพวาดปรับขนาดให้พอดีกับแคนวาส  
- **Low‑resolution PDF** – เพิ่มค่า `PageWidth`/`PageHeight` หรือกำหนด `Resolution` ใน `CadRasterizationOptions`  
- **File not found error** – ตรวจสอบว่า `MyDir` ชี้ไปยังไดเรกทอรีที่ถูกต้องและชื่อไฟล์ DXF ตรงกันอย่างแม่นยำ  

## คำถามที่พบบ่อย

### Q1: ฉันสามารถใช้ Aspose.CAD กับไลบรารี .NET อื่นได้หรือไม่?
A1: Yes, Aspose.CAD seamlessly integrates with other .NET libraries, providing enhanced capabilities for CAD manipulation.

### Q2: มีรุ่นทดลองฟรีสำหรับ Aspose.CAD หรือไม่?
A2: Yes, you can explore the features of Aspose.CAD with a free trial. Visit [here](https://releases.aspose.com/) to get started.

### Q3: ฉันจะได้รับการสนับสนุนสำหรับ Aspose.CAD อย่างไร?
A3: For support and discussions, visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19).

### Q4: ฉันจะหาเอกสารประกอบที่ครบถ้วนสำหรับ Aspose.CAD ได้จากที่ไหน?
A4: Refer to the [Aspose.CAD documentation](https://reference.aspose.com/cad/net/) for detailed information and examples.

### Q5: ฉันจะซื้อ Aspose.CAD สำหรับ .NET อย่างไร?
A5: To purchase Aspose.CAD, visit the [purchase page](https://purchase.aspose.com/buy).

**คำถามเพิ่มเติม**

**Q: ฉันสามารถส่งออกภาพวาด CAD แบบหลายหน้าเป็น PDF หน้าเดียวได้หรือไม่?**  
A: Yes. Set `PageCount` in `CadRasterizationOptions` and the library will concatenate pages into one PDF.

**Q: ขนาดแคนวาสมีผลต่อคุณภาพข้อมูลเวกเตอร์หรือไม่?**  
A: Vector data remains resolution‑independent; the canvas size only influences rasterized elements and image resolution.

**อัปเดตล่าสุด:** 2026-03-29  
**ทดสอบกับ:** Aspose.CAD 24.11 for .NET  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}