---
title: Set Canvas Size and Mode
linktitle: Set Canvas Size and Mode
second_title: Aspose.CAD Java API
description: Explore the power of Aspose.CAD for Java with our step-by-step guide on setting canvas size and mode. Effortlessly convert CAD files to PDF and TIFF formats.
type: docs
weight: 16
url: /java/advanced-cad-features/set-canvas-size-and-mode/
---
## Introduction

Are you looking to harness the power of Aspose.CAD for Java to enhance your CAD conversion process? This comprehensive guide will walk you through the steps of setting canvas size and mode using Aspose.CAD for Java. Whether you're a seasoned developer or just getting started, this tutorial will provide you with the insights you need.

## Prerequisites

Before diving into the tutorial, make sure you have the following prerequisites in place:

- Aspose.CAD for Java: Ensure that you have the Aspose.CAD library installed in your Java environment. You can download it [here](https://releases.aspose.com/cad/java/).

- Document Directory: Set up a document directory to store your CAD files. This directory will be referenced in the tutorial steps.

Now, let's get started with the step-by-step guide.

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

## Step 2: Set CadRasterizationOptions Properties

```java
// Create an instance of CadRasterizationOptions and set its various properties
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

Here, we create an instance of `CadRasterizationOptions` and configure properties such as page width, page height, and scaling options.

## Step 3: Create PdfOptions and Set VectorRasterizationOptions

```java
// Create an instance of PdfOptions
PdfOptions pdfOptions = new PdfOptions();

// Set the VectorRasterizationOptions property
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Now, we create a `PdfOptions` instance and set its `VectorRasterizationOptions` property to the previously configured `CadRasterizationOptions`.

## Step 4: Export to PDF

```java
// Export CAD to PDF
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

Finally, we save the CAD image to a PDF file using the specified options.

## Step 5: Create TiffOptions and Set VectorRasterizationOptions

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

Finally, we save the CAD image to a TIFF file using the specified options.

## Conclusion

Congratulations! You've successfully set the canvas size and mode using Aspose.CAD for Java. This tutorial provides a solid foundation for your CAD conversion projects. Explore more features and possibilities in the [Aspose.CAD documentation](https://reference.aspose.com/cad/java/).

## FAQ's

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
