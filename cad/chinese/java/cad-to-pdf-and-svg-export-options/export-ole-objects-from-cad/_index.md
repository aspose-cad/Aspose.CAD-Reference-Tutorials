---
date: 2026-01-04
description: 学习如何使用 Aspose.CAD for Java 将 CAD 保存为 PNG，并轻松导出 CAD 文件中的 OLE 对象。快速设置、完整代码示例以及最佳实践技巧。
linktitle: Export OLE Objects from CAD
second_title: Aspose.CAD Java API
title: 使用 Aspose.CAD for Java 将 CAD 保存为 PNG 并导出 OLE 对象
url: /zh/java/cad-to-pdf-and-svg-export-options/export-ole-objects-from-cad/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 保存 CAD 为 PNG 并导出 OLE 对象使用 Aspose.CAD for Java

## 介绍

在快速发展的计算机辅助设计（CAD）领域，能够 **保存 CAD 为 PNG** 并提取嵌入的 OLE（对象链接与嵌入）对象可以显著简化工作流程。无论您是构建批量转换工具、为 Web 门户生成缩略图，还是仅需归档 OLE 内容，Aspose.CAD for Java 都提供了一种简洁的编程方式来实现。在本教程中，我们将从项目设置到将每个 OLE 对象导出为 PNG 图像，完整演示整个过程。

## 快速回答
- **可以直接将 OLE 对象导出为 PNG 吗？** 可以 – Aspose.CAD 加载 CAD 文件并允许您将每个布局光栅化为 PNG。  
- **需要哪个 Java 版本？** Java 8 或更高版本。  
- **此功能需要许可证吗？** 免费试用可用于评估；生产环境需要许可证。  
- **矢量数据会被保留吗？** PNG 光栅化保持视觉保真度，但输出为光栅图像，而非矢量。  
- **支持批量处理吗？** 完全支持 – 如代码示例所示，可遍历文件数组进行处理。

## 前提条件

在开始之前，请确保具备以下条件：

- **Java Development Kit (JDK)** – 已安装并配置 Java 8+。  
- **Aspose.CAD for Java** – 从 [download link](https://releases.aspose.com/cad/java/) 下载最新库。  
- **CAD 源文件** – 包含您想要导出的 OLE 对象的任意 DWG/DXF/DGN 文件。

## 导入命名空间

要处理 CAD 文件，需要导入 Aspose.CAD 的核心类。请保持导入块与示例完全一致——它提供了后续教程中使用的类。

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

## 如何将 CAD 保存为 PNG

下面是一份简明的分步指南，展示 **如何导出 OLE 对象并保存 CAD 为 PNG**。每一步都包含简短说明以及需要复制到项目中的完整代码。

### 步骤 1：设置文档目录

定义存放 CAD 图纸的文件夹。将占位符替换为您机器上的实际路径。

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

### 步骤 2：定义 CAD 文件名

列出所有需要处理的 CAD 文件。您可以根据需要添加任意数量的条目。

```java
String[] files = new String[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

### 步骤 3：设置 PNG 导出选项

配置光栅化设置。此处我们针对特定布局（`Layout1`）并使用默认的 PNG 选项。

```java
PngOptions pngOptions = new PngOptions();
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.setVectorRasterizationOptions(rasterizationOptions);
rasterizationOptions.setLayouts(new String[] { "Layout1" });
```

### 步骤 4：遍历 CAD 文件并保存为 PNG

加载每个 CAD 文件，光栅化 OLE 对象，并写入输出 PNG 文件。`_out.png` 后缀有助于您识别生成的图像。

```java
for(String file : files)
{
    CadImage cadImage = (CadImage)Image.load(dataDir + file);
    cadImage.save(dataDir + file + "_out.png", pngOptions);
}
```

## 常见问题及解决方案

| Problem | Why it Happens | Fix |
|---------|----------------|-----|
| **`Image.load` throws `FileNotFoundException`** | The `dataDir` path is incorrect or the file name has a typo. | Double‑check the directory string and ensure the file names match exactly, including spaces. |
| **Output PNG is blank** | The layout name does not exist in the source CAD file. | Use `cadImage.getLayouts()` to list available layouts, then update `rasterizationOptions.setLayouts(...)`. |
| **Large CAD files cause OutOfMemoryError** | Rasterizing high‑resolution images consumes a lot of heap space. | Increase the JVM heap (`-Xmx2g`) or lower the rasterization resolution via `rasterizationOptions.setResolution(...)`. |

## 常见问答

### Q1: Aspose.CAD 是否兼容所有 CAD 文件格式？

A1: Aspose.CAD 支持多种 CAD 格式，包括 DWG、DXF 和 DGN。完整列表请参阅 [documentation](https://reference.aspose.com/cad/java/)。

### Q2: 我可以自定义 OLE 对象的导出设置吗？

A2: 可以，Aspose.CAD 提供了丰富的选项，允许您根据具体需求定制导出设置。

### Q3: Aspose.CAD 是否提供免费试用？

A3: 是的，您可以通过 [here](https://releases.aspose.com/) 获取免费试用，以探索 Aspose.CAD 的功能。

### Q4: 我在哪里可以获得 Aspose.CAD 的社区支持？

A4: 加入 Aspose.CAD 社区的 [forum](https://forum.aspose.com/c/cad/19)，获取帮助并分享经验。

### Q5: 如何购买 Aspose.CAD 的许可证？

A5: 请访问 [purchase page](https://purchase.aspose.com/buy) 购买符合您开发需求的许可证。

## 结论

通过遵循这五个简单步骤，您即可 **保存 CAD 为 PNG** 并使用几行 Java 代码提取所有嵌入的 OLE 对象。这种方法非常适合批量转换、自动化报告或任何需要 CAD 内容光栅图像而无需手动导出的场景。欢迎尝试不同的光栅化选项，以满足质量和性能的需求。

---

**Last Updated:** 2026-01-04  
**Tested With:** Aspose.CAD for Java 24.12 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}