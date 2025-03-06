---
title: 向 CAD 绘图添加水印 - Aspose.CAD for Java 教程
linktitle: 加水印
second_title: Aspose.CAD Java API
description: 使用 Aspose.CAD for Java 通过个性化水印增强您的 CAD 绘图。请按照我们的分步指南进行无缝集成。
weight: 12
url: /zh/java/other-cad-operations/add-watermark/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 向 CAD 绘图添加水印 - Aspose.CAD for Java 教程

## 介绍

欢迎阅读这份有关使用 Aspose.CAD for Java 向 CAD 绘图添加水印的综合指南。在本教程中，您将学习如何有效地集成水印，通过个性化消息或品牌增强您的 CAD 文档。 Aspose.CAD for Java 提供了一组强大的功能，使水印添加过程变得简单。

## 先决条件

在我们深入学习本教程之前，请确保您满足以下先决条件：

-  Aspose.CAD for Java：确保您的 Java 环境中安装了 Aspose.CAD 库。你可以下载它[这里](https://releases.aspose.com/cad/java/).
- Java 开发工具包 (JDK)：确保您的系统上安装了最新版本的 JDK。

## 导入包

在您的 Java 项目中，导入必要的 Aspose.CAD 包以开始使用：

```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.Cad3DPoint;
import com.aspose.cad.fileformats.cad.cadobjects.CadMText;
import com.aspose.cad.fileformats.cad.cadobjects.CadText;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## 第 1 步：添加新的多行文本

```java
//添加新的多行文本
CadMText watermark = new CadMText();
watermark.setText("Watermark message");
watermark.setInitialTextHeight(40);
watermark.setInsertionPoint(new Cad3DPoint(300, 40));
watermark.setLayerName("0");
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(watermark);
```

## 第 2 步：添加简单实体（例如文本）

您还可以添加更简单的实体，例如文本：

```java
//或添加更简单的实体，例如文本
CadText text = new CadText();
text.setDefaultValue("Watermark text");
text.setTextHeight(40);
text.setFirstAlignment(new Cad3DPoint(300, 40));
text.setLayerName("0") ;
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(text);
```

## 第 3 步：导出为 PDF

将添加水印的 CAD 绘图导出到 PDF 文件：

```java
//导出为 pdf
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
rasterizationOptions.setLayouts(new String[]{"Model"});
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
cadImage.save(dataDir + "AddWatermark_out.pdf", pdfOptions);

```

## 结论

恭喜！您已使用 Aspose.CAD for Java 成功向 CAD 绘图添加水印。这个简单而强大的过程允许您个性化您的设计或通过品牌保护它们。

## 常见问题解答

### Q1：Aspose.CAD 是否兼容所有 CAD 文件格式？

A1：Aspose.CAD支持多种CAD格式，包括DWG、DXF、DWT和DWF。

### Q2：我可以自定义水印文本的外观吗？

A2：是的，您可以完全控制水印的外观，包括文本大小、颜色和位置。

### Q3：Aspose.CAD for Java 有试用版吗？

 A3：是的，您可以下载试用版[这里](https://releases.aspose.com/).

### Q4：如何获得 Aspose.CAD 的支持？

 A4：访问[Aspose.CAD论坛](https://forum.aspose.com/c/cad/19)以获得社区支持。

### Q5：在哪里可以找到 Aspose.CAD for Java 的完整文档？

 A5：请参阅[文档](https://reference.aspose.com/cad/java/)获取详细信息。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
