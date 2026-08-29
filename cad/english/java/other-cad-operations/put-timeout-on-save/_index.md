---
title: How to Set Timeout on Save for CAD with Aspose.CAD
linktitle: Put Timeout on Save
second_title: Aspose.CAD Java API
description: Learn how to set timeout on saving CAD drawings with Aspose.CAD for Java. Boost performance, avoid hangs, and export CAD to PDF efficiently.
weight: 15
url: /java/other-cad-operations/put-timeout-on-save/
date: 2026-06-19
keywords:
  - how to set timeout
  - convert dwg to pdf
  - export cad to pdf
schemas:
- type: TechArticle
  headline: How to Set Timeout on Save for CAD with Aspose.CAD
  description: Learn how to set timeout on saving CAD drawings with Aspose.CAD for
    Java. Boost performance, avoid hangs, and export CAD to PDF efficiently.
  dateModified: '2026-06-19'
  author: Aspose
- type: HowTo
  name: How to Set Timeout on Save for CAD with Aspose.CAD
  description: Learn how to set timeout on saving CAD drawings with Aspose.CAD for
    Java. Boost performance, avoid hangs, and export CAD to PDF efficiently.
  steps:
  - name: Set Source and Output Directories
    text: Ensure you have the correct source and output directories for your CAD drawings.
  - name: Create Interruption Token Source
    text: Initialize an interruption token source to manage interruptions during the
      save operation.
  - name: Load CAD Drawing
    text: The `CadImage` class is Aspose.CAD's core object that represents a CAD drawing
      in memory, offering methods for rendering and conversion.
  - name: Configure Rasterization Options
    text: '`CadRasterizationOptions` specifies how the CAD drawing is rasterized into
      an image. Configure rasterization options for the CAD drawing.'
  - name: Configure PDF Options
    text: '`PdfOptions` defines settings for saving a CAD drawing as a PDF document.
      Set up PDF options with vector rasterization options and the interruption token.'
  - name: Save Drawing with Timeout
    text: Save the CAD drawing to a PDF file with the specified timeout.
  - name: Handle Interruption
    text: '`OperationCanceledException` is thrown when a save operation exceeds the
      specified timeout. Create a thread to handle the save operation and interrupt
      it after a specified timeout.'
- type: FAQPage
  questions:
  - question: Can I use this feature to convert DWG to PDF in a batch job?
    answer: Yes, wrap each conversion in its own thread with a separate interruption
      token to enforce per‑file time limits.
  - question: Does the timeout work on all output formats?
    answer: The timeout mechanism is tied to the `InterruptionTokenSource` and works
      with any format that respects the token, including PDF, PNG, and SVG.
  - question: What happens to partially written files after a timeout?
    answer: Aspose.CAD automatically discards incomplete output, so you won’t end
      up with corrupted PDFs.
  - question: Is a license required for production use?
    answer: Yes, a valid Aspose.CAD license is required for commercial deployments;
      a free trial is available for evaluation.
  - question: Where can I find more examples of using interruption tokens?
    answer: The official Aspose.CAD documentation provides additional code snippets
      and best‑practice guidelines.
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# How to Set Timeout on Save for CAD with Aspose.CAD

## Introduction

In this comprehensive guide you’ll learn **how to set timeout** when saving CAD drawings using Aspose.CAD for Java. Applying a timeout prevents long‑running save operations from hanging your application, which is especially important when you need to **export CAD to PDF** or **convert DWG to PDF** in batch processing scenarios. Aspose.CAD for Java supports more than 50 CAD formats and can handle multi‑hundred‑page files without loading the entire document into memory, giving you predictable performance and resource usage.

## Quick Answers
- **What does the timeout do?** It aborts the save operation after a specified period, freeing the thread and preventing resource leaks.  
- **Which class controls the timeout?** `InterruptionTokenSource` provides the cancellation token used by the save routine.  
- **Can I still export CAD to PDF after a timeout?** Yes – you can catch the interruption exception and retry or log the failure.  
- **Do I need a special license?** A regular Aspose.CAD license is sufficient; the timeout feature is built‑in.  
- **Is this approach thread‑safe?** Yes, when each save runs in its own thread with its own token.

## What is a timeout in CAD save operations?
A timeout is a configurable time limit that, when exceeded, forces the save process to stop and raise an interruption exception. This protects your Java application from indefinite hangs caused by complex drawings or I/O bottlenecks.

## Why set a timeout when saving CAD files?
Aspose.CAD can **convert DWG to PDF** and **export CAD to PDF** in under a second for typical drawings, but extremely large or corrupted files may take minutes. By defining a timeout you guarantee that any single save will not exceed, for example, 30 seconds, keeping overall batch throughput stable and preventing thread starvation.

## Prerequisites

Before diving into the tutorial, make sure you have the following prerequisites in place:
- **Aspose.CAD for Java Library** – Ensure that you have the Aspose.CAD for Java library integrated into your project. You can download the library from the [website](https://releases.aspose.com/cad/java/).
- **Development Environment** – Set up your Java development environment with all the necessary tools and dependencies.

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

Now, let's break down the example code into step‑by‑step instructions:

## How to set timeout on save for CAD drawings?

Load your CAD file, create an `InterruptionTokenSource` with the desired timeout, and pass the token to the PDF save options. If the operation exceeds the timeout, Aspose.CAD throws an `OperationCanceledException`, which you can catch to handle the failure gracefully.

### Step 1: Set Source and Output Directories

```java
final String SourceDir = Utils.getDataDir_DWGDrawings();
final String OutputDir = Utils.getDataDir_Output();
```

Ensure you have the correct source and output directories for your CAD drawings.

### Step 2: Create Interruption Token Source

```java
final InterruptionTokenSource source = new com.aspose.cad.InterruptionTokenSource();
```

Initialize an interruption token source to manage interruptions during the save operation.

### Step 3: Load CAD Drawing

The `CadImage` class is Aspose.CAD's core object that represents a CAD drawing in memory, offering methods for rendering and conversion.

```java
final CadImage cadImageBig = (CadImage)Image.load(SourceDir + "Drawing11.dwg");
```

### Step 4: Configure Rasterization Options

`CadRasterizationOptions` specifies how the CAD drawing is rasterized into an image.

```java
CadRasterizationOptions rasterizationOptionsBig = new CadRasterizationOptions();
rasterizationOptionsBig.setPageWidth(cadImageBig.getSize().getWidth() / 2);
rasterizationOptionsBig.setPageHeight(cadImageBig.getSize().getHeight() / 2);
```

Configure rasterization options for the CAD drawing.

### Step 5: Configure PDF Options

`PdfOptions` defines settings for saving a CAD drawing as a PDF document.

```java
final PdfOptions CADfBig = new PdfOptions();
CADfBig.setVectorRasterizationOptions(rasterizationOptionsBig);
CADfBig.setInterruptionToken(source.getToken());
```

Set up PDF options with vector rasterization options and the interruption token.

### Step 6: Save Drawing with Timeout

```java
cadImageBig.save(OutputDir + "PutTimeoutOnSave_out.pdf", CADfBig);
```

Save the CAD drawing to a PDF file with the specified timeout.

### Step 7: Handle Interruption

`OperationCanceledException` is thrown when a save operation exceeds the specified timeout.

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

## Common Issues and Solutions

- **Timeout Too Short** – If you receive frequent interruptions, increase the timeout value to accommodate larger drawings.  
- **InterruptedException Not Caught** – Always wrap the save call in a try‑catch block for `OperationCanceledException` to prevent the application from crashing.  
- **Memory Consumption** – Use `PdfOptions.setVectorRasterizationOptions` to stream output rather than loading the whole file into memory.

## Frequently Asked Questions

**Q: Can I use this feature to convert DWG to PDF in a batch job?**  
A: Yes, wrap each conversion in its own thread with a separate interruption token to enforce per‑file time limits.

**Q: Does the timeout work on all output formats?**  
A: The timeout mechanism is tied to the `InterruptionTokenSource` and works with any format that respects the token, including PDF, PNG, and SVG.

**Q: What happens to partially written files after a timeout?**  
A: Aspose.CAD automatically discards incomplete output, so you won’t end up with corrupted PDFs.

**Q: Is a license required for production use?**  
A: Yes, a valid Aspose.CAD license is required for commercial deployments; a free trial is available for evaluation.

**Q: Where can I find more examples of using interruption tokens?**  
A: The official Aspose.CAD documentation provides additional code snippets and best‑practice guidelines.

## Additional Resources

- [releases page](https://releases.aspose.com/cad/java/) – Direct download page for the latest Aspose.CAD for Java releases.  
- [documentation](https://reference.aspose.com/cad/java/) – Full API reference and developer guides.  
- [this link](https://releases.aspose.com/) – General Aspose product releases.  
- [here](https://purchase.aspose.com/temporary-license/) – Obtain a temporary license for testing.  
- [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) – Community support and discussions.

## Conclusion

You’ve now mastered **how to set timeout** for saving CAD drawings with Aspose.CAD for Java. By integrating an `InterruptionTokenSource` into your workflow you can reliably **export CAD to PDF** or **convert DWG to PDF** without risking long‑running hangs, keeping your application responsive and scalable.

---

**Last Updated:** 2026-06-19  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Related Tutorials

- [Export DWG to PDF or Raster Using Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [Export Specific DWG Layout to PDF Using Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [Convert DWG to PNG and Other Raster Formats Using Aspose.CAD for Java](/cad/java/cad-drawing-conversion/convert-cad-layout-to-raster-image/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}