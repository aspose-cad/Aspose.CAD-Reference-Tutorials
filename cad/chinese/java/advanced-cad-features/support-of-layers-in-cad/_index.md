---
date: 2026-02-17
description: 学习如何在 Java 中使用 Aspose.CAD 将 DWG 保存为 JPEG，添加多个图层，并调整 CAD 尺寸以实现精确的图像转换。
linktitle: Support of Layers in CAD
second_title: Aspose.CAD Java API
title: 在 Java 中将 DWG 保存为带图层支持的 JPEG
url: /zh/java/advanced-cad-features/support-of-layers-in-cad/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 将 DWG 保存为带图层支持的 JPEG（Java）

## 介绍

在本教程中，您将学习如何 **save DWG as JPEG**，并充分利用 Aspose.CAD for Java 的图层支持。图层可以将图纸的特定部分隔离开来，便于仅导出所需内容。我们将逐步演示，从环境搭建到导出仅包含所选图层的 JPEG。

## 快速解答
- **“save DWG as JPEG” 是什么意思？** 它将 DWG（或其他 CAD）图纸转换为光栅 JPEG 图像。  
- **我可以只包含选定的图层吗？** 可以——使用 `setLayers` 方法指定要渲染的图层。  
- **如何更改图像尺寸？** 在 `CadRasterizationOptions` 中调整 `setPageWidth` 和 `setPageHeight`。  
- **这是仅限 Java 的解决方案吗？** 示例使用 Aspose.CAD for Java，但相同的概念适用于其他语言。  
- **我需要许可证吗？** 免费试用可用于测试；生产环境需要商业许可证。

## 什么是 “save DWG as JPEG”？

将 DWG 保存为 JPEG 意味着将矢量 CAD 文件（DWG、DWF、DXF 等）光栅化为标准的 JPEG 位图。当您需要在仅支持光栅图像的网页、电子邮件或报告中嵌入 CAD 图纸时，这非常有用。

## 为什么使用支持图层的 JPEG 转换？

- **关注相关数据：**仅导出所需的图层，减少文件大小和视觉杂乱。  
- **保持设计意图：**图层保留对象的逻辑分组，您可以使用相同的源文件生成不同的输出。  
- **完全控制尺寸：**通过调整光栅化选项，您可以生成符合发布需求的高分辨率图像。

## 前提条件

在开始之前，请确保具备以下条件：

1. **Aspose.CAD for Java Library** – 从[网站](https://releases.aspose.com/cad/java/)下载。按照安装指南将 JAR 文件添加到项目的 classpath 中。  
2. **Java 开发环境** – 在机器上安装了最近的 JDK（8 或更高）。

现在我们已经准备就绪，下面来了解实现 **save DWG as JPEG** 并进行选择性图层渲染所需的代码。

## 导入命名空间

首先导入所需的 Aspose.CAD 类和标准 Java 工具：

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

定义源 DWF 文件所在位置以及输出 JPEG 的写入路径。

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

创建 `CadRasterizationOptions` 实例并设置期望的输出尺寸。更改这些值即可 **adjust CAD dimensions**，以获得最终的 JPEG。

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
```

### 步骤 4：指定图层（添加多个图层）

如果想渲染多个图层，只需将它们的名称添加到列表中。这里我们从单个名为 “LayerA” 的图层开始。

```java
List<String> stringList = new ArrayList<>(Arrays.asList("LayerA"));
rasterizationOptions.setLayers(stringList);
```

*技巧：* 要 **add multiple layers**，展开 `Arrays.asList` 调用，例如 `Arrays.asList("LayerA", "LayerB", "LayerC")`。这可以 **select specific CAD layers** 进行转换。

### 步骤 5：配置 JPEG 选项（Java 转换 CAD 图像）

将光栅化设置绑定到 JPEG 输出格式。

```java
JpegOptions jpegOptions = new JpegOptions();
jpegOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### 步骤 6：导出为 JPG（Save DWG as JPEG）

最后，将图像写入磁盘。此步骤 **saves the CAD drawing as a JPEG**，并仅包含所选图层。

```java
image.save(outFile, jpegOptions);
```

通过以上步骤，您已成功 **save DWG as JPEG**，并可控制显示的图层以及自定义图像尺寸。

## 如何在选择图层的情况下将 DWF 转换为 JPEG

虽然示例使用 DWF 作为源文件，但相同的光栅化管道适用于任何受支持的 CAD 格式（DWG、DXF、DGN 等）。只需在 `srcFile` 中更改文件扩展名，库即可自动完成 **convert DWF to JPEG**（或其他格式）的操作。

## 常见问题及解决方案

| 问题 | 解决方案 |
|-------|----------|
| **Layers not appearing** | 验证图层名称与 DWF 文件中存储的名称完全匹配（区分大小写）。 |
| **Output image is blank** | 确保 `setPageWidth` 和 `setPageHeight` 足够大，以覆盖图纸的范围。 |
| **License exception** | 使用试用许可证进行测试；生产环境请获取正式许可证。 |

## 常见问答

**Q: 我可以向光栅化选项中添加多个图层吗？**  
A: 当然可以。扩展 `stringList`，加入更多图层名称，例如 `Arrays.asList("LayerA", "LayerB")`。

**Q: Aspose.CAD 是否兼容其他 CAD 格式？**  
A: 是的，它支持 DWG、DXF、DWF 等多种格式。

**Q: 如何更改输出图像的尺寸？**  
A: 在 `CadRasterizationOptions` 实例中修改 `setPageWidth` 和 `setPageHeight`。

**Q: 在哪里可以购买 Aspose.CAD 的许可证？**  
A: 您可以在[此处](https://purchase.aspose.com/buy)了解许可选项。

**Q: 哪里可以获得社区支持？**  
A: 加入 Aspose.CAD 社区的[论坛](https://forum.aspose.com/c/cad/19)获取帮助和讨论。

---

**最后更新：** 2026-02-17  
**测试环境：** Aspose.CAD for Java 24.11  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}