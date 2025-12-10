---
date: 2025-12-10
description: 学习如何使用 Aspose.CAD for Java 通过自动布局缩放将 CAD 转换为 PDF。本分步指南将向您展示如何高效、可靠地将
  CAD 导出为 PDF。
linktitle: Setting Auto Layout Scaling
second_title: Aspose.CAD Java API
title: 使用 Aspose.CAD Java 从 CAD 创建 PDF – 自动布局缩放
url: /zh/java/advanced-cad-features/setting-auto-layout-scaling/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 从 CAD 创建 PDF – 使用 Aspose.CAD Java 的自动布局缩放

## 介绍

如果您需要**快速且完美缩放地创建 PDF from CAD**文件，Aspose.CAD for Java 能满足您的需求。Auto Layout Scaling 会自动调整布局尺寸，使生成的 PDF 完全符合预期，无论原始 CAD 页面大小如何。在本教程中，我们将完整演示整个过程——从加载 DXF 文件到导出 PDF——并重点展示库的**export CAD to PDF**功能。

## 快速答案
- **Auto Layout Scaling 的作用是什么？** 它在光栅化时自动调整 CAD 布局大小，以适配目标页面尺寸。  
- **我可以转换哪些格式？** 任何 Aspose.CAD 支持的格式（如 DXF、DWG、DWF）均可转换为 PDF。  
- **生产环境需要许可证吗？** 是的，非评估使用必须购买商业许可证。  
- **转换需要多长时间？** 在现代硬件上，标准文件通常在一秒以内完成。  
- **我可以更改页面大小吗？** 可以，通过 `CadRasterizationOptions` 设置自定义页面尺寸。

## 什么是“从 CAD 创建 PDF”？
从 CAD 创建 PDF 指的是将矢量工程图（DXF、DWG 等）光栅化为 PDF 文档。PDF 保留原始图纸的视觉保真度，同时能够在任何平台上广泛查看。

## 为什么使用自动布局缩放？
- **输出一致**：保证所有布局填满 PDF 页面，无需手动计算尺寸。  
- **节省时间**：无需为每个图纸单独调整缩放因子。  
- **高质量**：在转换过程中保持线宽和几何精度。

## 前提条件

1. **Aspose.CAD for Java Library** – 从[download page](https://releases.aspose.com/cad/java/)下载最新版本。  
2. **资源目录** – 在机器上创建一个文件夹用于存放 CAD 文件；在代码中将 `"Your Document Directory"` 替换为该路径。  
3. **示例 CAD 文件** – 本指南使用 `conic_pyramid.dxf`，它包含在 Aspose 示例数据集中。

## 导入命名空间

首先，导入所需的类。这使我们能够使用图像加载、光栅化和 PDF 导出功能。

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## 步骤 1：加载 CAD 文件

加载源文件是**如何将 CAD 导出为 PDF**的第一步。

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

## 步骤 2：创建光栅化选项

定义目标页面尺寸。如果需要自定义布局，也可以在此块中**手动设置 CAD 页面大小**。

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
```

## 步骤 3：设置自动布局缩放

启用自动缩放功能。这是**如何为 CAD‑to‑PDF 转换设置缩放**的核心。

```java
rasterizationOptions.setAutomaticLayoutsScaling(true);
```

## 步骤 4：创建 PDF 选项

将光栅化设置关联到 PDF 导出选项。

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## 步骤 5：导出为 PDF

最后，将渲染的图像保存为 PDF 文件。此步骤完成**convert DXF to PDF**工作流。

```java
image.save(dataDir + "result_out_.pdf", pdfOptions);
```

重复上述步骤即可处理任何其他 CAD 文件。

## 常见问题与故障排除

| 症状 | 可能原因 | 解决方法 |
|------|----------|----------|
| 空白 PDF 输出 | 未设置光栅化选项或文件路径不正确 | 检查 `srcFile` 路径并确保 `setPageWidth/Height` 为非零值 |
| 缩放失真 | `setAutomaticLayoutsScaling` 保持为 `false` | 启用自动缩放或手动计算缩放因子 |
| 缺少图层 | 源 DXF 包含不受支持的实体 | 查看 Aspose.CAD 发布说明，确认支持的实体类型 |

## 常见问答

### Q1: Aspose.CAD for Java 是否兼容所有 CAD 文件格式？

A1: Aspose.CAD for Java 支持多种 CAD 格式，包括 DWG、DXF 和 DWF。

### Q2: 我可以进一步自定义缩放选项吗？

A2: 可以，`CadRasterizationOptions` 类提供了多种属性，可用于微调缩放及其他设置。

### Q3: 在哪里可以找到 Aspose.CAD for Java 的更多文档？

A3: 请参阅[documentation](https://reference.aspose.com/cad/java/)获取深入信息和示例。

### Q4: Aspose.CAD for Java 是否提供免费试用？

A4: 是的，您可以通过[free trial](https://releases.aspose.com/)体验 Aspose.CAD for Java 的功能。

### Q5: 如何获取帮助或参与 Aspose.CAD for Java 的讨论？

A5: 访问[Aspose.CAD forum](https://forum.aspose.com/c/cad/19)与社区交流并获取支持。

**Additional Common Questions**

**Q: 如何将 DWG 文件转换为 PDF 而不是 DXF？**  
A: 代码相同，只需将 `srcFile` 的文件扩展名改为 `.dwg`。

**Q: 能否为更高分辨率的 PDF 设置自定义 DPI？**  
A: 可以，使用 `rasterizationOptions.setResolution(300);`（或您需要的任何 DPI）。

**Q: 能否在生成的 PDF 中嵌入字体？**  
A: Aspose.CAD 会将图纸光栅化，字体以矢量方式渲染，无需单独嵌入字体。

## 结论

通过本指南，您已经掌握了使用 Aspose.CAD for Java 通过自动布局缩放**创建 PDF from CAD**文件的方法。该流程简化了**export CAD to PDF**工作流，确保缩放一致，并为您节省宝贵的开发时间。欢迎尝试不同的页面尺寸、分辨率和 CAD 格式，以满足项目需求。

---

**Last Updated:** 2025-12-10  
**Tested With:** Aspose.CAD for Java 24.12 (latest)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}