---
title: 在 Aspose.CAD for .NET 中将 DGN 导出为 DWG 的一部分
linktitle: 将 DGN 导出为 DWG 的一部分
second_title: Aspose.CAD .NET - CAD 和 BIM 文件格式
description: 了解如何在 Aspose.CAD for .NET 中将 DGN 导出为 DWG 的一部分。请按照我们的分步指南进行无缝集成。
weight: 11
url: /zh/net/cad-export-formats/export-dgn-as-part-of-dwg/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 Aspose.CAD for .NET 中将 DGN 导出为 DWG 的一部分

## 介绍

在 .NET 开发领域，Aspose.CAD 作为处理计算机辅助设计 (CAD) 文件的强大库而脱颖而出。本教程将指导您完成使用 Aspose.CAD for .NET 将 DGN（设计）文件导出为 DWG（绘图）文件的一部分的过程。无论您是经验丰富的开发人员还是新手，本分步指南都将帮助您利用 Aspose.CAD 的功能高效地完成此特定任务。

## 先决条件

在深入学习本教程之前，请确保您具备以下先决条件：

-  Aspose.CAD for .NET：确保您已安装 Aspose.CAD for .NET 库。你可以下载它[这里](https://releases.aspose.com/cad/net/).

- 开发环境：设置您首选的 .NET 开发环境，例如 Visual Studio。

- C# 基础知识：熟悉 C# 编程语言。

## 导入命名空间

在您的 C# 项目中，包含访问 Aspose.CAD 功能所需的命名空间。在代码文件的开头添加以下 using 指令：

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

现在，让我们将提供的代码分解为多个步骤：

## 第 1 步：定义文件路径

```csharp
//输入和输出文件路径
string fileName = "BlockRefDgn.dwg";
string outPath = fileName + ".pdf";
```

## 第2步：创建PdfOptions实例

```csharp
//创建 PdfOptions 类的实例以将 DWG 导出为 PDF
PdfOptions exportOptions = new PdfOptions();
```

## 第 3 步：加载 DWG 文件

```csharp
//将现有 DWG 文件作为图像加载并将其转换为 CadImage 类型
using (CadImage cadImage = (CadImage)Image.Load(fileName))
```

## 第 4 步：迭代实体

```csharp
//迭代 DWG 文件中的每个实体
foreach (CadBaseEntity baseEntity in cadImage.Entities)
```

## 第 5 步：检查实体类型

```csharp
//检查实体是否是图像定义
if (baseEntity.TypeName == CadEntityTypeName.DGNUNDERLAY)
```

## 第6步：获取底层路径

```csharp
//如果是图像定义，则获取对象的外部引用
CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
Console.WriteLine(dgnFile.UnderlayPath);
```

## 第 7 步：定义光栅化选项

```csharp
//定义 CadRasterizationOptions 对象的设置
exportOptions.VectorRasterizationOptions = new CadRasterizationOptions()
{
    PageWidth = 1600,
    PageHeight = 1600,
    Layouts = new string[] { "Model" },
    AutomaticLayoutsScaling = false,
    NoScaling = true,
    BackgroundColor = Color.Black,
    DrawType = CadDrawTypeMode.UseObjectColor
};
```

## 步骤 8：将 DWG 导出为 PDF

```csharp
//通过调用 Save 方法将 DWG 导出为 PDF
cadImage.Save(outPath, exportOptions);
```

## 结论

恭喜！您已成功完成使用 Aspose.CAD for .NET 将 DGN 文件导出为 DWG 文件的一部分的过程。本教程为您提供了无缝完成此特定任务的基本步骤和代码片段。

## 常见问题解答

### Q1：我可以在我的商业项目中使用 Aspose.CAD for .NET 吗？
 A1: 是的，可以。访问[这里](https://purchase.aspose.com/buy)探索许可选项。

### 问题 2：我可以处理的 DWG 文件的大小有限制吗？
A2：Aspose.CAD 支持处理大型 DWG 文件，但可能存在硬件限制。

### Q3：有试用版吗？
A3：是的，您可以获得免费试用[这里](https://releases.aspose.com/).

### Q4：如何获得临时许可证？
 A4：可以获得临时许可证[这里](https://purchase.aspose.com/temporary-license/).

### Q5：如果遇到问题，我可以到哪里寻求帮助？
 A5：您可以访问Aspose.CAD论坛[这里](https://forum.aspose.com/c/cad/19)为了支持。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
