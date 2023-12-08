---
title: Aspose.CAD for .NET 中对 DGN V7 的 3D 支持
linktitle: DGN V7 支持 3D
second_title: Aspose.CAD .NET - CAD 和 BIM 文件格式
description: 释放 Aspose.CAD for .NET 中对 DGN V7 的 3D 支持的强大功能。请按照我们的分步教程进行操作。
type: docs
weight: 20
url: /zh/net/cad-features-and-support/support-of-3d-for-dgn-v7/
---
## 介绍

欢迎来到我们关于在 Aspose.CAD for .NET 中利用 3D for DGN V7 支持的综合教程！ Aspose.CAD 是一个功能强大的库，使开发人员能够在其 .NET 应用程序中无缝地使用 CAD 文件。在本教程中，我们将探讨利用 DGN V7 的 3D 支持的步骤，为您提供增强 CAD 相关项目的知识。

## 先决条件

在深入学习本教程之前，请确保您具备以下先决条件：

-  Aspose.CAD for .NET：确保您已安装 Aspose.CAD for .NET。如果没有，您可以从以下位置下载[这里](https://releases.aspose.com/cad/net/).

- 开发环境：为.NET应用程序开发设置合适的开发环境，例如Visual Studio。

- 示例 DGN 文件：准备好示例 DGN 文件以供测试。您可以使用提供的示例文件“Nikon_D90_Camera.dgn”。

现在，让我们开始使用 Aspose.CAD for .NET 实现对 DGN V7 的 3D 支持的步骤！

## 导入命名空间

在您的 .NET 应用程序中，首先导入必要的命名空间：

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

## 第 1 步：设置您的文档目录

确保您的项目中设置了文档目录。代替`"Your Document Directory"`与文档目录的实际路径。

```csharp
string MyDir = "Your Document Directory";
```

## 步骤 2：加载 DGN 文件

使用以下代码将现有 DGN 文件加载为 CadImage：

```csharp
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";
string outFile = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    //您用于进一步处理的代码位于此处
}
```

## 步骤 3：配置 PDF 导出选项

设置导出为 PDF 的选项，指定矢量光栅化选项，例如页面尺寸、自动布局缩放、背景颜色和要导出的布局。

```csharp
var options = new PdfOptions
{
    VectorRasterizationOptions = new CadRasterizationOptions
    {
        PageWidth = 1500,
        PageHeight = 1500,
        AutomaticLayoutsScaling = true,
        BackgroundColor = Color.Black,
        Layouts = new string[] { "1", "2", "3", "9" } //仅导出指定视图
    }
};
```

## 第四步：保存光栅图像

使用配置的选项将 DGN 文件另存为光栅图像。

```csharp
dgnImage.Save(outFile, options);
```

## 结论

恭喜！您已成功利用 Aspose.CAD for .NET 将支持 3D 的 DGN 文件导出为光栅图像。本教程为您提供了将此功能集成到 CAD 项目中的基本步骤。

## 常见问题解答

### Q1：我可以将 Aspose.CAD for .NET 与其他 CAD 文件格式一起使用吗？

A1：是的，Aspose.CAD支持各种CAD文件格式，包括DWG和DXF。

### Q2：使用Aspose.CAD时如何处理异常？

A2：将代码包装在 try-catch 块中，如提供的示例所示，以优雅地处理异常。

### Q3：Aspose.CAD适合商业项目吗？

 A3：当然！您可以购买 Aspose.CAD for .NET[这里](https://purchase.aspose.com/buy).

### Q4：我可以在购买前试用 Aspose.CAD for .NET 吗？

A4：当然！探索免费试用[这里](https://releases.aspose.com/).

### 问题 5：在哪里可以找到 Aspose.CAD for .NET 的社区支持？

 A5：访问社区论坛[这里](https://forum.aspose.com/c/cad/19).