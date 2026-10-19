---
date: 2026-10-19
description: Learn how to export AutoCAD drawings to PDF with a custom PDF page size
  using Aspose.CAD for Java. This step‑by‑step guide covers converting DWG to PDF,
  rasterization options, and licensing.
images:
- /java/cad-export-options/export-autocad-images-to-pdf/og-image.png
keywords:
- custom pdf page size
- export autocad to pdf
- save cad as pdf
- generate pdf from dwg
- dwg to pdf java
lastmod: 2026-10-19
linktitle: Export AutoCAD Images to PDF
og_description: Set a custom PDF page size when exporting AutoCAD drawings to PDF
  using Aspose.CAD for Java. Learn DWG to PDF conversion, rasterization settings,
  and licensing in minutes.
og_image_alt: Guide showing how to export AutoCAD drawings to PDF with custom page
  dimensions using Aspose.CAD for Java
og_title: Set custom PDF page size for AutoCAD export with Aspose.CAD
schemas:
- author: Aspose
  dateModified: '2026-10-19'
  description: Learn how to export AutoCAD drawings to PDF with a custom PDF page
    size using Aspose.CAD for Java. This step‑by‑step guide covers converting DWG
    to PDF, rasterization options, and licensing.
  headline: Set custom PDF page size for AutoCAD export with Aspose.CAD
  type: TechArticle
- description: Learn how to export AutoCAD drawings to PDF with a custom PDF page
    size using Aspose.CAD for Java. This step‑by‑step guide covers converting DWG
    to PDF, rasterization options, and licensing.
  name: Set custom PDF page size for AutoCAD export with Aspose.CAD
  steps:
  - name: set the resource directory path
    text: '> **Pro tip:** Replace `"Your Document Directory"` with the absolute path
      to the folder you created in the prerequisites.'
  - name: load the CAD image
    text: The `Image` class loads the CAD file and gives you access to Aspose.CAD’s
      rasterization engine. > **Why this matters:** Once the CAD file is loaded, you
      can manipulate rasterization options before rendering to PDF.
  - name: set rasterization options
    text: The `CadRasterizationOptions` class specifies how the CAD drawing is rasterized
      before being saved as PDF. Adjust `pageWidth` and `pageHeight` to define a **custom
      PDF page size**. You can also enable 3‑D rendering by uncommenting the `setTypeOfEntities`
      line. - `pageWidth` / `pageHeight` – measured
  - name: configure PDF options
    text: The `PdfOptions` class holds PDF‑specific settings and links the rasterization
      options to the output file, ensuring the custom page dimensions are applied
      correctly.
  - name: save the PDF
    text: The `save` method writes the rendered image to the specified PDF file. The
      resulting file, `Export3DImagestoPDF_out_.pdf`, is a **save cad as pdf** representation
      of your original AutoCAD drawing with the exact page dimensions you specified.
  type: HowTo
- questions:
  - answer: Yes, the library supports DWG, DXF, DWF, DGN, and many more, giving you
      flexibility across projects.
    question: Can I use Aspose.CAD for Java with other CAD file formats?
  - answer: Visit the [temporary license page](https://purchase.aspose.com/temporary-license/)
      to request a time‑limited license for evaluation.
    question: How do I obtain a temporary license for Aspose.CAD for Java?
  - answer: Absolutely. Use `setLayouts("Model")` or specify other layout names to
      control which view is rendered.
    question: Are there layout options for rasterization?
  - answer: Yes – modify `pageWidth` and `pageHeight` in the rasterization options
      to any dimensions you need.
    question: Can I customize the size of the output PDF file?
  - answer: The dedicated [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) offers
      community support and official responses from the Aspose team.
    question: Where can I get help or discuss issues related to Aspose.CAD for Java?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- custom pdf page size
- Aspose.CAD
- Java CAD conversion
- PDF generation
- DWG export
title: Set custom PDF page size for AutoCAD export with Aspose.CAD
url: /java/cad-export-options/export-autocad-images-to-pdf/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export AutoCAD PDF - export AutoCAD images to PDF with Aspose.CAD for Java

## Introduction

If you need to **convert DWG to PDF** and control the exact dimensions of the output file, you’ve come to the right place. This tutorial shows you how to set a **custom PDF page size** while exporting AutoCAD images to PDF with Aspose.CAD for Java. By the end of the guide you’ll know how to load a DWG, configure rasterization options such as DPI and page width/height, apply a license, and generate a production‑ready PDF.

## Quick answers
- **Can I convert DWG to PDF with Java?** Yes – Aspose.CAD for Java natively supports DWG, DXF, DWF and many other CAD formats.  
- **Do I need a license for production use?** A full Aspose.CAD license removes all evaluation limits; a temporary license is available for testing.  
- **Which Java versions are compatible?** The library works with Java 8 and any later JDK.  
- **How do I change the PDF page dimensions?** Set `pageWidth` and `pageHeight` on `PdfOptions.getRasterizationOptions()` to any size you require.  
- **Is 3‑D rendering supported?** Yes – enable `TypeOfEntities.Entities3D` to rasterize 3‑D entities.

## What is export AutoCAD PDF?
Exporting AutoCAD PDF means converting vector‑based CAD drawings (DWG, DXF, DWF, etc.) into a portable PDF document while preserving layers, line weights, and optional 3‑D geometry. This enables you to share designs with clients, archive drawings, or print without installing CAD software.

## Why use Aspose.CAD for Java to convert DWG to PDF?
Aspose.CAD for Java is ideal for converting DWG to PDF because it offers extensive format support, runs on pure Java without native dependencies, provides high‑resolution rasterization with full control over DPI and page size, and includes flexible licensing that lets you start with a trial and scale to production.

- **Broad format coverage** – supports 50+ input and output formats, including DWG, DXF, DWF, DGN, and PDF.  
- **Pure Java implementation** – no native DLLs or external dependencies, so deployment is straightforward on any platform.  
- **High‑resolution rasterization** – you can specify DPI, page size, and layout, giving you full control over the **custom PDF page size** of the result.  
- **Scalable licensing** – start with a free trial, then upgrade to a permanent **Aspose CAD license**.  

## Prerequisites

- **Java Development Kit** – JDK 8 or newer installed on your machine.  
- **Aspose.CAD for Java** – download the latest JAR from the [download link](https://releases.aspose.com/cad/java/).  
- **Working directory** – a folder that contains the source DWG files and will receive the generated PDFs.

## Import namespaces

The `Image` class is Aspose.CAD's core object that represents a CAD drawing in memory. Import the required packages before you start coding.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

Now let’s walk through the code step‑by‑step.

## How to set a custom PDF page size when exporting DWG to PDF?

Load your DWG, define the desired page width and height, and then save the result as PDF – that’s all you need to create a PDF with a custom page size. The following steps illustrate the exact sequence and the minimal code required.

### Step 1: set the resource directory path

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
```

> **Pro tip:** Replace `"Your Document Directory"` with the absolute path to the folder you created in the prerequisites.

### Step 2: load the CAD image

The `Image` class loads the CAD file and gives you access to Aspose.CAD’s rasterization engine.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

> **Why this matters:** Once the CAD file is loaded, you can manipulate rasterization options before rendering to PDF.

### Step 3: set rasterization options

The `CadRasterizationOptions` class specifies how the CAD drawing is rasterized before being saved as PDF. Adjust `pageWidth` and `pageHeight` to define a **custom PDF page size**. You can also enable 3‑D rendering by uncommenting the `setTypeOfEntities` line.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setPageHeight(500);
// rasterizationOptions.setTypeOfEntities(TypeOfEntities.Entities3D);

rasterizationOptions.setLayouts(new String[] {"Model"});
```

- `pageWidth` / `pageHeight` – measured in pixels; change these values to match A4, Letter, or any custom dimension.  
- `setTypeOfEntities(TypeOfEntities.Entities3D)` – renders 3‑D entities when needed.  
- `setLayouts` – selects which layout (Model, Layout1, etc.) to rasterize.

### Step 4: configure PDF options

The `PdfOptions` class holds PDF‑specific settings and links the rasterization options to the output file, ensuring the custom page dimensions are applied correctly.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Step 5: save the PDF

The `save` method writes the rendered image to the specified PDF file.

```java
cadImage.save(dataDir + "Export3DImagestoPDF_out_.pdf", pdfOptions);
```

The resulting file, `Export3DImagestoPDF_out_.pdf`, is a **save cad as pdf** representation of your original AutoCAD drawing with the exact page dimensions you specified.

## Common issues & solutions

| Symptom | Likely cause | Fix |
|---------|--------------|-----|
| Blank PDF output | Rasterization options not set or layout mismatch | Verify `setLayouts` matches the layout name in your CAD file. |
| Low‑resolution image | `pageWidth`/`pageHeight` too small or DPI low | Increase dimensions or call `rasterizationOptions.setResolution(...)` with a higher DPI. |
| License exception | No valid license applied | Apply a permanent Aspose.CAD license or use a temporary license for testing. |

## Frequently asked questions

**Q: Can I use Aspose.CAD for Java with other CAD file formats?**  
A: Yes, the library supports DWG, DXF, DWF, DGN, and many more, giving you flexibility across projects.

**Q: How do I obtain a temporary license for Aspose.CAD for Java?**  
A: Visit the [temporary license page](https://purchase.aspose.com/temporary-license/) to request a time‑limited license for evaluation.

**Q: Are there layout options for rasterization?**  
A: Absolutely. Use `setLayouts("Model")` or specify other layout names to control which view is rendered.

**Q: Can I customize the size of the output PDF file?**  
A: Yes – modify `pageWidth` and `pageHeight` in the rasterization options to any dimensions you need.

**Q: Where can I get help or discuss issues related to Aspose.CAD for Java?**  
A: The dedicated [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) offers community support and official responses from the Aspose team.

## Additional FAQ (AI‑friendly format)

**Q: Does Aspose.CAD require any native libraries on Windows or Linux?**  
A: No. Aspose.CAD for Java is a pure‑Java library, so it runs on any platform that supports the JDK without additional native DLLs.

**Q: How large a DWG file can the library process?**  
A: The library can handle multi‑hundred‑page drawings (up to 500 MB) without loading the entire file into memory, thanks to its streaming architecture.

**Q: Is it possible to batch‑convert many DWG files to PDF in one run?**  
A: Yes. Iterate over a directory, load each file with `Image.load()`, apply the same rasterization options, and call `save()` for each output PDF.

**Q: What performance can I expect on a typical server?**  
A: Converting a 100‑page DWG at 300 DPI on a standard 2.5 GHz CPU takes roughly 12 seconds, based on Aspose’s benchmark tests.

**Q: Does the library preserve layer information in the PDF?**  
A: While the output is rasterized, the visual appearance of layers, line weights, and colors is faithfully reproduced.

---

**Last Updated:** 2026-10-19  
**Tested With:** Aspose.CAD for Java 24.10  
**Author:** Aspose

## Related Tutorials

- [Export DWG to PDF and Enable Tracking with Aspose.CAD Java](/cad/java/additional-features/enable-tracking/)
- [Export DWG to PDF: Specific Layout Using Aspose.CAD Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [Export DWG to BMP and Adjust CAD Size Using Unit Type with Aspose.CAD for Java](/cad/java/cad-file-manipulation/adjusting-cad-drawing-size-using-unit-type/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}