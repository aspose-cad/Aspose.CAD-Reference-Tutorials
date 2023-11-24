---
title: Exporting Embedded DGN Files - Aspose.CAD Tutorial
linktitle: Exporting Embedded DGN Files
second_title: Aspose.CAD .NET - CAD and BIM File Format
description: Explore the power of Aspose.CAD for .NET. Learn to export embedded DGN files to PDF effortlessly with this step-by-step tutorial.
type: docs
weight: 14
url: /net/export-techniques/exporting-embedded-dgn-files/
---
## Introduction

In the dynamic world of software development, Aspose.CAD for .NET stands out as a powerful tool for handling Computer-Aided Design (CAD) files. This tutorial will guide you through the process of exporting embedded DGN files using Aspose.CAD for .NET. Whether you're a seasoned developer or a curious beginner, this step-by-step guide will help you harness the capabilities of Aspose.CAD effectively.

## Prerequisites

Before diving into the tutorial, ensure you have the following prerequisites in place:

1. Aspose.CAD for .NET: Download and install the library from [Aspose.CAD for .NET](https://releases.aspose.com/cad/net/).

2. Development Environment: Set up a .NET development environment with Visual Studio or any other preferred IDE.

3. Sample DXF File: For this tutorial, we'll use the "conic_pyramid.dxf" file. Make sure you have it available in your designated document directory.

## Import Namespaces

In your C# code, make sure to import the necessary namespaces:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
```

## Step 1: Load the DXF File

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Your code for further steps will go here
}
```

## Step 2: Set Rasterization Options

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new[] { "Model" };
```

## Step 3: Set PDF Options

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Step 4: Save as PDF

```csharp
cadImage.Save(MyDir + "conic_pyramid.pdf", pdfOptions);
```

## Step 5: Display Success Message

```csharp
Console.WriteLine("\nThe DXF drawing exported successfully to PDF.\nFile saved at " + MyDir);
```

## Conclusion

Congratulations! You've successfully exported an embedded DGN file to PDF using Aspose.CAD for .NET. This tutorial covered the essential steps, providing you with a foundation to explore more advanced functionalities offered by Aspose.CAD.

## FAQ's

### Q1: Can I use Aspose.CAD for .NET with other programming languages?

A1: Aspose.CAD primarily supports .NET, but Aspose provides libraries for various languages, including Java and Python.

### Q2: Is there a free trial available for Aspose.CAD for .NET?

A2: Yes, you can get a free trial from [here](https://releases.aspose.com/).

### Q3: Where can I find comprehensive documentation for Aspose.CAD for .NET?

A3: Refer to the official documentation [here](https://reference.aspose.com/cad/net/).

### Q4: How do I get temporary licensing for Aspose.CAD for .NET?

A4: Obtain a temporary license [here](https://purchase.aspose.com/temporary-license/).

### Q5: Need assistance or want to engage with the community?

A5: Visit the [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19) for support and discussions.
