---
title: 使用 Aspose.CAD for Java 制作动态 PDF
linktitle: 具有不同布局的单个 PDF
second_title: Aspose.CAD Java API
description: 使用 Aspose.CAD for Java 从 CAD 绘图创建具有不同布局的精美 PDF。为 Java 开发人员提供轻松集成和强大的功能。
type: docs
weight: 16
url: /zh/java/other-cad-operations/single-pdf-different-layouts/
---
## 介绍

欢迎来到 Aspose.CAD for Java 的世界，这是一个功能强大的库，使开发人员能够轻松操作 CAD 绘图。在本教程中，我们将深入研究使用 Aspose.CAD for Java 创建具有不同布局的单个 PDF。无论您是经验丰富的开发人员还是新手，本分步指南都将引导您完成整个过程。

## 先决条件

在我们开始这一旅程之前，请确保您具备以下先决条件：
- Java 环境：确保您的计算机上安装了 Java。
-  Aspose.CAD 库：从以下位置下载并安装适用于 Java 的 Aspose.CAD 库：[下载链接](https://releases.aspose.com/cad/java/).
- 文档目录：为 DWG 工程图设置目录。

## 导入包

在您的 Java 项目中，导入必要的包：

```java
import com.aspose.cad.Image;
import com.aspose.cad.SizeF;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.VectorRasterizationOptions;
```

## 第 1 步：加载 CAD 图纸

首先将 CAD 绘图加载到`CadImage`目的：

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
CadImage cadImage = (CadImage)Image.load(dataDir + "City skyway map.dwg");
```

## 第 2 步：配置光栅化选项

设置 CAD 图像的光栅化选项：

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1000);
rasterizationOptions.setPageHeight(1000);
```

## 第 3 步：自定义布局页面大小

为 CAD 绘图中的多个布局定义自定义尺寸：

```java
rasterizationOptions.getLayoutPageSizes().addItem("ANSI C Plot", new SizeF(500, 1000));
rasterizationOptions.getLayoutPageSizes().addItem("8.5 x 11 Plot", new SizeF(1000, 100));
```

## 步骤 4：设置 PDF 选项

配置 PDF 选项，合并光栅化设置：

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## 第 5 步：另存为 PDF

将处理后的 CAD 图像保存为 PDF：

```java
cadImage.save(dataDir + "singlePDF_out.pdf", pdfOptions);
```

恭喜！您已使用 Aspose.CAD for Java 成功创建了具有不同布局的单个 PDF。

## 结论

在本教程中，我们探索了 Aspose.CAD for Java 的无缝集成，以从 CAD 绘图生成具有不同布局的 PDF。该库的灵活性和强大功能使其成为 CAD 操作任务的首选。

## 常见问题解答

### Q1：我可以将 Aspose.CAD for Java 与其他 Java 库一起使用吗？

A1：是的，Aspose.CAD for Java 旨在与其他 Java 库无缝集成，提供广泛的功能。

### Q2：有试用版吗？

 A2：当然！您可以访问免费试用版[这里](https://releases.aspose.com/).

### Q3：我在哪里可以找到额外的支持？

 A3：访问[Aspose.CAD论坛](https://forum.aspose.com/c/cad/19)以获得社区支持和讨论。

### Q4：如何获得临时驾照？

 A4：您可以获得临时许可证[这里](https://purchase.aspose.com/temporary-license/).

### Q5：哪里可以购买完整版？

A5：购买完整版的 Aspose.CAD for Java[这里](https://purchase.aspose.com/buy).