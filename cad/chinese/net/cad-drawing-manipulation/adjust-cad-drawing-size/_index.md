---
date: 2026-03-19
description: 了解如何使用 Aspose.CAD 在 .NET 中调整 CAD 图纸的大小，包括如何缩放 CAD 图纸单位和调整布局尺寸。请按照我们的分步指南操作。
linktitle: Adjusting CAD Drawing Size
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: 如何使用 Aspose.CAD for .NET 调整 CAD 绘图尺寸
url: /zh/net/cad-drawing-manipulation/adjust-cad-drawing-size/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何使用 Aspose.CAD for .NET 调整 CAD 图纸大小

## 介绍

如果您需要 **如何调整 CAD** 文件直接在 .NET 应用程序中进行处理，您来对地方了。在本教程中，我们将展示如何更改 CAD 单位设置、缩放 CAD 图纸尺寸，以及使用 Aspose.CAD for .NET 以编程方式调整 CAD 大小。阅读完本指南后，您将拥有一个可靠、可用于生产环境的 CAD 调整解决方案，支持所有受支持的 CAD 格式。

## 快速答案
- **需要哪个库？** Aspose.CAD for .NET  
- **可以更改单位类型吗？** 可以 – 在 `CadRasterizationOptions` 中设置 `UnitType`  
- **生产环境需要许可证吗？** 非试用使用时需要有效的 Aspose.CAD 许可证  
- **示例导出为哪种图像格式？** BMP（但任何受支持的光栅格式均可）  
- **代码行数多少？** 完整的调整操作少于 30 行  

## 实际上 “如何调整 CAD” 是什么？
调整 CAD 图纸指的是将矢量数据以特定比例或单位（例如厘米、英寸）转换为光栅图像。这在需要将图纸嵌入报告、生成缩略图或在网页中集成 CAD 可视化时非常有用。

## 为什么使用 Aspose.CAD 调整 CAD 大小？
- **无需外部 CAD 软件** – 所有操作都在您的 .NET 代码中完成。  
- **细粒度控制** 单位、布局和光栅化选项。  
- **跨格式支持** – 同一段代码可用于 DWG、DXF、DWF 等多种格式。  

## 前置条件

在开始之前，请确保您已具备：

- Aspose.CAD for .NET 库：从 [Aspose.CAD for .NET 下载页面](https://releases.aspose.com/cad/net/) 下载并安装。  
- 示例 CAD 图纸：例如 `sample.dwg`，放置在项目的文档目录下。  

## 导入命名空间

首先，导入能够访问 Aspose.CAD 类的命名空间。

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## 步骤 1：加载 CAD 图纸

将源文件加载到 `Image` 对象中。该对象在内存中表示 CAD 图纸，并将作为后续所有操作的基础。

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "sample.dwg";

// Load a CAD drawing in an instance of Image
using (var image = Aspose.CAD.Image.Load(sourceFilePath))
{
    // Your code here...
}
```

## 步骤 2：创建 BmpOptions（或其他光栅格式）

`BmpOptions` 告诉 Aspose.CAD 在保存为位图时如何渲染矢量数据。您可以根据目标格式将其替换为 `PngOptions`、`JpegOptions` 等。

```csharp
Aspose.CAD.ImageOptions.BmpOptions bmpOptions = new Aspose.CAD.ImageOptions.BmpOptions();
```

## 步骤 3：设置 CadRasterizationOptions

`CadRasterizationOptions` 包含缩放、单位转换和布局选择的核心设置。将其链接到 `BmpOptions` 的 `VectorRasterizationOptions` 属性，可确保光栅化器使用您的自定义设置。

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions cadRasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
bmpOptions.VectorRasterizationOptions = cadRasterizationOptions;
```

## 步骤 4：设置 UnitType（更改 CAD 单位）

这里将 CAD 单位从默认值更改为厘米。这正是 **change cad unit** 关键字所在的位置，直接影响最终图像的尺寸。

```csharp
cadRasterizationOptions.UnitType = Aspose.CAD.ImageOptions.UnitType.Centimeter;
```

## 步骤 5：选择布局（设置 CAD 布局）

如果图纸包含多个布局（例如 Model、Sheet1），请指定要光栅化的布局。为获得调整后输出，正确选择布局是必不可少的，这正是 **set cad layouts** 所指的操作。

```csharp
cadRasterizationOptions.Layouts = new string[] { "Model" };
```

## 步骤 6：导出为 BMP（调整 CAD 图纸大小）

最后，保存光栅化后的图像。输出文件将反映您配置的新尺寸、单位和布局——从而完成 **resize CAD drawing** 操作。

```csharp
string outPath = sourceFilePath + ".bmp";
image.Save(outPath, bmpOptions);
```

现在您已经拥有一个表示已调整大小的 CAD 图纸的 BMP 文件，可用于后续处理或显示。

## 常见问题及解决方案

| 问题 | 产生原因 | 解决办法 |
|------|----------|----------|
| 输出模糊 | 默认 DPI（每英寸点数）过低 | 在保存前设置 `cadRasterizationOptions.Resolution = 300;` |
| 显示错误的布局 | 布局名称拼写错误 | 使用 CAD 查看器或 `Layouts` 集合确认准确的布局名称 |
| 单位转换不准确 | 公制与英制混用 | 确保 `UnitType` 与所需的计量系统匹配 |

## 常见问答

### Q1: Aspose.CAD for .NET 是否兼容所有 CAD 格式？

A1: Aspose.CAD for .NET 支持多种 CAD 格式，包括 DWG、DXF、DWF 等。完整列表请参阅 [文档](https://reference.aspose.com/cad/net/)。

### Q2: 我可以同时调整多个布局吗？

A2: 可以，通过在 `CadRasterizationOptions` 中调整 `Layouts` 数组即可实现对多个布局的批量调整。

### Q3: 哪里可以获取 Aspose.CAD for .NET 的支持？

A3: 访问 [Aspose.CAD 论坛](https://forum.aspose.com/c/cad/19) 获取社区支持和帮助。

### Q4: 是否提供免费试用？

A4: 是的，您可以通过 [免费试用](https://releases.aspose.com/) 评估 Aspose.CAD for .NET 的功能。

### Q5: 如何获取 Aspose.CAD for .NET 的临时许可证？

A5: 请在此处获取用于测试的临时许可证 [here](https://purchase.aspose.com/temporary-license/)。

## 常见问题

**问：如何在不更改单位类型的情况下缩放 CAD 图纸？**  
答：调整 `CadRasterizationOptions` 的 `Zoom` 属性（例如 `cadRasterizationOptions.Zoom = 2.0;`）即可在保持原始单位的前提下将尺寸放大一倍。

**问：可以导出为 BMP 之外的格式吗？**  
答：完全可以。只需将 `BmpOptions` 替换为 `PngOptions`、`JpegOptions` 或其他受支持的光栅格式类。

**问：是否可以批量处理文件夹中的图纸？**  
答：可以。遍历目录中的文件，应用相同的光栅化逻辑，并为每个输出文件生成唯一名称。

---

**最后更新：** 2026-03-19  
**测试环境：** Aspose.CAD for .NET 24.11（撰写时的最新版本）  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}