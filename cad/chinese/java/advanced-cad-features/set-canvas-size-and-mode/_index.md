---
date: 2026-08-29
description: 了解如何使用 Aspose.CAD for Java 设置 pdf 页面大小并将 CAD 转换为 PDF，支持自动布局缩放和 TIFF 导出。
keywords:
- set pdf page size
- convert cad to pdf
- canvas size java
- high resolution tiff
- change pdf dimensions
lastmod: 2026-08-29
linktitle: 设置 pdf 页面大小 – 将 cad 转换为 pdf
og_description: 了解如何在 Java 中使用 Aspose.CAD 将 CAD 图纸转换为 PDF 时设置 pdf 页面大小。本指南涵盖画布尺寸、自动布局缩放以及导出高分辨率
  TIFF。
og_image_alt: Tutorial showing how to set pdf page size and convert CAD to PDF in
  Java
og_title: 设置 pdf 页面大小 – 使用 Aspose 在 Java 中将 CAD 转换为 PDF
schemas:
- author: Aspose
  dateModified: '2026-08-29'
  description: Learn how to set pdf page size and convert CAD to PDF using Aspose.CAD
    for Java, with automatic layout scaling and TIFF export.
  headline: Set pdf page size – convert cad to pdf (Java)
  type: TechArticle
- questions:
  - answer: No. Canvas size controls page dimensions; vector data remains resolution‑independent,
      ensuring crisp rendering at any zoom level.
    question: does the canvas size affect vector quality in the PDF?
  - answer: Yes. Adjust `rasterizationOptions.setResolution(dpiValue)` before creating
      `TiffOptions`.
    question: can I set a different DPI for the TIFF output?
  - answer: Use Aspose.PDF to load the generated PDF and call `pdf.getPages().setPageSize(PageSize.A4)`
      or a custom size.
    question: how can I change PDF dimensions for an existing PDF without re‑rendering
      the CAD?
  - answer: Keep `setAutomaticLayoutsScaling(true)` and avoid `setNoScaling(true)`;
      this retains layer visibility and layout fidelity.
    question: what is the best way to convert dxf to pdf while preserving layers?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- set pdf page size
- convert cad
- Aspose.CAD
- Java
- high resolution tiff
title: 设置 pdf 页面大小 – 将 cad 转换为 pdf（Java）
url: /zh/java/advanced-cad-features/set-canvas-size-and-mode/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 设置 PDF 页面大小 – 将 CAD 转换为 PDF (Java)

## 介绍

如果您需要在将 CAD 图纸转换为 PDF 时**设置 PDF 页面大小**，那么您来对地方了。在本教程中，我们将展示如何使用 Aspose.CAD for Java 来定义精确的画布尺寸，启用自动布局缩放，然后将结果导出为 PDF 和 TIFF。无论是为打印准备工程示意图，还是为网页画廊生成缩略图，控制页面大小和输出分辨率都是必不可少的。

## 快速回答
- **“convert CAD to PDF” 是什么意思？** 将 CAD 图纸（例如 DXF、DWG）转换为可以在任何平台上查看的 PDF 文档。
- **Can I also export to TIFF?** 是的——使用 `TiffOptions` 创建高分辨率光栅图像。
- **哪个选项在 Java 中控制画布大小？** `CadRasterizationOptions.setPageWidth/Height`。
- **What is automatic layout scaling?** 当画布大小变化时，保持原始布局比例的标志 (`setAutomaticLayoutsScaling(true)`)。
- **Do I need a license for Aspose.CAD?** 生产使用需要临时或永久许可证。

## 在 Java 中将 CAD 转换为 PDF 时如何设置 PDF 页面大小

加载 CAD 文件，使用所需的宽度和高度配置 `CadRasterizationOptions`，启用自动布局缩放，然后将结果保存为 PDF。这种两步方法让您在不牺牲矢量质量的前提下，精确控制输出页面的尺寸。

## 什么是将 CAD 转换为 PDF？

将 CAD 转换为 PDF 是指将基于矢量的工程图纸渲染为 PDF 页面，保留线条、图层和几何形状，同时使文件能够在任何平台上通用访问。该过程根据指定的选项对图纸进行光栅化，生成的 PDF 可在任何设备上打开，无需 CAD 软件，并保持原始设计的视觉保真度。

## 为什么在 Java 中设置画布大小？

在 Java 中设置画布大小可以定义输出分辨率和页面尺寸，确保生成的 PDF 或 TIFF 符合您的打印或显示需求。它还让您能够控制缩放行为，这对于大幅图纸至关重要。

## 前置条件

- Aspose.CAD for Java：确保在您的 Java 环境中已安装 Aspose.CAD 库。您可以在[此处](https://releases.aspose.com/cad/java/)下载 Aspose.CAD for Java 库。
- 文档目录：设置一个文档目录来存放您的 CAD 文件。该目录将在教程步骤中被引用。

现在，让我们开始逐步指南。

## 导入命名空间

在此步骤中，我们将导入必要的命名空间以启动您的 Aspose.CAD 项目。

`Image` 是用于加载 CAD 文件的主要类。

```java
import java.awt.Image;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## 步骤 1：导入 Aspose.CAD 类

`Image` 类提供加载和保存 CAD 图纸的方法。

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
com.aspose.cad.Image objImage = com.aspose.cad.Image.load(srcFile);
```

在此代码片段中，我们设置资源目录的路径，并使用 Aspose.CAD 的 `Image` 类加载 DXF 文件。

## 步骤 2：设置 CadRasterizationOptions 属性（在 Java 中设置画布大小）

`CadRasterizationOptions` 指定 CAD 转光栅转换的光栅化设置，例如页面大小和缩放。

```java
// Create an instance of CadRasterizationOptions and set its various properties
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

这里，我们创建 `CadRasterizationOptions` 的实例，并配置页面宽度、页面高度以及**自动布局缩放**等属性。这是您转换过程中**配置画布模式**的核心。

## 步骤 3：创建 PdfOptions 并设置 vectorRasterizationOptions

`PdfOptions` 定义转换的 PDF 输出设置。

```java
// Create an instance of PdfOptions
PdfOptions pdfOptions = new PdfOptions();

// Set the VectorRasterizationOptions property
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

现在，我们创建 `PdfOptions` 实例，并将其 `VectorRasterizationOptions` 属性设置为先前配置的 `CadRasterizationOptions`。

## 步骤 4：导出为 PDF（将 CAD 转换为 PDF）

```java
// Export CAD to PDF
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

最后，我们使用指定的选项将 CAD 图像保存为 PDF 文件，完成 **将 CAD 转换为 PDF** 的过程。

## 步骤 5：创建 TiffOptions 并设置 vectorRasterizationOptions（将 CAD 导出为 TIFF）

`TiffOptions` 配置 TIFF 输出参数，例如压缩和分辨率。

```java
// Create an instance of TiffOptions
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);

// Set the VectorRasterizationOptions property
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
```

在此步骤中，我们设置 `TiffOptions` 实例并配置其 `VectorRasterizationOptions` 属性。

## 步骤 6：导出为 TIFF

```java
// Export CAD to TIFF
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

最后，我们使用指定的选项将 CAD 图像保存为 TIFF 文件，演示在配置画布大小后如何**将 CAD 导出为 TIFF**。

## 常见问题及解决方案

| 问题 | 原因 | 解决方案 |
|-------|-------|-----|
| 输出 PDF 为空 | `setNoScaling(true)` 会导致某些图纸不渲染 | 移除 `setNoScaling(true)` 或将其设为 `false`。 |
| TIFF 分辨率低 | 页面宽度/高度太小 | 增大 `setPageWidth` / `setPageHeight` 的数值。 |
| 布局失真 | 自动布局缩放被禁用 | 确保已启用 `setAutomaticLayoutsScaling(true)`。 |

## 为什么要调整画布大小和 DPI？

更改画布大小会直接影响输出的光栅化分辨率。如果需要**提高 TIFF 分辨率**，只需在创建 `TiffOptions` 之前提升 `setPageWidth` / `setPageHeight` 的数值，或调用 `rasterizationOptions.setResolution(300)`。这将为您提供适合打印或细致检查的高质量光栅图像。

## 常见问答

**Q1: 我可以将 Aspose.CAD for Java 与其他 Java 框架一起使用吗？**  
A: 是的，Aspose.CAD 旨在与各种 Java 框架无缝集成。

**Q2: 是否提供 Aspose.CAD 的临时许可证？**  
A: 是的，您可以在[此处](https://purchase.aspose.com/temporary-license/)获取临时许可证页面。

**Q3: 我在哪里可以获得 Aspose.CAD 的社区支持？**  
A: 请访问 Aspose.CAD 论坛 [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) 获取社区支持和讨论。

**Q4: 我可以免费试用 Aspose.CAD 吗？**  
A: 当然！在[此处](https://releases.aspose.com/)获取免费试用下载页面。

**Q5: 我如何购买 Aspose.CAD for Java？**  
A: 在[此处](https://purchase.aspose.com/buy)购买 Aspose.CAD for Java。

**Q: 画布大小会影响 PDF 中的矢量质量吗？**  
A: 不会。画布大小仅控制页面尺寸；矢量数据保持分辨率无关，确保在任何缩放级别下都能清晰渲染。

**Q: 我可以为 TIFF 输出设置不同的 DPI 吗？**  
A: 可以。在创建 `TiffOptions` 之前调整 `rasterizationOptions.setResolution(dpiValue)`。

**Q: 如何在不重新渲染 CAD 的情况下更改已有 PDF 的尺寸？**  
A: 使用 Aspose.PDF 加载生成的 PDF，并调用 `pdf.getPages().setPageSize(PageSize.A4)` 或自定义尺寸。

**Q: 将 dxf 转换为 pdf 时，如何在保留图层的同时获得最佳效果？**  
A: 保持 `setAutomaticLayoutsScaling(true)` 并避免使用 `setNoScaling(true)`；这可保留图层可见性和布局保真度。

## 结论

恭喜！您已成功**将 CAD 转换为 PDF**并**将 CAD 导出为 TIFF**，同时**在 Java 中设置画布大小**，实现了**自动布局缩放**，并学习了如何**配置画布模式**以获得高质量输出。本教程为您的 CAD 转换项目提供了坚实的基础。请在 [Aspose.CAD 文档](https://reference.aspose.com/cad/java/) 中探索更多功能和可能性。

**最后更新：** 2026-08-29  
**测试环境：** Aspose.CAD for Java 24.12  
**作者：** Aspose

## 相关教程

- [设置画布大小 – 使用 Aspose.CAD for Java 的高级 CAD 功能](/cad/java/advanced-cad-features/)
- [在 Java 中将 DWG 导出为 PDF – 使用 Aspose.CAD 设置 PDF 页面大小](/cad/java/cad-export-options/export-to-pdf/)
- [设置自定义页面大小 – 使用自动布局缩放从 CAD 生成 PDF](/cad/java/advanced-cad-features/setting-auto-layout-scaling/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}