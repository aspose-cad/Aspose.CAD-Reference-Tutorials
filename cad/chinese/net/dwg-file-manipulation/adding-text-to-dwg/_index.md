---
date: 2026-04-06
description: 学习如何使用 C# 和 Aspose.CAD 将 DWG 转换为 PDF 并添加自定义文本。本分步指南涵盖从 DWG 生成 PDF、插入文本实体以及更改
  DWG 文本字体。
keywords:
- convert dwg to pdf
- generate pdf from dwg
- insert text entity
- change dwg text font
- aspose cad dwg pdf
linktitle: 在 C# 中向 DWG 文件添加文本
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: 在 C# 中将 DWG 转换为 PDF 并添加文本 – Aspose.CAD 教程
url: /zh/net/dwg-file-manipulation/adding-text-to-dwg/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 将 DWG 转换为 PDF 并在 C# 中添加文本 – Aspose.CAD 教程

## 介绍

在 CAD 与 .NET 开发快速发展的世界中，**将 DWG 转换为 PDF** 并插入自定义注释是常见需求。无论是为客户生成可打印图纸，还是直接在 DWG 中嵌入动态备注，Aspose.CAD 都能让工作变得简单。在本教程中，你将学习如何**将 DWG 转换为 PDF**、**添加文本实体**，以及使用 C# **更改 DWG 文本字体**。

## 快速答案
- **哪个库最适合 DWG‑to‑PDF 转换？** Aspose.CAD for .NET  
- **转换时可以添加自定义文本吗？** 可以 – 创建 `CadText` 实体并在保存前添加。  
- **生产环境需要许可证吗？** 需要商业许可证；提供免费试用。  
- **支持哪些 .NET 版本？** .NET Framework 4.5+、.NET Core 3.1+、.NET 5/6+。  
- **可以更改文本字体吗？** 可以，调整 `CadText` 的 `StyleType`、`TextHeight` 等属性。

## 什么是“将 dwg 转换为 pdf”？

将 DWG 文件转换为 PDF 会把基于矢量的 CAD 图形转化为一种广泛共享、与设备无关的文档。PDF 保留原始几何形状和图层，同时允许嵌入注释、文本或其他元数据。Aspose.CAD 自动处理光栅化和矢量渲染，无需在服务器上安装任何第三方 CAD 软件。

## 为什么在转换前向 DWG 添加文本？

直接在 DWG 中嵌入文本可以完全控制其位置、样式和图层分配。文件随后转换为 PDF 时，文本会准确出现在你设定的位置，保持设计意图，省去在 PDF 编辑器中后期处理的步骤。

## 先决条件

在开始之前，请确保已具备以下条件：

- **Aspose.CAD Library** – 从 [download link](https://releases.aspose.com/cad/net/) 下载。  
- **可用的 .NET 环境**（Visual Studio 2022、.NET 6 或任何兼容版本）。  
- **用于存放测试文件的文件夹** – 本文中统一称为 `MyDir`。

现在，让我们一步步完成整个过程。

## 导入命名空间

添加所需的 `using` 语句，以便访问 Aspose.CAD 类。

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
using Aspose.CAD.ImageOptions;
```

## 步骤 1：加载 DWG 文件

将源 DWG 文件加载到 `Image` 对象中。该对象让你能够访问底层的 CAD 实体。

```csharp
string dwgPathToFile = MyDir + "SimpleEntites.dwg";
using (Image image = Image.Load(dwgPathToFile))
{
    // Subsequent steps will be performed inside this block
}
```

## 步骤 2：创建 CadText 对象（插入文本实体）

`CadText` 类表示 DWG 中的一行文本。这里我们设置其样式、值、颜色、图层和位置。通过调整 `StyleType` 或 `TextHeight` 可以 **更改 DWG 文本字体**。

```csharp
CadText cadText = new CadText();
cadText.StyleType = "Standard";          // Font/style – change to alter DWG text font
cadText.DefaultValue = "Some custom text";
cadText.ColorId = 256;                    // 256 = ByLayer (you can use a specific ACI color)
cadText.LayerName = "0";
cadText.FirstAlignment.X = 47.90;
cadText.FirstAlignment.Y = 5.56;
cadText.TextHeight = 0.8;                 // Height influences visual size
cadText.ScaleX = 0.0;
```

## 步骤 3：将文本实体添加到模型空间

DWG 的模型空间容纳大多数绘图实体。将我们的 `CadText` 添加到 `*Model_Space` 块后，文本就成为图纸的一部分。

```csharp
CadImage cadImage = (CadImage)image;
cadImage.BlockEntities["*Model_Space"].AddEntity(cadText);
```

## 步骤 4：配置 PDF 选项（从 DWG 生成 PDF）

设置光栅化选项，以控制 DWG 渲染为 PDF 的方式。你可以调整页面尺寸、绘制类型和布局等参数。

```csharp
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.VectorRasterizationOptions = cadRasterizationOptions;
cadRasterizationOptions.DrawType = CadDrawTypeMode.UseObjectColor;
cadRasterizationOptions.PageHeight = 1600;
cadRasterizationOptions.PageWidth = 1600;
cadRasterizationOptions.Layouts = new string[] { "Model" };
```

## 步骤 5：将修改后的 DWG 保存为 PDF

最后，导出修改后的图纸。生成的 PDF 将包含新插入的文本。

```csharp
image.Save(MyDir + "SimpleEntites_generated.pdf", pdfOptions);
```

> **专业提示：** 如果需要更高分辨率的 PDF，请按比例增加 `PageHeight` 和 `PageWidth`。

## 常见问题与解决方案

| 问题 | 原因 | 解决方案 |
|------|------|----------|
| 文本未出现在 PDF 中 | 图层或颜色 ID 错误 | 确保 `LayerName` 存在且 `ColorId` 设置为可见颜色（例如 7 表示白色）。 |
| 文本位置错误 | 对齐坐标不正确 | 验证 `FirstAlignment.X/Y` 值相对于图纸单位是否正确。 |
| PDF 空白 | 未设置光栅化选项 | 将 `DrawType` 设置为 `UseObjectColor` 或 `UseObjectLineWeight`。 |

## 常见问题（已存在）

### Q1: Aspose.CAD 是否兼容所有版本的 DWG 文件？

A1: Aspose.CAD 支持广泛的 DWG 文件版本，确保与各种 CAD 软件的兼容性。

### Q2: 能否使用 Aspose.CAD 向单个 DWG 文件添加多个文本实体？

A2: 可以，通过重复本教程中描述的步骤向 DWG 文件添加多个文本实体。

### Q3: 如何在 Aspose.CAD 中更改文本字体和样式？

A3: 在将 `CadText` 对象添加到 DWG 文件之前，修改其相应属性即可更改字体和样式。

### Q4: 在商业项目中使用 Aspose.CAD 有哪些许可注意事项？

A5: 是的，请确保遵守 Aspose.CAD 的许可条款。详情请参阅 [Aspose.CAD Purchase](https://purchase.aspose.com/buy)。

### Q5: 在哪里可以寻求帮助或讨论 Aspose.CAD 相关问题？

A5: 访问 [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) 与社区交流并获取支持。

## 附加常见问题

**Q: 如何在不添加文本的情况下直接从 DWG 生成 PDF？**  
A: 跳过 `CadText` 创建步骤，直接配置 `PdfOptions` 并调用 `image.Save(...)`。

**Q: 能否以编程方式更改文本颜色？**  
A: 可以，将 `cadText.ColorId` 设置为特定的 ACI 颜色编号（例如 1 表示红色）。

**Q: 是否可以插入多行文本？**  
A: 使用 `CadMText` 来处理多行文本块；使用方式与 `CadText` 类似。

**Q: Aspose.CAD 是否支持批量转换多个 DWG 文件？**  
A: 完全支持 – 遍历 DWG 文件目录，按相同步骤处理并将每个文件保存为 PDF。

## 结论

现在，你已经掌握了一套完整的、可投入生产的工作流，能够使用 C# 和 Aspose.CAD **将 DWG 转换为 PDF**、**添加自定义文本**，并 **自定义文本外观**。此技术非常适合自动化图纸生成、报告流水线或任何需要即时丰富 CAD 文件的场景。

---

**最后更新：** 2026-04-06  
**测试环境：** Aspose.CAD 24.11 for .NET  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}