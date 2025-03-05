---
title: Java DGN to JPEG Conversion with Aspose.CAD Tutorial
linktitle: Exporting DGN in AutoCAD Format to Raster Image Format
second_title: Aspose.CAD Java API
description: Learn how to export DGN files to JPEG images in Java using Aspose.CAD. This step-by-step tutorial guides you through the process effortlessly.
type: docs
weight: 13
url: /java/dgn-export-options/exporting-dgn-to-raster-image/
---
## Introduction

Welcome to this comprehensive tutorial on exporting DGN (Design) files to Raster Image Format using Aspose.CAD for Java. Aspose.CAD is a powerful library that enables Java developers to work with CAD files seamlessly. In this tutorial, we'll guide you through the process of converting DGN files to JPEG images, providing you with step-by-step instructions and code examples.

## Prerequisites

Before diving into the tutorial, make sure you have the following prerequisites in place:
1. Aspose.CAD Library: Ensure you have the Aspose.CAD for Java library installed. You can download it [here](https://releases.aspose.com/cad/java/).
2. Java Development Kit (JDK): Make sure you have Java installed on your machine.
3. Integrated Development Environment (IDE): Use a Java-compatible IDE like IntelliJ or Eclipse.

## Import Packages

In your Java project, import the necessary packages for Aspose.CAD. Add the following lines to your code:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
```

## Step 1: Load DGN File

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
DgnImage dgnImage = (DgnImage) Image.load(dataDir + "Nikon_D90_Camera.dgn");
```

## Step 2: Create JpegOptions Object

```java
ImageOptionsBase options = new JpegOptions();
```

## Step 3: Assign Rasterization Options

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(600);
vectorOptions.setPageHeight(400);
vectorOptions.setNoScaling(true);
vectorOptions.setAutomaticLayoutsScaling(false);
options.setVectorRasterizationOptions(vectorOptions);
```

## Step 4: Save the Converted Image

```java
OutputStream outStream = new FileOutputStream(dataDir + "ExportDGNToRasterImage_Out.jpg");
dgnImage.save(outStream, options);
```

Repeat these steps for your specific DGN files, adjusting the file paths accordingly.

## Conclusion

Congratulations! You've successfully learned how to export DGN files to Raster Image Format using Aspose.CAD for Java. This tutorial has equipped you with the knowledge to incorporate this functionality into your Java applications.

## FAQ's

### Q1: Can I use Aspose.CAD for Java with other CAD file formats?

A1: Yes, Aspose.CAD supports various CAD formats, providing a versatile solution for Java developers.

### Q2: Is there a free trial available for Aspose.CAD for Java?

A2: Yes, you can access a free trial [here](https://releases.aspose.com/).

### Q3: Where can I find documentation for Aspose.CAD for Java?

A3: Refer to the documentation [here](https://reference.aspose.com/cad/java/).

### Q4: How can I get support for Aspose.CAD for Java?

A4: Visit the support forum [here](https://forum.aspose.com/c/cad/19).

### Q5: Where can I purchase a license for Aspose.CAD for Java?

A5: You can buy a license [here](https://purchase.aspose.com/buy).
