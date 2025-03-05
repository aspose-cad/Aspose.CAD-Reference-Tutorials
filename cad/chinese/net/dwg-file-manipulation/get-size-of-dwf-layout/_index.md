---
title: 在 C# 中处理 DWG 文件 - 获取 DWF 布局的大小
linktitle: 在 C# 中处理 DWG 文件 - 获取 DWF 布局的大小
second_title: Aspose.CAD .NET - CAD 和 BIM 文件格式
description: 探索 Aspose.CAD for .NET 在处理 DWG 文件方面的强大功能。了解使用 C# 轻松提取 DWF 布局尺寸。
type: docs
weight: 10
url: /zh/net/dwg-file-manipulation/get-size-of-dwf-layout/
---
## 介绍

在计算机辅助设计 (CAD) 和 .NET 开发领域，Aspose.CAD 是处理 DWG 文件的强大工具。本教程将指导您完成在 C# 中处理 DWG 文件并提取 DWF 布局大小的过程。在我们深入研究代码之前，让我们确保您已做好开始此旅程的一切准备。

## 先决条件

要无缝地遵循本教程，请确保您具备以下先决条件：

-  Aspose.CAD for .NET：确保您已安装 Aspose.CAD for .NET。您可以从[Aspose.CAD for .NET 下载页面](https://releases.aspose.com/cad/net/).

现在您已经拥有了必要的工具，让我们进入编码领域。

## 导入命名空间

在开始使用代码之前，让我们导入所需的命名空间：

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Dwf;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

这些命名空间将提供在 C# 应用程序中使用 Aspose.CAD 处理 CAD 文件的基本类和方法。

## 第 1 步：设置您的环境

首先确保您为您的项目设置了正确的环境。在 C# 项目中引用 Aspose.CAD 库。

## 第 2 步：定义文件路径

定义 DWG 文件的路径以及生成的 JPG 文件的输出目录：

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "blocks_and_tables.dwf";
```

## 步骤 3：加载 DWF 图像

使用 Aspose.CAD 加载 DWF 图像：

```csharp
using (DwfImage image = (DwfImage)Aspose.CAD.Image.Load(sourceFilePath))
{
    //进一步步骤的代码将在此处
}
```

## 第 4 步：遍历页面

遍历 DWF 图像的页面：

```csharp
foreach (var page in image.Pages)
{
    //进一步步骤的代码将在此处
}
```

## 第5步：获取布局信息

获取每个页面的布局信息：

```csharp
var layout = page.Name;
System.Console.WriteLine("Layout= " + layout);
```

## 第 6 步：设置 JPG 选项

设置将布局保存为 JPG 文件的选项：

```csharp
using (FileStream fs = new FileStream(MyDir + "layout_" + layout + ".jpg", FileMode.Create))
{
    JpegOptions jpegOptions = new JpegOptions();
    CadRasterizationOptions options = new CadRasterizationOptions();
    options.Layouts = new string[] { layout };
    //进一步步骤的代码将在此处
}
```

## 第 7 步：确定页面大小

确定 DWF 布局的尺寸：

```csharp
double sizeExtX = page.MaxPoint.X - page.MinPoint.X;
double sizeExtY = page.MaxPoint.Y - page.MinPoint.Y;
//进一步步骤的代码将在此处
```

## 第 8 步：设置页面尺寸

根据单位类型设置页面尺寸：

```csharp
if (page.UnitType == UnitType.Inch)
{
    options.PageHeight = CommonHelper.INtoPixels(sizeExtY, CommonHelper.DPI);
    options.PageWidth = CommonHelper.INtoPixels(sizeExtX, CommonHelper.DPI);
}
else if (page.UnitType == UnitType.Millimeter)
{
    options.PageHeight = CommonHelper.MMtoPixels(sizeExtY, CommonHelper.DPI);
    options.PageWidth = CommonHelper.MMtoPixels(sizeExtX, CommonHelper.DPI);
}
else
{
    options.PageHeight = (float)sizeExtY;
    options.PageWidth = (float)sizeExtX;
}
```

## 第9步：保存JPG文件

使用指定选项保存 JPG 文件：

```csharp
jpegOptions.VectorRasterizationOptions = options;
image.Save(fs, jpegOptions);
}
```

现在，您已使用 C# 中的 Aspose.CAD 成功从 DWG 文件中提取了 DWF 布局的尺寸。请随意探索 Aspose.CAD 为 .NET 开发提供的更多特性和功能。

## 结论

在本教程中，我们演练了使用 Aspose.CAD 在 C# 中处理 DWG 文件的过程。通过执行这些步骤，您不仅可以获得 DWF 布局的大小，还可以利用 Aspose.CAD 的功能来执行 .NET 项目中的各种 CAD 相关任务。

## 常见问题解答

### Q1：Aspose.CAD 与最新的 DWG 文件格式兼容吗？

 A1：Aspose.CAD支持各种DWG文件格式，包括最新版本。请参阅[文档](https://reference.aspose.com/cad/net/)有关特定兼容性详细信息。

### Q2：我可以将 Aspose.CAD 用于商业和个人项目吗？

 A2：是的，Aspose.CAD 为商业和个人用途提供灵活的许可选项。参观[购买页面](https://purchase.aspose.com/buy)更多细节。

### Q3：如何获得 Aspose.CAD 的临时许可证？

A3：您可以从以下地点获得临时许可证：[这里](https://purchase.aspose.com/temporary-license/)出于评估目的。

### Q4：在哪里可以找到对 Aspose.CAD 的支持？

A4：如有任何疑问或帮助，请访问[Aspose.CAD论坛](https://forum.aspose.com/c/cad/19).

### Q5：Aspose.CAD 有免费试用版吗？

A5：是的，您可以访问 Aspose.CAD 的免费试用版[这里](https://releases.aspose.com/).