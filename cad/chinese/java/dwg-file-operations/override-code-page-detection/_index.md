---
date: 2026-01-12
description: 了解如何使用 Aspose.CAD for Java 将 CAD 导出为 PDF，同时覆盖 DWG 文件的自动代码页检测。处理编码和损坏的
  CIF/MIF。
linktitle: Override Automatic Code Page Detection in DWG Files
second_title: Aspose.CAD Java API
title: 将 CAD 导出为 PDF – 使用 Java 覆盖 DWG 文件的自动代码页检测
url: /zh/java/dwg-file-operations/override-code-page-detection/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 导出 CAD 为 PDF – 在 DWG 文件中使用 Java 覆盖自动代码页检测

## 简介

在本综合指南中，您将了解 **如何将 CAD 导出为 PDF**，同时覆盖可能导致 DWG 文件中文本损坏的自动代码页检测。Aspose.CAD for Java 为您提供对编码的细粒度控制，使您能够恢复损坏的 CIF/MIF 数据并生成可靠的 PDF 输出。无论您是构建批量转换器还是将 CAD 处理集成到更大的 Java 应用程序中，以下步骤将带您完成整个工作流。

## 快速答案
- **“override code page” 是什么意思？** 它强制 Aspose.CAD 使用特定的字符编码，而不是自行猜测。
- **我可以直接将 DWG 导出为 PDF 吗？** 可以——在设置正确的代码页后，您可以将 CAD 图像保存为 PDF。
- **哪种编码适用于日文文本？** `CodePages.Japanese` 和 `MifCodePages.Japanese` 是正确的选择。
- **生产环境需要许可证吗？** 需要商业许可证；临时许可证可用于测试。
- **需要哪个版本的 Aspose.CAD？** 任何支持 `LoadOptions` 和 `PdfOptions` 的近期版本。

## 什么是 “导出 CAD 为 PDF”？
将 CAD 导出为 PDF 将基于矢量的 CAD 图纸转换为一种广泛支持的固定布局文档格式。生成的 PDF 保留线条、图层和文本，同时使图纸易于共享、打印或嵌入到其他应用程序中。

## 为什么要覆盖自动代码页检测？
DWG 文件通常使用旧的代码页存储文本。Aspose.CAD 的自动检测可能会误解这些字节，导致字符乱码。通过手动指定代码页，您可以确保文本在导出的 PDF 中准确呈现，尤其是对于日文、俄文或阿拉伯文等非拉丁脚本。

## 先决条件
- **Java 开发环境** – JDK 8+ 和您喜欢的 IDE。
- **Aspose.CAD for Java** – 从官方站点 [here](https://releases.aspose.com/cad/java/) 下载库。
- **DWG 示例文件** – 使用提供的 `SimpleEntities.dwg` 或任何您需要转换的 DWG。

## 导入包
在您的 Java 项目中，导入必要的 Aspose.CAD 类：

```java
import com.aspose.cad.CodePages;
import com.aspose.cad.Image;
import com.aspose.cad.LoadOptions;
import com.aspose.cad.MifCodePages;
import com.aspose.cad.fileformats.cad.CadImage;
```

## 分步指南

### 步骤 1：设置 Java 项目
创建一个新的 Maven 或 Gradle 项目，并将 Aspose.CAD JAR 添加到类路径中。此步骤确保 IDE 能解析导入的类。

### 步骤 2：使用指定代码页加载 DWG 文件
告知 Aspose.CAD 使用哪种编码以及是否尝试恢复损坏的 CIF/MIF 数据。

```java
String SourceDir = "Your Document Directory";
String dwgPathToFile = SourceDir + "SimpleEntites.dwg";
LoadOptions opts = new LoadOptions();
opts.setSpecifiedEncoding(CodePages.Japanese);
opts.setSpecifiedMifEncoding(MifCodePages.Japanese);
opts.setRecoverMalformedCifMif(false);
CadImage cadImage = (CadImage) Image.load(dwgPathToFile, opts);
```

### 步骤 3：将 CAD 图像导出为 PDF
在应用正确的代码页后，您可以安全地导出图纸。`PdfOptions` 对象允许您微调 PDF 输出（压缩、光栅化等）。

```java
// Perform export or other operations with cadImage
// For example, exporting to PDF
PdfOptions pdfOptions = new PdfOptions();
cadImage.save("output.pdf", pdfOptions);
```

### 步骤 4：验证成功
简单的控制台消息可确认过程已成功完成且未出现异常。

```java
System.out.println("OverrideAutomaticCodePageDetectionDwg executed successfully");
```

您可以对多个 DWG 文件重复这些步骤，根据需要调整源路径和输出名称。

## 常见问题与解决方案
- **仍然出现乱码字符：** 再次检查 `specifiedEncoding` 是否与原始 DWG 的代码页匹配。如有必要，使用不同的 `CodePages` 枚举。
- **`cadImage.save` 抛出 `NullPointerException`：** 确保 DWG 文件正确加载；检查路径和文件权限。
- **PDF 文件大小过大：** 在 `PdfOptions` 中启用压缩（例如，`pdfOptions.setCompress(true)`）。

## 常见问题

**Q1：Aspose.CAD 是否兼容所有版本的 DWG 文件？**  
A1：Aspose.CAD 支持广泛的 DWG 版本，包括 AutoCAD 2018 及更早的版本。

**Q2：我可以在商业项目中使用 Aspose.CAD 吗？**  
A2：可以，生产环境需要商业许可证。您可以在 [here](https://purchase.aspose.com/buy) 获取许可证。

**Q3：免费试用版有什么限制吗？**  
A3：试用版对大小和功能有限制；请查阅官方文档获取详细信息。

**Q4：如何获取 Aspose.CAD 的支持？**  
A4：访问社区 [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) 获取帮助和讨论。

**Q5：是否有用于测试的临时许可证？**  
A5：是的，可在 [here](https://purchase.aspose.com/temporary-license/) 请求临时许可证。

---

**最后更新：** 2026-01-12  
**测试环境：** Aspose.CAD for Java 24.11 (latest at time of writing)  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}