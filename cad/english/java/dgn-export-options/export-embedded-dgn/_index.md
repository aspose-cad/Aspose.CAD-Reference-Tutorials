---
title: Export Embedded DGN to PDF with Aspose.CAD for Java
linktitle: Export Embedded DGN
second_title: Aspose.CAD Java API
description: Explore the step-by-step guide on exporting embedded DGN files to PDF using Aspose.CAD for Java. Enhance your Java applications with seamless CAD file manipulation.
weight: 11
url: /java/dgn-export-options/export-embedded-dgn/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export Embedded DGN to PDF with Aspose.CAD for Java

## Introduction

Welcome to this comprehensive tutorial on exporting embedded DGN files using Aspose.CAD for Java. Aspose.CAD is a powerful library that enables Java developers to work with CAD files seamlessly. In this tutorial, we'll guide you through the process of exporting embedded DGN files to PDF using step-by-step instructions. Whether you're a seasoned developer or just starting, this tutorial will help you harness the capabilities of Aspose.CAD to enhance your Java applications.

## Prerequisites

Before we dive into the tutorial, make sure you have the following prerequisites:
- Java Development Environment: Ensure that you have a Java development environment set up on your machine.
- Aspose.CAD for Java: Download and install Aspose.CAD for Java library from [here](https://releases.aspose.com/cad/java/).

## Import Packages

To get started, you need to import the necessary packages in your Java project. Add the following import statements to your code:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

Now, let's break down the example code into multiple steps:

## Step 1: Set Up Input and Output Paths

Define the directory path where your document is located and specify the input DWG file name.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
```

## Step 2: Load DWG File

Load the DWG file into an `Image` object using Aspose.CAD.

```java
Image objImage = Image.load(fileName);
```

## Step 3: Configure Rasterization Options

Configure rasterization options, such as layouts to be included in the export.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setLayouts(new String[] {"Model"});
```

## Step 4: Configure PDF Options

Set up PDF options, including vector rasterization options.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Step 5: Save PDF File

Save the PDF file with the configured options.
```java
objImage.save(dataDir + "BlockRefDgn.pdf", pdfOptions);
```

## Conclusion

Congratulations! You've successfully exported an embedded DGN file to PDF using Aspose.CAD for Java. This tutorial covered the essential steps to integrate Aspose.CAD into your Java application for efficient CAD file manipulation.

## FAQ's

### Q1: Can I use Aspose.CAD for Java in a commercial project?

A1: Yes, Aspose.CAD for Java is a commercial library. You can obtain a license from [here](https://purchase.aspose.com/buy).

### Q2:Is there a free trial available?

A2:Yes, you can access a free trial of Aspose.CAD for Java [here](https://releases.aspose.com/).

### Q3: How can I get support for Aspose.CAD for Java?

A3: You can seek support from the Aspose.CAD community on the [forum](https://forum.aspose.com/c/cad/19).

### Q4: What if I need a temporary license?

A4: You can obtain a temporary license [here](https://purchase.aspose.com/temporary-license/).

### Q5: Where can I find the documentation?

A5: The documentation is available [here](https://reference.aspose.com/cad/java/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
