---
title: 使用 Aspose.CAD 保存 CAD 时超时
linktitle: 保存超时
second_title: Aspose.CAD Java API
description: 了解如何使用 Aspose.CAD 提高 Java 应用程序的性能。为 CAD 工程图的保存设置超时。请遵循我们的分步指南。
type: docs
weight: 15
url: /zh/java/other-cad-operations/put-timeout-on-save/
---
## 介绍

欢迎阅读有关使用 Aspose.CAD for Java 设置保存超时的教程。在本指南中，我们将引导您完成设置保存 CAD 绘图超时的过程，以提高应用程序的性能。 Aspose.CAD for Java 是一个功能强大的库，可让您在 Java 应用程序中无缝地使用 CAD 文件。

## 先决条件

在深入学习本教程之前，请确保您具备以下先决条件：
-  Aspose.CAD for Java 库：确保您已将 Aspose.CAD for Java 库集成到您的项目中。您可以从以下位置下载该库[网站](https://releases.aspose.com/cad/java/).
- 开发环境：使用所有必要的工具和依赖项设置 Java 开发环境。

## 导入包

首先，将所需的包导入到您的 Java 项目中。在 Java 文件的开头添加以下行：

```java
import com.aspose.cad.Image;
import com.aspose.cad.InterruptionTokenSource;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.concurrent.TimeUnit;
```

现在，让我们将示例代码分解为分步说明：

## 第 1 步：设置源目录和输出目录

```java
final String SourceDir = Utils.getDataDir_DWGDrawings();
final String OutputDir = Utils.getDataDir_Output();
```

确保您的 CAD 工程图具有正确的源目录和输出目录。

## 第2步：创建中断令牌源

```java
final InterruptionTokenSource source = new com.aspose.cad.InterruptionTokenSource();
```

初始化中断令牌源以管理保存操作期间的中断。

## 第 3 步：加载 CAD 图纸

```java
final CadImage cadImageBig = (CadImage)Image.load(SourceDir + "Drawing11.dwg");
```

将 CAD 图纸加载到`CadImage`目的。

## 步骤 4：配置光栅化选项

```java
CadRasterizationOptions rasterizationOptionsBig = new CadRasterizationOptions();
rasterizationOptionsBig.setPageWidth(cadImageBig.getSize().getWidth() / 2);
rasterizationOptionsBig.setPageHeight(cadImageBig.getSize().getHeight() / 2);
```

配置 CAD 绘图的光栅化选项。

## 步骤 5：配置 PDF 选项

```java
final PdfOptions CADfBig = new PdfOptions();
CADfBig.setVectorRasterizationOptions(rasterizationOptionsBig);
CADfBig.setInterruptionToken(source.getToken());
```

使用矢量光栅化选项和中断标记设置 PDF 选项。

## 第 6 步：超时保存绘图

```java
cadImageBig.save(OutputDir + "PutTimeoutOnSave_out.pdf", CADfBig);
```

使用指定的超时将 CAD 绘图保存到 PDF 文件。

## 第 7 步：处理中断

```java
java.lang.Thread thread = new java.lang.Thread(new Runnable() {
    @Override
    public void run() {
        try {
            cadImageBig.save(OutputDir + "PutTimeoutOnSave_out.pdf", CADfBig);
        } catch (Throwable th) {
            System.out.println("interrupted !!!");
        }
    }
});
thread.start();
TimeUnit.SECONDS.sleep(3);
source.interrupt();
thread.join();
```

创建一个线程来处理保存操作并在指定的超时后中断它。

## 结论

恭喜！您已经成功学习了如何使用 Aspose.CAD for Java 设置保存超时。此功能可以大大提高您的 CAD 相关应用程序的效率。

## 常见问题解答

### Q1: 如何下载 Aspose.CAD for Java？

 A1：您可以从[发布页面](https://releases.aspose.com/cad/java/).

### Q2：在哪里可以找到 Aspose.CAD for Java 的文档？

 A2：请参阅[文档](https://reference.aspose.com/cad/java/)以获得全面的信息。

### Q3：有免费试用吗？

A3：是的，您可以从以下位置获得免费试用[这个链接](https://releases.aspose.com/).

### Q4：如何获得临时驾照？

 A4：参观[这里](https://purchase.aspose.com/temporary-license/)了解临时许可证详细信息。

### Q5: 需要帮助或有疑问吗？

 A5：前往[Aspose.CAD论坛](https://forum.aspose.com/c/cad/19)以获得社区支持。