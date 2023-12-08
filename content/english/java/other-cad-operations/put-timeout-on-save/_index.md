---
title: Timeout on Save for CAD with Aspose.CAD
linktitle: Put Timeout on Save
second_title: Aspose.CAD Java API
description: Learn how to boost your Java application's performance with Aspose.CAD. Put a timeout on save for CAD drawings. Follow our step-by-step guide.
type: docs
weight: 15
url: /java/other-cad-operations/put-timeout-on-save/
---
## Introduction

Welcome to the tutorial on putting a timeout on save using Aspose.CAD for Java. In this guide, we'll walk you through the process of setting a timeout for saving CAD drawings to enhance your application's performance. Aspose.CAD for Java is a powerful library that allows you to work with CAD files in your Java applications seamlessly.

## Prerequisites

Before diving into the tutorial, make sure you have the following prerequisites in place:
- Aspose.CAD for Java Library: Ensure that you have the Aspose.CAD for Java library integrated into your project. You can download the library from the [website](https://releases.aspose.com/cad/java/).
- Development Environment: Set up your Java development environment with all the necessary tools and dependencies.

## Import Packages

To get started, import the required packages into your Java project. Add the following lines at the beginning of your Java file:

```java
import com.aspose.cad.Image;
import com.aspose.cad.InterruptionTokenSource;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.concurrent.TimeUnit;
```

Now, let's break down the example code into step-by-step instructions:

## Step 1: Set Source and Output Directories

```java
final String SourceDir = Utils.getDataDir_DWGDrawings();
final String OutputDir = Utils.getDataDir_Output();
```

Ensure you have the correct source and output directories for your CAD drawings.

## Step 2: Create Interruption Token Source

```java
final InterruptionTokenSource source = new com.aspose.cad.InterruptionTokenSource();
```

Initialize an interruption token source to manage interruptions during the save operation.

## Step 3: Load CAD Drawing

```java
final CadImage cadImageBig = (CadImage)Image.load(SourceDir + "Drawing11.dwg");
```

Load the CAD drawing into a `CadImage` object.

## Step 4: Configure Rasterization Options

```java
CadRasterizationOptions rasterizationOptionsBig = new CadRasterizationOptions();
rasterizationOptionsBig.setPageWidth(cadImageBig.getSize().getWidth() / 2);
rasterizationOptionsBig.setPageHeight(cadImageBig.getSize().getHeight() / 2);
```

Configure rasterization options for the CAD drawing.

## Step 5: Configure PDF Options

```java
final PdfOptions CADfBig = new PdfOptions();
CADfBig.setVectorRasterizationOptions(rasterizationOptionsBig);
CADfBig.setInterruptionToken(source.getToken());
```

Set up PDF options with vector rasterization options and the interruption token.

## Step 6: Save Drawing with Timeout

```java
cadImageBig.save(OutputDir + "PutTimeoutOnSave_out.pdf", CADfBig);
```

Save the CAD drawing to a PDF file with the specified timeout.

## Step 7: Handle Interruption

```java
java.lang.Thread thread = new java.lang.Thread(new Runnable() {
    @Override
    public void run() {
        try {
            cadImageBig.save(OutputDir + "PutTimeoutOnSave_out.pdf", CADfBig);
        } catch (Throwable th) {
            System.out.println("interrupted !!!");
        }
    }
});
thread.start();
TimeUnit.SECONDS.sleep(3);
source.interrupt();
thread.join();
```

Create a thread to handle the save operation and interrupt it after a specified timeout.

## Conclusion

Congratulations! You have successfully learned how to put a timeout on save using Aspose.CAD for Java. This feature can greatly enhance the efficiency of your CAD-related applications.

## FAQ's

### Q1: How can I download Aspose.CAD for Java?

A1: You can download it from the [releases page](https://releases.aspose.com/cad/java/).

### Q2: Where can I find the documentation for Aspose.CAD for Java?

A2: Refer to the [documentation](https://reference.aspose.com/cad/java/) for comprehensive information.

### Q3: Is there a free trial available?

A3: Yes, you can get a free trial from [this link](https://releases.aspose.com/).

### Q4: How do I obtain a temporary license?

A4: Visit [here](https://purchase.aspose.com/temporary-license/) for temporary license details.

### Q5: Need help or have questions?

A5: Head over to the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for community support.
