---
title: Adjusting CAD Drawing Size in Aspose.CAD for .NET
linktitle: Adjusting CAD Drawing Size
second_title: Aspose.CAD .NET - CAD and BIM File Format
description: Learn how to effortlessly adjust CAD drawing sizes in .NET using Aspose.CAD. Follow our step-by-step guide for seamless resizing.
type: docs
weight: 10
url: /net/cad-drawing-manipulation/adjust-cad-drawing-size/
---
## Introduction

Are you looking to seamlessly adjust the size of CAD drawings in your .NET applications? Aspose.CAD for .NET provides a robust solution, allowing you to effortlessly handle CAD drawing resizing. In this tutorial, we'll guide you through the process, breaking down each step to ensure you grasp the intricacies of resizing CAD drawings using Aspose.CAD.

## Prerequisites

Before we dive into the tutorial, make sure you have the following prerequisites in place:

- Aspose.CAD for .NET Library: Download and install the library from the [Aspose.CAD for .NET download page](https://releases.aspose.com/cad/net/).
- Sample CAD Drawing: Ensure you have a sample CAD drawing file (e.g., "sample.dwg") in your document directory.

## Import Namespaces

Begin by importing the necessary namespaces into your .NET application. This step is crucial to access the functionalities provided by Aspose.CAD for .NET.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Step 1: Load CAD Drawing

Start by loading the CAD drawing into an instance of the Aspose.CAD.Image class. Ensure you have the correct file path for your sample drawing.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "sample.dwg";

// Load a CAD drawing in an instance of Image
using (var image = Aspose.CAD.Image.Load(sourceFilePath))
{
    // Your code here...
}
```

## Step 2: Create BmpOptions

Create an instance of the BmpOptions class, which is responsible for specifying options when saving the CAD drawing as a BMP file.

```csharp
Aspose.CAD.ImageOptions.BmpOptions bmpOptions = new Aspose.CAD.ImageOptions.BmpOptions();
```

## Step 3: Set CadRasterizationOptions

Instantiate the CadRasterizationOptions class and configure its properties for vector rasterization.

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions cadRasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
bmpOptions.VectorRasterizationOptions = cadRasterizationOptions;
```

## Step 4: Set UnitType Property

Set the UnitType property of CadRasterizationOptions to specify the unit type for resizing. In this example, it is set to Centimeter.

```csharp
cadRasterizationOptions.UnitType = Aspose.CAD.ImageOptions.UnitType.Centimeter;
```

## Step 5: Set Layouts Property

Specify the layouts you want to include in the resized drawing by setting the Layouts property.

```csharp
cadRasterizationOptions.Layouts = new string[] { "Model" };
```

## Step 6: Export to BMP

Finally, save the resized layout as a BMP file using the Save method.

```csharp
string outPath = sourceFilePath + ".bmp";
image.Save(outPath, bmpOptions);
```

Now you have successfully adjusted the size of your CAD drawing using Aspose.CAD for .NET!

## Conclusion

In this tutorial, we walked through the process of resizing CAD drawings in .NET using Aspose.CAD. By following these steps, you can seamlessly integrate this functionality into your applications, providing a smooth user experience.

## FAQs

### Q1: Is Aspose.CAD for .NET compatible with all CAD formats?

A1: Aspose.CAD for .NET supports a wide range of CAD formats, including DWG, DXF, DWF, and more. Check the [documentation](https://reference.aspose.com/cad/net/) for the complete list.

### Q2: Can I resize multiple layouts simultaneously?

A2: Yes, you can resize multiple layouts by adjusting the layouts array in the CadRasterizationOptions.

### Q3: Where can I get support for Aspose.CAD for .NET?

A3: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for community support and assistance.

### Q4: Is there a free trial available?

A4: Yes, you can explore a [free trial](https://releases.aspose.com/) to evaluate the features of Aspose.CAD for .NET.

### Q5: How can I obtain a temporary license for Aspose.CAD for .NET?

A5: Obtain a temporary license for testing purposes [here](https://purchase.aspose.com/temporary-license/).
