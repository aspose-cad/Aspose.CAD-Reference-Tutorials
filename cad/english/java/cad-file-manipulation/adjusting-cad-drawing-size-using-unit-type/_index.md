---
title: Export DWG to BMP: Adjust CAD Size Using Unit Type (Aspose.CAD Java)
linktitle: Adjusting CAD Drawing Size Using Unit Type
second_title: Aspose.CAD Java API
description: Learn how to export DWG to BMP and adjust CAD drawing size using unit type with Aspose.CAD for Java – a step‑by‑step guide for precise conversion.
weight: 14
url: /java/cad-file-manipulation/adjusting-cad-drawing-size-using-unit-type/
date: 2026-02-23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export DWG to BMP: Adjust CAD Drawing Size Using Unit Type with Aspose.CAD for Java

## Introduction

If you need to **export DWG to BMP** while keeping full control over the drawing’s dimensions, you’re in the right place. Changing the CAD unit type during conversion lets you **adjust CAD size** to match real‑world measurements such as centimeters or inches. In this tutorial we’ll walk through the exact steps to convert a DWG file to an image, set the desired unit, and produce a BMP output using Aspose.CAD for Java.

## Quick Answers
- **What does “export DWG to BMP” mean?** It converts a DWG vector file into a raster BMP image.  
- **Why set a unit type?** The unit determines the physical size of the exported image (e.g., centimeters vs. inches).  
- **Which library is required?** Aspose.CAD for Java.  
- **Do I need a license for production?** Yes, a commercial license is required for non‑trial use.  
- **Can I convert DWG to other image formats?** Absolutely – the same API supports PNG, JPEG, TIFF, etc.

## What is “export DWG to BMP”?
Exporting DWG to BMP means taking a CAD drawing (DWG) and rasterizing it into a bitmap (BMP) file. This is useful when you need a universally viewable image for reports, documentation, or web preview.

## Why use unit type when converting DWG to BMP?
Setting the unit type (e.g., `UnitType.Centimeter`) tells the rasterizer how many pixels correspond to a real‑world measurement. This helps you **adjust CAD size** accurately, ensuring that the resulting BMP matches the intended scale.

## Prerequisites

Before we dive into the code, make sure you have the following:

- **Java Development Environment** – JDK 8 or newer installed and configured.  
- **Aspose.CAD for Java Library** – Download the latest JAR from the official site [here](https://releases.aspose.com/cad/java/).  
- **A sample DWG file** – Place it in a folder that your Java project can access.

## Import Namespaces

In your Java source file, import the required Aspose.CAD classes:

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

## Step‑by‑Step Guide

### Step 1: Define Data Directory
Set the folder that contains your DWG file.

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

### Step 2: Load the CAD Drawing
Open the DWG file with Aspose.CAD’s `Image` class.

```java
String sourceFilePath = dataDir + "sample.dwg";
Image image = Image.load(sourceFilePath);
```

### Step 3: Create BMP Options
Instantiate `BmpOptions` – this tells Aspose.CAD that we want BMP output.

```java
BmpOptions bmpOptions = new BmpOptions();
```

### Step 4: Configure Rasterization Options
Link a `CadRasterizationOptions` object to the BMP options so we can control scaling, layout, and unit type.

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(cadRasterizationOptions);
```

### Step 5: Set Unit Type
Here we **how to set unit** for the export. Changing the unit type directly influences the final image size.

```java
cadRasterizationOptions.setUnitType(UnitType.Centimeter);
```

### Step 6: Choose Layouts
Select which layout(s) from the DWG file should be rendered. The “Model” layout is the most common.

```java
cadRasterizationOptions.setLayouts(new String[] { "Model" });
```

### Step 7: Export to BMP
Finally, save the rasterized image as a BMP file. This completes the **convert dwg to bmp** operation.

```java
String outPath = sourceFilePath + ".bmp";
image.save(outPath, bmpOptions);
```

## Common Issues and Solutions

| Issue | Reason | Fix |
|-------|--------|-----|
| **Output image is too small** | Unit type not set or default DPI too low | Use `cadRasterizationOptions.setUnitType(UnitType.Centimeter)` (or Millimeter) and adjust `cadRasterizationOptions.setResolution()` if needed. |
| **Blank BMP file** | Wrong layout name or missing layout in the source DWG | Verify the layout name with a CAD viewer and ensure it matches the string passed to `setLayouts`. |
| **License exception** | Running without a valid license in production | Apply a temporary or permanent license using `License license = new License(); license.setLicense("Aspose.CAD.lic");`. |

## Frequently Asked Questions

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

---

**Last Updated:** 2026-02-23  
**Tested With:** Aspose.CAD for Java latest version  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}