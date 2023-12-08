---
title: 使用 Aspose.CAD for Java 的单位类型调整 CAD 绘图尺寸
linktitle: 使用单位类型调整 CAD 绘图尺寸
second_title: Aspose.CAD Java API
description: 探索 Aspose.CAD for Java 轻松调整 CAD 绘图尺寸的强大功能。请遵循我们的分步指南，以实现精确性和适应性。
type: docs
weight: 14
url: /zh/java/cad-file-manipulation/adjusting-cad-drawing-size-using-unit-type/
---
## 介绍

在不断发展的计算机辅助设计 (CAD) 领域，精度和适应性至关重要。一项常见的要求是根据特定的单元类型调整 CAD 图纸的尺寸。 Aspose.CAD for Java 成为一个强大的盟友，提供以编程方式操作 CAD 文件的无缝功能。

## 先决条件

在深入学习本教程之前，请确保您具备以下先决条件：

- Java 开发环境：确保您的计算机上设置了功能齐全的 Java 开发环境。

-  Aspose.CAD for Java 库：下载 Aspose.CAD 库并将其集成到您的 Java 项目中。您可以获取该库[这里](https://releases.aspose.com/cad/java/).

## 导入命名空间

在您的 Java 代码中，包含访问 Aspose.CAD 功能所需的命名空间。添加以下导入：

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

现在，让我们将使用单位类型调整 CAD 绘图尺寸的过程分解为易于管理的步骤：

## 第 1 步：定义数据目录

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

设置 CAD 文件所在目录的路径。

## 第 2 步：加载 CAD 图纸

```java
String sourceFilePath = dataDir + "sample.dwg";
Image image = Image.load(sourceFilePath);
```

使用 Aspose.CAD 加载 CAD 绘图`Image`班级。

## 第 3 步：创建 BMP 选项

```java
BmpOptions bmpOptions = new BmpOptions();
```

实例化`BmpOptions`用于将 CAD 布局导出为 BMP 格式的类。

## 步骤 4：配置光栅化选项

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(cadRasterizationOptions);
```

创建一个实例`CadRasterizationOptions`并将其与`BmpOptions`用于矢量光栅化。

## 第 5 步：设置单位类型

```java
cadRasterizationOptions.setUnitType(UnitType.Centimeter);
```

指定 CAD 绘图所需的单位类型。在此示例中，我们将其设置为厘米。

## 第 6 步：设置布局

```java
cadRasterizationOptions.setLayouts(new String[] { "Model" });
```

定义导出期间要考虑的布局。在本例中，我们选择了“模型”布局。

## 第7步：导出为BMP

```java
String outPath = sourceFilePath + ".bmp";
image.save(outPath, bmpOptions);
```

最后将修改后的CAD图纸保存为BMP格式。

## 结论

借助 Aspose.CAD for Java，调整 CAD 绘图尺寸变得轻而易举。本教程将引导您完成整个过程，强调每个步骤对于获得精确结果的重要性。

## 常见问题解答

### Q1：我可以将 Aspose.CAD for Java 与其他编程语言一起使用吗？

A1：Aspose.CAD 主要支持 Java，但也有适用于其他语言（例如 .NET）的版本。

### 问题 2：Aspose.CAD 是否有任何许可选项？

 A2：是的，您可以探索许可选项并购买 Aspose.CAD[这里](https://purchase.aspose.com/buy).

### Q3：Aspose.CAD 有免费试用版吗？

 A3：当然，您可以免费试用[这里](https://releases.aspose.com/).

### 问题 4：如何获得 Aspose.CAD for Java 的支持？

 A4：访问 Aspose.CAD 论坛[这里](https://forum.aspose.com/c/cad/19)以获得全面的支持。

### Q5：我可以获得 Aspose.CAD 的临时许可证吗？

 A5：是的，您可以获得临时许可证[这里](https://purchase.aspose.com/temporary-license/).