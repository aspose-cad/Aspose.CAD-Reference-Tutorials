---
title: 设置画布大小和模式
linktitle: 设置画布大小和模式
second_title: Aspose.CAD Java API
description: 通过我们有关设置画布大小和模式的分步指南，探索 Aspose.CAD for Java 的强大功能。轻松将 CAD 文件转换为 PDF 和 TIFF 格式。
weight: 16
url: /zh/java/advanced-cad-features/set-canvas-size-and-mode/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 设置画布大小和模式

## 介绍

您是否希望利用 Aspose.CAD for Java 的强大功能来增强您的 CAD 转换过程？本综合指南将引导您完成使用 Aspose.CAD for Java 设置画布大小和模式的步骤。无论您是经验丰富的开发人员还是刚刚入门，本教程都将为您提供所需的见解。

## 先决条件

在深入学习本教程之前，请确保您具备以下先决条件：

-  Aspose.CAD for Java：确保您的 Java 环境中安装了 Aspose.CAD 库。你可以下载它[这里](https://releases.aspose.com/cad/java/).

- 文档目录：设置文档目录来存储 CAD 文件。该目录将在教程步骤中引用。

现在，让我们开始使用分步指南。

## 导入命名空间

在此步骤中，我们将导入必要的命名空间来启动您的 Aspose.CAD 项目。
```java
import java.awt.Image;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## 第1步：导入Aspose.CAD类

```java
//资源目录的路径。
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
com.aspose.cad.Image objImage = com.aspose.cad.Image.load(srcFile);
```

在此代码片段中，我们设置资源目录的路径并使用 Aspose.CAD 加载 DXF 文件`Image`班级。

## 步骤 2：设置 CadRasterizationOptions 属性

```java
//创建 CadRasterizationOptions 的实例并设置其各种属性
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

在这里，我们创建一个实例`CadRasterizationOptions`并配置页面宽度、页面高度和缩放选项等属性。

## 步骤 3：创建 PdfOptions 并设置 VectorRasterizationOptions

```java
//创建 PdfOptions 的实例
PdfOptions pdfOptions = new PdfOptions();

//设置 VectorRasterizationOptions 属性
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

现在，我们创建一个`PdfOptions`实例并设置其`VectorRasterizationOptions`属性改为之前配置的`CadRasterizationOptions`.

## 第 4 步：导出为 PDF

```java
//将 CAD 导出为 PDF
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

最后，我们使用指定的选项将 CAD 图像保存到 PDF 文件。

## 步骤 5：创建 TiffOptions 并设置 VectorRasterizationOptions

```java
//创建 TiffOptions 的实例
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);

//设置 VectorRasterizationOptions 属性
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
```

在这一步中，我们设置了一个`TiffOptions`实例并配置其`VectorRasterizationOptions`财产。

## 第 6 步：导出为 TIFF

```java
//将 CAD 导出为 TIFF
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

最后，我们使用指定的选项将 CAD 图像保存到 TIFF 文件。

## 结论

恭喜！您已使用 Aspose.CAD for Java 成功设置了画布大小和模式。本教程为您的 CAD 转换项目提供了坚实的基础。探索更多功能和可能性[Aspose.CAD 文档](https://reference.aspose.com/cad/java/).

## 常见问题解答

### Q1：我可以将 Aspose.CAD for Java 与其他 Java 框架一起使用吗？

A1：是的，Aspose.CAD 旨在与各种 Java 框架无缝集成。

### Q2：Aspose.CAD 是否有临时许可证？

 A2：是的，您可以获得临时许可证[这里](https://purchase.aspose.com/temporary-license/).

### 问题 3：我在哪里可以获得 Aspose.CAD 的社区支持？

 A3：访问[Aspose.CAD论坛](https://forum.aspose.com/c/cad/19)以获得社区支持和讨论。

### Q4：我可以免费试用Aspose.CAD吗？

 A4：当然！获得免费试用[这里](https://releases.aspose.com/).

### Q5: 如何购买 Aspose.CAD for Java？

A5：购买产品[这里](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
