---
title: Set PDF page size – Export 3D Images to PDF with Aspose.CAD
linktitle: Exporting 3D Images to PDF
second_title: Aspose.CAD .NET - CAD and BIM File Format
description: Learn how to set PDF page size and export PDF from 3D CAD images using Aspose.CAD for .NET – a step‑by‑step guide to convert DWG to PDF and save CAD as PDF.
weight: 10
url: /net/3d-image-export/exporting-3d-images-to-pdf/
date: 2026-07-04
keywords:
- set pdf page size
- export pdf from cad
- convert dwg to pdf
- save cad as pdf
- cad to pdf tutorial
schemas:
- type: TechArticle
  headline: Set PDF page size – Export 3D Images to PDF with Aspose.CAD
  description: Learn how to set PDF page size and export PDF from 3D CAD images using
    Aspose.CAD for .NET – a step‑by‑step guide to convert DWG to PDF and save CAD
    as PDF.
  dateModified: '2026-07-04'
  author: Aspose
- type: HowTo
  name: Set PDF page size – Export 3D Images to PDF with Aspose.CAD
  description: Learn how to set PDF page size and export PDF from 3D CAD images using
    Aspose.CAD for .NET – a step‑by‑step guide to convert DWG to PDF and save CAD
    as PDF.
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
- type: FAQPage
  questions:
  - question: Is Aspose.CAD compatible with all CAD file formats?
    answer: Yes, Aspose.CAD supports more than 50 input and output formats, including
      DWG, DXF, DGN, STL, and IFC, ensuring flexibility for any project.
  - question: Can I customize the page dimensions when exporting to PDF?
    answer: Absolutely. Set `PageWidth` and `PageHeight` in `RasterizationOptions`
      to any size in points, inches, or millimetres before calling `Save`.
  - question: Are temporary licenses available for Aspose.CAD?
    answer: Yes, you can obtain temporary licenses for Aspose.CAD by visiting [Temporary
      License](https://purchase.aspose.com/temporary-license/).
  - question: Where can I find additional support or community discussions?
    answer: Head to the [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19) for
      expert help and peer‑to‑peer advice.
  - question: Is there a free trial version of Aspose.CAD?
    answer: Yes, you can explore the features of Aspose.CAD by accessing the [free
      trial](https://releases.aspose.com/).
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exporting 3D Images to PDF - Aspose.CAD Tutorial

## Introduction

If you need to **set PDF page size** while converting a 3‑D CAD drawing to PDF, you’ve come to the right place. This tutorial shows you, step by step, how to load a CAD file, configure rasterization options—including custom page dimensions—and generate a high‑fidelity PDF using Aspose.CAD for .NET. By the end you’ll be able to **export PDF from CAD**, **save CAD as PDF**, and control every layout detail without installing AutoCAD.

## Quick Answers
- **What does “export PDF from CAD” mean?** It converts a CAD drawing (DWG, DXF, DGN, etc.) into a PDF that can be opened on any device.  
- **Which library performs the conversion?** Aspose.CAD for .NET provides rasterization and PDF export without external dependencies.  
- **Do I need a license?** A temporary or full license is required for production; a free trial is available.  
- **Can I set custom page dimensions?** Yes—use `PageWidth` and `PageHeight` in `RasterizationOptions`.  
- **Will 3‑D geometry be retained?** The 3‑D entities are rasterized; enable `TypeOfEntities.Entities3D` for full 3‑D support.

## What is “export PDF” in the context of CAD?

Exporting PDF from CAD means taking a CAD drawing (DWG, DXF, DGN, etc.) and converting it into a PDF file that can contain vector graphics, rasterized 3‑D views, and precise page layout information, making it easy to share with anyone who does not have CAD software.

## Why use Aspose.CAD to export PDF?

Aspose.CAD lets you **set PDF page size** and export PDFs entirely in managed .NET code. It supports over 50 CAD formats, processes files up to 2 GB without loading the whole document into memory, and preserves line weights, colors, and optional 3‑D entity rendering with a rasterization DPI of up to 1200. The library runs on Windows, Linux, and macOS, so the generated PDFs work on any platform.

## Prerequisites

- **Aspose.CAD for .NET** installed. Download it from the [Aspose.CAD for .NET download page](https://releases.aspose.com/cad/net/).  
- A folder containing the CAD files you want to convert (e.g., `C:\CAD\`).  
- .NET 6.0 or later (or .NET Framework 4.7.2).  

## Import Namespaces

`using` statements import the Aspose.CAD namespaces needed to work with rasterization and PDF options.  

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
```

## Step‑by‑Step Guide

### How to set PDF page size when exporting CAD to PDF?

Load your CAD file, configure the page dimensions in `RasterizationOptions`, attach those options to a `PdfOptions` instance, and call `Save`. This four‑step flow gives you full control over the output size and quality while keeping the code concise.

### Step 1: Load the CAD Image

`Image` class represents a CAD drawing loaded into memory, ready for rasterization.  

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";
using (Image cadImage = Image.Load(sourceFilePath))
{
    // Your code for loading the CAD image goes here
}
```

### Step 2: Configure Rasterization Options (Save CAD as PDF)

`RasterizationOptions` class defines how the CAD data is rasterized, including page size, DPI, and whether 3‑D entities are rendered.  

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
// rasterizationOptions.TypeOfEntities = TypeOfEntities.Entities3D;

rasterizationOptions.Layouts = new string[] { "Model" };
```

### Step 3: Set PDF Options (Create PDF from CAD)

`PdfOptions` class holds the output format settings and links the rasterization options to PDF generation.  

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

### Step 4: Save as PDF (Generate PDF from 3D Model)

`Save` method on the `Image` object writes the rasterized content to the specified PDF file, producing a ready‑to‑share document.  

```csharp
MyDir = MyDir + "Export3DImagestoPDF_out.pdf";
cadImage.Save(MyDir, pdfOptions);
```

## Common Issues and Solutions

| Issue | Reason | Fix |
|-------|--------|-----|
| **Output PDF is blank** | Wrong layout name or missing `Model` layout. | Verify `rasterizationOptions.Layouts` matches a layout present in the CAD file. |
| **Low resolution** | Default rasterization DPI is low. | Set `rasterizationOptions.Resolution = 300;` before saving. |
| **3‑D entities not shown** | `TypeOfEntities` is commented out. | Uncomment `rasterizationOptions.TypeOfEntities = TypeOfEntities.Entities3D;`. |
| **License exception** | Using a trial without a license. | Apply a temporary or permanent license via `License license = new License(); license.SetLicense("Aspose.CAD.lic");`. |

## Frequently Asked Questions

**Q: Is Aspose.CAD compatible with all CAD file formats?**  
A: Yes, Aspose.CAD supports more than 50 input and output formats, including DWG, DXF, DGN, STL, and IFC, ensuring flexibility for any project.

**Q: Can I customize the page dimensions when exporting to PDF?**  
A: Absolutely. Set `PageWidth` and `PageHeight` in `RasterizationOptions` to any size in points, inches, or millimetres before calling `Save`.

**Q: Are temporary licenses available for Aspose.CAD?**  
A: Yes, you can obtain temporary licenses for Aspose.CAD by visiting [Temporary License](https://purchase.aspose.com/temporary-license/).

**Q: Where can I find additional support or community discussions?**  
A: Head to the [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19) for expert help and peer‑to‑peer advice.

**Q: Is there a free trial version of Aspose.CAD?**  
A: Yes, you can explore the features of Aspose.CAD by accessing the [free trial](https://releases.aspose.com/).

## Conclusion

You now have a complete, production‑ready method to **set PDF page size** and **export PDF from 3D CAD images** using Aspose.CAD for .NET. By adjusting rasterization options you can fine‑tune resolution, page layout, and 3‑D entity rendering to meet any documentation requirement. Experiment with different DPI settings and page dimensions to achieve the perfect balance between file size and visual fidelity.

{{< blocks/products/products-backtop-button >}}

## Related Tutorials

- [Exporting Specific Layouts to PDF - Aspose.CAD Guide](/cad/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/)
- [Exporting DWG to PDF or Raster Images - Aspose.CAD Guide](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)
- [Export DGN to PDF in Aspose.CAD for .NET](/cad/net/cad-export-formats/export-dgn-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

--- 

**Last Updated:** 2026-07-04  
**Tested With:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose