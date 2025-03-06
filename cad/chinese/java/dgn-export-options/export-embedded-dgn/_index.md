---
title: 使用 Aspose.CAD for Java 将嵌入式 DGN 导出为 PDF
linktitle: 导出嵌入式 DGN
second_title: Aspose.CAD Java API
description: 探索有关使用 Aspose.CAD for Java 将嵌入式 DGN 文件导出为 PDF 的分步指南。通过无缝 CAD 文件操作增强您的 Java 应用程序。
weight: 11
url: /zh/java/dgn-export-options/export-embedded-dgn/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.CAD for Java 将嵌入式 DGN 导出为 PDF

## 介绍

欢迎阅读有关使用 Aspose.CAD for Java 导出嵌入式 DGN 文件的综合教程。 Aspose.CAD 是一个功能强大的库，使 Java 开发人员能够无缝地处理 CAD 文件。在本教程中，我们将按照分步说明指导您完成将嵌入式 DGN 文件导出为 PDF 的过程。无论您是经验丰富的开发人员还是新手，本教程都将帮助您利用 Aspose.CAD 的功能来增强您的 Java 应用程序。

## 先决条件

在我们深入学习本教程之前，请确保您具备以下先决条件：
- Java 开发环境：确保您的计算机上设置有 Java 开发环境。
-  Aspose.CAD for Java：从以下位置下载并安装 Aspose.CAD for Java 库[这里](https://releases.aspose.com/cad/java/).

## 导入包

首先，您需要在 Java 项目中导入必要的包。将以下导入语句添加到您的代码中：

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

现在，让我们将示例代码分解为多个步骤：

## 第 1 步：设置输入和输出路径

定义文档所在的目录路径并指定输入 DWG 文件名。

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
```

## 第 2 步：加载 DWG 文件

将 DWG 文件加载到`Image`使用 Aspose.CAD 的对象。

```java
Image objImage = Image.load(fileName);
```

## 步骤 3：配置光栅化选项

配置光栅化选项，例如要包含在导出中的布局。

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setLayouts(new String[] {"Model"});
```

## 步骤 4：配置 PDF 选项

设置 PDF 选项，包括矢量光栅化选项。

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## 第5步：保存PDF文件

使用配置的选项保存 PDF 文件。
```java
objImage.save(dataDir + "BlockRefDgn.pdf", pdfOptions);
```

## 结论

恭喜！您已使用 Aspose.CAD for Java 成功将嵌入的 DGN 文件导出为 PDF。本教程介绍了将 Aspose.CAD 集成到 Java 应用程序中以实现高效 CAD 文件操作的基本步骤。

## 常见问题解答

### Q1：我可以在商业项目中使用Aspose.CAD for Java吗？

 A1：是的，Aspose.CAD for Java 是一个商业库。您可以从以下位置获取许可证[这里](https://purchase.aspose.com/buy).

### Q2: 有免费试用吗？

 A2：是的，您可以免费试用 Aspose.CAD for Java[这里](https://releases.aspose.com/).

### 问题 3：如何获得 Aspose.CAD for Java 的支持？

A3：您可以向 Aspose.CAD 社区寻求支持[论坛](https://forum.aspose.com/c/cad/19).

### Q4：如果我需要临时许可证怎么办？

 A4：您可以获得临时许可证[这里](https://purchase.aspose.com/temporary-license/).

### Q5：在哪里可以找到文档？

 A5：文档可用[这里](https://reference.aspose.com/cad/java/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
