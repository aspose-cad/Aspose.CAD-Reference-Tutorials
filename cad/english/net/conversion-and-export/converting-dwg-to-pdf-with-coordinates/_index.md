---
title: How to Set Viewport while Converting DWG to PDF with Coordinates in C# - Aspose.CAD Tutorial
linktitle: Converting DWG to PDF with Coordinates in C#
second_title: Aspose.CAD .NET - CAD and BIM File Format
description: Learn how to set viewport and convert DWG to PDF in C# using Aspose.CAD. This dwg to pdf tutorial shows precise export with coordinates.
date: 2026-04-03
keywords:
- how to set viewport
- dwg to pdf tutorial
- convert dwg to pdf c#
weight: 11
url: /net/conversion-and-export/converting-dwg-to-pdf-with-coordinates/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Converting DWG to PDF with Coordinates in C# - Aspose.CAD Tutorial

## Introduction

Welcome to this comprehensive tutorial on **how to set viewport** while converting DWG files to PDF with specified coordinates using Aspose.CAD for .NET. By controlling the viewport you get pixel‑perfect PDFs that match exactly the area you need—perfect for construction drawings, floor‑plan previews, or any BIM workflow.

## Quick Answers
- **What does “set viewport” mean?** It defines the visible region and scaling of the CAD drawing during rasterization.  
- **Which library handles the conversion?** Aspose.CAD for .NET.  
- **Do I need a license?** A free trial works for evaluation; a commercial license is required for production.  
- **Supported platforms?** Windows, Linux, and macOS with .NET 5/6/7 or .NET Framework 4.6+.  
- **Typical implementation time?** About 10‑15 minutes for a basic conversion.

## Prerequisites

Before we begin, make sure you have the following prerequisites:

- **Aspose.CAD Library** – Download and install the Aspose.CAD library for .NET. You can find the library [here](https://releases.aspose.com/cad/net/).
- **Development Environment** – Visual Studio, Rider, or any IDE that supports .NET development.
- **DWG File** – Have a DWG file ready for conversion. You can use the provided example file or your custom DWG file.

## How to Set Viewport for Precise PDF Export

Setting the viewport is the core step that lets you define the exact area of the drawing you want to render. In the code below we create a new `CadVportTableObject`, position it with the top‑left coordinate, and calculate width, height, and aspect ratio. This is the **how to set viewport** implementation that drives the rest of the conversion.

## Import Namespaces

In your C# project, import the necessary namespaces:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadParameters;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.ImageOptions;
```

Let's break down the code into a step‑by‑step guide for a better understanding:

## Step 1: Define the Document Directory

```csharp
string MyDir = "Your Document Directory";
```

## Step 2: Set the Source DWG File Path

```csharp
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";
```

## Step 3: Load DWG File and Configure Rasterization Options

```csharp
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
    rasterizationOptions.Layouts = new string[] { "Model" };
    rasterizationOptions.NoScaling = true;
```

## Step 4: Define Coordinates and Viewport  

Here we actually **set the viewport** (how to set viewport) by specifying the top‑left corner, width, and height of the area you want to export.

```csharp
    Point topLeft = new Point(500, 1000);
    double width = 3108;
    double height = 2489;

    CadVportTableObject newView = new CadVportTableObject();
    newView.Name = new CadStringParameter();
    newView.Name.Init("*Active");
    newView.CenterPoint.X = topLeft.X + width / 2f;
    newView.CenterPoint.Y = topLeft.Y - height / 2f;
    newView.ViewHeight.Value = height;
    newView.ViewAspectRatio.Value = width / height;
```

## Step 5: Apply Viewport Settings

```csharp
    for (int i = 0; i < cadImage.ViewPorts.Count; i++)
    {
        CadVportTableObject currentView = (CadVportTableObject)(cadImage.ViewPorts[i]);
        if (cadImage.ViewPorts.Count == 1 || string.Equals(currentView.Name.Value.ToLowerInvariant(), "*active"))
        {
            cadImage.ViewPorts[i] = newView;
            break;
        }
    }
```

## Step 6: Configure PDF Options and Export  

Now we tie everything together and **convert DWG to PDF** using the rasterization options we just prepared.

```csharp
    Aspose.CAD.ImageOptions.PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions();
    pdfOptions.VectorRasterizationOptions = rasterizationOptions;

    MyDir = MyDir + "ConvertDWGToPDFBySupplyingCoordinates_out.pdf";
    cadImage.Save(MyDir, pdfOptions);
}
```

## Step 7: Display Success Message

```csharp
Console.WriteLine("\nThe DWG file exported successfully to PDF.\nFile saved at " + MyDir);
```

## Common Use Cases

- **Construction documentation** – Generate printable PDFs of specific floor‑plan sections.  
- **BIM coordination** – Export only the area of interest for clash detection.  
- **Client presentations** – Provide a clean PDF of a selected room or elevation without exposing the entire drawing.

## Conclusion

Congratulations! You've successfully **converted DWG to PDF** with precise coordinates and learned **how to set viewport** using Aspose.CAD for .NET. This **dwg to pdf tutorial** demonstrates how to **create pdf from dwg** and **export dwg as pdf c#** while keeping full control over the output area.

## FAQ's

### Q1: Can I use Aspose.CAD with other CAD file formats?

A1: Yes, Aspose.CAD supports various CAD formats, including DWG, DXF, DWF, and more.

### Q2: How can I handle errors during the conversion process?

A2: Implement error handling mechanisms using try‑catch blocks to capture and manage exceptions.

### Q3: Is Aspose.CAD suitable for both Windows and Linux environments?

A3: Yes, Aspose.CAD is compatible with both Windows and Linux platforms.

### Q4: Can I customize the PDF output further?

A4: Certainly! Explore the extensive options provided by Aspose.CAD to tailor the PDF output to your specific requirements.

### Q5: Where can I find additional support or community discussions?

A5: Visit the [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19) for community support and discussions.

## Additional Frequently Asked Questions

**Q: Does this approach work with large DWG files (hundreds of MB)?**  
A: Yes. The rasterization is performed page‑by‑page, and you can adjust `rasterizationOptions` (e.g., `Resolution`) to balance quality and memory usage.

**Q: Can I export multiple viewports into separate PDF pages?**  
A: You can loop through `cadImage.ViewPorts`, set each as active, and call `Save` for each page, then merge PDFs using Aspose.PDF.

**Q: Is it possible to add a watermark to the generated PDF?**  
A: After saving the PDF, you can reopen it with Aspose.PDF and apply a text or image watermark before delivering it to the user.

---

**Last Updated:** 2026-04-03  
**Tested With:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}