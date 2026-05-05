---
date: 2026-03-21
description: 学习如何使用 Aspose.CAD for .NET 从 DWG 创建 PDF 并将 DGN 导出为 DWG 的一部分。本指南还展示了如何将
  DWG 转换为 PDF 并设置 PDF 选项。
linktitle: Export DGN as Part of DWG
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: 从 DWG 创建 PDF 并将 DGN 导出为 DWG 的一部分 – Aspose.CAD for .NET
url: /zh/net/cad-export-formats/export-dgn-as-part-of-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 从 DWG 创建 PDF 并将 DGN 导出为 DWG 的一部分 – Aspose.CAD for .NET

## 介绍

如果您需要 **从 DWG 创建 PDF** 并且在 DWG 中嵌入 DGN 设计，Aspose.CAD for .NET 可以让这一步骤变得简单直观。在本教程中，我们将完整演示工作流：加载 DWG、定位嵌入的 DGN underlay、配置光栅化选项，最后将结果导出为 PDF 文档。无论您是在构建批量转换工具、报表引擎，还是 CAD‑BIM 集成服务，下面的步骤都能为您提供坚实、可投入生产的基础。

## 快速答疑
- **哪个库负责 DWG → PDF 转换？** Aspose.CAD for .NET  
- **创建 PDF 时能导出 DGN underlay 吗？** 可以 – 通过 `CadDgnUnderlay` 访问该 underlay。  
- **哪个方法设置 PDF 选项？** `PdfOptions` 与 `CadRasterizationOptions` 配合使用。  
- **商业使用是否需要许可证？** 需要，有效的 Aspose.CAD 许可证是必需的。  
- **支持的 .NET 版本？** .NET Framework 4.5+、.NET Core 3.1+、.NET 5/6/7。

## 什么是 “从 DWG 创建 PDF”？

从 DWG 文件创建 PDF 意味着将矢量图形渲染为光栅或矢量 PDF 文档。此过程便于向没有 CAD 软件的利益相关者共享图纸、归档或生成可打印的报告。Aspose.CAD 通过解析 DWG 实体并通过 `PdfOptions` 提供细粒度的输出控制，简化了这一任务。

## 为什么要将 DGN 导出为 DWG 的一部分？

DGN underlay 通常代表来自 MicroStation 项目的参考几何体。将 DGN 与 DWG 一起导出可以保留原始设计上下文，确保下游使用者看到完整的图纸集合。这在 DWG 与 DGN 文件共存的多学科项目中尤为重要。

## 前置条件

- **Aspose.CAD for .NET** – 在此处下载 [here](https://releases.aspose.com/cad/net/)。  
- **开发环境** – Visual Studio（任意近期版本）或您偏好的 .NET IDE。  
- **基础 C# 知识** – 您应熟悉 C# 语法和 .NET 项目结构。

## 导入命名空间

在 C# 源文件顶部添加所需的 `using` 指令：

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## 步骤指南

### 步骤 1：定义文件路径

设置输入 DWG 文件和输出 PDF 的名称。

```csharp
// Input and Output file paths
string fileName = "BlockRefDgn.dwg";
string outPath = fileName + ".pdf";
```

### 步骤 2：创建 `PdfOptions` 实例（设置 PDF 选项）

`PdfOptions` 让您可以控制 PDF 的生成方式，例如页面大小、压缩和元数据。

```csharp
// Create an instance of PdfOptions class for exporting DWG to PDF
PdfOptions exportOptions = new PdfOptions();
```

### 步骤 3：加载 DWG 文件

将 DWG 加载为 `CadImage`，以便检查其实体。

```csharp
// Load the existing DWG file as an image and convert it to CadImage type
using (CadImage cadImage = (CadImage)Image.Load(fileName))
```

### 步骤 4：遍历实体

遍历图纸中的每个实体，以定位 DGN underlay。

```csharp
// Iterate through each entity inside the DWG file
foreach (CadBaseEntity baseEntity in cadImage.Entities)
```

### 步骤 5：检查实体类型（如何导出 dgn）

判断当前实体是否为 DGN underlay。

```csharp
// Check if the entity is an image definition
if (baseEntity.TypeName == CadEntityTypeName.DGNUNDERLAY)
```

### 步骤 6：获取 Underlay 路径

获取 DGN 文件的外部引用路径。

```csharp
// If it's an image definition, get the external reference to the object
CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
Console.WriteLine(dgnFile.UnderlayPath);
```

### 步骤 7：定义光栅化选项（将 dwg 转换为 pdf）

配置在放入 PDF 之前 DWG 的光栅化方式。

```csharp
// Define settings for CadRasterizationOptions object
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

### 步骤 8：导出 DWG 为 PDF

最后，将渲染后的图像保存为 PDF 文件。

```csharp
// Export the DWG to PDF by calling Save method
cadImage.Save(outPath, exportOptions);
```

## 常见问题及解决方案

| 问题 | 原因 | 解决办法 |
|------|------|----------|
| **`Image.Load` 抛出 “File not found”** | 路径不正确或文件缺失。 | 使用绝对路径或确保 DWG 已复制到输出文件夹。 |
| **Underlay 路径为空** | DGN underlay 未嵌入或引用断开。 | 验证 DWG 实际包含 DGN underlay，且外部 DGN 文件可访问。 |
| **PDF 输出为空白** | 光栅化选项设置了零尺寸。 | 调整 `PageWidth`/`PageHeight` 或将 `NoScaling = false`。 |
| **许可证异常** | 未使用有效的 Aspose.CAD 许可证运行。 | 在加载图像前应用许可证：`License lic = new License(); lic.SetLicense("Aspose.CAD.lic");` |

## 常见问答

### Q1: 我可以在商业项目中使用 Aspose.CAD for .NET 吗？
A1: 可以。请访问 [here](https://purchase.aspose.com/buy) 了解授权选项。

### Q2: 处理的 DWG 文件大小是否有限制？
A2: Aspose.CAD 支持处理大型 DWG 文件，但受硬件限制影响。

### Q3: 有试用版吗？
A3: 有，您可以在此获取免费试用 [here](https://releases.aspose.com/)。  

### Q4: 如何获取临时许可证？
A4: 临时许可证可在此获取 [here](https://purchase.aspose.com/temporary-license/)。  

### Q5: 如果遇到问题，我可以在哪里寻求帮助？
A5: 您可以访问 Aspose.CAD 论坛 [here](https://forum.aspose.com/c/cad/19) 获取支持。

**问：如何设置额外的 PDF 元数据（作者、标题等）？**  
答：在调用 `Save` 之前使用 `exportOptions.Metadata` 属性进行设置。

**问：能否将多个布局导出为独立的 PDF 页面？**  
答：可以 – 在 `CadRasterizationOptions` 中设置 `Layouts = new string[] { "Layout1", "Layout2" }`。

**问：Aspose.CAD 是否支持将 DWG 转换为其他图像格式？**  
答：当然。您可以使用相应的 `Image.Save` 重载导出为 PNG、JPEG、SVG 等格式。

---

**最后更新：** 2026-03-21  
**测试环境：** Aspose.CAD 24.11 for .NET  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}