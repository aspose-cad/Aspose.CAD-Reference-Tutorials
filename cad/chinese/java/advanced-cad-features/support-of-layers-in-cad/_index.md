---
date: 2025-12-13
description: 学习如何在 Java 中使用 Aspose.CAD 将 CAD 保存为 JPEG，添加多个图层，并调整 CAD 尺寸以实现精确的图像转换。
linktitle: Support of Layers in CAD
second_title: Aspose.CAD Java API
title: 在 Java 中将 CAD 保存为 JPEG 并支持图层
url: /zh/java/advanced-cad-features/support-of-layers-in-cad/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 Java 中将 CAD 保存为 JPEG 并支持图层

## 介绍

在本教程中，您将了解如何在 Aspose.CAD for Java 中**将 CAD 保存为 JPEG**并充分利用图层支持。图层可以让您隔离图纸的特定部分，轻松仅导出所需内容。我们将逐步演示，从环境设置到导出仅包含所选图层的 JPEG。

## 快速答案
- **“将 CAD 保存为 JPEG”是什么意思？** 它将 CAD 图纸转换为光栅 JPEG 图像。
- **我可以仅包含选定的图层吗？** 可以——使用 `setLayers` 方法指定要渲染的图层。
- **如何更改图像尺寸？** 在 `CadRasterizationOptions` 中调整 `setPageWidth` 和 `setPageHeight`。
- **这是仅限 Java 的解决方案吗？** 示例使用 Aspose.CAD for Java，但相同概念适用于其他语言。
- **我需要许可证吗？** 免费试用可用于测试；生产环境需要商业许可证。

## 前置条件

在开始之前，请确保您具备以下条件：

1. **Aspose.CAD for Java 库** – 从[网站](https://releases.aspose.com/cad/java/)下载。按照安装指南将 JAR 文件添加到项目的类路径中。  
2. **Java 开发环境** – 在您的机器上安装了近期的 JDK（8 或更高）。

现在我们已经准备就绪，让我们了解实现**将 CAD 保存为 JPEG**并选择性渲染图层的代码。

## 导入命名空间

首先导入所需的 Aspose.CAD 类和标准 Java 实用程序：

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import java.util.ArrayList;
import java.util.Arrays;
import java.util.List;
```

## 步骤指南

### 步骤 1：设置文件路径

定义源 DWF 文件所在位置以及输出 JPEG 将写入的位置。

```java
String dataDir = "Your Document Directory" + "DWFDrawings/";
String srcFile = dataDir + "for_layers_test.dwf";
String outFile = dataDir + "for_layers_test.jpg";
```

### 步骤 2：加载 DWF 图像

使用 Aspose.CAD 的 `Image.load` 方法读取 CAD 图纸。

```java
Image image = Image.load(srcFile);
```

### 步骤 3：配置光栅化选项（调整 CAD 尺寸）

创建 `CadRasterizationOptions` 实例并设置所需的输出尺寸。更改这些值可让您**调整 CAD 尺寸**以生成最终的 JPEG。

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
```

### 步骤 4：指定图层（添加多个图层）

如果您想渲染多个图层，只需将它们的名称添加到列表中。这里我们从名为 “LayerA” 的单个图层开始。

```java
List<String> stringList = new ArrayList<>(Arrays.asList("LayerA"));
rasterizationOptions.setLayers(stringList);
```

*技巧提示：* 要**添加多个图层**，扩展 `Arrays.asList` 调用，例如 `Arrays.asList("LayerA", "LayerB", "LayerC")`。

### 步骤 5：配置 JPEG 选项（Java 转换 CAD 图像）

将光栅化设置绑定到 JPEG 输出格式。

```java
JpegOptions jpegOptions = new JpegOptions();
jpegOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### 步骤 6：导出为 JPG（将 CAD 保存为 JPEG）

最后，将图像写入磁盘。此步骤**将 CAD 图纸保存为仅包含所选图层的 JPEG**文件。

```java
image.save(outFile, jpegOptions);
```

通过遵循这些步骤，您已成功**将 CAD 保存为 JPEG**，并能够控制显示的图层以及自定义图像尺寸。

## 常见问题及解决方案

| 问题 | 解决方案 |
|-------|----------|
| **图层未显示** | 确认图层名称与 DWF 文件中存储的完全一致（区分大小写）。 |
| **输出图像为空** | 确保 `setPageWidth` 和 `setPageHeight` 足够大，以覆盖图纸的范围。 |
| **许可证异常** | 测试时使用试用许可证；在生产环境中获取正式许可证。 |

## 常见问题

**问：我可以向光栅化选项添加多个图层吗？**  
答：当然。通过在 `stringList` 中添加更多图层名称来扩展，例如 `Arrays.asList("LayerA", "LayerB")`。

**问：Aspose.CAD 是否兼容其他 CAD 格式？**  
答：是的，它支持 DWG、DXF、DWF 等多种格式。

**问：如何更改输出图像尺寸？**  
答：修改 `CadRasterizationOptions` 实例中的 `setPageWidth` 和 `setPageHeight`。

**问：在哪里可以购买 Aspose.CAD 的许可证？**  
答：您可以在[此处](https://purchase.aspose.com/buy)查看许可选项。

**问：在哪里可以获得社区支持？**  
答：加入 Aspose.CAD 社区的[论坛](https://forum.aspose.com/c/cad/19)获取帮助和讨论。

---

**最后更新：** 2025-12-13  
**测试环境：** Aspose.CAD for Java 24.11  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}