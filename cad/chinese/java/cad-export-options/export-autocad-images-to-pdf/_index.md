---
date: 2025-12-19
description: 了解如何使用 Aspose.CAD for Java 导出 AutoCAD PDF。本分步指南展示了如何将 DWG 转换为 PDF、将 CAD
  保存为 PDF，以及如何处理授权。
linktitle: Export AutoCAD Images to PDF
second_title: Aspose.CAD Java API
title: 导出 AutoCAD PDF - 使用 Aspose.CAD for Java 教程将 AutoCAD 图像导出为 PDF
url: /zh/java/cad-export-options/export-autocad-images-to-pdf/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 导出 AutoCAD PDF - 使用 Aspose.CAD for Java 将 AutoCAD 图像导出为 PDF

## 介绍

您是否想要使用 Java 无缝 **导出 AutoCAD PDF**？不必再寻找！在本教程中，我们将演示如何使用 Aspose.CAD for Java 将 AutoCAD 图像转换为 PDF，这是一款强大的库，可让 **convert DWG to PDF** 过程轻而易举。完成后，您将了解如何 **save CAD as PDF**、应用自定义光栅化设置，并在生产环境中使用 Aspose.CAD 许可证。

## 快速答复
- **我可以使用 Java 将 DWG 转换为 PDF 吗？** 是的，Aspose.CAD for Java 支持 DWG、DXF 以及许多其他格式。  
- **我需要许可证吗？** 需要 **Aspose CAD license** 才能无限制使用；评估期间可使用临时许可证。  
- **支持哪个 Java 版本？** Java 8+（该库兼容所有现代 JDK）。  
- **我可以自定义 PDF 页面大小吗？** 当然——在光栅化选项中调整 `pageWidth` 和 `pageHeight`。  
- **是否支持 3‑D 光栅化？** 是的，启用 `TypeOfEntities.Entities3D` 可实现完整的 3‑D 渲染。

## 什么是 **export autocad pdf**？
导出 AutoCAD PDF 指将基于矢量的 CAD 图纸（DWG、DXF、DWF 等）转换为可移植的 PDF 文档，同时保留图层、线宽，并可选地保留 3‑D 几何。此功能适用于与客户共享设计、归档或在无需 CAD 软件的情况下打印。

## 为什么使用 Aspose.CAD for Java 来 **export autocad pdf**？
- **完整格式支持** – 支持 DWG、DXF、DWF 等多种格式。  
- **无外部依赖** – 纯 Java 库，无需本机 DLL。  
- **高质量光栅化** – 可控制 DPI、页面尺寸和布局。  
- **许可证灵活** – 可先使用免费试用版，再升级为永久 **Aspose CAD license**。  

## 先决条件

在开始之前，请确保您具备：

- **Java 开发环境** – 已安装 JDK 8 或更高版本。  
- **Aspose.CAD for Java 库** – 从 [download link](https://releases.aspose.com/cad/java/) 下载。  
- **文档目录** – 您机器上的一个文件夹，用于存放源 CAD 文件和生成的 PDF。

## 导入命名空间

在您的 Java 项目中，导入使用 Aspose.CAD 所需的类：

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

现在让我们一步步查看代码。

## 分步指南

### 步骤 1：设置资源目录路径

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
```

> **小贴士：** 将 `"Your Document Directory"` 替换为您在先决条件中创建的文件夹的绝对路径。

### 步骤 2：加载 CAD 图像

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

> **为什么这很重要：** 将 CAD 文件加载到 `Image` 对象后，您即可完整访问 Aspose.CAD 的光栅化引擎。

### 步骤 3：设置光栅化选项

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setPageHeight(500);
// rasterizationOptions.setTypeOfEntities(TypeOfEntities.Entities3D);

rasterizationOptions.setLayouts(new String[] {"Model"});
```

- 调整 `pageWidth` 和 `pageHeight` 以改变输出 PDF 的尺寸。  
- 如需 **java convert cad pdf** 的 3‑D 实体，请取消注释 `setTypeOfEntities` 行。  
- `setLayouts` 调用用于选择要渲染的布局（Model、Layout1 等）。

### 步骤 4：配置 PDF 选项

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

此步骤将光栅化设置绑定到 PDF 输出，确保矢量数据被正确转换。

### 步骤 5：保存 PDF

```java
cadImage.save(dataDir + "Export3DImagestoPDF_out_.pdf", pdfOptions);
```

生成的文件 `Export3DImagestoPDF_out_.pdf` 是您原始 AutoCAD 图纸的 **save CAD as PDF** 表现形式。

## 常见问题与解决方案

| 症状 | 可能原因 | 解决办法 |
|------|----------|----------|
| PDF 空白输出 | 未设置光栅化选项或布局不匹配 | 验证 `setLayouts` 与 CAD 文件中的布局名称匹配。 |
| 低分辨率图像 | `pageWidth`/`pageHeight` 过小 | 增大尺寸或通过 `rasterizationOptions.setResolution(...)` 设置更高 DPI。 |
| 许可证异常 | 未应用有效许可证 | 应用 **Aspose CAD license** 或使用临时许可证进行测试。 |

## 常见问答

### Q1: 我可以在 Java 中使用 Aspose.CAD 处理其他 CAD 文件格式吗？
A1: 可以，Aspose.CAD 支持包括 DWG、DWF、DGN 在内的多种格式，为您的项目提供灵活性。

### Q2: 如何获取 Aspose.CAD for Java 的临时许可证？
A2: 访问 [here](https://purchase.aspose.com/temporary-license/) 获取用于评估的临时许可证。

### Q3: 光栅化是否有布局选项？
A3: 有，您可以通过 `setLayouts` 方法自定义布局（例如 `"Model"`、`"Layout1"`），以控制渲染的视图。

### Q4: 我可以自定义输出 PDF 文件的大小吗？
A4: 完全可以！在光栅化选项中调整 `pageWidth` 和 `pageHeight` 参数，以满足所需尺寸。

### Q5: 我在哪里可以获取帮助或讨论与 Aspose.CAD for Java 相关的问题？
A5: 前往 [Aspose.CAD 论坛](https://forum.aspose.com/c/cad/19) 获取专门的支持和社区讨论。

---

**最后更新：** 2025-12-19  
**测试环境：** Aspose.CAD for Java 24.10  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}