---
title: Setting Canvas Size and Mode in Aspose.CAD for .NET
linktitle: Setting Canvas Size and Mode
second_title: Aspose.CAD .NET - CAD and BIM File Format
description: Explore the step-by-step guide on setting canvas size and mode in Aspose.CAD for .NET. Optimize your CAD rendering with ease using this comprehensive tutorial.
weight: 16
url: /net/cad-features-and-support/setting-canvas-size-and-mode/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Setting Canvas Size and Mode in Aspose.CAD for .NET

## Introduction

Are you ready to unlock the full potential of Aspose.CAD for .NET and revolutionize your CAD rendering experience? In this step-by-step tutorial, we'll delve into the intricacies of setting canvas size and mode using the powerful Aspose.CAD library. Whether you're a seasoned developer or just starting, this guide will walk you through the process, ensuring you harness the capabilities of Aspose.CAD effectively.

## Prerequisites

Before we dive into the tutorial, make sure you have the following prerequisites in place:

- Aspose.CAD Library: Download and install the Aspose.CAD library from the [Aspose.CAD website](https://releases.aspose.com/cad/net/).

- Development Environment: Ensure you have a .NET development environment set up on your machine.

- Sample CAD File: For this tutorial, we'll use a sample DXF file. You can find one in the [Aspose.CAD documentation](https://reference.aspose.com/cad/net/).

## Import Namespaces

To get started, import the necessary namespaces at the beginning of your .NET application:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Step 1: Load CAD File

Begin by loading the CAD file using the following code:

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (Image image = Image.Load(sourceFilePath))
{
    // Your code for further steps will go here
}
```

## Step 2: Create CadRasterizationOptions

Create an instance of `CadRasterizationOptions` and set its properties:

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.AutomaticLayoutsScaling = true;
rasterizationOptions.NoScaling = false;
```

## Step 3: Create PdfOptions

Create an instance of `PdfOptions` and set its `VectorRasterizationOptions` property:

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Step 4: Export to PDF

Export the CAD file to PDF using the configured options:

```csharp
image.Save(MyDir + "result_out.pdf", pdfOptions);
```

## Step 5: Create TiffOptions

Create an instance of `TiffOptions` and set its `VectorRasterizationOptions` property:

```csharp
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Step 6: Export to TIFF

Export the CAD file to TIFF using the configured options:

```csharp
image.Save(MyDir + "result_out.tiff", tiffOptions);
```

## Conclusion

Congratulations! You've successfully set the canvas size and mode in Aspose.CAD for .NET. This powerful feature opens up a world of possibilities for CAD rendering. Experiment with different options and discover the full potential of Aspose.CAD in your .NET applications.

## FAQ's

### Q1: Can I use Aspose.CAD with other .NET libraries?

A1: Yes, Aspose.CAD seamlessly integrates with other .NET libraries, providing enhanced capabilities for CAD manipulation.

### Q2: Is a free trial available for Aspose.CAD?

A2: Yes, you can explore the features of Aspose.CAD with a free trial. Visit [here](https://releases.aspose.com/) to get started.

### Q3: How can I get support for Aspose.CAD?

A3: For support and discussions, visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19).

### Q4: Where can I find comprehensive documentation for Aspose.CAD?

A4: Refer to the [Aspose.CAD documentation](https://reference.aspose.com/cad/net/) for detailed information and examples.

### Q5: How do I purchase Aspose.CAD for .NET?

A5: To purchase Aspose.CAD, visit the [purchase page](https://purchase.aspose.com/buy).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
