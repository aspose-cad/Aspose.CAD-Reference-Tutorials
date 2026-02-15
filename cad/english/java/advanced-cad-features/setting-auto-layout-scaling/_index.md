---
title: Set Custom Page Size – PDF from CAD with Auto Layout Scaling
linktitle: Setting Auto Layout Scaling
second_title: Aspose.CAD Java API
description: Learn how to set custom page size and create PDF from CAD using Aspose.CAD for Java. This step‑by‑step guide covers export CAD to PDF with Auto Layout Scaling.
weight: 17
url: /java/advanced-cad-features/setting-auto-layout-scaling/
date: 2026-02-15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Set Custom Page Size – Create PDF from CAD with Auto Layout Scaling

## Introduction

If you need to **set custom page size** while you **create PDF from CAD** files quickly and with perfect scaling, Aspose.CAD for Java has you covered. Auto Layout Scaling automatically adjusts the layout dimensions so that the resulting PDF looks exactly as intended, regardless of the original CAD page size. In this tutorial we’ll walk through the complete process—from loading a DXF file to exporting a PDF—while highlighting the **export CAD to PDF** capabilities of the library and showing how you can also **convert DWG to PDF** or **increase PDF resolution** when needed.

## Quick Answers
- **What does Auto Layout Scaling do?** It automatically resizes CAD layouts to fit the target page dimensions when rasterizing.
- **Which formats can I convert?** Any format supported by Aspose.CAD (e.g., DXF, DWG, DWF) can be converted to PDF.
- **Do I need a license for production?** Yes, a commercial license is required for non‑evaluation use.
- **How long does the conversion take?** Typically under a second for standard files on modern hardware.
- **Can I change the page size?** Yes, you can set custom page dimensions via `CadRasterizationOptions`.

## What is “create PDF from CAD”?

Creating a PDF from CAD means taking a vector‑based engineering drawing (DXF, DWG, etc.) and rasterizing it into a PDF document. The PDF retains the visual fidelity of the original drawing while being widely viewable on any platform.

## Why use Auto Layout Scaling?

- **Consistent output:** Guarantees that all layouts fill the PDF page without manual size calculations.
- **Time‑saving:** Eliminates the need to manually adjust scaling factors for each drawing.
- **High quality:** Maintains line weight and geometry accuracy during conversion.
- **Flexibility:** Works for **convert dxf to pdf**, **convert dwg to pdf**, and even when you need to **increase PDF resolution** for print‑ready files.

## Prerequisites

1. **Aspose.CAD for Java Library** – download the latest version from the [download page](https://releases.aspose.com/cad/java/).  
2. **Resource Directory** – create a folder on your machine to store CAD files; replace `"Your Document Directory"` in the code with that path.  
3. **Sample CAD File** – for this guide we’ll use `conic_pyramid.dxf`, which is included in the Aspose sample data set.

## Import Namespaces

First, import the required classes. This gives us access to image loading, rasterization, and PDF export features.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## How to Set Custom Page Size for PDF from CAD

Before we dive into the step‑by‑step code, let’s understand why setting a custom page size matters. When you **set custom page size**, you control the physical dimensions of the resulting PDF (e.g., A4, Letter, or a bespoke size). This is essential for engineering workflows where drawings must match sheet standards or when you need to embed the PDF into larger documents.

### Step 1: Load the CAD File

Loading the source file is the first step in **how to export CAD** to a PDF document.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

### Step 2: Create Rasterization Options

Define the target page dimensions. You can also use this block to **set CAD page size** manually if you prefer a custom layout.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
```

### Step 3: Set Auto Layout Scaling

Enable the automatic scaling feature. This is the core of **how to set scaling** for a CAD‑to‑PDF conversion.

```java
rasterizationOptions.setAutomaticLayoutsScaling(true);
```

### Step 4: Create PDF Options

Link the rasterization settings to the PDF export options.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Step 5: Export to PDF

Finally, save the rendered image as a PDF file. This step completes the **convert dxf to pdf** workflow.

```java
image.save(dataDir + "result_out_.pdf", pdfOptions);
```

Repeat the steps above for any additional CAD files you need to process, whether they are **DWG**, **DWF**, or other supported formats.

## Common Use Cases

| Scenario | Why set a custom page size? |
|----------|-----------------------------|
| **Construction drawing submission** | Aligns the PDF with standard A1/A2 sheet sizes required by regulatory bodies. |
| **Embedding in technical manuals** | Guarantees the drawing fits the predefined layout of the manual without extra scaling. |
| **High‑resolution printing** | Allows you to increase DPI (e.g., `rasterizationOptions.setResolution(300)`) while keeping the page dimensions consistent. |

## Common Issues & Troubleshooting

| Symptom | Likely Cause | Fix |
|---------|--------------|-----|
| Blank PDF output | Rasterization options not set or file path incorrect | Verify `srcFile` path and ensure `setPageWidth/Height` are non‑zero |
| Distorted scaling | `setAutomaticLayoutsScaling` left as `false` | Enable automatic scaling or manually calculate scaling factor |
| Missing layers | Source DXF contains unsupported entities | Check the Aspose.CAD release notes for supported entity types |

## Frequently Asked Questions

**Q: Is Aspose.CAD for Java compatible with all CAD file formats?**  
A: Aspose.CAD for Java supports various CAD formats, including DWG, DXF, and DWF.

**Q: Can I customize the scaling options further?**  
A: Yes, the `CadRasterizationOptions` class provides properties for fine‑tuning scaling, DPI, and other rasterization settings.

**Q: Where can I find additional documentation for Aspose.CAD for Java?**  
A: Refer to the [documentation](https://reference.aspose.com/cad/java/) for in‑depth information and examples.

**Q: Is there a free trial available for Aspose.CAD for Java?**  
A: Yes, you can explore a [free trial](https://releases.aspose.com/) to experience the capabilities of Aspose.CAD for Java.

**Q: How can I seek assistance or engage in discussions about Aspose.CAD for Java?**  
A: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) to connect with the community and seek support.

**Additional Common Questions**

**Q: How do I convert a DWG file to PDF instead of DXF?**  
A: The same code works; just change the file extension in `srcFile` to `.dwg`.

**Q: Can I set a custom DPI for higher‑resolution PDFs?**  
A: Yes, use `rasterizationOptions.setResolution(300);` (or any DPI you need).

**Q: Is it possible to embed fonts in the generated PDF?**  
A: Aspose.CAD rasterizes the drawing, so fonts are rendered as vectors; no separate font embedding is required.

## Conclusion

By following this guide you now know how to **set custom page size** and **create PDF from CAD** files using Aspose.CAD for Java with Auto Layout Scaling. The process streamlines the **export CAD to PDF** workflow, ensures consistent scaling, and saves you valuable development time. Feel free to experiment with different page sizes, resolutions, and CAD formats to suit your project needs, whether you’re **converting DWG to PDF**, **increasing PDF resolution**, or building a **java CAD to PDF** batch processor.

---

**Last Updated:** 2026-02-15  
**Tested With:** Aspose.CAD for Java 24.12 (latest)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}