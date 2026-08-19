---
date: 2026-03-19
description: 学习如何在 .NET 中使用 Aspose.CAD 将 CAD 转换为 PNG，高效保存 CAD 为 PNG，并简化光栅图像工作流程。
linktitle: Convert CAD Drawing to Raster Image
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: 在 Aspose.CAD for .NET 中将 CAD 转换为 PNG
url: /zh/net/cad-drawing-manipulation/convert-cad-drawing-to-raster-image/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 Aspose.CAD for .NET 中将 CAD 转换为 PNG

## 简介

在现代以 CAD 为中心的应用中，**将 CAD 转换为 PNG** 是一个常见需求——无论是生成缩略图、在网页中嵌入图纸，还是将设计存档为光栅图像。本教程将手把手演示如何使用 Aspose.CAD for .NET 库将 CAD 图纸（DXF、DWG 等）转换为高质量的 PNG 文件。完成后，您将能够 **将 CAD 保存为 PNG**，并对光栅化设置进行完整控制，使工作流更快、更可靠。

## 快速回答
- **哪个库最适合 CAD 转 PNG 转换？** Aspose.CAD for .NET。  
- **哪些文件格式可以导出为 PNG？** DWG、DXF、DGN 以及其他受支持的 CAD 格式。  
- **生产环境是否需要许可证？** 是的，需购买商业许可证；提供免费试用版。  
- **我可以自定义图像尺寸和质量吗？** 当然——光栅化选项允许您设置页面宽度、高度、背景颜色等。  
- **代码是否兼容 .NET Core / .NET 6？** 是的，同一 API 可在 .NET Framework、.NET Core 和 .NET 5/6 上运行。

## 什么是“将 CAD 转换为 PNG”？
将 CAD 转换为 PNG 意味着将基于向量的 CAD 图纸光栅化为基于像素的图像格式（PNG）。此过程在保持视觉保真度的同时，使文件能够在浏览器、移动应用或任何不原生支持 CAD 格式的环境中轻松显示。

## 为什么使用 Aspose.CAD 将 CAD 转换为 PNG？
- **无外部依赖** – 纯 .NET 实现，无需本机 CAD 引擎。  
- **完整格式支持** – 支持 DWG、DXF、DGN 等多种格式。  
- **细粒度光栅化控制** – 页面尺寸、分辨率、背景、线宽等均可自定义。  
- **高性能** – 为服务器端批处理优化。

## 先决条件

在开始之前，请确保您已拥有：

1. **Aspose.CAD for .NET** – 从[下载页面](https://releases.aspose.com/cad/net/)获取。  
2. 支持 .NET 的 IDE（Visual Studio、Rider 或 VS Code），项目目标为 .NET Framework 4.6+ 或 .NET Core 3.1+。  

## 导入命名空间

在 .NET 项目中，导入必要的命名空间以使用 Aspose.CAD 功能。在代码文件开头添加如下内容：

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## 分步指南

### 步骤 1：定义文件路径
设置源 CAD 文件和目标 PNG 路径。将占位符替换为您机器上的实际目录。

```csharp
// The path to the documents directory.
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";
```

### 步骤 2：加载 CAD 图纸
使用 `Aspose.CAD.Image.Load` 打开 CAD 文件。这会在内存中创建图纸的表示，供后续光栅化使用。

```csharp
using (Aspose.CAD.Image image = Aspose.CAD.Image.Load(sourceFilePath))
{
```

### 步骤 3：配置光栅化选项  
定义向量数据如何转换为像素。这里我们设置了 1200 × 1200 像素的画布，您可以根据需要调整 `PageWidth` 和 `PageHeight`（例如在特定 DPI 下 **convert dwg to png**）。

```csharp
// Create an instance of CadRasterizationOptions
Aspose.CAD.ImageOptions.CadRasterizationOptions rasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
// Set page width & height
rasterizationOptions.PageWidth = 1200;
rasterizationOptions.PageHeight = 1200;
```

> **专业提示：** 为提升大图纸的渲染速度，您也可以将 `rasterizationOptions.BackgroundColor` 设置为纯色，或启用 `rasterizationOptions.DrawType` 以加快向量转换。

### 步骤 4：为生成的图像创建 PNG 选项  
将光栅化设置包装在 `PngOptions` 对象中，告知 Aspose.CAD 输出 PNG 文件。

```csharp
// Create an instance of PngOptions for the resultant image
ImageOptionsBase options = new Aspose.CAD.ImageOptions.PngOptions();
// Set rasterization options
options.VectorRasterizationOptions = rasterizationOptions;
```

### 步骤 5：保存生成的 PNG  
将目录路径与期望的文件名组合，并将光栅化后的图像写入磁盘。此步骤 **将 CAD 保存为 PNG**。

```csharp
MyDir = MyDir + "conic_pyramid_raster_image_out.png";
// Save resultant image
image.Save(MyDir, options);
```

### 步骤 6：显示成功信息  
确认转换成功并显示文件保存位置。

```csharp
//ExEnd:ConvertDrawingToRasterImage            
Console.WriteLine("\nCAD drawing converted successfully to raster image format.\nFile saved at " + MyDir);
```

> **注意：** 第 2 步中的 `using` 块会自动释放 `Image` 对象，确保所有资源得到释放。

## 常见问题及解决方案

| 问题 | 原因 | 解决方案 |
|-------|-------|-----|
| **空白 PNG 输出** | 未设置光栅化选项（例如缺少 `PageWidth`/`PageHeight`）。 | 确保 `CadRasterizationOptions` 定义了非零的画布大小。 |
| **颜色不正确** | 背景颜色默认白色；源图纸使用透明图层。 | 设置 `rasterizationOptions.BackgroundColor = Color.Transparent;` |
| **大型 DWG 文件性能延迟** | 高分辨率且未使用分块。 | 使用 `rasterizationOptions.LayoutOptions` 限制渲染区域或降低 DPI。 |
| **许可证异常** | 生产环境未使用有效许可证。 | 在加载图像前通过 `License license = new License(); license.SetLicense("Aspose.CAD.lic");` 应用许可证。 |

## 常见问题

### Q1: Aspose.CAD 是否兼容所有 CAD 文件格式？
A1: Aspose.CAD 支持广泛的 CAD 文件格式，包括 DWG、DXF、DGN 等。请参阅[文档](https://reference.aspose.com/cad/net/)获取完整列表。

### Q2: 我可以为不同项目自定义光栅化选项吗？
A2: 可以，Aspose.CAD 提供了丰富的光栅化选项，开发者可根据项目需求定制输出。

### Q3: Aspose.CAD 是否提供免费试用？
A3: 是的，您可以使用免费试用版探索 Aspose.CAD 的功能。请访问[此处](https://releases.aspose.com/)开始使用。

### Q4: 如何获取 Aspose.CAD 的技术支持？
A4: 如需帮助或咨询，请访问 Aspose.CAD 的[支持论坛](https://forum.aspose.com/c/cad/19)。

### Q5: 是否有临时许可证可供使用？
A5: 有，开发者可通过[此链接](https://purchase.aspose.com/temporary-license/)获取 Aspose.CAD 的临时许可证。

### Q6: 我可以使用此方法 **convert DWG to PNG** 吗？
A6: 完全可以。相同代码适用于 DWG 文件，只需将源文件扩展名改为 `.dwg`。

### Q7: 如何 **export DXF to image** 并使用透明背景？
A7: 在保存 PNG 前设置 `rasterizationOptions.BackgroundColor = Color.Transparent;`。

---

**最后更新：** 2026-03-19  
**测试环境：** Aspose.CAD 24.11 for .NET（最新发布）  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}