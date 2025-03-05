---
title: Aspose.CAD for .NET 支持的 DGN 元素
linktitle: 支持的 DGN 元素
second_title: Aspose.CAD .NET - CAD 和 BIM 文件格式
description: 探索 Aspose.CAD for .NET 处理 DGN 文件的强大功能。按照我们的分步指南无缝处理 2D 和 3D 元素。
type: docs
weight: 18
url: /zh/net/cad-features-and-support/supported-dgn-elements/
---
## 介绍

您是一位希望无缝使用 DGN 文件的 .NET 开发人员吗？ Aspose.CAD for .NET 提供了一个强大的解决方案来高效处理 DGN 文件。在本教程中，我们将深入研究支持的 DGN 元素，指导您完成使用 Aspose.CAD for .NET 的过程。

## 先决条件

在我们开始之前，请确保您具备以下条件：

- .NET 编程的基础知识。
- Visual Studio 安装在您的计算机上。
-  Aspose.CAD for .NET 库，您可以下载[这里](https://releases.aspose.com/cad/net/).

## 导入命名空间

要启动您的项目，请将必要的命名空间导入到您的 .NET 应用程序中。此步骤确保您可以访问 Aspose.CAD for .NET 提供的功能。

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Dgn;
using Aspose.CAD.FileFormats.Dgn.DgnElements;
```

## 步骤 1：加载 DGN 文件

首先将现有 DGN 文件作为 CadImage 加载到 .NET 应用程序中。

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    //你的代码在这里
}
```

## 步骤 2：迭代 DGN 元素

使用 foreach 循环迭代 DGN 元素。 Aspose.CAD for .NET 提供了多种可供您使用的 DGN 元素类型。

```csharp
foreach (DgnDrawingElementBase element in dgnImage.Elements)
{
    //你的代码在这里
}
```

## 第 3 步：处理先前支持的实体

处理以前支持的 2D 实体，现在也支持 3D。

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.Line:
    case DgnElementType.Ellipse:
    case DgnElementType.Curve:
    //其他案例
        {
            //你的代码在这里
            break;
        }
}
```

## 第 4 步：处理支持的 3D 实体

处理 Aspose.CAD for .NET 提供的受支持的 3D 实体。

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.SolidHeader3D:
    case DgnElementType.Cone:
    case DgnElementType.CellHeader:
        {
            //你的代码在这里
            break;
        }
}
```

## 第5步：导出并保存

最后将修改后的DGN文件导出为光栅图像并保存到指定目录。

```csharp
Console.WriteLine("\nThe DGN file exported successfully to raster image.\nFile saved at " + MyDir);
```

## 结论

在本教程中，我们探讨了 Aspose.CAD for .NET 在处理和操作 DGN 文件方面的功能。通过遵循分步指南，您可以高效地使用支持的 DGN 元素，无论它们是 2D 还是 3D 实体。 Aspose.CAD for .NET 使您能够将 DGN 文件处理无缝集成到您的 .NET 应用程序中。

## 常见问题解答

### Q1：在哪里可以找到 Aspose.CAD for .NET 的文档？

 A1：你可以找到文档[这里](https://reference.aspose.com/cad/net/).

### 问题 2：如何下载 Aspose.CAD for .NET？

 A2：您可以下载该库[这里](https://releases.aspose.com/cad/net/).

### 问题 3：Aspose.CAD for .NET 是否有免费试用版？

A3：是的，您可以免费试用[这里](https://releases.aspose.com/).

### 问题 4：在哪里可以获得 Aspose.CAD for .NET 的临时许可证？

 A4：可以使用临时许可证[这里](https://purchase.aspose.com/temporary-license/).

### Q5: 需要帮助或有疑问吗？

A5：访问 Aspose.CAD for .NET 社区[支持论坛](https://forum.aspose.com/c/cad/19).