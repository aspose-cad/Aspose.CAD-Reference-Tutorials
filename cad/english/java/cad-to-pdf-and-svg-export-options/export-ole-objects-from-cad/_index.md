---
title: "Save CAD as PNG and Export OLE Objects with Aspose.CAD for Java"
linktitle: Export OLE Objects from CAD
second_title: Aspose.CAD Java API
description: Learn how to **save CAD as PNG** and effortlessly export OLE objects from CAD files using Aspose.CAD for Java. Quick setup, full code sample, and best‑practice tips.
weight: 10
url: /java/cad-to-pdf-and-svg-export-options/export-ole-objects-from-cad/
date: 2026-01-04
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Save CAD as PNG and Export OLE Objects with Aspose.CAD for Java

## Introduction

In the fast‑moving world of Computer‑Aided Design (CAD), being able to **save CAD as PNG** while extracting embedded OLE (Object Linking and Embedding) objects can dramatically streamline your workflow. Whether you’re building a batch‑conversion tool, generating thumbnails for a web portal, or simply need to archive OLE content, Aspose.CAD for Java gives you a clean, programmatic way to do it. In this tutorial we’ll walk through the entire process, from setting up your project to exporting each OLE object as a PNG image.

## Quick Answers
- **Can I export OLE objects directly to PNG?** Yes – Aspose.CAD loads the CAD file and lets you rasterize each layout to PNG.  
- **What Java version is required?** Java 8 or later.  
- **Do I need a license for this feature?** A free trial works for evaluation; a license is required for production.  
- **Will vector data be preserved?** The PNG rasterization keeps visual fidelity, but the output is raster, not vector.  
- **Is batch processing supported?** Absolutely – iterate over an array of files as shown in the code sample.

## Prerequisites

Before you start, make sure you have the following:

- **Java Development Kit (JDK)** – Java 8+ installed and configured.  
- **Aspose.CAD for Java** – Download the latest library from the [download link](https://releases.aspose.com/cad/java/).  
- **CAD source files** – Any DWG/DXF/DGN files that contain OLE objects you want to export.

## Import Namespaces

To work with CAD files you need to import the core Aspose.CAD classes. Keep the import block exactly as shown – it provides the classes used later in the tutorial.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

## How to Save CAD as PNG

Below is a concise, step‑by‑step guide that shows **how to export OLE objects and save CAD as PNG**. Each step includes a short explanation followed by the exact code you need to copy into your project.

### Step 1: Set Your Document Directory

Define the folder that holds your CAD drawings. Replace the placeholder with the actual path on your machine.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

### Step 2: Define CAD File Names

List every CAD file you want to process. You can add as many entries as needed.

```java
String[] files = new String[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

### Step 3: Set PNG Export Options

Configure rasterization settings. Here we target a specific layout (`Layout1`) and use the default PNG options.

```java
PngOptions pngOptions = new PngOptions();
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.setVectorRasterizationOptions(rasterizationOptions);
rasterizationOptions.setLayouts(new String[] { "Layout1" });
```

### Step 4: Iterate Through CAD Files and Save as PNG

Load each CAD file, rasterize the OLE objects, and write the output PNG file. The `_out.png` suffix helps you identify the generated images.

```java
for(String file : files)
{
    CadImage cadImage = (CadImage)Image.load(dataDir + file);
    cadImage.save(dataDir + file + "_out.png", pngOptions);
}
```

## Common Issues and Solutions

| Problem | Why it Happens | Fix |
|---------|----------------|-----|
| **`Image.load` throws `FileNotFoundException`** | The `dataDir` path is incorrect or the file name has a typo. | Double‑check the directory string and ensure the file names match exactly, including spaces. |
| **Output PNG is blank** | The layout name does not exist in the source CAD file. | Use `cadImage.getLayouts()` to list available layouts, then update `rasterizationOptions.setLayouts(...)`. |
| **Large CAD files cause OutOfMemoryError** | Rasterizing high‑resolution images consumes a lot of heap space. | Increase the JVM heap (`-Xmx2g`) or lower the rasterization resolution via `rasterizationOptions.setResolution(...)`. |

## FAQ's

### Q1: Is Aspose.CAD compatible with all CAD file formats?

A1: Aspose.CAD supports various CAD formats, including DWG, DXF, and DGN. Refer to the [documentation](https://reference.aspose.com/cad/java/) for the complete list.

### Q2: Can I customize the export settings for OLE objects?

A2: Yes, Aspose.CAD provides extensive options for customizing export settings, allowing you to tailor the output to your specific requirements.

### Q3: Is there a free trial available for Aspose.CAD?

A3: Yes, you can explore the capabilities of Aspose.CAD by obtaining a free trial from [here](https://releases.aspose.com/).

### Q4: Where can I get community support for Aspose.CAD?

A4: Join the Aspose.CAD community at the [forum](https://forum.aspose.com/c/cad/19) to seek assistance and share your experiences.

### Q5: How can I purchase a license for Aspose.CAD?

A5: Visit the [purchase page](https://purchase.aspose.com/buy) to acquire a license that suits your development needs.

## Conclusion

By following these five simple steps you can **save CAD as PNG** and extract every embedded OLE object with just a few lines of Java code. This approach is ideal for batch conversions, automated reporting, or any scenario where you need raster images of CAD content without manual exporting. Feel free to experiment with different rasterization options to match your quality and performance requirements.

---

**Last Updated:** 2026-01-04  
**Tested With:** Aspose.CAD for Java 24.12 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}