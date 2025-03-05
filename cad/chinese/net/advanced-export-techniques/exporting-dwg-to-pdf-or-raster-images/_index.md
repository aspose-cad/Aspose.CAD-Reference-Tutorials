---
title: 将 DWG 导出为 PDF 或光栅图像 - Aspose.CAD 指南
linktitle: 将 DWG 导出为 PDF 或光栅图像
second_title: Aspose.CAD .NET - CAD 和 BIM 文件格式
description: 探索有关使用 Aspose.CAD for .NET 将 DWG 导出为 PDF 或光栅图像的综合指南。了解步骤、先决条件，并亲身体验这个强大的库。
type: docs
weight: 11
url: /zh/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/
---
## 介绍

您是否希望在 .NET 应用程序中将 DWG 文件无缝转换为 PDF 或光栅图像？别再犹豫了！本分步指南将引导您完成使用强大的 Aspose.CAD for .NET 库的过程。无论您是经验丰富的开发人员还是新手，本教程都适合所有技能水平。

## 先决条件

在我们深入学习本教程之前，请确保您已准备好以下内容：

- 对 .NET 编程有基本的了解。
- 安装了 Aspose.CAD for .NET 库。如果没有，请下载[这里](https://releases.aspose.com/cad/net/).
- 您最喜欢的用于 .NET 开发的集成开发环境 (IDE)。

## 导入命名空间

让我们首先在 .NET 项目中导入必要的命名空间。这确保您可以在代码中访问 Aspose.CAD 功能。

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

## 第 1 步：加载 DWG 文件

首先加载您想要转换的 DWG 文件。将“您的文档目录”替换为 DWG 文件的路径。

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    //您的加载 DWG 代码位于此处
}
```

## 第 2 步：设置 PDF 导出

现在，让我们配置 PDF 导出设置。此示例演示如何设置布局和处理单位转换。

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new string[] { "Model" };

//检查并定义单位制
bool currentUnitIsMetric = false;
double currentUnitCoefficient = 1.0;
DefineUnitSystem(cadImage.UnitType, out currentUnitIsMetric, out currentUnitCoefficient);

//设置 PDF 导出的代码位于此处
```

## 第 3 步：导出为 PDF

使用配置的设置执行导出为 PDF。

```csharp
PdfOptions pdfOptions = new PdfOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath, pdfOptions);
```

## 第 4 步：导出为光栅图像

扩展功能以导出为光栅图像，例如 PNG。

```csharp
// A4 尺寸，300 DPI - 2480 x 3508
rasterizationOptions.PageHeight = 3508;
rasterizationOptions.PageWidth = 2480;

PngOptions pngOptions = new PngOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath.Replace("pdf", "png"), pngOptions);
```

## 结论

恭喜！您已成功学习如何使用 Aspose.CAD for .NET 将 DWG 文件导出为 PDF 和光栅图像。这个强大的库简化了流程，使其高效且对开发人员友好。

## 常见问题解答

### Q1：我可以在我的商业项目中使用 Aspose.CAD for .NET 吗？

 A1: 是的，可以。访问[buy.aspose.com/buy](https://purchase.aspose.com/buy)了解许可详细信息。

### Q2: 有免费试用吗？

 A2：当然！获取免费试用[这里](https://releases.aspose.com/).

### 问题 3：如何获得 Aspose.CAD for .NET 支持？

A3：前往[Aspose.CAD论坛](https://forum.aspose.com/c/cad/19)以获得社区支持。

### Q4：我可以获得临时许可证用于测试目的吗？

 A4：是的，您可以获得临时许可证[这里](https://purchase.aspose.com/temporary-license/).

### Q5：在哪里可以找到详细的文档？

 A5：该文档可在以下位置获取：[CAD软件](https://reference.aspose.com/cad/net/).