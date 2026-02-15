---
date: 2026-02-15
description: 了解如何使用 Aspose.CAD for Java 设置 PDF 页面尺寸并将 CAD 转换为 PDF，支持自动布局缩放和 TIFF 导出。
linktitle: Set PDF Page Size – Convert CAD to PDF
second_title: Aspose.CAD Java API
title: 设置 PDF 页面大小 – 将 CAD 转换为 PDF（Java）
url: /zh/java/advanced-cad-features/set-canvas-size-and-mode/
weight: 16
---

 answer.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 设置画布大小和模式

## 介绍

如果您在将 CAD 图纸转换为 PDF 时需要 **set PDF page size**，那么您来对地方了。在本教程中，我们将展示如何使用 Aspose.CAD for Java 定义精确的画布尺寸、启用自动布局缩放，并将结果导出为 PDF 和 TIFF。无论是为打印准备工程原理图，还是为网页画廊生成缩略图，控制页面大小和输出分辨率都是必不可少的。

## 快速回答
- **What does “convert CAD to PDF” mean?** 将 CAD 图纸（例如 DXF、DWG）转换为可在任何平台上查看的 PDF 文档。  
- **Can I also export to TIFF?** 是的——使用 `TiffOptions` 创建高分辨率光栅图像。  
- **Which option controls canvas size in Java?** `CadRasterizationOptions.setPageWidth/Height`。  
- **What is automatic layout scaling?** 一个标志 (`setAutomaticLayoutsScaling(true)`) 在画布尺寸变化时保持原始布局比例。  
- **Do I need a license for Aspose.CAD?** 生产使用需要临时或永久许可证。

## 在将 CAD 转换为 PDF 时如何设置 PDF 页面大小（Java）

设置 PDF 页面大小（或画布大小）可以让您决定文档的最终尺寸，这在必须 **change PDF dimensions** 以符合印刷标准或 UI 要求时尤为有用。下面我们将逐步演示每一步，并解释每行代码背后的 *why*。

## 什么是 **convert CAD to PDF**？

将 CAD 转换为 PDF 意味着将基于矢量的工程图纸渲染为 PDF 页面，保留线条、图层和几何信息，同时使文件能够在任何平台上通用访问。

## 为什么在 **java** 中设置画布大小？

在 Java 中设置画布大小可以定义输出分辨率和页面尺寸，确保生成的 PDF 或 TIFF 符合您的打印或显示需求。同时，它还能让您控制缩放行为，这对大幅图纸尤为关键。

## 前提条件

在开始教程之前，请确保具备以下前提条件：

- Aspose.CAD for Java：确保在 Java 环境中安装了 Aspose.CAD 库。您可以在[此处](https://releases.aspose.com/cad/java/)下载。  
- 文档目录：设置一个文档目录用于存放您的 CAD 文件。该目录将在教程步骤中被引用。

现在，让我们开始逐步指南。

## 导入命名空间

在此步骤中，我们将导入必要的命名空间以启动您的 Aspose.CAD 项目。

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

在此代码片段中，我们设置资源目录的路径，并使用 Aspose.CAD 的 `Image` 类加载一个 DXF 文件。

## 步骤 2：设置 **CadRasterizationOptions** 属性（set canvas size java）

```java
// Create an instance of CadRasterizationOptions and set its various properties
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

在这里，我们创建 `CadRasterizationOptions` 实例并配置页面宽度、页面高度以及 **automatic layout scaling** 等属性。这是为您的转换 **configure canvas mode** 的核心步骤。

## 步骤 3：创建 PdfOptions 并设置 VectorRasterizationOptions

```java
// Create an instance of PdfOptions
PdfOptions pdfOptions = new PdfOptions();

// Set the VectorRasterizationOptions property
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

现在，我们创建 `PdfOptions` 实例，并将其 `VectorRasterizationOptions` 属性设置为先前配置的 `CadRasterizationOptions`。

## 步骤 4：导出为 PDF（convert cad to pdf）

```java
// Export CAD to PDF
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

最后，我们使用指定的选项将 CAD 图像保存为 PDF 文件，完成 **convert CAD to PDF** 过程。

## 步骤 5：创建 TiffOptions 并设置 VectorRasterizationOptions（export cad to tiff）

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

最后，我们使用指定的选项将 CAD 图像保存为 TIFF 文件，演示在配置画布大小后如何 **export CAD to TIFF**。

## 常见问题及解决方案

| 问题 | 原因 | 解决方案 |
|-------|-------|-----|
| Output PDF is blank | `setNoScaling(true)` disables rendering for some drawings | Remove `setNoScaling(true)` or set it to `false`. |
| TIFF resolution looks low | Page width/height too small | Increase `setPageWidth` / `setPageHeight` values. |
| Layout looks distorted | Automatic layout scaling disabled | Ensure `setAutomaticLayoutsScaling(true)` is enabled. |

## 为什么调整画布大小和 DPI？

直接更改画布大小会影响输出的光栅化分辨率。如果您需要 **increase TIFF resolution**，只需提升 `setPageWidth` / `setPageHeight` 的数值，或在创建 `TiffOptions` 前调用 `rasterizationOptions.setResolution(300)`。这可以为打印或细节检查提供高质量的光栅图像。

## 常见问题

### Q1: Can I use Aspose.CAD for Java with other Java frameworks?

A1: 是的，Aspose.CAD 设计为可无缝集成到各种 Java 框架中。

### Q2: Is a temporary license available for Aspose.CAD?

A2: 是的，您可以在[此处](https://purchase.aspose.com/temporary-license/)获取临时许可证。

### Q3: Where can I get community support for Aspose.CAD?

A3: 访问 [Aspose.CAD 论坛](https://forum.aspose.com/c/cad/19)获取社区支持和讨论。

### Q4: Can I try Aspose.CAD for free?

A4: 当然！在[此处](https://releases.aspose.com/)获取免费试用。

### Q5: How do I purchase Aspose.CAD for Java?

A5: 在[此处](https://purchase.aspose.com/buy)购买产品。

**Additional Q&A**

**Q: Does the canvas size affect vector quality in the PDF?**  
A: No. Canvas size controls page dimensions; vector data remains resolution‑independent, ensuring crisp rendering at any zoom level.

**Q: Can I set a different DPI for the TIFF output?**  
A: Yes. Adjust `rasterizationOptions.setResolution(dpiValue)` before creating `TiffOptions`.

**Q: How can I **change PDF dimensions** for an existing PDF without re‑rendering the CAD?**  
A: Use Aspose.PDF to load the generated PDF and call `pdf.getPages().setPageSize(PageSize.A4)` or a custom size.

**Q: What is the best way to **convert dxf to pdf** while preserving layers?**  
A: Keep `setAutomaticLayoutsScaling(true)` and avoid `setNoScaling(true)`; this retains layer visibility and layout fidelity.

## 结论

恭喜！您已成功 **convert CAD to PDF** 并 **export CAD to TIFF**，同时 **set canvas size java**，实现 **automatic layout scaling**，并学习了如何 **configure canvas mode** 以获得高质量输出。本教程为您的 CAD 转换项目奠定了坚实基础。探索更多功能和可能性，请参阅 [Aspose.CAD 文档](https://reference.aspose.com/cad/java/)。

---

**最后更新：** 2026-02-15  
**测试环境：** Aspose.CAD for Java 24.12  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}