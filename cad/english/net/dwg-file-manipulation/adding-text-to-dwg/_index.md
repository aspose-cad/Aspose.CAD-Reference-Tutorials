---
title: Convert DWG to PDF and Add Text in C# – Aspose.CAD Tutorial
linktitle: Adding Text to DWG Files in C#
second_title: Aspose.CAD .NET - CAD and BIM File Format
description: Learn how to convert DWG to PDF and add custom text using C# and Aspose.CAD. This step‑by‑step guide covers generating PDF from DWG, inserting a text entity, and changing DWG text font.
weight: 14
url: /net/dwg-file-manipulation/adding-text-to-dwg/
date: 2026-04-06
keywords:
- convert dwg to pdf
- generate pdf from dwg
- insert text entity
- change dwg text font
- aspose cad dwg pdf
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Convert DWG to PDF and Add Text in C# – Aspose.CAD Tutorial

## Introduction

In the fast‑moving world of CAD and .NET development, **converting DWG to PDF** while inserting custom annotations is a frequent requirement. Whether you need to generate printable drawings for clients or embed dynamic notes directly into a DWG, Aspose.CAD makes the job straightforward. In this tutorial you’ll learn how to **convert DWG to PDF**, **add a text entity**, and even **change DWG text font** using C#.

## Quick Answers
- **What library is best for DWG‑to‑PDF conversion?** Aspose.CAD for .NET  
- **Can I add custom text while converting?** Yes – create a `CadText` entity and add it before saving.  
- **Do I need a license for production use?** A commercial license is required; a free trial is available.  
- **Which .NET versions are supported?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Is it possible to change the text font?** Yes, adjust the `CadText` properties such as `StyleType` and `TextHeight`.

## What is “convert dwg to pdf”?

Converting a DWG file to PDF transforms a vector‑based CAD drawing into a widely shareable, device‑independent document. The PDF retains the original geometry and layers, while allowing you to embed annotations, text, or other metadata. Aspose.CAD handles the rasterization and vector rendering automatically, so you don’t need any third‑party CAD software on the server.

## Why add text to a DWG before conversion?

Embedding text directly into the DWG gives you full control over placement, styling, and layer assignment. When the file is later converted to PDF, the text appears exactly where you positioned it, preserving design intent and eliminating the need for post‑processing in a PDF editor.

## Prerequisites

Before we start, make sure you have:

- **Aspose.CAD Library** – download it from the [download link](https://releases.aspose.com/cad/net/).  
- **A working .NET environment** (Visual Studio 2022, .NET 6, or any compatible version).  
- **A folder for your test files** – we’ll refer to it as `MyDir` throughout the guide.

Now, let’s walk through the process step by step.

## Import Namespaces

Add the required `using` statements so you can access Aspose.CAD classes.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects.AttEntities;
using Aspose.CAD.ImageOptions;
```

## Step 1: Load the DWG File

Load your source DWG file into an `Image` object. This object gives you access to the underlying CAD entities.

```csharp
string dwgPathToFile = MyDir + "SimpleEntites.dwg";
using (Image image = Image.Load(dwgPathToFile))
{
    // Subsequent steps will be performed inside this block
}
```

## Step 2: Create a CadText Object (Insert Text Entity)

The `CadText` class represents a single line of text in a DWG. Here we set its style, value, color, layer, and position. Adjust `StyleType` or `TextHeight` to **change DWG text font**.

```csharp
CadText cadText = new CadText();
cadText.StyleType = "Standard";          // Font/style – change to alter DWG text font
cadText.DefaultValue = "Some custom text";
cadText.ColorId = 256;                    // 256 = ByLayer (you can use a specific ACI color)
cadText.LayerName = "0";
cadText.FirstAlignment.X = 47.90;
cadText.FirstAlignment.Y = 5.56;
cadText.TextHeight = 0.8;                 // Height influences visual size
cadText.ScaleX = 0.0;
```

## Step 3: Add the Text Entity to the Model Space

The DWG model space holds most drawing entities. By adding our `CadText` to the `*Model_Space` block, the text becomes part of the drawing.

```csharp
CadImage cadImage = (CadImage)image;
cadImage.BlockEntities["*Model_Space"].AddEntity(cadText);
```

## Step 4: Configure PDF Options (Generate PDF from DWG)

Set up rasterization options that control how the DWG is rendered into a PDF. You can tweak page size, draw type, and layout.

```csharp
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.VectorRasterizationOptions = cadRasterizationOptions;
cadRasterizationOptions.DrawType = CadDrawTypeMode.UseObjectColor;
cadRasterizationOptions.PageHeight = 1600;
cadRasterizationOptions.PageWidth = 1600;
cadRasterizationOptions.Layouts = new string[] { "Model" };
```

## Step 5: Save the Modified DWG as a PDF

Finally, export the modified drawing. The resulting PDF includes the newly inserted text.

```csharp
image.Save(MyDir + "SimpleEntites_generated.pdf", pdfOptions);
```

> **Pro tip:** If you need a higher‑resolution PDF, increase `PageHeight` and `PageWidth` proportionally.

## Common Issues & Solutions

| Issue | Reason | Fix |
|-------|--------|-----|
| Text does not appear in the PDF | Wrong layer or color ID | Ensure `LayerName` exists and `ColorId` is set to a visible color (e.g., 7 for white). |
| Text is misplaced | Incorrect alignment coordinates | Verify `FirstAlignment.X/Y` values relative to the drawing’s units. |
| PDF is blank | Rasterization options not set | Set `DrawType` to `UseObjectColor` or `UseObjectLineWeight`. |

## Frequently Asked Questions (Existing)

### Q1: Is Aspose.CAD compatible with all versions of DWG files?

A1: Aspose.CAD supports a wide range of DWG file versions, ensuring compatibility with various CAD software.

### Q2: Can I add multiple text entities to a single DWG file using Aspose.CAD?

A2: Yes, you can add multiple text entities to a DWG file by repeating the process outlined in the tutorial.

### Q3: How can I change the text font and style in Aspose.CAD?

A3: To modify text font and style, adjust the properties of the `CadText` object before adding it to the DWG file.

### Q4: Are there any licensing considerations for using Aspose.CAD in a commercial project?

A5: Yes, ensure compliance with Aspose.CAD licensing terms. Refer to [Aspose.CAD Purchase](https://purchase.aspose.com/buy) for details.

### Q5: Where can I seek help or discuss Aspose.CAD-related queries?

A5: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) to connect with the community and get support.

## Additional FAQs

**Q: How do I generate PDF from DWG without adding text?**  
A: Skip the `CadText` creation step and directly configure `PdfOptions` before calling `image.Save(...)`.

**Q: Can I change the text color programmatically?**  
A: Yes, set `cadText.ColorId` to a specific ACI color number (e.g., 1 for red).

**Q: Is it possible to insert multiline text?**  
A: Use `CadMText` for multiline text blocks; the approach is similar to `CadText`.

**Q: Does Aspose.CAD support batch conversion of multiple DWG files?**  
A: Absolutely – loop through a directory of DWG files, apply the same steps, and save each as PDF.

## Conclusion

You now have a complete, production‑ready workflow to **convert DWG to PDF**, **add custom text**, and **customize text appearance** using C# and Aspose.CAD. This technique is ideal for automated drawing generation, reporting pipelines, or any scenario where you need to enrich CAD files on the fly.

---

**Last Updated:** 2026-04-06  
**Tested With:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}