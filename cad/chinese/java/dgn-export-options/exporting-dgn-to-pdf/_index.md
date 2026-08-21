---
date: 2026-05-04
description: 学习如何使用 Aspose.CAD for Java 将 DGN 导出为 AutoCAD PDF，以转换 CAD PDF 文件。提供可自定义
  PDF 大小和选项的分步指南。
keywords:
- convert cad pdf
- how to export dgn
- customize pdf size
- aspose cad download
- set pdf options
linktitle: 将AutoCAD格式的DGN导出为PDF
second_title: Aspose.CAD Java API
title: 转换 CAD PDF – 使用 Aspose.CAD for Java 轻松实现 DGN 到 AutoCAD PDF 的导出
url: /zh/java/dgn-export-options/exporting-dgn-to-pdf/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 转换 CAD PDF：使用 Aspose.CAD for Java 轻松将 DGN 导出为 AutoCAD PDF

## 介绍

如果您需要 **转换 CAD PDF** 文件直接从 DGN 源文件，这里就是正确的地方。在本教程中，我们将演示如何使用 Aspose.CAD for Java 将 DGN 文件导出为兼容 AutoCAD 的 PDF。您将看到如何设置自定义页面尺寸、选择特定布局以及微调 PDF 输出——所有代码都清晰、一步步展示，您可以直接复制到自己的项目中。

## 快速回答
- **“convert CAD PDF” 是什么意思？** 它指的是将 CAD 源文件（如 DGN）转换为保留矢量数据和布局精度的 PDF。  
- **哪个库负责转换？** Aspose.CAD for Java 提供了可靠的、免许可证的试用版来完成此任务。  
- **开发时需要许可证吗？** 免费试用可用于测试；生产环境需要商业许可证。  
- **我可以自定义 PDF 大小吗？** 可以 – `CadRasterizationOptions` 允许您设置页面宽度、高度和缩放。  
- **需要多少行代码？** 少于 20 行 Java 代码即可加载、配置并保存 PDF。

## 什么是“convert CAD PDF”？
将 CAD PDF 转换指的是将原生 CAD 图纸（例如 DGN）生成一个保留原始矢量图形、图层和布局信息的 PDF。生成的 PDF 可在任何设备上查看，无需 CAD 软件，非常适合共享、打印或归档。

## 为什么使用 Aspose.CAD for Java 来转换 CAD PDF？
- **完整格式支持** – DGN、DWG、DXF 等多种格式。  
- **无外部依赖** – 纯 Java 实现，无需本机 DLL。  
- **细粒度控制** – 可选择导出哪些布局、设置自定义页面尺寸，并控制光栅化质量。  
- **批量作业可扩展** – 在循环中加载并保存大量文件，开销极小。

## 先决条件
在开始之前，请确保您具备以下条件：

- **Aspose.CAD 库** – 在此下载 [here](https://releases.aspose.com/cad/java/)。  
- **文档目录** – 您机器上的一个文件夹，用于存放输入的 DGN 文件和输出的 PDF。

## 导入包

在您的 Java 项目中，导入访问 Aspose.CAD 功能所需的包：

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

现在，让我们将示例代码拆分为多个步骤：

## 步骤 1：定义文件路径（如何导出 dgn）

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "Nikon_D90_Camera.dgn";
String outFile  = dataDir + "Nikon_D90_Camera.pdf";
```

请将 `"Your Document Directory"` 替换为实际的文件所在路径。

## 步骤 2：加载 DGN 图像

```java
DgnImage objImage = (DgnImage) Image.load(fileName);
```

使用 Aspose.CAD 加载 DGN 文件。

## 步骤 3：设置 PDF 导出选项（自定义 pdf 大小，设置 pdf 选项）

```java
PdfOptions options = new PdfOptions();
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
vectorOptions.setAutomaticLayoutsScaling(true);
vectorOptions.setLayouts(new String[] { "1", "2", "3", "9" }); // Export specific views
options.setVectorRasterizationOptions(vectorOptions);
```

在这里我们定义 PDF 导出选项，包括页面尺寸、自动缩放以及要在最终 PDF 中包含的特定 DGN 布局（视图）。

## 步骤 4：保存 PDF 文件

```java
objImage.save(outFile, options);
```

保存导出的 PDF 文件。`save` 方法会应用前一步配置的所有选项。

对任何其他 DGN 文件重复上述步骤即可。恭喜！您已成功 **convert CAD PDF**，通过 Aspose.CAD for Java 将 DGN 文件导出为 AutoCAD PDF 格式。

## 常见问题及解决方案
| 问题 | 出现原因 | 解决方案 |
|-------|----------------|-----|
| **File not found** | `dataDir` 路径不正确 | 仔细检查文件夹路径并确保 DGN 文件存在。 |
| **Blank pages in PDF** | `AutomaticLayoutsScaling` 设置为 `false` 或缺少布局 ID | 保持 `setAutomaticLayoutsScaling(true)` 并验证布局名称（如 `"1","2",…`）。 |
| **Low‑resolution output** | 默认光栅化 DPI 较低 | 使用 `vectorOptions.setResolution(300);` 提高质量（在 `setVectorRasterizationOptions` 之前添加）。 |
| **License exception** | 生产环境未使用有效许可证 | 按 Aspose 文档说明应用临时或正式许可证。 |

## 常见问题（附加）

**Q: 我可以只导出多布局 DGN 文件中的单个布局吗？**  
A: 可以 – 在 `vectorOptions.setLayouts(new String[] { "2" });` 中指定所需的布局 ID。

**Q: 能否在生成的 PDF 中嵌入字体？**  
A: Aspose.CAD 在光栅化矢量数据时会自动嵌入必要的字体；如有需要，也可以通过 `PdfOptions` 控制字体嵌入。

**Q: 如何批量处理大量 DGN 文件？**  
A: 将上述步骤放入 `for` 循环，遍历文件名列表，对每个文件复用同一个 `PdfOptions` 实例。

**Q: 库是否支持受密码保护的 PDF？**  
A: 支持 – 您可以在 `PdfOptions` 对象上使用 `options.setPassword("yourPassword");` 设置密码。

**Q: 在哪里可以找到更多示例？**  
A: 官方 Aspose.CAD 文档和示例仓库中提供了大量其他场景示例。

## 常见问题（原始）

### Q1: Aspose.CAD 是否兼容所有 CAD 文件格式？

A1: 是的，Aspose.CAD 支持广泛的 CAD 格式，能够灵活处理各种文件类型。

### Q2: 我可以自定义 PDF 导出设置吗？

A2: 当然。正如本教程所示，您可以调整页面尺寸、布局等选项以满足需求。

### Q3: 在哪里可以获得额外的支持或帮助？

A3: 访问 [Aspose.CAD 论坛](https://forum.aspose.com/c/cad/19) 获取社区支持和讨论。

### Q4: 是否提供免费试用？

A4: 是的，您可以在此获取免费试用 [here](https://releases.aspose.com/).

### Q5: 如何获取临时许可证？

A5: 请在此获取临时许可证 [here](https://purchase.aspose.com/temporary-license/).

## 结论

在本教程中，我们探讨了如何通过 Aspose.CAD for Java **convert CAD PDF**。只需几行代码，即可加载 DGN 图纸、微调 PDF 导出选项，并生成高质量的 PDF，适合共享或归档。欢迎尝试不同的页面尺寸、布局或批量处理，以满足项目需求。

---

**Last Updated:** 2026-05-04  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}