---
date: 2026-03-07
description: 学习如何使用 Aspose.CAD for .NET 将 CAD 导出为 SVG，定制 SVG 颜色，并高效地将 DWG 转换为 SVG。
linktitle: Exporting CAD Drawings to SVG Format
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: 将 CAD 导出为 SVG – 将 CAD 图纸导出为 SVG 格式 - Aspose.CAD 指南
url: /zh/net/advanced-export-techniques/exporting-cad-drawings-to-svg/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 导出 CAD 为 SVG – 将 CAD 图纸导出为 SVG 格式

## Introduction

Exporting CAD drawings to SVG is a common requirement when you need resolution‑independent graphics for web pages, reports, or interactive visualizations. In this tutorial you’ll learn **how to export CAD to SVG** with Aspose.CAD for .NET, explore options to **customize SVG color**, and see how to **convert DWG to SVG** (or DXF to SVG) in just a few lines of code. The steps are quick, the API is intuitive, and the resulting SVG files scale perfectly on any device.

## Quick Answers
- **处理转换的库是什么？** Aspose.CAD for .NET.  
- **我可以更改颜色模式吗？** 是的 – 使用 `SvgColorMode` 设置灰度、黑白或全彩。  
- **支持哪些 CAD 格式？** DWG、DXF 以及许多其他格式（参见 Aspose.CAD 文档）。  
- **开发是否需要许可证？** 可获取临时许可证用于测试。  
- **转换需要多长时间？** 对于标准图纸通常在一秒以内。  

## What is “export CAD to SVG”?
Export CAD to SVG means taking a native CAD file (such as DWG or DXF) and rendering it into the Scalable Vector Graphics format. SVG is XML‑based, lightweight, and can be styled with CSS—making it ideal for modern web and mobile applications.

## Why use Aspose.CAD for export CAD to SVG?
- **无外部依赖** – 纯 .NET API，无需安装 AutoCAD。  
- **细粒度控制** – 您可以 **customize SVG color**，决定文本是否保留为形状，并选择光栅化选项。  
- **广泛的格式支持** – 相同代码可用于 **convert DWG to SVG**、**convert DXF to SVG** 以及其他格式，简化代码库。  
- **高性能** – 为速度和低内存使用进行优化，适合批处理。  

## Prerequisites

Before you start, make sure you have:

- **已安装 Aspose.CAD for .NET**。您可以在[此处](https://releases.aspose.com/cad/net/)下载库。  
- 一个 .NET 开发环境（Visual Studio、Rider 或 .NET CLI）。  
- 要转换的 CAD 文件（DWG 或 DXF）。  

## Import Namespaces

First, bring the required namespaces into your project so the classes are available.

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Step‑by‑Step Guide

### Step 1: Set the Document Directory  
Define the folder where your source CAD file resides and where the SVG output will be saved.

```csharp
// The path to the documents directory.
string MyDir = "Your Document Directory";
```

### Step 2: Load the CAD Drawing  
Use `Image.Load` to read the DWG (or DXF) file. This works for **load DWG .NET** scenarios.

```csharp
using (Image image = Image.Load(MyDir + "sample.dwg"))
{
```

### Step 3: Configure SVG Export Options  
Adjust the export settings to match your needs. Here we set the color mode to grayscale and force all text to be rendered as vector shapes.

```csharp
    var options = new SvgOptions();
    options.ColorType = SvgColorMode.Grayscale;   // customize SVG color mode
    options.TextAsShapes = true;                  // ensures text appears as shapes
```

### Step 4: Save the SVG File  
Finally, write the SVG file to disk. This step **saves CAD as SVG** and completes the conversion.

```csharp
    image.Save(MyDir + "sample.svg", options);
}
```

By following these four concise steps, you can **convert DWG to SVG** (or **convert DXF to SVG**) with full control over the output appearance.

## Common Issues and Solutions

| 问题 | 原因 | 解决方案 |
|-------|-------|-----|
| **空白 SVG 输出** | 源文件路径不正确或文件已损坏。 | 验证 `MyDir` 并确保 CAD 文件能够正常打开。 |
| **颜色显示错误** | `SvgColorMode` 意外设置为灰度。 | 将 `options.ColorType` 更改为 `SvgColorMode.FullColor` 以保留原始颜色。 |
| **文本缺失** | `TextAsShapes` 设置为 `false`，且查看器不支持嵌入字体。 | 保持 `TextAsShapes = true`，或在 SVG 中嵌入所需字体。 |

## FAQ's

### Q1: Aspose.CAD 是否兼容所有 CAD 格式？

A1: Aspose.CAD 支持多种 CAD 格式，包括 DWG 和 DXF，确保广泛的兼容性。

### Q2: 导出为 SVG 时我可以自定义颜色模式吗？

A2: 可以，Aspose.CAD 允许您选择颜色模式，提供输出的灵活性。

### Q3: 是否提供用于测试的临时许可证？

A3: 可以，您可以在[此处](https://purchase.aspose.com/temporary-license/)获取临时许可证进行评估。

### Q4: 在哪里可以找到 Aspose.CAD 的详细文档？

A4: 文档可在[此处](https://reference.aspose.com/cad/net/)获取。

### Q5: 如何获取支持或提出与 Aspose.CAD 相关的问题？

A5: 请访问社区论坛[此处](https://forum.aspose.com/c/cad/19)获取支持和讨论。

## Frequently Asked Questions

**问：我可以在 .NET Core 或 .NET 6 中使用此代码吗？**  
**答：** 当然可以。Aspose.CAD for .NET 与 .NET Framework、 .NET Core 以及 .NET 5/6+ 兼容。

**问：是否可以仅导出特定布局或图层？**  
**答：** 可以。使用 `SvgOptions` 设置 `PageIndex` 或在保存前过滤图层。

**问：如何将自定义 CSS 样式嵌入生成的 SVG？**  
**答：** 保存后，您可以后处理 SVG XML 以注入 `<style>` 元素，或在新版本中使用 `options.CustomCss`（如果可用）。

**问：源 CAD 文件的大小有限制吗？**  
**答：** 库能够处理大文件，但内存消耗随复杂度增长。对于非常大的图纸，建议逐页处理。

**问：转换是否保留线宽和线型？**  
**答：** 默认情况下，线宽会被保留。您可以在 `SvgOptions` 中调整渲染选项以获得更细致的控制。

---

**最后更新：** 2026-03-07  
**测试环境：** Aspose.CAD for .NET 24.12  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}