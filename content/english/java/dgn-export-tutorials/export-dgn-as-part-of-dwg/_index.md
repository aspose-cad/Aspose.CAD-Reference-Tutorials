---
title: Export DGN to DWG with Aspose.CAD for Java
linktitle: Export DGN as Part of DWG - Aspose.CAD for Java Tutorial
second_title: Aspose.CAD Java API
description: Explore how to export DGN as part of DWG using Aspose.CAD for Java. Follow our step-by-step guide for efficient CAD file manipulation.
type: docs
weight: 10
url: /java/dgn-export-tutorials/export-dgn-as-part-of-dwg/
---
## Introduction

In this tutorial, we'll explore how to use Aspose.CAD for Java to export a DGN (MicroStation Design) file as part of a DWG (AutoCAD Drawing) file. Aspose.CAD is a powerful library that provides comprehensive functionality to work with CAD file formats. This step-by-step guide will help you understand the process of exporting DGN as part of DWG using Java.

## Prerequisites

Before we dive into the tutorial, make sure you have the following prerequisites in place:
1. Aspose.CAD Library: Download and install the Aspose.CAD library for Java. You can find the library [here](https://releases.aspose.com/cad/java/).
2. Java Development Kit (JDK): Ensure that you have Java installed on your system.
3. Integrated Development Environment (IDE): Choose a Java IDE like Eclipse or IntelliJ for a smoother development experience.

## Import Packages

In your Java project, import the necessary Aspose.CAD packages to enable CAD file manipulation. Here's an example:

```java
import com.aspose.cad;
import com.aspose.cad.imageoptions;
import com.aspose.cad.fileformats.cad.cadconsts;
import com.aspose.cad.fileformats.cad;
import com.aspose.cad.fileformats.cad.cadobjects;
```

## Step 1: Set File Paths

Define the input and output file paths for the DWG file. Update the `dataDir`, `fileName`, and `outPath` variables accordingly.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
String outPath = dataDir + "BlockRefDgn.dwg.pdf";
```

## Step 2: Create PdfOptions Instance

Create an instance of the `PdfOptions` class, as we are exporting the DWG file to PDF format.

```java
PdfOptions exportOptions = new PdfOptions();
```

## Step 3: Load DWG File

Load the existing DWG file as an image and convert it to the `CadImage` type.

```java
CadImage cadImage = (CadImage) Image.load(fileName);
```

## Step 4: Iterate Through Entities

Go through each entity inside the DWG file and check if it is an image definition. If it is, retrieve the external reference to the object.

```java
for (CadBaseEntity baseEntity : cadImage.getEntities()) {
    if (baseEntity.getTypeName() == CadEntityTypeName.DGNUNDERLAY) {
        CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
        System.out.println(dgnFile.getUnderlayPath());
    }
}
```

## Step 5: Define Rasterization Options

Define settings for the `CadRasterizationOptions` object, including page width, height, layouts, and background color.

```java
CadRasterizationOptions vectorRasterizationOptions = new CadRasterizationOptions();
vectorRasterizationOptions.setPageWidth(1600);
vectorRasterizationOptions.setPageHeight(1600);
vectorRasterizationOptions.setLayouts(new String[] { "Model" });
vectorRasterizationOptions.setAutomaticLayoutsScaling(false);
vectorRasterizationOptions.setNoScaling(true);
vectorRasterizationOptions.setBackgroundColor(Color.getBlack());
vectorRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
```

## Step 6: Set Vector Rasterization Options

Set the vector rasterization options for the export.

```java
exportOptions.setVectorRasterizationOptions(vectorRasterizationOptions);
```

## Step 7: Export DWG to PDF

Finally, export the DWG to PDF by calling the `save` method.

```java
cadImage.save(outPath, exportOptions);
```

## Conclusion

Congratulations! You've successfully learned how to export a DGN file as part of a DWG file using Aspose.CAD for Java. This powerful library provides extensive capabilities for working with CAD files, making your CAD file manipulation tasks efficient and straightforward.

## FAQ's

### Q1: Where can I find the documentation for Aspose.CAD for Java?

A1: The official documentation can be found [here](https://reference.aspose.com/cad/java/).

### Q2: How can I download the Aspose.CAD library for Java?

A2: You can download the library from [this link](https://releases.aspose.com/cad/java/).

### Q3: Is there a free trial available for Aspose.CAD for Java?

A3: Yes, you can find the free trial [here](https://releases.aspose.com/).

### Q4: Where can I get a temporary license for Aspose.CAD for Java?

A4: Obtain a temporary license [here](https://purchase.aspose.com/temporary-license/).

### Q5: Need help or have questions?

A5: Visit the Aspose.CAD community support forum [here](https://forum.aspose.com/c/cad/19).
