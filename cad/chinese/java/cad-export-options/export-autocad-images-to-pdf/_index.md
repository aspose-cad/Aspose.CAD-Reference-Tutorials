---
date: 2026-02-20
description: 了解如何使用 Aspose.CAD for Java 导出 AutoCAD PDF。本分步指南向您展示如何 **将 DWG 转换为 PDF**、**将
  CAD 保存为 PDF**，以及如何处理授权。
linktitle: Export AutoCAD Images to PDF
second_title: Aspose.CAD Java API
title: 将 DWG 转换为 PDF - 使用 Aspose.CAD for Java 将 AutoCAD 图像导出为 PDF
url: /zh/java/cad-export-options/export-autocad-images-to-pdf/
weight: 10
---

.

- Then ## Frequently Asked Questions => "## 常见问答"

- Then each Q.

- Then the footer lines: "Last Updated:", "Tested With:", "Author:" translate.

- Then closing shortcodes.

- Then backtop button shortcode.

Make sure to keep markdown formatting.

Let's craft translation.

Be careful with bold formatting: keep **text**.

Also keep code block placeholders as is.

Now produce final answer.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export AutoCAD PDF - Export AutoCAD Images to PDF with Aspose.CAD for Java

## 介绍

您是否正在寻找使用 Java **convert DWG to PDF** 的方法？不必再寻找！在本教程中，我们将手把手演示如何使用 Aspose.CAD for Java 将 AutoCAD 图像导出为 PDF，这是一款强大的库，可让 **convert DWG to PDF** 过程变得轻而易举。完成后，您将了解如何 **save CAD as PDF**、应用自定义光栅化设置，以及在生产环境中使用 Aspose.CAD 许可证。

## 快速答复
- **Can I convert DWG to PDF with Java?** 是的，Aspose.CAD for Java 支持 DWG、DXF 以及许多其他格式。  
- **Do I need a license?** 需要 **Aspose CAD license** 才能无限制使用；评估期间可使用临时许可证。  
- **What Java version is supported?** Java 8+（该库兼容所有现代 JDK）。  
- **Can I customize PDF page size?** 当然——在光栅化选项中调整 `pageWidth` 和 `pageHeight`。  
- **Is 3‑D rasterization possible?** 可以，启用 `TypeOfEntities.Entities3D` 即可实现完整的 3‑D 渲染。

## 什么是 **export autocad pdf**？
Exporting AutoCAD PDF 指将基于矢量的 CAD 图纸（DWG、DXF、DWF 等）转换为可移植的 PDF 文档，同时保留图层、线宽，并可选地保留 3‑D 几何信息。这对于与客户共享设计、归档或在无需 CAD 软件的情况下打印非常有用。

## 为什么使用 Aspose.CAD for Java 将 DWG 转换为 PDF？
- **Full format support** – 支持 DWG、DXF、DWF 等多种格式。  
- **No external dependencies** – 纯 Java 库，无需本机 DLL。  
- **High‑quality rasterization** – 可控制 DPI、页面尺寸和布局，轻松 **customize PDF page size** 以满足项目需求。  
- **License flexibility** – 可先使用免费试用版，随后升级为永久 **Aspose CAD license**。  

## 前置条件

在开始之前，请确保您已具备：

- **Java Development Environment** – 已安装 JDK 8 或更高版本。  
- **Aspose.CAD for Java Library** – 从 [download link](https://releases.aspose.com/cad/java/) 下载。  
- **Document Directory** – 在本机上创建一个文件夹，用于存放源 CAD 文件和生成的 PDF。

## 导入命名空间

在您的 Java 项目中，导入使用 Aspose.CAD 所需的类：

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

现在让我们一步步浏览代码。

## 如何使用 Aspose.CAD for Java 将 DWG 转换为 PDF

### 步骤 1：设置资源目录路径

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
```

> **Pro tip:** 将 `"Your Document Directory"` 替换为您在前置条件中创建的文件夹的绝对路径。

### 步骤 2：加载 CAD 图像

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

> **Why this matters:** 将 CAD 文件加载到 `Image` 对象中，可让您完整访问 Aspose.CAD 的光栅化引擎。

### 步骤 3：设置光栅化选项

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setPageHeight(500);
// rasterizationOptions.setTypeOfEntities(TypeOfEntities.Entities3D);

rasterizationOptions.setLayouts(new String[] {"Model"});
```

- 调整 `pageWidth` 和 `pageHeight` 以 **customize PDF page size**。  
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

生成的文件 `Export3DImagestoPDF_out_.pdf` 是您原始 AutoCAD 图纸的 **save cad as pdf** 表现形式。

## 常见问题与解决方案

| 症状 | 可能原因 | 解决办法 |
|------|----------|----------|
| 空白 PDF 输出 | 未设置光栅化选项或布局不匹配 | 确认 `setLayouts` 与 CAD 文件中的布局名称一致。 |
| 低分辨率图像 | `pageWidth`/`pageHeight` 设置过小 | 增大尺寸或通过 `rasterizationOptions.setResolution(...)` 提高 DPI。 |
| 许可证异常 | 未应用有效许可证 | 应用 **Aspose CAD license**，或使用临时许可证进行测试。 |

## 常见问答

### Q1: Can I use Aspose.CAD for Java with other CAD file formats?
A1: Yes, Aspose.CAD supports a wide range of formats including DWG, DWF, DGN, and more, giving you flexibility in your projects.

### Q2: How can I obtain a temporary license for Aspose.CAD for Java?
A2: Visit [here](https://purchase.aspose.com/temporary-license/) to obtain a temporary license for evaluation.

### Q3: Are there any layout options for rasterization?
A3: Yes, you can customize layouts (e.g., `"Model"`, `"Layout1"`) through the `setLayouts` method to control which view is rendered.

### Q4: Can I customize the size of the output PDF file?
A4: Absolutely! Adjust the `pageWidth` and `pageHeight` parameters in the rasterization options to fit your desired dimensions.

### Q5: Where can I seek help or discuss issues related to Aspose.CAD for Java?
A5: Head over to the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for dedicated support and community discussions.

---

**Last Updated:** 2026-02-20  
**Tested With:** Aspose.CAD for Java 24.10  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}