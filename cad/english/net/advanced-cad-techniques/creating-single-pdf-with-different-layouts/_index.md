---
title: Creating Single PDF with Different Layouts - Aspose.CAD Guide
linktitle: Creating Single PDF with Different Layouts
second_title: Aspose.CAD .NET - CAD and BIM File Format
description: Create a single PDF with different layouts using Aspose.CAD for .NET. Follow our step-by-step guide for seamless integration and efficient PDF generation.
type: docs
weight: 13
url: /net/advanced-cad-techniques/creating-single-pdf-with-different-layouts/
---
## Introduction

Are you looking to generate a single PDF document from a CAD drawing with different layouts using Aspose.CAD for .NET? This step-by-step guide will walk you through the process, helping you achieve seamless integration and efficient PDF creation. Aspose.CAD for .NET provides powerful features to manipulate CAD drawings programmatically, and in this tutorial, we will focus on creating a single PDF with different layouts.

## Prerequisites

Before diving into the tutorial, ensure you have the following prerequisites:

- Aspose.CAD for .NET: Make sure you have Aspose.CAD for .NET installed. You can download it from [here](https://releases.aspose.com/cad/net/).

- Development Environment: Set up a .NET development environment, and have a basic understanding of C# programming.

## Import Namespaces

In your C# project, include the necessary namespaces to leverage the functionalities of Aspose.CAD for .NET:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Step 1: Load the CAD Image

```csharp
// The path to the documents directory.
string MyDir = "Your Document Directory";

using (CadImage cadImage = (CadImage)Image.Load(MyDir + "City skyway map.dwg"))
{
    // Your code for Step 1 goes here
}
```

## Step 2: Customize Rasterization Options

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1000;
rasterizationOptions.PageHeight = 1000;

// Custom sizes for several layouts
rasterizationOptions.LayoutPageSizes.Add("ANSI C Plot", new SizeF(500, 1000));
rasterizationOptions.LayoutPageSizes.Add("8.5 x 11 Plot", new SizeF(1000, 100));
```

## Step 3: Define PDF Options

```csharp
PdfOptions pdfOptions = new PdfOptions() { VectorRasterizationOptions = rasterizationOptions };
```

## Step 4: Save as PDF

```csharp
cadImage.Save(MyDir + "singlePDF_out.pdf", pdfOptions);
```

Now you have successfully created a single PDF document with different layouts using Aspose.CAD for .NET. Feel free to explore more features and customize the code according to your specific requirements.

## Conclusion

In this tutorial, we covered the process of creating a single PDF from a CAD drawing with different layouts using Aspose.CAD for .NET. This powerful library simplifies CAD manipulation tasks and offers flexibility for various scenarios.

## FAQ's

### Q1: Can I use Aspose.CAD for .NET with other CAD formats?

A1: Yes, Aspose.CAD for .NET supports various CAD formats such as DWG, DXF, DGN, and more.

### Q2: Is there a free trial available?

A2: Yes, you can explore a free trial [here](https://releases.aspose.com/).

### Q3: How can I get support for Aspose.CAD for .NET?

A3: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for community support.

### Q4: Where can I find detailed documentation?

A4: Refer to the documentation [here](https://reference.aspose.com/cad/net/).

### Q5: Can I purchase a license for Aspose.CAD for .NET?

A5: Yes, you can buy a license [here](https://purchase.aspose.com/buy).
