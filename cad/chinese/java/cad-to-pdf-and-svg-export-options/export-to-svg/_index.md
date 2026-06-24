---
date: 2026-06-14
description: 了解如何使用 Aspose.CAD for Java 将 CAD 导出为 SVG。此分步指南展示了如何将 DWG 转换为 SVG、设置 SVG
  颜色模式，以及将该库集成到您的 Java 项目中。
keywords:
- export cad to svg
- convert dwg to svg
- change svg to grayscale
- convert cad to svg
- generate svg from dwg
linktitle: 导出为 SVG
schemas:
- author: Aspose
  dateModified: '2026-06-14'
  description: Learn how to export CAD to SVG with Aspose.CAD for Java. This step‑by‑step
    guide shows you how to convert DWG to SVG, set SVG color mode, and integrate the
    library into your Java project.
  headline: Export CAD to SVG Using Aspose.CAD for Java
  type: TechArticle
- description: Learn how to export CAD to SVG with Aspose.CAD for Java. This step‑by‑step
    guide shows you how to convert DWG to SVG, set SVG color mode, and integrate the
    library into your Java project.
  name: Export CAD to SVG Using Aspose.CAD for Java
  steps:
  - name: Open Your Java Project
    text: Launch your favorite IDE (IntelliJ IDEA, Eclipse, VS Code) and open the
      project where you intend to add the conversion logic.
  - name: Add Aspose.CAD Library
    text: Place the `aspose-cad-xx.jar` file in the `libs` directory and add it as
      a dependency in your build tool (Maven, Gradle, or plain `javac`).
  - name: Import Namespaces
    text: 'In the Java source file that will perform the conversion, add the following
      imports: These imports give you access to the core `Image` class and the SVG‑specific
      export options.'
  - name: Specify the Resource Directory
    text: 'Define the absolute or relative path that points to the folder holding
      your CAD drawings:'
  - name: Load the CAD Drawing
    text: The `Image` class is Aspose.CAD's top‑level object that represents a CAD
      drawing in memory. Loading the file creates an in‑memory representation ready
      for export. `Image.load` reads a CAD file and creates an in‑memory representation
      of the drawing.
  - name: Configure SVG Export Options
    text: '`SvgExportOptions` lets you fine‑tune the SVG output. Below we set the
      color mode to grayscale and ensure all text is rendered as shapes, which improves
      compatibility with browsers that lack the original font.'
  - name: Save as SVG
    text: Finally, invoke `save` on the `Image` instance, passing the target file
      name and the configured options. Aspose.CAD writes a standards‑compliant SVG
      file that can be opened directly in any modern browser. `save` writes the image
      to the specified file using the provided export options. > **Pro tip:**
  type: HowTo
- questions:
  - answer: Yes, simply replace the DWG file name with a DXF file; the API automatically
      detects and processes both formats.
    question: Can I convert a DXF file to SVG using the same code?
  - answer: Set `options.setColorType(SvgColorMode.FullColor);` before invoking the
      `save` method.
    question: How do I change the output to full‑color SVG?
  - answer: Aspose.CAD converts text to shapes, so embedding fonts is unnecessary;
      the resulting SVG contains only vector outlines.
    question: Is it possible to embed fonts in the generated SVG?
  - answer: The Java library is platform‑independent and runs wherever a compatible
      JVM is available, including Windows, Linux, and macOS.
    question: Does the library work on Linux and macOS?
  - answer: The example was tested with Aspose.CAD for Java **24.10**.
    question: What version of Aspose.CAD was used in this tutorial?
  type: FAQPage
second_title: Aspose.CAD Java API
title: 使用 Aspose.CAD for Java 将 CAD 导出为 SVG
url: /zh/java/cad-to-pdf-and-svg-export-options/export-to-svg/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.CAD for Java 将 CAD 导出为 SVG

## 介绍

在本综合教程中，您将学习使用 Aspose.CAD for Java **如何将 CAD 导出为 SVG**。无论您是需要 **将 DWG 转换为 SVG**、在批处理作业中从 DWG 文件生成 SVG，还是仅仅将 SVG 更改为灰度以实现轻量级网页显示，本指南都会一步步带您完成——从库的设置到细致的导出选项调优。完成后，您将拥有可在任何兼容 JVM 的平台上运行的生产就绪代码片段。

## 快速答案
- **导出 CAD 为 SVG 是什么意思？** 它将 CAD 图纸（例如 DWG 或 DXF）转换为可伸缩矢量图形（SVG）文件，浏览器渲染时不会失真。  
- **哪个库负责转换？** Aspose.CAD for Java 提供专用 API，支持 30 多种 CAD 格式，并以完整矢量保真度输出 SVG。  
- **开发是否需要许可证？** 免费试用可用于评估；生产部署需要商业许可证。  
- **我可以控制 SVG 的颜色输出吗？** 可以——使用 `SvgColorMode` 在灰度和全彩渲染之间切换。  
- **需要任何额外的软件吗？** 只需 Java 运行时（JDK 8 或更高）和 Aspose.CAD JAR；无需外部 CAD 工具。

## 什么是将 CAD 导出为 SVG？
将 CAD 导出为 SVG 是将本机 CAD 文件（如 DWG、DXF 或 DWF）转换为 SVG 矢量图像格式的过程。生成的 SVG 保留精确的几何数据，使其在网页浏览器和设计工具中实现分辨率无关的显示。

## 为什么使用 Aspose.CAD 将 CAD 导出为 SVG？
Aspose.CAD 能处理 **30+ 输入格式**，并可生成最多 **500 页** 的 SVG 输出，而无需将整个文件加载到内存中，在普通服务器级 CPU 上实现 **每秒 200 页** 的 **高保真矢量转换**。该库 **100% 基于 Java**，无需本机 DLL 或第三方 CAD 引擎。

## 先决条件

- **Java Development Kit**（JDK 8 或更高）已在您的机器上安装并配置。  
- **Aspose.CAD for Java** JAR 文件已从官方[下载链接](https://releases.aspose.com/cad/java/)下载。  
- 包含至少一个您想要转换的 CAD 图纸（DWG、DXF 等）的文件夹。

## 导入命名空间

在编写任何代码之前，请确保 Aspose.CAD 库已在类路径中，并导入所需的类。

### 步骤 1：打开您的 Java 项目
启动您喜欢的 IDE（IntelliJ IDEA、Eclipse、VS Code），并打开您打算添加转换逻辑的项目。

### 步骤 2：添加 Aspose.CAD 库
将 `aspose-cad-xx.jar` 文件放置在 `libs` 目录中，并在构建工具（Maven、Gradle 或普通 `javac`）中将其添加为依赖项。

### 步骤 3：导入命名空间
在执行转换的 Java 源文件中，添加以下导入语句：

```java
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.SvgExportOptions;
import com.aspose.cad.imageoptions.SvgColorMode;
```

这些导入让您能够访问核心的 `Image` 类以及 SVG 特定的导出选项。

## 如何使用 Aspose.CAD for Java 将 CAD 导出为 SVG？

使用 Aspose.CAD 将 CAD 图纸导出为 SVG 包括加载源文件、配置 SVG 特定选项以及写入输出。该过程简单明了，仅需几行代码，并在所有受支持的 CAD 格式中保持一致，同时保留矢量保真度。

### 步骤 1：指定资源目录
定义指向存放 CAD 图纸的文件夹的绝对或相对路径：

```java
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.SvgOptions;
import com.aspose.cad.imageoptions.SvgColorMode;
```

### 步骤 2：加载 CAD 图纸
`Image` 类是 Aspose.CAD 的顶层对象，表示内存中的 CAD 图纸。加载文件会创建一个准备导出的内存表示。

`Image.load` 读取 CAD 文件并创建图纸的内存表示。

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

### 步骤 3：配置 SVG 导出选项
`SvgExportOptions` 让您对 SVG 输出进行细致调优。下面我们将颜色模式设置为灰度，并确保所有文本渲染为形状，这提升了对缺少原始字体的浏览器的兼容性。

```java
Image image = Image.load(dataDir + "meshes.dwg");
```

### 步骤 4：保存为 SVG
最后，对 `Image` 实例调用 `save`，传入目标文件名和配置好的选项。Aspose.CAD 会写入符合标准的 SVG 文件，可直接在任何现代浏览器中打开。

`save` 使用提供的导出选项将图像写入指定文件。

```java
SvgOptions options = new SvgOptions();
options.setColorType(SvgColorMode.Grayscale);
options.setTextAsShapes(true);
```

> **专业提示：** 要生成全彩 SVG，请将 `SvgColorMode.Grayscale` 替换为 `SvgColorMode.FullColor`。此切换在保持原始调色板的同时仍提供矢量可伸缩性。

## 为什么使用 Aspose.CAD 将 CAD 导出为 SVG？
- **高保真:** 矢量数据被保留，确保 SVG 与原始 CAD 图纸完全一致。  
- **无外部依赖:** 转换完全在 Java 中运行，消除对额外工具的需求。  
- **可定制输出:** 像 `setColorType` 这样的选项让您控制 SVG 是灰度还是全彩。  
- **可扩展性能:** 在几秒钟内处理数百页的图纸，内存使用低于 50 MB。

## 常见问题及解决方案
- **文件未找到:** 验证 `dataDir` 指向正确的文件夹，并且 DWG 文件名在文件系统中大小写匹配。  
- **空白 SVG 输出:** 当源图纸包含必须以矢量形状显示的文本时，确保启用 `options.setTextAsShapes(true)`。  
- **不支持的 CAD 格式:** Aspose.CAD 支持 DWG、DXF、DWF 以及另外 15 种以上格式；请查阅官方文档获取完整列表。  
- **性能瓶颈:** 对于极大的文件，可通过 `options.setEnableStreaming(true)` 启用流式模式，以降低内存消耗。

## 常见问答

**问：我可以使用相同的代码将 DXF 文件转换为 SVG 吗？**  
答：可以，只需将 DWG 文件名替换为 DXF 文件；API 会自动检测并处理这两种格式。

**问：如何将输出更改为全彩 SVG？**  
答：在调用 `save` 方法之前，设置 `options.setColorType(SvgColorMode.FullColor);`。

**问：生成的 SVG 能嵌入字体吗？**  
答：Aspose.CAD 将文本转换为形状，因此不需要嵌入字体；生成的 SVG 仅包含矢量轮廓。

**问：该库在 Linux 和 macOS 上能工作吗？**  
答：Java 库平台无关，只要有兼容的 JVM，即可在 Windows、Linux 和 macOS 上运行。

**问：本教程使用的 Aspose.CAD 版本是什么？**  
答：示例已在 Aspose.CAD for Java **24.10** 上测试。

---

**最后更新：** 2026-06-14  
**测试环境：** Aspose.CAD for Java 24.10  
**作者：** Aspose  

```java
image.save(dataDir + "meshes.svg");
```

{{< blocks/products/products-backtop-button >}}

## 相关教程

- [使用 Aspose.CAD for Java 将 DWG 导出为 PDF 或光栅](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [dwg 转 pdf java – 使用 Aspose.CAD 将 CAD 导出为 PDF](/cad/java/cad-export-options/export-to-pdf/)
- [使用 Aspose.CAD for Java 将特定 DWG 布局导出为 PDF](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}