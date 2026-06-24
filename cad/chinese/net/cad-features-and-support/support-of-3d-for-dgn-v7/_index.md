---
date: 2026-03-29
description: 了解如何使用 Aspose.CAD for .NET 配置 CAD 光栅化选项并将 DGN 导出为支持 3D 的 PDF。
linktitle: Support of 3D for DGN V7
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: 为 DGN V7 3D 配置 CAD 栅格化选项
url: /zh/net/cad-features-and-support/support-of-3d-for-dgn-v7/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 配置 DGN V7 3D 的 CAD 光栅化选项

## 介绍

在本综合教程中，您将学习**如何配置 CAD 光栅化选项**，以使用 Aspose.CAD for .NET 将 3‑D DGN V7 文件导出为 PDF。无论您是构建 CAD 查看器、报告工具，还是自动化转换流水线，掌握这些设置都能让您精确控制页面尺寸、布局缩放、背景颜色以及要渲染的特定视图。让我们一步一步地完成此过程。

## 快速答案
- **“configure CAD rasterization options” 是什么意思？**  
  它指在将 CAD 文件转换为光栅格式（例如 PDF）之前，设置页面尺寸、缩放、背景颜色和布局选择等属性。
- **如何导出支持 3‑D 的 DGN 为 PDF？**  
  使用 `DgnImage` 加载 DGN，定义 `PdfOptions` + `CadRasterizationOptions`，然后调用 `Save`。
- **生产环境是否需要许可证？**  
  是的——部署需要商业许可证；提供免费试用版。
- **支持哪些 .NET 版本？**  
  .NET Framework 4.5+、.NET Core 3.1+、.NET 5/6/7。
- **可以选择特定视图导出吗？**  
  完全可以——在光栅化选项中设置 `Layouts` 数组。

## 什么是“configure CAD rasterization options”？

配置 CAD 光栅化选项意味着自定义 CAD 图纸的光栅化方式（从矢量转换为位图或 PDF）。通过调整这些设置，您可以控制输出的视觉效果、性能以及生成文档的文件大小。

## 为什么使用 Aspose.CAD 进行 3‑D DGN V7 导出？

- **完整的 .NET 集成** – 无需 COM 或本机 DLL。  
- **支持 3‑D 几何** – 在渲染为 PDF 时保留深度信息。  
- **细粒度控制** – 选择精确的布局、缩放和背景颜色。  
- **跨平台** – 在 Windows、Linux 和 macOS 上使用 .NET Core 工作。

## 前提条件

在开始之前，请确保您已拥有：

- **Aspose.CAD for .NET** – 从 [here](https://releases.aspose.com/cad/net/) 下载。  
- **Visual Studio** 或任何兼容的 .NET IDE。  
- **示例 DGN 文件** – 本指南使用 `Nikon_D90_Camera.dgn`（包含在 Aspose 示例包中）。  

现在一切准备就绪，让我们深入代码。

## 导入命名空间

在您的 .NET 项目中，导入所需的命名空间：

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Dgn;
using Aspose.CAD.ImageOptions;
```

## 步骤 1：设置文档目录

创建一个变量，指向存放源 DGN 和输出文件的文件夹。

```csharp
string MyDir = "Your Document Directory";
```

## 步骤 2：加载 DGN 文件

将 DGN 文件加载为 `DgnImage`。该对象让您能够访问 CAD 数据和光栅化管道。

```csharp
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";
string outFile = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Your code for further processing goes here
}
```

## 步骤 3：配置 PDF 导出选项（Configure CAD Rasterization Options）

在此我们**配置 CAD 光栅化选项**，决定 3‑D 模型如何渲染为 PDF。您可以调整页面尺寸、启用自动布局缩放、设置背景颜色，并选择要导出的精确布局（视图）。

```csharp
var options = new PdfOptions
{
    VectorRasterizationOptions = new CadRasterizationOptions
    {
        PageWidth = 1500,
        PageHeight = 1500,
        AutomaticLayoutsScaling = true,
        BackgroundColor = Color.Black,
        Layouts = new string[] { "1", "2", "3", "9" } // Only export specified views
    }
};
```

## 步骤 4：保存光栅图像

最后，使用刚才配置的选项将 DGN 导出为 PDF 文件。

```csharp
dgnImage.Save(outFile, options);
```

## 常见问题及解决方案

| 问题 | 解决方案 |
|-------|----------|
| **Blank PDF output** | 验证 `Layouts` 数组包含 DGN 文件中存在的正确视图标识符。 |
| **Incorrect colors** | 确保 `BackgroundColor` 设置为所需的值；使用 `Color.White` 可获得浅色背景。 |
| **Performance bottleneck on large files** | 启用 `AutomaticLayoutsScaling`，并考虑降低 `PageWidth/PageHeight` 以获得更小的光栅分辨率。 |
| **License exception** | 在加载图像之前安装有效的 Aspose.CAD 许可证，以避免试用水印。 |

## 常见问题

**Q: 我可以在 .NET 中使用 Aspose.CAD 处理其他 CAD 文件格式吗？**  
A: 可以，Aspose.CAD 支持 DWG、DXF、DWF、DGN 等多种格式。

**Q: 使用 Aspose.CAD 时如何处理异常？**  
A: 将代码包装在 `try‑catch` 块中，并检查 `Aspose.CAD.CADException` 以获取详细错误信息。

**Q: Aspose.CAD 适用于商业项目吗？**  
A: 绝对适用。您可以在 [here](https://purchase.aspose.com/buy) 购买许可证。

**Q: 在购买前我可以试用 Aspose.CAD for .NET 吗？**  
A: 可以，免费试用版可在 [here](https://releases.aspose.com/) 获取。

**Q: 哪里可以找到 Aspose.CAD 的社区支持？**  
A: 请前往讨论论坛 [here](https://forum.aspose.com/c/cad/19)。

---

**最后更新：** 2026-03-29  
**测试环境：** Aspose.CAD 24.11 for .NET  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}