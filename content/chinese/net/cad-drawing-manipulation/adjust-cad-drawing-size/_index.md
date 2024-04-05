---
title: 在 Aspose.CAD for .NET 中调整 CAD 绘图尺寸
linktitle: 调整 CAD 绘图尺寸
second_title: Aspose.CAD .NET - CAD 和 BIM 文件格式
description: 了解如何使用 Aspose.CAD 在 .NET 中轻松调整 CAD 绘图尺寸。请按照我们的分步指南进行无缝调整大小。
type: docs
weight: 10
url: /zh/net/cad-drawing-manipulation/adjust-cad-drawing-size/
---
## 介绍

您是否希望在 .NET 应用程序中无缝调整 CAD 绘图的尺寸？ Aspose.CAD for .NET 提供了强大的解决方案，使您可以轻松处理 CAD 绘图大小调整。在本教程中，我们将指导您完成整个过程，分解每个步骤，以确保您掌握使用 Aspose.CAD 调整 CAD 绘图大小的复杂性。

## 先决条件

在我们深入学习本教程之前，请确保您具备以下先决条件：

- Aspose.CAD for .NET 库：从以下位置下载并安装该库：[Aspose.CAD for .NET 下载页面](https://releases.aspose.com/cad/net/).
- 示例 CAD 绘图：确保文档目录中有示例 CAD 绘图文件（例如“sample.dwg”）。

## 导入命名空间

首先将必要的命名空间导入到您的 .NET 应用程序中。此步骤对于访问 Aspose.CAD for .NET 提供的功能至关重要。

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## 第 1 步：加载 CAD 图纸

首先将 CAD 绘图加载到 Aspose.CAD.Image 类的实例中。确保您的示例绘图具有正确的文件路径。

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "sample.dwg";

//在 Image 实例中加载 CAD 绘图
using (var image = Aspose.CAD.Image.Load(sourceFilePath))
{
    //你的代码在这里...
}
```

## 第2步：创建BmpOptions

创建 BmpOptions 类的实例，该类负责在将 CAD 图形保存为 BMP 文件时指定选项。

```csharp
Aspose.CAD.ImageOptions.BmpOptions bmpOptions = new Aspose.CAD.ImageOptions.BmpOptions();
```

## 步骤 3：设置 CadRasterizationOptions

实例化 CadRasterizationOptions 类并配置其属性以进行矢量光栅化。

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions cadRasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
bmpOptions.VectorRasterizationOptions = cadRasterizationOptions;
```

## 步骤 4：设置 UnitType 属性

设置 CadRasterizationOptions 的 UnitType 属性以指定调整大小的单位类型。在此示例中，它设置为厘米。

```csharp
cadRasterizationOptions.UnitType = Aspose.CAD.ImageOptions.UnitType.Centimeter;
```

## 第5步：设置布局属性

通过设置 Layouts 属性来指定要包含在调整大小的绘图中的布局。

```csharp
cadRasterizationOptions.Layouts = new string[] { "Model" };
```

## 第 6 步：导出为 BMP

最后，使用 Save 方法将调整大小的布局保存为 BMP 文件。

```csharp
string outPath = sourceFilePath + ".bmp";
image.Save(outPath, bmpOptions);
```

现在您已经使用 Aspose.CAD for .NET 成功调整了 CAD 绘图的尺寸！

## 结论

在本教程中，我们演示了使用 Aspose.CAD 在 .NET 中调整 CAD 绘图大小的过程。通过执行以下步骤，您可以将此功能无缝集成到您的应用程序中，从而提供流畅的用户体验。

## 常见问题解答

### Q1：Aspose.CAD for .NET 是否与所有 CAD 格式兼容？

 A1：Aspose.CAD for .NET 支持多种 CAD 格式，包括 DWG、DXF、DWF 等。检查[文档](https://reference.aspose.com/cad/net/)获取完整列表。

### Q2：我可以同时调整多个布局的大小吗？

A2：是的，您可以通过调整 CadRasterizationOptions 中的布局数组来调整多个布局的大小。

### 问题 3：在哪里可以获得 Aspose.CAD for .NET 的支持？

 A3：访问[Aspose.CAD论坛](https://forum.aspose.com/c/cad/19)以获得社区的支持和帮助。

### Q4：有免费试用吗？

 A4：是的，您可以探索[免费试用](https://releases.aspose.com/)评估 Aspose.CAD for .NET 的功能。

### 问题 5：如何获得 Aspose.CAD for .NET 的临时许可证？

 A5：获取用于测试目的的临时许可证[这里](https://purchase.aspose.com/temporary-license/).