---
title: Create PDF from DWG and Add Text Using Aspose.CAD for Java
linktitle: Add Text in DWG
second_title: Aspose.CAD Java API
description: Learn how to create PDF from DWG, save DWG as PDF, and add text to DWG drawings with Aspose.CAD for Java—step‑by‑step guide.
weight: 10
url: /java/cad-text-and-annotation/add-text-in-dwg/
date: 2025-12-28
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Create PDF from DWG and Add Text Using Aspose.CAD for Java

## Introduction

If you need to **create PDF from DWG** files while also inserting custom text, you’re in the right place. In this tutorial we’ll walk through the entire process—loading a DWG drawing, adding a text annotation, and finally saving the result as a PDF using Aspose.CAD for Java. By the end you’ll understand how to **save DWG as PDF**, customize text height, and even add basic annotations.

## Quick Answers
- **Can I convert DWG to PDF in Java?** Yes, Aspose.CAD for Java provides a straightforward API.  
- **Do I need a license for production use?** A commercial license is required; a free trial is available.  
- **Which method adds text to a DWG?** Use the `CadText` object and add it to the model space.  
- **Can I set the text height?** Absolutely—use `setTextHeight()` on the `CadText` instance.  
- **Is the output vector‑based?** When rasterization options are set to `UseObjectColor`, the PDF retains high‑quality vector data.

## Prerequisites

Before diving into the tutorial, ensure you have the following prerequisites in place:

- Aspose.CAD for Java Library: Download and install the library from the [Aspose.CAD for Java page](https://releases.aspose.com/cad/java/).

- Java Development Kit (JDK): Make sure you have the latest JDK installed on your system.

- DWG Drawing: Prepare a DWG drawing file where you want to add text.

## Import Namespaces

In your Java code, import the necessary namespaces for Aspose.CAD:

```java
import com.aspose.cad.Image;


import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadText;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

Now, let's break down the code snippet provided into multiple steps:

## Step 1: Set up Document Directory and DWG File Path

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String dwgPathToFile = dataDir + "SimpleEntites.dwg";
```

## Step 2: Load DWG Image

```java
Image image = Image.load(dwgPathToFile);
```

## Step 3: Create CadText Object (Add Text to DWG)

```java
CadText cadText = new CadText();
cadText.setStyleType("Standard");
cadText.setDefaultValue("Some custom text");
cadText.setColorId(256);
cadText.setLayerName("0");
cadText.getFirstAlignment().setX(47.9);
cadText.getFirstAlignment().setY(5.56);
cadText.setTextHeight(0.8);          // set text height in DWG units
cadText.setScaleX(0);
```

## Step 4: Add Text to CadImage (Insert Annotation)

```java
CadImage cadImage = ((CadImage)(image));
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(cadText);
```

## Step 5: Set Up PDF Options (Prepare to create PDF from DWG)

```java
PdfOptions pdfOptions = new PdfOptions();
```

## Step 6: Configure CadRasterizationOptions (Control PDF rendering)

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
cadRasterizationOptions.setPageHeight(1600);
cadRasterizationOptions.setPageWidth(1600);
cadRasterizationOptions.setLayouts(new String[] {"Model"});
```

## Step 7: Save the Modified DWG as PDF (dwg to pdf java)

```java
image.save(dataDir + "SimpleEntites_generated.dwg.pdf", pdfOptions);
```

By following these steps, you'll be able to **create PDF from DWG**, add custom text, and control text height—all with just a few lines of Java code.

## Why Add Text to DWG and Convert to PDF?

Adding text directly to a DWG file is useful for:

- **Marking up designs** with notes or part numbers.
- **Creating printable documentation** where the PDF serves as a read‑only, widely supported format.
- **Automating batch processing** of large CAD libraries without manual editing.

## Common Issues & Tips

- **Text not appearing?** Verify the X/Y coordinates are within the drawing extents and that the layer is visible.
- **Incorrect text height?** Adjust `setTextHeight()`; the value is in the drawing’s unit system.
- **PDF looks rasterized?** Ensure `CadDrawTypeMode.UseObjectColor` is set to keep vector information.
- **Performance on large files?** Increase `pageHeight`/`pageWidth` only as needed; larger values consume more memory.

## Frequently Asked Questions

**Q: Is Aspose.CAD compatible with all versions of DWG files?**  
A: Aspose.CAD supports various versions of DWG files, ensuring compatibility with a wide range of CAD software.

**Q: Can I customize the font and formatting of the added text?**  
A: Yes, you can customize the font, style, and other formatting options for the text added to DWG files using Aspose.CAD.

**Q: Is there a free trial available for Aspose.CAD for Java?**  
A: Yes, you can explore the features of Aspose.CAD by obtaining a free trial from [here](https://releases.aspose.com/).

**Q: Where can I find detailed documentation for Aspose.CAD for Java?**  
A: Refer to the documentation [here](https://reference.aspose.com/cad/java/) for in-depth information and examples.

**Q: How can I get support or seek help with Aspose.CAD?**  
A: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) to get assistance and connect with the community.

---

**Last Updated:** 2025-12-28  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}