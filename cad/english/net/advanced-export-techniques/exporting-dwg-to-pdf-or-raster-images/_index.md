---
title: How to convert DWG to PDF and Raster Images using Aspose.CAD for .NET
linktitle: Exporting DWG to PDF or Raster Images
second_title: Aspose.CAD .NET - CAD and BIM File Format
description: Learn how to convert DWG to PDF or raster images with Aspose.CAD for .NET. This step‑by‑step cad to pdf tutorial covers exporting DWG to image formats like PNG and shows how to export DWG to image files efficiently.
weight: 11
url: /net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/
date: 2026-03-16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exporting DWG to PDF or Raster Images - Aspose.CAD Guide

## Introduction

If you need to **convert DWG to PDF** (or to raster formats such as PNG) directly from a .NET application, you’re in the right place. In this tutorial we’ll walk through the exact steps required to use Aspose.CAD for .NET to perform the conversion, explain why the library is a solid choice, and show you how to handle both PDF and image output with just a few lines of code.

## Quick Answers
- **What library handles DWG conversion?** Aspose.CAD for .NET  
- **Can I export DWG to PNG as well as PDF?** Yes – the same rasterization options work for both formats.  
- **Do I need a license for development?** A free trial works for testing; a commercial license is required for production.  
- **Which .NET versions are supported?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Is unit conversion handled automatically?** You can define the unit system manually (metric or imperial) as shown in the code.

## What is “convert DWG to PDF”?
Converting DWG to PDF means taking a CAD drawing (DWG) and rendering it into a portable, view‑only document (PDF). This is useful for sharing designs with stakeholders who don’t have CAD software, creating printable documentation, or archiving drawings in a universally readable format.

## Why use Aspose.CAD for this conversion?
- **No external dependencies** – the library works entirely in managed code.  
- **High fidelity** – retains layers, line weights, and layout information.  
- **Built‑in raster options** – lets you export to PNG, JPEG, BMP, etc., with a single configuration object.  
- **Cross‑platform** – works on Windows, Linux, and macOS with .NET Core.

## Prerequisites

Before we dive into the tutorial, make sure you have the following in place:

- A basic understanding of .NET programming.  
- Aspose.CAD for .NET library installed. If not, download it [here](https://releases.aspose.com/cad/net/).  
- Your favorite integrated development environment (IDE) set up for .NET development.

## Import Namespaces

Let's kick things off by importing the necessary namespaces in your .NET project. This ensures that you have access to the Aspose.CAD functionality in your code.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
```

## Step 1: Load DWG File

Begin by loading the DWG file you wish to convert. Replace `"Your Document Directory"` with the path to your DWG file.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Your code for loading DWG goes here
}
```

## Step 2: Set up PDF Export (How to export DWG to PDF)

Now, let's configure the PDF export settings. This example demonstrates how to set the layout and handle unit conversions.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new string[] { "Model" };

// Check and define the unit system
bool currentUnitIsMetric = false;
double currentUnitCoefficient = 1.0;
DefineUnitSystem(cadImage.UnitType, out currentUnitIsMetric, out currentUnitCoefficient);

// Your code for setting up PDF export goes here
```

## Step 3: Export to PDF

Execute the export to PDF using the configured settings.

```csharp
PdfOptions pdfOptions = new PdfOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath, pdfOptions);
```

## Step 4: Export to Raster Images (export dwg to image)

Extend the functionality to export to raster images, such as PNG.

```csharp
// A4 size at 300 DPI - 2480 x 3508
rasterizationOptions.PageHeight = 3508;
rasterizationOptions.PageWidth = 2480;

PngOptions pngOptions = new PngOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath.Replace("pdf", "png"), pngOptions);
```

## Common Issues and Solutions

| Issue | Why it Happens | How to Fix |
|-------|----------------|------------|
| **Blank pages in PDF** | Layout not specified correctly | Ensure `rasterizationOptions.Layouts` includes the correct layout name (e.g., `"Model"`). |
| **Incorrect dimensions** | DPI or page size mismatch | Adjust `PageHeight`, `PageWidth`, and DPI values in `CadRasterizationOptions`. |
| **Units appear wrong** | Unit conversion not defined | Use `DefineUnitSystem` to set `currentUnitIsMetric` and `currentUnitCoefficient` based on `cadImage.UnitType`. |
| **License exception** | Trial version limits | Apply a temporary or permanent license before calling `Image.Load`. |

## Frequently Asked Questions

### Q1: Can I use Aspose.CAD for .NET in my commercial projects?
A1: Yes, you can. Visit [purchase.aspose.com/buy](https://purchase.aspose.com/buy) for licensing details.

### Q2: Is there a free trial available?
A2: Certainly! Grab your free trial [here](https://releases.aspose.com/).

### Q3: How can I get support for Aspose.CAD for .NET?
A3: Head over to the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for community support.

### Q4: Can I obtain a temporary license for testing purposes?
A4: Yes, you can get a temporary license [here](https://purchase.aspose.com/temporary-license/).

### Q5: Where can I find the detailed documentation?
A5: The documentation is available at [Aspose.CAD](https://reference.aspose.com/cad/net/).

### Q6: How do I **save CAD as PNG** with high quality?
A6: Set `PageHeight` and `PageWidth` to the desired pixel dimensions and choose a DPI of 300 or higher in `CadRasterizationOptions`.

### Q7: What is the best way to **how to convert dwg** when the source file contains multiple layouts?
A7: Populate `rasterizationOptions.Layouts` with all layout names you want to export, then loop through each layout and call `Save` for each output format.

---

**Last Updated:** 2026-03-16  
**Tested With:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}