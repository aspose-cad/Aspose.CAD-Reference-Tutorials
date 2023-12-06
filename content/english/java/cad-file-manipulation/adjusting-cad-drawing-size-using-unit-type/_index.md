---
title: Adjusting CAD Drawing Size Using Unit Type with Aspose.CAD for Java
linktitle: Adjusting CAD Drawing Size Using Unit Type
second_title: Aspose.CAD Java API
description: Explore the power of Aspose.CAD for Java in adjusting CAD drawing sizes effortlessly. Follow our step-by-step guide for precision and adaptability.
type: docs
weight: 14
url: /java/cad-file-manipulation/adjusting-cad-drawing-size-using-unit-type/
---
## Introduction

In the ever-evolving realm of Computer-Aided Design (CAD), precision and adaptability are paramount. One common requirement is adjusting the size of CAD drawings based on specific unit types. Aspose.CAD for Java emerges as a powerful ally, providing seamless capabilities for manipulating CAD files programmatically.

## Prerequisites

Before diving into the tutorial, make sure you have the following prerequisites in place:

- Java Development Environment: Ensure that you have a functional Java development environment set up on your machine.

- Aspose.CAD for Java Library: Download and integrate the Aspose.CAD library into your Java project. You can obtain the library [here](https://releases.aspose.com/cad/java/).

## Import Namespaces

In your Java code, include the necessary namespaces to access Aspose.CAD functionalities. Add the following imports:

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Now, let's break down the process of adjusting CAD drawing size using unit type into manageable steps:

## Step 1: Define Data Directory

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

Set the path for the directory where your CAD files are located.

## Step 2: Load CAD Drawing

```java
String sourceFilePath = dataDir + "sample.dwg";
Image image = Image.load(sourceFilePath);
```

Load the CAD drawing using Aspose.CAD's `Image` class.

## Step 3: Create BMP Options

```java
BmpOptions bmpOptions = new BmpOptions();
```

Instantiate the `BmpOptions` class for exporting the CAD layout to BMP format.

## Step 4: Configure Rasterization Options

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(cadRasterizationOptions);
```

Create an instance of `CadRasterizationOptions` and associate it with the `BmpOptions` for vector rasterization.

## Step 5: Set Unit Type

```java
cadRasterizationOptions.setUnitType(UnitType.Centimeter);
```

Specify the desired unit type for the CAD drawing. In this example, we've set it to Centimeter.

## Step 6: Set Layouts

```java
cadRasterizationOptions.setLayouts(new String[] { "Model" });
```

Define the layouts to be considered during the export. In this case, we've selected the "Model" layout.

## Step 7: Export to BMP

```java
String outPath = sourceFilePath + ".bmp";
image.save(outPath, bmpOptions);
```

Finally, save the modified CAD drawing in BMP format.

## Conclusion

With Aspose.CAD for Java, adjusting CAD drawing sizes becomes a breeze. This tutorial has walked you through the process, emphasizing each step's significance in achieving precise results.

## FAQ's

### Q1: Can I use Aspose.CAD for Java with other programming languages?

A1: Aspose.CAD primarily supports Java, but there are versions available for other languages like .NET.

### Q2: Are there any licensing options for Aspose.CAD?

A2: Yes, you can explore licensing options and purchase Aspose.CAD [here](https://purchase.aspose.com/buy).

### Q3: Is there a free trial available for Aspose.CAD?

A3: Certainly, you can access a free trial [here](https://releases.aspose.com/).

### Q4: How can I get support for Aspose.CAD for Java?

A4: Visit the Aspose.CAD forum [here](https://forum.aspose.com/c/cad/19) for comprehensive support.

### Q5: Can I obtain a temporary license for Aspose.CAD?

A5: Yes, you can acquire a temporary license [here](https://purchase.aspose.com/temporary-license/).
