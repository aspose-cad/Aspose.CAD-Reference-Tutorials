---
date: 2026-02-20
description: Ubah IFC menjadi PNG dengan mudah menggunakan Aspose.CAD untuk Java.
  Ikuti tutorial langkah demi langkah kami.
linktitle: Export IFC to PNG
second_title: Aspose.CAD Java API
title: Cara Mengonversi IFC ke PNG dengan Aspose.CAD untuk Java
url: /id/java/cad-export-options/export-ifc-to-png/
weight: 18
---

 -> "Pertanyaan yang Sering Diajukan". "Conclusion" -> "Kesimpulan". Ensure headings remain same level.

Now produce final.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export IFC to PNG with Aspose.CAD for Java

## Introduction

Selamat datang di tutorial langkah‑demi‑langkah ini tentang **cara mengonversi IFC ke PNG** menggunakan Aspose.CAD for Java. Baik Anda membangun pipeline BIM‑to‑image atau membutuhkan pratinjau visual cepat dari model IFC, panduan ini akan memandu Anda melalui setiap detail sehingga Anda dapat **mengonversi IFC ke PNG** secara andal dalam aplikasi Java Anda.

## Quick Answers
- **What library is required?** Aspose.CAD for Java  
- **Can I convert IFC to PNG in a few lines of code?** Yes – the core process fits in under 20 lines.  
- **Do I need a license for production?** A temporary license works for testing; a full license is required for commercial use.  
- **Is the output scalable?** The rasterization options let you set any pixel dimensions you need.  
- **Which Java version is supported?** Java 8 or higher.

## What is “convert IFC to PNG”?
Mengonversi IFC (Industry Foundation Classes) ke PNG berarti meraster data model bangunan 3‑D menjadi gambar bitmap 2‑D. Hal ini berguna untuk menghasilkan thumbnail, menyematkan model dalam laporan, atau membuat visualisasi siap web tanpa memerlukan penampil CAD lengkap.

## Why use Aspose.CAD for Java?
- **Full‑featured** support for many CAD formats, including IFC.  
- **No external dependencies** – pure Java, easy to integrate.  
- **Fine‑grained control** over rasterization (resolution, background, line weight).  
- **Cross‑platform** – works on Windows, Linux, and macOS.

## Prerequisites

Sebelum memulai, pastikan Anda memiliki hal‑hal berikut:

- **Aspose.CAD Library** – download and install the Aspose.CAD library for Java from the [download link](https://releases.aspose.com/cad/java/).  
- **Document Directory** – a folder on your system that contains the IFC file you want to convert.

## Import Namespaces

In your Java project, import the necessary classes:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

## Step‑by‑Step Guide

### Step 1: Load the IFC File
First, point to the folder where your IFC file lives and load it.

```java
String dataDir = "Your Document Directory" + "ExportingIFC/";
String fileName = dataDir + "example.ifc";
IfcImage cadImage = (IfcImage)Image.load(fileName);
```

> **Why this matters:** Loading the file as an `IfcImage` gives you access to Cad‑specific rasterization options later on.

### Step 2: Set Vector (Rasterization) Options
Define the output dimensions and any other vector‑related settings.

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
```

> You can adjust `PageWidth` and `PageHeight` to control the final PNG resolution, which is essential when you **save PNG java** files for high‑quality prints.

### Step 3: Configure PNG Options
Link the rasterization options to the PNG exporter.

```java
PngOptions pngOptions = new PngOptions();
pngOptions.setVectorRasterizationOptions(vectorOptions);
```

### Step 4: Save the Image as PNG
Finally, write the rasterized image to disk.

```java
String outPath = dataDir + "example.png";
cadImage.save(outPath, pngOptions);
```

> After this step you have successfully **converted IFC to PNG** and can use the resulting `example.png` anywhere you need a raster image.

## Common Use Cases
- **Generating thumbnails** for BIM models in web portals.  
- **Embedding floor‑plan snapshots** into PDF reports.  
- **Automated batch conversion** of large IFC libraries for archival.

## Troubleshooting & Tips
- **Memory issues:** When converting very large IFC files, increase the JVM heap (`-Xmx2g` or higher).  
- **Missing textures:** Ensure the IFC file references external resources that are accessible from `dataDir`.  
- **Pro tip:** Use `vectorOptions.setBackgroundColor(Color.getWhite())` if you need a white background instead of the default transparent PNG.

## FAQ's

### Q1: Is Aspose.CAD compatible with all versions of IFC files?
A1: Aspose.CAD supports various versions of IFC files. Refer to the [documentation](https://reference.aspose.com/cad/java/) for compatibility details.

### Q2: Can I customize the rasterization options further?
A2: Absolutely! Explore the [documentation](https://reference.aspose.com/cad/java/) for advanced customization options.

### Q3: Is there a trial version available?
A3: Yes, you can access the free trial version [here](https://releases.aspose.com/).

### Q4: How can I get temporary licensing for Aspose.CAD?
A4: Obtain a temporary license from [this link](https://purchase.aspose.com/temporary-license/).

### Q5: Where can I seek help or discuss issues?
A5: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for community support.

## Frequently Asked Questions

**Q: Can I use this approach to convert other CAD formats to PNG?**  
A: Yes, Aspose.CAD supports many formats (DWG, DXF, DGN, etc.). Just change the file extension and cast to the appropriate image class.

**Q: Does the library let me set a custom DPI?**  
A: You can control DPI indirectly by adjusting `PageWidth`/`PageHeight` relative to the desired physical size.

**Q: Is the PNG output loss‑less?**  
A: PNG is a lossless format, so the rasterized image retains full visual fidelity of the vector data.

## Conclusion

Anda kini telah mempelajari cara **mengonversi IFC ke PNG** secara efisien dengan Aspose.CAD for Java. Dengan mengikuti langkah‑langkah ini, Anda dapat mengintegrasikan konversi IFC‑to‑PNG ke dalam alur kerja berbasis Java apa pun, baik itu alat desktop, layanan sisi‑server, atau fungsi cloud.

---

**Last Updated:** 2026-02-20  
**Tested With:** Aspose.CAD for Java 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}