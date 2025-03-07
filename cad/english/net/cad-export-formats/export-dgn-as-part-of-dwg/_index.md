---
title: Export DGN as Part of DWG in Aspose.CAD for .NET
linktitle: Export DGN as Part of DWG
second_title: Aspose.CAD .NET - CAD and BIM File Format
description: Learn how to export DGN as part of DWG in Aspose.CAD for .NET. Follow our step-by-step guide for seamless integration.
weight: 11
url: /net/cad-export-formats/export-dgn-as-part-of-dwg/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export DGN as Part of DWG in Aspose.CAD for .NET

## Introduction

In the world of .NET development, Aspose.CAD stands out as a powerful library for working with Computer-Aided Design (CAD) files. This tutorial will guide you through the process of exporting a DGN (Design) file as part of a DWG (Drawing) file using Aspose.CAD for .NET. Whether you're a seasoned developer or just starting, this step-by-step guide will help you harness the capabilities of Aspose.CAD to achieve this specific task efficiently.

## Prerequisites

Before diving into the tutorial, make sure you have the following prerequisites in place:

- Aspose.CAD for .NET: Ensure that you have the Aspose.CAD library for .NET installed. You can download it [here](https://releases.aspose.com/cad/net/).

- Development Environment: Set up your preferred .NET development environment, such as Visual Studio.

- Basic Knowledge of C#: Familiarize yourself with the C# programming language.

## Import Namespaces

In your C# project, include the necessary namespaces to access the Aspose.CAD functionality. Add the following using directives at the beginning of your code file:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

Now, let's break down the provided code into multiple steps:

## Step 1: Define File Paths

```csharp
// Input and Output file paths
string fileName = "BlockRefDgn.dwg";
string outPath = fileName + ".pdf";
```

## Step 2: Create PdfOptions Instance

```csharp
// Create an instance of PdfOptions class for exporting DWG to PDF
PdfOptions exportOptions = new PdfOptions();
```

## Step 3: Load DWG File

```csharp
// Load the existing DWG file as an image and convert it to CadImage type
using (CadImage cadImage = (CadImage)Image.Load(fileName))
```

## Step 4: Iterate Through Entities

```csharp
// Iterate through each entity inside the DWG file
foreach (CadBaseEntity baseEntity in cadImage.Entities)
```

## Step 5: Check Entity Type

```csharp
// Check if the entity is an image definition
if (baseEntity.TypeName == CadEntityTypeName.DGNUNDERLAY)
```

## Step 6: Get Underlay Path

```csharp
// If it's an image definition, get the external reference to the object
CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
Console.WriteLine(dgnFile.UnderlayPath);
```

## Step 7: Define Rasterization Options

```csharp
// Define settings for CadRasterizationOptions object
exportOptions.VectorRasterizationOptions = new CadRasterizationOptions()
{
    PageWidth = 1600,
    PageHeight = 1600,
    Layouts = new string[] { "Model" },
    AutomaticLayoutsScaling = false,
    NoScaling = true,
    BackgroundColor = Color.Black,
    DrawType = CadDrawTypeMode.UseObjectColor
};
```

## Step 8: Export DWG to PDF

```csharp
// Export the DWG to PDF by calling Save method
cadImage.Save(outPath, exportOptions);
```

## Conclusion

Congratulations! You've successfully walked through the process of exporting a DGN file as part of a DWG file using Aspose.CAD for .NET. This tutorial has provided you with the fundamental steps and code snippets to achieve this specific task seamlessly.

## FAQ's

### Q1: Can I use Aspose.CAD for .NET in my commercial projects?
A1: Yes, you can. Visit [here](https://purchase.aspose.com/buy) to explore licensing options.

### Q2: Are there any limitations on the size of DWG files I can process?
A2: Aspose.CAD supports handling large DWG files, but hardware limitations may apply.

### Q3: Is there a trial version available?
A3: Yes, you can get a free trial [here](https://releases.aspose.com/).

### Q4: How can I get temporary licenses?
A4: Temporary licenses can be obtained [here](https://purchase.aspose.com/temporary-license/).

### Q5: Where can I seek assistance if I encounter issues?
A5: You can visit the Aspose.CAD forum [here](https://forum.aspose.com/c/cad/19) for support.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
