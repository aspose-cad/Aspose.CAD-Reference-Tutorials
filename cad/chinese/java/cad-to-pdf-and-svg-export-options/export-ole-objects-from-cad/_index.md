---
date: 2026-03-02
description: 释放 Aspose.CAD for Java 的潜能。轻松导出 OLE 对象并 **将 CAD 保存为 PNG**。立即下载，实现无缝的
  CAD 数据管理。
linktitle: Export OLE Objects from CAD
second_title: Aspose.CAD Java API
title: 将 CAD 保存为 PNG – 使用 Aspose.CAD for Java 导出 OLE 对象
url: /zh/java/cad-to-pdf-and-svg-export-options/export-ole-objects-from-cad/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 将 CAD 保存为 PNG – 使用 Aspose.CAD for Java 导出 OLE 对象

## 介绍

在计算机辅助设计（CAD）这个充满活力的领域中，高效管理和提取 OLE（对象链接与嵌入）对象——以及能够 **save CAD as PNG**——对于报告、网页预览或归档等下游工作流至关重要。Aspose.CAD for Java 提供了一个强大的、代码优先的解决方案，让您只需几行代码即可导出 OLE 对象并将 CAD 图纸转换为高质量的 PNG 图像。

## 快速答案
- **What does Aspose.CAD do?** 它可以读取、操作并转换 CAD 文件（DWG、DXF、DGN 等），无需本地 CAD 软件。  
- **Can I save CAD as PNG?** 可以——使用 `PngOptions` 配合 `CadRasterizationOptions` 对任意布局进行光栅化。  
- **How to export OLE objects?** 使用 `Image.load` 加载 CAD 文件，然后将每个包含 OLE 的布局保存为 PNG。  
- **Do I need a license?** 提供免费试用版；商业许可证可去除评估限制。  
- **What Java version is required?** 完全支持 Java 8 及更高版本。

## 什么是 **save CAD as PNG**？
将 CAD 保存为 PNG 意味着将基于矢量的 CAD 图纸光栅化为基于像素的 PNG 图像。当您需要一种轻量、通用的格式用于网页、移动应用或文档时，这种转换非常有用。

## 为什么使用 Aspose.CAD for Java 来 **convert CAD to PNG**？
- **无需安装 CAD** – 该库完全在 Java 环境中运行。  
- **保持布局保真度** – 您可以选择特定布局、控制 DPI，并保留线条质量。  
- **批量处理** – 通过简单的循环即可遍历多个文件。  
- **导出 OLE 对象** – 嵌入在 DWG/DXF 文件中的 OLE 内容会自动渲染到 PNG 输出中。

## 前提条件

在开始教程之前，请确保已具备以下前提条件：

- **Java 环境** – 确保您的机器上已搭建好 Java 开发环境。  
- **Aspose.CAD for Java** – 下载并安装 Aspose.CAD for Java 库。您可以在[下载链接](https://releases.aspose.com/cad/java/)找到该库。  
- **CAD 文件** – 准备好包含 OLE 对象的 CAD 文件，以便导出。

## 导入命名空间

首先，将必要的命名空间导入到您的 Java 项目中。这些命名空间提供了使用 Aspose.CAD 处理 CAD 文件所需的核心类和功能。

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

现在，让我们将从 CAD 导出 OLE 对象的过程拆分为多个步骤：

## 如何 **save CAD as PNG** 并导出 OLE 对象

### 步骤 1：设置文档目录

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

请将 `"Your Document Directory"` 替换为存放 CAD 文件的目录路径。

### 步骤 2：定义 CAD 文件名

```java
String[] files = new String[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

在 `files` 数组中指定您要处理的 CAD 文件名称。

### 步骤 3：设置 PNG 导出选项

```java
PngOptions pngOptions = new PngOptions();
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.setVectorRasterizationOptions(rasterizationOptions);
rasterizationOptions.setLayouts(new String[] { "Layout1" });
```

配置 PNG 导出选项，包括矢量光栅化和布局设置。这些选项使您能够 **convert CAD to PNG** 并获得所需的质量。

### 步骤 4：遍历 CAD 文件

```java
for(String file : files)
{
    CadImage cadImage = (CadImage)Image.load(dataDir + file);
    cadImage.save(dataDir + file + "_out.png", pngOptions);
}
```

遍历每个指定的 CAD 文件，使用 Aspose.CAD 加载并将 OLE 对象保存为 PNG 图像。此循环演示了如何批量 **convert DWG to PNG**。

## 常见问题及解决方案

| 问题 | 原因 | 解决方案 |
|-------|-------|----------|
| **Blank PNG output** | 布局名称不匹配 | 确认源 DWG 中存在布局名称（`"Layout1"`）。 |
| **Missing OLE graphics** | OLE 对象存放在其他布局中 | 在 `rasterizationOptions.setLayouts(...)` 中包含所有相关布局。 |
| **Out‑of‑memory error on large files** | DPI 设置过高 | 通过 `rasterizationOptions.setResolution(...)` 降低 DPI，或一次处理一个文件。 |

## 常见问题

**Q: Aspose.CAD 是否兼容所有 CAD 文件格式？**  
A: Aspose.CAD 支持多种 CAD 格式，包括 DWG、DXF 和 DGN。完整列表请参阅[文档](https://reference.aspose.com/cad/java/)。

**Q: 我可以自定义 OLE 对象的导出设置吗？**  
A: 可以，Aspose.CAD 提供了丰富的选项，允许您根据具体需求定制导出设置。

**Q: Aspose.CAD 是否提供免费试用？**  
A: 是的，您可以通过[此处](https://releases.aspose.com/)获取免费试用版，体验其功能。

**Q: 我在哪里可以获取 Aspose.CAD 的社区支持？**  
A: 请加入 Aspose.CAD 社区的[论坛](https://forum.aspose.com/c/cad/19)，获取帮助并分享经验。

**Q: 如何购买 Aspose.CAD 的许可证？**  
A: 请访问[购买页面](https://purchase.aspose.com/buy)获取适合您开发需求的许可证。

## 结论

通过这些简洁而强大的步骤，您可以使用 Aspose.CAD for Java 在导出 CAD 文件中的 OLE 对象的同时，轻松 **save CAD as PNG**。这款多功能工具帮助开发者高效管理 CAD 数据，为 CAD 应用开发和下游基于图像的工作流打开了新可能。

---

**Last Updated:** 2026-03-02  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}