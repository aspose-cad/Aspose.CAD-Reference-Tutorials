---
title: 使用 Aspose.CAD for Java 将 DGN 导出为 DWG
linktitle: 将 DGN 导出为 DWG 的一部分
second_title: Aspose.CAD Java API
description: 探索如何使用 Aspose.CAD for Java 将 DGN 导出为 DWG 的一部分。请按照我们的分步指南进行高效的 CAD 文件操作。
type: docs
weight: 10
url: /zh/java/dgn-export-options/export-dgn-as-part-of-dwg/
---
## 介绍

在本教程中，我们将探讨如何使用 Aspose.CAD for Java 将 DGN (MicroStation Design) 文件导出为 DWG (AutoCAD Drawing) 文件的一部分。 Aspose.CAD 是一个功能强大的库，提供了处理 CAD 文件格式的全面功能。本分步指南将帮助您了解使用 Java 将 DGN 导出为 DWG 的一部分的过程。

## 先决条件

在我们深入学习本教程之前，请确保您具备以下先决条件：
1. Aspose.CAD 库：下载并安装适用于 Java 的 Aspose.CAD 库。你可以找到图书馆[这里](https://releases.aspose.com/cad/java/).
2. Java 开发工具包 (JDK)：确保您的系统上安装了 Java。
3. 集成开发环境 (IDE)：选择 Eclipse 或 IntelliJ 等 Java IDE，以获得更流畅的开发体验。

## 导入包

在您的 Java 项目中，导入必要的 Aspose.CAD 包以启用 CAD 文件操作。这是一个例子：

```java
import com.aspose.cad;
import com.aspose.cad.imageoptions;
import com.aspose.cad.fileformats.cad.cadconsts;
import com.aspose.cad.fileformats.cad;
import com.aspose.cad.fileformats.cad.cadobjects;
```

## 第1步：设置文件路径

定义 DWG 文件的输入和输出文件路径。更新`dataDir`, `fileName`， 和`outPath`相应的变量。

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
String outPath = dataDir + "BlockRefDgn.dwg.pdf";
```

## 第2步：创建PdfOptions实例

创建一个实例`PdfOptions`类，因为我们要将 DWG 文件导出为 PDF 格式。

```java
PdfOptions exportOptions = new PdfOptions();
```

## 第 3 步：加载 DWG 文件

将现有 DWG 文件作为图像加载并将其转换为`CadImage`类型。

```java
CadImage cadImage = (CadImage) Image.load(fileName);
```

## 第 4 步：迭代实体

浏览 DWG 文件中的每个实体并检查它是否是图像定义。如果是，则检索该对象的外部引用。

```java
for (CadBaseEntity baseEntity : cadImage.getEntities()) {
    if (baseEntity.getTypeName() == CadEntityTypeName.DGNUNDERLAY) {
        CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
        System.out.println(dgnFile.getUnderlayPath());
    }
}
```

## 第 5 步：定义光栅化选项

定义设置`CadRasterizationOptions`对象，包括页面宽度、高度、布局和背景颜色。

```java
CadRasterizationOptions vectorRasterizationOptions = new CadRasterizationOptions();
vectorRasterizationOptions.setPageWidth(1600);
vectorRasterizationOptions.setPageHeight(1600);
vectorRasterizationOptions.setLayouts(new String[] { "Model" });
vectorRasterizationOptions.setAutomaticLayoutsScaling(false);
vectorRasterizationOptions.setNoScaling(true);
vectorRasterizationOptions.setBackgroundColor(Color.getBlack());
vectorRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
```

## 第 6 步：设置矢量光栅化选项

设置导出的矢量光栅化选项。

```java
exportOptions.setVectorRasterizationOptions(vectorRasterizationOptions);
```

## 第 7 步：将 DWG 导出为 PDF

最后，通过调用将 DWG 导出为 PDF`save`方法。

```java
cadImage.save(outPath, exportOptions);
```

## 结论

恭喜！您已成功学习如何使用 Aspose.CAD for Java 将 DGN 文件导出为 DWG 文件的一部分。这个强大的库提供了处理 CAD 文件的广泛功能，使您的 CAD 文件操作任务高效而简单。

## 常见问题解答

### Q1：在哪里可以找到 Aspose.CAD for Java 的文档？

 A1：文档可以找到[这里](https://reference.aspose.com/cad/java/).

### Q2：如何下载 Java 版 Aspose.CAD 库？

 A2：您可以从以下位置下载该库：[这个链接](https://releases.aspose.com/cad/java/).

### 问题 3：Aspose.CAD for Java 是否有免费试用版？

 A3：是的，您可以找到免费试用版[这里](https://releases.aspose.com/).

### 问题 4：在哪里可以获得 Aspose.CAD for Java 的临时许可证？

 A4：获得临时许可证[这里](https://purchase.aspose.com/temporary-license/).

### Q5: 需要帮助或有疑问吗？

 A5：访问 Aspose.CAD 社区支持论坛[这里](https://forum.aspose.com/c/cad/19).