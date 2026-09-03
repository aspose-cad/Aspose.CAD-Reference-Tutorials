---
date: 2026-08-29
description: 了解如何使用 Aspose.CAD for Java 設定 PDF 頁面尺寸並將 CAD 轉換為 PDF，支援自動版面縮放及 TIFF 匯出。
keywords:
- set pdf page size
- convert cad to pdf
- canvas size java
- high resolution tiff
- change pdf dimensions
lastmod: 2026-08-29
linktitle: 設定 PDF 頁面尺寸 – 轉換 CAD 為 PDF
og_description: 了解在 Java 中使用 Aspose.CAD 轉換 CAD 圖紙為 PDF 時如何設定 PDF 頁面尺寸。本指南涵蓋畫布尺寸、自動版面縮放，以及匯出高解析度
  TIFF。
og_image_alt: Tutorial showing how to set pdf page size and convert CAD to PDF in
  Java
og_title: 設定 PDF 頁面尺寸 – 使用 Aspose 在 Java 中將 CAD 轉換為 PDF
schemas:
- author: Aspose
  dateModified: '2026-08-29'
  description: Learn how to set pdf page size and convert CAD to PDF using Aspose.CAD
    for Java, with automatic layout scaling and TIFF export.
  headline: Set pdf page size – convert cad to pdf (Java)
  type: TechArticle
- questions:
  - answer: No. Canvas size controls page dimensions; vector data remains resolution‑independent,
      ensuring crisp rendering at any zoom level.
    question: does the canvas size affect vector quality in the PDF?
  - answer: Yes. Adjust `rasterizationOptions.setResolution(dpiValue)` before creating
      `TiffOptions`.
    question: can I set a different DPI for the TIFF output?
  - answer: Use Aspose.PDF to load the generated PDF and call `pdf.getPages().setPageSize(PageSize.A4)`
      or a custom size.
    question: how can I change PDF dimensions for an existing PDF without re‑rendering
      the CAD?
  - answer: Keep `setAutomaticLayoutsScaling(true)` and avoid `setNoScaling(true)`;
      this retains layer visibility and layout fidelity.
    question: what is the best way to convert dxf to pdf while preserving layers?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- set pdf page size
- convert cad
- Aspose.CAD
- Java
- high resolution tiff
title: 設定 PDF 頁面尺寸 – 轉換 CAD 為 PDF（Java）
url: /zh-hant/java/advanced-cad-features/set-canvas-size-and-mode/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 設定 PDF 頁面大小 – 將 CAD 轉換為 PDF（Java）

## 介紹

如果您在將 CAD 圖紙轉換為 PDF 時需要 **設定 PDF 頁面大小**，您來對地方了。在本教學中，我們將示範如何使用 Aspose.CAD for Java 定義精確的畫布尺寸、啟用自動版面縮放，然後將結果匯出為 PDF 與 TIFF。無論是為列印準備工程圖，或是為網站相簿產生縮圖，控制頁面大小與輸出解析度都是必不可少的。

## 快速回答
- **「將 CAD 轉換為 PDF」是什麼意思？** 將 CAD 圖紙（例如 DXF、DWG）轉換為可在任何平台上檢視的 PDF 文件。  
- **我也可以匯出為 TIFF 嗎？** 是的——使用 `TiffOptions` 產生高解析度的點陣圖像。  
- **哪個選項控制 Java 中的畫布大小？** `CadRasterizationOptions.setPageWidth/Height`。  
- **什麼是自動版面縮放？** 一個旗標（`setAutomaticLayoutsScaling(true)`），在畫布大小變更時保留原始版面比例。  
- **使用 Aspose.CAD 是否需要授權？** 在正式環境使用時需要臨時或永久授權。

## 如何在 Java 中將 CAD 轉換為 PDF 時設定 PDF 頁面大小

載入 CAD 檔案，使用所需的寬度與高度設定 `CadRasterizationOptions`，啟用自動版面縮放，然後將結果儲存為 PDF。此兩步驟方法讓您在不犧牲向量品質的前提下，精確控制輸出頁面的尺寸。

## 什麼是將 CAD 轉換為 PDF？

將 CAD 轉換為 PDF 意指將基於向量的工程圖紙渲染為 PDF 頁面，保留線條、圖層與幾何形狀，同時使檔案可在任何平台上通用存取。此過程會根據指定的選項對圖紙進行點陣化，產生可在任何裝置上開啟且不需 CAD 軟體的 PDF，且保留原始設計的視覺忠實度。

## 為什麼在 Java 中設定畫布大小？

在 Java 中設定畫布大小可讓您定義輸出解析度與頁面尺寸，確保產生的 PDF 或 TIFF 符合列印或顯示需求。它同時提供對縮放行為的控制，對於大幅圖紙尤為重要。

## 先決條件

在開始教學之前，請確保您已具備以下先決條件：

- Aspose.CAD for Java：確保已在您的 Java 環境中安裝 Aspose.CAD 程式庫。您可以在此處下載 Aspose.CAD for Java 程式庫 [here](https://releases.aspose.com/cad/java/)。
- 文件目錄：建立一個文件目錄以儲存您的 CAD 檔案。教學步驟將會參考此目錄。

現在，讓我們開始一步步的指南。

## 匯入命名空間

在此步驟中，我們將匯入必要的命名空間以啟動您的 Aspose.CAD 專案。

`Image` 是用來載入 CAD 檔案的主要類別。

```java
import java.awt.Image;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## 步驟 1：匯入 Aspose.CAD 類別

`Image` 類別提供載入與儲存 CAD 圖紙的方法。

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
com.aspose.cad.Image objImage = com.aspose.cad.Image.load(srcFile);
```

在此程式碼片段中，我們設定資源目錄的路徑，並使用 Aspose.CAD 的 `Image` 類別載入 DXF 檔案。

## 步驟 2：設定 CadRasterizationOptions 屬性（設定 Java 畫布大小）

`CadRasterizationOptions` 指定點陣化設定，例如頁面大小與縮放，用於 CAD 轉點陣的過程。

```java
// Create an instance of CadRasterizationOptions and set its various properties
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

在此，我們建立 `CadRasterizationOptions` 的實例，並設定頁寬、頁高以及 **自動版面縮放** 等屬性。這就是您轉換過程中 **設定畫布模式** 的核心。

## 步驟 3：建立 PdfOptions 並設定 vectorRasterizationOptions

`PdfOptions` 定義 PDF 輸出的設定。

```java
// Create an instance of PdfOptions
PdfOptions pdfOptions = new PdfOptions();

// Set the VectorRasterizationOptions property
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

現在，我們建立 `PdfOptions` 實例，並將其 `VectorRasterizationOptions` 屬性設定為先前配置好的 `CadRasterizationOptions`。

## 步驟 4：匯出為 PDF（將 CAD 轉換為 PDF）

```java
// Export CAD to PDF
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

最後，我們使用指定的選項將 CAD 圖像儲存為 PDF 檔案，完成 **將 CAD 轉換為 PDF** 的流程。

## 步驟 5：建立 TiffOptions 並設定 vectorRasterizationOptions（將 CAD 匯出為 TIFF）

`TiffOptions` 設定 TIFF 輸出的參數，例如壓縮與解析度。

```java
// Create an instance of TiffOptions
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);

// Set the VectorRasterizationOptions property
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
```

在此步驟中，我們建立 `TiffOptions` 實例，並設定其 `VectorRasterizationOptions` 屬性。

## 步驟 6：匯出為 TIFF

```java
// Export CAD to TIFF
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

最後，我們使用指定的選項將 CAD 圖像儲存為 TIFF 檔案，示範在配置畫布大小後如何 **將 CAD 匯出為 TIFF**。

## 常見問題與解決方案

| 問題 | 原因 | 解決方法 |
|------|------|----------|
| 輸出 PDF 為空白 | `setNoScaling(true)` 會導致某些圖形無法渲染 | 移除 `setNoScaling(true)` 或將其設為 `false`。 |
| TIFF 解析度看起來太低 | 頁面寬度/高度太小 | 增加 `setPageWidth` / `setPageHeight` 的數值。 |
| 版面看起來變形 | 自動版面縮放已停用 | 確保已啟用 `setAutomaticLayoutsScaling(true)`。 |

## 為什麼要調整畫布大小與 DPI？

直接變更畫布大小會影響輸出點陣化的解析度。如果您需要 **提升 TIFF 解析度**，只要提高 `setPageWidth` / `setPageHeight` 的數值，或在建立 `TiffOptions` 前呼叫 `rasterizationOptions.setResolution(300)`。這樣即可取得適合列印或細部檢查的高品質點陣圖像。

## 常見問答

**Q1：我可以將 Aspose.CAD for Java 與其他 Java 框架一起使用嗎？**  
A：是的，Aspose.CAD 設計上能無縫整合各種 Java 框架。

**Q2：Aspose.CAD 是否提供臨時授權？**  
A：是的，您可以在此取得臨時授權頁面 [here](https://purchase.aspose.com/temporary-license/)。

**Q3：我可以在哪裡取得 Aspose.CAD 的社群支援？**  
A：請造訪 Aspose.CAD 論壇 [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) 取得社群支援與討論。

**Q4：我可以免費試用 Aspose.CAD 嗎？**  
A：當然可以！取得免費試用下載頁面 [here](https://releases.aspose.com/)。

**Q5：我要如何購買 Aspose.CAD for Java？**  
A：在此購買 Aspose.CAD for Java [here](https://purchase.aspose.com/buy)。

**Q：畫布大小會影響 PDF 中的向量品質嗎？**  
A：不會。畫布大小僅控制頁面尺寸；向量資料仍保持與解析度無關，確保在任何縮放層級下皆能清晰呈現。

**Q：我可以為 TIFF 輸出設定不同的 DPI 嗎？**  
A：可以。在建立 `TiffOptions` 前調整 `rasterizationOptions.setResolution(dpiValue)`。

**Q：如何在不重新渲染 CAD 的情況下變更現有 PDF 的尺寸？**  
A：使用 Aspose.PDF 載入產生的 PDF，然後呼叫 `pdf.getPages().setPageSize(PageSize.A4)` 或自訂尺寸。

**Q：在保留圖層的前提下，將 dxf 轉換為 PDF 的最佳方法是什麼？**  
A：保留 `setAutomaticLayoutsScaling(true)` 並避免使用 `setNoScaling(true)`；這樣可保留圖層可見性與版面忠實度。

## 結論

恭喜！您已成功 **將 CAD 轉換為 PDF** 並 **將 CAD 匯出為 TIFF**，同時 **設定 Java 畫布大小**、啟用 **自動版面縮放**，並學會如何 **配置畫布模式** 以獲得高品質輸出。本教學為您的 CAD 轉換專案奠定了堅實基礎。探索更多功能與可能性，請參閱 [Aspose.CAD 文件](https://reference.aspose.com/cad/java/)。

---

**最後更新：** 2026-08-29  
**測試環境：** Aspose.CAD for Java 24.12  
**作者：** Aspose

## 相關教學

- [設定畫布大小 – 使用 Aspose.CAD for Java 的進階 CAD 功能](/cad/java/advanced-cad-features/)
- [在 Java 中將 DWG 匯出為 PDF – 使用 Aspose.CAD 設定 PDF 頁面大小](/cad/java/cad-export-options/export-to-pdf/)
- [設定自訂頁面大小 – 使用自動版面縮放將 CAD 轉為 PDF](/cad/java/advanced-cad-features/setting-auto-layout-scaling/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}