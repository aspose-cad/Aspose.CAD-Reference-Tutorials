---
title: Customize PDF Page Size: Export DGN to PDF with Aspose.CAD
linktitle: Exporting DGN in AutoCAD Format to PDF
second_title: Aspose.CAD Java API
description: Learn how to customize PDF page size while exporting DGN to PDF with Aspose.CAD for Java. Step‑by‑step guide for Java CAD to PDF conversion.
weight: 12
url: /java/dgn-export-options/exporting-dgn-to-pdf/
date: 2026-01-10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Customize PDF Page Size: Export DGN to PDF with Aspose.CAD

## Introduction

If you need to **customize PDF page size** when converting DGN drawings to PDF, you’ve come to the right place. In this tutorial we’ll walk through the complete process of exporting DGN files to PDF using Aspose.CAD for Java, while giving you full control over page dimensions, layout selection, and rasterization options. By the end, you’ll be able to integrate this into any Java application that requires **how to export DGN** files or **generate PDF from CAD** data.

## Quick Answers
- **Can I set a custom page size?** Yes – use `CadRasterizationOptions` to specify width and height.  
- **Which library handles the conversion?** Aspose.CAD for Java.  
- **Do I need a license for production?** A valid Aspose.CAD license is required; a free trial is available.  
- **Is the conversion loss‑less?** Vector data is rasterized at the resolution you define, preserving detail.  
- **Can I export specific layouts only?** Absolutely – set the `layouts` property with the desired view IDs.

## What is customizing PDF page size?
Customizing PDF page size means defining the exact width and height (in pixels) of the output PDF pages. This is essential when you need PDFs that match printing standards, fit inside predefined report templates, or align with other documents.

## Why customize PDF page size when exporting DGN?
- **Consistent branding** – match corporate stationery dimensions.  
- **Optimized file size** – larger pages can increase resolution, smaller pages reduce size.  
- **Better integration** – PDFs that fit into existing layouts without extra scaling.  

## Prerequisites
Before we dive in, ensure you have:

- **Aspose.CAD Library** – download it [here](https://releases.aspose.com/cad/java/).
- **Document Directory** – a folder on your system where the source DGN and the resulting PDF will reside.

## Import Packages

In your Java project, import the necessary packages to access Aspose.CAD functionalities:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## How to customize PDF page size when exporting DGN to PDF?

### Step 1: Define File Paths

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "Nikon_D90_Camera.dgn";
String outFile  = dataDir + "Nikon_D90_Camera.pdf";
```

Replace **“Your Document Directory”** with the actual path on your machine.

### Step 2: Load the DGN Image

```java
DgnImage objImage = (DgnImage) Image.load(fileName);
```

This line reads the DGN file into an `Image` object that Aspose.CAD can work with.

### Step 3: Set PDF Export Options (including custom page size)

```java
PdfOptions options = new PdfOptions();
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);   // <-- custom width in pixels
vectorOptions.setPageHeight(1500);  // <-- custom height in pixels
vectorOptions.setAutomaticLayoutsScaling(true);
vectorOptions.setLayouts(new String[] { "1", "2", "3", "9" }); // Export specific views
options.setVectorRasterizationOptions(vectorOptions);
```

Here we explicitly **customize PDF page size** by setting `PageWidth` and `PageHeight`. Adjust these values to meet your printing or layout requirements.

### Step 4: Save the PDF File

```java
objImage.save(outFile, options);
```

The `save` method writes the rasterized content to the output PDF using the options defined above.

You can repeat the same steps for any additional DGN files you need to convert.

## Common Issues and Solutions
| Issue | Solution |
|-------|----------|
| **PDF pages are blank** | Verify that the layout IDs in `setLayouts` match those in the source DGN. |
| **Output is low‑resolution** | Increase `PageWidth`/`PageHeight` or set `vectorOptions.setResolution(300)` for higher DPI. |
| **License exception** | Ensure a valid Aspose.CAD license file is loaded before calling `Image.load`. |
| **File not found** | Double‑check `dataDir` and file names; use absolute paths for testing. |

## Frequently Asked Questions

**Q: Is Aspose.CAD compatible with all CAD file formats?**  
A: Yes, Aspose.CAD supports a wide range of CAD formats, making it versatile for many conversion scenarios.

**Q: Can I customize other PDF settings besides page size?**  
A: Absolutely. You can modify compression, embed fonts, and set PDF version via `PdfOptions`.

**Q: Where can I get additional help or examples?**  
A: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for community support and code samples.

**Q: Is a free trial available?**  
A: Yes, you can download a trial version [here](https://releases.aspose.com/).

**Q: How do I obtain a temporary license for evaluation?**  
A: Get a temporary license [here](https://purchase.aspose.com/temporary-license/).

## Conclusion

We’ve covered everything you need to **customize PDF page size** while **exporting DGN to PDF** using Aspose.CAD for Java. By following the step‑by‑step guide, you can integrate this conversion into any Java application, whether you’re building a reporting engine, a document management system, or a CAD‑to‑PDF batch processor.

---  
**Last Updated:** 2026-01-10  
**Tested With:** Aspose.CAD for Java 24.12 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}