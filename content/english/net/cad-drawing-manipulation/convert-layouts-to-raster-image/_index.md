---
title: Convert Layouts to Raster Image in Aspose.CAD for .NET
linktitle: Convert Layouts to Raster Image
second_title: Aspose.CAD .NET - CAD and BIM File Format
description: Effortlessly convert CAD layouts to raster images using Aspose.CAD for .NET. Enhance your development with powerful CAD manipulation capabilities.
type: docs
weight: 12
url: /net/cad-drawing-manipulation/convert-layouts-to-raster-image/
---
## Introduction

Are you looking to effortlessly convert layouts to raster images in your .NET applications? Look no further! This step-by-step guide will walk you through the process using Aspose.CAD for .NET, a powerful library that simplifies Computer-Aided Design (CAD) tasks.

## Prerequisites

Before diving into the tutorial, ensure you have the following prerequisites in place:

- Aspose.CAD for .NET Library: Download and install the library from the [Aspose.CAD for .NET download page](https://releases.aspose.com/cad/net/).

- Development Environment: Make sure you have a working .NET development environment set up on your machine.

- Document to Convert: Prepare a CAD document that contains the layouts you want to convert to raster images.

- Your Document Directory: Replace the placeholder "Your Document Directory" in the code with the path to your document directory.

## Import Namespaces

Firstly, let's import the necessary namespaces to make the Aspose.CAD functionalities accessible in your code.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Step 1: Load the CAD Document

Begin by loading the CAD document using the Aspose.CAD library.

```csharp
string sourceFilePath = MyDir + "conic_pyramid.dxf";
using (Image image = Image.Load(sourceFilePath))
{
    // Your code for further steps will go here
}
```

## Step 2: Configure Rasterization Options

Create an instance of `CadRasterizationOptions` to set the page width, height, and specify the layouts you want to convert.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1200;
rasterizationOptions.PageHeight = 1200;
rasterizationOptions.Layouts = new string[] { "Model", "Layout1" };
```

## Step 3: Set Up TiffOptions for Resultant Image

Create an instance of `TiffOptions` to define the format of the resultant image.

```csharp
ImageOptionsBase options = new TiffOptions(TiffExpectedFormat.Default);
options.VectorRasterizationOptions = rasterizationOptions;
```

## Step 4: Save the Resultant Image

Specify the output path and save the converted image.

```csharp
string outputFilePath = MyDir + "conic_pyramid_layoutstorasterimage_out.tiff";
image.Save(outputFilePath, options);
```

## Conclusion

Congratulations! You've successfully converted CAD layouts to a raster image format using Aspose.CAD for .NET. The possibilities are vast, and this guide serves as a starting point for your CAD-related endeavors.

## FAQ's

### Q1: Is Aspose.CAD compatible with all CAD formats?

A1: Aspose.CAD supports a wide range of CAD formats, including DWG, DXF, DWF, STL, and more. Check the [documentation](https://reference.aspose.com/cad/net/) for a comprehensive list.

### Q2: How can I obtain a temporary license for Aspose.CAD?

A2: Visit the [temporary license page](https://purchase.aspose.com/temporary-license/) to acquire a temporary license for testing and evaluation purposes.

### Q3: Where can I find support for Aspose.CAD?

A3: Forums are a great place to seek assistance. Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) to connect with the community and get help.

### Q4: Can I try Aspose.CAD for free?

A4: Absolutely! Grab your [free trial](https://releases.aspose.com/) to explore the features and capabilities of Aspose.CAD.

### Q5: Where can I purchase a license for Aspose.CAD?

A5: Navigate to the [purchase page](https://purchase.aspose.com/buy) to buy a license and unlock the full potential of Aspose.CAD.
