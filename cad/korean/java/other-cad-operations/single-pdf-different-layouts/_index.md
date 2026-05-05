---
date: 2026-01-22
description: Aspose.CAD for Java를 사용하여 CAD 도면에서 PDF를 생성하고, DWG를 PDF로 변환하며, PDF 페이지
  크기를 사용자 지정하는 방법을 배웁니다.
linktitle: Single PDF with Different Layouts
second_title: Aspose.CAD Java API
title: Aspose.CAD for Java를 사용하여 CAD 도면을 PDF로 만드는 방법
url: /ko/java/other-cad-operations/single-pdf-different-layouts/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for Java를 사용하여 CAD 도면에서 PDF 만들기

## Introduction

이 튜토리얼에서는 Aspose.CAD 라이브러리를 사용하여 **CAD에서 PDF를 만드는 방법**을 알아봅니다. **DWG를 PDF로 변환**해야 하든, 복잡한 CAD 파일을 내보내든, **맞춤형 PDF 페이지 크기**를 적용하든, 아래 단계가 깔끔하고 프로그래밍 방식의 솔루션을 안내합니다. 몇 줄의 Java 코드만으로 여러 레이아웃 페이지를 포함하는 단일 PDF를 생성하는 과정을 함께 살펴보세요.

## Quick Answers
- **What does Aspose.CAD do?** It lets Java developers load, manipulate, and export CAD drawings to formats like PDF.
- **Can I export multiple layouts into one PDF?** Yes, by customizing layout page sizes before saving.
- **Which CAD formats are supported?** DWG, DXF, DWF, DGN and many more.
- **Do I need a license for production?** A temporary license works for testing; a full license is required for commercial use.
- **What version of Java is required?** Java 8 or later.

## What is “create PDF from CAD”?
CAD에서 PDF를 만든다는 것은 벡터 기반 CAD 도면을 고정 레이아웃 문서(PDF)로 래스터화하여 CAD 소프트웨어 없이도 모든 장치에서 볼 수 있게 하는 것을 의미합니다. 설계 공유, 청사진 인쇄, 엔지니어링 작업 보관 등에 이상적입니다.

## Why use Aspose.CAD for Java?
- **No external dependencies** – pure Java, no native DLLs.
- **Fine‑grained control** over rasterization options such as DPI, page size, and layout selection.
- **Batch processing** – handle many drawings in a single run.
- **Accurate conversion** – preserves line weights, colors, and layers.

## Prerequisites

Before we begin, make sure you have the following:

- **Java Environment** – JDK 8 or newer installed.
- **Aspose.CAD Library** – Download and install the Aspose.CAD library for Java from the [download link](https://releases.aspose.com/cad/java/).
- **Document Directory** – A folder that contains the DWG (or other CAD) drawings you want to convert.

## Import Packages

In your Java project, import the necessary classes:

```java
import com.aspose.cad.Image;
import com.aspose.cad.SizeF;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.VectorRasterizationOptions;
```

## Step‑by‑Step Guide

### Step 1: Load CAD Drawing

First, load the source CAD file (e.g., a DWG) into a `CadImage` object. This is the entry point for any **export CAD to PDF** operation.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
CadImage cadImage = (CadImage)Image.load(dataDir + "City skyway map.dwg");
```

### Step 2: Configure Rasterization Options

Define how the CAD data should be rasterized. Here we set a base page width and height that will be used for layouts that don’t have a custom size.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1000);
rasterizationOptions.setPageHeight(1000);
```

### Step 3: Customize Layout Page Sizes

If you need a **custom PDF page size**, add entries for each layout you want to appear in the final PDF. This lets you **convert DWG to PDF** with different dimensions per layout.

```java
rasterizationOptions.getLayoutPageSizes().addItem("ANSI C Plot", new SizeF(500, 1000));
rasterizationOptions.getLayoutPageSizes().addItem("8.5 x 11 Plot", new SizeF(1000, 100));
```

### Step 4: Set PDF Options

Combine the rasterization settings with PDF‑specific options. The `VectorRasterizationOptions` property tells Aspose.CAD to use the layout sizes we just defined.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Step 5: Save as PDF

Finally, export the CAD drawing to a single PDF file that contains all the specified layouts. This step **saves CAD as PDF** in one call.

```java
cadImage.save(dataDir + "singlePDF_out.pdf", pdfOptions);
```

> **Pro tip:** Re‑use the same `PdfOptions` object if you need to export multiple drawings in a batch – it the DPI by calling `);` before saving. |
| **License not applied** | Load your temporary or full license before any Aspose.CAD calls: `License license = new License(); license.setLicense("Aspose.CAD.lic");` |

## Frequently Asked Questions

### Q1: Can I use Aspose.CAD for Java with other Java libraries?

A1: Yes, Aspose.CAD for Java is designed to seamlessly integrate with other Java libraries, providing extensive functionality.

### Q2: Is there a trial version available?

A2: Absolutely! You can access a free trial version [here](https://releases.aspose.com/).

### Q3: Where can I find additional support?

A3: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for community support and discussions.

### Q4: How do I obtain a temporary license?

A4: You can obtain a temporary license [here](https://purchase.aspose.com/temporary-license/).

### Q5: Where can I purchase the full version?

A5: Purchase the full version of Aspose.CAD for Java [here](https://purchase.aspose.com/buy).

**Last Updated:** 2026-01-22  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}