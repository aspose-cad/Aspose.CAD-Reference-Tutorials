---
title: Create PDF from DWG and Export DGN as Part of DWG – Aspose.CAD for .NET
linktitle: Export DGN as Part of DWG
second_title: Aspose.CAD .NET - CAD and BIM File Format
description: Learn how to create PDF from DWG and export DGN as part of DWG using Aspose.CAD for .NET. This guide also shows how to convert DWG to PDF and set PDF options.
weight: 11
url: /net/cad-export-formats/export-dgn-as-part-of-dwg/
date: 2026-03-21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Create PDF from DWG and Export DGN as Part of DWG – Aspose.CAD for .NET

## Introduction

If you need to **create PDF from DWG** files while also embedding a DGN design as part of the DWG, Aspose.CAD for .NET makes it straightforward. In this tutorial we’ll walk through the entire workflow: loading a DWG, locating the embedded DGN underlay, configuring rasterization options, and finally exporting the result to a PDF document. Whether you’re building a batch conversion tool, a reporting engine, or a CAD‑BIM integration service, the steps below will give you a solid, production‑ready foundation.

## Quick Answers
- **What library handles DWG → PDF conversion?** Aspose.CAD for .NET  
- **Can I export a DGN underlay while creating the PDF?** Yes – the underlay is accessed via `CadDgnUnderlay`.  
- **Which method sets PDF options?** `PdfOptions` together with `CadRasterizationOptions`.  
- **Do I need a license for commercial use?** Yes, a valid Aspose.CAD license is required.  
- **Supported .NET versions?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## What is “create PDF from DWG”?

Creating a PDF from a DWG file means rendering the vector drawing into a raster or vector‑based PDF document. This process is useful for sharing drawings with stakeholders who don’t have CAD software, archiving, or generating printable reports. Aspose.CAD simplifies the task by handling the heavy lifting of parsing DWG entities and providing fine‑grained control over the output through `PdfOptions`.

## Why export DGN as part of a DWG?

A DGN underlay often represents reference geometry from MicroStation projects. By exporting the DGN together with the DWG you preserve the original design context, ensuring that downstream consumers see the complete drawing set. This is especially valuable in multidisciplinary projects where both DWG and DGN files coexist.

## Prerequisites

- **Aspose.CAD for .NET** – download it [here](https://releases.aspose.com/cad/net/).  
- **Development Environment** – Visual Studio (any recent version) or your preferred .NET IDE.  
- **Basic C# knowledge** – you should be comfortable with C# syntax and .NET project structure.

## Import Namespaces

Add the required `using` directives at the top of your C# source file:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Step‑by‑Step Guide

### Step 1: Define File Paths

Set the input DWG file and the output PDF name.

```csharp
// Input and Output file paths
string fileName = "BlockRefDgn.dwg";
string outPath = fileName + ".pdf";
```

### Step 2: Create `PdfOptions` Instance (set pdf options)

`PdfOptions` lets you control how the PDF is generated, such as page size, compression, and metadata.

```csharp
// Create an instance of PdfOptions class for exporting DWG to PDF
PdfOptions exportOptions = new PdfOptions();
```

### Step 3: Load the DWG File

Load the DWG as a `CadImage` so you can inspect its entities.

```csharp
// Load the existing DWG file as an image and convert it to CadImage type
using (CadImage cadImage = (CadImage)Image.Load(fileName))
```

### Step 4: Iterate Through Entities

Walk through every entity in the drawing to locate the DGN underlay.

```csharp
// Iterate through each entity inside the DWG file
foreach (CadBaseEntity baseEntity in cadImage.Entities)
```

### Step 5: Check Entity Type (how to export dgn)

Identify whether the current entity is a DGN underlay.

```csharp
// Check if the entity is an image definition
if (baseEntity.TypeName == CadEntityTypeName.DGNUNDERLAY)
```

### Step 6: Get Underlay Path

Retrieve the external reference path of the DGN file.

```csharp
// If it's an image definition, get the external reference to the object
CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
Console.WriteLine(dgnFile.UnderlayPath);
```

### Step 7: Define Rasterization Options (convert dwg to pdf)

Configure how the DWG is rasterized before being placed into the PDF.

```csharp
// Define settings for CadRasterizationOptions object
exportOptions.VectorRasterizationOptions = new CadRasterizationOptions()
{
    PageWidth = 1600,
    PageHeight = 1600,
    Layouts = new string[] { "Model" },
    AutomaticLayoutsScaling = false,
    NoScaling = true,
    BackgroundColor = Color.Black,
    DrawType = CadDrawTypeMode.UseObjectColor
};
```

### Step 8: Export DWG to PDF

Finally, save the rendered image as a PDF file.

```csharp
// Export the DWG to PDF by calling Save method
cadImage.Save(outPath, exportOptions);
```

## Common Issues and Solutions

| Issue | Reason | Fix |
|-------|--------|-----|
| **`Image.Load` throws “File not found”** | Incorrect path or missing file. | Use an absolute path or ensure the DWG is copied to the output folder. |
| **Underlay path is empty** | DGN underlay not embedded or reference broken. | Verify the DWG actually contains a DGN underlay and that the external DGN file is accessible. |
| **PDF output is blank** | Rasterization options set to zero size. | Adjust `PageWidth`/`PageHeight` or set `NoScaling = false`. |
| **License exception** | Running without a valid Aspose.CAD license. | Apply the license before loading the image: `License lic = new License(); lic.SetLicense("Aspose.CAD.lic");` |

## Frequently Asked Questions

### Q1: Can I use Aspose.CAD for .NET in my commercial projects?
A1: Yes, you can. Visit [here](https://purchase.aspose.com/buy) to explore licensing options.

### Q2: Are there any limitations on the size of DWG files I can process?
A2: Aspose.CAD supports handling large DWG files, but hardware limitations may apply.

### Q3: Is there a trial version available?
A3: Yes, you can get a free trial [here](https://releases.aspose.com/).

### Q4: How can I get temporary licenses?
A4: Temporary licenses can be obtained [here](https://purchase.aspose.com/temporary-license/).

### Q5: Where can I seek assistance if I encounter issues?
A5: You can visit the Aspose.CAD forum [here](https://forum.aspose.com/c/cad/19) for support.

**Q: How do I set additional PDF metadata (author, title, etc.)?**  
A: Use `exportOptions.Metadata` properties before calling `Save`.

**Q: Can I export multiple layouts into separate PDF pages?**  
A: Yes – set `Layouts = new string[] { "Layout1", "Layout2" }` in `CadRasterizationOptions`.

**Q: Does Aspose.CAD support converting DWG to other image formats?**  
A: Absolutely. You can export to PNG, JPEG, SVG, and more by using the corresponding `Image.Save` overloads.

---

**Last Updated:** 2026-03-21  
**Tested With:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}