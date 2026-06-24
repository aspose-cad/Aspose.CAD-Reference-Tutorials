---
date: 2026-03-05
description: 在本分步教程中，学习如何使用 Aspose.CAD for Java 将 DWG 导出为 PDF、启用隐藏线以及将 DWG 转换为 PDF。
linktitle: Export DWG as PDF Using Java
second_title: Aspose.CAD Java API
title: 将 DWG 导出为带隐藏线的 PDF – Aspose.CAD for Java
url: /zh/java/cad-text-and-formatting/support-hidden-lines-in-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 导出 DWG 为 PDF（含隐藏线） – Aspose.CAD for Java

## Introduction

在本教程中，您将学习如何使用 Aspose.CAD for Java **export dwg to pdf** 并保留隐藏线。无论您需要 **convert DWG to PDF**、编写 **dwg to pdf tutorial** 风格的指南，还是仅仅 **save DWG as PDF** 并支持隐藏线，我们都会一步步带您完成。完成后，您将拥有一个可直接嵌入任何 Java 项目的即用型解决方案。

## Quick Answers
- **What does this tutorial cover?** 在使用 Aspose.CAD for Java 将 DWG 导出为 PDF 时启用隐藏线渲染。  
- **Which primary operation is performed?** `export dwg to pdf`。  
- **Do I need a license?** 免费试用可用于测试；生产环境需要商业许可证。  
- **What are the prerequisites?** Java 开发环境、Aspose.CAD for Java 库以及 DWG 文件。  
- **How long does implementation take?** 基本设置约需 10‑15 分钟。

## What is “export dwg to pdf”?
将 DWG 文件导出为 PDF 会将基于矢量的 CAD 图纸转换为可移植文档格式，同时保留图层、线型以及可选的隐藏线渲染。这使得即使没有 CAD 软件的利益相关者也能轻松查看 CAD 设计。

## How to Enable Hidden Lines When Exporting DWG to PDF
隐藏线通过光栅化选项中的布局设置进行控制。选择 **Model** 布局后，Aspose.CAD 会将隐藏的边缘视为不可见，从而为 3‑D 模型提供干净的 2‑D 表现。

## Why enable hidden lines when exporting?
隐藏线在 2‑D 页面上提供了更清晰的复杂 3‑D 模型视觉表现，只强调可见边缘。这提升了可读性，并且常常是工程文档的必需要求。

## Prerequisites

1. **Aspose.CAD for Java** – 从官方网站下载库 [here](https://releases.aspose.com/cad/java/)。  
2. **DWG files** – 将源 DWG 图纸存放在已知目录中。  
3. **Java development environment** – JDK 8+ 以及您喜欢的 IDE（Eclipse、IntelliJ 等）。  

现在您已经准备就绪，让我们进入代码实现。

## Import Namespaces

首先导入必要的类，以便能够处理 CAD 图像和 PDF 选项。

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.Arrays;
import java.util.List;
```

## Step 1: Set Up Your Project

创建一个 Java 项目并将 Aspose.CAD JAR 添加到构建路径。随后定义存放 DWG 文件的目录。

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

> **Pro tip:** 使用绝对路径或根据项目的 resources 文件夹配置相对路径。

## Step 2: Load DWG File

将源 DWG 文件加载到 `CadImage` 对象中，以便后续操作。

```java
String sourceFilePath = dataDir + "Bottom_plate.dwg";
String outPath = dataDir + "Bottom_plate.pdf";
CadImage cadImage = (CadImage)Image.load(sourceFilePath);
```

## Step 3: Configure Rasterization Options

选择要包含的图层并将页面尺寸设置为与原始图纸匹配。在此步骤中，通过指定布局来启用隐藏线渲染。

```java
List<String> list = Arrays.asList("Print","L1_RegMark","L2_RegMark");
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageHeight(cadImage.getHeight());
rasterizationOptions.setPageWidth(cadImage.getWidth()) ;
rasterizationOptions.setLayers(list);
```

## Step 4: Set PDF Options

告诉 Aspose.CAD 将矢量数据光栅化为 PDF，并使用 “Model” 布局保持隐藏线隐藏。

```java
PdfOptions pdfOptions = new PdfOptions();
rasterizationOptions.setLayouts(new String[] { "Model" });
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Step 5: Save the Result

最后，将 DWG 导出为 PDF 文件。隐藏线将按照您设置的布局得到保留。

```java
cadImage.save(outPath, pdfOptions);
System.out.println("\nThe DWG file exported successfully to PDF.\nFile saved at " + dataDir);
```

> **Common Pitfall:** 未将布局设置为 `"Model"` 会导致所有线条（包括隐藏线）在 PDF 中显示为实线。

## Common Issues and Solutions

| 问题 | 产生原因 | 解决办法 |
|------|----------|----------|
| PDF 显示所有线条为实线 | 未将布局设置为 **Model** | 确保在保存前调用 `rasterizationOptions.setLayouts(new String[] { "Model" });`。 |
| 输出中缺少图层 | 图层名称不正确 | 检查 DWG 文件中的图层名称，并在 `list` 中完全匹配它们。 |
| 大文件出现内存不足错误 | 光栅化尺寸过大 | 如果可能，减小页面尺寸或分块处理图纸。 |

## Frequently Asked Questions

### Q1: Can I use Aspose.CAD for Java with other CAD file formats?
A1: 是的，Aspose.CAD 支持多种 CAD 格式，例如 DWG、DXF、DWF 等。

### Q2: Is there a free trial available for Aspose.CAD for Java?
A2: 有，您可以在此处获取免费试用 [here](https://releases.aspose.com/)。

### Q3: How do I get support for Aspose.CAD for Java?
A3: 请访问 Aspose.CAD 论坛 [here](https://forum.aspose.com/c/cad/19) 获取社区支持。

### Q4: Where can I find detailed documentation for Aspose.CAD for Java?
A4: 请参阅文档 [here](https://reference.aspose.com/cad/java/)。

### Q5: Can I purchase a temporary license for Aspose.CAD for Java?
A5: 可以，您可以在此获取临时许可证 [here](https://purchase.aspose.com/temporary-license/)。

### Q6: Does this method also work for converting DWG to PDF in a headless server environment?
A6: 当然可以。由于代码仅使用 Aspose.CAD API，无需任何 UI 依赖，极其适合服务器端自动化。

## Conclusion

现在您已经掌握了一套完整、可投入生产的 **export dwg to pdf** 方法，支持隐藏线渲染，可将其集成到批处理工具、Web 服务或桌面应用中，实现 CAD 到 PDF 的自动化转换。

---

**Last Updated:** 2026-03-05  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}