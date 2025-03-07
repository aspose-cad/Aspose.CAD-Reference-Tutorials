---
title: 使用 Aspose.CAD for Java 将 DWG 导出为 PDF 或光栅
linktitle: 将 DWG 导出为 PDF 或光栅
second_title: Aspose.CAD Java API
description: 探索使用 Aspose.CAD 将 DWG 文件导出为 PDF 或 Java 光栅图像的无缝过程。本分步指南可确保精度和效率。
weight: 13
url: /zh/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.CAD for Java 将 DWG 导出为 PDF 或光栅

## 介绍

在计算机辅助设计 (CAD) 的动态世界中，高效处理图纸至关重要。 Aspose.CAD for Java 提供了将 DWG 文件导出为 PDF 或光栅图像的强大解决方案。本教程将指导您完成整个过程，确保您充分利用 Aspose.CAD for Java 的潜力。

## 先决条件

在深入学习本教程之前，请确保您具备以下条件：

- 对 Java 编程有基本的了解。
- 安装了 Aspose.CAD for Java 库。如果没有，请下载[这里](https://releases.aspose.com/cad/java/).
- 用于测试目的的 DWG 文件。您可以使用提供的“Bottom_plate.dwg”文件。

## 导入命名空间

在您的 Java 项目中，导入必要的命名空间以启动该过程：

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.UnitType;
```

## 第 1 步：加载 DWG 文件

首先使用 Aspose.CAD 加载 DWG 文件`Image`班级：

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Bottom_plate.dwg";
Image objImage = Image.load(srcFile);
```

## 第 2 步：确定单位类型

接下来，检查加载的 DWG 文件的单位类型：

```java
Boolean currentUnitIsMetric = IsMetric(objImage.getUnitType());
int currentUnitCoefficient = objImage.getUnitType();
```

## 第 3 步：设置光栅化选项

根据单位类型，配置光栅化选项：

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();

if (currentUnitIsMetric) {
    //公制单位
    double metersCoeff = 1 / 1000.0;
    double scaleFactor = metersCoeff / currentUnitCoefficient;
    rasterizationOptions.setPageWidth((float)(210 * scaleFactor));
    rasterizationOptions.setPageHeight((float)(297 * scaleFactor));
    rasterizationOptions.setUnitType(UnitType.Millimeter);
} else {
    //英制单位
    rasterizationOptions.setPageWidth((float)(8.27f / currentUnitCoefficient));
    rasterizationOptions.setPageHeight((float)(11.69f / currentUnitCoefficient));
    rasterizationOptions.setUnitType(UnitType.Inch);
}
```

## 步骤 4：配置 PDF 选项

设置 PDF 导出选项：

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());
```

## 第 5 步：另存为 PDF

最后，将 DWG 文件另存为 PDF：

```java
objImage.save(dataDir + "Saved.pdf", pdfOptions);
```

现在你就拥有了！您已使用 Aspose.CAD for Java 成功将 DWG 文件导出为 PDF。

## 结论

本教程提供了有关利用 Aspose.CAD for Java 将 DWG 文件导出为 PDF 或光栅图像的分步指南。该库简化了流程，使您能够在 Java 应用程序中高效地处理 CAD 绘图。

## 常见问题解答

### Q1：我可以将 Aspose.CAD for Java 与其他 Java 框架一起使用吗？

A1：是的，Aspose.CAD for Java 与流行的 Java 框架无缝集成。

### 问题 2：Aspose.CAD for Java 是否有临时许可证？

 A2：是的，您可以获得临时许可证[这里](https://purchase.aspose.com/temporary-license/).

### 问题 3：在哪里可以找到 Aspose.CAD for Java 的支持？

 A3：访问[Aspose.CAD论坛](https://forum.aspose.com/c/cad/19)寻求社区的帮助。

### Q4：如何购买 Aspose.CAD for Java 的许可证？

 A4：您可以购买许可证[这里](https://purchase.aspose.com/buy).

### Q5：Aspose.CAD for Java 支持哪些单位？

A5：Aspose.CAD for Java 支持公制和英制单位。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
