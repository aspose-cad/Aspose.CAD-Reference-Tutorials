---
date: 2026-01-10
description: 学习如何使用 Aspose.CAD for Java 将 DGN 导出为 DWG 并将 MicroStation DGN 转换为 AutoCAD
  DWG。一步一步的指南。
linktitle: Export DGN as Part of DWG
second_title: Aspose.CAD Java API
title: 使用 Aspose.CAD for Java 将 DGN 导出为 DWG
url: /zh/java/dgn-export-options/export-dgn-as-part-of-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.CAD for Java 将 DGN 导出为 DWG

## 介绍

在本教程中，您将学习如何 **export dgn to dwg**，并使用 Aspose.CAD for Java 将 MicroStation DGN 设计嵌入到 AutoCAD DWG 文件中。无论是迁移旧版 MicroStation 图纸，还是需要将 DGN 底图与 DWG 布局组合，本指南都会一步步带您完成——从环境搭建到生成最终 DWG 的 PDF 预览。

## 快速回答
- **“export dgn to dwg” 能实现什么？** 它将 DGN 底图嵌入 DWG，实现 AutoCAD 中的无缝查看。
- **可以导出哪种格式进行快速预览？** 您可以使用 `PdfOptions` **export cad file to pdf**。
- **运行代码是否需要许可证？** 生产环境需要临时或付费的 Aspose.CAD 许可证。
- **支持哪个 Java 版本？** Java 8 及以上均可与最新的 Aspose.CAD for Java 版本配合使用。
- **是否提供免费试用？** 有——可从 Aspose 官网下载试用版。

## 什么是 “export dgn to dwg”？
将 DGN 导出为 DWG 意味着将 MicroStation DGN 设计转换或嵌入为 AutoCAD DWG 图纸中的底图。这样 CAD 专业人员即可在不重新创建几何体的情况下，直接利用已有的 DGN 资源。

## 为什么要将 MicroStation DGN 转换为 AutoCAD DWG？
- **协作：** 使用 AutoCAD 的团队可以直接查看和编辑 DGN 内容。
- **标准化：** DWG 是许多下游工作流（如 PDF 生成、3D 渲染）的事实标准格式。
- **保留性：** 保持原始 DGN 引用完整，降低数据丢失风险。

## 前置条件

在开始教程之前，请确保已具备以下前置条件：
1. **Aspose.CAD 库：** 下载并安装 Aspose.CAD for Java 库。您可以在[此处](https://releases.aspose.com/cad/java/)找到该库。
2. **Java 开发工具包 (JDK)：** 确保系统已安装 Java。
3. **集成开发环境 (IDE)：** 选择 Eclipse、IntelliJ 等 Java IDE，以获得更流畅的开发体验。

## 导入包

在 Java 项目中导入必要的 Aspose.CAD 包，以实现 CAD 文件的操作。示例代码如下：

```java
import com.aspose.cad;
import com.aspose.cad.imageoptions;
import com.aspose.cad.fileformats.cad.cadconsts;
import com.aspose.cad.fileformats.cad;
import com.aspose.cad.fileformats.cad.cadobjects;
```

## 步骤 1：设置文件路径

为 DWG 文件定义输入和输出路径。相应地更新 `dataDir`、`fileName` 和 `outPath` 变量。

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
String outPath = dataDir + "BlockRefDgn.dwg.pdf";
```

## 步骤 2：创建 PdfOptions 实例

创建 `PdfOptions` 类的实例，因为我们 **exporting the CAD file to PDF** 以便快速验证。

```java
PdfOptions exportOptions = new PdfOptions();
```

## 步骤 3：加载 DWG 文件

将已有的 DWG 文件作为图像加载，并转换为 `CadImage` 类型。

```java
CadImage cadImage = (CadImage) Image.load(fileName);
```

## 步骤 4：遍历实体

遍历 DWG 文件中的每个实体，检查它是否为图像定义。如果是，则获取该对象的外部引用。

```java
for (CadBaseEntity baseEntity : cadImage.getEntities()) {
    if (baseEntity.getTypeName() == CadEntityTypeName.DGNUNDERLAY) {
        CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
        System.out.println(dgnFile.getUnderlayPath());
    }
}
```

## 步骤 5：定义光栅化选项

为 `CadRasterizationOptions` 对象定义设置，包括页面宽度、高度、布局以及背景颜色。

```java
CadRasterizationOptions vectorRasterizationOptions = new CadRasterizationOptions();
vectorRasterizationOptions.setPageWidth(1600);
vectorRasterizationOptions.setPageHeight(1600);
vectorRasterizationOptions.setLayouts(new String[] { "Model" });
vectorRasterizationOptions.setAutomaticLayoutsScaling(false);
vectorRasterizationOptions.setNoScaling(true);
vectorRasterizationOptions.setBackgroundColor(Color.getBlack());
vectorRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
```

## 步骤 6：设置矢量光栅化选项

为导出设置矢量光栅化选项。

```java
exportOptions.setVectorRasterizationOptions(vectorRasterizationOptions);
```

## 步骤 7：将 DWG 导出为 PDF

最后，调用 `save` 方法将 DWG 导出为 PDF。

```java
cadImage.save(outPath, exportOptions);
```

## 常见问题及解决方案

| 问题 | 原因 | 解决方案 |
|------|------|----------|
| **未出现 DGN 底图** | DWG 中不包含 `DGNUNDERLAY` 实体。 | 确认源 DWG 包含 DGN 引用。 |
| **PDF 空白** | 光栅化选项设置了零尺寸或布局错误。 | 确保 `setPageWidth`/`setPageHeight` 为正值，且 `setLayouts` 与 DWG 布局名称匹配。 |
| **许可证异常** | 未使用有效的 Aspose.CAD 许可证运行。 | 在调用任何 API 方法前应用临时或购买的许可证。 |

## 常见问答

### Q1: 在哪里可以找到 Aspose.CAD for Java 的文档？

A1: 文档可在[此处](https://reference.aspose.com/cad/java/)查看。

### Q2: 如何下载 Aspose.CAD for Java 库？

A2: 您可以从[此链接](https://releases.aspose.com/cad/java/)下载该库。

### Q3: 是否提供 Aspose.CAD for Java 的免费试用？

A3: 是的，免费试用可在[此处](https://releases.aspose.com/)获取。

### Q4: 在哪里可以获取 Aspose.CAD for Java 的临时许可证？

A4: 请在[此处](https://purchase.aspose.com/temporary-license/)获取临时许可证。

### Q5: 需要帮助或有其他问题？

A5: 访问 Aspose.CAD 社区支持论坛[此处](https://forum.aspose.com/c/cad/19)。

### Q6: 能否将生成的 PDF 再转换回 DWG？

A6: PDF 仅为光栅预览；若需逆向转换为 DWG，需要使用专门的逆向工程工具。

### Q7: 该方法是否适用于其他 CAD 格式，如 DWF 或 DXF？

A7: 是的，Aspose.CAD 支持多种格式，只需相应调整文件扩展名和光栅化设置即可。

---

**最后更新：** 2026-01-10  
**测试环境：** Aspose.CAD for Java 24.11  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}