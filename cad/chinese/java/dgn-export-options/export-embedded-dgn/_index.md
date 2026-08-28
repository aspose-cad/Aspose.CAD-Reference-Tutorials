---
date: 2026-06-14
description: 了解如何使用 Aspose.CAD for Java 将 CAD 导出为 PDF 并将 DGN 转换为 PDF。面向 Java 开发者的分步指南。
keywords:
- export cad to pdf
- convert dwg to pdf
- convert dgn to pdf
- java convert cad pdf
- batch convert dgn pdf
linktitle: 导出嵌入式 DGN
schemas:
- author: Aspose
  dateModified: '2026-06-14'
  description: Learn how to export CAD to PDF and convert DGN to PDF using Aspose.CAD
    for Java. Step‑by‑step guide for Java developers.
  headline: Export CAD to PDF – Export Embedded DGN with Aspose.CAD for Java
  type: TechArticle
- description: Learn how to export CAD to PDF and convert DGN to PDF using Aspose.CAD
    for Java. Step‑by‑step guide for Java developers.
  name: Export CAD to PDF – Export Embedded DGN with Aspose.CAD for Java
  steps:
  - name: Set Up Input and Output Paths
    text: Define the directory that contains your source file and specify the DWG
      that holds the embedded DGN.
  - name: Load DWG File
    text: '`Image` loads the DWG and automatically detects any embedded DGN data,
      exposing it for further processing.'
  - name: Configure Rasterization Options
    text: Select which layout(s) you want to include in the PDF. In this example we
      export only the **Model** layout, which is the most common view for engineering
      drawings.
  - name: Configure PDF Options
    text: Attach the rasterization settings to the PDF export options so that the
      final document respects the chosen layout and DPI.
  - name: Save PDF File
    text: Finally, write the PDF to disk using the configured options. The `save`
      method writes the configured image to the target file format on disk.
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD for Java is a commercial library. You can obtain a license
      from [here](https://purchase.aspose.com/buy).
    question: Can I use Aspose.CAD for Java in a commercial project?
  - answer: Yes, you can access a free trial of Aspose.CAD for Java [here](https://releases.aspose.com/).
    question: Is there a free trial available?
  - answer: You can seek support from the Aspose.CAD community on the [forum](https://forum.aspose.com/c/cad/19).
    question: How can I get support for Aspose.CAD for Java?
  - answer: You can obtain a temporary license [here](https://purchase.aspose.com/temporary-license/).
    question: What if I need a temporary license?
  - answer: The documentation is available [here](https://reference.aspose.com/cad/java/).
    question: Where can I find the official documentation?
  type: FAQPage
second_title: Aspose.CAD Java API
title: 将 CAD 导出为 PDF – 使用 Aspose.CAD for Java 导出嵌入式 DGN
url: /zh/java/dgn-export-options/export-embedded-dgn/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 导出 CAD 为 PDF – 使用 Aspose.CAD for Java 导出嵌入式 DGN

## 介绍

在本教程中，您将了解 **如何将 CAD 导出为 PDF**，方法是使用 Aspose.CAD for Java 将嵌入的 DGN 文件转换为高质量的 PDF 文档。Aspose.CAD 是一个强大的库，为 Java 开发者提供对 CAD 文件操作的完整控制，无论您需要 **将 DGN 转换为 PDF**、**将 DWG 转换为 PDF**，还是仅仅以其他格式渲染 CAD 图纸。请按照下面的逐步指南操作，您即可在几分钟内将此功能集成到您的应用程序中。

## 快速答案
- **“export CAD to PDF” 是什么意思？** 它将 CAD 图纸（DWG、DGN 等）转换为 PDF 文件，同时保留矢量质量。  
- **使用哪个库？** Aspose.CAD for Java。  
- **我需要许可证吗？** 生产环境需要许可证；提供免费试用版。  
- **主要前提条件是什么？** Java 开发环境以及 Aspose.CAD for Java 的 JAR 包。  
- **我可以自定义输出吗？** 可以——您可以选择布局、设置光栅化选项，并控制 PDF 设置。

## 什么是 “export CAD to PDF”？

Export CAD to PDF 将原生 CAD 图纸（DWG、DGN 等）转换为 PDF 文件，保留原始的矢量几何、图层和布局，使任何人无需 CAD 软件即可查看、打印或共享设计。此转换生成的文档与平台无关，在任何缩放级别下都保持一致外观，非常适合协作和归档。

## 为什么使用 Aspose.CAD for Java 将 DGN 转换为 PDF？

Aspose.CAD for Java 提供纯 Java 解决方案，消除对外部 CAD 工具的需求，确保生成的 PDF 在矢量精度上完全一致，并提供丰富的配置选项，如布局选择、DPI 控制和字体嵌入，适用于简单和企业级的转换任务。

- **无外部依赖** – 在任何操作系统上纯 Java 运行。  
- **保留矢量数据** – PDF 在任何缩放级别下都保持清晰。  
- **细粒度控制** – 选择特定布局、设置光栅化 DPI，并嵌入字体。  
- **企业级准备** – 支持高达 **2 GB** 的文件，批量处理数千个图纸，并提供灵活的授权方式。  

## 前提条件

在开始之前，请确保您具备以下条件：

- **Java 开发环境** – 已安装并配置 JDK 8 或更高版本。  
- **Aspose.CAD for Java** – 从 [此处](https://releases.aspose.com/cad/java/) 下载最新的 JAR。

## 导入包

`import` 语句将所需的 Aspose.CAD 类引入作用域。  
`Image` 是表示任何可光栅化 CAD 文件的核心类，而 `PdfOptions` 和 `RasterizationOptions` 让您能够细致调节 PDF 输出。  
`CadRasterizationOptions` 指定光栅化参数，如 DPI、页面尺寸和布局，用于 CAD 渲染。

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## 如何使用 Aspose.CAD for Java 导出 CAD 为 PDF？

该过程首先加载包含嵌入式 DGN 的 DWG 文件，然后设置光栅化参数以定义输出分辨率和布局，将这些参数附加到 `PdfOptions` 对象，最后调用 `save` 方法生成 PDF。此方法可在最少代码量的情况下确保高质量、保留矢量的结果。

下面是一段清晰的编号演练，准确展示如何将嵌入在 DWG 中的 DGN 文件转换为 PDF。

### 步骤 1：设置输入和输出路径

定义包含源文件的目录，并指定包含嵌入式 DGN 的 DWG。

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
```

### 步骤 2：加载 DWG 文件

`Image` 加载 DWG 并自动检测任何嵌入的 DGN 数据，随后可对其进行进一步处理。

```java
Image objImage = Image.load(fileName);
```

### 步骤 3：配置光栅化选项

选择要在 PDF 中包含的布局。本例仅导出 **Model** 布局，这是工程图纸最常用的视图。

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setLayouts(new String[] {"Model"});
```

### 步骤 4：配置 PDF 选项

将光栅化设置附加到 PDF 导出选项，以便最终文档遵循所选布局和 DPI。

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### 步骤 5：保存 PDF 文件

最后，使用配置好的选项将 PDF 写入磁盘。`save` 方法将配置好的图像写入目标文件格式。

```java
objImage.save(dataDir + "BlockRefDgn.pdf", pdfOptions);
```

## 将 DWG 转换为 PDF – 额外提示

如果您的源文件是普通 DWG（未嵌入 DGN），可以复用相同的代码——只需将 `fileName` 更改为指向您想要转换的 DWG。光栅化和 PDF 选项保持不变，为您提供一致的 **convert DWG to PDF** 工作流。

## 常见问题及解决方案

| 问题 | 原因 | 解决方案 |
|-------|--------|----------|
| **PDF 输出为空** | 布局名称不匹配 | 确认传递给 `setLayouts` 的布局名称与源文件中的布局完全一致（区分大小写）。 |
| **许可证异常** | 在未授权的情况下使用试用版 | 在加载图像之前应用有效的 Aspose.CAD 许可证（`License license = new License(); license.setLicense("Aspose.CAD.lic");`）。 |
| **未找到文件** | `dataDir` 路径不正确 | 使用绝对路径，或确保相对路径相对于项目工作目录是正确的。 |
| **低分辨率图形** | 默认光栅化 DPI 较低 | 设置 `rasterizationOptions.setResolution(300)` 或调整 `setPageWidth/Height` 以提升 DPI。 |

## 常见问题

**问：我可以在商业项目中使用 Aspose.CAD for Java 吗？**  
答：可以，Aspose.CAD for Java 是商业库。您可以从 [此处](https://purchase.aspose.com/buy) 获取许可证。

**问：是否提供免费试用？**  
答：是的，您可以在 [此处](https://releases.aspose.com/) 获取 Aspose.CAD for Java 的免费试用版。

**问：如何获取 Aspose.CAD for Java 的支持？**  
答：您可以在 [论坛](https://forum.aspose.com/c/cad/19) 上向 Aspose.CAD 社区寻求帮助。

**问：如果需要临时许可证怎么办？**  
答：您可以在 [此处](https://purchase.aspose.com/temporary-license/) 获取临时许可证。

**问：在哪里可以找到官方文档？**  
答：文档可在 [此处](https://reference.aspose.com/cad/java/) 获取。

## 结论

您现在已经学习了如何 **导出 CAD 为 PDF**，特别是如何使用 Aspose.CAD for Java **将 DGN 转换为 PDF**，甚至 **将 DWG 转换为 PDF**。按照上述步骤，您可以将无缝的 CAD‑to‑PDF 转换集成到任何基于 Java 的解决方案中，为用户提供高质量的 PDF，而无需额外的 CAD 软件。

---

**Last Updated:** 2026-06-14  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose

{{< blocks/products/products-backtop-button >}}

## 相关教程

- [使用 Aspose.CAD for Java 导出 DGN 为 DWG – 教程](/cad/java/dgn-export-options/)
- [使用 Aspose.CAD for Java 轻松将 DGN 导出为 AutoCAD PDF](/cad/java/dgn-export-options/exporting-dgn-to-pdf/)
- [dwg 转 pdf java – 使用 Aspose.CAD 导出 CAD 为 PDF](/cad/java/cad-export-options/export-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}