---
date: 2026-10-14
description: 了解 Java CAD 库 Aspose.CAD for Java 如何快速、准确地将 DWG 导出为 PDF 或光栅图像。
keywords:
- export dwg pdf
- high quality pdf
- dwg to pdf tutorial
- aspose cad java
- java cad library
lastmod: 2026-10-14
linktitle: 导出 DWG PDF 和光栅图像
og_description: 使用 Aspose.CAD for Java 快速导出 DWG 为 PDF。了解高质量 PDF 转换、光栅选项和授权的分步指南。
og_image_alt: Tutorial showing Java code to convert DWG drawings to PDF and raster
  formats with Aspose.CAD
og_title: 使用 Java CAD 库 Aspose.CAD 导出 DWG 为 PDF 和光栅图像
schemas:
- author: Aspose
  dateModified: '2026-10-14'
  description: Learn how the Java CAD library Aspose.CAD for Java can export DWG to
    PDF or raster images quickly and accurately.
  headline: Export DWG PDF and raster images using Java CAD library Aspose.CAD
  type: TechArticle
- description: Learn how the Java CAD library Aspose.CAD for Java can export DWG to
    PDF or raster images quickly and accurately.
  name: Export DWG PDF and raster images using Java CAD library Aspose.CAD
  steps:
  - name: Load the DWG file
    text: First, load your DWG drawing using the `Image` class. This creates an in‑memory
      representation that Aspose.CAD can work with.
  - name: Determine unit type
    text: Understanding whether the drawing uses metric or imperial units is essential
      for correct scaling. The helper method `IsMetric` (implementation omitted for
      brevity) returns a boolean flag.
  - name: Set rasterization options
    text: The `CadRasterizationOptions` class defines rasterization parameters such
      as DPI, page size, and unit conversion. Based on the unit system, configure
      page size, scaling, and the target unit type. These options drive how the DWG
      is rasterized before being wrapped into a PDF.
  - name: Configure PDF options (pdf options cad)
    text: The `PdfOptions` class specifies PDF‑specific settings, including compression
      and metadata. Create a `PdfOptions` instance and attach the rasterization settings.
      This tells Aspose.CAD how to embed the rasterized content into the final PDF.
  - name: Save as PDF
    text: The `save` method writes the image to the given file path using the supplied
      options. Finally, export the drawing to a PDF file. The `save` method takes
      the output path and the configured `PdfOptions`. When the code finishes, you’ll
      find **Saved.pdf** in your `DWGDrawings` folder, ready for distribu
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD for Java seamlessly integrates with popular Java frameworks
      such as Spring, Jakarta EE, and Android.
    question: Can I use Aspose.CAD for Java with other Java frameworks?
  - answer: Yes, you can obtain a temporary license **[obtain a temporary license](https://purchase.aspose.com/temporary-license/)**.
    question: Is a temporary license available for Aspose.CAD for Java?
  - answer: Visit the **[Aspose.CAD forum](https://forum.aspose.com/c/cad/19)** for
      assistance from the community and Aspose engineers.
    question: Where can I find support for Aspose.CAD for Java?
  - answer: You can purchase a license **[purchase a license](https://purchase.aspose.com/buy)**.
    question: How can I purchase a license for Aspose.CAD for Java?
  - answer: Aspose.CAD for Java supports both metric and imperial units, automatically
      detecting the drawing’s unit system.
    question: What units does Aspose.CAD for Java support?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- export dwg
- aspose.cad
- java cad conversion
title: 使用 Java CAD 库 Aspose.CAD 导出 DWG 为 PDF 和光栅图像
url: /zh/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Java CAD 库 Aspose.CAD 导出 DWG PDF 和光栅图像

## 介绍

将 DWG 导出为 PDF 是工程师、建筑师以及任何需要在不暴露原始文件格式的情况下共享 CAD 图纸的人员的常见需求。使用 **Aspose.CAD for Java**，您可以仅用几行 Java 代码 **export dwg pdf** — 或光栅图像 — 完成导出，同时保持矢量保真度和布局精度。本教程将指导您加载 DWG 文件、配置光栅化并将结果保存为高质量的 PDF 或图像。您还将了解为何 Aspose.CAD 是可靠的跨平台转换的首选 Java CAD 库。

如需仅针对 PDF 转换的专门指南，请参阅 [Export DWG to PDF tutorial](/java/cad-drawing-conversion/export-dwg-to-pdf/).

## 快速答案
- **本教程涵盖什么内容？** 使用 Aspose.CAD for Java 将 DWG 文件导出为 PDF 或光栅图像。  
- **我需要许可证吗？** 可获得免费临时许可证用于评估；生产环境需要完整许可证。  
- **支持哪个 Java 版本？** 任意 Java 8+ 运行时均可与最新的 Aspose.CAD Java API 配合使用。  
- **我可以将 DWG 转换为其他图像格式吗？** 可以——相同的光栅化选项可输出 PNG、JPEG、BMP 等。  
- **转换需要多长时间？** 对于标准图纸通常在一秒以内；较大的文件可能需要几秒钟。

## 为什么 Java CAD 库是 DWG 转换的最佳选择？

Aspose.CAD for Java 是最佳选择，因为它提供纯 Java 实现，无需本机 DLL，能够自动检测公制或英制单位，提供最高 1200 DPI 的光栅输出，并生成保留矢量的 PDF，无需外部依赖。该库还提供灵活的许可模式，让您可以从临时许可证开始并扩展到企业级使用。

## 什么是 “export dwg to pdf”？

`Export dwg pdf` 是将原生 DWG 绘图文件转换为 PDF 文档的过程，同时保留矢量数据、图层和比例。此转换生成的文件与设备无关，可在任何平台上查看，无需 AutoCAD。由于 PDF 保留了矢量信息，文本仍可搜索，图形在任何缩放级别下都保持清晰，非常适合文档编制、客户审阅和归档存储。

## 为什么在此转换中使用 Aspose.CAD Java？

您应该使用 Aspose.CAD Java，因为该库在内部处理单位转换、光栅化和 PDF 嵌入，消除了对第三方工具或复杂命令行管道的需求。其 API 为开发者而设计：单个 `Image` 对象表示绘图，少量配置对象即可微调 DPI、页面尺寸和压缩。这样可在 Windows、Linux 和 macOS 环境中实现一致、可重复的输出。

## 前提条件

- 基本的 Java 编程知识。  
- 已安装 Aspose.CAD for Java 库。如果您尚未下载，请获取 **[download Aspose.CAD for Java](https://releases.aspose.com/cad/java/)**。  
- 用于测试的 DWG 文件——本指南使用示例 **Bottom_plate.dwg**。

## 导入命名空间

在您的 Java 项目中，导入必要的类以启动转换：

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.UnitType;
```

## 分步指南

### 步骤 1：加载 DWG 文件

首先，使用 `Image` 类加载 DWG 绘图。这会创建 Aspose.CAD 可处理的内存表示。

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Bottom_plate.dwg";
Image objImage = Image.load(srcFile);
```

### 步骤 2：确定单位类型

了解绘图使用的是公制还是英制单位对于正确缩放至关重要。辅助方法 `IsMetric`（为简洁起见省略实现）返回布尔标志。

```java
Boolean currentUnitIsMetric = IsMetric(objImage.getUnitType());
int currentUnitCoefficient = objImage.getUnitType();
```

### 步骤 3：设置光栅化选项

`CadRasterizationOptions` 类定义光栅化参数，如 DPI、页面尺寸和单位转换。根据单位系统，配置页面尺寸、缩放和目标单位类型。这些选项决定 DWG 在包装成 PDF 前的光栅化方式。

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();

if (currentUnitIsMetric) {
    // Metric units
    double metersCoeff = 1 / 1000.0;
    double scaleFactor = metersCoeff / currentUnitCoefficient;
    rasterizationOptions.setPageWidth((float)(210 * scaleFactor));
    rasterizationOptions.setPageHeight((float)(297 * scaleFactor));
    rasterizationOptions.setUnitType(UnitType.Millimeter);
} else {
    // Imperial units
    rasterizationOptions.setPageWidth((float)(8.27f / currentUnitCoefficient));
    rasterizationOptions.setPageHeight((float)(11.69f / currentUnitCoefficient));
    rasterizationOptions.setUnitType(UnitType.Inch);
}
```

### 步骤 4：配置 PDF 选项（pdf options cad）

`PdfOptions` 类指定 PDF 特定设置，包括压缩和元数据。创建 `PdfOptions` 实例并附加光栅化设置。此操作告诉 Aspose.CAD 如何将光栅化内容嵌入最终 PDF。

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());
```

### 步骤 5：保存为 PDF

`save` 方法使用提供的选项将图像写入指定文件路径。最后，将绘图导出为 PDF 文件。`save` 方法接受输出路径和配置好的 `PdfOptions`。

```java
objImage.save(dataDir + "Saved.pdf", pdfOptions);
```

代码执行完毕后，您将在 `DWGDrawings` 文件夹中找到 **Saved.pdf**，可用于分发或归档。

## 如何使用 Java CAD 库将 DWG 转换为光栅图像？

您可以通过将 `PdfOptions` 替换为光栅专用选项类（如 `PngOptions` 或 `JpegOptions`）来将 DWG 转换为光栅格式。复用相同的 `CadRasterizationOptions` 实例，调整输出格式，并使用新的选项对象调用 `save` 方法。此方法只需一行代码即可生成 PNG、JPEG、BMP 或 TIFF 文件，保持工作流一致。

## 如何使用 PDF options CAD 生成 PDF DWG？

上述示例已经 **generates pdf dwg** 输出。要微调 PDF 大小，可通过调用 `pdfOptions.setCompress(true)` 启用压缩。您还可以嵌入自定义元数据、设置 PDF 版本或通过额外的 `PdfOptions` 属性添加密码保护。这些调整让您无需离开 Java 代码库即可完全控制最终 PDF。

## 常见问题与技巧

- **页面尺寸不正确** – 仔细检查单位转换逻辑；系数不匹配可能导致页面过大。  
- **缺少字体或线宽** – 确保 DWG 在转换前引用了所有外部资源。  
- **大型图纸的性能** – 仅在需要更高质量时提升 `CadRasterizationOptions` 中的 `DPI` 设置；降低 DPI 可加快处理速度。  
- **许可证问题** – 评估时可使用 **temporary license Aspose**；生产部署需要完整许可证。

## 常见问答

**Q: 我可以将 Aspose.CAD for Java 与其他 Java 框架一起使用吗？**  
A: 可以，Aspose.CAD for Java 可无缝集成到流行的 Java 框架，如 Spring、Jakarta EE 和 Android。

**Q: Aspose.CAD for Java 是否提供临时许可证？**  
A: 可以，您可以获取临时许可证 **[obtain a temporary license](https://purchase.aspose.com/temporary-license/)**。

**Q: 我在哪里可以找到 Aspose.CAD for Java 的支持？**  
A: 请访问 **[Aspose.CAD forum](https://forum.aspose.com/c/cad/19)** 获取社区和 Aspose 工程师的帮助。

**Q: 我如何购买 Aspose.CAD for Java 的许可证？**  
A: 您可以购买许可证 **[purchase a license](https://purchase.aspose.com/buy)**。

**Q: Aspose.CAD for Java 支持哪些单位？**  
A: Aspose.CAD for Java 同时支持公制和英制单位，能够自动检测绘图的单位系统。

**Q: 我可以使用相同的 API 将 DWG 转换为其他图像格式（例如 PNG、JPEG）吗？**  
A: 当然可以。将 `PdfOptions` 替换为相应的光栅图像选项（例如 `PngOptions`），并复用相同的 `CadRasterizationOptions`。

## 结论

本教程演示了如何使用 **java cad library** Aspose.CAD for Java **export dwg pdf** 并导出光栅图像。通过遵循分步指南，您可以将可靠的 CAD 转换集成到任何 Java 应用程序中，无论是用于文档的 PDF 还是用于网页显示的光栅图像。该库的纯 Java 特性、高质量输出和灵活的许可模式，使其成为小型工具和大规模企业流水线的可靠选择。

---

**最后更新：** 2026-10-14  
**测试环境：** Aspose.CAD for Java 24.10  
**作者：** Aspose

## 相关教程

- [使用 Aspose.CAD for Java 导出 DWG 为 PDF：特定布局](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [在 Java 中导出 DWG 为 PDF – 使用 Aspose.CAD 设置 PDF 页面尺寸](/cad/java/cad-export-options/export-to-pdf/)
- [使用 Aspose.CAD for Java 导出带隐藏线的 DWG 为 PDF](/cad/java/cad-text-and-formatting/support-hidden-lines-in-dwg/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}