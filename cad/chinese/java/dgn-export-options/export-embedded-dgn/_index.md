---
date: 2026-01-07
description: 了解如何使用 Aspose.CAD for Java 将 CAD 导出为 PDF 并将 DGN 转换为 PDF。面向 Java 开发者的逐步指南。
linktitle: Export Embedded DGN
second_title: Aspose.CAD Java API
title: 将 CAD 导出为 PDF – 使用 Aspose.CAD for Java 导出嵌入的 DGN
url: /zh/java/dgn-export-options/export-embedded-dgn/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 将 CAD 导出为 PDF – 使用 Aspose.CAD for Java 导出嵌入式 DGN

## 介绍

在本教程中，您将了解 **如何通过将嵌入的 DGN 文件转换为高质量 PDF 文档** 来实现 CAD 导出为 PDF。Aspose.CAD 是一个强大的库，为 Java 开发者提供对 CAD 文件操作的完整控制，无论您是需要 **将 DGN 转换为 PDF**、**将 DWG 转换为 PDF**，还是仅仅在其他格式中渲染 CAD 图纸。按照下面的分步指南操作，您即可在几分钟内将此功能集成到您的应用程序中。

## 快速答案
- **“将 CAD 导出为 PDF”是什么意思？** 它将 CAD 图纸（DWG、DGN 等）转换为 PDF 文件，同时保留矢量质量。  
- **使用的库是什么？** Aspose.CAD for Java。  
- **需要许可证吗？** 生产环境需要许可证；提供免费试用版。  
- **主要前置条件是什么？** Java 开发环境和 Aspose.CAD for Java JAR 包。  
- **可以自定义输出吗？** 可以 – 您可以选择布局、设置光栅化选项以及控制 PDF 设置。

## 什么是 “将 CAD 导出为 PDF”？
将 CAD 导出为 PDF 意味着将原生 CAD 文件（如 DWG 或 DGN）生成一个 PDF 文档，忠实呈现原始几何形状。该 PDF 可在任何平台上查看，无需 CAD 软件，非常适合共享、打印或归档。

## 为什么使用 Aspose.CAD for Java 将 DGN 转换为 PDF？
- **无外部依赖** – 完全在 Java 中运行。  
- **保留矢量数据** – PDF 在任何缩放级别下都保持清晰。  
- **细粒度控制** – 可选择特定布局、设置光栅化 DPI 并嵌入字体。  
- **企业级** – 支持大文件、批处理以及多种授权方式。

## 前置条件

在开始之前，请确保您具备以下条件：

- **Java 开发环境** – 已安装并配置 JDK 8 或更高版本。  
- **Aspose.CAD for Java** – 从 [here](https://releases.aspose.com/cad/java/) 下载最新的 JAR 包。  

## 导入包

要开始使用，您需要在 Java 项目中导入必要的类。将以下 import 语句添加到源文件中：

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

## 如何使用 Aspose.CAD for Java 将 DGN 导出为 PDF？

下面是一段清晰的、编号的操作步骤，展示如何将嵌入在 DWG 中的 DGN 文件转换为 PDF。

### 步骤 1：设置输入和输出路径

定义包含源文件的目录，并指定包含嵌入 DGN 的 DWG 文件。

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
```

### 步骤 2：加载 DWG 文件

将 DWG 文件加载到 `Image` 对象中。Aspose.CAD 会自动检测嵌入的 DGN 数据。

```java
Image objImage = Image.load(fileName);
```

### 步骤 3：配置光栅化选项

选择要在 PDF 中包含的布局。本例仅导出 **Model** 布局。

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setLayouts(new String[] {"Model"});
```

### 步骤 4：配置 PDF 选项

将光栅化设置附加到 PDF 导出选项中。

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### 步骤 5：保存 PDF 文件

使用配置好的选项将 PDF 写入磁盘。

```java
objImage.save(dataDir + "BlockRefDgn.pdf", pdfOptions);
```

## 将 DWG 转换为 PDF – 额外提示

如果您的源文件是普通 DWG（未嵌入 DGN），完全可以复用上述代码——只需将 `fileName` 更改为指向要转换的 DWG。光栅化和 PDF 选项保持不变，为您提供一致的 **将 DWG 转换为 PDF** 工作流。

## 常见问题及解决方案

| 问题 | 原因 | 解决方案 |
|-------|--------|----------|
| **PDF 输出为空白** | 布局名称不匹配 | 确认传递给 `setLayouts` 的布局名称与源文件中的布局完全一致（区分大小写）。 |
| **许可证异常** | 使用试用版未加载许可证 | 在加载图像前应用有效的 Aspose.CAD 许可证 (`License license = new License(); license.setLicense("Aspose.CAD.lic");`)。 |
| **文件未找到** | `dataDir` 路径错误 | 使用绝对路径或确保相对路径相对于项目工作目录是正确的。 |
| **图形分辨率低** | 默认光栅化 DPI 较低 | 设置 `rasterizationOptions.setPageWidth/Height` 或 `setResolution` 以提升 DPI。 |

## 常见问答

**问：可以在商业项目中使用 Aspose.CAD for Java 吗？**  
答：可以，Aspose.CAD for Java 是商业库。您可以在 [here](https://purchase.aspose.com/buy) 获取许可证。

**问：是否提供免费试用？**  
答：提供，您可以在 [here](https://releases.aspose.com/) 获取 Aspose.CAD for Java 的免费试用版。

**问：如何获取 Aspose.CAD for Java 的支持？**  
答：您可以在 [forum](https://forum.aspose.com/c/cad/19) 上的 Aspose.CAD 社区寻求帮助。

**问：如果需要临时许可证怎么办？**  
答：您可以在 [here](https://purchase.aspose.com/temporary-license/) 获取临时许可证。

**问：文档在哪里可以找到？**  
答：文档可在 [here](https://reference.aspose.com/cad/java/) 查看。

## 结论

现在，您已经学会了如何 **将 CAD 导出为 PDF**，特别是如何 **将 DGN 转换为 PDF**，以及 **将 DWG 转换为 PDF**，全部使用 Aspose.CAD for Java。按照上述步骤操作，您即可在任何基于 Java 的解决方案中无缝集成 CAD 到 PDF 的转换，为用户提供高质量的 PDF，而无需额外的 CAD 软件。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**最后更新：** 2026-01-07  
**测试环境：** Aspose.CAD for Java 24.12  
**作者：** Aspose