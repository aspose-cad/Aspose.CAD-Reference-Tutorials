---
date: 2026-03-02
description: 学习如何使用 Aspise.CAD for .NET 创建包含不同布局的单个 PDF——将 CAD 转换为 PDF，导出 DWG 为 PDF，并高效地将
  CAD 保存为 PDF。
linktitle: Creating Single PDF with Different Layouts
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: 如何使用不同布局创建单个 PDF - Aspose.CAD 指南
url: /zh/net/advanced-cad-techniques/creating-single-pdf-with-different-layouts/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何使用不同布局创建单个 PDF - Aspose.CAD 指南

## 介绍

如果您需要 **创建单个 PDF** 文件并且其中包含多个 CAD 布局，您来对地方了。在本教程中，我们将逐步演示将 CAD 图纸转换为一个 PDF 文档的完整步骤，并在此过程中处理多个布局。您将看到 Aspose.CAD for .NET 如何仅用几行 C# 代码就能轻松实现 **将 CAD 转换为 PDF**、**将 DWG 导出为 PDF**，以及 **将 CAD 保存为 PDF**。

## 快速答案
- **本教程覆盖哪些内容？** 生成一个包含多个 CAD 布局的 PDF。  
- **使用的库是什么？** Aspose.CAD for .NET。  
- **需要许可证吗？** 免费试用可用于评估；生产环境需要许可证。  
- **支持的 CAD 格式？** DWG、DXF、DGN 等多种格式。  
- **典型实现时间？** 基本转换大约需要 10‑15 分钟。

## 在 CAD 环境中，“创建单个 PDF” 是什么意思？

创建单个 PDF 指的是将一个可能包含多个布局定义（图纸空间）的 CAD 源文件，合并每个布局为同一 PDF 文档的不同页面。这在建筑平面图、工程原理图或任何客户需要统一 PDF 包的场景中尤为有用。

## 为什么选择 Aspose.CAD 来完成此任务？

- **无外部依赖** – 纯 .NET 实现，无需安装 AutoCAD。  
- **完全控制光栅化** – 可以设置页面尺寸、DPI 以及自定义布局尺寸。  
- **高保真渲染** – 在可能的情况下保留矢量数据，确保输出清晰。  
- **批处理友好** – 同一段代码可放入循环中自动处理大量图纸。

## 前置条件

- Aspose.CAD for .NET：确保已安装 Aspose.CAD for .NET。可从 [here](https://releases.aspose.com/cad/net/) 下载。  
- 开发环境：搭建 .NET 开发环境，并具备基本的 C# 编程知识。

## 导入命名空间

在 C# 项目中，加入必要的命名空间以使用 Aspose.CAD for .NET 的功能：

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## 步骤指南

### 步骤 1：加载 CAD 图像

首先，加载源 CAD 文件（例如 DWG 图纸）。`CadImage` 类可以让您访问文件中的所有布局。

```csharp
// The path to the documents directory.
string MyDir = "Your Document Directory";

using (CadImage cadImage = (CadImage)Image.Load(MyDir + "City skyway map.dwg"))
{
    // Your code for Step 1 goes here
}
```

### 步骤 2：自定义光栅化选项

定义每个布局的光栅化方式。您可以先设置默认页面尺寸，然后使用 `LayoutPageSizes` 为特定布局覆盖该设置。

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1000;
rasterizationOptions.PageHeight = 1000;

// Custom sizes for several layouts
rasterizationOptions.LayoutPageSizes.Add("ANSI C Plot", new SizeF(500, 1000));
rasterizationOptions.LayoutPageSizes.Add("8.5 x 11 Plot", new SizeF(1000, 100));
```

> **专业提示：** 如需更高分辨率的细节图纸，可调整 DPI（`rasterizationOptions.Resolution`）。

### 步骤 3：定义 PDF 选项

将光栅化设置封装到 `PdfOptions` 对象中。这告诉 Aspose.CAD 直接将 CAD 数据渲染为 PDF 流。

```csharp
PdfOptions pdfOptions = new PdfOptions() { VectorRasterizationOptions = rasterizationOptions };
```

### 步骤 4：保存为 PDF

最后，对 `CadImage` 实例调用 `Save`，传入目标 PDF 文件名和已准备好的选项。库将生成一个包含每个布局页面的单一 PDF。

```csharp
cadImage.Save(MyDir + "singlePDF_out.pdf", pdfOptions);
```

调用完成后，您将得到一个将 “ANSI C Plot” 与 “8.5 x 11 Plot” 布局合并为一个整体文档的 PDF。

## 常见问题与排查

| 问题 | 原因 | 解决方案 |
|------|------|----------|
| PDF 中缺少布局 | 未为布局名称定义 `LayoutPageSizes` | 核实 CAD 文件中的布局名称（区分大小写）。 |
| 输出质量低 | 默认 DPI 为 96 | 在保存前设置 `rasterizationOptions.Resolution = 300`（或更高）。 |
| 找不到文件 | `MyDir` 路径错误 | 使用 `Path.Combine` 构建跨平台路径。 |

## 常见问答

### Q1：我可以在 .NET 上使用 Aspose.CAD 处理其他 CAD 格式吗？

A1：可以，Aspose.CAD for .NET 支持多种 CAD 格式，如 DWG、DXF、DGN 等。

### Q2：是否提供免费试用？

A2：可以，点击 [here](https://releases.aspose.com/) 进行免费试用。

### Q3：如何获取 Aspose.CAD for .NET 的技术支持？

A3：访问 [Aspose.CAD 论坛](https://forum.aspose.com/c/cad/19) 获取社区支持。

### Q4：在哪里可以找到详细文档？

A4：请参阅文档 [here](https://reference.aspose.com/cad/net/)。

### Q5：如何购买 Aspose.CAD for .NET 的许可证？

A5：可在此处购买许可证 [here](https://purchase.aspose.com/buy)。

**其他问答**

**问：** 如何使用自定义页面尺寸 **导出 DWG 为 PDF**？  
**答：** 使用 `CadRasterizationOptions.LayoutPageSizes` 将每个 DWG 布局映射到所需的 PDF 页面尺寸，参见步骤 2。

**问：** 能否 **将 CAD 保存为 PDF** 而不进行光栅化？  
**答：** Aspose.CAD 在生成 PDF 时始终进行光栅化，但可以提升 DPI 以保持视觉保真度。

## 结论

本指南演示了如何使用 Aspose.CAD for .NET 将包含多个布局的 CAD 图纸 **创建单个 PDF** 文件。您现在掌握了 **将 CAD 转换为 PDF**、**导出 DWG 为 PDF**，以及 **将 CAD 保存为 PDF** 的完整工作流。请根据项目质量需求尝试不同的光栅化设置，并将此代码集成到更大的批处理流水线中。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**最后更新：** 2026-03-02  
**测试环境：** Aspose.CAD for .NET 24.11  
**作者：** Aspose  

---