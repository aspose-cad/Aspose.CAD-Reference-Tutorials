---
date: 2025-12-10
description: 學習如何使用 Aspose.CAD for Java 及自動佈局縮放功能，將 CAD 轉換為 PDF。本分步指南將教您如何高效且可靠地將
  CAD 匯出為 PDF。
linktitle: Setting Auto Layout Scaling
second_title: Aspose.CAD Java API
title: 從 CAD 產生 PDF – 使用 Aspose.CAD Java 進行自動版面縮放
url: /zh-hant/java/advanced-cad-features/setting-auto-layout-scaling/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 從 CAD 建立 PDF – 使用 Aspose.CAD Java 的自動版面縮放

## Introduction

如果您需要 **create PDF from CAD** 檔案快速且完美縮放，Aspose.CAD for Java 能滿足您的需求。自動版面縮放會自動調整版面尺寸，使最終的 PDF 完全符合預期，無論原始 CAD 頁面大小為何。在本教學中，我們將逐步說明完整流程——從載入 DXF 檔案到匯出 PDF——同時強調 **export CAD to PDF** 功能。

## Quick Answers
- **What does Auto Layout Scaling do?** 它會在光柵化時自動調整 CAD 版面大小，以符合目標頁面尺寸。
- **Which formats can I convert?** 任何 Aspose.CAD 支援的格式（例如 DXF、DWG、DWF）皆可轉換為 PDF。
- **Do I need a license for production?** 是的，非評估用途必須購買商業授權。
- **How long does the conversion take?** 通常在現代硬體上，標準檔案的轉換時間不到一秒。
- **Can I change the page size?** 可以，您可以透過 `CadRasterizationOptions` 設定自訂頁面尺寸。

## What is “create PDF from CAD”?

從 CAD 建立 PDF 意指將向量式工程圖（DXF、DWG 等）光柵化為 PDF 文件。PDF 會保留原始圖紙的視覺忠實度，同時可在任何平台上廣泛檢視。

## Why use Auto Layout Scaling?
- **Consistent output:** 保證所有版面在 PDF 頁面上完整填滿，無需手動計算尺寸。
- **Time‑saving:** 免除為每張圖紙手動調整縮放比例的需求。
- **High quality:** 轉換過程中維持線寬與幾何精度。

## Prerequisites

1. **Aspose.CAD for Java Library** – 從 [download page](https://releases.aspose.com/cad/java/) 下載最新版本。  
2. **Resource Directory** – 在本機建立資料夾以存放 CAD 檔案；將程式碼中的 `"Your Document Directory"` 替換為該路徑。  
3. **Sample CAD File** – 本教學使用 `conic_pyramid.dxf`，此檔案已包含於 Aspose 範例資料集中。

## Import Namespaces

首先匯入所需的類別，以取得圖像載入、光柵化與 PDF 匯出功能。

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Step 1: Load the CAD File

載入來源檔案是 **how to export CAD** 為 PDF 文件的第一步。

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

## Step 2: Create Rasterization Options

定義目標頁面尺寸。若您想使用自訂版面，也可以在此區塊手動 **set CAD page size**。

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
```

## Step 3: Set Auto Layout Scaling

啟用自動縮放功能。這是 **how to set scaling** 為 CAD‑to‑PDF 轉換的核心。

```java
rasterizationOptions.setAutomaticLayoutsScaling(true);
```

## Step 4: Create PDF Options

將光柵化設定連結至 PDF 匯出選項。

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Step 5: Export to PDF

最後，將渲染後的圖像儲存為 PDF 檔案。此步驟完成 **convert DXF to PDF** 工作流程。

```java
image.save(dataDir + "result_out_.pdf", pdfOptions);
```

重複上述步驟，即可處理任何其他需要轉換的 CAD 檔案。

## Common Issues & Troubleshooting

| Symptom | Likely Cause | Fix |
|---------|--------------|-----|
| Blank PDF output | Rasterization options not set or file path incorrect | Verify `srcFile` path and ensure `setPageWidth/Height` are non‑zero |
| Distorted scaling | `setAutomaticLayoutsScaling` left as `false` | Enable automatic scaling or manually calculate scaling factor |
| Missing layers | Source DXF contains unsupported entities | Check the Aspose.CAD release notes for supported entity types |

## FAQ's

### Q1: Is Aspose.CAD for Java compatible with all CAD file formats?

A1: Aspose.CAD for Java supports various CAD formats, including DWG, DXF, and DWF.

### Q2: Can I customize the scaling options further?

A2: Yes, the `CadRasterizationOptions` class provides various properties for fine‑tuning scaling and other settings.

### Q3: Where can I find additional documentation for Aspose.CAD for Java?

A3: Refer to the [documentation](https://reference.aspose.com/cad/java/) for in‑depth information and examples.

### Q4: Is there a free trial available for Aspose.CAD for Java?

A4: Yes, you can explore a [free trial](https://releases.aspose.com/) to experience the capabilities of Aspose.CAD for Java.

### Q5: How can I seek assistance or engage in discussions about Aspose.CAD for Java?

A5: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) to connect with the community and seek support.

**Additional Common Questions**

**Q: How do I convert a DWG file to PDF instead of DXF?**  
A: The same code works; just change the file extension in `srcFile` to `.dwg`.

**Q: Can I set a custom DPI for higher‑resolution PDFs?**  
A: Yes, use `rasterizationOptions.setResolution(300);` (or any DPI you need).

**Q: Is it possible to embed fonts in the generated PDF?**  
A: Aspose.CAD rasterizes the drawing, so fonts are rendered as vectors; no separate font embedding is required.

## Conclusion

透過本指南，您現在已掌握如何使用 Aspose.CAD for Java 及自動版面縮放 **create PDF from CAD** 檔案。此流程簡化了 **export CAD to PDF** 工作流程，確保縮放一致，並為您節省寶貴的開發時間。歡迎自行嘗試不同的頁面尺寸、解析度與 CAD 格式，以符合專案需求。

---

**Last Updated:** 2025-12-10  
**Tested With:** Aspose.CAD for Java 24.12 (latest)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}