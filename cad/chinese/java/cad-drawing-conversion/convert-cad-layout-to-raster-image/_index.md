---
date: 2026-10-04
description: 了解如何使用 Aspose.CAD for Java 快速将 DWG 转换为 PNG，并将 CAD 导出为 PNG 或其他光栅格式。快速获得高质量结果。
keywords:
- convert dwg to png
- dwg to raster image
- convert cad to pdf
- export cad as png
- convert dwg to jpeg
lastmod: 2026-10-04
linktitle: 将 CAD 布局转换为光栅图像格式
og_description: 使用 Aspose.CAD for Java 快速将 DWG 转换为 PNG。一步步学习如何将 CAD 导出为 PNG、JPEG、TIFF
  等格式。
og_image_alt: 'Developer guide: Convert DWG to PNG and other raster formats using
  Aspose.CAD for Java'
og_title: 使用 Aspose.CAD for Java 将 DWG 转换为 PNG 及其他光栅格式
schemas:
- author: Aspose
  dateModified: '2026-10-04'
  description: Learn how to quickly convert dwg to png and export cad as png or other
    raster formats using Aspose.CAD for Java. Get high‑quality results fast.
  headline: Convert DWG to PNG and other raster formats using Aspose.CAD for Java
  type: TechArticle
- description: Learn how to quickly convert dwg to png and export cad as png or other
    raster formats using Aspose.CAD for Java. Get high‑quality results fast.
  name: Convert DWG to PNG and other raster formats using Aspose.CAD for Java
  steps:
  - name: set up the resource directory
    text: Replace `"Your Document Directory"` with the absolute path where your CAD
      files reside. This directory will be used for both input and output files.
  - name: load the CAD file
    text: '`Image.load` parses the source file and creates an in‑memory representation
      that you can rasterize. You can load any supported format (DWG, DXF, DGN, etc.)
      – this is the **how to convert cad** part.'
  - name: configure rasterization options
    text: '`CadRasterizationOptions` defines how the vector data is turned into pixels.
      `setPageWidth` and `setPageHeight` control output resolution (larger values
      = higher DPI). `setLayouts` lets you **convert CAD to raster** for specific
      layouts; omit it to rasterize the whole drawing.'
  - name: set image options
    text: '`TiffOptions` (or `PngOptions` for PNG) tells Aspose which raster format
      to generate and lets you fine‑tune compression, color depth, and other format‑specific
      settings. Choose the options class that matches your desired output.'
  - name: save the resultant image
    text: Call `save` on the `Image` instance, passing the output file name and the
      options object. Change the file extension to `.png` (and use `PngOptions`) to
      **save CAD as PNG**. The same pattern works for JPEG, BMP, or PDF. > **Common
      pitfall:** Forgetting to match the file extension with the options cla
  type: HowTo
- questions:
  - answer: Yes, it supports over 30 CAD and raster formats, including DWG, DXF, DGN,
      and SVG.
    question: Is Aspose.CAD compatible with different CAD file formats?
  - answer: Absolutely. Adjust `setPageWidth`, `setPageHeight`, or `setResolution`
      in `CadRasterizationOptions` to achieve the desired DPI.
    question: Can I customize the resolution of the output raster image?
  - answer: Provide an array with all layout names to `setLayouts`, e.g., `new String[]{"Model","Layout1","Layout2"}`.
    question: How can I convert multiple CAD layouts in a single run?
  - answer: Yes—PNG, JPEG, BMP, PDF, and more are available via their respective `*Options`
      classes.
    question: Are there output formats besides TIFF supported?
  - answer: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for community
      support and official assistance.
    question: Where can I get help or share my experience with Aspose.CAD?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- convert dwg
- Aspose.CAD
- Java raster conversion
- CAD image processing
title: 使用 Aspose.CAD for Java 将 DWG 转换为 PNG 及其他光栅格式
url: /zh/java/cad-drawing-conversion/convert-cad-layout-to-raster-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.CAD for Java 将 DWG 转换为 PNG 及其他光栅格式

## 介绍

`Aspose.CAD for Java` 是一个库，可实现对 CAD 文件进行程序化转换为光栅图像，如 PNG、JPEG 和 TIFF。将 DWG 转换为 PNG（或其他光栅图像格式）是常见需求，例如在团队成员没有 CAD 查看器时共享 CAD 图纸、在文档中嵌入设计，或为网页画廊生成缩略图。在本指南中，您将学习如何快速可靠地将 dwg 转换为 png，无论是处理完整的绘图文件还是仅特定布局。您可能还需要 **convert CAD to raster** 用于网页预览、报告工具或移动应用。

## 快速答案
- **哪个库处理 DWG 到 PNG？** Aspose.CAD for Java provides the conversion engine.  
- **我可以导出哪些光栅格式？** PNG, JPEG, TIFF, PDF, BMP, and more than 30 additional formats.  
- **测试需要许可证吗？** A free trial works for development; a commercial license is required for production.  
- **我可以选择特定布局吗？** Yes – use `setLayouts` to target “Model”, “Layout1”, etc.  
- **是否可以输出高分辨率？** Absolutely – adjust `setPageWidth` and `setPageHeight` (or `setResolution`) to control DPI.

## 什么是 “convert dwg to png”？

Convert dwg to png 意味着将 DWG 矢量图转换为像素化的 PNG 图像，任何标准图像查看器都可以显示。此过程将矢量实体光栅化，保留线宽、颜色和图层，同时将其转换为固定分辨率的位图。该结果非常适合嵌入 PDF、Word 文档或矢量支持受限的网页中。

## 为什么将 CAD 导出为 PNG（或其他光栅格式）？

将 CAD 导出为 PNG 可提供通用兼容性、快速加载以及在所有主流平台上的轻松嵌入。相较于打开庞大的 DWG 文件，光栅图像加载瞬间完成，且 PNG 的无损压缩确保视觉保真度。通过控制分辨率、背景颜色和布局，您可以保证每位利益相关者看到相同的外观，无论文件在桌面、移动设备还是浏览器中查看。

## 常见使用场景

| 场景 | 光栅输出的优势 |
|----------|------------------------|
| **项目文档** | 在 PDF 或 Word 文档中嵌入 PNG 可避免审阅者需要 CAD 软件。 |
| **Web 门户** | 从 DWG 文件生成的缩略图加载瞬间并提升用户体验。 |
| **移动应用** | 光栅图像在没有 CAD 查看器的设备上能够正确显示。 |
| **自动化报告** | 批量将多个布局转换为 PNG/JPEG，以便在图表或仪表板中使用。 |

## 前置条件

在开始之前，请确保您拥有：

1. **Java 开发环境** – 已安装并配置 JDK 8 或更高版本。  
2. **Aspose.CAD for Java** – 从 [Aspose.CAD for Java documentation](https://reference.aspose.com/cad/java/) 下载最新的 JAR。  

## 导入命名空间

`com.aspose.cad.Image` 是表示内存中任何 CAD 文件的核心类。`com.aspose.cad.imageoptions.*` 为每种光栅格式提供选项对象。导入您需要的类以加载图纸、配置光栅化并保存输出。

> **Pro tip:** 如果您计划 **export CAD as PNG** 而不是 TIFF，请将 `TiffOptions` 替换为 `PngOptions`（位于 `com.aspose.cad.imageoptions.PngOptions`）。

## 分步指南

### 步骤 1：设置资源目录

将 `"Your Document Directory"` 替换为 CAD 文件所在的绝对路径。此目录将用于输入和输出文件。

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

### 步骤 2：加载 CAD 文件

`Image.load` 解析源文件并创建可进行光栅化的内存表示。您可以加载任何受支持的格式（DWG、DXF、DGN 等）——这就是 **how to convert cad** 的部分。

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";
```

### 步骤 3：配置光栅化选项

`CadRasterizationOptions` 定义了向量数据如何转换为像素。`setPageWidth` 和 `setPageHeight` 控制输出分辨率（值越大 DPI 越高）。`setLayouts` 允许您对特定布局 **convert CAD to raster**；如果省略，则光栅化整个图纸。

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

### 步骤 4：设置图像选项

`TiffOptions`（或用于 PNG 的 `PngOptions`）告诉 Aspose 生成哪种光栅格式，并允许您微调压缩、颜色深度以及其他特定格式的设置。选择与所需输出相匹配的选项类。

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1200);
rasterizationOptions.setPageHeight(1200);
rasterizationOptions.setLayouts(new String[] {"Model", "Layout1"});
```

### 步骤 5：保存生成的图像

在 `Image` 实例上调用 `save`，传入输出文件名和选项对象。将文件扩展名改为 `.png`（并使用 `PngOptions`）即可 **save CAD as PNG**。相同模式适用于 JPEG、BMP 或 PDF。

```java
ImageOptionsBase options = new TiffOptions(TiffExpectedFormat.Default);
options.setVectorRasterizationOptions(rasterizationOptions);
```

> **Common pitfall:** 忘记使文件扩展名与选项类匹配会导致 `UnsupportedFormatException`。请始终保持一致。

## 常见问题及解决方案

| 问题 | 解决方案 |
|-------|----------|
| **空白输出图像** | 确保 `setLayouts` 中的布局名称与源 CAD 文件中的完全匹配。 |
| **低分辨率 PNG** | 增加 `setPageWidth` / `setPageHeight` 或在光栅化选项上设置 `setResolution`。 |
| **不受支持的 DWG 版本** | 确保使用最新的 Aspose.CAD 版本；旧版本可能不支持更新的 DWG。 |
| **大文件内存错误** | 一次处理单页或增加 JVM 堆内存 (`-Xmx2g`)。 |

## 常见问题

**Q: Aspose.CAD 是否兼容不同的 CAD 文件格式？**  
A: 是的，它支持超过 30 种 CAD 和光栅格式，包括 DWG、DXF、DGN 和 SVG。

**Q: 我可以自定义输出光栅图像的分辨率吗？**  
A: 当然。调整 `CadRasterizationOptions` 中的 `setPageWidth`、`setPageHeight` 或 `setResolution` 以实现所需的 DPI。

**Q: 如何在一次运行中转换多个 CAD 布局？**  
A: 向 `setLayouts` 提供包含所有布局名称的数组，例如 `new String[]{"Model","Layout1","Layout2"}`。

**Q: 除了 TIFF 之外还有其他支持的输出格式吗？**  
A: 有——通过各自的 `*Options` 类可使用 PNG、JPEG、BMP、PDF 等更多格式。

**Q: 我可以在哪里获取帮助或分享使用 Aspose.CAD 的经验？**  
A: 访问 [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) 获取社区支持和官方帮助。

## 结论

按照这些步骤，您即可 **convert DWG to PNG**、**export CAD as PNG**、**save CAD as JPEG**，或生成所需的任何其他光栅格式。Aspose.CAD for Java 负责繁重的工作，让您专注于将高质量图像集成到应用程序、文档或网页门户中。该库支持 30 多种格式，并且能够在不将整个文件加载到内存的情况下渲染数百页的图纸，是企业级 CAD 光栅化的可靠选择。

---

**最后更新：** 2026-10-04  
**测试环境：** Aspose.CAD for Java 24.12  
**作者：** Aspose  







```java
image.save(dataDir + "conic_pyramid_layoutstorasterimage_out_.tiff", options);
```

```bash
java -jar aspose-cad.jar -i input.dwg -o output.png -w 1200 -h 1200
```

## 相关教程

- [快速使用 java cad 库 Aspose.CAD for Java 将 DWG 导出为 PDF 或光栅](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [使用 Aspose.CAD for Java 将 DWG 转换为 BMP](/cad/java/cad-export-options/export-to-bmp/)
- [使用 Aspose.CAD for Java 将 DWG 导出为 PDF：特定布局](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}