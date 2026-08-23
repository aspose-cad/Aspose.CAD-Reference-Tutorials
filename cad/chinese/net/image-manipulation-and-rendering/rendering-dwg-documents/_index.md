---
date: 2026-08-23
description: 了解如何使用 Aspose.CAD 在 C# 中创建 DWG 视口。本指南涵盖加载 DWG 文件、配置光栅化、定义视口以及将结果保存为 PDF。
keywords:
- create viewport dwg c#
- render dwg c#
- aspose.cad .net
lastmod: 2026-08-23
linktitle: 在 C# 中渲染 DWG 文档
og_description: 了解如何在 .NET 中使用 Aspose.CAD 创建 DWG 视口（C#）。本分步指南展示了加载、光栅化、定义视口以及保存为 PDF
  的过程。
og_image_alt: Guide showing how to create viewport dwg c# with Aspose.CAD in .NET
og_title: 如何在 C# 中使用 Aspose.CAD for .NET 创建 DWG 视口
schemas:
- author: Aspose
  dateModified: '2026-08-23'
  description: Learn how to create viewport dwg c# using Aspose.CAD. This guide covers
    loading a DWG file, configuring rasterization, defining a viewport, and saving
    the result as PDF.
  headline: How to create viewport dwg c# with Aspose.CAD for .NET
  type: TechArticle
- questions:
  - answer: Load the DWG file with `CadImage.Load`.
    question: What is the first step?
  - answer: '`Viewport` inside `CadRasterizationOptions`.'
    question: Which class defines the view area?
  - answer: Yes, using `PdfOptions` after rasterization.
    question: Can I output to PDF?
  - answer: A commercial license is required; a free trial works for evaluation.
    question: Do I need a license for production?
  - answer: Absolutely – Aspose.CAD works with .NET Framework, .NET Core, and .NET 5/6.
    question: Is .NET Core supported?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- create viewport dwg c#
- Aspose.CAD
- C# CAD rendering
- DWG to PDF
- CAD viewports
title: 如何在 C# 中使用 Aspose.CAD for .NET 创建 DWG 视口
url: /zh/net/image-manipulation-and-rendering/rendering-dwg-documents/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 C# 中渲染 DWG 文档 – 创建视口 dwg c# 教程

## 介绍

在本综合教程中，您将学习如何使用 Aspose.CAD **create viewport dwg c#** 并将 DWG 文件渲染为 PDF。无论您需要提取特定布局、生成可打印的图纸，还是在报告中嵌入 CAD 视图，控制视口都能提供精确的渲染控制。Aspose.CAD 支持 **20+ CAD formats**，并且能够在不将整个文档加载到内存的情况下处理包含数千个实体的文件，使其非常适合高性能的 .NET 应用程序。

## 快速答案

- **第一步是什么？** 使用 `CadImage.Load` 加载 DWG 文件。
- **哪个类定义了视图区域？** `CadRasterizationOptions` 中的 `Viewport`。
- **我可以输出为 PDF 吗？** 可以，光栅化后使用 `PdfOptions`。
- **生产环境需要许可证吗？** 需要商业许可证；免费试用可用于评估。
- **.NET Core 是否受支持？** 绝对支持 – Aspose.CAD 可在 .NET Framework、.NET Core 和 .NET 5/6 上运行。

## 先决条件

在深入代码之前，请确保您具备以下条件：

- 基本的 C# 编程知识。
- 已安装 Visual Studio（任意近期版本）。
- 已将 Aspose.CAD 库添加到项目中。您可以从 [Aspose.CAD 下载页面](https://releases.aspose.com/cad/net/) 下载。
- 一个示例 DWG 文件，例如 **Bottom_plate.dwg**，用于跟随教程。

## 导入命名空间

在 C# 文件的顶部添加所需的 `using` 指令，以便编译器能够找到 Aspose.CAD 类型。

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.FileFormats.Cad;
```

现在环境已准备好，让我们一步一步地 walkthrough 实现。

## 如何创建 viewport dwg c#？

要创建自定义视口，首先将 DWG 文件加载到 `CadImage` 对象中，然后使用所需的布局和缩放配置 `CadRasterizationOptions`。定义要显示的区域，使用计算得到的中心、高度和宽高比实例化 `CadVportTableObject`，替换活动视口，设置 PDF 选项，最后保存结果。

## 步骤 1：加载 dwg 文件

`CadImage.Load` 将 DWG 文件加载到 `CadImage` 对象中，该对象在内存中表示 CAD 图纸。

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Your code for loading the DWG file goes here.
}
```

## 步骤 2：配置光栅化选项

`CadRasterizationOptions` 指定 CAD 图纸的光栅化方式，包括布局选择、缩放和输出尺寸。

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new string[] { "Model" };
rasterizationOptions.NoScaling = true;
// Additional rasterization configurations can be added here.
```

## 步骤 3：定义绘制区域

`Point` 定义要渲染区域左上角的 X 和 Y 坐标。

```csharp
Point topLeft = new Point(6156, 7053);
double width = 3108;
double height = 2489;
```

## 步骤 4：创建新视口

`CadVportTableObject` 表示一个视口对象，用于控制渲染图纸的可见区域和宽高比。

```csharp
CadVportTableObject newView = new CadVportTableObject();
newView.Name.Value = "*Active";
newView.CenterPoint.X = topLeft.X + width / 2f;
newView.CenterPoint.Y = topLeft.Y - height / 2f;
newView.ViewHeight.Value = height;
newView.ViewAspectRatio.Value = width / height;
```

## 步骤 5：替换活动视口

该循环将活动视口替换为新创建的视口，以应用自定义视图设置。

```csharp
for (int i = 0; i < cadImage.ViewPorts.Count; i++)
{
    CadVportTableObject currentView = (CadVportTableObject)(cadImage.ViewPorts[i]);
    if ((currentView.Name.Value == null && cadImage.ViewPorts.Count == 1) ||
    string.Equals(currentView.Name.Value.ToLowerInvariant(), "*active"))
    {
        cadImage.ViewPorts[i] = newView;
        break;
    }
}
```

## 步骤 6：配置 PDF 选项

`PdfOptions` 配置 PDF 输出参数，例如压缩和元数据。

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## 步骤 7：将渲染的 dwg 保存为 PDF

`image.Save` 使用指定的格式选项将渲染的图像写入文件。

```csharp
cadImage.Save(MyDir, pdfOptions);
```

## 渲染 DWG 时为何使用自定义视口？

自定义视口可以让您隔离特定布局或区域，从而减小文件大小并提升渲染速度。使用聚焦视口时，Aspose.CAD 能在 2 秒以内渲染 300 页的 DWG，而完整图纸渲染可能需要多几秒的时间。

## 常见问题及解决方案

- **空白输出** – 确保视口坐标位于图纸范围内；使用 `CadImage.Size` 验证边界。
- **缺少图层** – 将 `CadRasterizationOptions.Layouts` 设置为正确的布局名称；否则默认布局可能为空。
- **性能下降** – 如果只需要快速预览，请在 `CadRasterizationOptions` 中禁用抗锯齿。

## 常见问答

### Q1：我可以将 Aspose.CAD 与其他 CAD 文件格式一起使用吗？

A1：是的，Aspose.CAD 支持多种格式，包括 DWG、DXF、DWF，以及超过 20 种其他 CAD 类型。

### Q2：Aspose.CAD 与 .NET Core 兼容吗？

A2：是的，Aspose.CAD 可在 .NET Framework、.NET Core 以及最新的 .NET 发行版上运行。

### Q3：如何处理 DWG 文件中的不同布局？

A3：在渲染之前，使用 `CadRasterizationOptions` 的 `Layouts` 属性指定所需的布局。

### Q4：使用 Aspose.CAD 有哪些许可方面的考虑？

A4：有关许可详情，请访问 [Aspose.CAD 许可页面](https://purchase.aspose.com/buy)。

### Q5：我可以在哪里找到更多支持？

A5：访问 [Aspose.CAD 论坛](https://forum.aspose.com/c/cad/19) 获取社区帮助和讨论。

### Q6：我可以直接渲染为 PNG 而不是 PDF 吗？

A6：是的，将 `PdfOptions` 改为 `PngOptions` 并调用 `image.Save("output.png", pngOptions)`。

### Q7：如何将渲染的图像嵌入到 Windows Forms 应用程序中？

A7：使用 `Image.FromFile("output.png")` 将保存的图像加载到 `PictureBox` 控件中。

## 结论

您现在已经了解如何 **create viewport dwg c#** 并使用 Aspose.CAD 将 DWG 文件渲染为 PDF（或其他光栅格式）。通过掌握视口操作，您可以对可视输出进行细粒度控制，这对于生成精确的工程图纸、报告或缩略图至关重要。探索更多光栅化设置，尝试不同的输出格式，并将代码集成到更大的 .NET 服务或桌面工具中。

---

**最后更新：** 2026-08-23  
**测试环境：** Aspose.CAD 24.11 for .NET  
**作者：** Aspose

## 相关教程

- [如何在 C# 中使用坐标将 DWG 转换为 PDF 时设置视口 - Aspose.CAD 教程](/cad/net/conversion-and-export/converting-dwg-to-pdf-with-coordinates/)
- [学习设置 CAD 光栅化选项 – 使用 Aspose.CAD 导出特定布局为 PDF](/cad/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/)
- [如何使用 Aspose.CAD for .NET 将 DWG 转换为 PDF 和光栅图像](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}