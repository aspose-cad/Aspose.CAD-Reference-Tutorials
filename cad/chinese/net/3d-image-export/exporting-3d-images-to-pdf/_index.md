---
date: 2026-07-04
description: 了解如何使用 Aspose.CAD for .NET 设置 PDF 页面大小并从 3D CAD 图像导出 PDF – 步骤指南，教您将 DWG
  转换为 PDF 并将 CAD 保存为 PDF。
keywords:
- set pdf page size
- export pdf from cad
- convert dwg to pdf
- save cad as pdf
- cad to pdf tutorial
linktitle: 导出 3D 图像为 PDF
schemas:
- author: Aspose
  dateModified: '2026-07-04'
  description: Learn how to set PDF page size and export PDF from 3D CAD images using
    Aspose.CAD for .NET – a step‑by‑step guide to convert DWG to PDF and save CAD
    as PDF.
  headline: Set PDF page size – Export 3D Images to PDF with Aspose.CAD
  type: TechArticle
- description: Learn how to set PDF page size and export PDF from 3D CAD images using
    Aspose.CAD for .NET – a step‑by‑step guide to convert DWG to PDF and save CAD
    as PDF.
  name: Set PDF page size – Export 3D Images to PDF with Aspose.CAD
  steps:
  - name: Load the CAD Image
    text: '`Image` class represents a CAD drawing loaded into memory, ready for rasterization.'
  - name: Configure Rasterization Options (Save CAD as PDF)
    text: '`RasterizationOptions` class defines how the CAD data is rasterized, including
      page size, DPI, and whether 3‑D entities are rendered.'
  - name: Set PDF Options (Create PDF from CAD)
    text: '`PdfOptions` class holds the output format settings and links the rasterization
      options to PDF generation.'
  - name: Save as PDF (Generate PDF from 3D Model)
    text: '`Save` method on the `Image` object writes the rasterized content to the
      specified PDF file, producing a ready‑to‑share document.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD supports more than 50 input and output formats, including
      DWG, DXF, DGN, STL, and IFC, ensuring flexibility for any project.
    question: Is Aspose.CAD compatible with all CAD file formats?
  - answer: Absolutely. Set `PageWidth` and `PageHeight` in `RasterizationOptions`
      to any size in points, inches, or millimetres before calling `Save`.
    question: Can I customize the page dimensions when exporting to PDF?
  - answer: Yes, you can obtain temporary licenses for Aspose.CAD by visiting [Temporary
      License](https://purchase.aspose.com/temporary-license/).
    question: Are temporary licenses available for Aspose.CAD?
  - answer: Head to the [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19) for
      expert help and peer‑to‑peer advice.
    question: Where can I find additional support or community discussions?
  - answer: Yes, you can explore the features of Aspose.CAD by accessing the [free
      trial](https://releases.aspose.com/).
    question: Is there a free trial version of Aspose.CAD?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: 设置 PDF 页面大小 – 使用 Aspose.CAD 导出 3D 图像为 PDF
url: /zh/net/3d-image-export/exporting-3d-images-to-pdf/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 将 3D 图像导出为 PDF - Aspose.CAD 教程

## 简介

如果您需要在将 3‑D CAD 图纸转换为 PDF 时 **set PDF page size**，那么您来对地方了。本教程将逐步演示如何加载 CAD 文件，配置光栅化选项——包括自定义页面尺寸——并使用 Aspose.CAD for .NET 生成高保真 PDF。完成后，您将能够 **export PDF from CAD**、**save CAD as PDF**，并在无需安装 AutoCAD 的情况下控制每个布局细节。

## 快速回答

- **“export PDF from CAD” 是什么意思？** 它将 CAD 图纸（DWG、DXF、DGN 等）转换为可以在任何设备上打开的 PDF。  
- **哪个库执行转换？** Aspose.CAD for .NET 提供光栅化和 PDF 导出，无需外部依赖。  
- **我需要许可证吗？** 生产环境需要临时或完整许可证；提供免费试用。  
- **我可以设置自定义页面尺寸吗？** 是的——在 `RasterizationOptions` 中使用 `PageWidth` 和 `PageHeight`。  
- **会保留 3‑D 几何形状吗？** 3‑D 实体会被光栅化；启用 `TypeOfEntities.Entities3D` 可获得完整的 3‑D 支持。  

## 在 CAD 环境中，“export PDF” 是什么？

从 CAD 导出 PDF 意味着将 CAD 图纸（DWG、DXF、DGN 等）转换为 PDF 文件，该文件可以包含矢量图形、光栅化的 3‑D 视图以及精确的页面布局信息，便于与没有 CAD 软件的任何人共享。

## 为什么使用 Aspose.CAD 导出 PDF？

Aspose.CAD 让您 **set PDF page size** 并在托管的 .NET 代码中完整导出 PDF。它支持超过 50 种 CAD 格式，能够处理高达 2 GB 的文件而无需将整个文档加载到内存中，并保留线宽、颜色以及可选的 3‑D 实体渲染，光栅化 DPI 可达 1200。该库可在 Windows、Linux 和 macOS 上运行，因此生成的 PDF 可在任何平台使用。

## 先决条件

- **Aspose.CAD for .NET** 已安装。请从 [Aspose.CAD for .NET download page](https://releases.aspose.com/cad/net/) 下载。  
- 包含您要转换的 CAD 文件的文件夹（例如 `C:\CAD\`）。  
- .NET 6.0 或更高版本（或 .NET Framework 4.7.2）。  

## 导入命名空间

`using` 语句导入处理光栅化和 PDF 选项所需的 Aspose.CAD 命名空间。  

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
```

## 分步指南

### 在将 CAD 导出为 PDF 时如何设置 PDF 页面尺寸？

加载 CAD 文件，在 `RasterizationOptions` 中配置页面尺寸，将这些选项附加到 `PdfOptions` 实例，然后调用 `Save`。这一四步流程让您能够全面控制输出尺寸和质量，同时保持代码简洁。

### 步骤 1：加载 CAD 图像

`Image` 类表示已加载到内存中、准备进行光栅化的 CAD 图纸。  

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";
using (Image cadImage = Image.Load(sourceFilePath))
{
    // Your code for loading the CAD image goes here
}
```

### 步骤 2：配置光栅化选项（将 CAD 保存为 PDF）

`RasterizationOptions` 类定义 CAD 数据的光栅化方式，包括页面尺寸、DPI 以及是否渲染 3‑D 实体。  

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
// rasterizationOptions.TypeOfEntities = TypeOfEntities.Entities3D;

rasterizationOptions.Layouts = new string[] { "Model" };
```

### 步骤 3：设置 PDF 选项（从 CAD 创建 PDF）

`PdfOptions` 类保存输出格式设置，并将光栅化选项关联到 PDF 生成。  

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

### 步骤 4：保存为 PDF（从 3D 模型生成 PDF）

`Image` 对象的 `Save` 方法将光栅化内容写入指定的 PDF 文件，生成可直接共享的文档。  

```csharp
MyDir = MyDir + "Export3DImagestoPDF_out.pdf";
cadImage.Save(MyDir, pdfOptions);
```

## 常见问题及解决方案

| 问题 | 原因 | 解决方案 |
|-------|--------|-----|
| **输出 PDF 为空** | 布局名称错误或缺少 `Model` 布局。 | 确认 `rasterizationOptions.Layouts` 与 CAD 文件中存在的布局匹配。 |
| **分辨率低** | 默认光栅化 DPI 较低。 | 在保存前设置 `rasterizationOptions.Resolution = 300;`。 |
| **未显示 3‑D 实体** | `TypeOfEntities` 被注释掉。 | 取消注释 `rasterizationOptions.TypeOfEntities = TypeOfEntities.Entities3D;`。 |
| **许可证异常** | 使用未授权的试用版。 | 通过 `License license = new License(); license.SetLicense("Aspose.CAD.lic");` 应用临时或永久许可证。 |

## 常见问题

**Q: Aspose.CAD 是否兼容所有 CAD 文件格式？**  
A: 是的，Aspose.CAD 支持超过 50 种输入和输出格式，包括 DWG、DXF、DGN、STL 和 IFC，确保任何项目的灵活性。

**Q: 导出为 PDF 时我可以自定义页面尺寸吗？**  
A: 当然可以。在调用 `Save` 之前，在 `RasterizationOptions` 中设置 `PageWidth` 和 `PageHeight` 为任意点、英寸或毫米尺寸。

**Q: Aspose.CAD 是否提供临时许可证？**  
A: 是的，您可以访问 [Temporary License](https://purchase.aspose.com/temporary-license/) 获取 Aspose.CAD 的临时许可证。

**Q: 我可以在哪里找到更多支持或社区讨论？**  
A: 前往 [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19) 获取专家帮助和同行建议。

**Q: Aspose.CAD 是否有免费试用版？**  
A: 是的，您可以通过访问 [free trial](https://releases.aspose.com/) 试用 Aspose.CAD 的功能。

## 结论

现在，您已经拥有使用 Aspose.CAD for .NET **set PDF page size** 和 **export PDF from 3D CAD images** 的完整、可投入生产的方法。通过调整光栅化选项，您可以微调分辨率、页面布局和 3‑D 实体渲染，以满足任何文档需求。尝试不同的 DPI 设置和页面尺寸，以实现文件大小与视觉保真度之间的最佳平衡。

{{< blocks/products/products-backtop-button >}}

## 相关教程

- [导出特定布局为 PDF - Aspose.CAD 指南](/cad/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/)
- [导出 DWG 为 PDF 或光栅图像 - Aspose.CAD 指南](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)
- [在 Aspose.CAD for .NET 中导出 DGN 为 PDF](/cad/net/cad-export-formats/export-dgn-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

--- 

**最后更新：** 2026-07-04  
**测试环境：** Aspose.CAD 24.11 for .NET  
**作者：** Aspose