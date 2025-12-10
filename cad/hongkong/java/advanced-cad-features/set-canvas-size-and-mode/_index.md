---
date: 2025-12-10
description: 了解如何使用 Aspose.CAD for Java 將 CAD 轉換為 PDF，同時設定畫布尺寸、自動版面縮放，並匯出為 TIFF。
linktitle: Convert CAD to PDF – Set Canvas Size & Mode
second_title: Aspose.CAD Java API
title: 將 CAD 轉換為 PDF – 設定畫布大小與模式（Java）
url: /zh-hant/java/advanced-cad-features/set-canvas-size-and-mode/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 設定畫布大小與模式

## 介紹

您是否正在尋找 **convert CAD to PDF** 的方法，同時希望完整掌控畫布大小與渲染模式？本完整指南將一步步帶您在 Java 中設定畫布大小、啟用自動版面縮放，並使用 Aspose.CAD 將結果匯出為 PDF 與 TIFF 格式。無論是優化生產流程還是試驗原型，您都能在此找到清晰、可執行的說明。

## 快速解答
- **「convert CAD to PDF」是什麼意思？** 將 CAD 圖紙（例如 DXF、DWG）轉換成可在任何平台上檢視的 PDF 文件。  
- **我也可以匯出為 TIFF 嗎？** 可以——使用 `TiffOptions` 產生高解析度的點陣圖。  
- **哪個選項在 Java 中控制畫布大小？** `CadRasterizationOptions.setPageWidth/Height`。  
- **什麼是自動版面縮放？** 透過 `setAutomaticLayoutsScaling(true)` 的旗標，在畫布大小變更時保留原始版面比例。  
- **使用 Aspose.CAD 是否需要授權？** 生產環境必須使用臨時或永久授權。

## 什麼是 **convert CAD to PDF**？

將 CAD 轉換為 PDF 意指將向量式工程圖以 PDF 頁面的形式呈現，保留線條、圖層與幾何資訊，同時使檔案具備通用可存取性。

## 為什麼要在 **java** 中設定畫布大小？

在 Java 中設定畫布大小可讓您自訂輸出解析度與頁面尺寸，確保產生的 PDF 或 TIFF 符合列印或顯示需求。此設定亦能控制縮放行為，對於大幅圖紙尤為重要。

## 前置條件

在開始教學之前，請先確保具備以下條件：

- Aspose.CAD for Java：確保已在您的 Java 環境中安裝 Aspose.CAD 程式庫。您可以在此下載 [here](https://releases.aspose.com/cad/java/)。
- 文件目錄：建立一個用於存放 CAD 檔案的目錄，教學步驟將會引用此目錄。

現在，讓我們開始逐步教學。

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

## 步驟 2：設定 **CadRasterizationOptions** 屬性（設定畫布大小 java）

```java
// Create an instance of CadRasterizationOptions and set its various properties
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

在此我們建立 `CadRasterizationOptions` 實例，並設定頁寬、頁高以及 **automatic layout scaling** 等屬性。這是您轉換過程中 **configure canvas mode** 的核心設定。

## 步驟 3：建立 PdfOptions 並設定 VectorRasterizationOptions

```java
// Create an instance of PdfOptions
PdfOptions pdfOptions = new PdfOptions();

// Set the VectorRasterizationOptions property
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

現在，我們建立 `PdfOptions` 實例，並將其 `VectorRasterizationOptions` 屬性指向先前配置好的 `CadRasterizationOptions`。

## 步驟 4：匯出為 PDF（convert cad to pdf）

```java
// Export CAD to PDF
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

最後，我們使用上述選項將 CAD 圖像儲存為 PDF 檔案，完成 **convert CAD to PDF** 的整個流程。

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

最後，我們使用指定的選項將 CAD 圖像儲存為 TIFF 檔案，示範在設定畫布大小後如何 **export CAD to TIFF**。

## 常見問題與解決方案

| 問題 | 原因 | 解決方案 |
|------|------|----------|
| 輸出 PDF 為空白 | `setNoScaling(true)` 會對某些圖紙停用渲染 | 移除 `setNoScaling(true)` 或改為 `false`。 |
| TIFF 解析度偏低 | 頁寬/頁高設定過小 | 增加 `setPageWidth` / `setPageHeight` 的數值。 |
| 版面變形 | 未啟用自動版面縮放 | 確認已啟用 `setAutomaticLayoutsScaling(true)`。 |

## 結論

恭喜！您已成功 **convert CAD to PDF** 並 **export CAD to TIFF**，同時 **set canvas size java**、啟用 **automatic layout scaling**，並學會如何 **configure canvas mode** 以產生高品質輸出。本教學為您的 CAD 轉換專案奠定了堅實基礎。欲了解更多功能與可能性，請參閱 [Aspose.CAD 文件](https://reference.aspose.com/cad/java/)。

## 常見問答

### Q1: 我可以在其他 Java 框架中使用 Aspose.CAD for Java 嗎？

A1: 可以，Aspose.CAD 設計上能無縫整合至各種 Java 框架。

### Q2: Aspose.CAD 是否提供臨時授權？

A2: 有的，您可以在此取得臨時授權 [here](https://purchase.aspose.com/temporary-license/)。

### Q3: 我可以在哪裡取得 Aspose.CAD 的社群支援？

A3: 請前往 [Aspose.CAD 論壇](https://forum.aspose.com/c/cad/19) 取得社群支援與討論。

### Q4: 我可以免費試用 Aspose.CAD 嗎？

A4: 當然可以！請在此取得免費試用版 [here](https://releases.aspose.com/)。

### Q5: 我要如何購買 Aspose.CAD for Java？

A5: 請在此購買產品 [here](https://purchase.aspose.com/buy)。

**Additional Q&A**

**Q: 畫布大小會影響 PDF 中向量的品質嗎？**  
A: 不會。畫布大小僅決定頁面尺寸，向量資料仍保持解析度獨立，無論放大多少皆能保持清晰。

**Q: 我可以為 TIFF 輸出設定不同的 DPI 嗎？**  
A: 可以。在建立 `TiffOptions` 前，先使用 `rasterizationOptions.setResolution(dpiValue)` 調整解析度。

---

**最後更新：** 2025-12-10  
**測試環境：** Aspose.CAD for Java 24.12  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}