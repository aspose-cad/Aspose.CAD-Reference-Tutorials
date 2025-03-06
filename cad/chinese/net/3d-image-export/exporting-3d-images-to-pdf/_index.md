---
title: 将 3D 图像导出为 PDF - Aspose.CAD 教程
linktitle: 将 3D 图像导出为 PDF
second_title: Aspose.CAD .NET - CAD 和 BIM 文件格式
description: 使用 Aspose.CAD for .NET 轻松将 3D CAD 图像转换为 PDF。按照我们的分步教程进行无缝 PDF 导出。
weight: 10
url: /zh/net/3d-image-export/exporting-3d-images-to-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 将 3D 图像导出为 PDF - Aspose.CAD 教程

## 介绍

您是否希望使用 Aspose.CAD for .NET 将 3D 图像无缝导出为 PDF？本分步教程将指导您完成整个过程，确保您利用 Aspose.CAD 的强大功能轻松将 3D 图像转换为 PDF 格式。

## 先决条件

在深入学习本教程之前，请确保您具备以下先决条件：

-  Aspose.CAD for .NET：确保您已安装 Aspose.CAD for .NET 库。如果没有，您可以从以下位置下载[Aspose.CAD for .NET 下载页面](https://releases.aspose.com/cad/net/).

- 文档目录：设置存储 CAD 文件的目录，并记下路径。

## 导入命名空间

在您的 .NET 项目中，导入使用 Aspose.CAD 所需的命名空间。将以下行添加到代码文件的顶部：

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
```

## 第 1 步：加载 CAD 图像

首先加载要导出为 PDF 的 CAD 图像。使用`Load`Aspose.CAD 库中的方法。代替`"conic_pyramid.dxf"`以及 CAD 文件的路径。

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";
using (Image cadImage = Image.Load(sourceFilePath))
{
    //用于加载 CAD 图像的代码位于此处
}
```

## 第 2 步：配置光栅化选项

配置 CAD 图像的光栅化选项。设置页面宽度、页面高度和布局等参数。取消注释相关行`TypeOfEntities`如果您的实体是 3D 的。

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
// rasterizationOptions.TypeOfEntities = TypeOfEntities.Entities3D;

rasterizationOptions.Layouts = new string[] { "Model" };
```

## 步骤 3：设置 PDF 选项

创建 PDF 选项并将其与光栅化选项关联。

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## 第 4 步：另存为 PDF

使用配置的选项将 CAD 图像另存为 PDF 文件。指定 PDF 文件的输出路径。

```csharp
MyDir = MyDir + "Export3DImagestoPDF_out.pdf";
cadImage.Save(MyDir, pdfOptions);
```

## 结论

恭喜！您已使用 Aspose.CAD for .NET 成功将 3D 图像导出为 PDF。这个简单的教程可确保您轻松地将 CAD 文件转换为更易于访问的格式。

## 常见问题解答

### Q1：Aspose.CAD 是否兼容所有 CAD 文件格式？

A1：是的，Aspose.CAD 支持多种 CAD 格式，确保处理各种文件类型的灵活性。

### Q2：导出PDF时可以自定义页面尺寸吗？

A2：当然。本教程演示如何根据您的要求配置页面宽度和高度。

### 问题 3：Aspose.CAD 是否提供临时许可证？

 A3：是的，您可以通过访问获取 Aspose.CAD 的临时许可证[临时牌照](https://purchase.aspose.com/temporary-license/).

### 问题 4：我在哪里可以找到其他支持或社区讨论？

A4：前往[Aspose.CAD论坛](https://forum.aspose.com/c/cad/19)以寻求社区的支持和参与。

### Q5：Aspose.CAD 有免费试用版吗？

 A5：是的，您可以通过访问 Aspose.CAD 的功能来探索[免费试用](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
