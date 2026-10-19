---
date: 2026-10-19
description: 了解如何使用 Aspose.CAD for Java 将 AutoCAD 图纸导出为自定义 PDF 页面尺寸的 PDF。本分步指南涵盖 DWG
  转 PDF、光栅化选项和授权信息。
keywords:
- custom pdf page size
- export autocad to pdf
- save cad as pdf
- generate pdf from dwg
- dwg to pdf java
lastmod: 2026-10-19
linktitle: 导出 AutoCAD 图像为 PDF
og_description: 使用 Aspose.CAD for Java 导出 AutoCAD 图纸为 PDF 时设置自定义 PDF 页面尺寸。几分钟内了解 DWG
  转 PDF、光栅化设置和授权信息。
og_image_alt: Guide showing how to export AutoCAD drawings to PDF with custom page
  dimensions using Aspose.CAD for Java
og_title: 使用 Aspose.CAD 设置 AutoCAD 导出自定义 PDF 页面尺寸
schemas:
- author: Aspose
  dateModified: '2026-10-19'
  description: Learn how to export AutoCAD drawings to PDF with a custom PDF page
    size using Aspose.CAD for Java. This step‑by‑step guide covers converting DWG
    to PDF, rasterization options, and licensing.
  headline: Set custom PDF page size for AutoCAD export with Aspose.CAD
  type: TechArticle
- description: Learn how to export AutoCAD drawings to PDF with a custom PDF page
    size using Aspose.CAD for Java. This step‑by‑step guide covers converting DWG
    to PDF, rasterization options, and licensing.
  name: Set custom PDF page size for AutoCAD export with Aspose.CAD
  steps:
  - name: set the resource directory path
    text: '> **Pro tip:** Replace `"Your Document Directory"` with the absolute path
      to the folder you created in the prerequisites.'
  - name: load the CAD image
    text: The `Image` class loads the CAD file and gives you access to Aspose.CAD’s
      rasterization engine. > **Why this matters:** Once the CAD file is loaded, you
      can manipulate rasterization options before rendering to PDF.
  - name: set rasterization options
    text: The `CadRasterizationOptions` class specifies how the CAD drawing is rasterized
      before being saved as PDF. Adjust `pageWidth` and `pageHeight` to define a **custom
      PDF page size**. You can also enable 3‑D rendering by uncommenting the `setTypeOfEntities`
      line. - `pageWidth` / `pageHeight` – measured
  - name: configure PDF options
    text: The `PdfOptions` class holds PDF‑specific settings and links the rasterization
      options to the output file, ensuring the custom page dimensions are applied
      correctly.
  - name: save the PDF
    text: The `save` method writes the rendered image to the specified PDF file. The
      resulting file, `Export3DImagestoPDF_out_.pdf`, is a **save cad as pdf** representation
      of your original AutoCAD drawing with the exact page dimensions you specified.
  type: HowTo
- questions:
  - answer: Yes, the library supports DWG, DXF, DWF, DGN, and many more, giving you
      flexibility across projects.
    question: Can I use Aspose.CAD for Java with other CAD file formats?
  - answer: Visit the [temporary license page](https://purchase.aspose.com/temporary-license/)
      to request a time‑limited license for evaluation.
    question: How do I obtain a temporary license for Aspose.CAD for Java?
  - answer: Absolutely. Use `setLayouts("Model")` or specify other layout names to
      control which view is rendered.
    question: Are there layout options for rasterization?
  - answer: Yes – modify `pageWidth` and `pageHeight` in the rasterization options
      to any dimensions you need.
    question: Can I customize the size of the output PDF file?
  - answer: The dedicated [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) offers
      community support and official responses from the Aspose team.
    question: Where can I get help or discuss issues related to Aspose.CAD for Java?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- custom pdf page size
- Aspose.CAD
- Java CAD conversion
- PDF generation
- DWG export
title: 使用 Aspose.CAD 设置 AutoCAD 导出自定义 PDF 页面尺寸
url: /zh/java/cad-export-options/export-autocad-images-to-pdf/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 导出 AutoCAD PDF - 使用 Aspose.CAD for Java 将 AutoCAD 图像导出为 PDF

## 介绍

如果您需要 **将 DWG 转换为 PDF** 并控制输出文件的精确尺寸，您来对地方了。本教程将向您展示如何在使用 Aspose.CAD for Java 将 AutoCAD 图像导出为 PDF 时设置 **自定义 PDF 页面尺寸**。完成本指南后，您将了解如何加载 DWG、配置光栅化选项（如 DPI 和页面宽度/高度）、应用许可证以及生成可投入生产的 PDF。

## 快速答案
- **我可以使用 Java 将 DWG 转换为 PDF 吗？** 是的 – Aspose.CAD for Java 原生支持 DWG、DXF、DWF 以及许多其他 CAD 格式。  
- **生产使用是否需要许可证？** 完整的 Aspose.CAD 许可证可移除所有评估限制；也提供临时许可证用于测试。  
- **兼容哪些 Java 版本？** 该库兼容 Java 8 及更高版本的 JDK。  
- **如何更改 PDF 页面尺寸？** 在 `PdfOptions.getRasterizationOptions()` 上设置 `pageWidth` 和 `pageHeight` 为所需的任意尺寸。  
- **是否支持 3‑D 渲染？** 是的 – 启用 `TypeOfEntities.Entities3D` 可光栅化 3‑D 实体。

## 什么是导出 AutoCAD PDF？
导出 AutoCAD PDF 指将基于矢量的 CAD 图纸（DWG、DXF、DWF 等）转换为可移植的 PDF 文档，同时保留图层、线宽以及可选的 3‑D 几何信息。这使您能够在不安装 CAD 软件的情况下与客户共享设计、归档图纸或直接打印。

## 为什么使用 Aspose.CAD for Java 将 DWG 转换为 PDF？
Aspose.CAD for Java 是将 DWG 转换为 PDF 的理想选择，因为它提供了广泛的格式支持、纯 Java 实现无需本地依赖、具备高分辨率光栅化并可完全控制 DPI 与页面尺寸，同时提供灵活的授权模式，让您可以先使用试用版再升级到正式版。

- **广泛的格式覆盖** – 支持 50 多种输入和输出格式，包括 DWG、DXF、DWF、DGN 和 PDF。  
- **纯 Java 实现** – 无需本机 DLL 或外部依赖，部署在任何平台上都非常简便。  
- **高分辨率光栅化** – 您可以指定 DPI、页面尺寸和布局，从而对结果的 **自定义 PDF 页面尺寸** 拥有完整控制。  
- **可扩展的授权** – 可先使用免费试用版，然后升级为永久的 **Aspose CAD 许可证**。  

## 前提条件

- **Java Development Kit** – 在您的机器上已安装 JDK 8 或更高版本。  
- **Aspose.CAD for Java** – 从 [下载链接](https://releases.aspose.com/cad/java/) 下载最新的 JAR 包。  
- **工作目录** – 包含源 DWG 文件并将接收生成的 PDF 的文件夹。

## 导入命名空间

`Image` 类是 Aspose.CAD 的核心对象，表示内存中的 CAD 图纸。在编写代码之前请先导入所需的包。

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

现在让我们逐步浏览代码。

## 如何在将 DWG 导出为 PDF 时设置自定义 PDF 页面尺寸？

加载 DWG，定义所需的页面宽度和高度，然后将结果保存为 PDF —— 这就是创建具有自定义页面尺寸的 PDF 所需的全部步骤。以下步骤展示了确切的顺序以及所需的最小代码。

### 步骤 1：设置资源目录路径

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
```

> **技巧提示：** 将 `"Your Document Directory"` 替换为您在前提条件中创建的文件夹的绝对路径。

### 步骤 2：加载 CAD 图像

`Image` 类加载 CAD 文件并让您访问 Aspose.CAD 的光栅化引擎。

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

> **重要原因：** 一旦加载了 CAD 文件，您就可以在渲染为 PDF 之前操作光栅化选项。

### 步骤 3：设置光栅化选项

`CadRasterizationOptions` 类指定在保存为 PDF 之前如何对 CAD 图纸进行光栅化。调整 `pageWidth` 和 `pageHeight` 以定义 **自定义 PDF 页面尺寸**。您还可以通过取消注释 `setTypeOfEntities` 行来启用 3‑D 渲染。

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setPageHeight(500);
// rasterizationOptions.setTypeOfEntities(TypeOfEntities.Entities3D);

rasterizationOptions.setLayouts(new String[] {"Model"});
```

- `pageWidth` / `pageHeight` – 以像素为单位；更改这些值以匹配 A4、Letter 或任何自定义尺寸。  
- `setTypeOfEntities(TypeOfEntities.Entities3D)` – 在需要时渲染 3‑D 实体。  
- `setLayouts` – 选择要光栅化的布局（Model、Layout1 等）。

### 步骤 4：配置 PDF 选项

`PdfOptions` 类保存 PDF 特定设置，并将光栅化选项链接到输出文件，确保正确应用自定义页面尺寸。

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### 步骤 5：保存 PDF

`save` 方法将渲染后的图像写入指定的 PDF 文件。

```java
cadImage.save(dataDir + "Export3DImagestoPDF_out_.pdf", pdfOptions);
```

生成的文件 `Export3DImagestoPDF_out_.pdf` 是您原始 AutoCAD 图纸的 **save cad as pdf** 表现形式，具备您指定的精确页面尺寸。

## 常见问题与解决方案

| 症状 | 可能原因 | 解决办法 |
|------|----------|----------|
| 空白 PDF 输出 | 未设置光栅化选项或布局不匹配 | 验证 `setLayouts` 与 CAD 文件中的布局名称相匹配。 |
| 低分辨率图像 | `pageWidth`/`pageHeight` 太小或 DPI 低 | 增大尺寸或调用 `rasterizationOptions.setResolution(...)` 使用更高 DPI。 |
| 许可证异常 | 未应用有效许可证 | 应用永久 Aspose.CAD 许可证或使用临时许可证进行测试。 |

## 常见问题

**Q: 我可以在 Java 中使用 Aspose.CAD 处理其他 CAD 文件格式吗？**  
A: 可以，库支持 DWG、DXF、DWF、DGN 等众多格式，为项目提供灵活性。

**Q: 如何获取 Aspose.CAD for Java 的临时许可证？**  
A: 访问 [临时许可证页面](https://purchase.aspose.com/temporary-license/) 申请限时评估许可证。

**Q: 光栅化是否有布局选项？**  
A: 当然。使用 `setLayouts("Model")` 或指定其他布局名称来控制渲染哪个视图。

**Q: 我可以自定义输出 PDF 文件的尺寸吗？**  
A: 可以 – 在光栅化选项中修改 `pageWidth` 和 `pageHeight` 为任意所需尺寸。

**Q: 在哪里可以获取帮助或讨论 Aspose.CAD for Java 相关问题？**  
A: 专用的 [Aspose.CAD 论坛](https://forum.aspose.com/c/cad/19) 提供社区支持和官方团队的答复。

## 附加常见问题（AI 友好格式）

**Q: Aspose.CAD 在 Windows 或 Linux 上是否需要任何本机库？**  
A: 不需要。Aspose.CAD for Java 是纯 Java 库，可在支持 JDK 的任何平台上运行，无需额外的本机 DLL。

**Q: 库能够处理多大的 DWG 文件？**  
A: 该库可处理多页（最高约 500 MB）图纸，而无需一次性将整个文件加载到内存中，得益于其流式架构。

**Q: 能否一次性批量将多个 DWG 文件转换为 PDF？**  
A: 可以。遍历目录，使用 `Image.load()` 加载每个文件，应用相同的光栅化选项，然后对每个输出 PDF 调用 `save()`。

**Q: 在典型服务器上性能如何？**  
A: 根据 Aspose 的基准测试，在标准 2.5 GHz CPU 上将 100 页 DWG 以 300 DPI 转换大约需要 12 秒。

**Q: 库在 PDF 中是否保留图层信息？**  
A: 虽然输出是光栅化的，但图层、线宽和颜色的视觉外观会被忠实再现。

---

**最后更新：** 2026-10-19  
**测试版本：** Aspose.CAD for Java 24.10  
**作者：** Aspose

## 相关教程

- [使用 Aspose.CAD Java 导出 DWG 为 PDF 并启用跟踪](/cad/java/additional-features/enable-tracking/)
- [使用 Aspose.CAD Java 导出 DWG 为 PDF：特定布局](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [使用 Aspose.CAD for Java 将 DWG 导出为 BMP 并通过单位类型调整 CAD 大小](/cad/java/cad-file-manipulation/adjusting-cad-drawing-size-using-unit-type/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}