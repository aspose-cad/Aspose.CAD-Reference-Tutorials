---
title: 在 Aspose.CAD for .NET 中获取 CAD 布局的大小
linktitle: 获取 CAD 布局的尺寸
second_title: Aspose.CAD .NET - CAD 和 BIM 文件格式
description: 了解如何使用 Aspose.CAD 在 .NET 中检索 CAD 布局尺寸。请按照我们的分步指南进行高效的 CAD 文件操作。
type: docs
weight: 14
url: /zh/net/cad-drawing-manipulation/get-size-of-cad-layout/
---
## 介绍

欢迎阅读这份有关使用 Aspose.CAD for .NET 获取 CAD 布局尺寸的综合指南。 Aspose.CAD 是一个功能强大的库，使开发人员能够无缝地使用 CAD 文件。在本教程中，我们将使用实际示例和分步说明引导您完成检索 CAD 布局尺寸的过程。

## 先决条件

在我们深入学习本教程之前，请确保您具备以下先决条件：

-  Aspose.CAD for .NET：确保您已安装 Aspose.CAD 库。您可以从[Aspose.CAD for .NET 下载页面](https://releases.aspose.com/cad/net/).

- 文档文件：准备您要使用的 CAD 文件。本教程使用“conic_pyramid.dxf”和“Bottom_plate.dwg”作为示例。

现在，让我们开始吧！

## 导入命名空间

在您的 .NET 项目中，首先导入必要的命名空间：

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

## 第 1 步：设置文档目录

设置文档目录的路径。代替`"Your Document Directory"`与实际路径。

```csharp
string MyDir = "Your Document Directory";
```

## 步骤 2：指定 CAD 文件路径

定义要分析的 CAD 文件路径数组。在此示例中，我们使用“conic_pyramid.dxf”和“Bottom_plate.dwg”。

```csharp
string[] sourceFilePaths = new[]
{
    MyDir + "conic_pyramid.dxf",
    MyDir + "Bottom_plate.dwg"
};
```

## 第 3 步：迭代 CAD 文件

迭代每个 CAD 文件并检索布局信息。

```csharp
foreach (var sourceFilePath in sourceFilePaths)
{
    string extension = Path.GetExtension(sourceFilePath);
    using (CadImage cadImage = (CadImage)Aspose.CAD.Image.Load(sourceFilePath))
    {
        // ...（继续下一步）
    }
}
```

## 第 4 步：获取非空布局

定义一个辅助方法以根据 CAD 文件类型获取非空布局。

```csharp
private static List<string> GetNotEmptyLayouts(Image cadImage, string extension)
{
    // ...（继续下一步）
}
```

## 步骤 5：获取 DWG 文件的布局

实现逻辑以检索 DWG 文件的非空布局。

```csharp
private static List<string> GetNotEmptyLayoutsForDwg(CadImage cadImage)
{
    // ...（继续下一步）
}
```

## 第 6 步：获取 DXF 文件的布局

实现逻辑以检索 DXF 文件的非空布局。

```csharp
private static List<string> GetNotEmptyLayoutsForDxf(CadImage cadImage)
{
    // ...（继续下一步）
}
```

## 第 7 步：检索布局尺寸并另存为图像

完成获取布局尺寸并将其保存为图像的过程。

```csharp
foreach (string layout in layouts)
{
    // ...（继续下一步）
}
```

## 结论

恭喜！您已经成功学习了如何使用 Aspose.CAD for .NET 获取 CAD 布局的大小。本教程涵盖了从设置项目到检索布局信息并将其另存为图像的基本步骤。现在，您可以将这些知识合并到您的 .NET 应用程序中，以实现高效的 CAD 文件操作。

## 常见问题解答

### Q1：Aspose.CAD 是否兼容所有 CAD 文件格式？

A1：是的，Aspose.CAD支持各种CAD文件格式，包括DWG和DXF。

### Q2：我可以自定义图像保存选项吗？

A2：当然！您可以调整图像选项，例如格式和分辨率，以满足您的特定要求。

### Q3：在哪里可以找到其他文档？

 A3：请参阅[Aspose.CAD 文档](https://reference.aspose.com/cad/net/)获取详细信息和示例。

### Q4：有免费试用吗？

A4：是的，您可以使用[免费试用](https://releases.aspose.com/).

### Q5；我如何获得技术支持？

 A5：如需技术支持，请访问[Aspose.CAD论坛](https://forum.aspose.com/c/cad/19).