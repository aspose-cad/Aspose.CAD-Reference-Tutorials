---
title: Export DWG as PDF with Hidden Lines – Aspose.CAD for Java
linktitle: Export DWG as PDF with Hidden Lines Using Java
second_title: Aspose.CAD Java API
description: Learn how to export DWG as PDF, enable hidden lines, and convert DWG to PDF with Aspose.CAD for Java in this step‑by‑step tutorial.
weight: 11
url: /java/cad-text-and-formatting/support-hidden-lines-in-dwg/
date: 2026-01-02
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export DWG as PDF with Hidden Lines – Aspose.CAD for Java

## Introduction

In this tutorial you’ll learn how to **export DWG as PDF** while preserving hidden lines using Aspose.CAD for Java. Whether you need to **convert DWG to PDF**, generate a **dwg to pdf tutorial**‑style guide, or simply **save DWG as PDF** with hidden‑line support, we’ll walk you through every step. By the end, you’ll have a ready‑to‑use solution that you can drop into any Java project.

## Quick Answers
- **What does this tutorial cover?** Enabling hidden‑line rendering while exporting DWG to PDF with Aspose.CAD for Java.  
- **Which primary operation is performed?** `export dwg as pdf`.  
- **Do I need a license?** A free trial works for testing; a commercial license is required for production.  
- **What are the prerequisites?** Java development environment, Aspose.CAD for Java library, and DWG files.  
- **How long does implementation take?** About 10‑15 minutes for a basic setup.

## What is “export dwg as pdf”?
Exporting a DWG file to PDF converts the vector‑based CAD drawing into a portable document format while preserving layers, line types, and optional hidden‑line rendering. This makes it easy to share CAD designs with stakeholders who may not have CAD software.

## Why enable hidden lines when exporting?
Hidden lines provide a clearer visual representation of complex 3D models on a 2‑D page, ensuring that only visible edges are emphasized. This improves readability and is often required for engineering documentation.

## Prerequisites

1. **Aspose.CAD for Java** – download the library from the official site [here](https://releases.aspose.com/cad/java/).  
2. **DWG files** – have the source DWG drawings stored in a known directory.  
3. **Java development environment** – JDK 8+ and your preferred IDE (Eclipse, IntelliJ, etc.).  

Now that you’re set up, let’s dive into the code.

## Import Namespaces

Begin by importing the necessary classes so you can work with CAD images and PDF options.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.Arrays;
import java.util.List;
```

## Step 1: Set Up Your Project

Create a Java project and add the Aspose.CAD JAR to your build path. Then define the directory that holds your DWG files.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

> **Pro tip:** Use an absolute path or configure a relative path based on your project’s resources folder.

## Step 2: Load DWG File

Load the source DWG file into a `CadImage` object so you can manipulate it.

```java
String sourceFilePath = dataDir + "Bottom_plate.dwg";
String outPath = dataDir + "Bottom_plate.pdf";
CadImage cadImage = (CadImage)Image.load(sourceFilePath);
```

## Step 3: Configure Rasterization Options

Select the layers you want to include and set the page size to match the original drawing. This is where we enable hidden‑line rendering by specifying the layout.

```java
List<String> list = Arrays.asList("Print","L1_RegMark","L2_RegMark");
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageHeight(cadImage.getHeight());
rasterizationOptions.setPageWidth(cadImage.getWidth()) ;
rasterizationOptions.setLayers(list);
```

## Step 4: Set PDF Options

Tell Aspose.CAD to rasterize the vector data into a PDF, using the “Model” layout to keep hidden lines hidden.

```java
PdfOptions pdfOptions = new PdfOptions();
rasterizationOptions.setLayouts(new String[] { "Model" });
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Step 5: Save the Result

Finally, export the DWG as a PDF file. The hidden lines will be respected according to the layout you set.

```java
cadImage.save(outPath, pdfOptions);
System.out.println("\nThe DWG file exported successfully to PDF.\nFile saved at " + dataDir);
```

> **Common Pitfall:** Forgetting to set the layout to `"Model"` will cause all lines (including hidden ones) to appear solid in the PDF.

## Conclusion

You now have a complete, production‑ready method to **export DWG as PDF** with hidden‑line support using Aspose.CAD for Java. This approach can be integrated into batch processing tools, web services, or desktop applications to automate CAD‑to‑PDF conversion.

## Frequently Asked Questions

### Q1: Can I use Aspose.CAD for Java with other CAD file formats?
A1: Yes, Aspose.CAD supports various CAD formats such as DWG, DXF, DWF, and more.

### Q2: Is there a free trial available for Aspose.CAD for Java?
A2: Yes, you can find the free trial [here](https://releases.aspose.com/).

### Q3: How do I get support for Aspose.CAD for Java?
A3: Visit the Aspose.CAD forum [here](https://forum.aspose.com/c/cad/19) for community support.

### Q4: Where can I find detailed documentation for Aspose.CAD for Java?
A4: Refer to the documentation [here](https://reference.aspose.com/cad/java/).

### Q5: Can I purchase a temporary license for Aspose.CAD for Java?
A5: Yes, you can obtain a temporary license [here](https://purchase.aspose.com/temporary-license/).

### Q6: Does this method also work for converting DWG to PDF in a headless server environment?
A6: Absolutely. Since the code uses only the Aspose.CAD API, it runs without any UI dependencies, making it ideal for server‑side automation.

---

**Last Updated:** 2026-01-02  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}