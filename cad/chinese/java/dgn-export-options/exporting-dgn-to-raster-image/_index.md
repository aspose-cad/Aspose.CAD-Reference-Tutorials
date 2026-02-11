---
date: 2026-01-10
description: 学习如何使用 Aspose.CAD for Java 将 DGN 文件转换为 JPEG。本分步教程将向您展示如何高效地将 DGN 转换为
  JPEG。
linktitle: Exporting DGN in AutoCAD Format to Raster Image Format
second_title: Aspose.CAD Java API
title: 如何使用 Aspose.CAD for Java 从 DGN 创建 JPEG
url: /zh/java/dgn-export-options/exporting-dgn-to-raster-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.CAD for Java 将 DGN 转换为 JPEG

## 介绍

在本完整指南中，您只需几行 Java 代码即可 **将 DGN 创建为 JPEG** 文件。无论是构建批量转换工具，还是需要将 CAD 图纸显示为网页友好的图像，DGN 转 JPEG 是许多工程和设计工作流的常见需求。我们将逐步演示——从设置 Aspose.CAD 库到保存最终光栅图像——让您能够立即将该解决方案集成到自己的应用程序中。

## 快速回答
- **需要哪个库？** Aspose.CAD for Java  
- **我可以将其他 CAD 格式转换为 JPEG 吗？** 是的，Aspose.CAD 支持多种格式（参见次要关键词 *convert cad to jpeg*）  
- **生产环境需要许可证吗？** 非试用使用需要商业许可证  
- **支持哪个 Java 版本？** Java 8 或更高版本  
- **典型的转换需要多长时间？** 标准尺寸图纸通常在一秒以内完成  

## 什么是“将 DGN 创建为 JPEG”？
将 DGN 文件创建为 JPEG 意味着将基于矢量的 DGN 图纸光栅化为基于像素的图像（JPEG）。此过程在保持视觉保真度的同时，生成轻量级文件，可在浏览器、电子邮件或报告中显示，而无需 CAD 软件。

## 为什么要将 DGN 转换为 JPEG？
- **Easy sharing:** JPEG 在任何设备上均可通用查看。  
- **Performance:** 光栅图像在网页中的加载速度快于矢量 CAD 文件。  
- **Compatibility:** 许多下游工具（例如报表引擎）仅接受光栅格式。  

## 前提条件

在开始之前，请确保您具备以下条件：

1. **Aspose.CAD Library** – 从官方站点 **[here](https://releases.aspose.com/cad/java/)** 下载。  
2. **Java Development Kit (JDK)** – 已在机器上安装 Java 8 或更高版本。  
3. **IDE** – 任意支持 Java 的 IDE，例如 IntelliJ IDEA 或 Eclipse。  

## 导入包

将所需的导入添加到您的 Java 类中：

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

## 步骤指南

### 步骤 1：加载 DGN 文件

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
DgnImage dgnImage = (DgnImage) Image.load(dataDir + "Nikon_D90_Camera.dgn");
```

*说明：* `Image.load` 方法读取源 DGN 文件并返回一个 `DgnImage` 对象，随后我们可以对其进行光栅化。

### 步骤 2：创建 JpegOptions 对象

```java
ImageOptionsBase options = new JpegOptions();
```

*说明：* `JpegOptions` 告诉 Aspose.CAD 输出格式应为 JPEG。它还允许我们附加光栅化设置。

### 步骤 3：配置光栅化设置

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(600);
vectorOptions.setPageHeight(400);
vectorOptions.setNoScaling(true);
vectorOptions.setAutomaticLayoutsScaling(false);
options.setVectorRasterizationOptions(vectorOptions);
```

*说明：* 这些选项定义生成图像的尺寸并控制缩放行为。根据目标分辨率调整 `PageWidth` 和 `PageHeight`。

### 步骤 4：保存转换后的图像

```java
OutputStream outStream = new FileOutputStream(dataDir + "ExportDGNToRasterImage_Out.jpg");
dgnImage.save(outStream, options);
```

*说明：* `save` 方法将光栅化的 JPEG 写入指定的输出流。完成此步骤后，您将拥有一个可直接使用的 JPEG 文件。

> **技巧提示：** 将转换代码放在 try‑with‑resources 块中，以确保流自动关闭。

## 常见使用场景

- **为 CAD 文件浏览器生成缩略图**。  
- **将图纸嵌入 PDF 报告或 HTML 页面**。  
- **对设计档案进行自动批量处理**。  

## 故障排除与常见陷阱

| 问题 | 原因 | 解决方案 |
|------|------|----------|
| 输出图像为空白或白色 | 光栅化选项不正确（例如 `NoScaling` 设置为 true 且页面尺寸不匹配） | 调整 `PageWidth`/`PageHeight` 或将 `NoScaling` 设置为 false |
| 大型 DGN 文件导致内存不足错误 | 在未使用流式处理的情况下加载非常大的文件 | 增加 JVM 堆内存 (`-Xmx`) 或将文件分成更小的块处理 |
| JPEG 质量不足 | 默认 JPEG 质量较低 | 在保存前使用 `((JpegOptions)options).setQuality(100);` |

## 常见问题

### 问题 1：我可以在 Java 中使用 Aspose.CAD 处理其他 CAD 文件格式吗？

A1: 是的，Aspose.CAD 支持多种格式，您可以 **将 CAD 转换为 JPEG** 以及许多其他光栅或矢量输出。

### 问题 2：Aspose.CAD for Java 有免费试用吗？

A2: 是的，您可以在 **[此处](https://releases.aspose.com/)** 获取免费试用。

### 问题 3：在哪里可以找到 Aspose.CAD for Java 的文档？

A3: 请参阅文档 **[此处](https://reference.aspose.com/cad/java/)**。

### 问题 4：如何获取 Aspose.CAD for Java 的支持？

A4: 访问支持论坛 **[此处](https://forum.aspose.com/c/cad/19)**。

### 问题 5：在哪里可以购买 Aspose.CAD for Java 的许可证？

A5: 您可以在 **[此处](https://purchase.aspose.com/buy)** 购买许可证。

## 结论

您现在已经学习了如何使用 Aspose.CAD for Java **将 DGN 创建为 JPEG** 文件。通过遵循上述步骤，您可以将 DGN‑to‑JPEG 转换无缝集成到任何 Java 应用程序中，无论是桌面工具、Web 服务还是自动化流水线。

---

**Last Updated:** 2026-01-10  
**Tested With:** Aspose.CAD for Java 24.11 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}