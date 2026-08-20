---
title: "How to Create PDF from CAD: Set Canvas Size and Mode in Aspose.CAD for .NET"
linktitle: Setting Canvas Size and Mode
second_title: Aspose.CAD .NET - CAD and BIM File Format
description: Learn how to create PDF from CAD, set canvas size, and export CAD to PDF or TIFF using Aspose.CAD for .NET in this step‑by‑step guide.
weight: 16
url: /net/cad-features-and-support/setting-canvas-size-and-mode/
date: 2026-03-29
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Setting Canvas Size and Mode in Aspose.CAD for .NET

## Introduction

Ready to **create PDF from CAD** files while controlling the output dimensions? In this tutorial we’ll walk through setting the canvas size and mode, loading a CAD file, and exporting it to PDF or TIFF with Aspose.CAD for .NET. Whether you need to **convert DXF to PDF**, generate high‑resolution drawings, or simply adjust the rasterization area, the steps below will give you a solid, production‑ready solution.

## Quick Answers
- **What does “create PDF from CAD” mean?** Converting a CAD drawing (e.g., DXF, DWG) into a PDF document that preserves vector and raster details.  
- **Which option controls the output size?** `CadRasterizationOptions.PageWidth` and `PageHeight` (canvas size).  
- **Can I export to TIFF as well?** Yes – use `TiffOptions` with the same rasterization settings.  
- **Do I need a license for production?** A commercial license is required; a free trial is available.  
- **Supported .NET versions?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## What is “create PDF from CAD”?
Creating a PDF from CAD means rendering the CAD drawing into a page‑oriented format (PDF) that can be viewed, printed, or shared without needing CAD software. Aspose.CAD handles the heavy lifting, letting you define canvas size, scaling, and output format.

## Why set canvas size when creating PDF from CAD?
Setting the canvas size gives you precise control over the resolution and dimensions of the resulting PDF or TIFF. This is especially useful when:
- Preparing drawings for printing on specific paper sizes.  
- Generating thumbnails or high‑resolution images for web preview.  
- Ensuring consistent layout across multiple documents.

## Prerequisites

- Aspose.CAD Library: Download and install the Aspose.CAD library from the [Aspose.CAD website](https://releases.aspose.com/cad/net/).
- Development Environment: Ensure you have a .NET development environment set up on your machine.
- Sample CAD File: For this tutorial, we'll use a sample DXF file. You can find one in the [Aspose.CAD documentation](https://reference.aspose.com/cad/net/).

## Import Namespaces

First, import the namespaces required for CAD processing:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## How to Create PDF from CAD with Custom Canvas Size

### Step 1: Load CAD File

We start by **loading the CAD file** (e.g., a DXF) into an `Image` object. This is the point where you **load CAD file** into memory.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (Image image = Image.Load(sourceFilePath))
{
    // Your code for further steps will go here
}
```

### Step 2: Create CadRasterizationOptions

Create a `CadRasterizationOptions` instance and define the canvas size. The `PageWidth` and `PageHeight` properties let you **set canvas size** to the exact dimensions you need.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.AutomaticLayoutsScaling = true;
rasterizationOptions.NoScaling = false;
```

### Step 3: Create PdfOptions (Export CAD to PDF)

Link the rasterization settings to a `PdfOptions` object. This configuration enables you to **export CAD to PDF** with the custom canvas you defined.

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

### Step 4: Export to PDF (Convert DXF to PDF)

Now save the image as a PDF. This step **creates PDF from CAD** using the options we set.

```csharp
image.Save(MyDir + "result_out.pdf", pdfOptions);
```

### Step 5: Create TiffOptions (Export CAD to TIFF)

If you also need a raster image, configure `TiffOptions`. The same rasterization options are reused, so the **export CAD to TIFF** respects the canvas size.

```csharp
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.VectorRasterizationOptions = rasterizationOptions;
```

### Step 6: Export to TIFF

Finally, save the drawing as a TIFF file.

```csharp
image.Save(MyDir + "result_out.tiff", tiffOptions);
```

## Common Issues and Solutions

- **Canvas appears cropped** – Verify that `AutomaticLayoutsScaling` is set to `true` and `NoScaling` is `false` so the drawing scales to fit the canvas.  
- **Low‑resolution PDF** – Increase `PageWidth`/`PageHeight` or set `Resolution` on `CadRasterizationOptions`.  
- **File not found error** – Ensure `MyDir` points to a valid directory and the DXF file name matches exactly.

## Frequently Asked Questions

### Q1: Can I use Aspose.CAD with other .NET libraries?
A1: Yes, Aspose.CAD seamlessly integrates with other .NET libraries, providing enhanced capabilities for CAD manipulation.

### Q2: Is a free trial available for Aspose.CAD?
A2: Yes, you can explore the features of Aspose.CAD with a free trial. Visit [here](https://releases.aspose.com/) to get started.

### Q3: How can I get support for Aspose.CAD?
A3: For support and discussions, visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19).

### Q4: Where can I find comprehensive documentation for Aspose.CAD?
A4: Refer to the [Aspose.CAD documentation](https://reference.aspose.com/cad/net/) for detailed information and examples.

### Q5: How do I purchase Aspose.CAD for .NET?
A5: To purchase Aspose.CAD, visit the [purchase page](https://purchase.aspose.com/buy).

**Additional Q&A**

**Q: Can I export a multi‑page CAD drawing to a single PDF?**  
A: Yes. Set `PageCount` in `CadRasterizationOptions` and the library will concatenate pages into one PDF.

**Q: Does the canvas size affect vector data quality?**  
A: Vector data remains resolution‑independent; the canvas size only influences rasterized elements and image resolution.

---

**Last Updated:** 2026-03-29  
**Tested With:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}