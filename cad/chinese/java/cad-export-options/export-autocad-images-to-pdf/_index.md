---
date: 2026-10-19
description: 了解如何使用 Aspose.CAD 在 Java 中将 DWG 转换为 PDF。本分步指南展示了如何导出 AutoCAD PDF、将 CAD
  保存为 PDF，以及如何应用许可证。
keywords:
- dwg to pdf java
- export autocad pdf
- java pdf export library
- aspose cad license
- save cad pdf
- customize pdf page size
lastmod: 2026-10-19
linktitle: 导出 AutoCAD 图像为 PDF
og_description: 了解如何使用 Aspose.CAD 在 Java 中将 DWG 转换为 PDF。本指南带您一步步完成导出 AutoCAD PDF、将
  CAD 保存为 PDF，以及许可证的使用。
og_image_alt: 'Tutorial: convert DWG to PDF in Java with Aspose.CAD'
og_title: 使用 Aspose.CAD 在 Java 中将 DWG 转换为 PDF
schemas:
- author: Aspose
  dateModified: '2026-10-19'
  description: Learn how to convert DWG to PDF in Java with Aspose.CAD. This step‑by‑step
    guide shows you how to export AutoCAD PDF, save CAD as PDF, and apply a license.
  headline: Convert DWG to PDF in Java using Aspose.CAD
  type: TechArticle
- description: Learn how to convert DWG to PDF in Java with Aspose.CAD. This step‑by‑step
    guide shows you how to export AutoCAD PDF, save CAD as PDF, and apply a license.
  name: Convert DWG to PDF in Java using Aspose.CAD
  steps:
  - name: set the resource directory path
    text: Replace `"Your Document Directory"` with the absolute path to the folder
      you created in the prerequisites. > **Pro tip:** Use `Paths.get(...).toAbsolutePath()`
      to avoid path‑related errors on different operating systems.
  - name: load the CAD image
    text: Loading the CAD file into an `Image` object gives you full access to Aspose.CAD’s
      rasterization engine. The `Image` class loads the DWG file and prepares it for
      conversion. > **Why this matters:** Once the drawing is in memory, you can query
      its layouts, layers, and metadata before rasterizing.
  - name: set rasterization options
    text: Adjust `pageWidth` and `pageHeight` to **customize PDF page size**. Enabling
      `setTypeOfEntities(TypeOfEntities.Entities3D)` allows full 3‑D rendering when
      needed. The `RasterizationOptions` object controls DPI, page dimensions, and
      entity types for the output. - `pageWidth` / `pageHeight` are measur
  - name: configure PDF options
    text: Tie the rasterization settings to the PDF output, ensuring the vector data
      is correctly transformed. The `PdfOptions` class links the rasterization configuration
      with the final PDF file.
  - name: save the PDF
    text: The resulting file, `Export3DImagestoPDF_out_.pdf`, is a **save cad as pdf**
      representation of your original AutoCAD drawing. The `save` method writes the
      rasterized image to a PDF file on disk.
  type: HowTo
- questions:
  - answer: Yes – the library supports DWG, DXF, DWF, DGN, and over 30 additional
      formats, giving you flexibility across projects.
    question: Can I use Aspose.CAD for Java with other CAD file formats?
  - answer: Visit the [temporary license page](https://purchase.aspose.com/temporary-license/)
      to request a time‑limited license for evaluation.
    question: How do I obtain a temporary license for Aspose.CAD for Java?
  - answer: Absolutely. Use `setLayouts("Model")`, `setLayouts("Layout1")`, etc.,
      to choose which view is rendered into the PDF.
    question: Are there layout options for rasterization?
  - answer: Yes – modify `pageWidth` and `pageHeight` in the rasterization options
      to match any required page dimensions.
    question: Can I change the size of the output PDF file?
  - answer: The dedicated community is available at the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19)
      where you can ask questions and share solutions.
    question: Where can I get help if I run into problems?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- dwg to pdf
- aspose.cad
- java cad conversion
- export autocad pdf
title: 使用 Aspose.CAD 在 Java 中将 DWG 转换为 PDF
url: /zh/java/cad-export-options/export-autocad-images-to-pdf/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 导出 AutoCAD PDF – 使用 Aspose.CAD for Java 导出 AutoCAD 图像为 PDF

## 简介

如果您需要在 Java 中 **将 DWG 转换为 PDF**，那么您来对地方了。本教程展示如何使用 Aspose.CAD for Java 将 AutoCAD 图像导出为 PDF，这是一款纯 Java 库，可处理 DWG、DXF、DWF 以及许多其他 CAD 格式，无需本地依赖。完成后，您将能够 **将 CAD 保存为 PDF**，调整如页面尺寸等光栅化选项，并正确应用 **Aspose CAD 许可证** 以用于生产环境。

## 快速答案

- **我可以使用 Java 将 DWG 转换为 PDF 吗？** 是的 – Aspose.CAD for Java 原生支持 DWG、DXF 以及数十种其他 CAD 格式。  
- **我需要许可证吗？** 永久的 **Aspose CAD 许可证** 可移除所有评估限制；也提供临时许可证用于测试。  
- **支持哪些 Java 版本？** 完全支持 Java 8 及更高版本。  
- **我可以控制 PDF 页面尺寸吗？** 当然可以 – 在光栅化选项中设置 `pageWidth` 和 `pageHeight`。  
- **是否支持 3‑D 渲染？** 是的 – 启用 `TypeOfEntities.Entities3D` 可对 3‑D 实体进行光栅化。

## 什么是导出 AutoCAD PDF？

导出 AutoCAD PDF 是将矢量 CAD 图纸转换为可携带的 PDF 文档的过程。它保留图层、线宽、颜色，并可选地保留 3‑D 几何形状，使得与客户共享设计或在无需 CAD 软件的情况下进行归档变得简便。

## 为什么使用 Aspose.CAD for Java 将 DWG 转换为 PDF？

Aspose.CAD 支持 **50 多种输入和输出格式**，能够在不将整个文件加载到内存的情况下处理数百页的图纸，并可在任何支持 Java 8+ 的平台上运行。该库让您完全控制 DPI、页面尺寸和布局，您可以 **自定义 PDF 页面尺寸** 以匹配精确的项目规范，且无需安装本地 DLL。

## 先决条件

- **Java Development Kit** – 在工作站上安装 JDK 8 或更高版本。  
- **Aspose.CAD for Java** – 从 [download link](https://releases.aspose.com/cad/java/) 下载最新的 JAR。  
- **工作目录** – 用于存放源 DWG 文件和生成的 PDF 的文件夹。

## 导入命名空间

`Image` 类表示任何可光栅化的 CAD 图纸，而 `RasterizationOptions` 和 `PdfOptions` 让您可以微调转换过程。

`Image` 类是 Aspose.CAD 的顶层对象，用于在内存中保存 CAD 图纸。

`RasterizationOptions` 类定义在写入 PDF 之前如何对矢量数据进行光栅化。

`PdfOptions` 类将光栅化设置与 PDF 特定的输出参数捆绑在一起。

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

现在让我们一步一步地浏览代码。

## 如何使用 Aspose.CAD for Java 将 DWG 转换为 PDF？

要使用 Aspose.CAD for Java 将 DWG 文件转换为 PDF，首先使用 Image 类加载图纸，配置 CadRasterizationOptions（如 DPI、页面尺寸和实体类型），将这些选项包装在 PdfOptions 中，然后调用 save 方法并指定 .pdf 文件名。此流程确保矢量数据被正确光栅化，生成的 PDF 符合您的布局要求。

### 步骤 1：设置资源目录路径

将 `"Your Document Directory"` 替换为您在先决条件中创建的文件夹的绝对路径。

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
```

> **小贴士：** 使用 `Paths.get(...).toAbsolutePath()` 可避免在不同操作系统上出现路径相关错误。

### 步骤 2：加载 CAD 图像

将 CAD 文件加载到 `Image` 对象中，可让您完全访问 Aspose.CAD 的光栅化引擎。

`Image` 类加载 DWG 文件并为转换做好准备。

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

> **为什么重要：** 一旦图纸在内存中，您就可以在光栅化之前查询其布局、图层和元数据。

### 步骤 3：设置光栅化选项

调整 `pageWidth` 和 `pageHeight` 以 **自定义 PDF 页面尺寸**。启用 `setTypeOfEntities(TypeOfEntities.Entities3D)` 可在需要时实现完整的 3‑D 渲染。

`RasterizationOptions` 对象控制输出的 DPI、页面尺寸和实体类型。

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setPageHeight(500);
// rasterizationOptions.setTypeOfEntities(TypeOfEntities.Entities3D);

rasterizationOptions.setLayouts(new String[] {"Model"});
```

- `pageWidth` / `pageHeight` 以点为单位（1 pt = 1/72 in）。  
- 取消注释 `setTypeOfEntities` 行以进行 3‑D 光栅化。  
- `setLayouts` 选择要渲染的布局（Model、Layout1 等）。

### 步骤 4：配置 PDF 选项

将光栅化设置绑定到 PDF 输出，确保矢量数据被正确转换。

`PdfOptions` 类将光栅化配置与最终的 PDF 文件关联起来。

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### 步骤 5：保存 PDF

生成的文件 `Export3DImagestoPDF_out_.pdf` 是您原始 AutoCAD 图纸的 **save cad as pdf** 表示。

`save` 方法将光栅化的图像写入磁盘上的 PDF 文件。

```java
cadImage.save(dataDir + "Export3DImagestoPDF_out_.pdf", pdfOptions);
```

## 常见问题与解决方案

| 症状 | 可能原因 | 解决办法 |
|---------|--------------|-----|
| 空白 PDF 输出 | 未设置光栅化选项或布局不匹配 | 确认 `setLayouts` 与 CAD 文件中的布局名称匹配。 |
| 低分辨率图像 | `pageWidth`/`pageHeight` 过小 | 增大尺寸或通过 `rasterizationOptions.setResolution(...)` 设置更高的 DPI。 |
| 许可证异常 | 未应用有效许可证 | 应用 **Aspose CAD 许可证** 或使用临时许可证进行测试。 |

## 常见问题

**Q: 我可以在 Java 中使用 Aspose.CAD 处理其他 CAD 文件格式吗？**  
A: 是的 – 该库支持 DWG、DXF、DWF、DGN 以及超过 30 种其他格式，为您的项目提供灵活性。

**Q: 我如何获取 Aspose.CAD for Java 的临时许可证？**  
A: 请访问 [temporary license page](https://purchase.aspose.com/temporary-license/) 以申请用于评估的限时许可证。

**Q: 是否有光栅化的布局选项？**  
A: 当然。使用 `setLayouts("Model")`、`setLayouts("Layout1")` 等来选择要渲染到 PDF 的视图。

**Q: 我可以更改输出 PDF 文件的大小吗？**  
A: 可以 – 在光栅化选项中修改 `pageWidth` 和 `pageHeight` 以匹配任何所需的页面尺寸。

**Q: 如果遇到问题，我可以在哪里获取帮助？**  
A: 可在 [Aspose.CAD 论坛](https://forum.aspose.com/c/cad/19) 的专属社区提问并分享解决方案。

---

**最后更新:** 2026-10-19  
**测试环境:** Aspose.CAD for Java 24.10  
**作者:** Aspose

## 相关教程

- [在 Java 中导出 DWG 为 PDF – 使用 Aspose.CAD 设置 PDF 页面尺寸](/cad/java/cad-export-options/export-to-pdf/)
- [导出 DWG 为 PDF：使用 Aspose.CAD for Java 的特定布局](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [导出 DWG 为 PDF 并使用 Aspose.CAD Java 启用跟踪](/cad/java/additional-features/enable-tracking/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}