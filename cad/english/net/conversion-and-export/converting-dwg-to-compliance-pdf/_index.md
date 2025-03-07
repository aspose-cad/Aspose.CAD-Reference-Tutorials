---
title: Converting DWG to Compliance PDF - Aspose.CAD Tutorial
linktitle: Converting DWG to Compliance PDF
second_title: Aspose.CAD .NET - CAD and BIM File Format
description: Convert DWG to Compliance PDF with Aspose.CAD for .NET. Follow our tutorial for step-by-step guidance.
weight: 13
url: /net/conversion-and-export/converting-dwg-to-compliance-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Converting DWG to Compliance PDF - Aspose.CAD Tutorial

## Introduction

Welcome to our step-by-step tutorial on converting DWG files to Compliance PDF using Aspose.CAD for .NET. Aspose.CAD is a powerful .NET API that enables developers to work with CAD file formats effortlessly. In this tutorial, we'll guide you through the process of converting a DWG file to Compliance PDF with detailed examples and explanations.

## Prerequisites

Before we begin, ensure you have the following prerequisites in place:

- Aspose.CAD for .NET: Make sure you have the Aspose.CAD library integrated into your .NET project. You can download it [here](https://releases.aspose.com/cad/net/).

- Development Environment: Have a working .NET development environment installed, and ensure it's configured correctly.

- Sample DWG File: Download a sample DWG file that you want to convert to Compliance PDF.

## Import Namespaces

In your .NET project, import the necessary namespaces to utilize Aspose.CAD functionalities.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
```

Now, let's break down the process of converting a DWG file to Compliance PDF into multiple steps.

## Step 1: Load the DWG File

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";

Aspose.CAD.Image cadImage = Aspose.CAD.Image.Load(sourceFilePath);
```

## Step 2: Set Rasterization Options

Create an instance of `CadRasterizationOptions` and configure its properties, such as background color, page width, and page height.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions
{
    BackgroundColor = Aspose.CAD.Color.White,
    PageWidth = 1600,
    PageHeight = 1600
};
```

## Step 3: Create PDF Options

Create an instance of `PdfOptions` and set the vector rasterization options.

```csharp
PdfOptions pdfOptions = new PdfOptions
{
    VectorRasterizationOptions = rasterizationOptions,
    CorePdfOptions = new PdfDocumentOptions { Compliance = PdfCompliance.PdfA1a }
};
```

## Step 4: Save as PDF (A1a Compliance)

Save the CAD image as Compliance PDF with A1a compliance.

```csharp
cadImage.Save(MyDir + "PDFA1_A.pdf", pdfOptions);
```

## Step 5: Save as PDF (A1b Compliance)

Change the compliance type to A1b and save the CAD image as Compliance PDF.

```csharp
pdfOptions.CorePdfOptions.Compliance = PdfCompliance.PdfA1b;
cadImage.Save(MyDir + "PDFA1_B.pdf", pdfOptions);
```

## Conclusion

Congratulations! You have successfully converted a DWG file to Compliance PDF using Aspose.CAD for .NET. This tutorial provides a comprehensive guide for developers looking to integrate CAD conversion capabilities into their applications.

## FAQ's

### Q1: Can I convert other CAD formats to Compliance PDF using Aspose.CAD?

A1: Yes, Aspose.CAD supports various CAD formats, enabling conversion to Compliance PDF.

### Q2: Is Aspose.CAD compatible with .NET Core?

A2: Yes, Aspose.CAD is compatible with both .NET Framework and .NET Core.

### Q3: Are there any licensing options for Aspose.CAD?

A3: Yes, you can explore licensing options [here](https://purchase.aspose.com/buy).

### Q4: Is there a free trial available?

A4: Yes, you can get a free trial [here](https://releases.aspose.com/).

### Q5: Where can I get support for Aspose.CAD?

A5: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for any support-related queries.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
