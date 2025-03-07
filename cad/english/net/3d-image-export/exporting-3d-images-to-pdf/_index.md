---
title: Exporting 3D Images to PDF - Aspose.CAD Tutorial
linktitle: Exporting 3D Images to PDF
second_title: Aspose.CAD .NET - CAD and BIM File Format
description: Effortlessly convert 3D CAD images to PDF with Aspose.CAD for .NET. Follow our step-by-step tutorial for seamless PDF export.
weight: 10
url: /net/3d-image-export/exporting-3d-images-to-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exporting 3D Images to PDF - Aspose.CAD Tutorial

## Introduction

Are you looking to seamlessly export 3D images to PDF using Aspose.CAD for .NET? This step-by-step tutorial will guide you through the process, ensuring that you harness the power of Aspose.CAD to effortlessly convert your 3D images to PDF format.

## Prerequisites

Before diving into the tutorial, make sure you have the following prerequisites in place:

- Aspose.CAD for .NET: Ensure that you have the Aspose.CAD library for .NET installed. If not, you can download it from the [Aspose.CAD for .NET download page](https://releases.aspose.com/cad/net/).

- Document Directory: Set up a directory where your CAD files are stored, and note down the path.

## Import Namespaces

In your .NET project, import the necessary namespaces for working with Aspose.CAD. Add the following lines to the top of your code file:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
```

## Step 1: Load the CAD Image

Begin by loading the CAD image you want to export to PDF. Use the `Load` method from the Aspose.CAD library. Replace `"conic_pyramid.dxf"` with the path to your CAD file.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";
using (Image cadImage = Image.Load(sourceFilePath))
{
    // Your code for loading the CAD image goes here
}
```

## Step 2: Configure Rasterization Options

Configure the rasterization options for the CAD image. Set parameters such as page width, page height, and layouts. Uncomment the line related to `TypeOfEntities` if your entities are 3D.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
// rasterizationOptions.TypeOfEntities = TypeOfEntities.Entities3D;

rasterizationOptions.Layouts = new string[] { "Model" };
```

## Step 3: Set PDF Options

Create PDF options and associate them with the rasterization options.

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Step 4: Save as PDF

Save the CAD image as a PDF file using the configured options. Specify the output path for the PDF file.

```csharp
MyDir = MyDir + "Export3DImagestoPDF_out.pdf";
cadImage.Save(MyDir, pdfOptions);
```

## Conclusion

Congratulations! You've successfully exported 3D images to PDF using Aspose.CAD for .NET. This straightforward tutorial ensures that you effortlessly convert your CAD files into a more accessible format.

## FAQ's

### Q1: Is Aspose.CAD compatible with all CAD file formats?

A1: Yes, Aspose.CAD supports a wide range of CAD formats, ensuring flexibility in handling various file types.

### Q2: Can I customize the page dimensions when exporting to PDF?

A2: Absolutely. The tutorial demonstrates how to configure page width and height according to your requirements.

### Q3: Are temporary licenses available for Aspose.CAD?

A3: Yes, you can obtain temporary licenses for Aspose.CAD by visiting [Temporary License](https://purchase.aspose.com/temporary-license/).

### Q4: Where can I find additional support or community discussions?

A4: Head to the [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19) for support and engaging with the community.

### Q5: Is there a free trial version of Aspose.CAD available?

A5: Yes, you can explore the features of Aspose.CAD by accessing the [free trial](https://releases.aspose.com/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
