---
date: 2026-03-24
description: 了解如何使用 Aspose.CAD for .NET 将 dgn 转换为 png 并将 cad 保存为 jpeg——CAD 转图像转换的快速指南。
linktitle: Export DGN to Raster Image
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: 如何在 Aspose.CAD for .NET 中将 DGN 转换为 PNG
url: /zh/net/cad-export-formats/export-dgn-to-raster-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 将 DGN 转换为 PNG（使用 Aspose.CAD for .NET）

在现代 .NET 开发中，**convert dgn to png** 是在网页上显示 CAD 图纸或在报告中嵌入图纸时的常见需求。Aspose.CAD for .NET 让此转换变得简单，只需几行代码即可将 DGN 文件转换为高质量的光栅图像。本文将从项目设置到保存最终 PNG（或 JPEG）文件，完整演示整个过程。

## 快速回答
- **可以使用 Aspose.CAD 将 DGN 转换为 PNG 吗？** 可以——只需配置光栅化选项并选择 PNG 或 JPEG 输出。  
- **生产环境需要许可证吗？** 非试用部署必须使用有效的 Aspose.CAD 许可证。  
- **支持哪些 .NET 版本？** .NET Framework 4.6+、.NET Core 3.1+、.NET 5/6/7。  
- **有哪些图像格式可用？** PNG、JPEG、BMP、GIF、TIFF 等。  
- **是否需要异常处理？** 必须——请使用 try/catch 捕获文件访问等异常。

## 什么是 “convert dgn to png”？
将 DGN（MicroStation）文件转换为 PNG，即将矢量 CAD 数据光栅化为基于像素的图像。这对于生成预览、在 HTML 邮件中嵌入图纸或为文档管理系统创建缩略图非常有用。

## 为什么选择 Aspose.CAD 进行 CAD 到图像的转换？
- **无外部依赖** —— 完全在托管代码中运行。  
- **高保真** —— 保留线宽、图层和颜色。  
- **灵活的输出** —— 只需更改一个选项即可在 PNG、JPEG、BMP 等之间切换。  
- **性能优化** —— 即使是大型图纸，光栅化也非常快速。

## 前置条件

在开始之前，请确保您已：

- 在项目中安装 **Aspose.CAD for .NET**。可从[官方网站](https://reference.aspose.com/cad/net/)下载。  
- 将示例 DGN 文件（例如 `Nikon_D90_Camera.dgn`）放置在已知目录下。

## 导入命名空间

首先添加所需的 `using` 语句，以便访问 Aspose.CAD 类。

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## 步骤 1：加载 DGN 文件

将源 DGN 加载到 `CadImage` 对象中。该对象在内存中表示 CAD 图纸，是后续光栅化的来源。

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Your code for further processing goes here
}
```

## 步骤 2：定义光栅化选项

配置 CAD 图纸的光栅化方式。可以在此控制图像尺寸、缩放比例以及背景颜色等。

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 600;
rasterizationOptions.PageHeight = 300;
rasterizationOptions.NoScaling = true;
rasterizationOptions.AutomaticLayoutsScaling = false;
```

## 步骤 3：选择输出格式（PNG 或 JPEG）

虽然本教程侧重于 PNG，您也可以 **save cad as jpeg**。创建相应的图像选项对象并关联光栅化设置。

```csharp
ImageOptionsBase options = new JpegOptions();   // Change to PngOptions() for PNG output
options.VectorRasterizationOptions = rasterizationOptions;
```

> **专业提示：** 若要生成 PNG 文件，请将 `new JpegOptions()` 替换为 `new PngOptions()`。

## 步骤 4：保存光栅图像

最后，对 `CadImage` 实例调用 `Save`，提供目标文件名和前面配置的选项对象。

```csharp
cadImage.Save(MyDir + "ExportDGNToRasterImage_out.jpg", options);
```

如果使用 `PngOptions`，文件将保存为 `ExportDGNToRasterImage_out.png`。

## 常见问题及解决方案

| 问题 | 原因 | 解决方案 |
|------|------|----------|
| **输出图像为空白** | `NoScaling` 设置不当或未选择布局 | 将 `AutomaticLayoutsScaling = true`，或指定所需布局。 |
| **大文件导致内存不足** | 未使用流式加载直接加载巨型 DGN | 使用 `Image.Load(sourceFilePath, new LoadOptions { LoadOnDemand = true })`。 |
| **不支持的 DGN 版本** | 旧版 MicroStation 文件 | 确保使用支持旧格式的最新 Aspose.CAD 版本。 |

## 常见问答

**Q: 能否将 DGN 导出为 JPEG 之外的其他格式？**  
A: 可以，Aspose.CAD for .NET 支持 PNG、BMP、GIF、TIFF 等，只需更换对应的选项类（例如 `new PngOptions()`）。

**Q: 转换过程中应如何处理异常？**  
A: 将转换代码放在 `try/catch` 块中，并记录 `Aspose.CAD.CadException` 以获取详细错误信息。

**Q: 是否提供 Aspose.CAD for .NET 的试用版？**  
A: 有，您可以使用免费试用版。更多信息请访问[此处](https://releases.aspose.com/)。

**Q: 在哪里可以获取帮助或讨论 Aspose.CAD for .NET 的相关问题？**  
A: 前往[Aspose.CAD 论坛](https://forum.aspose.com/c/cad/19)获取社区支持和讨论。

**Q: 如何获取 Aspose.CAD for .NET 的临时许可证？**  
A: 访问[此链接](https://purchase.aspose.com/temporary-license/)获取开发所需的临时许可证。

## 结论

现在您已经掌握了使用 Aspose.CAD for .NET **convert dgn to png**（或 JPEG）的完整流程。通过调整光栅化选项并切换图像选项类，您可以根据项目需求定制输出。欢迎尝试不同的页面尺寸、DPI 设置和文件格式，以获得最适合您应用的光栅图像。

---

**最后更新：** 2026-03-24  
**测试环境：** Aspose.CAD 24.11 for .NET  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}