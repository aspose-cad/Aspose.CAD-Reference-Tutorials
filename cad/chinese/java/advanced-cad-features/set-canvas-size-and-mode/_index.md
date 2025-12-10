---
date: 2025-12-10
description: 了解如何使用 Aspose.CAD for Java 将 CAD 转换为 PDF，同时设置画布大小、自动布局缩放，并导出为 TIFF。
linktitle: Convert CAD to PDF – Set Canvas Size & Mode
second_title: Aspose.CAD Java API
title: 将 CAD 转换为 PDF – 设置画布大小和模式（Java）
url: /zh/java/advanced-cad-features/set-canvas-size-and-mode/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 设置画布大小和模式

## 介绍

您是否希望在 **将 CAD 转换为 PDF** 的同时，完全控制画布大小和渲染模式？本完整指南将逐步演示如何在 Java 中设置画布大小、启用自动布局缩放，然后使用 Aspose.CAD 将结果导出为 PDF 和 TIFF 格式。无论您是在完善生产流水线，还是在尝试原型，都能在此找到清晰、可操作的说明。

## 快速答疑
- **“将 CAD 转换为 PDF” 是什么意思？** 将 CAD 图纸（如 DXF、DWG）转换为可在任何平台上查看的 PDF 文档。  
- **我还能导出为 TIFF 吗？** 可以——使用 `TiffOptions` 创建高分辨率光栅图像。  
- **在 Java 中哪个选项控制画布大小？** `CadRasterizationOptions.setPageWidth/Height`。  
- **什么是自动布局缩放？** 一个标志 (`setAutomaticLayoutsScaling(true)`) ，在画布大小变化时保持原始布局比例。  
- **使用 Aspose.CAD 是否需要许可证？** 生产环境下需要临时或永久许可证。

## 什么是 **convert CAD to PDF**？

将 CAD 转换为 PDF 意味着将基于矢量的工程图纸渲染为 PDF 页面，保留线条、图层和几何信息，同时使文件能够在任何设备上通用访问。

## 为什么要在 **java** 中设置画布大小？

在 Java 中设置画布大小可以定义输出分辨率和页面尺寸，确保生成的 PDF 或 TIFF 符合您的打印或显示要求。它还让您能够控制缩放行为，这对大幅图纸尤为关键。

## 前置条件

在开始教程之前，请确保具备以下前置条件：

- Aspose.CAD for Java：确保已在 Java 环境中安装 Aspose.CAD 库。您可以在[此处](https://releases.aspose.com/cad/java/)下载。  
- 文档目录：创建用于存放 CAD 文件的文档目录，后续教程步骤将引用该目录。

现在，让我们开始逐步指南。

## 导入命名空间

在本步骤中，我们将导入必要的命名空间，以启动您的 Aspose.CAD 项目。

```java
import java.awt.Image;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## 步骤 1：导入 Aspose.CAD 类

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
com.aspose.cad.Image objImage = com.aspose.cad.Image.load(srcFile);
```

在此代码片段中，我们设置资源目录路径，并使用 Aspose.CAD 的 `Image` 类加载 DXF 文件。

## 步骤 2：设置 **CadRasterizationOptions** 属性（set canvas size java）

```java
// Create an instance of CadRasterizationOptions and set its various properties
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

这里，我们创建 `CadRasterizationOptions` 实例并配置页面宽度、页面高度以及 **自动布局缩放** 等属性。这是 **configure canvas mode** 的核心。

## 步骤 3：创建 PdfOptions 并设置 VectorRasterizationOptions

```java
// Create an instance of PdfOptions
PdfOptions pdfOptions = new PdfOptions();

// Set the VectorRasterizationOptions property
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

现在，创建 `PdfOptions` 实例，并将其 `VectorRasterizationOptions` 属性设为前面配置好的 `CadRasterizationOptions`。

## 步骤 4：导出为 PDF（convert cad to pdf）

```java
// Export CAD to PDF
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

最后，使用指定的选项将 CAD 图像保存为 PDF 文件，完成 **convert CAD to PDF** 过程。

## 步骤 5：创建 TiffOptions 并设置 VectorRasterizationOptions（export cad to tiff）

```java
// Create an instance of TiffOptions
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);

// Set the VectorRasterizationOptions property
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
```

在本步骤中，我们设置 `TiffOptions` 实例，并配置其 `VectorRasterizationOptions` 属性。

## 步骤 6：导出为 TIFF

```java
// Export CAD to TIFF
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

最终，使用指定的选项将 CAD 图像保存为 TIFF 文件，演示如何在配置画布大小后 **export CAD to TIFF**。

## 常见问题及解决方案

| 问题 | 原因 | 解决办法 |
|------|------|----------|
| 输出的 PDF 空白 | `setNoScaling(true)` 对某些图纸会禁用渲染 | 移除 `setNoScaling(true)` 或将其设为 `false`。 |
| TIFF 分辨率偏低 | 页面宽度/高度设置过小 | 增大 `setPageWidth` / `setPageHeight` 的数值。 |
| 布局失真 | 自动布局缩放未启用 | 确保 `setAutomaticLayoutsScaling(true)` 已开启。 |

## 结论

恭喜！您已成功 **convert CAD to PDF** 并 **export CAD to TIFF**，同时 **set canvas size java**，实现 **automatic layout scaling**，并学习了如何 **configure canvas mode** 以获得高质量输出。本教程为您的 CAD 转换项目奠定了坚实基础。请在 [Aspose.CAD 文档](https://reference.aspose.com/cad/java/) 中探索更多功能与可能性。

## 常见问答

### Q1：我可以在其他 Java 框架中使用 Aspose.CAD 吗？

A1：可以，Aspose.CAD 设计为可无缝集成到各种 Java 框架中。

### Q2：Aspose.CAD 是否提供临时许可证？

A2：可以，您可在[此处](https://purchase.aspose.com/temporary-license/)获取临时许可证。

### Q3：在哪里可以获得 Aspose.CAD 的社区支持？

A3：访问 [Aspose.CAD 论坛](https://forum.aspose.com/c/cad/19) 获取社区支持与讨论。

### Q4：我可以免费试用 Aspose.CAD 吗？

A4：当然！请在[此处](https://releases.aspose.com/)获取免费试用。

### Q5：如何购买 Aspose.CAD for Java？

A5：请在[此处](https://purchase.aspose.com/buy)购买产品。

**附加问答**

**问：画布大小会影响 PDF 中矢量的质量吗？**  
答：不会。画布大小决定页面尺寸；矢量数据保持分辨率无关性，任何缩放级别下都能保持清晰渲染。

**问：我可以为 TIFF 输出设置不同的 DPI 吗？**  
答：可以。在创建 `TiffOptions` 前，使用 `rasterizationOptions.setResolution(dpiValue)` 调整 DPI。

---

**最后更新：** 2025-12-10  
**测试环境：** Aspose.CAD for Java 24.12  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}