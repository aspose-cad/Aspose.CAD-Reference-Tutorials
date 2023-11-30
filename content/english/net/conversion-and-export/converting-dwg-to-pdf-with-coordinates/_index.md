---
title: Converting DWG to PDF with Coordinates in C# - Aspose.CAD Tutorial
linktitle: Converting DWG to PDF with Coordinates in C#
second_title: Aspose.CAD .NET - CAD and BIM File Format
description: Learn how to convert DWG to PDF with specific coordinates in C# using Aspose.CAD. Follow our step-by-step guide for precise and efficient CAD file conversions.
type: docs
weight: 11
url: /net/conversion-and-export/converting-dwg-to-pdf-with-coordinates/
---
## Introduction

Welcome to this comprehensive tutorial on converting DWG files to PDF with specified coordinates using Aspose.CAD for .NET. Aspose.CAD is a powerful library that allows developers to work with CAD file formats in their .NET applications seamlessly. In this tutorial, we'll walk you through the process of converting a DWG file to PDF while providing specific coordinates to enhance precision.

## Prerequisites

Before we begin, make sure you have the following prerequisites:

- Aspose.CAD Library: Download and install the Aspose.CAD library for .NET. You can find the library [here](https://releases.aspose.com/cad/net/).

- Development Environment: Ensure that you have a compatible development environment set up, including Visual Studio or any other preferred IDE.

- DWG File: Have a DWG file ready for conversion. You can use the provided example file or your custom DWG file.

## Import Namespaces

In your C# project, import the necessary namespaces:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadParameters;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.ImageOptions;
```

Let's break down the code into a step-by-step guide for a better understanding:

## Step 1: Define the Document Directory

```csharp
string MyDir = "Your Document Directory";
```

## Step 2: Set the Source DWG File Path

```csharp
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";
```

## Step 3: Load DWG File and Configure Rasterization Options

```csharp
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
    rasterizationOptions.Layouts = new string[] { "Model" };
    rasterizationOptions.NoScaling = true;
```

## Step 4: Define Coordinates and Viewport

```csharp
    Point topLeft = new Point(500, 1000);
    double width = 3108;
    double height = 2489;

    CadVportTableObject newView = new CadVportTableObject();
    newView.Name = new CadStringParameter();
    newView.Name.Init("*Active");
    newView.CenterPoint.X = topLeft.X + width / 2f;
    newView.CenterPoint.Y = topLeft.Y - height / 2f;
    newView.ViewHeight.Value = height;
    newView.ViewAspectRatio.Value = width / height;
```

## Step 5: Apply Viewport Settings

```csharp
    for (int i = 0; i < cadImage.ViewPorts.Count; i++)
    {
        CadVportTableObject currentView = (CadVportTableObject)(cadImage.ViewPorts[i]);
        if (cadImage.ViewPorts.Count == 1 || string.Equals(currentView.Name.Value.ToLowerInvariant(), "*active"))
        {
            cadImage.ViewPorts[i] = newView;
            break;
        }
    }
```

## Step 6: Configure PDF Options and Export

```csharp
    Aspose.CAD.ImageOptions.PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions();
    pdfOptions.VectorRasterizationOptions = rasterizationOptions;

    MyDir = MyDir + "ConvertDWGToPDFBySupplyingCoordinates_out.pdf";
    cadImage.Save(MyDir, pdfOptions);
}
```

## Step 7: Display Success Message

```csharp
Console.WriteLine("\nThe DWG file exported successfully to PDF.\nFile saved at " + MyDir);
```

## Conclusion

Congratulations! You've successfully converted a DWG file to PDF with specified coordinates using Aspose.CAD for .NET. This tutorial covered essential steps and provided a clear guide for developers.

## FAQ's

### Q1: Can I use Aspose.CAD with other CAD file formats?

A1: Yes, Aspose.CAD supports various CAD formats, including DWG, DXF, DWF, and more.

### Q2: How can I handle errors during the conversion process?

A2: Implement error handling mechanisms using try-catch blocks to capture and manage exceptions.

### Q3: Is Aspose.CAD suitable for both Windows and Linux environments?

A3: Yes, Aspose.CAD is compatible with both Windows and Linux platforms.

### Q4: Can I customize the PDF output further?

A4: Certainly! Explore the extensive options provided by Aspose.CAD to tailor the PDF output to your specific requirements.

### Q5: Where can I find additional support or community discussions?

A5: Visit the [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19) for community support and discussions.
