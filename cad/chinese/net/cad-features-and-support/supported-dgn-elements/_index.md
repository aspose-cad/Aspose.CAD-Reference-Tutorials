---
date: 2026-03-29
description: 了解如何使用 Aspose.CAD for .NET 将 DGN 转换为 PNG。本指南还涵盖 CAD 文件格式支持以及全部受支持的 DGN
  元素。
linktitle: Supported DGN Elements
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: 使用 Aspose.CAD for .NET 将 DGN 转换为 PNG
url: /zh/net/cad-features-and-support/supported-dgn-elements/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 将 DGN 转换为 PNG（使用 Aspose.CAD for .NET）

## 介绍

您是一名希望**无缝将 DGN 转换为 PNG**的 .NET 开发者吗？Aspose.CAD for .NET 提供了强大的解决方案，可高效处理 DGN 文件。在本教程中，我们将深入探讨受支持的 DGN 元素，指导您使用 Aspose.CAD for .NET 的整个过程，并准确演示如何将这些元素导出为 PNG 图像。

## 快速答案
- **Aspose.CAD 的作用是什么？** 它读取、修改并将 CAD/BIM 文件（包括 DGN）转换为 PNG 等光栅格式。  
- **我可以转换 2D 和 3D DGN 元素吗？** 可以——支持 2‑D 和 3‑D 实体。  
- **需要哪些 .NET 版本？** .NET Framework 4.5+、.NET Core 3.1+、.NET 5/6+。  
- **测试需要许可证吗？** 提供免费试用；生产环境需要许可证。  
- **在哪里获取库？** 从官方 Aspose 网站下载（链接在下方）。

## 什么是“将 DGN 转换为 PNG”？
将 DGN 转换为 PNG 意味着将基于矢量的 DGN 图纸（2‑D 或 3‑D）渲染为光栅图像格式（PNG）。当您需要在网页上显示 CAD 图纸、嵌入报告或生成缩略图而不依赖 CAD 查看器时，这非常有用。

## 为什么在 CAD 文件格式支持上使用 Aspose.CAD for .NET？
- **完整的 CAD 文件格式支持** – DGN、DWG、DXF、DWF 等。  
- **无外部依赖** – 纯 .NET 库，无需本地 CAD 安装。  
- **高保真渲染** – 保留线宽、颜色和 3‑D 几何体。  
- **批量处理** – 可在服务器端应用中轻松循环处理大量文件。

## 前置条件

在开始之前，请确保您具备以下条件：

- 基本的 .NET 编程知识。  
- 机器上已安装 Visual Studio。  
- Aspose.CAD for .NET 库，可在[此处](https://releases.aspose.com/cad/net/)下载。

## 导入命名空间

要启动项目，请在 .NET 应用程序中导入必要的命名空间。这一步确保您能够使用 Aspose.CAD for .NET 提供的功能。

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Dgn;
using Aspose.CAD.FileFormats.Dgn.DgnElements;
```

## 如何将 DGN 转换为 PNG

下面是一份逐步指南，帮助您加载 DGN 文件、遍历其元素、处理 2‑D 与 3‑D 实体，最后将结果导出为 PNG 光栅图像。

### 步骤 1：加载 DGN 文件

在 .NET 应用程序中将现有 DGN 文件加载为 `DgnImage`。

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Your code here
}
```

### 步骤 2：遍历 DGN 元素

使用 `foreach` 循环遍历 DGN 元素。Aspose.CAD for .NET 提供了多种 DGN 元素类型供您使用。

```csharp
foreach (DgnDrawingElementBase element in dgnImage.Elements)
{
    // Your code here
}
```

### 步骤 3：处理之前已支持的 2‑D 实体

这些实体现在也支持 3‑D 渲染。switch 语句可根据元素类型分支逻辑。

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.Line:
    case DgnElementType.Ellipse:
    case DgnElementType.Curve:
    // Additional cases
        {
            // Your code here
            break;
        }
}
```

### 步骤 4：处理已支持的 3‑D 实体

Aspose.CAD 为多个 3‑D DGN 元素提供了完整支持。根据需要扩展 switch 以处理它们。

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.SolidHeader3D:
    case DgnElementType.Cone:
    case DgnElementType.CellHeader:
        {
            // Your code here
            break;
        }
}
```

### 步骤 5：导出并保存为 PNG

在完成所需的任何操作后，将 DGN 图纸导出为 PNG 光栅图像并保存到指定目录。

```csharp
Console.WriteLine("\nThe DGN file exported successfully to raster image.\nFile saved at " + MyDir);
```

> **技巧提示：** 使用 `Image.Save` 与 `new PngOptions()` 来控制分辨率、背景颜色以及其他 PNG 特定设置。

## CAD 文件格式支持概览

Aspose.CAD for .NET 不仅限于 DGN，还支持 DWG、DXF、DWF 等众多 CAD 格式，为您提供一个统一的 API 来处理各种工程图纸。这使其成为需要跨多种标准实现**CAD 文件格式支持**的项目的理想选择。

## 常见问题与解决方案

| 问题 | 原因 | 解决方案 |
|-------|--------|-----|
| **图像为空白** | 导出时 DPI 为零 | 在 `PngOptions` 中指定 `ResolutionX` 和 `ResolutionY`。 |
| **缺少 3‑D 几何体** | 在 switch 中未处理该元素类型 | 添加缺失的 `DgnElementType` case 并相应渲染。 |
| **大文件导致内存不足** | 一次性加载整个文件 | 分批处理元素或在可能的情况下使用流式处理。 |

## 常见问题

### 问题 1：在哪里可以找到 Aspose.CAD for .NET 的文档？
A1: 您可以在[此处](https://reference.aspose.com/cad/net/)找到文档。

### 问题 2：如何下载 Aspose.CAD for .NET？
A2: 您可以在[此处](https://releases.aspose.com/cad/net/)下载库。

### 问题 3：是否提供 Aspose.CAD for .NET 的免费试用？
A3: 是的，您可以在[此处](https://releases.aspose.com/)获取免费试用。

### 问题 4：在哪里可以获取 Aspose.CAD for .NET 的临时许可证？
A4: 临时许可证可在[此处](https://purchase.aspose.com/temporary-license/)获取。

### 问题 5：需要帮助或有疑问？
A5: 访问 Aspose.CAD for .NET 社区的[支持论坛](https://forum.aspose.com/c/cad/19)。

---

**最后更新：** 2026-03-29  
**测试版本：** Aspose.CAD for .NET 24.11  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}