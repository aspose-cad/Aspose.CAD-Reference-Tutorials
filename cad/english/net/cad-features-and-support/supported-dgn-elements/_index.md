---
title: Convert DGN to PNG with Aspose.CAD for .NET
linktitle: Supported DGN Elements
second_title: Aspose.CAD .NET - CAD and BIM File Format
description: Learn how to convert DGN to PNG using Aspose.CAD for .NET. This guide also covers CAD file format support and the full set of supported DGN elements.
weight: 18
url: /net/cad-features-and-support/supported-dgn-elements/
date: 2026-03-29
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Convert DGN to PNG with Aspose.CAD for .NET

## Introduction

Are you a .NET developer looking to **convert DGN to PNG** seamlessly? Aspose.CAD for .NET provides a robust solution to handle DGN files efficiently. In this tutorial, we will delve into the supported DGN elements, guiding you through the process of working with Aspose.CAD for .NET while showing you exactly how to export those elements to PNG images.

## Quick Answers
- **What does Aspose.CAD do?** It reads, modifies, and converts CAD/BIM files (including DGN) to raster formats such as PNG.  
- **Can I convert 2D and 3D DGN elements?** Yes – both 2‑D and 3‑D entities are supported.  
- **Which .NET versions are required?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Do I need a license for testing?** A free trial is available; a license is required for production.  
- **Where do I get the library?** Download it from the official Aspose site (link below).

## What is “convert DGN to PNG”?
Converting DGN to PNG means rendering the vector‑based DGN drawing (2‑D or 3‑D) into a raster image format (PNG). This is useful when you need to display CAD drawings on the web, embed them in reports, or generate thumbnails without requiring a CAD viewer.

## Why use Aspose.CAD for .NET for CAD file format support?
- **Full CAD file format support** – DGN, DWG, DXF, DWF, and more.  
- **No external dependencies** – pure .NET library, no native CAD installations.  
- **High‑fidelity rendering** – preserves line weights, colors, and 3‑D geometry.  
- **Batch processing** – easily loop through many files in a server‑side application.

## Prerequisites

Before we begin, make sure you have the following:

- Basic knowledge of .NET programming.  
- Visual Studio installed on your machine.  
- Aspose.CAD for .NET library, which you can download [here](https://releases.aspose.com/cad/net/).

## Import Namespaces

To kickstart your project, import the necessary namespaces into your .NET application. This step ensures that you have access to the functionalities provided by Aspose.CAD for .NET.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Dgn;
using Aspose.CAD.FileFormats.Dgn.DgnElements;
```

## How to Convert DGN to PNG

Below is a step‑by‑step guide that walks you through loading a DGN file, iterating its elements, handling both 2‑D and 3‑D entities, and finally exporting the result to a PNG raster image.

### Step 1: Load the DGN File

Begin by loading an existing DGN file as a `DgnImage` in your .NET application.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Your code here
}
```

### Step 2: Iterate Through DGN Elements

Iterate through the DGN elements using a `foreach` loop. Aspose.CAD for .NET provides a variety of DGN element types that you can work with.

```csharp
foreach (DgnDrawingElementBase element in dgnImage.Elements)
{
    // Your code here
}
```

### Step 3: Handle Previously Supported 2‑D Entities

These entities are now also supported for 3‑D rendering. The switch statement lets you branch logic based on the element type.

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.Line:
    case DgnElementType.Ellipse:
    case DgnElementType.Curve:
    // Additional cases
        {
            // Your code here
            break;
        }
}
```

### Step 4: Handle Supported 3‑D Entities

Aspose.CAD adds full support for several 3‑D DGN elements. Extend the switch to process them as needed.

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.SolidHeader3D:
    case DgnElementType.Cone:
    case DgnElementType.CellHeader:
        {
            // Your code here
            break;
        }
}
```

### Step 5: Export and Save as PNG

After any required manipulation, export the DGN drawing to a PNG raster image and save it to the specified directory.

```csharp
Console.WriteLine("\nThe DGN file exported successfully to raster image.\nFile saved at " + MyDir);
```

> **Pro tip:** Use `Image.Save` with `new PngOptions()` to control resolution, background color, and other PNG‑specific settings.

## CAD File Format Support Overview

Aspose.CAD for .NET isn’t limited to DGN. It also supports DWG, DXF, DWF, and many other CAD formats, giving you a single API to handle a broad spectrum of engineering drawings. This makes it ideal for projects that require **CAD file format support** across multiple standards.

## Common Issues & Solutions

| Issue | Reason | Fix |
|-------|--------|-----|
| **Image appears blank** | Exported with zero DPI | Specify `ResolutionX` and `ResolutionY` in `PngOptions`. |
| **Missing 3‑D geometry** | Element type not handled in switch | Add the missing `DgnElementType` case and render accordingly. |
| **Out‑of‑memory on large files** | Loading whole file at once | Process elements in batches or use streaming where possible. |

## Frequently Asked Questions

### Q1: Where can I find the documentation for Aspose.CAD for .NET?
A1: You can find the documentation [here](https://reference.aspose.com/cad/net/).

### Q2: How do I download Aspose.CAD for .NET?
A2: You can download the library [here](https://releases.aspose.com/cad/net/).

### Q3: Is there a free trial available for Aspose.CAD for .NET?
A3: Yes, you can access the free trial [here](https://releases.aspose.com/).

### Q4: Where can I get temporary licenses for Aspose.CAD for .NET?
A4: Temporary licenses are available [here](https://purchase.aspose.com/temporary-license/).

### Q5: Need help or have questions?
A5: Visit the Aspose.CAD for .NET community [support forum](https://forum.aspose.com/c/cad/19).

---

**Last Updated:** 2026-03-29  
**Tested With:** Aspose.CAD for .NET 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}