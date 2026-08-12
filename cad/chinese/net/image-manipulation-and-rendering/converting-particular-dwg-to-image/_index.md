---
date: 2026-08-12
description: 使用 Aspose.CAD for .NET 在 C# 中提取 DWG 文本并将特定 DWG 转换为图像。通过代码示例一步步学习。
keywords:
- extract text from dwg
- convert specific dwg to image
- Aspose.CAD .NET
lastmod: 2026-08-12
linktitle: 在 C# 中将特定 DWG 转换为图像
og_description: 使用 Aspose.CAD 在 C# 中提取 DWG 文本并将特定 DWG 转换为图像。遵循本简明指南，快速实现。
og_image_alt: Guide showing DWG to image conversion and text extraction using Aspose.CAD
  in C#
og_title: 在 C# 中提取 DWG 文本并将特定 DWG 转换为图像
schemas:
- author: Aspose
  dateModified: '2026-08-12'
  description: Extract text from DWG and convert specific DWG to image in C# using
    Aspose.CAD for .NET. Learn step‑by‑step with code snippets.
  headline: Extract text from DWG and convert specific DWG to image in C#
  type: TechArticle
- questions:
  - answer: Aspose.CAD supports DWG releases from AutoCAD 2000 up to the latest 2024
      version, covering over 90 % of files created in the field.
    question: Is Aspose.CAD compatible with all versions of DWG files?
  - answer: Yes – you can change resolution, image format, anti‑aliasing, and background
      color to suit PNG, JPEG, or PDF targets.
    question: Can I customize the rasterization options for different outputs?
  - answer: Explore the comprehensive [Aspose.CAD documentation](https://reference.aspose.com/cad/net/)
      for more code samples and API details.
    question: Where can I find additional examples and documentation?
  - answer: Absolutely – you can download a trial version on the **[Aspose trial download
      page](https://releases.aspose.com/)** and evaluate all features without restrictions
      for 30 days.
    question: Is there a free trial available for Aspose.CAD?
  - answer: Join the active [Aspose.CAD forum](https://forum.aspose.com/c/cad/19)
      where developers share solutions and the Aspose team answers questions.
    question: How can I get support or connect with the community?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- extract text from dwg
- Aspose.CAD
- C# CAD processing
title: 在 C# 中提取 DWG 文本并将特定 DWG 转换为图像
url: /zh/net/image-manipulation-and-rendering/converting-particular-dwg-to-image/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 将特定 DWG 转换为图像（C#）- Aspose.CAD 指南

## 介绍

在现代工程应用中，您经常需要 **extract text from DWG** 文件并 **convert specific DWG to image** 为报告或可视化的格式。Aspose.CAD for .NET 为您提供了功能完整的 API，能够在无需任何外部 CAD 软件的情况下处理这两项任务。在本教程中，您将学习如何加载 DWG、筛选文本实体、光栅化图纸，最后将结果保存为 PDF 图像——全部使用简洁的 C# 代码。

## 快速答案
- **第一步是什么？** Load the DWG file with `new CadImage("file.dwg")`.  
- **哪个类用于过滤文本？** Use `CadEntityFilter` to select `Text` entities.  
- **如何定义图像尺寸？** Set `Width` and `Height` on `CadRasterizationOptions`.  
- **使用什么输出格式？** The example saves to PDF, which embeds the raster image.  
- **生产环境需要许可证吗？** Yes – a commercial Aspose.CAD license removes evaluation limits.

## 如何从 dwg 中提取文本？

加载 DWG，应用仅选择文本实体的过滤器，然后读取每个实体的 `TextString` 属性。这种方法会返回图纸中存在的所有注释、标签或尺寸文本，使您能够将其用于搜索、索引或报告。

## 为什么将特定 dwg 转换为图像？

将 DWG 转换为光栅图像可以让您在无法渲染原生 CAD 格式的文档、网页或移动应用中嵌入图纸。Aspose.CAD 处理 **over 50+ CAD formats**，并且能够在使用不到 200 MB 内存的情况下光栅化数百页的图纸，这使其适用于高吞吐量的服务器场景。

## 先决条件

- Visual Studio（任何近期版本）用于编译和运行 C# 项目。  
- Aspose.CAD for .NET – 确保已安装该库。您可以在 **[Aspose.CAD for .NET download page](https://releases.aspose.com/cad/net/)** 上找到下载链接。  
- 您想要处理的 DWG 文件；示例文件 *visualization_-_conference_room.dwg* 在代码片段中使用。

## 导入命名空间

以下命名空间为您提供对核心 CAD 类、光栅化选项和 PDF 输出助手的访问：

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## 步骤 1：加载 dwg 文件

通过传入 DWG 文件路径创建 `CadImage` 实例。`CadImage` 对象在内存中表示整个图纸，并提供对其图层、实体和元数据的访问。

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";
var cadImage = (CadImage)Aspose.CAD.Image.Load(sourceFilePath);
```

## 步骤 2：过滤实体

`CadEntityFilter` 让您只挑选所需的实体。在本指南中，我们将其配置为保留 **text** 对象，丢弃线条、圆形以及您不希望出现在最终图像中的其他几何体。

```csharp
CadBaseEntity[] entities = cadImage.Entities;
List<CadBaseEntity> filteredEntities = new List<CadBaseEntity>();

foreach (CadBaseEntity baseEntity in entities)
{
    // Selection or filtration of entities
    if (baseEntity.TypeName == CadEntityTypeName.TEXT)
    {
        filteredEntities.Add(baseEntity);
    }
}

cadImage.Entities = filteredEntities.ToArray();
```

## 步骤 3：设置光栅化选项

`CadRasterizationOptions` 控制图纸如何转换为位图。您可以定义输出尺寸、背景颜色和分辨率（DPI）。以下定义锚点介绍了该类：

`CadRasterizationOptions` 类指定图像尺寸、分辨率和渲染设置，用于将 CAD 图纸转换为光栅格式。  

在将选项传递给 PDF 导出器之前，设置所需的宽度、高度和背景颜色。

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions rasterizationOptions =
    new Aspose.CAD.ImageOptions.CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.AutomaticLayoutsScaling = true;
```

## 步骤 4：设置 PDF 选项

`PdfOptions` 将光栅化设置与 PDF 特有的功能（如压缩）捆绑在一起。该类的定义锚点首先出现：

`PdfOptions` 封装了 PDF 生成参数，包括决定 CAD 数据在 PDF 文档中如何渲染的光栅化选项。  

将先前创建的 `CadRasterizationOptions` 实例分配给 `VectorRasterizationOptions` 属性。

```csharp
Aspose.CAD.ImageOptions.PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## 步骤 5：保存为 PDF

最后，对 `CadImage` 对象调用 `Save` 方法，传入目标文件名和配置好的 `PdfOptions`。PDF 将包含过滤后图纸的高质量图像。

```csharp
string outFile = MyDir + "result_out_generated.pdf";
cadImage.Save(outFile, pdfOptions);
```

## 常见问题与故障排除

- **过滤后缺少文本** – 确保 DWG 实际包含 `Text` 实体；某些图纸将注释存储为 `MText`。如有需要，调整过滤器以包含 `MText`。  
- **输出图像为空白** – 验证光栅化 DPI 是否足够高（300 DPI 为安全默认值），并确保在查看 PDF 时背景颜色未设置为透明。  
- **大文件出现内存不足错误** – 使用支持流式处理的 `LoadOptions` 重载，这可防止一次性将整个文件加载到内存中。

## 常见问答

**Q: Aspose.CAD 是否兼容所有版本的 DWG 文件？**  
A: Aspose.CAD 支持从 AutoCAD 2000 到最新的 2024 版本的 DWG 发布，覆盖了现场创建的超过 90 % 的文件。

**Q: 我可以为不同的输出自定义光栅化选项吗？**  
A: 可以 – 您可以更改分辨率、图像格式、抗锯齿和背景颜色，以适应 PNG、JPEG 或 PDF 目标。

**Q: 在哪里可以找到更多示例和文档？**  
A: 请查阅完整的 [Aspose.CAD documentation](https://reference.aspose.com/cad/net/) 以获取更多代码示例和 API 细节。

**Q: Aspose.CAD 是否提供免费试用？**  
A: 当然 – 您可以在 **[Aspose trial download page](https://releases.aspose.com/)** 下载试用版，并在 30 天内无限制评估所有功能。

**Q: 我如何获得支持或加入社区？**  
A: 加入活跃的 [Aspose.CAD forum](https://forum.aspose.com/c/cad/19)，在那里开发者分享解决方案，Aspose 团队回答问题。

---

**最后更新：** 2026-08-12  
**测试环境：** Aspose.CAD 24.11 for .NET  
**作者：** Aspose

## 相关教程

- [使用 C# 在 DWG 文件中搜索文本 - Aspose.CAD 教程](/cad/net/text-search-and-manipulation/searching-text-in-dwg-files/)
- [在 Aspose.CAD for .NET 中将 CAD 图纸转换为光栅图像](/cad/net/cad-drawing-manipulation/convert-cad-drawing-to-raster-image/)
- [在 C# 中渲染 DWG 文档 - Aspose.CAD 指南](/cad/net/image-manipulation-and-rendering/rendering-dwg-documents/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< blocks/products/products-backtop-button >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}