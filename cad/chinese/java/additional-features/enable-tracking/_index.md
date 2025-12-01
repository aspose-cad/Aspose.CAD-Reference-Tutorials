---
date: 2025-12-01
description: 了解如何使用 Aspose.CAD for Java 设置 PDF 页面尺寸、将 DWG 转换为 PDF 并启用 DWG 更改的跟踪。
language: zh
linktitle: Set PDF Page Size and Track DWG with Java
second_title: Aspose.CAD Java API
title: 使用 Aspose.CAD Java 设置 PDF 页面大小并跟踪 DWG
url: /java/additional-features/enable-tracking/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 设置 PDF 页面尺寸并跟踪 DWG（使用 Aspose.CAD Java）

## 介绍

在 CAD 项目协作时，您常常需要 **设置 PDF 页面尺寸** 以保持布局一致，**将 DWG 转换为 PDF**，并跟踪对图纸所做的每一次更改。Aspose.CAD for Java 能够在单一、流畅的工作流中实现这些功能。在本教程中，我们将逐步演示如何 **设置 PDF 页面尺寸**、启用 **DWG 更改跟踪**，并使用 Java 将图纸导出为 PDF。

## 快速答复
- **如何设置 PDF 页面尺寸？** 在导出前使用 `CadRasterizationOptions.setPageWidth()` 和 `setPageHeight()`。  
- **导出时可以跟踪更改吗？** 可以 – 实现自定义 `CadRenderHandler` 来捕获跟踪结果。  
- **哪个方法将 DWG 转换为 PDF？** 在配置好选项后调用 `image.save(stream, pdfOptions)`。  
- **主要前置条件是什么？** JDK、Aspose.CAD for Java，以及包含 DWG/DXF 文件的文件夹。  
- **生产环境是否需要许可证？** 需要，非试用部署必须使用有效的 Aspose.CAD 许可证。

## 在 DWG 导出上下文中，“设置 PDF 页面尺寸” 是什么？

设置 PDF 页面尺寸决定了生成的 PDF 画布的尺寸（宽 × 高，单位为像素）。当您希望导出的图纸适配特定纸张大小或屏幕布局时，这一点尤为重要，能够确保所有元素准确出现在预期位置。

## 为什么在导出 DWG 文件时启用跟踪？

跟踪（或更改跟踪）记录在转换过程中出现的渲染问题、缺失字体或不受支持的实体。通过捕获这些信息，您可以：

- 快速定位需要在最终交付前修复的问题。  
- 向团队成员提供明确的反馈，说明哪些内容被更改或省略。  
- 为合规性要求严格的行业维护审计追踪。

## 前置条件

- **Java Development Kit (JDK)** – 任意近期版本（8 及以上）。  
- **Aspose.CAD for Java** – 从官方 [Aspose CAD 下载页面](https://releases.aspose.com/cad/java/) 获取。  
- **文档目录** – 包含待处理 DWG/DXF 文件的文件夹。

## 导入命名空间

首先导入必要的 Aspose.CAD 类以及标准的 Java I/O 类。

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

## 步骤 1：加载 DWG（或 DXF）文件

将源图纸加载到 `Image` 对象中。请将路径调整为指向您自己的目录。

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
Image image = Image.load(dataDir + "conic_pyramid.dxf");
```

## 步骤 2：配置 PDF 导出选项（包括页面尺寸）

在这里我们设置 PDF 选项，并显式 **设置 PDF 页面尺寸** 为 800 × 600 像素。这正是主要关键词所在的位置。

```java
OutputStream stream = new FileOutputStream(dataDir + "output_conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);   // set PDF page width
cadRasterizationOptions.setPageHeight(600);  // set PDF page height
```

## 步骤 3：实现跟踪

创建一个自定义错误处理器，在转换过程中接收跟踪信息。

```java
cadRasterizationOptions.RenderResult = new ErrorHandler();
```

## 步骤 4：导出为 PDF

在配置好选项和跟踪处理器后，执行导出。此步骤 **将 DWG 转换为 PDF**（在本例中也适用于 DXF）。

```java
System.out.println("Exporting to pdf format");
image.save(stream, pdfOptions);
```

## 步骤 5：CadRenderHandler 类 – 捕获跟踪结果

`ErrorHandler` 类继承自 `CadRenderHandler`，并打印在 **跟踪 DWG 更改** 时出现的任何渲染问题。

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

## 常见问题及解决方法

| 问题 | 产生原因 | 解决方案 |
|------|----------|----------|
| **缺失字体** | CAD 文件引用了服务器上未安装的字体。 | 安装所需字体或将其嵌入源图纸中。 |
| **不受支持的实体** | 某些 DWG 实体尚未被 Aspose.CAD 支持。 | 使用跟踪输出识别这些实体并简化图纸。 |
| **页面尺寸不正确** | 导出前未调用 `setPageWidth/Height`。 | 确保如上所示在 `CadRasterizationOptions` 中设置页面尺寸。 |

## 常见问题

### Q1: 我可以为其他 CAD 文件格式启用跟踪吗？

A1: Aspose.CAD 主要支持对 DWG/DXF 文件的跟踪。其他格式的功能请参考官方文档了解可用特性。

### Q2: 如何在 Aspose.CAD for Java 中处理其他导出选项？

A2: 该库提供了诸如 DPI、背景颜色、矢量光栅化等多种选项。请在 [Aspose.CAD Java 文档](https://reference.aspose.com/cad/java/) 中查阅详细信息。

### Q3: 是否有 Aspose.CAD for Java 的试用版？

A3: 有，您可以从 [Aspose.CAD 免费试用](https://releases.aspose.com/) 下载。

### Q4: 哪里可以获取帮助或讨论 Aspose.CAD for Java 的相关问题？

A4: 访问 [Aspose.CAD 论坛](https://forum.aspose.com/c/cad/19) 与社区成员交流，提出问题并分享经验。

### Q5: 如何获取 Aspose.CAD for Java 的临时许可证？

A5: 请按照 [临时许可证](https://purchase.aspose.com/temporary-license/) 页面上的步骤申请限时评估许可证。

### Q6: 能否在 **将 DWG 转换为 PDF** 时保留图层信息？

A6: 可以。通过配置 `CadRasterizationOptions`，您可以在生成的 PDF 中保留图层信息。

### Q7: 使用自定义页面尺寸 **导出 DWG 为 PDF** 的最佳方法是什么？

A7: 在调用 `image.save()` 之前，使用 `setPageWidth` 和 `setPageHeight` 设置所需的宽高——正如步骤 2 中演示的那样。

## 结论

按照上述步骤，您即可使用 Aspose.CAD for Java **设置 PDF 页面尺寸**、**将 DWG 转换为 PDF**，并 **跟踪 DWG 文件的更改**。该工作流让您全面掌控输出布局，同时提供有价值的诊断信息，确保 CAD 协作顺畅且无错误。欢迎探索更多渲染选项，并将此代码集成到更大的自动化流水线中。

---

**最后更新：** 2025-12-01  
**测试环境：** Aspose.CAD for Java 24.12（撰写时最新版本）  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}