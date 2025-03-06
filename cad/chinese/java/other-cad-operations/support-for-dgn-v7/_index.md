---
title: DGN 到 PDF 转换指南 - Aspose.CAD for Java
linktitle: 支持 DGN V7
second_title: Aspose.CAD Java API
description: 使用 Aspose.CAD for Java 轻松将 DGN 文件转换为 PDF。请遵循我们的分步指南，实现无缝集成和高效的工作流程。
weight: 11
url: /zh/java/other-cad-operations/support-for-dgn-v7/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DGN 到 PDF 转换指南 - Aspose.CAD for Java

## 介绍

在 CAD（计算机辅助设计）的动态世界中，将 DGN（设计）文件高效转换为 PDF（便携式文档格式）是一项至关重要的要求。 Aspose.CAD for Java 作为一个强大的解决方案出现，提供无缝集成和强大的功能。本分步指南旨在引导您完成使用 Aspose.CAD for Java 将 DGN 文件导出为 PDF 的过程，确保工作流程顺利高效。

## 先决条件

在深入学习本教程之前，请确保您具备以下先决条件：
-  Aspose.CAD for Java Library：从以下位置下载并安装该库：[Aspose.CAD for Java 下载页面](https://releases.aspose.com/cad/java/).
- Java 开发环境：确保您的计算机上设置了 Java 开发环境。

## 导入包

首先将必要的包导入到您的 Java 项目中：

## 第1步：导入必要的包

在您的 Java 项目中，导入 Aspose.CAD for Java 所需的包。
```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadRasterizationOptions;
import com.aspose.cad.fileformats.cad.cadobjects.DgnImage;
import com.aspose.cad.imageoptions.PdfOptions;
import java.awt.Color;
```

## 第2步：设置文件路径

定义输入 DGN 文件和输出 PDF 文件的路径。

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "Nikon_D90_Camera.dgn";
String outFile  = dataDir + "Nikon_D90_Camera.pdf";
```

## 步骤 3：加载 DGN 图像

使用 Aspose.CAD 库加载 DGN 图像。

```java
DgnImage objImage = (DgnImage)Image.load(fileName);
```

## 步骤 4：配置 PDF 导出选项

设置导出为 PDF 的选项，包括页面尺寸、自动布局缩放、背景颜色和要导出的特定布局。

```java
PdfOptions options = new PdfOptions();
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
vectorOptions.setAutomaticLayoutsScaling(true);
vectorOptions.setBackgroundColor(Color.getBlack());
vectorOptions.setLayouts(new String[] { "1", "2", "3", "9" }); //仅导出 4 个（1、2、3 和 9）视图
options.setVectorRasterizationOptions(vectorOptions);
```

## 第5步：保存PDF文件

使用指定选项将 DGN 图像另存为 PDF 文件。

```java
objImage.save(outFile, options);
```

对不同的 DGN 文件重复这些步骤，根据需要调整文件路径和选项。

## 结论

借助 Aspose.CAD for Java，将 DGN 文件转换为 PDF 成为一个简单的过程。本指南为您提供了将该库无缝集成到 Java 项目中的知识，从而促进高效的 CAD 文件转换。

## 常见问题解答

### Q1：我可以将 Aspose.CAD for Java 与其他 CAD 文件格式一起使用吗？

A1：是的，Aspose.CAD 支持各种 CAD 格式，提供除 DGN 到 PDF 转换之外的多种功能。

### 问题 2：Aspose.CAD for Java 是否有临时许可证？

 A2：是的，您可以获得临时许可证[这里](https://purchase.aspose.com/temporary-license/)用于测试目的。

### 问题 3：如何寻求有关 Aspose.CAD for Java 的支持或提出问题？

 A3：访问[Aspose.CAD论坛](https://forum.aspose.com/c/cad/19)与社区联系并寻求帮助。

### 问题 4：将 DGN 转换为 PDF 时可以导出哪些布局？

 A4：您可以通过自定义来指定要导出的布局`setLayouts`代码中的数组。

### 问题 5：在哪里可以找到 Aspose.CAD for Java 的综合文档？

 A5：请参阅[Aspose.CAD for Java 文档](https://reference.aspose.com/cad/java/)获取详细信息。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
