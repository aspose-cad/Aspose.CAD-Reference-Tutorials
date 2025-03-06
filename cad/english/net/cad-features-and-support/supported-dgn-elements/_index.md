---
title: Supported DGN Elements in Aspose.CAD for .NET
linktitle: Supported DGN Elements
second_title: Aspose.CAD .NET - CAD and BIM File Format
description: Explore Aspose.CAD for .NET's powerful features for handling DGN files. Follow our step-by-step guide to work seamlessly with 2D and 3D elements.
weight: 18
url: /net/cad-features-and-support/supported-dgn-elements/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Supported DGN Elements in Aspose.CAD for .NET

## Introduction

Are you a .NET developer looking to work with DGN files seamlessly? Aspose.CAD for .NET provides a robust solution to handle DGN files efficiently. In this tutorial, we will delve into the supported DGN elements, guiding you through the process of working with Aspose.CAD for .NET.

## Prerequisites

Before we begin, make sure you have the following:

- Basic knowledge of .NET programming.
- Visual Studio installed on your machine.
- Aspose.CAD for .NET library, which you can download [here](https://releases.aspose.com/cad/net/).

## Import Namespaces

To kickstart your project, import the necessary namespaces into your .NET application. This step ensures that you have access to the functionalities provided by Aspose.CAD for .NET.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Dgn;
using Aspose.CAD.FileFormats.Dgn.DgnElements;
```

## Step 1: Load the DGN File

Begin by loading an existing DGN file as a CadImage in your .NET application.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Your code here
}
```

## Step 2: Iterate Through DGN Elements

Iterate through the DGN elements using a foreach loop. Aspose.CAD for .NET provides a variety of DGN element types that you can work with.

```csharp
foreach (DgnDrawingElementBase element in dgnImage.Elements)
{
    // Your code here
}
```

## Step 3: Handle Previously Supported Entities

Handle the previously supported 2D entities, which are now also supported for 3D.

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.Line:
    case DgnElementType.Ellipse:
    case DgnElementType.Curve:
    // Additional cases
        {
            // Your code here
            break;
        }
}
```

## Step 4: Handle Supported 3D Entities

Handle the supported 3D entities provided by Aspose.CAD for .NET.

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.SolidHeader3D:
    case DgnElementType.Cone:
    case DgnElementType.CellHeader:
        {
            // Your code here
            break;
        }
}
```

## Step 5: Export and Save

Finally, export the modified DGN file to a raster image and save it to the specified directory.

```csharp
Console.WriteLine("\nThe DGN file exported successfully to raster image.\nFile saved at " + MyDir);
```

## Conclusion

In this tutorial, we explored the capabilities of Aspose.CAD for .NET in handling and manipulating DGN files. By following the step-by-step guide, you can efficiently work with supported DGN elements, whether they are 2D or 3D entities. Aspose.CAD for .NET empowers you to seamlessly integrate DGN file processing into your .NET applications.

## FAQ's

### Q1: Where can I find the documentation for Aspose.CAD for .NET?

A1: You can find the documentation [here](https://reference.aspose.com/cad/net/).

### Q2: How do I download Aspose.CAD for .NET?

A2: You can download the library [here](https://releases.aspose.com/cad/net/).

### Q3: Is there a free trial available for Aspose.CAD for .NET?

A3: Yes, you can access the free trial [here](https://releases.aspose.com/).

### Q4: Where can I get temporary licenses for Aspose.CAD for .NET?

A4: Temporary licenses are available [here](https://purchase.aspose.com/temporary-license/).

### Q5: Need help or have questions?

A5: Visit the Aspose.CAD for .NET community [support forum](https://forum.aspose.com/c/cad/19).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
