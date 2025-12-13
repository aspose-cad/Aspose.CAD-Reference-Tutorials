---
title: Save CAD as JPEG with Layer Support in Java
linktitle: Support of Layers in CAD
second_title: Aspose.CAD Java API
description: Learn how to save CAD as JPEG in Java using Aspose.CAD, add multiple layers, and adjust CAD dimensions for precise image conversion.
weight: 18
url: /java/advanced-cad-features/support-of-layers-in-cad/
date: 2025-12-13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Save CAD as JPEG with Layer Support in Java

## Introduction

In this tutorial you’ll discover how to **save CAD as JPEG** while taking full advantage of layer support in Aspose.CAD for Java. Layers let you isolate specific parts of a drawing, making it easy to export only what you need. We’ll walk through each step, from setting up the environment to exporting a JPEG that includes just the layers you choose.

## Quick Answers
- **What does “save CAD as JPEG” mean?** It converts a CAD drawing into a raster JPEG image.
- **Can I include only selected layers?** Yes – use the `setLayers` method to specify which layers to render.
- **How do I change the image size?** Adjust `setPageWidth` and `setPageHeight` in `CadRasterizationOptions`.
- **Is this a Java‑only solution?** The example uses Aspose.CAD for Java, but the same concepts apply to other languages.
- **Do I need a license?** A free trial works for testing; a commercial license is required for production.

## Prerequisites

Before diving in, make sure you have the following:

1. **Aspose.CAD for Java Library** – download it from the [website](https://releases.aspose.com/cad/java/). Follow the installation guide to add the JAR files to your project’s classpath.  
2. **Java Development Environment** – a recent JDK (8 or newer) installed on your machine.

Now that we’re set up, let’s explore the code needed to **save CAD as JPEG** with selective layer rendering.

## Import Namespaces

Begin by importing the required Aspose.CAD classes and standard Java utilities:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import java.util.ArrayList;
import java.util.Arrays;
import java.util.List;
```

## Step‑by‑Step Guide

### Step 1: Set Up File Paths

Define where the source DWF file lives and where the output JPEG will be written.

```java
String dataDir = "Your Document Directory" + "DWFDrawings/";
String srcFile = dataDir + "for_layers_test.dwf";
String outFile = dataDir + "for_layers_test.jpg";
```

### Step 2: Load the DWF Image

Use Aspose.CAD’s `Image.load` method to read the CAD drawing.

```java
Image image = Image.load(srcFile);
```

### Step 3: Configure Rasterization Options (Adjust CAD Dimensions)

Create a `CadRasterizationOptions` instance and set the desired output size. Changing these values lets you **adjust CAD dimensions** for the final JPEG.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
```

### Step 4: Specify Layers (Add Multiple Layers)

If you want to render more than one layer, simply add their names to the list. Here we start with a single layer called “LayerA”.

```java
List<String> stringList = new ArrayList<>(Arrays.asList("LayerA"));
rasterizationOptions.setLayers(stringList);
```

*Pro tip:* To **add multiple layers**, expand the `Arrays.asList` call, e.g., `Arrays.asList("LayerA", "LayerB", "LayerC")`.

### Step 5: Configure JPEG Options (Java Convert CAD Image)

Tie the rasterization settings to the JPEG output format.

```java
JpegOptions jpegOptions = new JpegOptions();
jpegOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Step 6: Export to JPG (Save CAD as JPEG)

Finally, write the image to disk. This step **saves the CAD drawing as a JPEG** file that contains only the selected layers.

```java
image.save(outFile, jpegOptions);
```

By following these steps you’ve successfully **saved CAD as JPEG** while controlling which layers appear and customizing the image dimensions.

## Common Issues and Solutions

| Issue | Solution |
|-------|----------|
| **Layers not appearing** | Verify that the layer names match exactly what is stored in the DWF file (case‑sensitive). |
| **Output image is blank** | Ensure `setPageWidth` and `setPageHeight` are large enough for the drawing’s extents. |
| **License exception** | Use a trial license for testing; obtain a full license for production environments. |

## Frequently Asked Questions

**Q: Can I add multiple layers to the rasterization options?**  
A: Absolutely. Extend the `stringList` with additional layer names, e.g., `Arrays.asList("LayerA", "LayerB")`.

**Q: Is Aspose.CAD compatible with other CAD formats?**  
A: Yes, it supports DWG, DXF, DWF, and many more formats.

**Q: How can I change the output image dimensions?**  
A: Modify `setPageWidth` and `setPageHeight` in the `CadRasterizationOptions` instance.

**Q: Where can I purchase a license for Aspose.CAD?**  
A: You can explore licensing options [here](https://purchase.aspose.com/buy).

**Q: Where can I get community support?**  
A: Join the Aspose.CAD community on the [forum](https://forum.aspose.com/c/cad/19) for assistance and discussions.

---

**Last Updated:** 2025-12-13  
**Tested With:** Aspose.CAD for Java 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}