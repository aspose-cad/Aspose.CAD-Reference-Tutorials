---
title: Save CAD as PNG – Export OLE Objects Using Aspose.CAD for Java
linktitle: Export OLE Objects from CAD
second_title: Aspose.CAD Java API
description: Unlock the potential of Aspose.CAD for Java. Effortlessly export OLE objects and **save CAD as PNG**. Download now for seamless CAD data management.
weight: 10
url: /java/cad-to-pdf-and-svg-export-options/export-ole-objects-from-cad/
date: 2026-03-02
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Save CAD as PNG – Export OLE Objects Using Aspose.CAD for Java

## Introduction

In the dynamic world of Computer-Aided Design (CAD), managing and extracting OLE (Object Linking and Embedding) objects efficiently—and being able to **save CAD as PNG**—is crucial for downstream workflows such as reporting, web preview, or archival. Aspose.CAD for Java provides a powerful, code‑first solution that lets you both export OLE objects and convert CAD drawings to high‑quality PNG images in just a few lines of code.

## Quick Answers
- **What does Aspose.CAD do?** It reads, manipulates, and converts CAD files (DWG, DXF, DGN, etc.) without needing native CAD software.  
- **Can I save CAD as PNG?** Yes—use the `PngOptions` together with `CadRasterizationOptions` to rasterize any layout.  
- **How to export OLE objects?** Load the CAD file with `Image.load` and save each OLE‑containing layout as PNG.  
- **Do I need a license?** A free trial is available; a commercial license removes evaluation limitations.  
- **What Java version is required?** Java 8 or higher is fully supported.

## What is **save CAD as PNG**?
Saving CAD as PNG means rasterizing vector‑based CAD drawings into a pixel‑based PNG image. This conversion is useful when you need a lightweight, universally viewable format for web pages, mobile apps, or documentation.

## Why use Aspose.CAD for Java to **convert CAD to PNG**?
- **No CAD installation needed** – the library works entirely in Java.  
- **Preserves layout fidelity** – you can choose specific layouts, control DPI, and retain line quality.  
- **Batch processing** – iterate over multiple files with a simple loop.  
- **Export OLE objects** – OLE content embedded in DWG/DXF files is automatically rendered into the PNG output.

## Prerequisites

Before diving into the tutorial, make sure you have the following prerequisites in place:

- **Java Environment** – Ensure you have a Java development environment set up on your machine.  
- **Aspose.CAD for Java** – Download and install the Aspose.CAD for Java library. You can find the library at the [download link](https://releases.aspose.com/cad/java/).  
- **CAD Files** – Prepare the CAD files containing OLE objects that you want to export.

## Import Namespaces

To begin, import the necessary namespaces into your Java project. These namespaces provide the essential classes and functionalities required for working with CAD files using Aspose.CAD.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Now, let's break down the process of exporting OLE objects from CAD into multiple steps:

## How to **save CAD as PNG** and export OLE objects

### Step 1: Set Your Document Directory

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

Ensure to replace `"Your Document Directory"` with the path to the directory containing your CAD files.

### Step 2: Define CAD File Names

```java
String[] files = new String[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

Specify the names of the CAD files that you want to process in the `files` array.

### Step 3: Set PNG Export Options

```java
PngOptions pngOptions = new PngOptions();
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.setVectorRasterizationOptions(rasterizationOptions);
rasterizationOptions.setLayouts(new String[] { "Layout1" });
```

Configure the PNG export options, including vector rasterization and layout settings. These options are what enable you to **convert CAD to PNG** with the desired quality.

### Step 4: Iterate Through CAD Files

```java
for(String file : files)
{
    CadImage cadImage = (CadImage)Image.load(dataDir + file);
    cadImage.save(dataDir + file + "_out.png", pngOptions);
}
```

Iterate through each specified CAD file, load it using Aspose.CAD, and save the OLE objects as PNG images. This loop demonstrates a simple way to **convert DWG to PNG** in bulk.

## Common Issues and Solutions

| Issue | Cause | Solution |
|-------|-------|----------|
| **Blank PNG output** | Layout name mismatch | Verify that the layout name (`"Layout1"`) exists in the source DWG. |
| **Missing OLE graphics** | OLE objects are stored in a different layout | Include all relevant layouts in `rasterizationOptions.setLayouts(...)`. |
| **Out‑of‑memory error on large files** | High DPI settings | Reduce DPI via `rasterizationOptions.setResolution(...)` or process files one at a time. |

## Frequently Asked Questions

**Q: Is Aspose.CAD compatible with all CAD file formats?**  
A: Aspose.CAD supports various CAD formats, including DWG, DXF, and DGN. Refer to the [documentation](https://reference.aspose.com/cad/java/) for the complete list.

**Q: Can I customize the export settings for OLE objects?**  
A: Yes, Aspose.CAD provides extensive options for customizing export settings, allowing you to tailor the output to your specific requirements.

**Q: Is there a free trial available for Aspose.CAD?**  
A: Yes, you can explore the capabilities of Aspose.CAD by obtaining a free trial from [here](https://releases.aspose.com/).

**Q: Where can I get community support for Aspose.CAD?**  
A: Join the Aspose.CAD community at the [forum](https://forum.aspose.com/c/cad/19) to seek assistance and share your experiences.

**Q: How can I purchase a license for Aspose.CAD?**  
A: Visit the [purchase page](https://purchase.aspose.com/buy) to acquire a license that suits your development needs.

## Conclusion

With these simple yet powerful steps, you can seamlessly **save CAD as PNG** while exporting OLE objects from CAD files using Aspose.CAD for Java. This versatile tool empowers developers to manage CAD data efficiently, opening up new possibilities in CAD application development and downstream image‑based workflows.

---

**Last Updated:** 2026-03-02  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}