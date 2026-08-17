---
date: 2026-08-17
description: 了解如何使用 C# 和 Aspose.CAD for .NET 向 DWG 文件添加图像。本指南将带您完成导入图像、设置插入点以及导出为
  PDF 的过程。
keywords:
- add image to dwg
- convert dwg to pdf
- set insertion point dwg
- embed png in dwg
- save dwg as pdf
lastmod: 2026-08-17
linktitle: 使用 C# 将图像导入 DWG 文件
og_description: 了解如何使用 C# 向 DWG 文件添加图像。本教程涵盖导入图像、设置插入点以及使用 Aspose.CAD 将 DWG 转换为 PDF。
og_image_alt: Guide showing C# code to embed an image into a DWG file using Aspose.CAD
og_title: 如何使用 C# 和 Aspose.CAD 向 DWG 文件添加图像
schemas:
- author: Aspose
  dateModified: '2026-08-17'
  description: Learn how to add image to dwg files using C# and Aspose.CAD for .NET.
    This guide walks you through importing images, setting insertion points, and exporting
    to PDF.
  headline: How to add image to dwg files with C# using Aspose.CAD
  type: TechArticle
- description: Learn how to add image to dwg files using C# and Aspose.CAD for .NET.
    This guide walks you through importing images, setting insertion points, and exporting
    to PDF.
  name: How to add image to dwg files with C# using Aspose.CAD
  steps:
  - name: set up your document directory
    text: Prepare the folder that contains the source DWG and the image you want to
      embed.
  - name: load the dwg file
    text: The `CadImage` class represents a DWG drawing and provides access to its
      entities, layers, and metadata.
  - name: define the image properties
    text: Create an `Image` object that points to the raster file (e.g., PNG) and
      specify its format.
  - name: set insertion point dwg and vectors
    text: Specify where the image should appear inside the drawing and how it should
      be scaled. The insertion point is defined by a 2‑D coordinate, while the vectors
      control width and height.
  - name: create and configure the raster image
    text: Instantiate a `RasterImage` object, assign the image data, and set any additional
      rendering options.
  - name: add image to dwg file
    text: Insert the configured raster image into the DWG’s entities collection so
      it becomes part of the drawing.
  - name: save as pdf (export dwg to pdf)
    text: After embedding the image you can **convert dwg to pdf** or **save dwg as
      pdf** with a single call. This is useful for sharing the drawing with stakeholders
      who don’t have CAD software.
  type: HowTo
- questions:
  - answer: The core library is .NET‑specific, but Aspose offers equivalent APIs for
      Java, Python and other platforms.
    question: Can I use Aspose.CAD for .NET with other programming languages?
  - answer: Yes, you can explore a free trial on the [Aspose free trial page](https://releases.aspose.com/).
    question: Is a free trial available for Aspose.CAD?
  - answer: The documentation is available in the [Aspose.CAD .NET API reference](https://reference.aspose.com/cad/net/).
    question: Where can I find detailed documentation for Aspose.CAD?
  - answer: Visit the [temporary license page](https://purchase.aspose.com/temporary-license/)
      to get a temporary license.
    question: How do I obtain a temporary license for Aspose.CAD?
  - answer: Yes, you can seek support and engage with the community in the [Aspose.CAD
      community forum](https://forum.aspose.com/c/cad/19).
    question: Are there community forums for Aspose.CAD support?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- CAD
- Aspose.CAD
- C# image processing
- DWG manipulation
title: 如何使用 C# 和 Aspose.CAD 向 DWG 文件添加图像
url: /zh/net/image-manipulation-and-rendering/importing-images-into-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何使用 C# 和 Aspose.CAD 向 DWG 文件添加图像

## 介绍

在需要使用徽标、照片或光栅图形丰富 CAD 图纸时，向 DWG 文件添加图像是一项常规需求。在本教程中，您将学习如何使用 C# 和 Aspose.CAD for .NET **编程方式向 DWG 添加图像**，随后可选择将结果转换为 PDF。步骤已拆分，您可以将每个部分复制粘贴到自己的项目中。

## 快速答案
- **哪个库负责此工作？** Aspose.CAD for .NET。
- **我可以嵌入 PNG 文件吗？** 可以 – 支持 PNG、JPEG、BMP 以及其他光栅格式。
- **开发时需要许可证吗？** 免费试用可用于测试；生产环境需要商业许可证。
- **支持 PDF 导出吗？** 完全支持 – 您可以一行代码将更新后的 DWG 转换为 PDF。
- **兼容哪些 .NET 版本？** .NET Framework 4.6+、.NET Core 3.1+、.NET 5/6/7。

## DWG 文件是什么？

DWG 文件是 Autodesk AutoCAD 绘图的原生二进制格式，存储矢量几何、图层和元数据。它在建筑、工程和施工领域被广泛使用，Aspose.CAD 能在无需安装 AutoCAD 的情况下读取和写入此格式。

## 为什么使用 Aspose.CAD 向 DWG 添加图像？

Aspose.CAD 支持 **50 多种输入和输出格式**，能够在不将整个文档加载到内存中的情况下处理超过 500 MB 的文件，并提供在无头服务器环境下可靠运行的确定性 API。这使得批量处理 DWG 图纸既快速又可靠。

## 先决条件
- 基本的 C# 编程知识。
- 已安装 Aspose.CAD for .NET。您可以从 [Aspose.CAD for .NET 下载页面](https://releases.aspose.com/cad/net/) 下载。还可以在 [Aspose 发布页面](https://releases.aspose.com/) 探索其他 Aspose 产品。
- Visual Studio 2022 或更高版本等开发环境。

## 如何使用 Aspose.CAD 向 DWG 添加图像？

加载目标 DWG，创建描述要嵌入图片的光栅图像对象，设置插入点和缩放向量，然后将图像附加到图纸。最后，保存修改后的 DWG 或直接导出为 PDF。整个工作流只需少量 API 调用，典型的 2 页图纸在一秒内完成。

### 导入命名空间
包含您需要的 CAD 类所在的命名空间。

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

### 步骤 1：设置文档目录
准备包含源 DWG 和要嵌入图像的文件夹。

```csharp
string MyDir = "Your Document Directory";
```

### 步骤 2：加载 DWG 文件
`CadImage` 类表示 DWG 绘图，并提供对其实体、图层和元数据的访问。

```csharp
string dwgPathToFile = MyDir + "Drawing11.dwg";
CadImage cadImage1 = (CadImage)Image.Load(dwgPathToFile);
```

### 步骤 3：定义图像属性
创建指向光栅文件（例如 PNG）的 `Image` 对象并指定其格式。

```csharp
CadRasterImageDef cadRasterImageDef = new CadRasterImageDef("road-sign-custom.png", 640, 562);
cadRasterImageDef.ObjectHandle = "A3B4";
```

### 步骤 4：设置插入点和向量
指定图像在图纸中的出现位置以及缩放方式。插入点由二维坐标定义，向量控制宽度和高度。

```csharp
Cad3DPoint insertionPoint = new Cad3DPoint(26.77, 22.35);
Cad3DPoint uVector = new Cad3DPoint(0.0061565450840500831, 0);
Cad3DPoint vVector = new Cad3DPoint(0, 0.0061565450840500822);
```

### 步骤 5：创建并配置光栅图像
实例化 `RasterImage` 对象，分配图像数据，并设置其他渲染选项。

```csharp
CadRasterImage cadRasterImage = new CadRasterImage(cadRasterImageDef, insertionPoint, uVector, vVector);
cadRasterImage.ImageDefReference = "A3B4";
cadRasterImage.DisplayFlags = 7;
cadRasterImage.ClippingState = 0;
cadRasterImage.ClipBoundaryVertexList.Add(new Cad2DPoint(-0.5, 0.5));
cadRasterImage.ClipBoundaryVertexList.Add(new Cad2DPoint(639.5, 561.5));
```

### 步骤 6：向 DWG 文件添加图像
将配置好的光栅图像插入 DWG 的实体集合，使其成为图纸的一部分。

```csharp
CadImage cadImage = (CadImage)cadImage1;
cadImage.BlockEntities["*Model_Space"].AddEntity(cadRasterImage);

List<CadBaseObject> list = new List<CadBaseObject>(cadImage.Objects);
list.Add(cadRasterImageDef);
cadImage.Objects = list.ToArray();
```

### 步骤 7：另存为 PDF（将 DWG 导出为 PDF）
嵌入图像后，您可以使用单行代码 **将 dwg 转换为 pdf** 或 **将 dwg 保存为 pdf**。这对于向没有 CAD 软件的利益相关者共享图纸非常有用。

```csharp
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.VectorRasterizationOptions = cadRasterizationOptions;
cadRasterizationOptions.DrawType = CadDrawTypeMode.UseObjectColor;

cadRasterizationOptions.PageHeight = 1600;
cadRasterizationOptions.PageWidth = 1600;
cadRasterizationOptions.Layouts = new string[] { "Model" };
cadImage1.Save(MyDir + "export2.pdf", pdfOptions);
```

## 如何在嵌入图像后将 DWG 转换为 PDF？

对 `CadImage` 实例调用 `Save` 方法，传入 `SaveFormat.Pdf`，并可选地提供 `PdfOptions` 对象以控制页面大小、光栅化和元数据。Aspose.CAD 会保留嵌入的光栅图像、图层和线宽，生成可在任何查看器中打开的忠实 PDF 表现。此转换仅需一行代码即可完成。

## 常见问题及解决方案
- **图像出现在错误位置** – 仔细检查插入点坐标和方向向量；它们相对于图纸原点。
- **大图像导致内存峰值** – 在插入前使用光栅图像的 `Resize` 选项，或使用分辨率较低的副本。
- **PDF 导出失去矢量质量** – 确保使用保留矢量数据的 `PdfOptions` 保存；光栅图像始终按原样嵌入。

## 常见问题

**Q: 我可以在其他编程语言中使用 Aspose.CAD for .NET 吗？**  
A: 核心库是 .NET 专用的，但 Aspose 为 Java、Python 等平台提供了等效的 API。

**Q: Aspose.CAD 有免费试用吗？**  
A: 有，您可以在 [Aspose 免费试用页面](https://releases.aspose.com/) 进行试用。

**Q: 哪里可以找到 Aspose.CAD 的详细文档？**  
A: 文档位于 [Aspose.CAD .NET API 参考](https://reference.aspose.com/cad/net/) 中。

**Q: 如何获取 Aspose.CAD 的临时许可证？**  
A: 请访问 [临时许可证页面](https://purchase.aspose.com/temporary-license/) 获取临时许可证。

**Q: 是否有 Aspose.CAD 的社区论坛？**  
A: 有，您可以在 [Aspose.CAD 社区论坛](https://forum.aspose.com/c/cad/19) 寻求支持并与社区交流。

---

**最后更新：** 2026-08-17  
**测试版本：** Aspose.CAD 24.11 for .NET  
**作者：** Aspose

## 相关教程

- [导出 DWG 为 PDF 或光栅图像 - Aspose.CAD 指南](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)
- [在 C# 中将 DWG 导出为 DXF 格式 - Aspose.CAD 教程](/cad/net/advanced-export-techniques/exporting-dwg-to-dxf/)
- [导出特定布局为 PDF - Aspose.CAD 指南](/cad/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}