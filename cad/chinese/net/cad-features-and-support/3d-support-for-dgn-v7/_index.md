---
date: 2026-03-24
description: 学习如何使用 Aspose.CAD for .NET 将 DGN（包括 DGN V7）转换为 PDF（和 PNG），并支持 3D——一步一步的指南。
linktitle: 3D Support for DGN V7
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: 使用 Aspose.CAD for .NET 将 DGN 转换为 PDF（支持 3D）
url: /zh/net/cad-features-and-support/3d-support-for-dgn-v7/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.CAD for .NET 将 DGN 转换为 PDF（支持 3D）

## 介绍

在现代 CAD 工作流中，能够快速 **将 DGN 转换为 PDF** 并保留 3‑D 几何信息至关重要。无论是生成文档、向非 CAD 利益相关者共享设计，还是归档项目，Aspose.CAD for .NET 都提供了一种可靠的方式，将 DGN V7 文件转换为高质量的 PDF（甚至 PNG）输出。在本教程中，我们将逐步演示启用 3D 支持并从 DGN 文件生成 PDF 的完整步骤。

## 快速答疑
- **本教程覆盖哪些内容？** 启用 3D 支持并使用 Aspose.CAD for .NET 将 DGN V7 转换为 PDF。  
- **主要生成的格式是什么？** PDF（可选 PNG 导出）。  
- **是否需要许可证？** 免费试用可用于测试；生产环境需购买商业许可证。  
- **支持的 .NET 版本？** .NET Framework 4.5+、.NET Core 3.1+、.NET 5/6+。  
- **实现大约需要多长时间？** 基本转换约 10‑15 分钟。

## 什么是 “convert DGN to PDF”？

将 DGN 转换为 PDF 意味着将 MicroStation DGN 文件中存储的矢量数据渲染为一种可在任何设备上查看的便携文档格式，无需专门的 CAD 软件。借助 Aspose.CAD 的 3‑D 光栅化引擎，转换过程保留布局、颜色和深度信息，呈现出忠实的视觉效果。

## 为什么选择 Aspose.CAD 进行此转换？

- **完整的 3‑D 光栅化** – 保留深度和布局信息。  
- **无外部依赖** – 纯 .NET 库，无需 MicroStation。  
- **多种输出格式** – PDF、PNG、JPEG、TIFF 等（二级关键字 *convert dgn to png* 已开箱即用）。  
- **跨平台** – 支持 Windows、Linux 和 macOS。

## 前置条件

在开始之前，请确保具备以下条件：

- 已安装 Aspose.CAD for .NET。您可以从 [Aspose.CAD for .NET 下载页面](https://releases.aspose.com/cad/net/) 获取。  
- 一个有效的 DGN V7 文件。  
- .NET 开发环境（Visual Studio、VS Code 或 CLI）。安装说明请参阅 [.NET 文档](https://docs.microsoft.com/en-us/dotnet/core/install/)。

## 导入命名空间

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

这些命名空间为您提供对 Aspose.CAD 核心类和标准 .NET 实用程序的访问。

## 步骤 1：设置环境

定义源 DGN 文件所在位置以及输出 PDF 的保存路径。

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";
```

> **专业提示：** 使用 `Path.Combine` 构建平台无关的路径。

## 步骤 2：加载 DGN 文件

通过 `Image.Load` 加载文件，创建 `DgnImage` 实例。此步骤为光栅化准备 CAD 数据。

```csharp
using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Code snippet continues...
}
```

## 步骤 3：配置导出选项

设置 `PdfOptions` 并配合 `CadRasterizationOptions`。在此您可以控制页面尺寸、背景以及要导出的布局（视图）。

```csharp
var options = new PdfOptions
{
    VectorRasterizationOptions = new CadRasterizationOptions
    {
        PageWidth = 1500,
        PageHeight = 1500,
        CenterDrawing = true,
        AutomaticLayoutsScaling = true,
        BackgroundColor = Color.Black,
        Layouts = new string[] { "1", "2", "3", "9" } // Export specific views
    }
};
```

如果需要 **将 DGN 转换为 PNG**，只需将 `PdfOptions` 替换为 `PngOptions`，其余光栅化设置保持不变。

## 步骤 4：保存结果

最后，将渲染后的输出写入指定位置。

```csharp
string outFile = "Your Output Directory"; // Specify the output directory
dgnImage.Save(outFile, options);
```

执行完毕后，您将在目标位置找到一个 PDF 文件（若更改了选项则为 PNG），它忠实地呈现了原始 3‑D DGN 图纸。

## 常见问题与技巧

- **缺少布局：** 确保 `Layouts` 中的布局名称与 DGN 文件中的一致，否则会被忽略。  
- **大文件处理：** 逐步增大 `PageWidth`/`PageHeight`，以避免高内存占用。  
- **颜色准确性：** 若背景呈现为暗色，请检查 `BackgroundColor` 是否设置为期望的值（例如 `Color.White`）。

## 结论

您现在已经掌握了使用 Aspose.CAD for .NET 进行 **将 DGN 转换为 PDF** 并完整支持 3‑D 的方法。此工作流可集成到自动化流水线、桌面工具或 Web 服务中，为任何受众提供 CAD 可视化。

## 常见问答

### Q1：我可以使用此方法同时处理多个 DGN 文件吗？

A1：可以，您可以将代码修改为在循环中处理多个文件，或作为批处理系统的一部分。

### Q2：Aspose.CAD for .NET 还支持哪些导出格式？

A2：Aspose.CAD for .NET 支持多种导出格式，包括 PDF、PNG、JPG 等。详情请参阅 [文档](https://reference.aspose.com/cad/net/)。

### Q3：Aspose.CAD for .NET 是否兼容最新的 .NET Core 版本？

A3：是的，Aspose.CAD for .NET 设计上兼容最新的 .NET Core 版本。请确保在环境中安装了相应的版本。

### Q4：我可以进一步自定义导出设置以满足特定需求吗？

A4：当然！示例代码提供了一个起点。您可以在 [Aspose.CAD 文档](https://reference.aspose.com/cad/net/) 中探索更多选项和配置。

### Q5：我在哪里可以获取帮助或分享使用 Aspose.CAD for .NET 的经验？

A5：加入 Aspose.CAD 社区的 [论坛](https://forum.aspose.com/c/cad/19)，与其他开发者交流并获取帮助。

---

**最后更新：** 2026-03-24  
**测试环境：** Aspose.CAD 24.11 for .NET  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}