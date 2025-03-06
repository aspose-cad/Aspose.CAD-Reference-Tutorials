---
title: 导出嵌入的 DGN 文件 - Aspose.CAD 教程
linktitle: 导出嵌入的 DGN 文件
second_title: Aspose.CAD .NET - CAD 和 BIM 文件格式
description: 探索 Aspose.CAD for .NET 的强大功能。通过此分步教程，学习如何轻松地将嵌入的 DGN 文件导出为 PDF。
weight: 14
url: /zh/net/export-techniques/exporting-embedded-dgn-files/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 导出嵌入的 DGN 文件 - Aspose.CAD 教程

## 介绍

在软件开发的动态世界中，Aspose.CAD for .NET 作为处理计算机辅助设计 (CAD) 文件的强大工具脱颖而出。本教程将指导您完成使用 Aspose.CAD for .NET 导出嵌入式 DGN 文件的过程。无论您是经验丰富的开发人员还是好奇的初学者，本分步指南都将帮助您有效地利用 Aspose.CAD 的功能。

## 先决条件

在深入学习本教程之前，请确保您具备以下先决条件：

1.  Aspose.CAD for .NET：从以下位置下载并安装该库[Aspose.CAD for .NET](https://releases.aspose.com/cad/net/).

2. 开发环境：使用 Visual Studio 或任何其他首选 IDE 设置 .NET 开发环境。

3. 示例 DXF 文件：在本教程中，我们将使用“conic_pyramid.dxf”文件。确保您指定的文档目录中有该文件。

## 导入命名空间

在您的 C# 代码中，确保导入必要的命名空间：

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
```

## 第 1 步：加载 DXF 文件

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    //您的进一步步骤的代码将位于此处
}
```

## 第 2 步：设置光栅化选项

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new[] { "Model" };
```

## 步骤 3：设置 PDF 选项

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## 第 4 步：另存为 PDF

```csharp
cadImage.Save(MyDir + "conic_pyramid.pdf", pdfOptions);
```

## 第5步：显示成功消息

```csharp
Console.WriteLine("\nThe DXF drawing exported successfully to PDF.\nFile saved at " + MyDir);
```

## 结论

恭喜！您已使用 Aspose.CAD for .NET 成功将嵌入的 DGN 文件导出为 PDF。本教程涵盖了基本步骤，为您探索 Aspose.CAD 提供的更高级功能奠定了基础。

## 常见问题解答

### Q1：我可以将 Aspose.CAD for .NET 与其他编程语言一起使用吗？

A1：Aspose.CAD主要支持.NET，但Aspose提供了各种语言的库，包括Java和Python。

### 问题 2：Aspose.CAD for .NET 是否有免费试用版？

 A2：是的，您可以从以下位置获得免费试用[这里](https://releases.aspose.com/).

### 问题 3：在哪里可以找到 Aspose.CAD for .NET 的综合文档？

 A3：参考文档[这里](https://reference.aspose.com/cad/net/).

### 问题 4：如何获得 Aspose.CAD for .NET 的临时许可？

 A4：获得临时许可证[这里](https://purchase.aspose.com/temporary-license/).

### Q5：需要帮助或想与社区互动？

A5：访问[Aspose.CAD论坛](https://forum.aspose.com/c/cad/19)以寻求支持和讨论。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
