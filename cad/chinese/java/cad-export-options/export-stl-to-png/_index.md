---
date: 2026-02-20
description: 了解如何使用 Aspose.CAD for Java 将 STL 转换为 PNG。本分步指南展示了如何高效导出 STL 文件。
linktitle: Export STL to PNG
second_title: Aspose.CAD Java API
title: 使用 Aspose.CAD for Java 将 STL 转换为 PNG 的方法
url: /zh/java/cad-export-options/export-stl-to-png/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 将 STL 转换为 PNG（使用 Aspose.CAD for Java）

## 介绍

如果您需要在 Java 应用程序中 **将 STL 转换为 PNG**，Aspose.CAD for Java 能够快速且可靠地完成此任务。在本教程中，我们将完整演示整个过程——从项目设置到保存最终的 PNG 图像——让您能够自信地将 STL 转换集成到工作流中。

## 快速答疑
- **库的功能是什么？** 它将 CAD 格式（包括 STL）转换为 PNG 等光栅图像。  
- **使用的语言是什么？** Java，使用 Aspose.CAD API。  
- **是否需要许可证？** 生产环境使用需要临时许可证或正式许可证。  
- **实现大约需要多长时间？** 基本转换大约需要 10‑15 分钟。  
- **可以自定义图像尺寸吗？** 可以，通过 `CadRasterizationOptions`。

## 什么是将 STL 转换为 PNG？

将 STL 转换为 PNG 是将 3D 网格文件（STL）转换为 2D 光栅图像（PNG）的过程。当您需要快速的视觉预览、生成缩略图，或在网页中嵌入模型而无需 3D 查看器时，这非常有用。

## 为什么选择 Aspose.CAD for Java？

- **功能完整的 API** – 支持多种 CAD 格式，不仅限于 STL。  
- **无外部依赖** – 纯 Java，易于添加到任何 Maven/Gradle 项目中。  
- **高质量光栅输出** – 可控制分辨率、背景和抗锯齿。  
- **支持“如何导出 STL”场景** – 适用于批处理或即时转换。

## 前置条件

在开始之前，请确保您已具备以下条件：

- 已在机器上安装 Java Development Kit（JDK）。  
- 已下载 Aspose.CAD for Java 库。您可以在[此处](https://releases.aspose.com/cad/java/)获取。  
- 拥有有效许可证或从[此处](https://purchase.aspose.com/temporary-license/)获取的临时许可证。

## 导入命名空间

在 Java 项目中，导入所需的类：

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

现在，让我们将示例拆分为多个步骤。

## 步骤 1：设置项目

创建一个新的 Java 项目，并将 Aspose.CAD for Java 库添加到项目依赖中（Maven、Gradle 或手动 JAR 引入）。

## 步骤 2：指定 STL 文件

定义要转换的 STL 文件路径：

```java
String dataDir = "Your Document Directory" + "ExportingSTL/";
String fileName = dataDir + "example.stl";
```

## 步骤 3：加载 STL 文件

使用 `Image.load` 方法加载 STL 文件。这将创建一个 **CAD image** 对象，您可以对其进行光栅化：

```java
CadImage cadImage = (CadImage)Image.load(fileName);
```

## 步骤 4：配置光栅化选项

设置光栅化选项以控制输出 PNG 的尺寸和质量。这些选项是 **cad image to png** 转换过程的一部分：

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
```

## 步骤 5：配置 PNG 选项

创建 `PngOptions` 实例。如果希望应用光栅化设置，请取消注释下面的行：

```java
PngOptions pngOptions = new PngOptions();
// Uncomment the line below if you want to set vector rasterization options
// pngOptions.setVectorRasterizationOptions(vectorOptions);
```

## 步骤 6：保存为 PNG

最后，将 CAD 图像导出为 PNG 文件——这就是 **save PNG Java** 步骤：

```java
String outPath = dataDir + "galeon.stl.png";
cadImage.save(outPath, pngOptions);
```

> **专业提示：** 调整 `PageWidth` 和 `PageHeight` 以匹配所需的缩略图尺寸，从而加快处理速度。

恭喜！您已成功使用 Aspose.CAD for Java **将 STL 文件转换为 PNG**。

## 常见问题及解决方案

| 问题 | 原因 | 解决方案 |
|-------|--------|----------|
| 空白 PNG 输出 | 未设置光栅化选项 | 取消注释 `pngOptions.setVectorRasterizationOptions(vectorOptions);` 或指定背景颜色 |
| 大型 STL 文件导致 OutOfMemoryError | 堆内存不足 | 增加 JVM 堆大小（`-Xmx2g`）或分块处理文件 |
| LicenseException | 没有有效许可证 | 在加载图像前应用临时或购买的许可证 |

## 常见问答

### Q1：Aspose.CAD for Java 是否兼容所有 STL 文件版本？
A1：Aspose.CAD for Java 支持多种 STL 文件版本，确保与大多数常见格式兼容。

### Q2：我可以在商业项目中使用 Aspose.CAD for Java 吗？
A2：可以。只需从[此处](https://purchase.aspose.com/buy)获取有效许可证。

### Q3：免费试用是否需要临时许可证？
A3：不需要，免费试用无需临时许可证。您可以立即通过[此处](https://releases.aspose.com/)的试用版开始使用。

### Q4：在哪里可以获得更多支持或提问？
A4：访问 Aspose.CAD 论坛[此处](https://forum.aspose.com/c/cad/19)获取支持或提问。

### Q5：是否有完整的文档可供参考？
A5：有，文档可在[此处](https://reference.aspose.com/cad/java/)查阅。

## 结论

本指南演示了如何使用 Aspose.CAD for Java 高效地 **将 STL 转换为 PNG**。按照上述步骤操作，您可以将 STL 到 PNG 的转换集成到任何基于 Java 的流水线中，无论是构建桌面工具、Web 服务还是自动化报告工具。

---

**Last Updated:** 2026-02-20  
**Tested With:** Aspose.CAD for Java 24.12 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}