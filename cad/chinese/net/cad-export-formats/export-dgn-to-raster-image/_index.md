---
title: 在 Aspose.CAD for .NET 中将 DGN 导出为光栅图像
linktitle: 将 DGN 导出为光栅图像
second_title: Aspose.CAD .NET - CAD 和 BIM 文件格式
description: 使用 Aspose.CAD for .NET 轻松将 DGN 转换为光栅图像。探索分步指南并释放 .NET 在 CAD 文件操作方面的强大功能。
weight: 13
url: /zh/net/cad-export-formats/export-dgn-to-raster-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 Aspose.CAD for .NET 中将 DGN 导出为光栅图像

## 介绍

在 .NET 开发的动态领域中，Aspose.CAD 成为处理计算机辅助设计 (CAD) 文件的强大工具。本教程深入介绍使用 Aspose.CAD for .NET 将 DGN 文件导出为光栅图像的过程。如果您热衷于将 DGN 文件无缝转换为视觉上引人注目的光栅图像，那么您来对地方了。

## 先决条件

在我们开始这一旅程之前，请确保您具备以下先决条件：

-  Aspose.CAD for .NET：确保您的 .NET 项目中安装了 Aspose.CAD 库。您可以在以下位置找到该库和相关文档[网站](https://reference.aspose.com/cad/net/).

- 示例 DGN 文件：准备好用于转换的 DGN 文件。在我们的示例中，我们将使用“Nikon_D90_Camera.dgn”。

现在，让我们深入了解分步指南。

## 导入命名空间

在您的 .NET 项目中，首先导入 Aspose.CAD 所需的命名空间。此步骤允许您访问 DGN 到光栅图像转换所需的类和方法。

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## 第 1 步：加载 DGN 文件

首先将 DGN 文件加载到`CadImage`目的。这为后续的操作提供了基础。

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    //您用于进一步处理的代码位于此处
}
```

## 第 2 步：定义光栅化选项

创建一个`CadRasterizationOptions`对象并设置各种属性以根据您的要求自定义光栅化过程。

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 600;
rasterizationOptions.PageHeight = 300;
rasterizationOptions.NoScaling = true;
rasterizationOptions.AutomaticLayoutsScaling = false;
```

## 第 3 步：创建 JpegOptions 对象

由于我们的目标是将 DGN 文件转换为 JPEG，因此创建一个`JpegOptions`对象并分配先前定义的`CadRasterizationOptions`到它。

```csharp
ImageOptionsBase options = new JpegOptions();
options.VectorRasterizationOptions = rasterizationOptions;
```

## 第四步：保存光栅图像

利用`Save`的方法`CadImage`类将 DGN 文件导出为所需格式的光栅图像（在本例中为 JPEG）。

```csharp
cadImage.Save(MyDir + "ExportDGNToRasterImage_out.jpg", options);
```

## 结论

恭喜！您已成功完成使用 Aspose.CAD for .NET 将 DGN 文件导出为光栅图像的步骤。本教程为您提供了轻松将此功能集成到您的 .NET 项目中的基本知识。

## 常见问题解答

### 问题 1：我可以将 DGN 文件导出为 JPEG 以外的格式吗？

A1：是的，Aspose.CAD for .NET 支持各种输出格式。您可以在步骤 3 中相应修改选项。

### Q2 转换过程中出现异常如何处理？

A2：确保您有正确的异常处理（如提供的代码中所示），以解决潜在问题。

### 问题 3：Aspose.CAD for .NET 有试用版吗？

 A3：是的，您可以通过免费试用来探索该产品。访问[这里](https://releases.aspose.com/)了解更多信息。

### 问题 4：我可以在哪里寻求帮助或讨论与 Aspose.CAD for .NET 相关的问题？

 A4：前往[Aspose.CAD论坛](https://forum.aspose.com/c/cad/19)以获得社区支持和讨论。

### 问题 5：如何获得 Aspose.CAD for .NET 的临时许可证？

 A5：参观[这个链接](https://purchase.aspose.com/temporary-license/)获取满足您的开发需求的临时许可证。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
