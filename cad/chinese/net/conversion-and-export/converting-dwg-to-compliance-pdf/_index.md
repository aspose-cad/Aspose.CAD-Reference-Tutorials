---
date: 2026-03-31
description: 使用 Aspose.CAD for .NET 将 DWG 转换为 PDF，支持 .NET Core PDF 转换。请按照我们的分步指南操作。
keywords:
- convert dwg to pdf
- net core pdf conversion
- aspose cad compliance pdf
- dwg to pdf conversion .net
- cad file format conversion
linktitle: 将 DWG 转换为合规 PDF
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: 如何使用 Aspose.CAD for .NET 将 DWG 转换为 PDF（合规）
url: /zh/net/conversion-and-export/converting-dwg-to-compliance-pdf/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 将 dwg 转换为 pdf – Aspose.CAD 教程

## 介绍

欢迎！在本教程中，您将学习使用 Aspose.CAD .NET 库 **将 DWG 转换为 PDF**。无论您是构建桌面实用程序、Web 服务，还是必须生成符合 PDF/A‑1a 或 PDF/A‑1b 标准的 .NET Core 应用程序，本指南都会一步步带您完成——从加载 DWG 文件到保存符合标准的 PDF。  

在本指南结束时，您将拥有一段可直接放入任何 .NET 项目的即用代码片段。

## 快速答案
- **需要哪个库？** Aspose.CAD for .NET (supports .NET Framework and .NET Core).  
- **覆盖哪些 PDF 合规级别？** PDF/A‑1a and PDF/A‑1b.  
- **测试是否需要许可证？** A free trial works perfectly for development; a commercial license is required for production.  
- **可以在 .NET Core 上运行吗？** Yes – the same code runs on .NET Core, .NET 5/6+.  
- **典型的实现时间是多少？** About 10 minutes for a basic conversion.

## 什么是“将 DWG 转换为 PDF”？

DWG 是 AutoCAD 绘图的原生文件格式，而 PDF 是一种通用的可查看文档格式。将 DWG 转换为 PDF 可让您与没有 CAD 软件的利益相关者共享图纸，PDF/A 合规性确保长期归档和法律可接受性。

## 为什么在 .NET Core PDF 转换中使用 Aspose.CAD？

- **零安装 CAD 引擎** – no AutoCAD or third‑party binaries required.  
- **完整的 .NET Core 兼容性** – write once, run anywhere.  
- **内置 PDF/A 合规性** – generate archival‑ready PDFs with a single property change.  
- **高保真光栅化** – preserve line weights, colors, and layers.

## 前提条件

- **Aspose.CAD for .NET** – download it [此处](https://releases.aspose.com/cad/net/).  
- 一个 **.NET 开发环境**（Visual Studio 2022、带 C# 扩展的 VS Code，或您喜欢的任何 IDE）。  
- 一个 **示例 DWG 文件**，您想要转换的文件（本教程使用 `Bottom_plate.dwg`）。

## 导入命名空间

在您的 .NET 项目中，导入必要的命名空间以使用 Aspose.CAD 功能。

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
```

现在，让我们将转换过程分解为清晰的编号步骤。

## 步骤 1：加载 DWG 文件

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";

Aspose.CAD.Image cadImage = Aspose.CAD.Image.Load(sourceFilePath);
```

*说明:*  
`Image.Load` 会自动检测 DWG 格式并创建一个内存中的表示 (`cadImage`)，我们随后可以对其进行光栅化或导出。

## 步骤 2：设置光栅化选项

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions
{
    BackgroundColor = Aspose.CAD.Color.White,
    PageWidth = 1600,
    PageHeight = 1600
};
```

*原因:*  
光栅化将矢量 CAD 数据转换为 PDF 可嵌入的位图。调整 `PageWidth`/`PageHeight` 可控制最终 PDF 的分辨率。

## 步骤 3：创建 PDF 选项

```csharp
PdfOptions pdfOptions = new PdfOptions
{
    VectorRasterizationOptions = rasterizationOptions,
    CorePdfOptions = new PdfDocumentOptions { Compliance = PdfCompliance.PdfA1a }
};
```

*提示:*  
稍后将 `PdfCompliance` 更改为 `PdfA1b`，即可在不重新编写光栅化设置的情况下获得略有不同的 PDF/A 级别。

## 步骤 4：保存为 PDF（A1a 合规）

```csharp
cadImage.Save(MyDir + "PDFA1_A.pdf", pdfOptions);
```

*结果:*  
`PDFA1_A.pdf` 是符合 PDF/A‑1a 的文件，适用于严格的归档要求。

## 步骤 5：保存为 PDF（A1b 合规）

```csharp
pdfOptions.CorePdfOptions.Compliance = PdfCompliance.PdfA1b;
cadImage.Save(MyDir + "PDFA1_B.pdf", pdfOptions);
```

*结果:*  
`PDFA1_B.pdf` 符合 PDF/A‑1b 合规性，虽然稍宽松，但仍被广泛接受用于归档。

## 常见问题及解决方案

| 问题 | 原因 | 解决方案 |
|-------|-------|-----|
| **空白 PDF 输出** | 未设置光栅化选项（例如，背景颜色透明） | Set `BackgroundColor = Aspose.CAD.Color.White` or another visible color. |
| **大型 DWG 导致内存不足** | 将极大的图纸加载到内存中 | Use `CadRasterizationOptions` with lower `PageWidth`/`PageHeight` or process the file in chunks if possible. |
| **合规性错误** | 使用缺少 PDF/A 支持的旧版 Aspose.CAD | Upgrade to the latest Aspose.CAD release (checked on the download page). |

## 常见问题 (新)

**问：我可以使用 Aspose.CAD 将其他 CAD 格式转换为合规 PDF 吗？**  
答：是的，Aspose.CAD 支持多种格式（DWG、DXF、DGN 等），并且可以将它们导出为 PDF/A。

**问：Aspose.CAD 与 .NET Core 兼容吗？**  
答：完全兼容。相同的 API 可在 .NET Framework、.NET Core 和 .NET 5/6+ 上运行。

**问：Aspose.CAD 有哪些授权选项？**  
答：有的，您可以在[此处](https://purchase.aspose.com/buy)查看授权选项。

**问：是否提供免费试用？**  
答：有的，您可以在[此处](https://releases.aspose.com/)获取免费试用。

**问：在哪里可以获得 Aspose.CAD 的支持？**  
答：请访问 [Aspose.CAD 论坛](https://forum.aspose.com/c/cad/19) 获取任何支持相关的查询。

## 结论

您现在已经看到一个完整的、可投入生产的示例，展示了如何使用 Aspose.CAD for .NET **将 DWG 转换为 PDF** 并实现 PDF/A 合规性。相同的方法同样适用于 .NET Core 项目，为桌面、Web 或基于云的应用提供灵活的解决方案。欢迎尝试不同的光栅化设置、页面尺寸或合规级别，以满足您的具体需求。

---

**最后更新：** 2026-03-31  
**测试环境：** Aspose.CAD 24.12 for .NET  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}