---
title: 使用 Aspose.CAD for Java 自动调整 CAD 绘图尺寸
linktitle: 自动调整 CAD 图纸尺寸
second_title: Aspose.CAD Java API
description: 探索使用 Aspose.CAD 在 Java 中自动调整 CAD 绘图尺寸的无缝过程。请按照我们的分步指南进行高效的 CAD 文件操作。
weight: 13
url: /zh/java/cad-file-manipulation/auto-adjusting-cad-drawing-size/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.CAD for Java 自动调整 CAD 绘图尺寸

## 介绍

在 CAD（计算机辅助设计）领域，调整绘图尺寸是一项常见要求，而使用 Aspose.CAD for Java，它成为一个无缝过程。这个功能强大的库提供了用于在 Java 应用程序中处理 CAD 文件的综合工具。在本教程中，我们将探索使用 Aspose.CAD 自动调整 CAD 绘图尺寸的分步过程。

## 先决条件

在深入学习本教程之前，请确保您具备以下先决条件：

1.  Java 开发环境：确保您的计算机上安装了 Java。你可以下载它[这里](https://www.java.com/en/download/).

2. Aspose.CAD 库：下载并安装适用于 Java 的 Aspose.CAD 库[这里](https://releases.aspose.com/cad/java/).

3. 示例 CAD 文件：在文档目录中提供一个示例 CAD 文件（例如，sample.dwg）。

## 导入命名空间

在您的 Java 应用程序中，包含必要的命名空间以利用 Aspose.CAD 功能。这是一个例子：

```java

import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

现在，让我们将自动调整 CAD 绘图尺寸的过程分解为可管理的步骤。

## 第 1 步：加载 CAD 图纸

```java
String dataDir = "Your Document Directory" + "CADConversion/";
String sourceFilePath = dataDir + "sample.dwg";
Image objImage = Image.load(sourceFilePath);
```

此步骤涉及从指定文件路径加载 CAD 绘图。

## 第2步：创建BmpOptions

```java
BmpOptions bmpOptions = new BmpOptions();
```

实例化`BmpOptions`类，它将用于设置 BMP 格式的各种选项。

## 步骤 3：创建 CadRasterizationOptions

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(cadRasterizationOptions);
```

创建一个实例`CadRasterizationOptions`自定义 CAD 文件的光栅化设置。

## 第4步：设置布局属性

```java
cadRasterizationOptions.setLayouts(new String[]{"Model"});
```

指定要包含在输出中的布局。在本例中，我们使用“模型”布局。

## 第5步：导出为BMP格式

```java
String outPath = sourceFilePath + ".bmp";
objImage.save(outPath, bmpOptions);
```

最后将调整后的CAD图纸以BMP格式保存到指定的输出路径。

在 Java 应用程序中重复这些步骤，您就可以使用 Aspose.CAD for Java 成功自动调整 CAD 绘图尺寸。

## 结论

在本教程中，我们介绍了使用 Aspose.CAD for Java 自动调整 CAD 绘图尺寸的过程。该库简化了 CAD 文件操作，为开发人员提供了强大的解决方案。

## 常见问题解答

### Q1: Aspose.CAD 是否兼容不同的 CAD 文件格式？

A1：是的，Aspose.CAD支持各种CAD格式，包括DWG、DXF、DGN等。

### Q2：我可以将Aspose.CAD用于商业项目吗？

 A2：当然！访问[这里](https://purchase.aspose.com/buy)探索许可选项。

### Q3：如何获得用于测试目的的临时许可证？

 A3：获得临时许可证[这里](https://purchase.aspose.com/temporary-license/)用于测试和评估。

### Q4：在哪里可以找到对 Aspose.CAD 的支持？

A4：加入 Aspose.CAD 社区[论坛](https://forum.aspose.com/c/cad/19)寻求帮助和讨论。

### Q5：Aspose.CAD for Java 有免费试用版吗？

 A5：是的，您可以免费试用[这里](https://releases.aspose.com/)探索图书馆的能力。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
