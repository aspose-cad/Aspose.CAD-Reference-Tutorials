---
date: 2025-12-03
description: 学习如何在使用 Aspose.CAD for Java 将 DWG 转换为 PDF 时设置 PDF 页面尺寸，并在 DWG 文件中启用跟踪——完整指南，精准导出
  CAD 图纸为 PDF。
language: zh
linktitle: Set PDF Page Size and Enable Tracking in DWG Files Using Java
second_title: Aspose.CAD Java API
title: 使用 Aspose.CAD 在 Java 中设置 PDF 页面大小并在 DWG 文件中启用跟踪
url: /java/additional-features/enable-tracking/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.CAD for Java 在 DWG 文件中设置 PDF 页面大小并启用跟踪

## Introduction

如果您在*将 DWG 转换为 PDF*时需要**设置 PDF 页面大小**，并且希望跟踪任何渲染问题，Aspose.CAD for Java 为您提供了一种简洁的编程方式来同时实现这两项功能。本教程将逐步演示如何配置页面尺寸、启用跟踪以及导出 CAD 绘图 PDF——全部使用 Java 完成。结束时，您将了解为何为 CAD 绘图设置正确的页面大小至关重要，以及如何在导出过程中捕获详细的跟踪信息。

## Quick Answers
- **“设置 PDF 页面大小”会有什么影响？** 它定义了生成的 PDF 画布的宽度和高度，确保您的图纸能够完整显示。  
- **使用此功能是否需要许可证？** 试用版可用于测试；生产环境需要商业许可证。  
- **需要哪个版本的 Aspose.CAD？** 任意支持 `CadRasterizationOptions` 的近期版本均可。  
- **可以用于其他 CAD 格式吗？** 示例展示了 DWG/DXF，但相同方法同样适用于大多数受支持的格式。  
- **转换需要多长时间？** 对于一般文件通常在一秒以内；大型图纸可能需要更长时间。

## What is “set PDF page size” in the context of CAD export?

设置 PDF 页面大小即告诉渲染器输出画布的精确尺寸（以像素或点为单位）。这在需要保持比例和布局的技术图纸中尤为重要。如果不显式设置页面大小，PDF 可能会采用默认尺寸，从而导致图纸被裁剪或变形。

## Why set PDF page size when exporting CAD drawings?
- **保持比例** – 工程师依赖真实比例的打印件。  
- **适配纸张** – 可选择 A4、Letter 或自定义尺寸，以符合项目规范。  
- **提升可读性** – 更大的页面可以在不放大的情况下显示细节。  
- **输出一致** – 自动化流水线每次生成的 PDF 尺寸保持一致。

## How to set PDF page size when converting DWG to PDF?
下面我们将在导出前使用自定义宽高值配置 `CadRasterizationOptions`。此步骤直接对应关键词 **set PDF page size**。

## Prerequisites

- **Java Development Kit (JDK)** – 已在机器上安装 Java 8 或更高版本。  
- **Aspose.CAD for Java** – 从官方 [Aspose CAD download page](https://releases.aspose.com/cad/java/) 下载。  
- **Document Directory** – 包含待处理 DWG/DXF 文件的文件夹。

## Import Namespaces

First, import the classes you’ll need. The code block is unchanged from the original tutorial.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.CadRenderResult;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.RenderResult;
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
```

## Step 1: Load the DWG/DXF File

Load your source drawing. Adjust the path to point at your own file.

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
Image image = Image.load(dataDir + "conic_pyramid.dxf");
```

## Step 2: Configure PDF Export Options (including page size)

Here we set the page width and height—this is where we **set PDF page size**. The values are in pixels; you can convert from inches or millimeters as needed.

```java
OutputStream stream = new FileOutputStream(dataDir + "output_conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);   // <-- custom width
cadRasterizationOptions.setPageHeight(600);  // <-- custom height
```

> **Tip:** 如果您倾向于使用标准纸张尺寸，可使用 `1 inch = 72 points` 的换算。对于 A4 纸（8.27 × 11.69 in），设置 `pageWidth = 595` 和 `pageHeight = 842`。

## Step 3: Implement Tracking

Tracking captures any rendering problems. We attach a custom handler that will be invoked after the export.

```java
cadRasterizationOptions.RenderResult = new ErrorHandler();
```

## Step 4: Export to PDF

Now perform the conversion. The PDF will be created with the dimensions you specified, and any tracking information will be printed to the console.

```java
System.out.println("Exporting to pdf format");
image.save(stream, pdfOptions);
```

## Step 5: CadRenderHandler Class

The handler prints out any failures that occurred during rendering. This helps you debug issues when **exporting CAD drawing PDF**.

```java
public static class ErrorHandler extends CadRasterizationOptions.CadRenderHandler {
    @Override
    public void invoke(CadRenderResult result) {
        System.out.println("Tracking results of exporting");

        if (result.isRenderComplete())
            return;

        System.out.println("Have some problems:");

        int idxError = 1;
        for (RenderResult rr : result.getFailures()) {
            System.out.printf("{0}. {1}, {2}", idxError, rr.getRenderCode(), rr.getMessage());
            idxError++;
        }
    }
}
```

## Common Issues and Solutions

| Issue | Cause | Fix |
|-------|-------|-----|
| **Blank PDF** | 页面大小设置为 0 或过小 | 确认 `setPageWidth` 和 `setPageHeight` 为正值。 |
| **Missing geometry** | 渲染错误被处理程序捕获 | 查看 `ErrorHandler` 的控制台输出，并处理相应的 `RenderCode`。 |
| **File not found** | `dataDir` 路径不正确 | 使用绝对路径或确保目录存在。 |
| **License exception** | 在大文件上使用试用版且未提供有效许可证 | 在加载图像前应用您的 Aspose.CAD 许可证。 |

## Frequently Asked Questions

**Q: Can I enable tracking for other CAD file formats using Aspose.CAD for Java?**  
A: Aspose.CAD 主要支持 DWG/DXF 的跟踪。其他格式请参考官方文档。

**Q: How can I handle additional export options in Aspose.CAD for Java?**  
A: 该库提供了 DPI、背景颜色、矢量光栅化等多种选项。详见 [Aspose.CAD Java Documentation](https://reference.aspose.com/cad/java/)。

**Q: Is there a trial version available for Aspose.CAD for Java?**  
A: 有，您可以从 [Aspose.CAD Free Trial](https://releases.aspose.com/) 下载免费试用版。

**Q: Where can I seek assistance or discuss issues related to Aspose.CAD for Java?**  
A: 请访问 [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) 获取社区支持和官方答复。

**Q: How do I obtain a temporary license for Aspose.CAD for Java?**  
A: 请按照 [Temporary License](https://purchase.aspose.com/temporary-license/) 页面上的步骤操作。

---

**Last Updated:** 2025-12-03  
**Tested With:** Aspose.CAD for Java 24.11（撰写时的最新版本）  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}