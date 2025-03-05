---
title: 使用 Aspose.CAD 教程将 Java DGN 转换为 JPEG
linktitle: 将 AutoCAD 格式的 DGN 导出为光栅图像格式
second_title: Aspose.CAD Java API
description: 了解如何使用 Aspose.CAD 将 DGN 文件导出为 Java 中的 JPEG 图像。本分步教程将指导您轻松完成整个过程。
type: docs
weight: 13
url: /zh/java/dgn-export-options/exporting-dgn-to-raster-image/
---
## 介绍

欢迎阅读有关使用 Aspose.CAD for Java 将 DGN（设计）文件导出为光栅图像格式的综合教程。 Aspose.CAD 是一个功能强大的库，使 Java 开发人员能够无缝地处理 CAD 文件。在本教程中，我们将指导您完成将 DGN 文件转换为 JPEG 图像的过程，并为您提供分步说明和代码示例。

## 先决条件

在深入学习本教程之前，请确保您具备以下先决条件：
1.  Aspose.CAD 库：确保您已安装 Aspose.CAD for Java 库。你可以下载它[这里](https://releases.aspose.com/cad/java/).
2. Java 开发工具包 (JDK)：确保您的计算机上安装了 Java。
3. 集成开发环境 (IDE)：使用与 Java 兼容的 IDE，例如 IntelliJ 或 Eclipse。

## 导入包

在您的 Java 项目中，导入 Aspose.CAD 所需的包。将以下行添加到您的代码中：

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
```

## 第 1 步：加载 DGN 文件

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
DgnImage dgnImage = (DgnImage) Image.load(dataDir + "Nikon_D90_Camera.dgn");
```

## 第2步：创建JpegOptions对象

```java
ImageOptionsBase options = new JpegOptions();
```

## 第 3 步：分配光栅化选项

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(600);
vectorOptions.setPageHeight(400);
vectorOptions.setNoScaling(true);
vectorOptions.setAutomaticLayoutsScaling(false);
options.setVectorRasterizationOptions(vectorOptions);
```

## 第四步：保存转换后的图像

```java
OutputStream outStream = new FileOutputStream(dataDir + "ExportDGNToRasterImage_Out.jpg");
dgnImage.save(outStream, options);
```

对特定 DGN 文件重复这些步骤，并相应地调整文件路径。

## 结论

恭喜！您已成功学习如何使用 Aspose.CAD for Java 将 DGN 文件导出为光栅图像格式。本教程为您提供了将此功能合并到 Java 应用程序中的知识。

## 常见问题解答

### Q1：我可以将 Aspose.CAD for Java 与其他 CAD 文件格式一起使用吗？

A1：是的，Aspose.CAD支持各种CAD格式，为Java开发人员提供了多功能的解决方案。

### 问题 2：Aspose.CAD for Java 是否有免费试用版？

 A2：是的，您可以免费试用[这里](https://releases.aspose.com/).

### 问题 3：在哪里可以找到 Aspose.CAD for Java 的文档？

 A3：参考文档[这里](https://reference.aspose.com/cad/java/).

### 问题 4：如何获得 Aspose.CAD for Java 的支持？

 A4：访问支持论坛[这里](https://forum.aspose.com/c/cad/19).

### Q5：在哪里可以购买 Aspose.CAD for Java 的许可证？

 A5：您可以购买许可证[这里](https://purchase.aspose.com/buy).