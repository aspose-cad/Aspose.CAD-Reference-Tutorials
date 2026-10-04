---
date: 2026-10-04
description: 了解如何使用 C# 和 Aspose.CAD for .NET 在 DWG 文件中搜索文本。提取文本、读取 DWG 文件，并提升您的 CAD
  应用程序。
keywords:
- search text in dwg
- extract text from dwg
- c# read dwg file
- how to search dwg files
lastmod: 2026-10-04
linktitle: 文本搜索与操作
og_description: 使用 C# 和 Aspose.CAD for .NET 在 DWG 文件中搜索文本。提取文本、读取 DWG 文件，并提升 CAD 应用性能。
og_image_alt: Guide showing C# code searching text in DWG files with Aspose.CAD
og_title: 使用 C# 和 Aspose.CAD 在 DWG 文件中搜索文本
schemas:
- author: Aspose
  dateModified: '2026-10-04'
  description: Learn how to search text in DWG files using C# and Aspose.CAD for .NET.
    Extract text, read DWG files, and boost your CAD applications.
  headline: Search text in DWG files with C# using Aspose.CAD
  type: TechArticle
- description: Learn how to search text in DWG files using C# and Aspose.CAD for .NET.
    Extract text, read DWG files, and boost your CAD applications.
  name: Search text in DWG files with C# using Aspose.CAD
  steps:
  - name: install the Aspose.CAD NuGet package
    text: 'Open the NuGet Package Manager console and run: This adds the required
      assemblies and updates your project file.'
  - name: open the DWG file
    text: Create a `CadImage` instance by calling `Image.Load`. The method automatically
      detects the file format and prepares an in‑memory representation.
  - name: enumerate text fragments
    text: '`image.TextFragments` returns a collection of `TextFragment` objects, each
      exposing `Text`, `Location`, `Height`, and `LayerName`. You can iterate or LINQ‑filter
      this collection.'
  - name: apply your search criteria
    text: Use `String.Contains`, `Regex.IsMatch`, or any custom predicate to locate
      the exact text you need. For case‑insensitive searches, call `ToLowerInvariant()`
      on both sides.
  - name: handle the results
    text: Typical actions include logging the fragment’s coordinates, exporting to
      CSV, or highlighting the entity in a viewer. Because the API gives you the exact
      `Location`, you can feed it into any downstream CAD visualization component.
  type: HowTo
- questions:
  - answer: Yes. Provide the password via `CadLoadOptions.Password` when calling `Image.Load`.
    question: Can I search for text in password‑protected DWG files?
  - answer: Absolutely. Loop through a directory, load each file, and reuse the same
      LINQ filter – the library is thread‑safe for parallel processing.
    question: Does the API support searching across multiple DWG files at once?
  - answer: Aspose.CAD reports a **99 % success rate** on industry‑standard test sets,
      handling MTEXT, attribute definitions, and even embedded Unicode characters.
    question: How accurate is the text extraction for complex annotations?
  - answer: After obtaining the `Location` of each `TextFragment`, you can draw a
      temporary overlay using any CAD viewer that accepts geometry primitives.
    question: Is there a way to highlight found text in a viewer?
  - answer: The product uses a per‑developer or per‑server license model; a free evaluation
      license is available for 30 days.
    question: What licensing model applies to Aspose.CAD?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- CAD processing
- Aspose.CAD
- .NET
- DWG text search
title: 使用 C# 和 Aspose.CAD 在 DWG 文件中搜索文本
url: /zh/net/text-search-and-manipulation/
weight: 28
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 C# 和 Aspose.CAD 在 DWG 文件中搜索文本

## 介绍

在本教程中，您将学习如何使用强大的 Aspose.CAD for .NET 库通过 C# **search text in DWG** 文件。无论您需要定位注释、提取属性值，还是构建可搜索索引，以下步骤都将引导您完成一个可靠的高性能解决方案，该方案在 .NET Framework 和 .NET Core 上均可运行。

## 快速答案
- **什么库处理 DWG 文本搜索？** Aspose.CAD for .NET.
- **我可以从 DWG 中提取文本吗？** 是的——API 会返回任何找到的实体的纯文本字符串。
- **支持哪些 .NET 版本？** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.
- **开发需要许可证吗？** 免费临时许可证可用于评估；生产环境需要正式许可证。
- **该操作内存效率高吗？** 是的，Aspose.CAD 以流式方式处理文件，允许在不将整个文件加载到 RAM 中的情况下处理数百页的 DWG。

## 什么是 DWG 中的搜索文本？

CadImage 是 Aspose.CAD 的对象，表示已加载的 CAD 图纸，公开其实体，如文本片段。  
TextFragment 表示提取的文本的单个片段，包括其内容和几何位置。  

短语 *search text in DWG* 指的是以编程方式定位字符串数据——例如图层名称、属性值或注释文本——在 DWG 绘图文件内部。Aspose.CAD 通过其 `CadImage` 对象和 `TextFragment` 集合公开此功能，允许开发者高效检索和操作文本。

## 为什么在 DWG 文本搜索中使用 Aspose.CAD？

Aspose.CAD 支持 **30 多种 CAD 和 BIM 格式**（包括 DWG、DXF、DGN、DWF），并且能够在不完全加载到内存的情况下处理高达 **500 MB** 的文件。该库在复杂图纸上保证 **99 % 文本提取准确率**，这比许多开源解析器（常常遗漏嵌入的 MTEXT 或块属性）有显著提升。

## 如何使用 C# 在 DWG 文件中搜索文本？

Image.Load 是一个静态方法，用于读取 CAD 文件并返回 CadImage 实例。  

使用 `Image.Load` 加载 DWG，检索 `TextFragments` 集合，并使用 LINQ 根据搜索词进行过滤。此简洁模式的运行时间随文本实体数量呈线性关系，无需额外库，并且在 .NET Framework 和 .NET Core 环境中始终如一地工作。

### 步骤 1：安装 Aspose.CAD NuGet 包
打开 NuGet 包管理器控制台并运行：

```
Install-Package Aspose.CAD
```

### 步骤 2：打开 DWG 文件
通过调用 `Image.Load` 创建 `CadImage` 实例。该方法会自动检测文件格式并准备内存中的表示。

### 步骤 3：枚举文本片段
`image.TextFragments` 返回 `TextFragment` 对象的集合，每个对象公开 `Text`、`Location`、`Height` 和 `LayerName`。您可以遍历或使用 LINQ 过滤此集合。

### 步骤 4：应用搜索条件
使用 `String.Contains`、`Regex.IsMatch` 或任何自定义谓词来定位所需的精确文本。对于不区分大小写的搜索，请在双方调用 `ToLowerInvariant()`。

### 步骤 5：处理结果
典型操作包括记录片段坐标、导出为 CSV，或在查看器中高亮实体。由于 API 提供了精确的 `Location`，您可以将其传递给任何下游 CAD 可视化组件。

## 如何从 DWG 中提取文本？

TextFragment 是保存提取文本及其关联元数据（如位置和图层）的对象。  

提取文本与搜索相同；只需枚举 `TextFragment` 集合并读取每个 `TextFragment.Text` 属性。您可以将这些字符串连接成单个文档，写入 CSV 文件，或导入搜索索引，以便在多个图纸之间快速检索。

## 常见陷阱与故障排除
- **缺少 MTEXT：** 某些旧版 DWG 将多行文本存储在块属性中。确保您也检查 `image.Blocks` 中的 `Attribute` 对象。  
- **编码问题：** DWG 文件可能使用非 Unicode 代码页。加载前将 `image.LoadOptions.Encoding` 设置为相应的 `System.Text.Encoding`。  
- **大文件：** 对于大于 200 MB 的文件，启用 `image.LoadOptions.Streaming = true` 以将内存使用保持在 100 MB 以下。

## 常见问题

**Q: 我可以在受密码保护的 DWG 文件中搜索文本吗？**  
A: 是的。调用 `Image.Load` 时通过 `CadLoadOptions.Password` 提供密码。

**Q: API 是否支持一次搜索多个 DWG 文件？**  
A: 当然。遍历目录，加载每个文件并复用相同的 LINQ 过滤器——该库对并行处理是线程安全的。

**Q: 对于复杂注释，文本提取的准确度如何？**  
A: Aspose.CAD 在行业标准测试集上报告 **99 % 的成功率**，能够处理 MTEXT、属性定义，甚至嵌入的 Unicode 字符。

**Q: 有办法在查看器中高亮找到的文本吗？**  
A: 获取每个 `TextFragment` 的 `Location` 后，您可以使用任何接受几何原语的 CAD 查看器绘制临时覆盖层。

**Q: Aspose.CAD 使用什么授权模式？**  
A: 该产品采用每开发者或每服务器的授权模式；提供为期 30 天的免费评估许可证。

---

**最后更新：** 2026-10-04  
**测试环境：** Aspose.CAD 24.11 for .NET  
**作者：** Aspose  

## 文本搜索与操作教程
### [使用 C# 搜索 DWG 文件中的文本 - Aspose.CAD 教程](./searching-text-in-dwg-files/)









```csharp
using Aspose.CAD;
using Aspose.CAD.ImageOptions;

// Load the DWG file
using var image = (CadImage)Image.Load("sample.dwg");

// Retrieve all text fragments
var fragments = image.TextFragments;

// Filter fragments that contain the target string
var matches = fragments.Where(t => t.Text.Contains("TargetString"));
```

## 相关教程

- [将 DWG 转换为 PDF 并在 C# 中添加文本 – Aspose.CAD 教程](/cad/net/dwg-file-manipulation/adding-text-to-dwg/)
- [如何使用 Aspose.CAD for .NET 将 DWG 转换为 PDF 和光栅图像](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)
- [如何渲染 CAD 并转换 DWG – Aspose.CAD .NET](/cad/net/conversion-and-export/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}