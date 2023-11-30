---
title: Aspose.CAD for .NET 支持 DGN V7
linktitle: 支持 DGN V7
second_title: Aspose.CAD .NET - CAD 和 BIM 文件格式
description: 探索 Aspose.CAD for .NET 对 DGN V7 的无缝支持。通过分步指导，轻松将 DGN 文件转换为光栅图像。
type: docs
weight: 19
url: /zh/net/cad-features-and-support/support-for-dgn-v7/
---
## 介绍

在 .NET 开发领域，Aspose.CAD 作为处理计算机辅助设计 (CAD) 文件的强大库脱颖而出。本教程深入探讨 Aspose.CAD for .NET 的特定功能 — 对 DGN V7 文件的支持。 DGN 是 Design 的缩写，是 CAD 领域广泛使用的文件格式。 Aspose.CAD 简化了使用 DGN V7 文件的过程，为开发人员提供无缝体验。

## 先决条件

在我们深入实施之前，请确保您具备以下先决条件：

-  Aspose.CAD for .NET：确保您已安装 Aspose.CAD 库。您可以从[网站](https://releases.aspose.com/cad/net/).

- 开发环境：设置有效的 .NET 开发环境，包括 Visual Studio 或任何其他首选 IDE。

现在我们已经满足了先决条件，让我们探讨如何利用 Aspose.CAD for .NET 中对 DGN V7 的支持。

## 导入命名空间

首先导入必要的命名空间以访问 Aspose.CAD 的功能：

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## 第 1 步：加载 DGN 文件

首先加载现有的 DGN 文件作为`CadImage`。代替`"Your Document Directory"`和`"Nikon_D90_Camera.dgn"`具有适当的目录路径和文件名。

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    //进一步步骤的代码位于此处...
}
```

## 第 2 步：配置光栅化选项

创建一个`CadRasterizationOptions`对象来定义和设置与光栅化相关的各种属性。

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions
{
    PageWidth = 600,
    PageHeight = 300,
    NoScaling = true,
    AutomaticLayoutsScaling = false
};
```

## 步骤 3：设置矢量光栅化选项

创建一个`JpegOptions`对象，因为我们打算将 DGN 文件转换为 JPEG。分配之前创建的`CadRasterizationOptions`反对它。

```csharp
ImageOptionsBase options = new JpegOptions
{
    VectorRasterizationOptions = rasterizationOptions
};
```

## 步骤 4：保存光栅化图像

致电`Save`的方法`CadImage`类对象将 DGN 文件导出为光栅图像（在本例中为 JPEG）。

```csharp
cadImage.Save(MyDir + "ExportDGNToRasterImage_out.jpeg", options);
```

完成这些步骤后，DGN 文件已成功导出为光栅图像。

## 结论

在本教程中，我们探索了 Aspose.CAD for .NET 中对 DGN V7 的无缝支持。通过遵循分步指南，开发人员可以轻松地将 DGN 文件转换为光栅图像，从而扩展其 .NET 应用程序的功能。

## 常见问题解答

### Q1：Aspose.CAD 是否兼容最新的 DGN V7 规范？

A1：是的，Aspose.CAD 旨在无缝处理 DGN V7 文件，确保与最新规范的兼容性。

### 问题 2：我可以自定义 DGN 文件转换的光栅化选项吗？

 A2：当然。本教程演示了如何创建和配置`CadRasterizationOptions`定制转换过程。

### Q3：除了JPEG之外，还有其他支持的输出格式吗？

A3：是的，Aspose.CAD支持各种输出格式。您可以浏览文档以获得完整的列表。

### Q4：如何获得 Aspose.CAD 相关查询的支持？

 A4：访问[Aspose.CAD论坛](https://forum.aspose.com/c/cad/19)以获得社区支持和讨论。

### 问题 5：Aspose.CAD for .NET 是否有免费试用版？

 A5：是的，您可以免费试用[这里](https://releases.aspose.com/).