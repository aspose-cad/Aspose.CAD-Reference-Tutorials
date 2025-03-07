---
title: Working with DWG Files in C# - Get Size of DWF Layout
linktitle: Working with DWG Files in C# - Get Size of DWF Layout
second_title: Aspose.CAD .NET - CAD and BIM File Format
description: Explore the power of Aspose.CAD for .NET in handling DWG files. Learn to extract DWF layout sizes effortlessly using C#.
weight: 10
url: /net/dwg-file-manipulation/get-size-of-dwf-layout/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Working with DWG Files in C# - Get Size of DWF Layout

## Introduction

In the realm of computer-aided design (CAD) and .NET development, Aspose.CAD stands as a powerful tool for handling DWG files. This tutorial will guide you through the process of working with DWG files in C# and extracting the size of a DWF layout. Before we dive into the code, let's ensure you have everything set up to embark on this journey.

## Prerequisites

To follow this tutorial seamlessly, make sure you have the following prerequisites in place:

- Aspose.CAD for .NET: Ensure that you have Aspose.CAD for .NET installed. You can download it from the [Aspose.CAD for .NET download page](https://releases.aspose.com/cad/net/).

Now that you have the necessary tools, let's jump into the coding arena.

## Import Namespaces

Before we start working with the code, let's import the required namespaces:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Dwf;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

These namespaces will provide the essential classes and methods for handling CAD files with Aspose.CAD in your C# application.

## Step 1: Set Up Your Environment

Begin by ensuring you have the correct environment set up for your project. Reference the Aspose.CAD library in your C# project.

## Step 2: Define File Paths

Define the paths for your DWG file and the output directory for the generated JPG files:

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "blocks_and_tables.dwf";
```

## Step 3: Load the DWF Image

Load the DWF image using Aspose.CAD:

```csharp
using (DwfImage image = (DwfImage)Aspose.CAD.Image.Load(sourceFilePath))
{
    // Code for further steps will go here
}
```

## Step 4: Iterate Through Pages

Iterate through the pages of the DWF image:

```csharp
foreach (var page in image.Pages)
{
    // Code for further steps will go here
}
```

## Step 5: Get Layout Information

Get layout information from each page:

```csharp
var layout = page.Name;
System.Console.WriteLine("Layout= " + layout);
```

## Step 6: Set Up JPG Options

Set up options for saving the layout as a JPG file:

```csharp
using (FileStream fs = new FileStream(MyDir + "layout_" + layout + ".jpg", FileMode.Create))
{
    JpegOptions jpegOptions = new JpegOptions();
    CadRasterizationOptions options = new CadRasterizationOptions();
    options.Layouts = new string[] { layout };
    // Code for further steps will go here
}
```

## Step 7: Determine Page Size

Determine the size of the DWF layout:

```csharp
double sizeExtX = page.MaxPoint.X - page.MinPoint.X;
double sizeExtY = page.MaxPoint.Y - page.MinPoint.Y;
// Code for further steps will go here
```

## Step 8: Set Up Page Dimensions

Set up the page dimensions based on the unit type:

```csharp
if (page.UnitType == UnitType.Inch)
{
    options.PageHeight = CommonHelper.INtoPixels(sizeExtY, CommonHelper.DPI);
    options.PageWidth = CommonHelper.INtoPixels(sizeExtX, CommonHelper.DPI);
}
else if (page.UnitType == UnitType.Millimeter)
{
    options.PageHeight = CommonHelper.MMtoPixels(sizeExtY, CommonHelper.DPI);
    options.PageWidth = CommonHelper.MMtoPixels(sizeExtX, CommonHelper.DPI);
}
else
{
    options.PageHeight = (float)sizeExtY;
    options.PageWidth = (float)sizeExtX;
}
```

## Step 9: Save the JPG File

Save the JPG file with the specified options:

```csharp
jpegOptions.VectorRasterizationOptions = options;
image.Save(fs, jpegOptions);
}
```

Now you have successfully extracted the size of the DWF layout from the DWG file using Aspose.CAD in C#. Feel free to explore more features and functionalities that Aspose.CAD offers for .NET development.

## Conclusion

In this tutorial, we've walked through the process of working with DWG files in C# using Aspose.CAD. By following these steps, you can not only get the size of a DWF layout but also leverage the capabilities of Aspose.CAD for various CAD-related tasks in your .NET projects.

## FAQ's

### Q1: Is Aspose.CAD compatible with the latest DWG file formats?

A1: Aspose.CAD supports various DWG file formats, including the latest versions. Refer to the [documentation](https://reference.aspose.com/cad/net/) for specific compatibility details.

### Q2: Can I use Aspose.CAD for both commercial and personal projects?

A2: Yes, Aspose.CAD offers flexible licensing options for both commercial and personal use. Visit the [purchase page](https://purchase.aspose.com/buy) for more details.

### Q3: How can I obtain a temporary license for Aspose.CAD?

A3: You can get a temporary license from [here](https://purchase.aspose.com/temporary-license/) for evaluation purposes.

### Q4: Where can I find support for Aspose.CAD?

A4: For any queries or assistance, visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19).

### Q5: Is there a free trial available for Aspose.CAD?

A5: Yes, you can access a free trial version of Aspose.CAD [here](https://releases.aspose.com/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
