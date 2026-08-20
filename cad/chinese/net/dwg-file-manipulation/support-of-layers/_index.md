---
date: 2026-04-09
description: 学习如何使用 C# 与 Aspose.CAD for .NET 导出 DWG 图层、转换 DWG 图像并保存为 DWG JPEG。一步一步的指南，帮助高效操作
  CAD 文件。
keywords:
- export dwg layers
- convert dwg image
- dwg layer visibility
- save dwg jpeg
linktitle: 使用 C# 处理 DWG 文件中的图层
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: 使用 C# 导出 DWG 图层 – Aspose.CAD 教程
url: /zh/net/dwg-file-manipulation/support-of-layers/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 C# 导出 DWG 图层 – Aspose.CAD 教程

## 介绍

在本综合指南中，您将学习如何使用 C# 和 Aspose.CAD 库**导出 DWG 图层**。无论您需要**转换 DWG 图像**格式、控制**DWG 图层可见性**，还是仅仅**保存 DWG JPEG** 文件，下面的步骤都将向您展示如何高效完成。教程结束时，您将拥有一段可直接运行的代码片段，能够隔离特定图层并将其渲染为高质量 JPEG。

## 快速答疑
- **“export dwg layers” 是什么意思？** 它指将 DWG 文件中选定的图层光栅化为 JPEG、PNG 等图像格式。  
- **哪个库最适合此任务？** Aspose.CAD for .NET 提供完整功能，无需 AutoCAD。  
- **可以一次导出多个图层吗？** 可以——将图层名称数组传递给光栅化选项。  
- **生产环境需要许可证吗？** 需要商业许可证；可获取免费试用版进行评估。  
- **支持哪些输出格式？** JPEG、PNG、BMP、TIFF 等多种格式，均通过 ImageOptions 类实现。

## 什么是导出 DWG 图层？
导出 DWG 图层是指将 DWG 图纸中一个或多个图层的矢量数据光栅化为位图图像。当您希望共享图纸的特定部分而不暴露完整 CAD 文件时，这非常有用。

## 为什么要控制 DWG 图层可见性？
控制图层可见性可以：

- 为演示或文档创建干净的视觉资产。  
- 通过仅导出所需几何体来减小文件大小。  
- 通过隐藏机密图层来保护专有设计细节。  

## 前置条件

在开始之前，请确认您具备以下条件：

- 基本的 C# 编程语言知识。  
- 已在机器上安装 Visual Studio。  
- Aspose.CAD for .NET 库，可从 [Aspose.CAD website](https://releases.aspose.com/cad/net/) 下载。

## 导入命名空间

首先，导入能够使用光栅化和图像导出功能的命名空间。

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

## 步骤 1：加载 DWG 文件

将源 DWG（或 DWF）文件加载到 `Image` 对象中。该对象在内存中表示整个图纸。

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "for_layers_test.dwf";

using (Aspose.CAD.Image image = Aspose.CAD.Image.Load(sourceFilePath))
{
    // Your code for subsequent steps goes here
}
```

*为什么重要：* 只加载一次文件即可在多个图层导出操作中复用同一 `image` 实例，从而提升性能。

## 步骤 2：配置光栅化选项

创建 `CadRasterizationOptions` 实例，以告知 Aspose.CAD 如何渲染图纸。这里我们设置高分辨率（1600 × 1600），确保导出的 JPEG 清晰锐利。

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions rasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
```

如有需要，还可以调整背景颜色、线宽缩放或抗锯齿设置。

## 步骤 3：指定图层（DWG 图层可见性）

添加您想要**导出 dwg layers**的图层。在本例中仅导出 “LayerA”。若要导出多个图层，只需在数组中列出它们。

```csharp
rasterizationOptions.Layers = new string[] { "LayerA" };
```

*专业提示：* 使用图纸中出现的准确图层名称；图层名称区分大小写。

## 步骤 4：配置图像导出选项

选择要创建的图像格式。这里使用 `JpegOptions`，因为 JPEG 在质量与文件大小之间提供了良好平衡，适合用于 **save dwg jpeg** 的网页预览。

```csharp
JpegOptions jpegOptions = new JpegOptions();
jpegOptions.VectorRasterizationOptions = rasterizationOptions;
```

如果需要**convert dwg image** 为 PNG 或 TIFF，只需将 `JpegOptions` 替换为相应的选项类。

## 步骤 5：保存导出的图像

定义输出文件路径并调用 `Save`。光栅化引擎会遵循您提供的图层列表，仅在最终 JPEG 中显示 “LayerA”。

```csharp
MyDir = MyDir + "for_layers_test.jpg";
image.Save(MyDir, jpegOptions);
```

执行此行代码后，您将在文档目录中看到 `for_layers_test.jpg`，其中仅包含所选图层。

## 常见问题与解决方案

| 问题 | 解决方案 |
|-------|------------|
| **未找到图层名称** | 核实原始 DWG 中图层的拼写和大小写。可使用 CAD 查看器列出图层名称。 |
| **输出图像为空白** | 确保光栅化选项的背景非透明，并且所选图层确实包含几何体。 |
| **输出分辨率低** | 增加 `PageWidth`、`PageHeight` 或在 `CadRasterizationOptions` 中设置更高的 `Resolution`。 |
| **不支持的 DWG 版本** | 更新至最新的 Aspose.CAD 版本；新版本会添加对最新 AutoCAD 发行版的支持。 |

## 常见问答

### Q1: 能否同时处理多个图层？
A1: 可以。只需将图层名称添加到 `rasterizationOptions.Layers` 数组中。

### Q2: Aspose.CAD 有试用版吗？
A2: 有，您可以从 [here](https://releases.aspose.com/) 获取免费试用版。

### Q3: 文档在哪里可以找到？
A3: 文档可在 [here](https://reference.aspose.com/cad/net/) 查看。

### Q4: 如何获取 Aspose.CAD 的支持？
A4: 可在 [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) 寻求帮助。

### Q5: Aspose.CAD 的授权方式有哪些？
A5: 您可以在 [here](https://purchase.aspose.com/buy) 查看并购买授权选项。

**附加问答**

**Q: 能否将图纸导出为 PNG 而不是 JPEG？**  
A: 完全可以。将 `JpegOptions` 替换为 `PngOptions`，并相应更改文件扩展名。

**Q: 库是否保留线型和颜色？**  
A: 会的。所有矢量属性在光栅化过程中都会忠实呈现。

---

**最后更新：** 2026-04-09  
**测试环境：** Aspose.CAD for .NET（最新发布）  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}