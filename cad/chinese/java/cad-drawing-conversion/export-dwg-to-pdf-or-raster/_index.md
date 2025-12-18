---
date: 2025-12-18
description: 探索如何使用 Aspose.CAD 在 Java 中将 DWG 导出为 PDF 或光栅图像。本分步指南确保精确、高效，并轻松实现 DWG
  文件的转换。
linktitle: Export DWG to PDF or Raster
second_title: Aspose.CAD Java API
title: 使用 Aspose.CAD for Java 将 DWG 导出为 PDF 或光栅
url: /zh/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.CAD for Java 将 DWG 导出为 PDF 或光栅图像

## 介绍

在计算机辅助设计（CAD）日新月异的领域，图纸的高效处理至关重要。借助 **Aspose.CAD for Java**，您可以仅用几行代码 **将 dwg 导出为 pdf** — 或光栅图像 — 。本教程将带您完整演示从加载 DWG 文件到生成高质量 PDF 的全过程，并阐明为何 Aspose.CAD Java 是 CAD 转换任务的首选库。

## 快速答疑
- **本教程覆盖哪些内容？** 使用 Aspose.CAD for Java 将 DWG 文件导出为 PDF 或光栅图像。  
- **需要许可证吗？** 提供免费临时许可证用于评估；正式生产环境需购买完整许可证。  
- **支持哪个 Java 版本？** 任意 Java 8+ 运行时均可使用最新的 Aspose.CAD Java API。  
- **可以将 DWG 转换为其他图像格式吗？** 可以——相同的光栅化选项支持输出 PNG、JPEG、BMP 等。  
- **转换耗时多久？** 对于普通图纸通常在一秒以内；大型文件可能需要几秒。

## 什么是 “export dwg to pdf”？
将 DWG 导出为 PDF 即把原生 AutoCAD 图纸转换为便携、与设备无关的 PDF 文档。生成的 PDF 保留矢量数据、图层和比例，适合共享、打印或归档。

## 为什么使用 Aspose.CAD Java 进行此转换？
- **无外部依赖** – 纯 Java 实现，无需本机 DLL。  
- **精确的单位处理** – 自动遵循公制或英制单位。  
- **高质量光栅输出** – 可细调 DPI 与页面尺寸。  
- **完整的 PDF 支持** – 在不依赖额外库的情况下生成保留矢量的 PDF。

## 前置条件

在开始编写代码之前，请确保您已具备：

- 基本的 Java 编程知识。  
- 已安装 Aspose.CAD for Java 库。若尚未下载，请前往 **[here](https://releases.aspose.com/cad/java/)** 获取。  
- 用于测试的 DWG 文件——本指南使用示例 **Bottom_plate.dwg**。

## 导入命名空间

在 Java 项目中，引入必要的类以启动转换：

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.UnitType;
```

## 步骤指南

### 步骤 1：加载 DWG 文件

首先，使用 `Image` 类加载 DWG 图纸。这会在内存中创建 Aspose.CAD 可操作的表示。

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Bottom_plate.dwg";
Image objImage = Image.load(srcFile);
```

### 步骤 2：确定单位类型

了解图纸使用的是公制还是英制单位对于正确缩放至关重要。辅助方法 `IsMetric`（此处省略实现）返回布尔标志。

```java
Boolean currentUnitIsMetric = IsMetric(objImage.getUnitType());
int currentUnitCoefficient = objImage.getUnitType();
```

### 步骤 3：设置光栅化选项

根据单位体系，配置页面尺寸、缩放比例以及目标单位类型。这些选项决定了 DWG 在包装成 PDF 前的光栅化方式。

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();

if (currentUnitIsMetric) {
    // Metric units
    double metersCoeff = 1 / 1000.0;
    double scaleFactor = metersCoeff / currentUnitCoefficient;
    rasterizationOptions.setPageWidth((float)(210 * scaleFactor));
    rasterizationOptions.setPageHeight((float)(297 * scaleFactor));
    rasterizationOptions.setUnitType(UnitType.Millimeter);
} else {
    // Imperial units
    rasterizationOptions.setPageWidth((float)(8.27f / currentUnitCoefficient));
    rasterizationOptions.setPageHeight((float)(11.69f / currentUnitCoefficient));
    rasterizationOptions.setUnitType(UnitType.Inch);
}
```

### 步骤 4：配置 PDF 选项

创建 `PdfOptions` 实例并附加光栅化设置。这样 Aspose.CAD 就知道如何将光栅化内容嵌入最终的 PDF。

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());
```

### 步骤 5：保存为 PDF

最后，将图纸导出为 PDF 文件。`save` 方法接受输出路径和已配置的 `PdfOptions`。

```java
objImage.save(dataDir + "Saved.pdf", pdfOptions);
```

代码执行完毕后，您将在 `DWGDrawings` 文件夹中看到 **Saved.pdf**，即可用于分发或归档。

## 常见问题与技巧

- **页面尺寸不正确** – 仔细检查单位转换逻辑；系数不匹配会导致页面过大。  
- **缺少字体或线宽** – 在转换前确保 DWG 已引用所有外部资源。  
- **大图纸的性能** – 仅在需要更高质量时提升 `CadRasterizationOptions` 中的 `DPI`，降低 DPI 可加快处理速度。

## 常见问答

**Q: Aspose.CAD for Java 能与其他 Java 框架一起使用吗？**  
A: 能，Aspose.CAD for Java 可无缝集成到 Spring、Jakarta EE、Android 等流行框架中。

**Q: 是否提供 Aspose.CAD for Java 的临时许可证？**  
A: 提供，您可以在 **[here](https://purchase.aspose.com/temporary-license/)** 获取临时许可证。

**Q: 在哪里可以获得 Aspose.CAD for Java 的技术支持？**  
A: 访问 **[Aspose.CAD forum](https://forum.aspose.com/c/cad/19)**，获取社区和 Aspose 工程师的帮助。

**Q: 如何购买 Aspose.CAD for Java 的许可证？**  
A: 请前往 **[here](https://purchase.aspose.com/buy)** 进行购买。

**Q: Aspose.CAD for Java 支持哪些单位？**  
A: 支持公制和英制单位，并会自动检测图纸的单位体系。

**Q: 能否使用相同的 API 将 DWG 转换为其他图像格式（如 PNG、JPEG）？**  
A: 完全可以。将 `PdfOptions` 替换为相应的光栅图像选项（例如 `PngOptions`），并复用相同的 `CadRasterizationOptions`。

## 结论

本教程演示了如何使用 Aspose.CAD for Java **将 dwg 导出为 pdf** 以及光栅图像。通过遵循上述步骤，您可以在任何 Java 应用中集成可靠的 CAD 转换功能，无论是用于文档的 PDF，还是用于网页显示的光栅图像。

---

**最后更新：** 2025-12-18  
**测试环境：** Aspose.CAD for Java 24.10  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}