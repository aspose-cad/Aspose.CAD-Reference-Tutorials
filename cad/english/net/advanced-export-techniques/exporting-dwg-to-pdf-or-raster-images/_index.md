---
title: Exporting DWG to PDF or Raster Images - Aspose.CAD Guide
linktitle: Exporting DWG to PDF or Raster Images
second_title: Aspose.CAD .NET - CAD and BIM File Format
description: Explore a comprehensive guide on exporting DWG to PDF or raster images using Aspose.CAD for .NET. Learn the steps, prerequisites, and get hands-on with this powerful library.
weight: 11
url: /net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exporting DWG to PDF or Raster Images - Aspose.CAD Guide

## Introduction

Are you looking to seamlessly convert DWG files to PDF or raster images in your .NET application? Look no further! This step-by-step guide will walk you through the process using the powerful Aspose.CAD for .NET library. Whether you're a seasoned developer or just starting, this tutorial caters to all skill levels.

## Prerequisites

Before we dive into the tutorial, make sure you have the following in place:

- A basic understanding of .NET programming.
- Aspose.CAD for .NET library installed. If not, download it [here](https://releases.aspose.com/cad/net/).
- Your favorite integrated development environment (IDE) set up for .NET development.

## Import Namespaces

Let's kick things off by importing the necessary namespaces in your .NET project. This ensures that you have access to the Aspose.CAD functionality in your code.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
```

## Step 1: Load DWG File

Begin by loading the DWG file you wish to convert. Replace "Your Document Directory" with the path to your DWG file.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Your code for loading DWG goes here
}
```

## Step 2: Set up PDF Export

Now, let's configure the PDF export settings. This example demonstrates how to set the layout and handle unit conversions.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new string[] { "Model" };

// Check and define the unit system
bool currentUnitIsMetric = false;
double currentUnitCoefficient = 1.0;
DefineUnitSystem(cadImage.UnitType, out currentUnitIsMetric, out currentUnitCoefficient);

// Your code for setting up PDF export goes here
```

## Step 3: Export to PDF

Execute the export to PDF using the configured settings.

```csharp
PdfOptions pdfOptions = new PdfOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath, pdfOptions);
```

## Step 4: Export to Raster Images

Extend the functionality to export to raster images, such as PNG.

```csharp
// A4 size at 300 DPI - 2480 x 3508
rasterizationOptions.PageHeight = 3508;
rasterizationOptions.PageWidth = 2480;

PngOptions pngOptions = new PngOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath.Replace("pdf", "png"), pngOptions);
```

## Conclusion

Congratulations! You've successfully learned how to use Aspose.CAD for .NET to export DWG files to both PDF and raster images. This powerful library streamlines the process, making it efficient and developer-friendly.

## FAQ's

### Q1: Can I use Aspose.CAD for .NET in my commercial projects?

A1: Yes, you can. Visit [purchase.aspose.com/buy](https://purchase.aspose.com/buy) for licensing details.

### Q2: Is there a free trial available?

A2: Certainly! Grab your free trial [here](https://releases.aspose.com/).

### Q3: How can I get support for Aspose.CAD for .NET?

A3: Head over to the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for community support.

### Q4: Can I obtain a temporary license for testing purposes?

A4: Yes, you can get a temporary license [here](https://purchase.aspose.com/temporary-license/).

### Q5: Where can I find the detailed documentation?

A5: The documentation is available at [Aspose.CAD](https://reference.aspose.com/cad/net/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
