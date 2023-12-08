---
title: Effortless DGN to AutoCAD PDF Export with Aspose.CAD for Java
linktitle: Exporting DGN in AutoCAD Format to PDF
second_title: Aspose.CAD Java API
description: Explore the step-by-step guide on exporting DGN files to AutoCAD format in PDF using Aspose.CAD for Java. Elevate your Java application's CAD handling capabilities effortlessly.
type: docs
weight: 12
url: /java/dgn-export-options/exporting-dgn-to-pdf/
---
## Introduction

Welcome to this comprehensive tutorial on using Aspose.CAD for Java to export DGN files in AutoCAD format to PDF. If you're looking to enhance your Java application's capability to handle CAD files, Aspose.CAD is an excellent choice. In this tutorial, we'll guide you through the process of exporting DGN files step by step.


## Prerequisites
Before we dive into the tutorial, make sure you have the following prerequisites:
- Aspose.CAD Library: Ensure that you have the Aspose.CAD library for Java installed. You can download it [here](https://releases.aspose.com/cad/java/).
- Document Directory: Set up a document directory where your input and output files will be stored.

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

Now, let's break down the example code into multiple steps:

## Step 1: Define File Paths

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "Nikon_D90_Camera.dgn";
String outFile  = dataDir + "Nikon_D90_Camera.pdf";
```

Make sure to replace "Your Document Directory" with the actual path where your files are located.

## Step 2: Load DGN Image

```java
DgnImage objImage = (DgnImage) Image.load(fileName);
```

Load the DGN file using Aspose.CAD.

## Step 3: Set PDF Export Options

```java
PdfOptions options = new PdfOptions();
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
vectorOptions.setAutomaticLayoutsScaling(true);
vectorOptions.setLayouts(new String[] { "1", "2", "3", "9" }); // Export specific views
options.setVectorRasterizationOptions(vectorOptions);
```

Define the PDF export options, including page dimensions and layout preferences.

## Step 4: Save PDF File

```java
objImage.save(outFile, options);
```

Save the exported PDF file.

Repeat these steps for any additional DGN files you want to convert. Congratulations! You've successfully exported DGN files to AutoCAD format in PDF using Aspose.CAD for Java.

## Conclusion

In this tutorial, we explored how to leverage Aspose.CAD for Java to enhance your application's CAD file handling capabilities. With easy-to-follow steps and code examples, you can now seamlessly export DGN files to AutoCAD format in PDF.

## FAQ's

### Q1: Is Aspose.CAD compatible with all CAD file formats?

A1: Yes, Aspose.CAD supports a wide range of CAD formats, ensuring versatility in handling various file types.

### Q2: Can I customize the PDF export settings?

A2: Absolutely. As shown in the tutorial, you can adjust options such as page dimensions and layouts to suit your requirements.

### Q3: Where can I find additional support or assistance?

A3: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for community support and discussions.

### Q4: Is there a free trial available?

A4: Yes, you can access the free trial [here](https://releases.aspose.com/).

### Q5: How can I obtain a temporary license?

A5: Get a temporary license [here](https://purchase.aspose.com/temporary-license/).
