---
date: 2026-02-17
description: 了解 Java CAD 库 Aspose.CAD for Java 如何快速、准确地将 DWG 导出为 PDF 或光栅图像。
linktitle: Export DWG to PDF or Raster
second_title: Aspose.CAD Java API
title: 使用 Java CAD 库 Aspose.CAD for Java 将 DWG 导出为 PDF 或光栅图像
url: /zh/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/
weight: 13
---

 final output.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 java cad library Aspose.CAD for Java 将 DWG 导出为 PDF 或光栅图像

## Introduction

在计算机辅助设计（CAD）的动态世界中，高效处理图纸至关重要。使用 **java cad library** **Aspose.CAD for Java**，您可以 **export dwg to pdf** — 或光栅图像 — 仅用几行代码。本教程将带您完成整个过程，从加载 DWG 文件到生成高质量 PDF，并阐明为何 Aspose.CAD Java 是 CAD 转换任务的首选库。

## Quick Answers
- **本教程涵盖什么内容？** 使用 Aspose.CAD for Java 将 DWG 文件导出为 PDF 或光栅图像。  
- **我需要许可证吗？** 可获得免费临时许可证用于评估；生产环境需要正式许可证。  
- **支持哪个 Java 版本？** 任意 Java 8+ 运行时均可与最新的 Aspose.CAD Java API 配合使用。  
- **我可以将 DWG 转换为其他图像格式吗？** 可以——相同的光栅化选项支持输出 PNG、JPEG、BMP 等。  
- **转换需要多长时间？** 对于普通图纸通常在一秒以内；较大的文件可能需要几秒。

## Why java cad library is the best choice for DWG conversion?

- **纯 Java 实现** – 无需本机 DLL 或外部工具。  
- **精确的单位处理** – 自动检测公制和英制单位。  
- **高质量光栅输出** – 可细调 DPI 和页面尺寸。  
- **完整的 PDF 支持** – 在不依赖额外组件的情况下生成保留矢量的 PDF。  
- **灵活的许可模式** – 可先使用 **temporary license aspose** 进行测试，正式上线后再升级。

## What is “export dwg to pdf”?

将 DWG 导出为 PDF 指的是将原生 AutoCAD 图纸转换为可移植、设备无关的 PDF 文档。生成的 PDF 保留矢量数据、图层和比例，适用于共享、打印或归档。

## Why use Aspose.CAD Java for this conversion?

因为 **java cad library** 在内部处理从单位转换到光栅化的所有工作，您无需使用第三方工具，即可在各平台上获得一致的结果。

## Prerequisites

- 具备 Java 编程基础。  
- 已安装 Aspose.CAD for Java 库。如果尚未下载，请前往 **[here](https://releases.aspose.com/cad/java/)** 获取。  
- 用于测试的 DWG 文件——本指南使用示例 **Bottom_plate.dwg**。

## Import Namespaces

在 Java 项目中，导入必要的类以启动转换：

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.UnitType;
```

## Step‑by‑Step Guide

### Step 1: Load the DWG File

首先，使用 `Image` 类加载 DWG 图纸。这会在内存中创建 Aspose.CAD 可处理的表示。

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Bottom_plate.dwg";
Image objImage = Image.load(srcFile);
```

### Step 2: Determine Unit Type

了解图纸使用的是公制还是英制单位对于正确缩放至关重要。辅助方法 `IsMetric`（此处省略实现）返回布尔标志。

```java
Boolean currentUnitIsMetric = IsMetric(objImage.getUnitType());
int currentUnitCoefficient = objImage.getUnitType();
```

### Step 3: Set Rasterization Options

根据单位体系，配置页面尺寸、缩放比例以及目标单位类型。这些选项决定 DWG 在包装成 PDF 前的光栅化方式。

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

### Step 4: Configure PDF Options (pdf options cad)

创建 `PdfOptions` 实例并附加光栅化设置。此操作告知 Aspose.CAD 如何将光栅化内容嵌入最终 PDF。

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());
```

### Step 5: Save as PDF

最后，将图纸导出为 PDF 文件。`save` 方法接受输出路径以及已配置的 `PdfOptions`。

```java
objImage.save(dataDir + "Saved.pdf", pdfOptions);
```

代码执行完毕后，您将在 `DWGDrawings` 文件夹中看到 **Saved.pdf**，可用于分发或归档。

## How to convert dwg raster images with java cad library

如果需要光栅图像而非 PDF，只需将 `PdfOptions` 替换为相应的光栅图像选项（如 `PngOptions`、`JpegOptions`）。同一个 `CadRasterizationOptions` 实例可重复使用，使您能够以最少的代码更改 **convert dwg raster** 文件。

## How to generate pdf dwg using pdf options cad

上述示例已经 **generates pdf dwg** 输出。通过调整 `pdfOptions`——例如设置 `pdfOptions.setCompress(true)`——可以控制 PDF 的大小和质量。这展示了 **pdf options cad** API 的灵活性。

## Common Issues & Tips

- **页面尺寸不正确** – 仔细检查单位转换逻辑；系数不匹配可能导致页面过大。  
- **缺少字体或线宽** – 确保 DWG 在转换前引用了所有外部资源。  
- **大图纸的性能** – 仅在需要更高质量时提升 `CadRasterizationOptions` 中的 `DPI` 设置；降低 DPI 可加快处理速度。  
- **许可证问题** – 评估时可使用 **temporary license aspose**；生产部署需正式许可证。

## Frequently Asked Questions

**问：我可以在其他 Java 框架中使用 Aspose.CAD for Java 吗？**  
**答：** 可以，Aspose.CAD for Java 可无缝集成到 Spring、Jakarta EE、Android 等流行 Java 框架中。

**问：Aspose.CAD for Java 是否提供临时许可证？**  
**答：** 是的，您可以在 **[here](https://purchase.aspose.com/temporary-license/)** 获取临时许可证。

**问：在哪里可以获得 Aspose.CAD for Java 的支持？**  
**答：** 请访问 **[Aspose.CAD forum](https://forum.aspose.com/c/cad/19)**，获取社区和 Aspose 工程师的帮助。

**问：如何购买 Aspose.CAD for Java 的许可证？**  
**答：** 您可以在 **[here](https://purchase.aspose.com/buy)** 购买许可证。

**问：Aspose.CAD for Java 支持哪些单位？**  
**答：** Aspose.CAD for Java 同时支持公制和英制单位，能够自动检测图纸的单位体系。

**问：我可以使用相同的 API 将 DWG 转换为其他图像格式（如 PNG、JPEG）吗？**  
**答：** 完全可以。将 `PdfOptions` 替换为相应的光栅图像选项（如 `PngOptions`），并复用相同的 `CadRasterizationOptions`。

## Conclusion

本教程演示了如何使用 **java cad library** Aspose.CAD for Java **export dwg to pdf** 并生成光栅图像。遵循此分步指南，您即可在任何 Java 应用中集成可靠的 CAD 转换，无论是用于文档的 PDF 还是用于网页显示的光栅图像。

---

**最后更新：** 2026-02-17  
**测试环境：** Aspose.CAD for Java 24.10  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}