---
description: 学习如何使用 Aspose.CAD for .NET 将 DWG 转换为 PNG 并从 DWG 文件中提取 OLE 对象——快速、代码为中心的指南。
linktitle: Exporting OLE Objects from DWG Files
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: 将 DWG 转换为 PNG 并导出 OLE 对象 - Aspose.CAD 教程
url: /zh/net/advanced-export-techniques/exporting-ole-objects-from-dwg/
weight: 12
---

 careful to keep markdown formatting.

Also note "step‑by‑step" contains a non-breaking hyphen; keep same.

Let's translate.

Will produce final answer.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 从 DWG 文件导出 OLE 对象 - Aspose.CAD 教程

## Introduction

如果您需要在提取嵌入的 OLE 对象的同时 **convert DWG to PNG**，那么您来对地方了。Aspose.CAD for .NET 让这两步过程变得简单，只需几行 C# 代码即可实现自动提取和光栅化。在接下来的几分钟里，我们将完整演示工作流，从环境搭建到将每个 DWG 保存为包含提取后 OLE 数据的 PNG。

## Quick Answers
- **What does this tutorial cover?** 使用 Aspose.CAD for .NET 将 DWG 转换为 PNG 并提取 OLE 对象。  
- **Do I need a license?** 开发阶段可使用免费试用版；生产环境需要商业许可证。  
- **Which .NET versions are supported?** .NET Framework 4.5+、.NET Core 3.1+、.NET 5/6+。  
- **Can I process multiple DWG files at once?** 可以——示例代码会遍历文件名数组。  
- **Where can I find more examples?** 请查看下面的官方 Aspose.CAD 文档和论坛链接。

## What is **convert DWG to PNG**?
将 DWG（AutoCAD 图纸）转换为 PNG 图像会对矢量数据进行光栅化，使其易于在网页、报告或其他不原生支持 DWG 的应用中查看或嵌入。当图纸中包含 OLE 对象时，转换过程还能将这些对象提取并保存为独立资源。

## Why extract OLE objects from CAD files?
许多 DWG 图纸会将电子表格、图表或其他 Office 文档以 OLE 对象的形式嵌入。提取这些对象可以重新利用原始数据、实现自动化报表，或在迁移到新格式时保留嵌入信息。

## Prerequisites

- Aspose.CAD for .NET Library: 确保已安装该库。您可以从 [Aspose.CAD for .NET download page](https://releases.aspose.com/cad/net/) 下载。
- Document Directory: 创建一个存放 DWG 文件的目录。将示例代码中的 `"Your Document Directory"` 替换为实际路径。

## Import Namespaces

在 .NET 项目中导入所需的命名空间：

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Step‑by‑Step Guide

### Step 1: Set the Document Directory

```csharp
string MyDir = "Your Document Directory";
```

将 `"Your Document Directory"` 替换为 DWG 文件所在的路径。

### Step 2: List the DWG files you want to process

```csharp
string[] files = new string[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

### Step 3: Configure export options for PNG conversion

```csharp
PngOptions pngOptions = new PngOptions { };
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.VectorRasterizationOptions = rasterizationOptions;
rasterizationOptions.Layouts = new string[] { "Layout1" };
```

您可以调整 `CadRasterizationOptions`（例如 `PageWidth`、`PageHeight`、`BackgroundColor`）以匹配所需的输出分辨率。

### Step 4: Iterate through each DWG and perform the conversion

```csharp
foreach (string file in files)
{
    using (CadImage cadImage = (CadImage)Image.Load(MyDir + file))
    {
        cadImage.Save(MyDir + file + "_out.png", pngOptions);
    }
}
```

在此循环中，库会自动 **extracts OLE objects**，将每个图纸中嵌入的 OLE 对象提取并包含在生成的 PNG 中。如果需要原始 OLE 流，可访问 `cadImage.OleObjects` 集合——这是一种 **how to extract ole** 数据的便捷编程方式。

## Common Issues & Troubleshooting

- **Missing layout name** – 确保示例中指定的布局（如 `"Layout1"`）在源 DWG 中存在，否则光栅化器会回退到默认模型空间。  
- **Large files cause memory pressure** – 如示例所示一次处理一个文件，并使用 `using` 及时释放 `CadImage` 对象。  
- **Unexpected colors** – 如需透明度，请将 `rasterizationOptions.BackgroundColor` 设置为与图纸背景相匹配的颜色。

## Frequently Asked Questions

### Q1: Is Aspose.CAD for .NET suitable for both junior and senior CAD files?
A1: 是的，Aspose.CAD for .NET 功能强大，能够处理各种 CAD 文件，包括 junior 和 senior 变体。

### Q2: Can I customize export options for different layouts?
A2: 当然！正如教程中所示，您可以为不同布局定制导出选项，以满足具体需求。

### Q3: Where can I find detailed documentation for Aspose.CAD for .NET?
A3: 请访问 [Aspose.CAD for .NET documentation](https://reference.aspose.com/cad/net/) 获取深入信息和示例。

### Q4: Is there a free trial available?
A4: 有的，您可以通过免费试用体验 Aspose.CAD for .NET 的功能。访问 [this link](https://releases.aspose.com/) 开始使用。

### Q5: How can I get support or connect with the community?
A5: 如需支持或参与社区交流，请前往 [Aspose.CAD forum](https://forum.aspose.com/c/cad/19)。

### Q6: How do I **extract OLE from CAD** files without converting to PNG?
A6: 加载 DWG 后使用 `CadImage.OleObjects` 集合，遍历每个 `OleObject` 并将其原始数据保存为文件即可。

## Conclusion

现在您已经了解如何使用 Aspose.CAD for .NET **convert DWG to PNG** 的同时无缝 **extracting OLE objects**。此方法可节省时间，消除手动复制粘贴步骤，并能轻松集成到自动化流水线中。欢迎尝试其他光栅格式（JPEG、BMP），或探索 Aspose 提供的丰富 CAD 操作功能。

---

**Last Updated:** 2026-03-13  
**Tested With:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}