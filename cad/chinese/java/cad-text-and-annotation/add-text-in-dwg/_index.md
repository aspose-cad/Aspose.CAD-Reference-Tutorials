---
date: 2025-12-28
description: 学习如何使用 Aspose.CAD for Java 将 DWG 创建为 PDF、将 DWG 保存为 PDF，并向 DWG 图纸添加文本——一步一步的指南。
linktitle: Add Text in DWG
second_title: Aspose.CAD Java API
title: 使用 Aspose.CAD for Java 将 DWG 转换为 PDF 并添加文本
url: /zh/java/cad-text-and-annotation/add-text-in-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.CAD for Java 将 DWG 转换为 PDF 并添加文本

## 介绍

如果您需要 **从 DWG 创建 PDF** 并插入自定义文本，您来对地方了。在本教程中，我们将完整演示整个过程——加载 DWG 图纸、添加文本注释，最后使用 Aspose.CAD for Java 将结果保存为 PDF。完成后，您将了解如何 **将 DWG 保存为 PDF**、自定义文本高度，甚至添加基本注释。

## 快速回答
- **可以在 Java 中将 DWG 转换为 PDF 吗？** 可以，Aspose.CAD for Java 提供了直接的 API。  
- **生产环境需要许可证吗？** 需要商业许可证；提供免费试用版。  
- **哪种方法向 DWG 添加文本？** 使用 `CadText` 对象并将其添加到模型空间。  
- **可以设置文本高度吗？** 当然——对 `CadText` 实例调用 `setTextHeight()`。  
- **输出是矢量化的吗？** 当光栅化选项设置为 `UseObjectColor` 时，PDF 保留高质量的矢量数据。

## 前置条件

在开始教程之前，请确保已具备以下前置条件：

- Aspose.CAD for Java 库：从 [Aspose.CAD for Java 页面](https://releases.aspose.com/cad/java/) 下载并安装该库。  
- Java 开发工具包 (JDK)：确保系统上已安装最新的 JDK。  
- DWG 图纸：准备好需要添加文本的 DWG 文件。

## 导入命名空间

在 Java 代码中，导入 Aspose.CAD 所需的命名空间：

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

按照这些步骤，您即可 **从 DWG 创建 PDF**、添加自定义文本，并通过几行 Java 代码控制文本高度。

## 为什么要向 DWG 添加文本并转换为 PDF？

直接在 DWG 文件中添加文本对于以下场景非常有用：

- **在设计上做标注**，添加备注或部件编号。  
- **创建可打印文档**，PDF 作为只读、广泛支持的格式。  
- **自动化批量处理** 大型 CAD 库，无需手动编辑。

## 常见问题与技巧

- **文本未显示？** 检查 X/Y 坐标是否在图纸范围内，并确认所在图层可见。  
- **文本高度不正确？** 调整 `setTextHeight()`；该值使用图纸的单位系统。  
- **PDF 看起来是光栅化的？** 确保将 `CadDrawTypeMode.UseObjectColor` 设置为保留矢量信息。  
- **大文件性能如何？** 仅在必要时增大 `pageHeight`/`pageWidth`，更大的值会消耗更多内存。

## 常见问答

**问：Aspose.CAD 是否兼容所有版本的 DWG 文件？**  
答：Aspose.CAD 支持多种 DWG 版本，确保与广泛的 CAD 软件兼容。

**问：我可以自定义添加文本的字体和格式吗？**  
答：可以，使用 Aspose.CAD 可以自定义字体、样式以及其他文本格式选项。

**问：是否有 Aspose.CAD for Java 的免费试用版？**  
答：有，您可以通过 [此处](https://releases.aspose.com/) 获取免费试用。

**问：在哪里可以找到 Aspose.CAD for Java 的详细文档？**  
答：请参阅文档 [此处](https://reference.aspose.com/cad/java/) 获取深入信息和示例。

**问：如何获取 Aspose.CAD 的支持或帮助？**  
答：访问 [Aspose.CAD 论坛](https://forum.aspose.com/c/cad/19) 获取帮助并与社区交流。

---

**最后更新：** 2025-12-28  
**测试环境：** Aspose.CAD for Java 24.12  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}