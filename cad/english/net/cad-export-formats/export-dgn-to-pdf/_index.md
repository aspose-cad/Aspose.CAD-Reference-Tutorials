---
title: Export DGN to PDF in Aspose.CAD for .NET
linktitle: Export DGN to PDF
second_title: Aspose.CAD .NET - CAD and BIM File Format
description: Learn how to export DGN files to PDF effortlessly with Aspose.CAD for .NET. A step-by-step guide for seamless CAD file manipulation.
weight: 12
url: /net/cad-export-formats/export-dgn-to-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export DGN to PDF in Aspose.CAD for .NET

## Introduction

In the world of .NET development, Aspose.CAD is a powerful library that facilitates the manipulation and conversion of CAD files. One common task developers often encounter is exporting DGN files to PDF format. In this tutorial, we'll walk through the process step by step, using Aspose.CAD for .NET.

## Prerequisites

Before diving into the tutorial, ensure you have the following in place:

- A working knowledge of C# and the .NET framework.
- Aspose.CAD for .NET library installed. You can download it [here](https://releases.aspose.com/cad/net/).
- A sample DGN file, for instance, "Nikon_D90_Camera.dgn" for this tutorial.

## Import Namespaces

In your C# project, begin by importing the necessary namespaces:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Step 1: Load DGN File

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage cadImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Your code here...
}
```

## Step 2: Configure Rasterization Options

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 600;
rasterizationOptions.PageHeight = 300;
rasterizationOptions.NoScaling = true;
rasterizationOptions.AutomaticLayoutsScaling = false;
```

## Step 3: Create PDF Options

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Step 4: Save as PDF

```csharp
cadImage.Save(MyDir + "ExportDGNToPdf_out.pdf", pdfOptions);
```

## Conclusion

Congratulations! You've successfully exported a DGN file to PDF using Aspose.CAD for .NET. This tutorial covered the essential steps, from loading the DGN file to configuring rasterization options and saving the output as a PDF.

## FAQ's

### Q1: Can I use Aspose.CAD for .NET without prior CAD knowledge?

A1: Absolutely! Aspose.CAD simplifies complex CAD tasks, making it accessible for developers with diverse backgrounds.

### Q2: Where can I find more examples and documentation for Aspose.CAD?

A2: Explore the [documentation](https://reference.aspose.com/cad/net/) for comprehensive guides and examples.

### Q3: Is there a free trial available for Aspose.CAD?

A3: Yes, you can get a free trial [here](https://releases.aspose.com/).

### Q4: How can I get temporary licenses for Aspose.CAD?

A4: Obtain temporary licenses [here](https://purchase.aspose.com/temporary-license/).

### Q5: Need help or have questions?

A5: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for community support.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
