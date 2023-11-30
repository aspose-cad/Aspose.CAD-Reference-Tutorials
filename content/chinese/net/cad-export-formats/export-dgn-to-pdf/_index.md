---
title: 在 Aspose.CAD for .NET 中将 DGN 导出为 PDF
linktitle: 将 DGN 导出为 PDF
second_title: Aspose.CAD .NET - CAD 和 BIM 文件格式
description: 了解如何使用 Aspose.CAD for .NET 将 DGN 文件轻松导出为 PDF。无缝 CAD 文件操作的分步指南。
type: docs
weight: 12
url: /zh/net/cad-export-formats/export-dgn-to-pdf/
---
## 介绍

在 .NET 开发领域，Aspose.CAD 是一个功能强大的库，可促进 CAD 文件的操作和转换。开发人员经常遇到的一项常见任务是将 DGN 文件导出为 PDF 格式。在本教程中，我们将使用 Aspose.CAD for .NET 逐步完成该过程。

## 先决条件

在深入学习本教程之前，请确保您已具备以下条件：

- C# 和 .NET 框架的应用知识。
- 安装了 Aspose.CAD for .NET 库。你可以下载它[这里](https://releases.aspose.com/cad/net/).
- 示例 DGN 文件，例如本教程的“Nikon_D90_Camera.dgn”。

## 导入命名空间

在您的 C# 项目中，首先导入必要的命名空间：

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## 第 1 步：加载 DGN 文件

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage cadImage = (DgnImage)Image.Load(sourceFilePath))
{
    //你的代码在这里...
}
```

## 第 2 步：配置光栅化选项

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 600;
rasterizationOptions.PageHeight = 300;
rasterizationOptions.NoScaling = true;
rasterizationOptions.AutomaticLayoutsScaling = false;
```

## 第 3 步：创建 PDF 选项

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## 第 4 步：另存为 PDF

```csharp
cadImage.Save(MyDir + "ExportDGNToPdf_out.pdf", pdfOptions);
```

## 结论

恭喜！您已使用 Aspose.CAD for .NET 成功将 DGN 文件导出为 PDF。本教程涵盖了从加载 DGN 文件到配置光栅化选项以及将输出保存为 PDF 的基本步骤。

## 常见问题解答

### Q1：如果没有 CAD 知识，我可以使用 Aspose.CAD for .NET 吗？

A1：当然！ Aspose.CAD 简化了复杂的 CAD 任务，使具有不同背景的开发人员都可以使用它。

### Q2：在哪里可以找到更多 Aspose.CAD 示例和文档？

 A2：探索[文档](https://reference.aspose.com/cad/net/)获取全面的指南和示例。

### Q3：Aspose.CAD 有免费试用版吗？

 A3：是的，您可以获得免费试用[这里](https://releases.aspose.com/).

### Q4：如何获得 Aspose.CAD 的临时许可证？

 A4：获取临时许可证[这里](https://purchase.aspose.com/temporary-license/).

### Q5: 需要帮助或有疑问吗？

 A5：访问[Aspose.CAD论坛](https://forum.aspose.com/c/cad/19)以获得社区支持。