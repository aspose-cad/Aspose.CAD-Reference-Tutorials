---
title: "Set PDF Page Size – Convert CAD to PDF (Java)"
linktitle: "Set PDF Page Size – Convert CAD to PDF"
second_title: "Aspose.CAD Java API"
description: "Learn how to set PDF page size and convert CAD to PDF using Aspose.CAD for Java, with automatic layout scaling and TIFF export."
weight: 16
url: /java/advanced-cad-features/set-canvas-size-and-mode/
date: 2026-02-15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Set Canvas Size and Mode

## Introduction

If you need to **set PDF page size** while converting CAD drawings to PDF, you’ve come to the right place. In this tutorial we’ll show you how to use Aspose.CAD for Java to define exact canvas dimensions, enable automatic layout scaling, and then export the result to both PDF and TIFF. Whether you’re preparing engineering schematics for print or generating thumbnails for a web gallery, controlling the page size and output resolution is essential.

## Quick Answers
- **What does “convert CAD to PDF” mean?** Transforming a CAD drawing (e.g., DXF, DWG) into a PDF document that can be viewed on any platform.  
- **Can I also export to TIFF?** Yes—use `TiffOptions` to create high‑resolution raster images.  
- **Which option controls canvas size in Java?** `CadRasterizationOptions.setPageWidth/Height`.  
- **What is automatic layout scaling?** A flag (`setAutomaticLayoutsScaling(true)`) that preserves the original layout proportions when the canvas size changes.  
- **Do I need a license for Aspose.CAD?** A temporary or permanent license is required for production use.

## How to Set PDF Page Size When Converting CAD to PDF (Java)

Setting the PDF page size (or canvas size) lets you dictate the final dimensions of the document, which is especially useful when you must **change PDF dimensions** to match printing standards or UI requirements. Below we walk through each step, explaining the *why* behind every line of code.

## What is **convert CAD to PDF**?

Converting CAD to PDF means taking vector‑based engineering drawings and rendering them as PDF pages, preserving line work, layers, and geometry while making the file universally accessible.

## Why set canvas size **java**?

Setting the canvas size in Java lets you define the output resolution and page dimensions, ensuring that the resulting PDF or TIFF matches your printing or display requirements. It also gives you control over scaling behavior, which is essential for large‑format drawings.

## Prerequisites

Before diving into the tutorial, make sure you have the following prerequisites in place:

- Aspose.CAD for Java: Ensure that you have the Aspose.CAD library installed in your Java environment. You can download it [here](https://releases.aspose.com/cad/java/).
- Document Directory: Set up a document directory to store your CAD files. This directory will be referenced in the tutorial steps.

Now, let's get started with the step‑by‑step guide.

## Import Namespaces

In this step, we'll import the necessary namespaces to kickstart your Aspose.CAD project.

```java
import java.awt.Image;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## Step 1: Import Aspose.CAD Classes

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
com.aspose.cad.Image objImage = com.aspose.cad.Image.load(srcFile);
```

In this snippet, we set up the path to the resource directory and load a DXF file using Aspose.CAD's `Image` class.

## Step 2: Set **CadRasterizationOptions** Properties (set canvas size java)

```java
// Create an instance of CadRasterizationOptions and set its various properties
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

Here, we create an instance of `CadRasterizationOptions` and configure properties such as page width, page height, and **automatic layout scaling**. This is the core of **configure canvas mode** for your conversion.

## Step 3: Create PdfOptions and Set VectorRasterizationOptions

```java
// Create an instance of PdfOptions
PdfOptions pdfOptions = new PdfOptions();

// Set the VectorRasterizationOptions property
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Now, we create a `PdfOptions` instance and set its `VectorRasterizationOptions` property to the previously configured `CadRasterizationOptions`.

## Step 4: Export to PDF (convert cad to pdf)

```java
// Export CAD to PDF
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

Finally, we save the CAD image to a PDF file using the specified options, completing the **convert CAD to PDF** process.

## Step 5: Create TiffOptions and Set VectorRasterizationOptions (export cad to tiff)

```java
// Create an instance of TiffOptions
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);

// Set the VectorRasterizationOptions property
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
```

In this step, we set up a `TiffOptions` instance and configure its `VectorRasterizationOptions` property.

## Step 6: Export to TIFF

```java
// Export CAD to TIFF
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

Finally, we save the CAD image to a TIFF file using the specified options, demonstrating how to **export CAD to TIFF** after configuring canvas size.

## Common Issues and Solutions

| Issue | Cause | Fix |
|-------|-------|-----|
| Output PDF is blank | `setNoScaling(true)` disables rendering for some drawings | Remove `setNoScaling(true)` or set it to `false`. |
| TIFF resolution looks low | Page width/height too small | Increase `setPageWidth` / `setPageHeight` values. |
| Layout looks distorted | Automatic layout scaling disabled | Ensure `setAutomaticLayoutsScaling(true)` is enabled. |

## Why Adjust Canvas Size and DPI?

Changing the canvas size directly influences the rasterization resolution of the output. If you need to **increase TIFF resolution**, simply raise the `setPageWidth` / `setPageHeight` values or call `rasterizationOptions.setResolution(300)` before creating the `TiffOptions`. This gives you high‑quality raster images suitable for print or detailed inspection.

## Frequently Asked Questions

### Q1: Can I use Aspose.CAD for Java with other Java frameworks?

A1: Yes, Aspose.CAD is designed to seamlessly integrate with various Java frameworks.

### Q2: Is a temporary license available for Aspose.CAD?

A2: Yes, you can obtain a temporary license [here](https://purchase.aspose.com/temporary-license/).

### Q3: Where can I get community support for Aspose.CAD?

A3: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for community support and discussions.

### Q4: Can I try Aspose.CAD for free?

A4: Absolutely! Get a free trial [here](https://releases.aspose.com/).

### Q5: How do I purchase Aspose.CAD for Java?

A5: Purchase the product [here](https://purchase.aspose.com/buy).

**Additional Q&A**

**Q: Does the canvas size affect vector quality in the PDF?**  
A: No. Canvas size controls page dimensions; vector data remains resolution‑independent, ensuring crisp rendering at any zoom level.

**Q: Can I set a different DPI for the TIFF output?**  
A: Yes. Adjust `rasterizationOptions.setResolution(dpiValue)` before creating `TiffOptions`.

**Q: How can I **change PDF dimensions** for an existing PDF without re‑rendering the CAD?**  
A: Use Aspose.PDF to load the generated PDF and call `pdf.getPages().setPageSize(PageSize.A4)` or a custom size.

**Q: What is the best way to **convert dxf to pdf** while preserving layers?**  
A: Keep `setAutomaticLayoutsScaling(true)` and avoid `setNoScaling(true)`; this retains layer visibility and layout fidelity.

## Conclusion

Congratulations! You've successfully **convert CAD to PDF** and **export CAD to TIFF** while **set canvas size java**, enabling **automatic layout scaling**, and learning how to **configure canvas mode** for high‑quality outputs. This tutorial provides a solid foundation for your CAD conversion projects. Explore more features and possibilities in the [Aspose.CAD documentation](https://reference.aspose.com/cad/java/).

---

**Last Updated:** 2026-02-15  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}