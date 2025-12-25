---
date: 2025-12-25
description: 学习如何使用 Aspose.CAD for Java 将 DWG 导出为 BMP。本分步指南展示了如何调整 CAD 图纸尺寸并高效地将 CAD
  转换为 BMP。
linktitle: Adjusting CAD Drawing Size Using Unit Type
second_title: Aspose.CAD Java API
title: 将 DWG 导出为 BMP – 使用单位类型调整 CAD 大小（Java）
url: /zh/java/cad-file-manipulation/adjusting-cad-drawing-size-using-unit-type/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 导出 DWG 为 BMP – 使用 Aspose.CAD for Java 的单位类型调整 CAD 绘图尺寸

## 介绍

当您需要 **export DWG to BMP** 时，控制输出尺寸和计量单位对于后续处理或打印至关重要。在本教程中，您将学习如何使用 Aspose.CAD for Java 调整 CAD 绘图尺寸并将 CAD 转换为 BMP，使用 `UnitType` 属性来定义计量单位。步骤以通俗的语言说明，即使您是库的新手也能跟随操作。

## 快速答案
- **“export DWG to BMP” 是什么意思？** 将 DWG 绘图转换为 BMP 栅格图像。  
- **哪个属性控制输出尺寸？** `CadRasterizationOptions.setUnitType()` 设置单位（例如厘米）。  
- **运行代码是否需要许可证？** 免费试用可用于评估；生产环境需要许可证。  
- **我可以选择其他布局吗？** 可以，使用 `setLayouts()` 指定模型或纸空间布局。  
- **支持哪些输出格式？** 除了 BMP，您还可以通过更改选项类导出为 PNG、JPEG、TIFF 等。

## 什么是 **export DWG to BMP**？

将 DWG 导出为 BMP 意味着将基于矢量的 DWG 文件光栅化为位图图像（BMP）。当您需要为旧系统、图像处理流水线或简单显示场景提供像素级精确的表示时，这非常有用。

## 为什么使用 **Unit Type** 调整 CAD 绘图尺寸？

设置单位类型可以让您在不手动计算缩放因子的情况下控制导出图像的实际尺寸。这确保位图符合实际测量（例如厘米），对工程图纸和打印文档至关重要。

## 先决条件

在深入教程之前，请确保已具备以下先决条件：

- **Java 开发环境** – 一个可用的 JDK（8 或更高）以及 IDE 或构建工具（Maven/Gradle）。
- **Aspose.CAD for Java 库** – 下载并将 Aspose.CAD 库集成到您的 Java 项目中。您可以在[此处](https://releases.aspose.com/cad/java/)获取该库。

## 导入命名空间

在您的 Java 代码中，包含访问 Aspose.CAD 功能所需的命名空间。添加以下导入：

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

现在，让我们将使用单位类型调整 CAD 绘图尺寸的过程分解为可管理的步骤：

## 步骤 1：定义数据目录

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

设置存放 CAD 文件的目录路径。

## 步骤 2：加载 CAD 绘图

```java
String sourceFilePath = dataDir + "sample.dwg";
Image image = Image.load(sourceFilePath);
```

使用 Aspose.CAD 的 `Image` 类加载 CAD 绘图。

## 步骤 3：创建 BMP 选项

```java
BmpOptions bmpOptions = new BmpOptions();
```

实例化 `BmpOptions` 类，以将 CAD 布局导出为 BMP 格式。

## 步骤 4：配置光栅化选项

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(cadRasterizationOptions);
```

创建 `CadRasterizationOptions` 实例，并将其与 `BmpOptions` 关联，以进行矢量光栅化。

## 步骤 5：设置单位类型

```java
cadRasterizationOptions.setUnitType(UnitType.Centimeter);
```

为 CAD 绘图指定所需的单位类型。在本例中，我们将其设置为 **Centimeter**（厘米），这会直接影响在 **adjust CAD drawing size** 时导出图像的尺寸。

## 步骤 6：设置布局

```java
cadRasterizationOptions.setLayouts(new String[] { "Model" });
```

定义导出时要考虑的布局。在本例中，我们选择了 **"Model"** 布局，但如果需要也可以切换到纸空间布局。

## 步骤 7：导出为 BMP

```java
String outPath = sourceFilePath + ".bmp";
image.save(outPath, bmpOptions);
```

最后，将修改后的 CAD 绘图保存为 BMP 格式。此步骤完成 **export DWG to BMP** 工作流，同时保留您配置的尺寸调整。

## 常见问题及解决方案

| 问题 | 原因 | 解决办法 |
|-------|--------|-----|
| **输出图像太小** | 未设置单位类型或使用默认（像素） | 调用 `setUnitType()` 并传入所需的计量单位（例如 `UnitType.Centimeter`）。 |
| **导出错误的布局** | 布局名称拼写错误 | 使用 CAD 查看器确认布局名称；在 `setLayouts()` 中使用完全匹配的字符串。 |
| **许可证异常** | 在生产环境中未使用有效许可证运行 | 按照 FAQ 中的说明应用临时或永久许可证。 |

## 常见问题解答（扩展）

**Q: 我可以将 Aspose.CAD for Java 与其他编程语言一起使用吗？**  
A: Aspose.CAD 主要支持 Java，但也提供 .NET 等其他语言的版本。

**Q: Aspose.CAD 有哪些授权选项？**  
A: 有，您可以在[此处](https://purchase.aspose.com/buy)查看授权选项并购买 Aspose.CAD。

**Q: 是否提供 Aspose.CAD 的免费试用？**  
A: 当然，您可以在[此处](https://releases.aspose.com/)获取免费试用。

**Q: 如何获取 Aspose.CAD for Java 的支持？**  
A: 请访问 Aspose.CAD 论坛[此处](https://forum.aspose.com/c/cad/19)获取全面支持。

**Q: 我可以获取 Aspose.CAD 的临时许可证吗？**  
A: 可以，您可以在[此处](https://purchase.aspose.com/temporary-license/)获取临时许可证。

---

**最后更新：** 2025-12-25  
**测试环境：** Aspose.CAD for Java 24.10  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}