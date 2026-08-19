---
date: 2026-03-16
description: 学习如何使用 Aspose.CAD for .NET 将 DWG 转换为 PDF 或光栅图像。本一步步的 CAD 转 PDF 教程涵盖将
  DWG 导出为 PNG 等图像格式，并展示如何高效地将 DWG 导出为图像文件。
linktitle: Exporting DWG to PDF or Raster Images
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: 如何使用 Aspose.CAD for .NET 将 DWG 转换为 PDF 和光栅图像
url: /zh/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 将 DWG 导出为 PDF 或光栅图像 - Aspose.CAD 指南

## 介绍

如果您需要在 .NET 应用程序中 **将 DWG 转换为 PDF**（或转换为 PNG 等光栅格式），那么您来对地方了。在本教程中，我们将逐步演示使用 Aspose.CAD for .NET 完成转换的具体步骤，说明为何该库是可靠的选择，并展示仅用几行代码即可同时处理 PDF 和图像输出。

## 快速答案
- **哪个库负责 DWG 转换？** Aspose.CAD for .NET  
- **我可以同时导出 DWG 为 PNG 和 PDF 吗？** 可以——相同的光栅化选项适用于两种格式。  
- **开发阶段需要许可证吗？** 免费试用可用于测试；生产环境需要商业许可证。  
- **支持哪些 .NET 版本？** .NET Framework 4.5+、.NET Core 3.1+、.NET 5/6+。  
- **单位转换会自动处理吗？** 您可以像代码示例中那样手动定义单位系统（公制或英制）。

## 什么是 “convert DWG to PDF”？
将 DWG 转换为 PDF 意味着将 CAD 图纸（DWG）渲染为一种便携的、只能查看的文档（PDF）。这对于向没有 CAD 软件的利益相关者共享设计、创建可打印文档或以通用可读格式归档图纸非常有用。

## 为什么使用 Aspose.CAD 进行此转换？
- **无外部依赖** – 库完全基于托管代码运行。  
- **高保真度** – 保留图层、线宽和布局信息。  
- **内置光栅选项** – 只需一个配置对象即可导出为 PNG、JPEG、BMP 等。  
- **跨平台** – 在 Windows、Linux 和 macOS 上均可通过 .NET Core 使用。

## 前置条件

在开始教程之前，请确保具备以下条件：

- 对 .NET 编程有基本了解。  
- 已安装 Aspose.CAD for .NET 库。若未安装，请在此处下载 [here](https://releases.aspose.com/cad/net/)。  
- 已配置好用于 .NET 开发的集成开发环境（IDE）。

## 导入命名空间

首先在 .NET 项目中导入必要的命名空间，以便在代码中使用 Aspose.CAD 功能。

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
```

## 第一步：加载 DWG 文件

加载您想要转换的 DWG 文件。将 `"Your Document Directory"` 替换为 DWG 文件的实际路径。

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Your code for loading DWG goes here
}
```

## 第二步：设置 PDF 导出（如何将 DWG 导出为 PDF）

接下来配置 PDF 导出设置。此示例演示如何设置布局并处理单位转换。

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new string[] { "Model" };

// Check and define the unit system
bool currentUnitIsMetric = false;
double currentUnitCoefficient = 1.0;
DefineUnitSystem(cadImage.UnitType, out currentUnitIsMetric, out currentUnitCoefficient);

// Your code for setting up PDF export goes here
```

## 第三步：导出为 PDF

使用已配置的设置执行 PDF 导出。

```csharp
PdfOptions pdfOptions = new PdfOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath, pdfOptions);
```

## 第四步：导出为光栅图像（export dwg to image）

扩展功能以导出为光栅图像，例如 PNG。

```csharp
// A4 size at 300 DPI - 2480 x 3508
rasterizationOptions.PageHeight = 3508;
rasterizationOptions.PageWidth = 2480;

PngOptions pngOptions = new PngOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath.Replace("pdf", "png"), pngOptions);
```

## 常见问题及解决方案

| 问题 | 产生原因 | 解决办法 |
|-------|----------------|------------|
| **PDF 中出现空白页** | 布局未正确指定 | 确保 `rasterizationOptions.Layouts` 包含正确的布局名称（例如 `"Model"`）。 |
| **尺寸不正确** | DPI 或页面尺寸不匹配 | 在 `CadRasterizationOptions` 中调整 `PageHeight`、`PageWidth` 和 DPI 值。 |
| **单位显示错误** | 未定义单位转换 | 使用 `DefineUnitSystem` 根据 `cadImage.UnitType` 设置 `currentUnitIsMetric` 和 `currentUnitCoefficient`。 |
| **许可证异常** | 试用版限制 | 在调用 `Image.Load` 之前应用临时或永久许可证。 |

## 常见问答

### Q1: 我可以在商业项目中使用 Aspose.CAD for .NET 吗？
A1: 可以。请访问 [purchase.aspose.com/buy](https://purchase.aspose.com/buy) 获取授权详情。

### Q2: 是否提供免费试用？
A2: 当然！在此处获取免费试用 [here](https://releases.aspose.com/)。  

### Q3: 如何获取 Aspose.CAD for .NET 的支持？
A3: 前往 [Aspose.CAD 论坛](https://forum.aspose.com/c/cad/19) 获取社区支持。

### Q4: 我可以获取用于测试的临时许可证吗？
A4: 可以，临时许可证请点击 [here](https://purchase.aspose.com/temporary-license/)。  

### Q5: 哪里可以找到详细文档？
A5: 文档位于 [Aspose.CAD](https://reference.aspose.com/cad/net/)。  

### Q6: 如何 **将 CAD 保存为 PNG** 并保持高质量？
A6: 在 `CadRasterizationOptions` 中将 `PageHeight` 与 `PageWidth` 设置为所需像素尺寸，并选择 300 DPI 或更高的 DPI。  

### Q7: 当源文件包含多个布局时，**如何转换 dwg** 是最佳做法？
A7: 将所有需要导出的布局名称填入 `rasterizationOptions.Layouts`，然后遍历每个布局并对每种输出格式调用 `Save`。

---

**最后更新：** 2026-03-16  
**测试环境：** Aspose.CAD 24.11 for .NET  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}