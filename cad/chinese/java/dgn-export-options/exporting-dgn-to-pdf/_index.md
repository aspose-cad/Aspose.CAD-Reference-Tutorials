---
title: 使用 Aspose.CAD for Java 轻松将 DGN 导出为 AutoCAD PDF
linktitle: 将 AutoCAD 格式的 DGN 导出为 PDF
second_title: Aspose.CAD Java API
description: 探索有关使用 Aspose.CAD for Java 将 DGN 文件导出为 PDF 中的 AutoCAD 格式的分步指南。轻松提升 Java 应用程序的 CAD 处理能力。
weight: 12
url: /zh/java/dgn-export-options/exporting-dgn-to-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.CAD for Java 轻松将 DGN 导出为 AutoCAD PDF

## 介绍

欢迎阅读这个关于使用 Aspose.CAD for Java 将 AutoCAD 格式的 DGN 文件导出为 PDF 的综合教程。如果您希望增强 Java 应用程序处理 CAD 文件的能力，Aspose.CAD 是一个很好的选择。在本教程中，我们将指导您逐步完成导出 DGN 文件的过程。


## 先决条件
在我们深入学习本教程之前，请确保您具备以下先决条件：
-  Aspose.CAD 库：确保您已安装适用于 Java 的 Aspose.CAD 库。你可以下载它[这里](https://releases.aspose.com/cad/java/).
- 文档目录：设置将存储输入和输出文件的文档目录。

## 导入包

在您的 Java 项目中，导入必要的包以访问 Aspose.CAD 功能：

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

现在，让我们将示例代码分解为多个步骤：

## 第 1 步：定义文件路径

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "Nikon_D90_Camera.dgn";
String outFile  = dataDir + "Nikon_D90_Camera.pdf";
```

确保将“您的文档目录”替换为文件所在的实际路径。

## 步骤 2：加载 DGN 图像

```java
DgnImage objImage = (DgnImage) Image.load(fileName);
```

使用 Aspose.CAD 加载 DGN 文件。

## 第 3 步：设置 PDF 导出选项

```java
PdfOptions options = new PdfOptions();
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
vectorOptions.setAutomaticLayoutsScaling(true);
vectorOptions.setLayouts(new String[] { "1", "2", "3", "9" }); //导出特定视图
options.setVectorRasterizationOptions(vectorOptions);
```

定义 PDF 导出选项，包括页面尺寸和布局首选项。

## 第 4 步：保存 PDF 文件

```java
objImage.save(outFile, options);
```

保存导出的 PDF 文件。

对要转换的任何其他 DGN 文件重复这些步骤。恭喜！您已使用 Aspose.CAD for Java 成功将 DGN 文件导出为 AutoCAD 格式的 PDF。

## 结论

在本教程中，我们探讨了如何利用 Aspose.CAD for Java 来增强应用程序的 CAD 文件处理功能。通过易于遵循的步骤和代码示例，您现在可以将 DGN 文件无缝导出为 PDF 格式的 AutoCAD 格式。

## 常见问题解答

### Q1：Aspose.CAD 是否兼容所有 CAD 文件格式？

A1：是的，Aspose.CAD 支持多种 CAD 格式，确保处理各种文件类型的多功能性。

### Q2：我可以自定义 PDF 导出设置吗？

A2：当然。如教程中所示，您可以调整页面尺寸和布局等选项以满足您的要求。

### 问题 3：我在哪里可以找到额外的支持或帮助？

 A3：访问[Aspose.CAD论坛](https://forum.aspose.com/c/cad/19)以获得社区支持和讨论。

### Q4：有免费试用吗？

 A4：是的，您可以免费试用[这里](https://releases.aspose.com/).

### Q5：如何获得临时驾照？

 A5：获得临时许可证[这里](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
