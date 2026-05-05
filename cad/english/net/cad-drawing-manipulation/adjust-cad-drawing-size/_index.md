---
title: How to Resize CAD Drawings with Aspose.CAD for .NET
linktitle: Adjusting CAD Drawing Size
second_title: Aspose.CAD .NET - CAD and BIM File Format
description: Learn how to resize CAD drawings in .NET with Aspose.CAD, including how to scale CAD drawing units and adjust layout size. Follow our step‑by‑step guide.
weight: 10
url: /net/cad-drawing-manipulation/adjust-cad-drawing-size/
date: 2026-03-19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# How to Resize CAD Drawings with Aspose.CAD for .NET

## Introduction

If you need to **how to resize CAD** files directly from your .NET application, you’ve come to the right place. In this tutorial we’ll show you how to change CAD unit settings, scale CAD drawing dimensions, and adjust CAD size programmatically using Aspose.CAD for .NET. By the end of the guide you’ll have a solid, production‑ready solution for resizing any supported CAD format.

## Quick Answers
- **What library is required?** Aspose.CAD for .NET  
- **Can I change the unit type?** Yes – set `UnitType` in `CadRasterizationOptions`  
- **Is a license needed for production?** A valid Aspose.CAD license is required for non‑trial use  
- **Which image format does the example export to?** BMP (but any supported raster format works)  
- **How many lines of code?** Less than 30 lines for a complete resize operation  

## What is “how to resize CAD” in practice?
Resizing a CAD drawing means converting the vector data into a raster image at a specific scale or unit (e.g., centimeters, inches). This is useful when you need to embed drawings in reports, generate thumbnails, or integrate CAD visuals into web pages.

## Why adjust CAD size with Aspose.CAD?
- **No external CAD software** – everything runs inside your .NET code.  
- **Fine‑grained control** over units, layouts, and rasterization options.  
- **Cross‑format support** – the same code works for DWG, DXF, DWF, and more.  

## Prerequisites

Before we dive in, make sure you have:

- Aspose.CAD for .NET Library: Download and install the library from the [Aspose.CAD for .NET download page](https://releases.aspose.com/cad/net/).  
- Sample CAD Drawing: A file such as `sample.dwg` placed in your project’s document directory.  

## Import Namespaces

First, import the namespaces that give you access to Aspose.CAD’s classes.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Step 1: Load the CAD Drawing

Load the source file into an `Image` object. This object represents the CAD drawing in memory and will be the basis for all further operations.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "sample.dwg";

// Load a CAD drawing in an instance of Image
using (var image = Aspose.CAD.Image.Load(sourceFilePath))
{
    // Your code here...
}
```

## Step 2: Create BmpOptions (or any other raster format)

`BmpOptions` tells Aspose.CAD how to render the vector data when you save it as a bitmap. You could swap this for `PngOptions`, `JpegOptions`, etc., depending on your target format.

```csharp
Aspose.CAD.ImageOptions.BmpOptions bmpOptions = new Aspose.CAD.ImageOptions.BmpOptions();
```

## Step 3: Set CadRasterizationOptions

`CadRasterizationOptions` holds the core settings for scaling, unit conversion, and layout selection. Linking it to the `VectorRasterizationOptions` property of `BmpOptions` ensures the rasterizer uses your custom settings.

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions cadRasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
bmpOptions.VectorRasterizationOptions = cadRasterizationOptions;
```

## Step 4: Set UnitType (change CAD unit)

Here we change the CAD unit from its default to centimeters. This is where the **change cad unit** keyword lives, and it directly influences the final image size.

```csharp
cadRasterizationOptions.UnitType = Aspose.CAD.ImageOptions.UnitType.Centimeter;
```

## Step 5: Choose Layouts (set CAD layouts)

If your drawing contains multiple layouts (e.g., Model, Sheet1), specify which ones you want to rasterize. Selecting the correct layout is essential when you **set cad layouts** for a resized output.

```csharp
cadRasterizationOptions.Layouts = new string[] { "Model" };
```

## Step 6: Export to BMP (resize CAD drawing)

Finally, save the rasterized image. The output file reflects the new size, unit, and layout you configured—effectively completing the **resize CAD drawing** operation.

```csharp
string outPath = sourceFilePath + ".bmp";
image.Save(outPath, bmpOptions);
```

You now have a BMP file that represents the resized CAD drawing, ready for further processing or display.

## Common Issues and Solutions

| Issue | Why it Happens | Fix |
|-------|----------------|-----|
| Output is blurry | Low DPI (dots per inch) default | Set `cadRasterizationOptions.Resolution = 300;` before saving |
| Wrong layout appears | Layout name typo | Verify the exact layout name using a CAD viewer or the `Layouts` collection |
| Unit conversion looks off | Mixing metric and imperial units | Ensure `UnitType` matches the desired measurement system |

## FAQs

### Q1: Is Aspose.CAD for .NET compatible with all CAD formats?

A1: Aspose.CAD for .NET supports a wide range of CAD formats, including DWG, DXF, DWF, and more. Check the [documentation](https://reference.aspose.com/cad/net/) for the complete list.

### Q2: Can I resize multiple layouts simultaneously?

A2: Yes, you can resize multiple layouts by adjusting the `Layouts` array in the `CadRasterizationOptions`.

### Q3: Where can I get support for Aspose.CAD for .NET?

A3: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for community support and assistance.

### Q4: Is there a free trial available?

A4: Yes, you can explore a [free trial](https://releases.aspose.com/) to evaluate the features of Aspose.CAD for .NET.

### Q5: How can I obtain a temporary license for Aspose.CAD for .NET?

A5: Obtain a temporary license for testing purposes [here](https://purchase.aspose.com/temporary-license/).

## Frequently Asked Questions

**Q: How do I scale a CAD drawing without changing the unit type?**  
A: Adjust the `Zoom` property of `CadRasterizationOptions` (e.g., `cadRasterizationOptions.Zoom = 2.0;`) to double the size while keeping the original unit.

**Q: Can I export to formats other than BMP?**  
A: Absolutely. Replace `BmpOptions` with `PngOptions`, `JpegOptions`, or any other supported raster format class.

**Q: Is it possible to batch‑process a folder of drawings?**  
A: Yes. Loop through the files in a directory, apply the same rasterization logic, and save each output with a unique name.

---

**Last Updated:** 2026-03-19  
**Tested With:** Aspose.CAD for .NET 24.11 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}