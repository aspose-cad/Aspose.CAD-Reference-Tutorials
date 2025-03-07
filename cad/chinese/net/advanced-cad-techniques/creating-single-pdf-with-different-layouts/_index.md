---
title: 创建具有不同布局的单个 PDF - Aspose.CAD 指南
linktitle: 创建具有不同布局的单个 PDF
second_title: Aspose.CAD .NET - CAD 和 BIM 文件格式
description: 使用 Aspose.CAD for .NET 创建具有不同布局的单个 PDF。按照我们的分步指南进行无缝集成和高效 PDF 生成。
weight: 13
url: /zh/net/advanced-cad-techniques/creating-single-pdf-with-different-layouts/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 创建具有不同布局的单个 PDF - Aspose.CAD 指南

## 介绍

您是否希望使用 Aspose.CAD for .NET 从具有不同布局的 CAD 绘图生成单个 PDF 文档？本分步指南将引导您完成整个过程，帮助您实现无缝集成和高效的 PDF 创建。 Aspose.CAD for .NET 提供了强大的功能来以编程方式操作 CAD 绘图，在本教程中，我们将重点关注创建具有不同布局的单个 PDF。

## 先决条件

在深入学习本教程之前，请确保您具备以下先决条件：

-  Aspose.CAD for .NET：确保您已安装 Aspose.CAD for .NET。您可以从以下位置下载：[这里](https://releases.aspose.com/cad/net/).

- 开发环境：搭建.NET开发环境，对C#编程有基本了解。

## 导入命名空间

在您的 C# 项目中，包含必要的命名空间以利用 Aspose.CAD for .NET 的功能：

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## 第 1 步：加载 CAD 图像

```csharp
//文档目录的路径。
string MyDir = "Your Document Directory";

using (CadImage cadImage = (CadImage)Image.Load(MyDir + "City skyway map.dwg"))
{
    //第 1 步的代码位于此处
}
```

## 第 2 步：自定义光栅化选项

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1000;
rasterizationOptions.PageHeight = 1000;

//多种布局的自定义尺寸
rasterizationOptions.LayoutPageSizes.Add("ANSI C Plot", new SizeF(500, 1000));
rasterizationOptions.LayoutPageSizes.Add("8.5 x 11 Plot", new SizeF(1000, 100));
```

## 第 3 步：定义 PDF 选项

```csharp
PdfOptions pdfOptions = new PdfOptions() { VectorRasterizationOptions = rasterizationOptions };
```

## 第 4 步：另存为 PDF

```csharp
cadImage.Save(MyDir + "singlePDF_out.pdf", pdfOptions);
```

现在您已经使用 Aspose.CAD for .NET 成功创建了具有不同布局的单个 PDF 文档。请随意探索更多功能并根据您的具体要求自定义代码。

## 结论

在本教程中，我们介绍了使用 Aspose.CAD for .NET 从具有不同布局的 CAD 绘图创建单个 PDF 的过程。这个功能强大的库简化了 CAD 操作任务，并为各种场景提供了灵活性。

## 常见问题解答

### Q1：我可以将 Aspose.CAD for .NET 与其他 CAD 格式一起使用吗？

A1：是的，Aspose.CAD for .NET 支持各种 CAD 格式，例如 DWG、DXF、DGN 等。

### Q2: 有免费试用吗？

 A2：是的，您可以探索免费试用[这里](https://releases.aspose.com/).

### 问题 3：如何获得 Aspose.CAD for .NET 支持？

 A3：访问[Aspose.CAD论坛](https://forum.aspose.com/c/cad/19)以获得社区支持。

### Q4：哪里可以找到详细的文档？

A4：参考文档[这里](https://reference.aspose.com/cad/net/).

### Q5：我可以购买 Aspose.CAD for .NET 的许可证吗？

 A5：是的，您可以购买许可证[这里](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
