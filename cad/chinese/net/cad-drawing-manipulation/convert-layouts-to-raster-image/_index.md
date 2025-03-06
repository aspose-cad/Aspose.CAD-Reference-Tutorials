---
title: 在 Aspose.CAD for .NET 中将布局转换为光栅图像
linktitle: 将布局转换为光栅图像
second_title: Aspose.CAD .NET - CAD 和 BIM 文件格式
description: 使用 Aspose.CAD for .NET 轻松将 CAD 布局转换为光栅图像。利用强大的 CAD 操作功能增强您的开发。
weight: 12
url: /zh/net/cad-drawing-manipulation/convert-layouts-to-raster-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 Aspose.CAD for .NET 中将布局转换为光栅图像

## 介绍

您是否希望在 .NET 应用程序中轻松地将布局转换为光栅图像？别再犹豫了！本分步指南将引导您完成使用 Aspose.CAD for .NET 的过程，这是一个功能强大的库，可简化计算机辅助设计 (CAD) 任务。

## 先决条件

在深入学习本教程之前，请确保您具备以下先决条件：

- Aspose.CAD for .NET 库：从以下位置下载并安装该库：[Aspose.CAD for .NET 下载页面](https://releases.aspose.com/cad/net/).

- 开发环境：确保您的计算机上设置了有效的 .NET 开发环境。

- 要转换的文档：准备包含要转换为光栅图像的布局的 CAD 文档。

- 您的文档目录：将代码中的占位符“您的文档目录”替换为您的文档目录的路径。

## 导入命名空间

首先，让我们导入必要的命名空间，以使 Aspose.CAD 功能可以在您的代码中访问。

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## 第 1 步：加载 CAD 文档

首先使用 Aspose.CAD 库加载 CAD 文档。

```csharp
string sourceFilePath = MyDir + "conic_pyramid.dxf";
using (Image image = Image.Load(sourceFilePath))
{
    //您的进一步步骤的代码将位于此处
}
```

## 第 2 步：配置光栅化选项

创建一个实例`CadRasterizationOptions`设置页面宽度、高度并指定要转换的布局。

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1200;
rasterizationOptions.PageHeight = 1200;
rasterizationOptions.Layouts = new string[] { "Model", "Layout1" };
```

## 步骤 3：为结果图像设置 TiffOptions

创建一个实例`TiffOptions`定义结果图像的格式。

```csharp
ImageOptionsBase options = new TiffOptions(TiffExpectedFormat.Default);
options.VectorRasterizationOptions = rasterizationOptions;
```

## 第 4 步：保存结果图像

指定输出路径并保存转换后的图像。

```csharp
string outputFilePath = MyDir + "conic_pyramid_layoutstorasterimage_out.tiff";
image.Save(outputFilePath, options);
```

## 结论

恭喜！您已使用 Aspose.CAD for .NET 成功将 CAD 布局转换为光栅图像格式。可能性是巨大的，本指南可以作为您进行 CAD 相关工作的起点。

## 常见问题解答

### Q1：Aspose.CAD 是否兼容所有 CAD 格式？

 A1：Aspose.CAD支持多种CAD格式，包括DWG、DXF、DWF、STL等。检查[文档](https://reference.aspose.com/cad/net/)以获得完整的列表。

### Q2：如何获得Aspose.CAD的临时许可证？

 A2：访问[临时许可证页面](https://purchase.aspose.com/temporary-license/)获得用于测试和评估目的的临时许可证。

### Q3：在哪里可以找到对 Aspose.CAD 的支持？

 A3：论坛是寻求帮助的好地方。参观[Aspose.CAD论坛](https://forum.aspose.com/c/cad/19)与社区联系并获得帮助。

### Q4：我可以免费试用Aspose.CAD吗？

A4：当然！抓住你的[免费试用](https://releases.aspose.com/)探索 Aspose.CAD 的特性和功能。

### Q5：在哪里可以购买 Aspose.CAD 的许可证？

 A5：导航至[购买页面](https://purchase.aspose.com/buy)购买许可证并释放 Aspose.CAD 的全部潜力。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
