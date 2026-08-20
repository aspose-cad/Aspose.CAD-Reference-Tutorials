---
date: 2026-04-06
description: 学习如何使用 Aspose.CAD 在 C# 中将 DWF 转换为 JPG，并了解如何从 DWG 文件中提取 DWF 布局尺寸。
keywords:
- convert dwf to jpg
- how to extract dwf
- convert dwg to jpg
linktitle: 在 C# 中处理 DWG 文件 - 获取 DWF 布局的尺寸
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: 在 C# 中将 DWF 转换为 JPG – 从 DWG 获取 DWF 布局尺寸
url: /zh/net/dwg-file-manipulation/get-size-of-dwf-layout/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 将 DWF 转换为 JPG（C#） – 从 DWG 获取 DWF 布局尺寸

## 介绍

如果您需要 **将 DWF 转换为 JPG** 并且还要确定精确的布局尺寸，那么您来对地方了。在本教程中，我们将通过一个完整的端到端示例，使用 Aspose.CAD for .NET 打开由 DWG 派生的 DWF 文件，读取每个布局的尺寸，并将布局保存为高质量的 JPG 图像。完成后，您不仅会了解如何提取 DWF 布局信息，还会拥有一段可在任何 C# 项目中直接使用的可复用代码片段。

## 快速答案
- **将 “convert DWF to JPG” 是什么意思？** 它指的是将矢量 DWF 布局光栅化为位图 JPEG 图像。  
- **为什么要先读取布局尺寸？** 知道精确的范围可以让您设置正确的页面尺寸，避免图像拉伸或被裁剪。  
- **哪个库负责此操作？** Aspose.CAD for .NET 提供对 DWG、DWF 和光栅图像转换的完整支持。  
- **我需要许可证吗？** 临时许可证可用于评估；生产环境需要正式许可证。  
- **支持哪些 .NET 版本？** .NET Framework 4.5+、.NET Core 3.1+、.NET 5/6/7。

## 什么是 “convert DWF to JPG”，以及它为何重要？

将 DWF（Design Web Format）文件转换为 JPG 可生成可在浏览器中显示、嵌入报告或与没有 CAD 软件的利益相关者共享的便携图像。该转换还使您能够使用标准图像处理工具对图像进行操作（如调整大小、压缩、添加水印）。

## 为什么提取 DWF 布局尺寸？

DWF 文件可以包含多个布局，每个布局都有自己的坐标系和单位（英寸、毫米等）。提取布局尺寸可以让您：

1. 在光栅化时保持原始宽高比。  
2. 为高分辨率输出选择正确的 DPI。  
3. 在无需手动调整的情况下自动批量处理多个布局。

## 前提条件

要顺利完成本教程，请确保已具备以下前提条件：

- Aspose.CAD for .NET：确保已安装 Aspose.CAD for .NET。您可以从 [Aspose.CAD for .NET download page](https://releases.aspose.com/cad/net/) 下载。

拥有该库后，您可以专注于代码，而无需寻找依赖项。

## 导入命名空间

在开始编写代码之前，导入所需的命名空间。这些命名空间提供了处理 CAD 文件、光栅化选项和文件 I/O 所需的类。

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Dwf;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

## 步骤 1：设置环境

创建一个新的 C# 控制台或类库项目，添加对 **Aspose.CAD.dll** 的引用，并确保项目针对兼容的 .NET 版本。

## 步骤 2：定义文件路径（如何提取 DWF）

指定源 DWF 文件所在位置以及生成的 JPG 文件应写入的路径。

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "blocks_and_tables.dwf";
```

> **技巧提示：** 在不同操作系统上使用 `Path.Combine(MyDir, "blocks_and_tables.dwf")` 进行更安全的路径处理。

## 步骤 3：加载 DWF 图像

将 DWF 文件加载到 `Aspose.CAD.Image` 对象中。我们将其强制转换为 `DwfImage`，因为需要访问页面特定属性。

```csharp
using (DwfImage image = (DwfImage)Aspose.CAD.Image.Load(sourceFilePath))
{
    // Code for further steps will go here
}
```

## 步骤 4：遍历页面

一个 DWF 可以包含多个页面（布局）。循环遍历每个页面，以便单独处理。

```csharp
foreach (var page in image.Pages)
{
    // Code for further steps will go here
}
```

## 步骤 5：获取布局信息

在循环内部，获取布局名称。该名称将用于日志记录以及输出 JPG 文件的命名。

```csharp
var layout = page.Name;
System.Console.WriteLine("Layout= " + layout);
```

## 步骤 6：设置 JPG 选项

创建 `JpegOptions` 实例并配置光栅化选项。`Layouts` 属性告诉 Aspose.CAD 渲染哪个布局。

```csharp
using (FileStream fs = new FileStream(MyDir + "layout_" + layout + ".jpg", FileMode.Create))
{
    JpegOptions jpegOptions = new JpegOptions();
    CadRasterizationOptions options = new CadRasterizationOptions();
    options.Layouts = new string[] { layout };
    // Code for further steps will go here
}
```

## 步骤 7：确定页面尺寸（convert dwg to jpg）

计算布局在其原始单位下的宽度和高度。此信息对于正确设置光栅页面尺寸至关重要。

```csharp
double sizeExtX = page.MaxPoint.X - page.MinPoint.X;
double sizeExtY = page.MaxPoint.Y - page.MinPoint.Y;
// Code for further steps will go here
```

## 步骤 8：设置页面尺寸

使用 Aspose.CAD 提供的辅助方法将原始单位（英寸或毫米）转换为像素。如果单位类型不属于上述两者，则回退使用原始数值。

```csharp
if (page.UnitType == UnitType.Inch)
{
    options.PageHeight = CommonHelper.INtoPixels(sizeExtY, CommonHelper.DPI);
    options.PageWidth = CommonHelper.INtoPixels(sizeExtX, CommonHelper.DPI);
}
else if (page.UnitType == UnitType.Millimeter)
{
    options.PageHeight = CommonHelper.MMtoPixels(sizeExtY, CommonHelper.DPI);
    options.PageWidth = CommonHelper.MMtoPixels(sizeExtX, CommonHelper.DPI);
}
else
{
    options.PageHeight = (float)sizeExtY;
    options.PageWidth = (float)sizeExtX;
}
```

## 步骤 9：保存 JPG 文件

最后，将光栅化选项绑定到 JPEG 选项并将图像保存到磁盘。

```csharp
jpegOptions.VectorRasterizationOptions = options;
image.Save(fs, jpegOptions);
}
```

循环结束后，您将拥有每个布局对应的 JPG 文件，尺寸完全匹配原始 DWF 的尺寸。

## 常见问题及解决方案

| 症状 | 可能原因 | 解决办法 |
|---------|--------------|-----|
| 空的 JPG 输出 | `options.Layouts` 未正确设置 | 验证布局名称与 `page.Name` 匹配。 |
| 图像失真 | DPI 转换错误 | 在转换前使用 `CommonHelper.DPI = 300`（或您目标的 DPI）。 |
| 文件未找到 | `MyDir` 路径不正确 | 使用绝对路径或 `Path.Combine`。 |
| 许可证异常 | 未加载许可证 | 在调用 `Image.Load` 之前加载临时或永久许可证。 |

## 常见问答

### Q1：Aspose.CAD 是否兼容最新的 DWG 文件格式？

A1：Aspose.CAD 支持多种 DWG 文件格式，包括最新版本。请参阅 [documentation](https://reference.aspose.com/cad/net/) 获取具体兼容性细节。

### Q2：我可以在商业和个人项目中使用 Aspose.CAD 吗？

A2：是的，Aspose.CAD 为商业和个人使用提供灵活的授权选项。请访问 [purchase page](https://purchase.aspose.com/buy) 获取更多详情。

### Q3：如何获取 Aspose.CAD 的临时许可证？

A3：您可以从 [here](https://purchase.aspose.com/temporary-license/) 获取临时许可证用于评估。

### Q4：在哪里可以找到 Aspose.CAD 的支持？

A4：如有任何疑问或需要帮助，请访问 [Aspose.CAD forum](https://forum.aspose.com/c/cad/19)。

### Q5：Aspose.CAD 是否提供免费试用？

A5：是的，您可以在 [here](https://releases.aspose.com/) 获取 Aspose.CAD 的免费试用版。

### Q6：如何在不先提取 DWF 的情况下直接将 DWG 文件转换为 JPG？

A6：您可以使用 `Aspose.CAD.Image.Load` 加载 DWG 文件并使用相同的光栅化工作流；只需将 `options.Layouts` 设置为 DWG 中所需的布局名称。

### Q7：转换是否保留矢量质量？

A7：一旦光栅化为 JPG，图像即为位图，矢量可伸缩性将丢失。若需无损缩放，建议导出为 PNG 或 SVG。

---

**最后更新：** 2026-04-06  
**测试环境：** Aspose.CAD 24.11 for .NET  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}