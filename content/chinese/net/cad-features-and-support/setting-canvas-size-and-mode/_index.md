---
title: 在 Aspose.CAD for .NET 中设置画布大小和模式
linktitle: 设置画布大小和模式
second_title: Aspose.CAD .NET - CAD 和 BIM 文件格式
description: 探索有关在 Aspose.CAD for .NET 中设置画布大小和模式的分步指南。使用此综合教程轻松优化您的 CAD 渲染。
type: docs
weight: 16
url: /zh/net/cad-features-and-support/setting-canvas-size-and-mode/
---
## 介绍

您准备好释放 Aspose.CAD for .NET 的全部潜力并彻底改变您的 CAD 渲染体验了吗？在本分步教程中，我们将深入研究使用强大的 Aspose.CAD 库设置画布大小和模式的复杂性。无论您是经验丰富的开发人员还是新手，本指南都将引导您完成整个过程，确保您有效地利用 Aspose.CAD 的功能。

## 先决条件

在我们深入学习本教程之前，请确保您具备以下先决条件：

-  Aspose.CAD 库：从以下位置下载并安装 Aspose.CAD 库：[Aspose.CAD 网站](https://releases.aspose.com/cad/net/).

- 开发环境：确保您的计算机上设置了 .NET 开发环境。

- 示例 CAD 文件：在本教程中，我们将使用示例 DXF 文件。您可以在[Aspose.CAD 文档](https://reference.aspose.com/cad/net/).

## 导入命名空间

首先，在 .NET 应用程序的开头导入必要的命名空间：

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## 第 1 步：加载 CAD 文件

首先使用以下代码加载 CAD 文件：

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (Image image = Image.Load(sourceFilePath))
{
    //您的进一步步骤的代码将位于此处
}
```

## 第 2 步：创建 CadRasterizationOptions

创建一个实例`CadRasterizationOptions`并设置其属性：

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.AutomaticLayoutsScaling = true;
rasterizationOptions.NoScaling = false;
```

## 第 3 步：创建 PdfOptions

创建一个实例`PdfOptions`并设置其`VectorRasterizationOptions`财产：

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## 第 4 步：导出为 PDF

使用配置的选项将 CAD 文件导出为 PDF：

```csharp
image.Save(MyDir + "result_out.pdf", pdfOptions);
```

## 第 5 步：创建 TiffOptions

创建一个实例`TiffOptions`并设置其`VectorRasterizationOptions`财产：

```csharp
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.VectorRasterizationOptions = rasterizationOptions;
```

## 第 6 步：导出为 TIFF

使用配置的选项将 CAD 文件导出为 TIFF：

```csharp
image.Save(MyDir + "result_out.tiff", tiffOptions);
```

## 结论

恭喜！您已在 Aspose.CAD for .NET 中成功设置画布大小和模式。这一强大的功能为 CAD 渲染开辟了无限可能。尝试不同的选项并发现 Aspose.CAD 在 .NET 应用程序中的全部潜力。

## 常见问题解答

### Q1：我可以将 Aspose.CAD 与其他 .NET 库一起使用吗？

A1：是的，Aspose.CAD 与其他 .NET 库无缝集成，为 CAD 操作提供增强的功能。

### Q2：Aspose.CAD 可以免费试用吗？

 A2：是的，您可以通过免费试用来探索 Aspose.CAD 的功能。访问[这里](https://releases.aspose.com/)开始。

### Q3：如何获得 Aspose.CAD 的支持？

A3： 如需支持和讨论，请访问[Aspose.CAD论坛](https://forum.aspose.com/c/cad/19).

### 问题 4：在哪里可以找到 Aspose.CAD 的综合文档？

 A4：请参阅[Aspose.CAD 文档](https://reference.aspose.com/cad/net/)获取详细信息和示例。

### Q5：如何购买 Aspose.CAD for .NET？

 A5：要购买 Aspose.CAD，请访问[购买页面](https://purchase.aspose.com/buy).