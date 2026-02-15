---
date: 2026-02-15
description: 學習如何使用 Aspose.CAD for Java 設定 PDF 頁面大小並將 CAD 轉換為 PDF，具備自動版面縮放與 TIFF 匯出功能。
linktitle: Set PDF Page Size – Convert CAD to PDF
second_title: Aspose.CAD Java API
title: 設定 PDF 頁面大小 – 將 CAD 轉換為 PDF（Java）
url: /zh-hant/java/advanced-cad-features/set-canvas-size-and-mode/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 設定畫布尺寸與模式

## 簡介

如果您需要在將 CAD 圖紙轉換為 PDF 時 **設定 PDF 頁面尺寸**，您來對地方了。在本教學中，我們將示範如何使用 Aspose.CAD for Java 來定義精確的畫布尺寸、啟用自動版面縮放，然後將結果匯出為 PDF 與 TIFF。無論您是為列印準備工程圖紙，或是為網站畫廊產生縮圖，控制頁面尺寸與輸出解析度都是必不可少的。

## 快速解答
- **什麼是「convert CAD to PDF」？** 將 CAD 圖紙（例如 DXF、DWG）轉換為可在任何平台上檢視的 PDF 文件。  
- **我也可以匯出為 TIFF 嗎？** 可以——使用 `TiffOptions` 產生高解析度的點陣圖。  
- **哪個選項在 Java 中控制畫布尺寸？** `CadRasterizationOptions.setPageWidth/Height`。  
- **什麼是自動版面縮放？** 一個旗標 (`setAutomaticLayoutsScaling(true)`) 用於在畫布尺寸變更時保留原始版面的比例。  
- **使用 Aspose.CAD 是否需要授權？** 生產環境需要臨時或永久授權。

## 在將 CAD 轉換為 PDF 時如何設定 PDF 頁面尺寸（Java）

設定 PDF 頁面尺寸（或畫布尺寸）讓您能決定文件的最終尺寸，這在必須 **變更 PDF 尺寸** 以符合列印標準或使用者介面需求時特別有用。以下我們將逐步說明每個步驟，解釋每行程式碼背後的 *原因*。

## 什麼是 **convert CAD to PDF**？

將 CAD 轉換為 PDF 意指將向量式的工程圖紙渲染成 PDF 頁面，保留線條、圖層與幾何形狀，同時使檔案能在任何平台上通用。

## 為什麼在 **java** 中設定畫布尺寸？

在 Java 中設定畫布尺寸可讓您定義輸出解析度與頁面尺寸，確保產生的 PDF 或 TIFF 符合您的列印或顯示需求。它同時讓您掌控縮放行為，這對大型圖紙尤為重要。

## 前置條件

在深入教學之前，請確保已具備以下前置條件：

- Aspose.CAD for Java：確保已在您的 Java 環境中安裝 Aspose.CAD 程式庫。您可在[此處](https://releases.aspose.com/cad/java/)下載。
- 文件目錄：建立一個目錄以存放您的 CAD 檔案。教學步驟中會參考此目錄。

現在，讓我們開始逐步指南。

## 匯入命名空間

在此步驟中，我們將匯入必要的命名空間，以啟動您的 Aspose.CAD 專案。

```java
import java.awt.Image;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## 步驟 1：匯入 Aspose.CAD 類別

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
com.aspose.cad.Image objImage = com.aspose.cad.Image.load(srcFile);
```

在此程式碼片段中，我們設定資源目錄的路徑，並使用 Aspose.CAD 的 `Image` 類別載入 DXF 檔案。

## 步驟 2：設定 **CadRasterizationOptions** 屬性（設定畫布尺寸 java）

```java
// Create an instance of CadRasterizationOptions and set its various properties
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

在此，我們建立 `CadRasterizationOptions` 的實例，並設定頁寬、頁高以及 **自動版面縮放** 等屬性。這是您轉換過程中 **設定畫布模式** 的核心。

## 步驟 3：建立 PdfOptions 並設定 VectorRasterizationOptions

```java
// Create an instance of PdfOptions
PdfOptions pdfOptions = new PdfOptions();

// Set the VectorRasterizationOptions property
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

現在，我們建立 `PdfOptions` 實例，並將其 `VectorRasterizationOptions` 屬性設定為先前配置好的 `CadRasterizationOptions`。

## 步驟 4：匯出為 PDF（convert cad to pdf）

```java
// Export CAD to PDF
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

最後，我們使用指定的選項將 CAD 圖像儲存為 PDF 檔案，完成 **convert CAD to PDF** 流程。

## 步驟 5：建立 TiffOptions 並設定 VectorRasterizationOptions（export cad to tiff）

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

最後，我們使用指定的選項將 CAD 圖像儲存為 TIFF 檔案，示範在設定畫布尺寸後如何 **export CAD to TIFF**。

## 常見問題與解決方案

| 問題 | 原因 | 解決方法 |
|-------|-------|-----|
| 輸出 PDF 為空白 | `setNoScaling(true)` 會對某些圖紙停用渲染 | 移除 `setNoScaling(true)` 或將其設為 `false`。 |
| TIFF 解析度過低 | 頁寬/頁高設定過小 | 增加 `setPageWidth` / `setPageHeight` 的數值。 |
| 版面變形 | 未啟用自動版面縮放 | 確保已啟用 `setAutomaticLayoutsScaling(true)`。 |

## 為什麼要調整畫布尺寸與 DPI？

變更畫布尺寸會直接影響輸出之點陣化解析度。如果您需要 **提高 TIFF 解析度**，只要在建立 `TiffOptions` 前提升 `setPageWidth` / `setPageHeight` 的數值，或呼叫 `rasterizationOptions.setResolution(300)` 即可。這樣即可取得適合列印或細部檢查的高品質點陣圖。

## 常見問答

### Q1：我可以在其他 Java 框架中使用 Aspose.CAD for Java 嗎？

A1：可以，Aspose.CAD 設計上能無縫整合各種 Java 框架。

### Q2：Aspose.CAD 是否提供臨時授權？

A2：可以，您可在[此處](https://purchase.aspose.com/temporary-license/)取得臨時授權。

### Q3：我可以在哪裡取得 Aspose.CAD 的社群支援？

A3：請前往 [Aspose.CAD 論壇](https://forum.aspose.com/c/cad/19) 獲取社群支援與討論。

### Q4：我可以免費試用 Aspose.CAD 嗎？

A4：當然可以！在[此處](https://releases.aspose.com/)取得免費試用。

### Q5：如何購買 Aspose.CAD for Java？

A5：請在[此處](https://purchase.aspose.com/buy)購買本產品。

**Q: 畫布尺寸會影響 PDF 中向量的品質嗎？**  
A: 不會。畫布尺寸僅控制頁面尺寸；向量資料保持解析度獨立，確保在任何縮放層級下皆能清晰呈現。

**Q: 我可以為 TIFF 輸出設定不同的 DPI 嗎？**  
A: 可以。在建立 `TiffOptions` 前調整 `rasterizationOptions.setResolution(dpiValue)`。

**Q: 如何在不重新渲染 CAD 的情況下 **變更 PDF 尺寸**？**  
A: 使用 Aspose.PDF 載入已產生的 PDF，然後呼叫 `pdf.getPages().setPageSize(PageSize.A4)` 或自訂尺寸。

**Q: 在保留圖層的前提下，將 **dxf 轉換為 pdf** 的最佳方法是什麼？**  
A: 保持 `setAutomaticLayoutsScaling(true)` 並避免使用 `setNoScaling(true)`；這樣可保留圖層可見性與版面忠實度。

## 結論

恭喜！您已成功 **convert CAD to PDF** 並 **export CAD to TIFF**，同時 **set canvas size java**，啟用 **automatic layout scaling**，並學會如何 **configure canvas mode** 以產生高品質的輸出。本教學為您的 CAD 轉換專案奠定了堅實的基礎。請在 [Aspose.CAD 文件](https://reference.aspose.com/cad/java/) 中探索更多功能與可能性。

---

**最後更新：** 2026-02-15  
**測試環境：** Aspose.CAD for Java 24.12  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}