---
date: 2026-02-28
description: 学习如何使用 Aspose.CAD for Java 将 DWG 转换为 PDF、将 DWG 保存为 PDF，并向 DWG 图纸添加文本——一步步指南。
linktitle: Add Text in DWG
second_title: Aspose.CAD Java API
title: 使用 Aspose.CAD for Java 将 DWG 转换为 PDF 并添加文本
url: /zh/java/cad-text-and-annotation/add-text-in-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.CAD for Java 从 DWG 创建 PDF 并添加文本

## 介绍

如果您需要 **create PDF from DWG** 文件并插入自定义文本，您来对地方了。在本教程中，我们将完整演示整个过程——加载 DWG 图纸、添加文本注释，最后使用 Aspose.CAD for Java 将结果保存为 PDF。完成后，您将了解如何 **save DWG as PDF**、自定义文本高度，甚至添加基本注释。

## 快速答案
- **我可以在 Java 中将 DWG 转换为 PDF 吗？** 是的，Aspose.CAD for Java 提供了直接的 API。  
- **我需要许可证才能在生产环境使用吗？** 需要商业许可证；提供免费试用版。  
- **哪种方法向 DWG 添加文本？** 使用 `CadText` 对象并将其添加到模型空间。  
- **我可以设置文本高度吗？** 当然——在 `CadText` 实例上使用 `setTextHeight()`。  
- **输出是矢量的吗？** 当光栅化选项设置为 `UseObjectColor` 时，PDF 保留高质量的矢量数据。

## 什么是“从 DWG 创建 PDF”？
将 DWG 图纸转换为 PDF 意味着把原生 CAD 格式转化为一种广泛支持的只读文档，同时保留原始几何形状。当需要与没有 CAD 软件的利益相关者共享设计时，这种转换尤为重要。

## 为什么使用 Aspose.CAD for Java 将 DWG 转换为 PDF？
Aspose.CAD 提供了纯 Java 解决方案，无需外部 CAD 安装。它支持 **convert DWG to PDF**，保持矢量保真度，并且在转换前允许您以编程方式添加文本、尺寸或自定义图形等注释。

## 先决条件

在开始教程之前，请确保具备以下条件：

- Aspose.CAD for Java Library：从 [Aspose.CAD for Java page](https://releases.aspose.com/cad/java/) 下载并安装库。  
- Java Development Kit (JDK)：确保系统已安装最新的 JDK。  
- DWG Drawing：准备好需要添加文本的 DWG 图纸文件。

## 导入命名空间

在您的 Java 代码中，导入 Aspose.CAD 所需的命名空间：

```java
import com.aspose.cad.Image;


import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadText;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

现在，让我们将提供的代码片段拆分为多个步骤：

## 步骤 1：设置文档目录和 DWG 文件路径

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String dwgPathToFile = dataDir + "SimpleEntites.dwg";
```

## 步骤 2：加载 DWG 图像

```java
Image image = Image.load(dwgPathToFile);
```

## 步骤 3：创建 CadText 对象（向 DWG 添加文本）

```java
CadText cadText = new CadText();
cadText.setStyleType("Standard");
cadText.setDefaultValue("Some custom text");
cadText.setColorId(256);
cadText.setLayerName("0");
cadText.getFirstAlignment().setX(47.9);
cadText.getFirstAlignment().setY(5.56);
cadText.setTextHeight(0.8);          // set text height in DWG units
cadText.setScaleX(0);
```

## 步骤 4：将文本添加到 CadImage（插入注释）

```java
CadImage cadImage = ((CadImage)(image));
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(cadText);
```

## 步骤 5：设置 PDF 选项（准备从 DWG 创建 PDF）

```java
PdfOptions pdfOptions = new PdfOptions();
```

## 步骤 6：配置 CadRasterizationOptions（控制 PDF 渲染）

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
cadRasterizationOptions.setPageHeight(1600);
cadRasterizationOptions.setPageWidth(1600);
cadRasterizationOptions.setLayouts(new String[] {"Model"});
```

## 步骤 7：将修改后的 DWG 保存为 PDF（dwg to pdf java）

```java
image.save(dataDir + "SimpleEntites_generated.dwg.pdf", pdfOptions);
```

通过遵循这些步骤，您将能够 **create PDF from DWG**，添加自定义文本，并控制文本高度——只需几行 Java 代码即可实现。

## 如何在大规模下将 DWG 转换为 PDF（Java）？
如果需要 **batch convert DWG PDF** 文件，可将上述代码包装在遍历 DWG 文件夹的循环中。仅在必要时调整 `pageHeight`/`pageWidth` 以保持低内存占用，并为每个文件复用同一 `PdfOptions` 实例以提升性能。

## 常见问题与技巧

- **文本未显示？** 验证 X/Y 坐标在图纸范围内且图层可见。  
- **文本高度不正确？** 调整 `setTextHeight()`；该值使用图纸的单位系统。  
- **PDF 看起来是光栅化的？** 确保将 `CadDrawTypeMode.UseObjectColor` 设置为保留矢量信息。  
- **大文件的性能如何？** 仅在必要时增加 `pageHeight`/`pageWidth`；更大的值会消耗更多内存。

## 常见问答

**Q: Aspose.CAD 是否兼容所有版本的 DWG 文件？**  
A: Aspose.CAD 支持多种 DWG 版本，确保与广泛的 CAD 软件兼容。

**Q: 我可以自定义添加文本的字体和格式吗？**  
A: 可以，使用 Aspose.CAD 您可以自定义添加到 DWG 文件的文本的字体、样式及其他格式选项。

**Q: 是否提供 Aspose.CAD for Java 的免费试用？**  
A: 是的，您可以通过 [here](https://releases.aspose.com/) 获取免费试用，探索 Aspose.CAD 的功能。

**Q: 在哪里可以找到 Aspose.CAD for Java 的详细文档？**  
A: 请参阅文档 [here](https://reference.aspose.com/cad/java/) 获取深入信息和示例。

**Q: 如何获取 Aspose.CAD 的支持或帮助？**  
A: 访问 [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) 获取帮助并与社区交流。

---

**Last Updated:** 2026-02-28  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}