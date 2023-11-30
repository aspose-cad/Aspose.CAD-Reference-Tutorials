---
title: 在 C# 中使用坐标将 DWG 转换为 PDF - Aspose.CAD 教程
linktitle: 在 C# 中使用坐标将 DWG 转换为 PDF
second_title: Aspose.CAD .NET - CAD 和 BIM 文件格式
description: 了解如何使用 Aspose.CAD 在 C# 中将 DWG 转换为具有特定坐标的 PDF。按照我们的分步指南进行精确高效的 CAD 文件转换。
type: docs
weight: 11
url: /zh/net/conversion-and-export/converting-dwg-to-pdf-with-coordinates/
---
## 介绍

欢迎阅读这个关于使用 Aspose.CAD for .NET 将 DWG 文件转换为具有指定坐标的 PDF 的综合教程。 Aspose.CAD 是一个功能强大的库，允许开发人员在其 .NET 应用程序中无缝地使用 CAD 文件格式。在本教程中，我们将引导您完成将 DWG 文件转换为 PDF 的过程，同时提供特定坐标以提高精度。

## 先决条件

在我们开始之前，请确保您具备以下先决条件：

-  Aspose.CAD 库：下载并安装适用于 .NET 的 Aspose.CAD 库。你可以找到图书馆[这里](https://releases.aspose.com/cad/net/).

- 开发环境：确保您设置了兼容的开发环境，包括 Visual Studio 或任何其他首选 IDE。

- DWG 文件：准备好 DWG 文件以供转换。您可以使用提供的示例文件或自定义 DWG 文件。

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

让我们将代码分解为分步指南，以便更好地理解：

## 第 1 步：定义文档目录

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

## 第 4 步：定义坐标和视口

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

## 第 5 步：应用视口设置

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

## 第 6 步：配置 PDF 选项并导出

```csharp
    Aspose.CAD.ImageOptions.PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions();
    pdfOptions.VectorRasterizationOptions = rasterizationOptions;

    MyDir = MyDir + "ConvertDWGToPDFBySupplyingCoordinates_out.pdf";
    cadImage.Save(MyDir, pdfOptions);
}
```

## 第7步：显示成功消息

```csharp
Console.WriteLine("\nThe DWG file exported successfully to PDF.\nFile saved at " + MyDir);
```

## 结论

恭喜！您已使用 Aspose.CAD for .NET 成功将 DWG 文件转换为具有指定坐标的 PDF。本教程涵盖了基本步骤，并为开发人员提供了清晰的指南。

## 常见问题解答

### Q1：我可以将 Aspose.CAD 与其他 CAD 文件格式一起使用吗？

A1：是的，Aspose.CAD支持各种CAD格式，包括DWG、DXF、DWF等。

### Q2：转换过程中出现错误如何处理？

A2：使用 try-catch 块实现错误处理机制来捕获和管理异常。

### Q3：Aspose.CAD同时适用于Windows和Linux环境吗？

A3：是的，Aspose.CAD 兼容 Windows 和 Linux 平台。

### Q4：我可以进一步定制PDF输出吗？

A4：当然！探索 Aspose.CAD 提供的广泛选项，根据您的特定要求定制 PDF 输出。

### 问题 5：我在哪里可以找到其他支持或社区讨论？

 A5：访问[Aspose.CAD论坛](https://forum.aspose.com/c/cad/19)以获得社区支持和讨论。