---
date: 2026-06-29
description: 了解如何使用 Aspose.CAD for Java 将 DWG 创建为 PDF 并自定义 PDF 布局。为 Java 开发者提供简便的集成方案。
keywords:
- create pdf from dwg
- convert cad to pdf
- pdf different page sizes
- export dwg to pdf
- customize pdf layout
linktitle: 单个 PDF 的不同布局
schemas:
- author: Aspose
  dateModified: '2026-06-29'
  description: Learn how to create PDF from DWG and customize PDF layout using Aspose.CAD
    for Java. Easy integration for Java developers.
  headline: Create PDF from DWG with Aspose.CAD for Java
  type: TechArticle
- questions:
  - answer: Yes, Aspose.CAD for Java integrates seamlessly with libraries such as
      Apache POI, Jackson, or Spring Boot.
    question: Can I use Aspose.CAD for Java with other Java libraries?
  - answer: Absolutely! You can access a free trial version [here](https://releases.aspose.com/).
    question: Is there a trial version available?
  - answer: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for community
      support and discussions.
    question: Where can I find additional support?
  - answer: You can obtain a temporary license [here](https://purchase.aspose.com/temporary-license/).
    question: How do I obtain a temporary license?
  - answer: Purchase the full version of Aspose.CAD for Java [here](https://purchase.aspose.com/buy).
    question: Where can I purchase the full version?
  type: FAQPage
second_title: Aspose.CAD Java API
title: 使用 Aspose.CAD for Java 将 DWG 转换为 PDF
url: /zh/java/other-cad-operations/single-pdf-different-layouts/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.CAD for Java 将 DWG 创建为 PDF

## 介绍

在本教程中，您将 **将 DWG 创建为 PDF** 并使用 Aspose.CAD for Java 应用多种页面尺寸布局。无论您需要生成建筑蓝图、工程示意图，还是面向营销的 PDF，以下步骤将展示如何在 Java 环境中将 CAD 图纸转换为 PDF、定制每个布局的尺寸，并生成一个包含多页的文档，全部无需离开 Java。

## 快速答案
- **本教程涵盖什么？** 将 DWG 图纸转换为包含多种页面尺寸的单个 PDF。  
- **需要哪个库？** Aspose.CAD for Java（最新版本）。  
- **我需要许可证吗？** 免费试用可用于开发；生产环境需要商业许可证。  
- **我可以导出其他格式吗？** 可以——API 还支持导出为 PNG、JPEG 和 SVG。  
- **Java 8 足够吗？** 该库兼容 Java 8 及更高版本的运行时。

## 什么是“从 DWG 创建 PDF”？

**从 DWG 创建 PDF** 指将原生 AutoCAD DWG 文件转换为 PDF 文档，同时保留矢量精度、图层和线宽，并允许布局自定义。Aspose.CAD 完全在内存中完成此转换，无需外部 CAD 软件，生成的 PDF 可直接编辑或打印。

## 为什么要自定义 DWG 的 PDF 布局？

Aspose.CAD 支持 **30 多种 CAD 格式**，并可生成最高 **500 MB** 的 PDF 而无需将整个文件加载到内存。通过为每个布局定义单独的页面尺寸，您可以生成符合 ISO、ANSI 或自定义尺寸的可打印图纸——这是一项可量化的优势，可节省时间并消除手动后处理。

## 前置条件

在开始之前，请确保具备以下条件：
- Java 环境：确保您的机器已安装 Java。  
- Aspose.CAD 库：从[download link](https://releases.aspose.com/cad/java/)下载并安装适用于 Java 的 Aspose.CAD 库。  
- 文档目录：为您的 DWG 图纸设置一个目录。

## 导入包

`CadImage` 类是 Aspose.CAD 的核心对象，表示内存中的 CAD 图纸。开始之前请先导入所需的命名空间：

```java
import com.aspose.cad.Image;
import com.aspose.cad.SizeF;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.VectorRasterizationOptions;
```

## 步骤 1：加载 CAD 图纸

`CadImage` 加载 DWG 文件并提供对其矢量数据的访问。首先将您的 CAD 图纸加载到 `CadImage` 对象中：

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
CadImage cadImage = (CadImage)Image.load(dataDir + "City skyway map.dwg");
```

## 步骤 2：配置光栅化选项

`RasterizationOptions` 定义在将 CAD 矢量光栅化并放入 PDF 之前的行为。为 CAD 图像设置光栅化选项：

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1000);
rasterizationOptions.setPageHeight(1000);
```

## 步骤 3：自定义布局页面尺寸

`PdfOptions` 允许您为 DWG 中的每个布局分配不同的页面尺寸。为 CAD 图纸中的多个布局定义自定义尺寸：

```java
rasterizationOptions.getLayoutPageSizes().addItem("ANSI C Plot", new SizeF(500, 1000));
rasterizationOptions.getLayoutPageSizes().addItem("8.5 x 11 Plot", new SizeF(1000, 100));
```

## 步骤 4：设置 PDF 选项

`PdfOptions` 是将光栅化设置和布局定义组合在一起的容器。配置 PDF 选项，包含光栅化设置：

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## 步骤 5：保存为 PDF

`PdfSaveOptions` 完成转换并写入输出文件。将处理后的 CAD 图像保存为 PDF：

```java
cadImage.save(dataDir + "singlePDF_out.pdf", pdfOptions);
```

恭喜！您已成功使用 Aspose.CAD for Java 将 **DWG 创建为 PDF**，并使用不同的页面尺寸。

## 常见问题及解决方案

- **输出 PDF 中出现空白页** – 确保 `PageSize` 值与 DWG 文件中实际布局尺寸匹配。  
- **大图纸出现内存不足错误** – 使用 `CadImage.load(..., LoadOptions)` 并调用 `LoadOptions.setLoadMode(LoadMode.Memory)` 以流式读取文件，而不是一次性加载全部。  
- **缩放不正确** – 调整 `RasterizationOptions.setPageWidth` 和 `setPageHeight` 以匹配所需的 DPI（每英寸点数）。

## 常见问答

**Q: 我可以将 Aspose.CAD for Java 与其他 Java 库一起使用吗？**  
A: 可以，Aspose.CAD for Java 可无缝集成 Apache POI、Jackson 或 Spring Boot 等库。

**Q: 是否提供试用版？**  
A: 当然！您可以在[here](https://releases.aspose.com/)获取免费试用版。

**Q: 我在哪里可以找到更多支持？**  
A: 请访问[Aspose.CAD forum](https://forum.aspose.com/c/cad/19)获取社区支持和讨论。

**Q: 我如何获取临时许可证？**  
A: 您可以在[here](https://purchase.aspose.com/temporary-license/)获取临时许可证。

**Q: 我在哪里可以购买完整版本？**  
A: 请在[here](https://purchase.aspose.com/buy)购买 Aspose.CAD for Java 的完整版本。

---

**最后更新：** 2026-06-29  
**测试环境：** Aspose.CAD for Java 24.10  
**作者：** Aspose

## 相关教程

- [使用 Aspose.CAD for Java 将 DWG 导出为 PDF 或光栅](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [使用 Aspose.CAD for Java 将 CAD 布局导出为 PDF](/cad/java/cad-export-options/export-cad-layouts-to-pdf/)
- [使用 Aspose.CAD for Java 将特定 DWG 布局导出为 PDF](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< blocks/products/products-backtop-button >}}
{{< /blocks/products/pf/main-wrap-class >}}