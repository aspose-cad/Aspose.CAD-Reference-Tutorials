---
title: Export DGN to Raster Image in Aspose.CAD for .NET
linktitle: Export DGN to Raster Image
second_title: Aspose.CAD .NET - CAD and BIM File Format
description: Convert DGN to raster images effortlessly using Aspose.CAD for .NET. Explore step-by-step guide and unleash the power of .NET in CAD file manipulation.
weight: 13
url: /net/cad-export-formats/export-dgn-to-raster-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export DGN to Raster Image in Aspose.CAD for .NET

## Introduction

In the dynamic realm of .NET development, Aspose.CAD emerges as a powerful tool for handling Computer-Aided Design (CAD) files. This tutorial dives into the process of exporting DGN files to raster images using Aspose.CAD for .NET. If you're keen on transforming your DGN files into visually compelling raster images seamlessly, you're in the right place.

## Prerequisites

Before we embark on this journey, make sure you have the following prerequisites in place:

- Aspose.CAD for .NET: Ensure you have the Aspose.CAD library installed in your .NET project. You can find the library and relevant documentation on the [website](https://reference.aspose.com/cad/net/).

- Sample DGN File: Have a DGN file ready for conversion. In our example, we'll use "Nikon_D90_Camera.dgn."

Now, let's dive into the step-by-step guide.

## Import Namespaces

In your .NET project, begin by importing the necessary namespaces for Aspose.CAD. This step allows you to access the classes and methods required for DGN to raster image conversion.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Step 1: Load DGN File

Start by loading the DGN file into a `CadImage` object. This provides a foundation for subsequent operations.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Your code for further processing goes here
}
```

## Step 2: Define Rasterization Options

Create a `CadRasterizationOptions` object and set various properties to customize the rasterization process according to your requirements.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 600;
rasterizationOptions.PageHeight = 300;
rasterizationOptions.NoScaling = true;
rasterizationOptions.AutomaticLayoutsScaling = false;
```

## Step 3: Create JpegOptions Object

Since we aim to convert the DGN file to JPEG, create a `JpegOptions` object and assign the previously defined `CadRasterizationOptions` to it.

```csharp
ImageOptionsBase options = new JpegOptions();
options.VectorRasterizationOptions = rasterizationOptions;
```

## Step 4: Save the Raster Image

Utilize the `Save` method of the `CadImage` class to export the DGN file to a raster image in the desired format, in this case, a JPEG.

```csharp
cadImage.Save(MyDir + "ExportDGNToRasterImage_out.jpg", options);
```

## Conclusion

Congratulations! You've successfully navigated through the steps to export a DGN file to a raster image using Aspose.CAD for .NET. This tutorial has equipped you with the essential knowledge to integrate this functionality into your .NET projects effortlessly.

## FAQ's

### Q1: Can I export DGN files to formats other than JPEG?

A1: Yes, Aspose.CAD for .NET supports various output formats. You can modify the options accordingly in Step 3.

### Q2 How can I handle exceptions during the conversion process?

A2: Ensure you have proper exception handling, as demonstrated in the provided code, to address potential issues.

### Q3: Is there a trial version available for Aspose.CAD for .NET?

A3: Yes, you can explore the product with a free trial. Visit [here](https://releases.aspose.com/) for more information.

### Q4: Where can I seek assistance or discuss issues related to Aspose.CAD for .NET?

A4: Head over to the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for community support and discussions.

### Q5: How do I obtain a temporary license for Aspose.CAD for .NET?

A5: Visit [this link](https://purchase.aspose.com/temporary-license/) to acquire a temporary license for your development needs.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
