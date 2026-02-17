---
date: 2026-02-17
description: 学习如何使用 Aspose.CAD for Java 将 dwg 转换为 png，并将 CAD 导出为 png 或其他栅格格式。快速获得高质量的结果。
linktitle: Convert CAD Layout to Raster Image Format
second_title: Aspose.CAD Java API
title: 使用 Aspose.CAD for Java 将 DWG 转换为 PNG 及其他光栅格式
url: /zh/java/cad-drawing-conversion/convert-cad-layout-to-raster-image/
weight: 12
---

" translate to Chinese: "# 使用 Aspose.CAD for Java 将 DWG 转换为 PNG 及其他光栅格式"

Similarly subheadings.

Translate paragraphs.

Need to keep code block placeholders unchanged.

Tables: translate column headers and content.

Make sure not to translate URLs.

Proceed.

Let's craft translation.

Be careful with bullet lists.

Also keep emphasis **.

Ok produce final content.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.CAD for Java 将 DWG 转换为 PNG 及其他光栅格式

## 介绍

将 DWG 转换为 PNG（或其他光栅图像格式）是当您需要与没有 CAD 查看器的团队成员共享 CAD 图纸、在文档中嵌入设计，或为网页图库生成缩略图时的常见需求。**在本指南中，您将学习如何快速且可靠地将 dwg 转换为 png**，无论是处理完整的图纸文件还是仅针对特定布局。您可能还需要**将 CAD 转换为光栅**以用于网页预览、报表工具或移动应用。Aspose.CAD for Java 使此转换变得简单，并让您完全控制分辨率、布局选择和输出格式。

## 快速答案
- **哪个库处理 DWG 到 PNG？** Aspose.CAD for Java  
- **可以导出哪些格式？** PNG、JPEG、TIFF、PDF、BMP 等  
- **测试需要许可证吗？** 开发阶段可使用免费试用版；生产环境需要许可证  
- **可以选择特定布局吗？** 可以，使用 `setLayouts` 指定 “Model”、 “Layout1” 等  
- **是否支持高分辨率输出？** 当然——通过调整 `setPageWidth` 和 `setPageHeight` 控制 DPI  

## 什么是 “convert dwg to png”？

“convert dwg to png” 这一短语描述了将基于向量的 DWG 文件（许多 CAD 应用的原生格式）栅格化为基于像素的 PNG 图像的过程。光栅图像非常适合网页显示、电子邮件共享以及在非 CAD 软件中的集成。

## 为什么要将 CAD 导出为 PNG（或其他光栅格式）？

- **通用兼容性：** PNG 和 JPEG 几乎被所有图像查看器和浏览器支持。  
- **加载快速：** 与打开大型 DWG 文件相比，光栅图像加载瞬间完成。  
- **易于嵌入：** 可直接将 PNG 插入 Word、PowerPoint 或 HTML，无需额外插件。  
- **外观一致：** 您可以控制分辨率、背景和布局，确保每位利益相关者看到相同的视觉效果。  

## 常见使用场景

| 场景 | 光栅输出的优势 |
|----------|------------------------|
| **项目文档** | 在 PDF 或 Word 文档中嵌入 PNG，可避免审阅者需要 CAD 软件。 |
| **网页门户** | 从 DWG 文件生成的缩略图加载瞬间，提升用户体验。 |
| **移动应用** | 光栅图像可在缺少 CAD 查看器的设备上正确显示。 |
| **自动化报表** | 批量将多个布局转换为 PNG/JPEG，以便在图表或仪表盘中使用。 |

## 前置条件

在开始之前，请确保您已具备：

1. **Java 开发环境** – 已安装并配置 JDK 8 或更高版本。  
2. **Aspose.CAD for Java** – 从 [Aspose.CAD for Java 文档](https://reference.aspose.com/cad/java/) 下载最新 JAR 包。  

## 导入命名空间

首先，导入您需要的类。这些导入为您提供图像加载、栅格化选项以及 TIFF/PNG 输出设置的访问权限。

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

> **专业提示：** 如果您计划**将 CAD 导出为 PNG**而不是 TIFF，请将 `TiffOptions` 替换为 `PngOptions`（位于 `com.aspose.cad.imageoptions.PngOptions`）。

## 步骤指南

### 步骤 1：设置资源目录

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";
```

将 `"Your Document Directory"` 替换为存放 CAD 文件的绝对路径。

### 步骤 2：加载 CAD 文件

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

您可以加载任何受支持的格式（DWG、DXF、DGN 等）。这就是**如何将 cad 转换**的部分——只需指向文件，Aspose 即会处理解析。

### 步骤 3：配置栅格化选项

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1200);
rasterizationOptions.setPageHeight(1200);
rasterizationOptions.setLayouts(new String[] {"Model", "Layout1"});
```

- `setPageWidth` / `setPageHeight` 控制输出分辨率（数值越大 DPI 越高）。  
- `setLayouts` 让您**将 CAD 转换为光栅**时仅针对特定布局；若省略则栅格化整个图纸。

### 步骤 4：设置图像选项

```java
ImageOptionsBase options = new TiffOptions(TiffExpectedFormat.Default);
options.setVectorRasterizationOptions(rasterizationOptions);
```

如果您更倾向于 PNG，请实例化 `PngOptions` 而不是 `TiffOptions`。这正是**将 CAD 导出为 PNG**的地方。

### 步骤 5：保存生成的图像

```java
image.save(dataDir + "conic_pyramid_layoutstorasterimage_out_.tiff", options);
```

将文件扩展名改为 `.png`（并将选项对象改为 `PngOptions`）即可**将 CAD 保存为 JPEG/PNG**。

> **常见错误：** 文件扩展名与选项类不匹配会导致 `UnsupportedFormatException`。请始终保持两者一致。

## 常见问题及解决方案

| 问题 | 解决方案 |
|-------|----------|
| **输出图像为空白** | 确认 `setLayouts` 中的布局名称与源 CAD 文件中的完全一致。 |
| **PNG 分辨率低** | 增大 `setPageWidth` / `setPageHeight` 或在栅格化选项上设置 `setResolution`。 |
| **不支持的 DWG 版本** | 确保使用最新的 Aspose.CAD 版本；旧版本可能不支持较新的 DWG。 |
| **大文件内存错误** | 一次处理单页或增加 JVM 堆内存 (`-Xmx2g`)。 |

## 常见问答

**问：Aspose.CAD 是否兼容不同的 CAD 文件格式？**  
答：是的，支持 DWG、DXF、DGN 等多种格式。

**问：我可以自定义输出光栅图像的分辨率吗？**  
答：当然。可在 `CadRasterizationOptions` 中调整 `setPageWidth`、`setPageHeight` 或 `setResolution`。

**问：如何一次性转换多个 CAD 布局？**  
答：向 `setLayouts` 提供包含所有布局名称的数组，例如 `new String[]{"Model","Layout1","Layout2"}`。

**问：除了 TIFF 之外还有其他输出格式吗？**  
答：有——PNG、JPEG、BMP、PDF 等均可通过各自的 `*Options` 类使用。

**问：在哪里可以获取帮助或分享使用 Aspose.CAD 的经验？**  
答：访问 [Aspose.CAD 论坛](https://forum.aspose.com/c/cad/19) 获取社区支持和官方帮助。

## 结论

按照这些步骤，您即可**将 DWG 转换为 PNG**、**将 CAD 导出为 PNG**、**将 CAD 保存为 JPEG**，或生成任何所需的光栅格式。Aspose.CAD for Java 负责繁重的转换工作，让您专注于将高质量图像集成到应用、文档或网页门户中。

---

**最后更新：** 2026-02-17  
**测试环境：** Aspose.CAD for Java 24.12  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}