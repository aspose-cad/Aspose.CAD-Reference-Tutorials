---
date: 2026-03-21
description: 了解如何在 .NET 中使用 Aspose.CAD 获取 CAD 布局尺寸。按照我们的分步指南，高效操作 CAD 文件。
linktitle: Get Size of CAD Layout
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: 在 Aspose.CAD for .NET 中获取 CAD 布局尺寸
url: /zh/net/cad-drawing-manipulation/get-size-of-cad-layout/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 获取 Aspose.CAD for .NET 中的 CAD 布局尺寸

## Introduction

在本综合教程中，您将了解**如何使用 Aspose.CAD for .NET 库获取 CAD 布局尺寸**。无论您是构建 CAD 查看器、生成缩略图，或需要精确的布局尺寸用于后续处理，了解每个布局的确切尺寸都是必不可少的。我们将一步步演示完整工作流——从加载图纸到提取布局尺寸，并可选择将其保存为图像——帮助您自信地将此功能集成到自己的应用程序中。

## Quick Answers
- **“获取 CAD 布局尺寸” 是什么意思？** 它指的是检索 CAD 文件中每个非空布局的宽度和高度（以图纸单位表示）。  
- **哪个库支持此功能？** Aspose.CAD for .NET 提供了一个简易的 API 来访问布局信息。  
- **我需要许可证吗？** 免费试用可用于评估；生产环境需要商业许可证。  
- **支持的格式？** 完全支持 DWG、DXF 以及许多其他 CAD/BIM 格式。  
- **典型实现时间？** 基本的尺寸检索例程大约需要 10‑15 分钟。

## 什么是“获取 CAD 布局尺寸”？

获取 CAD 布局尺寸是指提取 CAD 图纸中每个布局（纸空间）的几何范围。这些范围以图纸的原生单位（通常为毫米或英寸）表示，可用于缩放、打印或生成预览图像等任务。

## 为什么使用 Aspose.CAD 获取 CAD 布局尺寸？

- **无需 CAD 软件** – 完全在服务器端运行。  
- **跨平台** – 支持 .NET Framework、.NET Core 以及 .NET 5/6+。  
- **精确测量** – 返回文件中存储的精确范围，避免手动解析。  
- **易于集成** – 简单的 API 调用自然融入现有的 C# 项目。

## 先决条件

在开始编写代码之前，请确保您具备以下条件：

- 已安装 Aspose.CAD for .NET。您可以从 [Aspose.CAD for .NET 下载页面](https://releases.aspose.com/cad/net/) 下载。  
- 一个或多个您想要分析的 CAD 文件（DWG、DXF 等）。本指南使用 `conic_pyramid.dxf` 和 `Bottom_plate.dwg` 作为示例文件。

## 导入命名空间

在您的 .NET 项目中，首先导入所需的命名空间：

```csharp
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.ImageOptions;
```

## 步骤 1：设置文档目录

定义包含 CAD 文件的文件夹。将占位符替换为您机器上的实际路径。

```csharp
string MyDir = "Your Document Directory";
```

## 步骤 2：指定 CAD 文件路径

创建一个数组，指向您想要处理的每个 CAD 文件。

```csharp
string[] sourceFilePaths = new[]
{
    MyDir + "conic_pyramid.dxf",
    MyDir + "Bottom_plate.dwg"
};
```

## 步骤 3：遍历 CAD 文件

加载每个文件，检测其格式，并准备提取布局信息。

```csharp
foreach (var sourceFilePath in sourceFilePaths)
{
    string extension = Path.GetExtension(sourceFilePath);
    using (CadImage cadImage = (CadImage)Aspose.CAD.Image.Load(sourceFilePath))
    {
        // ... (continue to the next step)
    }
}
```

## 步骤 4：获取非空布局

我们需要一个辅助方法，仅返回实际包含绘图实体的布局。空布局将被忽略，因为它们没有可报告的尺寸。

```csharp
private static List<string> GetNotEmptyLayouts(Image cadImage, string extension)
{
    // ... (continue to the next step)
}
```

## 步骤 5：获取 DWG 文件的布局

DWG 文件将布局信息存储在 `HeaderVariables` 表中。以下方法提取 DWG 图纸中所有非空布局的名称。

```csharp
private static List<string> GetNotEmptyLayoutsForDwg(CadImage cadImage)
{
    // ... (continue to the next step)
}
```

## 步骤 6：获取 DXF 文件的布局

DXF 文件使用不同的结构。此方法解析 `Tables` 集合，以查找包含实体的纸空间布局。

```csharp
private static List<string> GetNotEmptyLayoutsForDxf(CadImage cadImage)
{
    // ... (continue to the next step)
}
```

## 步骤 7：检索布局尺寸并保存为图像

最后，遍历每个发现的布局，读取其范围，并可选择将布局渲染为图像文件以进行可视化验证。

```csharp
foreach (string layout in layouts)
{
    // ... (continue to the next step)
}
```

## 常见问题与技巧

- **缺少布局名称：** 确保 CAD 文件实际包含纸空间布局；有些文件仅有模型空间。  
- **单位不正确：** 尺寸以图纸的原生单位返回。如有需要，请转换为毫米或英寸。  
- **性能：** 加载非常大的 DWG/DXF 文件可能会占用大量内存；考虑异步或批量处理文件。

## 常见问题解答

**问：Aspose.CAD 是否兼容所有 CAD 文件格式？**  
**答：** 是的，Aspose.CAD 支持广泛的格式，包括 DWG、DXF、DGN 以及许多 BIM 文件类型。

**问：我可以自定义图像保存选项吗？**  
**答：** 当然可以！您可以调整 `CadRasterizationOptions`（格式、分辨率、背景颜色等）以满足您的特定需求。

**问：在哪里可以找到更多文档？**  
**答：** 请参考 [Aspose.CAD 文档](https://reference.aspose.com/cad/net/)，其中包含详细的 API 参考和更多示例。

**问：是否提供免费试用？**  
**答：** 是的，您可以通过 [免费试用](https://releases.aspose.com/) 体验 Aspose.CAD。

**问：如何获取技术支持？**  
**答：** 请访问 [Aspose.CAD 论坛](https://forum.aspose.com/c/cad/19) 获取技术支持。

---

**最后更新：** 2026-03-21  
**测试环境：** Aspose.CAD 24.11 for .NET  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}