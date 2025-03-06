---
title: Export DWG to PDF or Raster Using Aspose.CAD for Java
linktitle: Export DWG to PDF or Raster
second_title: Aspose.CAD Java API
description: Explore the seamless process of exporting DWG files to PDF or raster images in Java using Aspose.CAD. This step-by-step guide ensures precision and efficiency.
weight: 13
url: /java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export DWG to PDF or Raster Using Aspose.CAD for Java

## Introduction

In the dynamic world of computer-aided design (CAD), efficient handling of drawings is crucial. Aspose.CAD for Java provides a powerful solution for exporting DWG files to PDF or raster images. This tutorial will guide you through the process, ensuring you harness the full potential of Aspose.CAD for Java.

## Prerequisites

Before diving into the tutorial, make sure you have the following:

- Basic understanding of Java programming.
- Aspose.CAD for Java library installed. If not, download it [here](https://releases.aspose.com/cad/java/).
- A DWG file for testing purposes. You can use the provided "Bottom_plate.dwg" file.

## Import Namespaces

In your Java project, import the necessary namespaces to kickstart the process:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.UnitType;
```

## Step 1: Load the DWG File

Start by loading your DWG file using Aspose.CAD's `Image` class:

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Bottom_plate.dwg";
Image objImage = Image.load(srcFile);
```

## Step 2: Determine Unit Type

Next, check the unit type of the loaded DWG file:

```java
Boolean currentUnitIsMetric = IsMetric(objImage.getUnitType());
int currentUnitCoefficient = objImage.getUnitType();
```

## Step 3: Set Rasterization Options

Based on the unit type, configure the rasterization options:

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();

if (currentUnitIsMetric) {
    // Metric units
    double metersCoeff = 1 / 1000.0;
    double scaleFactor = metersCoeff / currentUnitCoefficient;
    rasterizationOptions.setPageWidth((float)(210 * scaleFactor));
    rasterizationOptions.setPageHeight((float)(297 * scaleFactor));
    rasterizationOptions.setUnitType(UnitType.Millimeter);
} else {
    // Imperial units
    rasterizationOptions.setPageWidth((float)(8.27f / currentUnitCoefficient));
    rasterizationOptions.setPageHeight((float)(11.69f / currentUnitCoefficient));
    rasterizationOptions.setUnitType(UnitType.Inch);
}
```

## Step 4: Configure PDF Options

Set up PDF export options:

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());
```

## Step 5: Save as PDF

Finally, save the DWG file as a PDF:

```java
objImage.save(dataDir + "Saved.pdf", pdfOptions);
```

And there you have it! You've successfully exported a DWG file to PDF using Aspose.CAD for Java.

## Conclusion

This tutorial provided a step-by-step guide on leveraging Aspose.CAD for Java to export DWG files to PDF or raster images. This library simplifies the process, allowing you to efficiently handle CAD drawings in your Java applications.

## FAQ's

### Q1: Can I use Aspose.CAD for Java with other Java frameworks?

A1: Yes, Aspose.CAD for Java seamlessly integrates with popular Java frameworks.

### Q2: Is a temporary license available for Aspose.CAD for Java?

A2: Yes, you can obtain a temporary license [here](https://purchase.aspose.com/temporary-license/).

### Q3: Where can I find support for Aspose.CAD for Java?

A3: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for assistance from the community.

### Q4: How can I purchase a license for Aspose.CAD for Java?

A4: You can purchase a license [here](https://purchase.aspose.com/buy).

### Q5: What units does Aspose.CAD for Java support?

A5: Aspose.CAD for Java supports both metric and imperial units.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
