---
date: 2026-04-03
description: 学习如何在 C# 中使用 Aspose.CAD 设置视口并将 DWG 转换为 PDF。本 DWG 转 PDF 教程展示了带坐标的精确导出。
keywords:
- how to set viewport
- dwg to pdf tutorial
- convert dwg to pdf c#
linktitle: 在 C# 中将 DWG 转换为带坐标的 PDF
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: 如何在 C# 中将 DWG 转换为带坐标的 PDF 时设置视口 - Aspose.CAD 教程
url: /zh/net/conversion-and-export/converting-dwg-to-pdf-with-coordinates/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 C# 中使用坐标将 DWG 转换为 PDF - Aspose.CAD 教程

## 介绍

欢迎阅读本综合教程，介绍如何在使用 Aspose.CAD for .NET 将 DWG 文件转换为带指定坐标的 PDF 时 **如何设置视口**。通过控制视口，您可以获得像素级精确的 PDF，完全匹配所需区域——非常适用于施工图纸、平面图预览或任何 BIM 工作流。

## 快速答案
- **“set viewport” 是什么意思？** 它定义了光栅化过程中 CAD 图形的可见区域和缩放比例。  
- **哪个库负责转换？** Aspose.CAD for .NET。  
- **我需要许可证吗？** 免费试用可用于评估；生产环境需要商业许可证。  
- **支持的平台？** Windows、Linux 和 macOS，使用 .NET 5/6/7 或 .NET Framework 4.6+。  
- **典型实现时间？** 基本转换大约需要 10‑15 分钟。

## 先决条件

在开始之前，请确保您具备以下先决条件：

- **Aspose.CAD 库** – 下载并安装适用于 .NET 的 Aspose.CAD 库。您可以在 [此处](https://releases.aspose.com/cad/net/) 找到该库。  
- **开发环境** – Visual Studio、Rider 或任何支持 .NET 开发的 IDE。  
- **DWG 文件** – 准备好用于转换的 DWG 文件。您可以使用提供的示例文件或自定义的 DWG 文件。

## 如何设置视口以实现精确的 PDF 导出

设置视口是核心步骤，可让您定义要渲染的图形的精确区域。下面的代码中，我们创建一个新的 `CadVportTableObject`，使用左上坐标定位，并计算宽度、高度和宽高比。这就是 **如何设置视口** 的实现，驱动后续的转换。

## 导入命名空间

在您的 C# 项目中，导入必要的命名空间：

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadParameters;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.ImageOptions;
```

让我们逐步拆解代码，以便更好地理解：

## 步骤 1：定义文档目录

```csharp
string MyDir = "Your Document Directory";
```

## 步骤 2：设置源 DWG 文件路径

```csharp
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";
```

## 步骤 3：加载 DWG 文件并配置光栅化选项

```csharp
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
    rasterizationOptions.Layouts = new string[] { "Model" };
    rasterizationOptions.NoScaling = true;
```

## 步骤 4：定义坐标和视口  

在这里，我们实际 **设置视口**（如何设置视口），通过指定左上角、宽度和高度来确定要导出的区域。

```csharp
    Point topLeft = new Point(500, 1000);
    double width = 3108;
    double height = 2489;

    CadVportTableObject newView = new CadVportTableObject();
    newView.Name = new CadStringParameter();
    newView.Name.Init("*Active");
    newView.CenterPoint.X = topLeft.X + width / 2f;
    newView.CenterPoint.Y = topLeft.Y - height / 2f;
    newView.ViewHeight.Value = height;
    newView.ViewAspectRatio.Value = width / height;
```

## 步骤 5：应用视口设置

```csharp
    for (int i = 0; i < cadImage.ViewPorts.Count; i++)
    {
        CadVportTableObject currentView = (CadVportTableObject)(cadImage.ViewPorts[i]);
        if (cadImage.ViewPorts.Count == 1 || string.Equals(currentView.Name.Value.ToLowerInvariant(), "*active"))
        {
            cadImage.ViewPorts[i] = newView;
            break;
        }
    }
```

## 步骤 6：配置 PDF 选项并导出  

现在我们将所有内容结合起来，使用刚刚准备的光栅化选项 **将 DWG 转换为 PDF**。

```csharp
    Aspose.CAD.ImageOptions.PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions();
    pdfOptions.VectorRasterizationOptions = rasterizationOptions;

    MyDir = MyDir + "ConvertDWGToPDFBySupplyingCoordinates_out.pdf";
    cadImage.Save(MyDir, pdfOptions);
}
```

## 步骤 7：显示成功消息

```csharp
Console.WriteLine("\nThe DWG file exported successfully to PDF.\nFile saved at " + MyDir);
```

## 常见使用场景

- **施工文档** – 生成特定平面图部分的可打印 PDF。  
- **BIM 协调** – 仅导出感兴趣的区域以进行冲突检测。  
- **客户演示** – 提供所选房间或立面的简洁 PDF，而不暴露整个图纸。

## 结论

恭喜！您已成功使用 Aspose.CAD for .NET **将 DWG 转换为 PDF**，并通过精确坐标学习了 **如何设置视口**。本 **dwg to pdf 教程** 演示了如何 **从 dwg 创建 pdf** 和 **将 dwg 导出为 pdf c#**，同时对输出区域保持完整控制。

## 常见问题

### Q1：我可以将 Aspose.CAD 与其他 CAD 文件格式一起使用吗？

A1：是的，Aspose.CAD 支持多种 CAD 格式，包括 DWG、DXF、DWF 等。

### Q2：我该如何处理转换过程中的错误？

A2：使用 try‑catch 块实现错误处理机制，以捕获和管理异常。

### Q3：Aspose.CAD 是否适用于 Windows 和 Linux 环境？

A3：是的，Aspose.CAD 兼容 Windows 和 Linux 平台。

### Q4：我可以进一步自定义 PDF 输出吗？

A4：当然！探索 Aspose.CAD 提供的丰富选项，以根据您的具体需求定制 PDF 输出。

### Q5：我在哪里可以找到更多支持或社区讨论？

A5：访问 [Aspose.CAD 论坛](https://forum.aspose.com/c/cad/19) 获取社区支持和讨论。

## 其他常见问题

**Q：此方法是否适用于大型 DWG 文件（数百 MB）？**  
A：是的。光栅化按页进行，您可以调整 `rasterizationOptions`（例如 `Resolution`）以在质量和内存使用之间取得平衡。

**Q：我可以将多个视口导出为单独的 PDF 页面吗？**  
A：您可以遍历 `cadImage.ViewPorts`，将每个设为活动状态，并对每页调用 `Save`，随后使用 Aspose.PDF 合并 PDF。

**Q：是否可以向生成的 PDF 添加水印？**  
A：保存 PDF 后，您可以使用 Aspose.PDF 重新打开它，并在交付给用户之前应用文字或图片水印。

---

**最后更新：** 2026-04-03  
**测试环境：** Aspose.CAD 24.11 for .NET  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}