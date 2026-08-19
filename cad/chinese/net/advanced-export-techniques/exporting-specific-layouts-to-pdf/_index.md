---
date: 2026-03-13
description: 了解如何使用 Aspose.CAD for .NET 设置 CAD 栅格化选项并将特定 DWG 布局导出为 PDF——创建 CAD 文件
  PDF 的权威指南。
linktitle: Exporting Specific Layouts to PDF
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: 设置 CAD 栅格化选项 – 将特定布局导出为 PDF - Aspose.CAD 指南
url: /zh/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 导出特定布局为 PDF - Aspose.CAD 指南

## Introduction

在本教程中，您将了解 **如何设置 CAD 光栅化选项**，以便直接将 DWG 文件中的单个布局或多个布局导出为 PDF。Aspose.CAD for .NET 使 *dwg to pdf conversion c#* 过程变得简单，您可以完全控制页面大小、分辨率和布局选择。阅读完本指南后，您只需几行代码即可 **从 CAD 文件创建 PDF**。

## Quick Answers
- **“set cad rasterization options” 做什么？**  
  它告诉 Aspose.CAD 如何将矢量数据（布局、图层、线宽）渲染为光栅化的 PDF 页面。  
- **哪个方法可以将 DWG 布局导出为 PDF？**  
  使用配置了 `PdfOptions` 且包含您的 `CadRasterizationOptions` 的 `Image.Save`。  
- **我可以一次导出多个布局吗？**  
  可以——在 `Layouts` 属性中提供布局名称数组。  
- **生产环境需要许可证吗？**  
  需要商业许可证；提供免费试用供评估。  
- **支持哪些 .NET 版本？**  
  .NET Framework 4.5+、.NET Core 3.1+、.NET 5/6 及更高版本。

## What is “set cad rasterization options”?

`CadRasterizationOptions` 是控制在转换为基于光栅的格式（如 PDF）时 CAD 实体如何光栅化的类。通过配置其属性——页面尺寸、布局选择、背景颜色等——您可以决定 **export dwg layout to pdf** 操作的视觉结果。

## Why set CAD rasterization options?

- **Precision** – 精确保留线宽和比例，完全呈现原始 CAD 图纸的外观。  
- **Performance** – 仅渲染所需布局，降低文件大小和处理时间。  
- **Flexibility** – 调整页面宽/高、DPI 和背景，以符合您的报表标准。  

## Prerequisites

在开始编写代码之前，请确保您已具备：

- 已安装 **Aspose.CAD for .NET**。您可以在 [here](https://releases.aspose.com/cad/net/) 下载。  
- .NET 开发环境（Visual Studio、VS Code 或任意您喜欢的 IDE）。  
- 包含至少一个布局的 DWG 文件（此处示例文件为 `visualization_-_conference_room.dwg`）。

## Import Namespaces

在您的 .NET 项目中，导入 Aspose.CAD 所需的命名空间：

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Step‑by‑Step Guide

### Step 1: Load the DWG file

首先，指向您想要转换的源 DWG 文件。

```csharp
// The path to the documents directory.
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";

using (Image image = Image.Load(sourceFilePath))
{
    // Your code for further steps goes here.
}
```

### Step 2: Set **CadRasterizationOptions**

在此我们配置决定 PDF 页面尺寸和分辨率的光栅化设置。

```csharp
// Create an instance of CadRasterizationOptions and set its various properties
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
```

> **Pro tip:** 调整 `PageWidth` 和 `PageHeight` 以匹配目标 PDF 布局的尺寸。更大的数值会提升细节，但也会增大文件体积。

### Step 3: Specify the layout name

告诉 Aspose.CAD 渲染哪个布局。将 `"Layout1"` 替换为 DWG 文件中布局的准确名称。

```csharp
// Specify desired layout name
rasterizationOptions.Layouts = new string[] { "Layout1" };
```

> **Why this matters:** 通过限制 `Layouts` 数组，可避免导出不需要的图纸，从而使 **dwg to pdf conversion c#** 操作更快，生成的 PDF 更简洁。

### Step 4: Create `PdfOptions`

将光栅化设置关联到 PDF 导出选项。

```csharp
// Create an instance of PdfOptions
PdfOptions pdfOptions = new PdfOptions();
// Set the VectorRasterizationOptions property
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

### Step 5: Export to PDF

最后，将渲染后的布局保存为 PDF 文件。

```csharp
MyDir = MyDir + "ExportSpecificLayoutToPDF_out.pdf";
// Export the DWG to PDF
image.Save(MyDir, pdfOptions);
```

### Step 6: Display a success message

快速的控制台输出可确认操作成功。

```csharp
// Display success message
Console.WriteLine("\nThe DWG file with a specific layout exported successfully to PDF.\nFile saved at " + MyDir);
```

## Common Issues & Solutions

| Issue | Cause | Fix |
|-------|-------|-----|
| **未生成 PDF** | `Layouts` 数组未匹配 DWG 中的任何布局名称。 | 使用 CAD 查看器确认布局名称并更新 `Layouts` 属性。 |
| **空白页** | `PageWidth`/`PageHeight` 设置为 0 或极小值。 | 使用合理尺寸（例如 1600 × 1600），或省略这些属性让 Aspose 自动计算。 |
| **比例不正确** | 高分辨率输出时未设置 DPI。 | 在导出前设置 `rasterizationOptions.Resolution = 300;`（或所需 DPI）。 |

## Frequently Asked Questions

**Q: 我可以同时导出多个布局吗？**  
A: 可以，只需在第 3 步中修改 `Layouts` 数组，包含所有需要的布局名称，例如 `new string[] { "Layout1", "Layout2" }`。

**Q: Aspose.CAD 是否兼容其他 CAD 文件格式？**  
A: 当然。它支持 DWG、DXF、DWF、DGN 等多种格式。

**Q: 除了页面尺寸外，我还能调整哪些 PDF 输出设置？**  
A: 可探索 `CadRasterizationOptions` 的其他属性，如 `Resolution`、`BackgroundColor`、`DrawType`，以微调输出效果。

**Q: 我在哪里可以找到更多 Aspose.CAD 文档？**  
A: 请访问 [documentation](https://reference.aspose.com/cad/net/) 获取深入的 API 参考和示例。

**Q: 是否提供免费试用？**  
A: 是的，您可以在 [here](https://releases.aspose.com/) 获取免费试用。

## Conclusion

您现在已经学会了 **设置 CAD 光栅化选项** 并使用它们 **将特定 DWG 布局导出为 PDF**，使用的是 Aspose.CAD for .NET。这种方法让您对转换过程拥有精确控制，能够快速、可靠地将 CAD‑to‑PDF 功能集成到任何 C# 应用程序中。

---

**Last Updated:** 2026-03-13  
**Tested With:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}