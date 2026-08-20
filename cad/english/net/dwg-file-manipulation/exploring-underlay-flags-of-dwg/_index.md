---
title: Convert DWG to Image – Exploring Underlay Flags of DWG Files - Aspose.CAD Tutorial
linktitle: Exploring Underlay Flags of DWG Files
second_title: Aspose.CAD .NET - CAD and BIM File Format
description: Learn how to convert DWG to image and how to read underlay flags using Aspose.CAD for .NET in this step‑by‑step guide.
date: 2026-04-09
weight: 13
url: /net/dwg-file-manipulation/exploring-underlay-flags-of-dwg/
keywords:
- convert dwg to image
- how to read underlay
- Aspose.CAD DWG underlay flags
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exploring Underlay Flags of DWG Files - Aspose.CAD Tutorial

## Introduction

If you're delving into the intricate world of CAD files, specifically DWG files, and you want to **convert DWG to image** while also discovering **how to read underlay** flags, you're in the right place. This tutorial walks you through every step using the powerful Aspose.CAD for .NET library, so you can extract underlay information and render the drawing as an image with confidence.

## Quick Answers
- **What does “convert DWG to image” mean?**  
  It means rendering a DWG drawing into a raster format (PNG, JPEG, etc.) using Aspose.CAD.
- **Which method reveals underlay flags?**  
  Access the `CadUnderlay` object’s `Flags` property after loading the DWG.
- **Do I need a license for Aspose.CAD?**  
  A temporary license is available for evaluation; a full license is required for production.
- **What .NET versions are supported?**  
  .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6 and later.
- **Can I extract underlay geometry?**  
  Yes – the underlay path, insertion point, scale, rotation, and flag states are all accessible.

## What is “convert DWG to image” and why does it matter?

Converting a DWG file to an image lets you display CAD drawings in browsers, embed them in reports, or share them with stakeholders who don’t have a CAD viewer. While rendering, you often need to inspect **underlay** objects (e.g., DGN references) to ensure they appear correctly. Understanding the underlay flags helps you troubleshoot clipping, monochrome rendering, and visibility issues before you generate the final image.

## Prerequisites

- A basic understanding of C# and .NET programming.  
- **Aspose.CAD for .NET** library installed. If you don’t have it yet, download it **[here](https://releases.aspose.com/cad/net/)**.  
- A DWG file for testing – the sample file **“BlockRefDgn.dwg”** is used throughout this guide.

## Import Namespaces

To get started, import the necessary namespaces:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Step 1: Load DWG File and Convert to `CadImage`

First, load the DWG file and cast it to a `CadImage`. This object gives you access to all drawing entities, including underlays.

```csharp
string fileName = MyDir + "BlockRefDgn.dwg";

// Load DWG file and convert to CadImage
using (CadImage image = (CadImage)Image.Load(fileName))
{
    // Your code for subsequent steps will go here
}
```

## Step 2: Iterate Through Entities

Next, loop through every entity in the drawing. This is where you’ll locate underlay objects.

```csharp
foreach (CadBaseEntity entity in image.Entities)
{
    // Your code for subsequent steps will go here
}
```

## Step 3: Check for `CadDgnUnderlay` Type

Identify underlay entities by checking their runtime type. The `CadDgnUnderlay` class represents DGN underlays embedded in a DWG.

```csharp
if (entity is CadDgnUnderlay)
{
    // Your code for subsequent steps will go here
}
```

## Step 4: Access Underlay Flags

Once you have a `CadDgnUnderlay`, cast it to `CadUnderlay` to read its properties and flag states. The flags tell you whether the underlay is visible, clipped, or rendered in monochrome.

```csharp
CadUnderlay underlay = entity as CadUnderlay;

Console.WriteLine(underlay.UnderlayPath);
Console.WriteLine(underlay.UnderlayName);
Console.WriteLine(underlay.InsertionPoint.X);
Console.WriteLine(underlay.InsertionPoint.Y);
Console.WriteLine(underlay.RotationAngle);
Console.WriteLine(underlay.ScaleX);
Console.WriteLine(underlay.ScaleY);
Console.WriteLine(underlay.ScaleZ);
Console.WriteLine((underlay.Flags & UnderlayFlags.UnderlayIsOn) == UnderlayFlags.UnderlayIsOn);
Console.WriteLine((underlay.Flags & UnderlayFlags.ClippingIsOn) == UnderlayFlags.ClippingIsOn);
Console.WriteLine((underlay.Flags & UnderlayFlags.Monochrome) != UnderlayFlags.Monochrome);
```

### What the output tells you

- **UnderlayPath / UnderlayName** – where the external DGN file resides.  
- **InsertionPoint (X, Y)** – coordinates where the underlay is placed in the DWG space.  
- **RotationAngle** – rotation applied to the underlay.  
- **ScaleX / ScaleY / ScaleZ** – scaling factors for each axis.  
- **Flags** – boolean values indicating visibility (`UnderlayIsOn`), clipping (`ClippingIsOn`), and monochrome rendering (`Monochrome`).

## Common Issues & Solutions

| Issue | Reason | Fix |
|-------|--------|-----|
| No output for flag checks | Underlay flags are defaulted to 0 when the underlay is turned off. | Ensure the DWG actually contains an active underlay or toggle visibility in the source CAD file. |
| `Invalid cast` exception | The entity is not a `CadDgnUnderlay`. | Verify the `if (entity is CadDgnUnderlay)` guard before casting. |
| Image rendering fails after flag extraction | Underlay may be clipped or turned off, leading to a blank area. | Adjust the flags (`UnderlayIsOn = true`, `ClippingIsOn = false`) before rendering the final image. |

## Frequently Asked Questions

### Q1: Can I use Aspose.CAD for .NET with other CAD file formats?

A1: Aspose.CAD supports various CAD formats, including DWG, DXF, DGN, and more. Check the documentation for the full list.

### Q2: Is a temporary license available for Aspose.CAD for .NET?

A2: Yes, you can obtain a temporary license **[here](https://purchase.aspose.com/temporary-license/)**.

### Q3: Where can I find support for Aspose.CAD for .NET?

A3: Visit the support forum **[here](https://forum.aspose.com/c/cad/19)** for assistance.

### Q4: How do I buy Aspose.CAD for .NET?

A4: Purchase the library **[here](https://purchase.aspose.com/buy)**.

### Q5: Is there a free trial available?

A5: Yes, you can access the free trial **[here](https://releases.aspose.com/)**.

## Conclusion

Congratulations! You've successfully learned **how to convert DWG to image** while also mastering **how to read underlay** flags using Aspose.CAD for .NET. With this knowledge you can:

- Render DWG drawings as raster images for web or reporting scenarios.  
- Inspect and manipulate underlay properties to ensure correct display.  
- Debug visibility, clipping, and monochrome issues before final image generation.

Feel free to explore other Aspose.CAD features such as layer management, text extraction, and batch conversion to further extend your CAD automation workflows.

---

**Last Updated:** 2026-04-09  
**Tested With:** Aspose.CAD for .NET 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}