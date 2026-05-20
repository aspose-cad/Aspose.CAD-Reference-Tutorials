---
date: 2026-05-20
description: 了解如何使用 Aspose.CAD for Java 将 DWG 转换为 PDF，同时覆盖自动代码页检测。包括导出 dwg 到 pdf 的步骤、编码技巧和故障排除。
keywords:
- convert dwg pdf
- export dwg to pdf
- Aspose.CAD Java
linktitle: 在 DWG 文件中覆盖自动代码页检测
schemas:
- author: Aspose
  dateModified: '2026-05-20'
  description: Learn how to convert DWG to PDF while overriding automatic code page
    detection using Aspose.CAD for Java. Includes export dwg to pdf steps, encoding
    tips, and troubleshooting.
  headline: Convert DWG to PDF – Override Code Page Detection in Java
  type: TechArticle
- description: Learn how to convert DWG to PDF while overriding automatic code page
    detection using Aspose.CAD for Java. Includes export dwg to pdf steps, encoding
    tips, and troubleshooting.
  name: Convert DWG to PDF – Override Code Page Detection in Java
  steps:
  - name: Set Up the Java Project
    text: Create a Maven or Gradle project and add the Aspose.CAD JAR to the classpath.
      This ensures the IDE can resolve the imported classes and that the runtime can
      locate the library.
  - name: Load the DWG File with a Specified Code Page
    text: Tell Aspose.CAD which encoding to use and whether to attempt recovery of
      malformed CIF/MIF data.
  - name: Export the CAD Image to PDF
    text: With the correct code page applied, you can safely export the drawing. The
      `PdfOptions` object lets you fine‑tune the PDF output (compression, rasterization,
      etc.).
  - name: Verify Success
    text: A simple console message confirms that the process completed without exceptions.
      You can repeat these steps for multiple DWG files, adjusting the source path
      and output name as needed.
  type: HowTo
- questions:
  - answer: It forces Aspose.CAD to use a specific character encoding instead of guessing.
    question: What does “override code page” mean?
  - answer: Yes – after setting the correct code page, you can save the CAD image
      as PDF.
    question: Can I export DWG directly to PDF?
  - answer: '`CodePages.Japanese` and `MifCodePages.Japanese` are the right choices.'
    question: Which encoding works for Japanese text?
  - answer: A commercial license is required; a temporary license is available for
      testing.
    question: Do I need a license for production use?
  - answer: Any recent version that supports `LoadOptions` and `PdfOptions`.
    question: What version of Aspose.CAD is needed?
  type: FAQPage
second_title: Aspose.CAD Java API
title: 将 DWG 转换为 PDF – 在 Java 中覆盖代码页检测
url: /zh/java/dwg-file-operations/override-code-page-detection/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 将 DWG 转换为 PDF – 在 Java 中覆盖代码页检测

在本综合教程中，您将学习 **如何将 DWG 转换为 PDF**，同时覆盖可能导致文本损坏的自动代码页检测。Aspose.CAD for Java 为您提供对字符编码的精确控制，使您能够恢复畸形的 CIF/MIF 数据并生成可靠的 PDF 输出。无论您是构建批量转换器还是将 CAD 处理添加到更大的 Java 服务中，以下步骤将引导您完成整个工作流——从项目设置到验证。

## 快速答案
- **“override code page” 是什么意思？** 它强制 Aspose.CAD 使用特定的字符编码，而不是自行猜测。
- **我可以直接将 DWG 导出为 PDF 吗？** 可以——在设置正确的代码页后，您可以将 CAD 图像保存为 PDF。
- **哪种编码适用于日文文本？** `CodePages.Japanese` 和 `MifCodePages.Japanese` 是正确的选择。
- **生产使用需要许可证吗？** 需要商业许可证；临时许可证可用于测试。
- **需要哪个版本的 Aspose.CAD？** 任何支持 `LoadOptions` 和 `PdfOptions` 的近期版本均可。

## 什么是 “export CAD to PDF”？
将 CAD 导出为 PDF 将基于矢量的 DWG 图纸转换为一种通用可视、固定布局的 PDF 文档。转换会保留所有几何实体、线条、图层和嵌入的文本，同时将图纸展平成一种可轻松共享、打印、归档或嵌入其他应用程序的格式，无需 CAD 软件。

## 为什么要覆盖自动代码页检测？
手动指定代码页可确保文本字节被正确解释，消除 Aspose.CAD 自动检测错误猜测旧版编码时常出现的乱码字符。这对于日文、俄文或阿拉伯文等非拉丁脚本尤为重要，并且可确保导出的 PDF 与原始设计保持一致。

## 前提条件
- **Java 开发环境** – JDK 8+ 和您偏好的 IDE。  
- **Aspose.CAD for Java** – 从官方网站 [here](https://releases.aspose.com/cad/java/) 下载库。  
- **DWG 示例文件** – 使用提供的 `SimpleEntities.dwg` 或任何您需要转换的 DWG。

## 导入包
`Document`、`LoadOptions` 和 `PdfOptions` 类是转换过程的核心。

`Document` 类在内存中表示 CAD 图纸，提供加载、操作和以各种格式保存文件的方法。  
`LoadOptions` 类允许您在加载 DWG 文件时指定代码页和恢复选项。  
`PdfOptions` 类控制 PDF 特定设置，如压缩、光栅化和元数据。

在您的 Java 项目中，导入必要的 Aspose.CAD 类：

```java
import com.aspose.cad.CodePages;
import com.aspose.cad.Image;
import com.aspose.cad.LoadOptions;
import com.aspose.cad.MifCodePages;
import com.aspose.cad.fileformats.cad.CadImage;
```

## 如何在覆盖代码页的情况下将 DWG 转换为 PDF？
使用 `LoadOptions` 加载 DWG 文件以指定精确的代码页，然后在生成的 `CadImage` 上调用带有已配置 `PdfOptions` 实例的 `save` 方法。此两步方法确保文本被正确解释，并且生成的 PDF 保持原始图纸的保真度、图层和矢量质量。

### 步骤 1：设置 Java 项目
创建一个 Maven 或 Gradle 项目，并将 Aspose.CAD JAR 添加到类路径中。这可确保 IDE 能解析导入的类，运行时也能找到该库。

### 步骤 2：使用指定的代码页加载 DWG 文件
告诉 Aspose.CAD 使用哪种编码以及是否尝试恢复畸形的 CIF/MIF 数据。

```java
String SourceDir = "Your Document Directory";
String dwgPathToFile = SourceDir + "SimpleEntites.dwg";
LoadOptions opts = new LoadOptions();
opts.setSpecifiedEncoding(CodePages.Japanese);
opts.setSpecifiedMifEncoding(MifCodePages.Japanese);
opts.setRecoverMalformedCifMif(false);
CadImage cadImage = (CadImage) Image.load(dwgPathToFile, opts);
```

### 步骤 3：将 CAD 图像导出为 PDF
在应用正确的代码页后，您可以安全地导出图纸。`PdfOptions` 对象允许您微调 PDF 输出（压缩、光栅化等）。

```java
// Perform export or other operations with cadImage
// For example, exporting to PDF
PdfOptions pdfOptions = new PdfOptions();
cadImage.save("output.pdf", pdfOptions);
```

### 步骤 4：验证成功
简单的控制台消息可确认过程已在无异常的情况下完成。

```java
System.out.println("OverrideAutomaticCodePageDetectionDwg executed successfully");
```

您可以对多个 DWG 文件重复这些步骤，根据需要调整源路径和输出名称。

## 常见问题与解决方案
- **仍然出现乱码字符：** 再次确认 `specifiedEncoding` 与原始 DWG 的代码页匹配。如有需要，使用不同的 `CodePages` 枚举。  
- **`cadImage.save` 时的 NullPointerException：** 确保 DWG 文件正确加载；检查路径和文件权限。  
- **PDF 文件大小过大：** 在 `PdfOptions` 中启用压缩（例如 `pdfOptions.setCompress(true)`），以在不失真质量的情况下减小文件大小。

## 常见问题

**Q1: Aspose.CAD 是否兼容所有版本的 DWG 文件？**  
A1: Aspose.CAD 支持超过 30 种 DWG 版本，包括 AutoCAD 2018 及更早的版本。

**Q2: 我可以在商业项目中使用 Aspose.CAD 吗？**  
A2: 可以，生产使用需要商业许可证。您可以在 [here](https://purchase.aspose.com/buy) 获取许可证。

**Q3: 免费试用版是否有任何限制？**  
A1: 试用版对大小和功能有限制；请查阅官方文档了解详情。

**Q4: 我如何获取 Aspose.CAD 的支持？**  
A4: 访问社区 [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) 获取帮助和讨论。

**Q5: 是否有可用于测试的临时许可证？**  
A5: 有，您可以在 [here](https://purchase.aspose.com/temporary-license/) 申请临时许可证。

---

**最后更新：** 2026-05-20  
**测试环境：** Aspose.CAD for Java 24.11 (latest at time of writing)  
**作者：** Aspose

## 相关教程

- [导出 DWG 为 PDF 并转换 CAD 图纸 – Aspose.CAD Java 教程](/cad/java/cad-drawing-conversion/)
- [使用 Aspose.CAD for Java 导出特定 DWG 布局为 PDF](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [使用 Aspose.CAD for Java 将 DWG 导出为 PDF 或光栅图像](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< blocks/products/products-backtop-button >}}

{{< /blocks/products/pf/main-wrap-class >}}