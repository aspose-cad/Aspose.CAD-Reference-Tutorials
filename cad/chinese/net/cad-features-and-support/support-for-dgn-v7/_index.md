---
date: 2026-03-29
description: 了解如何使用 Aspose.CAD for .NET 将 DGN 转换为 JPEG，全面支持 DGN V7，并让您轻松将 CAD 转换为光栅图像。
linktitle: Support for DGN V7
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: 使用 Aspose.CAD for .NET 将 DGN 转换为 JPEG – 支持 V7
url: /zh/net/cad-features-and-support/support-for-dgn-v7/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 将 DGN 转换为 JPEG 使用 Aspose.CAD for .NET – V7 支持

## 介绍

在本教程中，您将学习如何使用 Aspose.CAD for .NET **将 DGN 转换为 JPEG**，充分利用库对 DGN V7 的完整支持。将 DGN 文件转换为 JPEG 等光栅图像是常见需求，尤其在需要将 CAD 图纸嵌入网页、移动应用或报表工具时。Aspose.CAD 还能高效地 **将 CAD 转换为光栅** 格式，为您在呈现设计数据时提供灵活性。

## 快速答案
- **本教程涵盖什么内容？** 使用 Aspose.CAD for .NET 将 DGN V7 文件转换为 JPEG 光栅图像。  
- **需要哪个库版本？** 任何包含 DGN V7 支持的近期 Aspose.CAD for .NET 发行版。  
- **我需要许可证吗？** 免费试用可用于开发；生产环境需要商业许可证。  
- **我可以更改输出尺寸吗？** 可以——光栅化选项允许您设置页面宽度、高度和缩放。  
- **JPEG 是唯一的输出格式吗？** 不是——Aspose.CAD 支持多种光栅格式（PNG、BMP、TIFF 等）。

## 什么是 DGN V7？
DGN（Design）是一种最初由 Bentley Systems 为 MicroStation 创建的文件格式。第 7 版增加了更丰富的几何形状和元数据，因而在土木工程和基础设施项目中广受欢迎。Aspose.CAD for .NET 能直接读取 DGN V7 文件，并将其内容以 `CadImage` 对象的形式呈现，您可以对其进行光栅化或转换为其他格式。

## 为什么将 DGN 转换为 JPEG？
- **适合 Web：** JPEG 图像体积轻巧，可在浏览器中即时显示，无需特殊插件。  
- **跨平台：** JPEG 可在任何设备上查看，非常适合与非技术利益相关者共享 CAD 图纸。  
- **简化工作流：** 转换为光栅格式后，下游流程无需 CAD 专用查看器。

## 先决条件

在深入实现之前，请确保您具备以下条件：

- **Aspose.CAD for .NET** – 从 [website](https://releases.aspose.com/cad/net/) 下载。  
- **开发环境** – Visual Studio（或任何支持 .NET 的 IDE）。

准备好这些后，您即可顺利按照步骤进行。

## 导入命名空间

首先导入处理 CadImage 和光栅化所需的命名空间。

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## 步骤 1：加载 DGN 文件

将源 DGN 文件加载到 `CadImage` 对象中。将占位符路径替换为包含 DGN 文件的文件夹路径。

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Subsequent steps will be placed here.
}
```

## 步骤 2：配置光栅化选项

定义 DGN 图纸的光栅化方式。您可以控制输出尺寸和缩放行为。

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions
{
    PageWidth = 600,
    PageHeight = 300,
    NoScaling = true,
    AutomaticLayoutsScaling = false
};
```

## 步骤 3：设置矢量光栅化选项

创建 `JpegOptions` 对象（或其他光栅格式选项），并附加光栅化设置。

```csharp
ImageOptionsBase options = new JpegOptions
{
    VectorRasterizationOptions = rasterizationOptions
};
```

## 步骤 4：保存光栅化图像

最后，使用 `Save` 方法将 DGN 图纸导出为 JPEG 文件。

```csharp
cadImage.Save(MyDir + "ExportDGNToRasterImage_out.jpeg", options);
```

代码成功运行后，您将在指定文件夹中找到原始 DGN V7 图纸的 JPEG 表示。

## 常见问题和解决方案

| 问题 | 解决方案 |
|-------|----------|
| **未找到文件** | 确认 `MyDir` 以路径分隔符（`\\` 或 `/`）结尾，并且文件名正确。 |
| **输出图像为空** | 确保 `NoScaling` 设置得当；如果希望图纸填满页面，请将其设为 `false`。 |
| **不受支持的实体** | Aspose.CAD 支持大多数 DGN 实体，但非常旧或自定义的对象可能会被忽略。请检查转换日志中的警告。 |

## 常见问题

### Q1：Aspose.CAD 是否兼容最新的 DGN V7 规范？
**A:** 是的，Aspose.CAD 完全支持 DGN V7，能够根据最新标准处理几何和元数据。

### Q2：我可以自定义 DGN 文件转换的光栅化选项吗？
**A:** 当然可以。`CadRasterizationOptions` 类允许您调整页面大小、缩放、线宽、背景颜色等。

### Q3：除了 JPEG 之外还有其他支持的输出格式吗？
**A:** 有，Aspose.CAD 可以导出为 PNG、BMP、TIFF 等多种光栅格式。只需使用相应的 `*Options` 类（例如 `PngOptions`）。

### Q4：如何获取 Aspose.CAD 相关问题的帮助？
**A:** 访问 [Aspose.CAD 论坛](https://forum.aspose.com/c/cad/19) 获取社区支持和官方回复。

### Q5：Aspose.CAD for .NET 是否提供免费试用？
**A:** 是的，您可以从 [here](https://releases.aspose.com/) 下载试用版。

**最后更新：** 2026-03-29  
**测试环境：** Aspose.CAD 24.12 for .NET  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}