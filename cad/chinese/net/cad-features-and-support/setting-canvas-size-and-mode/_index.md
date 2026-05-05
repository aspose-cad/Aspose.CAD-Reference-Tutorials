---
date: 2026-03-29
description: 在本分步指南中，了解如何使用 Aspose.CAD for .NET 将 CAD 创建为 PDF、设置画布大小，以及将 CAD 导出为 PDF
  或 TIFF。
linktitle: Setting Canvas Size and Mode
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: 如何从 CAD 创建 PDF：在 Aspose.CAD for .NET 中设置画布大小和模式
url: /zh/net/cad-features-and-support/setting-canvas-size-and-mode/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 Aspose.CAD for .NET 中设置画布大小和模式

## 介绍

准备好在 **从 CAD 创建 PDF** 时控制输出尺寸了吗？本教程将演示如何设置画布大小和模式、加载 CAD 文件，并使用 Aspose.CAD for .NET 将其导出为 PDF 或 TIFF。无论您是需要 **将 DXF 转换为 PDF**、生成高分辨率图纸，还是仅仅调整光栅化区域，下面的步骤都能为您提供可靠的生产级解决方案。

## 快速答案
- **“从 CAD 创建 PDF”是什么意思？** 将 CAD 图纸（如 DXF、DWG）转换为 PDF 文档，保留矢量和光栅细节。  
- **哪个选项控制输出大小？** `CadRasterizationOptions.PageWidth` 和 `PageHeight`（画布大小）。  
- **我还能导出为 TIFF 吗？** 可以——使用带有相同光栅化设置的 `TiffOptions`。  
- **生产环境需要许可证吗？** 需要商业许可证；提供免费试用。  
- **支持的 .NET 版本？** .NET Framework 4.5+、.NET Core 3.1+、.NET 5/6/7。

## 什么是 “从 CAD 创建 PDF”？
从 CAD 创建 PDF 指将 CAD 图纸渲染为面向页面的格式（PDF），以便在无需 CAD 软件的情况下查看、打印或共享。Aspose.CAD 负责繁重的工作，让您可以定义画布大小、缩放比例和输出格式。

## 为什么在从 CAD 创建 PDF 时要设置画布大小？
设置画布大小可以精确控制生成的 PDF 或 TIFF 的分辨率和尺寸。这在以下情况下尤为有用：
- 为特定纸张尺寸的打印准备图纸。  
- 为网页预览生成缩略图或高分辨率图像。  
- 确保多个文档之间布局一致。

## 前置条件

- Aspose.CAD 库：从 [Aspose.CAD 网站](https://releases.aspose.com/cad/net/) 下载并安装 Aspose.CAD 库。  
- 开发环境：确保机器上已配置 .NET 开发环境。  
- 示例 CAD 文件：本教程使用示例 DXF 文件。您可以在 [Aspose.CAD 文档](https://reference.aspose.com/cad/net/) 中找到该文件。

## 导入命名空间

首先，导入 CAD 处理所需的命名空间：

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## 如何使用自定义画布大小从 CAD 创建 PDF

### 步骤 1：加载 CAD 文件

我们首先 **加载 CAD 文件**（例如 DXF）到 `Image` 对象中。这一步将 CAD 文件加载到内存。

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (Image image = Image.Load(sourceFilePath))
{
    // Your code for further steps will go here
}
```

### 步骤 2：创建 CadRasterizationOptions

创建 `CadRasterizationOptions` 实例并定义画布大小。`PageWidth` 和 `PageHeight` 属性让您 **设置画布大小** 为所需的精确尺寸。

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.AutomaticLayoutsScaling = true;
rasterizationOptions.NoScaling = false;
```

### 步骤 3：创建 PdfOptions（将 CAD 导出为 PDF）

将光栅化设置关联到 `PdfOptions` 对象。此配置使您能够 **将 CAD 导出为 PDF**，并使用自定义画布。

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

### 步骤 4：导出为 PDF（将 DXF 转换为 PDF）

现在将图像保存为 PDF。此步骤 **从 CAD 创建 PDF**，使用我们之前设置的选项。

```csharp
image.Save(MyDir + "result_out.pdf", pdfOptions);
```

### 步骤 5：创建 TiffOptions（将 CAD 导出为 TIFF）

如果还需要光栅图像，配置 `TiffOptions`。相同的光栅化选项会被复用，因此 **将 CAD 导出为 TIFF** 时会遵循画布大小。

```csharp
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.VectorRasterizationOptions = rasterizationOptions;
```

### 步骤 6：导出为 TIFF

最后，将图纸保存为 TIFF 文件。

```csharp
image.Save(MyDir + "result_out.tiff", tiffOptions);
```

## 常见问题及解决方案

- **画布被裁剪** – 确认 `AutomaticLayoutsScaling` 设置为 `true`，且 `NoScaling` 为 `false`，以便图纸按画布尺寸缩放。  
- **PDF 分辨率低** – 增大 `PageWidth`/`PageHeight` 或在 `CadRasterizationOptions` 上设置 `Resolution`。  
- **文件未找到错误** – 确保 `MyDir` 指向有效目录，且 DXF 文件名完全匹配。

## 常见问答

### Q1：我可以将 Aspose.CAD 与其他 .NET 库一起使用吗？
A1：可以，Aspose.CAD 可无缝集成其他 .NET 库，提供更强大的 CAD 操作能力。

### Q2：Aspose.CAD 有免费试用吗？
A2：有，您可以使用免费试用探索 Aspose.CAD 功能。访问 [此处](https://releases.aspose.com/) 开始使用。

### Q3：如何获取 Aspose.CAD 的支持？
A3：请前往 [Aspose.CAD 论坛](https://forum.aspose.com/c/cad/19) 获取支持和讨论。

### Q4：在哪里可以找到 Aspose.CAD 的完整文档？
A4：请参考 [Aspose.CAD 文档](https://reference.aspose.com/cad/net/) 获取详细信息和示例。

### Q5：如何购买 Aspose.CAD for .NET？
A5：请访问 [购买页面](https://purchase.aspose.com/buy) 完成购买。

**其他问答**

**问：我可以将多页 CAD 图纸导出为单个 PDF 吗？**  
答：可以。设置 `CadRasterizationOptions` 中的 `PageCount`，库会将页面合并为一个 PDF。

**问：画布大小会影响矢量数据的质量吗？**  
答：矢量数据保持分辨率无关；画布大小仅影响光栅化元素和图像分辨率。

---

**最后更新：** 2026-03-29  
**测试版本：** Aspose.CAD 24.11 for .NET  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}