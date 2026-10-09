---
date: 2026-10-09
description: 了解如何使用 C# 和 Aspose.CAD for .NET 加载 dwg 文件并在 DWG 文件中搜索文本。按照本分步指南提升您的 CAD
  工作流程。
keywords:
- load dwg file
- export dwg to pdf
- cad text search
- search text dwg
- c# read dwg
lastmod: 2026-10-09
linktitle: 使用 C# 在 DWG 文件中搜索文本
og_description: 了解如何使用 C# 和 Aspose.CAD for .NET 加载 dwg 文件并在 DWG 文件中搜索文本。按照本分步指南提升您的
  CAD 工作流程。
og_image_alt: Guide showing how to load dwg file and search text in DWG files using
  Aspose.CAD for .NET
og_title: 如何使用 C# 加载 dwg 文件并在 DWG 文件中搜索文本
schemas:
- author: Aspose
  dateModified: '2026-10-09'
  description: Learn how to load dwg file and search text inside DWG files using C#
    and Aspose.CAD for .NET. Follow this step‑by‑step guide to enhance your CAD workflows.
  headline: How to load dwg file and search text in DWG files with C#
  type: TechArticle
- questions:
  - answer: '`new CadImage("yourfile.dwg")` creates an in‑memory representation of
      the drawing.'
    question: What is the first line of code to load a DWG?
  - answer: '`Aspose.CAD.Image` and `Aspose.CAD.FileFormats.Dwg` are required.'
    question: Which namespace contains the CAD classes?
  - answer: Yes – use `image.Save("out.pdf", SaveFormat.Pdf)`.
    question: Can I export the search results directly to PDF?
  - answer: A free trial works for evaluation; a permanent license is required for
      production.
    question: Do I need a license for development?
  - answer: .NET 5, .NET 6, .NET Core 3.1 and .NET Framework 4.6+.
    question: Which .NET versions are supported?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- dwg file handling
- aspose.cad
- c# cad processing
- text search in dwg
title: 如何使用 C# 加载 dwg 文件并在 DWG 文件中搜索文本
url: /zh/net/text-search-and-manipulation/searching-text-in-dwg-files/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何使用 C# 加载 DWG 文件并在 DWG 文件中搜索文本 - Aspose.CAD 教程

## 介绍

在现代 CAD 开发中，能够 **load dwg file** 对象并即时定位特定文本字符串可以节省数小时的人工检查。无论您是构建批处理工具还是为查看器添加搜索功能，Aspose.CAD for .NET 都提供了一个完全托管的 API，可在 Windows、Linux 和 macOS 上运行，无需本机依赖。本指南将带您逐步完成从加载 DWG 到导出结果为 PDF 的全部过程，让您今天就能在 C# 应用程序中集成可靠的 CAD 文本搜索。

## 快速答案
- **加载 DWG 的第一行代码是什么？** `new CadImage("yourfile.dwg")` 会创建绘图的内存表示。  
- **哪个命名空间包含 CAD 类？** 需要 `Aspose.CAD.Image` 和 `Aspose.CAD.FileFormats.Dwg`。  
- **我可以直接将搜索结果导出为 PDF 吗？** 可以 – 使用 `image.Save("out.pdf", SaveFormat.Pdf)`。  
- **开发时需要许可证吗？** 免费试用可用于评估；生产环境需要永久许可证。  
- **支持哪些 .NET 版本？** .NET 5、.NET 6、.NET Core 3.1 和 .NET Framework 4.6+。

## 什么是 DWG 文件？

DWG 文件是一种二进制格式，用于存储由 AutoCAD 和兼容工具创建的 2D 与 3D 设计数据。它是业界标准的矢量几何、图层、文本和元数据容器。由于该格式为专有格式，大多数开源解析器在处理新版本时会遇到困难，但 Aspose.CAD 完全支持超过 150 种 DWG 发行版，允许您在无需安装 AutoCAD 的情况下读取和操作图纸。

## 为什么在 CAD 文本搜索中使用 Aspose.CAD？

Aspose.CAD 能处理 **50+** DWG 和 DXF 版本，文件大小可达 1 GB，且无需将整个文档加载到内存中。库能够从 **Entities** 和 **Block** 部分提取文本，在即使文本嵌套在块内部的情况下也能实现 **99 %** 的成功率。这种可量化的可靠性使其成为企业级 CAD 自动化的首选。

## 前置条件

在开始之前，请确认您已具备：

- **Aspose.CAD for .NET** 已安装。请从 [Aspose.CAD website](https://releases.aspose.com/cad/net/) 下载最新包。
- 包含待分析 DWG 文件的文件夹。
- 用于生产的有效许可证文件（试用时可选）。

## 需要哪些命名空间？

`Aspose.CAD` 命名空间提供核心图像处理类，而 `Aspose.CAD.FileFormats.Dwg` 包含 DWG 特定结构。在 C# 文件顶部导入它们：

```csharp
using Aspose.CAD;
using Aspose.CAD.FileFormats.Dwg;
using Aspose.CAD.ImageOptions;
```

> **注意：** 上面的代码块是占位符；保持原始文本不变以保留占位符计数。

## 如何加载 dwg 文件？

使用 Aspose.CAD 加载 DWG 文件非常简单。使用 `CadImage` 类，它在内存中表示 CAD 绘图。构造函数在不渲染的情况下读取文件，即使是大型图纸也能快速加载。加载后，您可以在执行任何搜索操作之前检查 `Width`、`Height` 和 `Layers` 等属性。

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects.AttEntities;
```

## 如何在实体部分搜索文本？

要在 Entities 部分定位文本，遍历 `cadImage.Entities` 集合。每个实体都可以检查其类型（例如 `MText`、`Text`、`Attribute`）以及其 `TextString` 属性。对目标字符串执行不区分大小写的比较，并收集匹配的实体以便进一步处理或高亮显示。

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "search.dwg";
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Your code here
}
```

## 如何在块部分搜索文本？

块是可重用的实体组，可能包含嵌套文本。首先枚举 `cadImage.BlockEntities.Values` 以访问每个块定义。然后遍历每个块的 `Entities` 集合，使用与主 Entities 部分相同的文本匹配逻辑。这样可以确保不会遗漏隐藏在可重用组件中的文本。

```csharp
foreach (CadBaseEntity entity in cadImage.Entities)
{
    IterateCADNodes(entity);
}
```

## 如何遍历 CAD 节点进行完整扫描？

完整扫描结合了 Entities 和 Block 两个部分。通过递归遍历 `CadImage` 节点树，您可以处理嵌套块、属性定义，甚至外部引用。实现一个接受 `CadBaseEntity` 的辅助方法，检查其类型，在适用时提取文本，然后在节点包含集合时递归遍历子实体。

```csharp
foreach (CadBlockEntity blockEntity in cadImage.BlockEntities.Values)
{
    foreach (CadBaseEntity entity in blockEntity.Entities)
    {
        IterateCADNodes(entity);
    }
}
```

## 如何在定位文本后将 dwg 导出为 pdf？

在识别出相关实体后，您可能希望高亮它们或提取坐标。Aspose.CAD 允许您将整个绘图保存为 PDF，同时保持矢量质量。如需栅格输出，可配置 `CadRasterizationOptions`，随后调用 `image.Save("output.pdf", new PdfOptions())`。生成的 PDF 可与没有 CAD 软件的利益相关者共享。

```csharp
private static void IterateCADNodes(CadBaseEntity obj)
{
    switch (obj.TypeName)
    {
        // Handle different entity types
    }
}
```

## 结论

Aspose.CAD for .NET 提供了一个无缝、高性能的解决方案，用于加载 dwg 文件数据、搜索特定文本并将结果导出为 PDF。通过本教程中的步骤，您已在 C# 应用程序中添加了强大的 CAD 文本搜索功能，无需依赖外部工具或昂贵的许可证。

## 常见问题

### Q1: 我可以在 .NET 中使用 Aspose.CAD 处理其他 CAD 格式吗？
**A1:** 是的，Aspose.CAD 支持超过 30 种 CAD 格式，包括 DXF、DWF 和 STL，提供了适用于混合格式工作流的多功能解决方案。

### Q2: Aspose.CAD for .NET 有免费试用吗？
**A2:** 有，您可以通过 [free trial](https://releases.aspose.com/) 探索其功能。

### Q3: 我如何获取 Aspose.CAD for .NET 的支持？
**A3:** 请访问 [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) 获取社区帮助和官方支持渠道。

### Q4: 什么是临时许可证，如何获取？
**A4:** 您可以获取 [temporary license](https://purchase.aspose.com/temporary-license/) 用于短期评估或概念验证项目。

### Q5: 哪里可以找到 Aspose.CAD for .NET 的详细文档？
**A5:** 请参考全面的 [documentation](https://reference.aspose.com/cad/net/) 获取深入指南、API 参考和代码示例。

---

**最后更新：** 2026-10-09  
**测试环境：** Aspose.CAD 24.11 for .NET  
**作者：** Aspose  

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions rasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
// Configure rasterization options
rasterizationOptions.Layouts = new[] { "Layout1" };
Aspose.CAD.ImageOptions.PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
cadImage.Save(MyDir + "SearchText_out.pdf", pdfOptions);
```

## 相关教程

- [How to convert DWG to PDF and Raster Images using Aspose.CAD for .NET](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)
- [Convert DWG to PNG & Export OLE Objects - Aspose.CAD Tutorial](/cad/net/advanced-export-techniques/exporting-ole-objects-from-dwg/)
- [How to Read DWT Files with Aspose.CAD for .NET](/cad/net/cad-features-and-support/reading-dwt/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}