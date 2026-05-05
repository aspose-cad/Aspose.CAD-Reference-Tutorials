---
date: 2026-01-22
description: 了解如何使用 Aspose.CAD for Java 从 CAD 图纸创建 PDF、将 DWG 转换为 PDF，并自定义 PDF 页面尺寸。
linktitle: Single PDF with Different Layouts
second_title: Aspose.CAD Java API
title: 如何使用 Aspose.CAD for Java 将 CAD 图纸创建为 PDF
url: /zh/java/other-cad-operations/single-pdf-different-layouts/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何使用 Aspose.CAD for Java 将 CAD 图纸创建为 PDF

## 介绍

在本教程中，您将了解 **如何使用 Aspose.CAD for Java 库将 CAD 图纸创建为 PDF**。无论您需要 **将 DWG 转换为 PDF**、导出复杂的 CAD 文件，还是应用 **自定义 PDF 页面尺寸**，下面的步骤都将为您提供一个简洁的编程解决方案。让我们一起走完整个过程，您只需几行 Java 代码即可生成一个包含多个布局页面的单一 PDF。

## 快速回答
- **Aspose.CAD 的作用是什么？** 它让 Java 开发者加载、操作并导出 CAD 图纸为 PDF 等格式。
- **我可以将多个布局导出到同一个 PDF 吗？** 可以，在保存之前自定义布局页面尺寸即可。
- **支持哪些 CAD 格式？** DWG、DXF、DWF、DGN 等众多格式。
- **生产环境需要许可证吗？** 临时许可证可用于测试，商业使用需购买正式许可证。
- **需要哪个版本的 Java？** Java 8 或更高版本。

## 什么是“从 CAD 创建 PDF”？
从 CAD 创建 PDF 意味着将基于矢量的 CAD 图纸光栅化为固定布局的文档（PDF），该文档可在任何设备上查看，无需 CAD 软件。这非常适合共享设计、打印蓝图或归档工程作品。

## 为什么使用 Aspose.CAD for Java？
- **无外部依赖** – 纯 Java 实现，无需本机 DLL。
- **细粒度控制** – 可调 DPI、页面尺寸、布局选择等光栅化选项。
- **批量处理** – 一次运行即可处理大量图纸。
- **精准转换** – 保留线宽、颜色和图层信息。

## 先决条件

在开始之前，请确保您具备以下条件：

- **Java 环境** – 已安装 JDK 8 或更高版本。
- **Aspose.CAD 库** – 从 [download link](https://releases.aspose.com/cad/java/) 下载并安装 Aspose.CAD for Java。
- **文档目录** – 包含待转换 DWG（或其他 CAD）图纸的文件夹。

## 导入包

在您的 Java 项目中导入必要的类：

```java
import com.aspose.cad.Image;
import com.aspose.cad.SizeF;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.VectorRasterizationOptions;
```

## 分步指南

### 步骤 1：加载 CAD 图纸

首先，将源 CAD 文件（例如 DWG）加载到 `CadImage` 对象中。这是任何 **导出 CAD 为 PDF** 操作的入口。

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
CadImage cadImage = (CadImage)Image.load(dataDir + "City skyway map.dwg");
```

### 步骤 2：配置光栅化选项

定义 CAD 数据的光栅化方式。这里我们设置一个基础页面宽度和高度，用于那些没有自定义尺寸的布局。

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1000);
rasterizationOptions.setPageHeight(1000);
```

### 步骤 3：自定义布局页面尺寸

如果需要 **自定义 PDF 页面尺寸**，请为每个希望出现在最终 PDF 中的布局添加条目。这样即可 **将 DWG 转换为 PDF**，并为每个布局指定不同的尺寸。

```java
rasterizationOptions.getLayoutPageSizes().addItem("ANSI C Plot", new SizeF(500, 1000));
rasterizationOptions.getLayoutPageSizes().addItem("8.5 x 11 Plot", new SizeF(1000, 100));
```

### 步骤 4：设置 PDF 选项

将光栅化设置与 PDF‑专用选项相结合。`VectorRasterizationOptions` 属性告诉 Aspose.CAD 使用我们刚才定义的布局尺寸。

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### 步骤 5：保存为 PDF

最后，将 CAD 图纸导出为包含所有指定布局的单一 PDF 文件。此步骤 **一次调用即可将 CAD 保存为 PDF**。

```java
cadImage.save(dataDir + "singlePDF_out.pdf", pdfOptions);
```

> **专业提示：** 如果需要批量导出多个图纸，请复用同一个 `PdfOptions` 对象——这可以减少对象创建的开销。

## 常见问题及解决方案

| 问题 | 解决方案 |
|------|----------|
| **输出 PDF 中出现空白页** | 确认布局名称（如 `"ANSI C Plot"`、`"8.5 x 11 Plot"`）与 CAD 文件中定义的完全一致。 |
| **低分辨率输出** | 在保存前调用 `rasterizationOptions.setResolution(300);` 提高 DPI。 |
| **许可证未应用** | 在任何 Aspose.CAD 调用之前加载临时或正式许可证：`License license = new License(); license.setLicense("Aspose.CAD.lic");` |

## 常见问题

### Q1: 我可以将 Aspose.CAD for Java 与其他 Java 库一起使用吗？

A1: 可以，Aspose.CAD for Java 设计为可无缝集成到其他 Java 库中，提供丰富的功能。

### Q2: 是否提供试用版本？

A2: 当然！您可以在 [here](https://releases.aspose.com/) 获取免费试用版。

### Q3: 我在哪里可以获得更多支持？

A3: 请访问 [Aspose.CAD 论坛](https://forum.aspose.com/c/cad/19) 获取社区支持和讨论。

### Q4: 如何获取临时许可证？

A4: 您可以在 [here](https://purchase.aspose.com/temporary-license/) 获取临时许可证。

### Q5: 哪里可以购买正式版？

A5: 请在 [here](https://purchase.aspose.com/buy) 购买 Aspose.CAD for Java 的正式版。

---

**最后更新：** 2026-01-22  
**测试环境：** Aspose.CAD for Java 24.12  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}