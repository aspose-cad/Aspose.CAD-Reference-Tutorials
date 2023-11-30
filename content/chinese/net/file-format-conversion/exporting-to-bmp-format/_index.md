---
title: 导出为 BMP 格式 - Aspose.CAD 教程
linktitle: 导出为 BMP 格式
second_title: Aspose.CAD .NET - CAD 和 BIM 文件格式
description: 使用 Aspose.CAD for .NET 探索将 3D 图像导出为 BMP 的无缝世界。按照我们的教程获得无忧的体验。
type: docs
weight: 11
url: /zh/net/file-format-conversion/exporting-to-bmp-format/
---
## 介绍

在软件开发的动态世界中，Aspose.CAD for .NET 作为处理计算机辅助设计 (CAD) 文件的强大工具脱颖而出。如果您希望将 CAD 图像导出为广泛使用的 BMP 格式，本教程是您的首选指南。在本分步演练中，我们将探索使用 Aspose.CAD for .NET 将 3D 图像导出为 BMP 的过程。让我们深入了解吧！

## 先决条件

在开始本教程之前，请确保您具备以下先决条件：

-  Aspose.CAD for .NET：从以下位置下载并安装 Aspose.CAD 库：[这里](https://releases.aspose.com/cad/net/).
- 开发环境：搭建.NET开发环境。
- CAD 文件：准备好用于导出的 CAD 文件。在此示例中，我们将使用“18-12-11 9644 - site.dwf”。

## 导入命名空间

在您的 .NET 项目中，确保导入必要的命名空间：

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

首先将 CAD 图像加载到您的项目中。将“您的文档目录”替换为实际目录路径。

```csharp
string MyDir = "Your Document Directory";
string inputFile = MyDir + "18-12-11 9644 - site.dwf";

using (Image image = Image.Load(inputFile))
{
    //您加载图像的代码位于此处
}
```

## 步骤 2：配置 BMP 导出选项

设置 BMP 导出选项，包括 CAD 文件的矢量光栅化选项。

```csharp
BmpOptions bmpOptions = new BmpOptions();
var dwfRasterizationOptions = new CadRasterizationOptions();
bmpOptions.VectorRasterizationOptions = dwfRasterizationOptions;

dwfRasterizationOptions.PageHeight = 500;
dwfRasterizationOptions.PageWidth = 500;
```

## 第 3 步：导出为 BMP

执行导出过程，指定 BMP 文件的输出路径。

```csharp
string outPath = MyDir + "18-12-11 9644 - site.bmp";
image.Save(outPath, bmpOptions);
```

## 结论

恭喜！您已使用 Aspose.CAD for .NET 成功将 3D 图像导出为 BMP。本教程让您了解 Aspose.CAD 的多功能性，让复杂的任务变得轻而易举。

## 常见问题解答

### Q1：我可以将 Aspose.CAD for .NET 与任何 CAD 文件格式一起使用吗？

A1：是的，Aspose.CAD 支持各种 CAD 文件格式，为您的项目提供灵活性。

### Q2：临时许可证是否可用于测试目的？

 A2：当然！您可以获得临时许可证[这里](https://purchase.aspose.com/temporary-license/)进行评估。

### 问题 3：在哪里可以找到 Aspose.CAD 的综合文档？

 A3：参考文档[这里](https://reference.aspose.com/cad/net/)获取详细信息和示例。

### Q4：我如何寻求支持或与社区联系？

 A4：访问 Aspose.CAD 论坛[这里](https://forum.aspose.com/c/cad/19)提出问题并与社区互动。

### Q5：我可以购买 Aspose.CAD for .NET 吗？

 A5: 是的，您可以购买Aspose.CAD[这里](https://purchase.aspose.com/buy)为您的项目释放其全部潜力。
