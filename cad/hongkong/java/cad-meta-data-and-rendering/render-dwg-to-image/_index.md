---
date: 2025-12-28
description: 學習如何使用 Aspose.CAD for Java 將 DWG 轉換為 PDF，從 CAD 建立 PDF。按照逐步說明將 DWG 版面匯出為
  PDF 並產生圖像。
linktitle: Render DWG Document to Image with Java
second_title: Aspose.CAD Java API
title: 從 CAD 建立 PDF - 使用 Aspose.CAD for Java 將 DWG 轉為圖像
url: /zh-hant/java/cad-meta-data-and-rendering/render-dwg-to-image/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.CAD for Java 將 DWG 文件渲染為圖像

## 簡介

在充滿活力的 Java 開發領域，Aspose.CAD 脫穎而出，成為處理電腦輔助設計（CAD）檔案的強大工具。**本教學將示範如何從 CAD 建立 PDF**，方法是先將 DWG 文件渲染為圖像，再匯出為 PDF。無論您是資深開發者或剛踏入程式設計之路，此一步一步的指南都會清晰且輕鬆地帶領您完成整個流程。

## 快速解答
- **需要什麼函式庫？** Aspose.CAD for Java.
- **可以將 DWG 轉換為 PDF 嗎？** Yes – the example demonstrates converting a DWG layout to PDF.
- **生產環境需要授權嗎？** A valid Aspose.CAD license is required for non‑evaluation use.
- **支援哪些 IDE？** Eclipse, IntelliJ IDEA, NetBeans, and any IDE that supports Java.
- **有哪些輸出格式？** PDF, PNG, JPEG, BMP, and other raster formats.

## 什麼是從 CAD 建立 PDF？

從 CAD 建立 PDF 意指將向量繪圖（例如 DWG 檔案）轉換為 PDF 文件，無論是光柵化或向量化。這使得技術圖紙能輕鬆分享、列印與保存，而不必依賴原始的 CAD 應用程式。

## 為什麼使用 Aspose.CAD for Java？

- **無需外部相依性** – 此函式庫即開箱即用。
- **高保真渲染** – 保持線寬、圖層與版面配置。
- **批次處理** – 可一次執行多個圖紙的轉換。
- **跨平台** – 支援 Windows、Linux 與 macOS。

## 前置條件

- **Java 開發環境** – 已安裝 JDK 8 或更高版本。
- **Aspose.CAD for Java 函式庫** – 從 [download link](https://releases.aspose.com/cad/java/) 下載。
- **DWG 文件** – 您想要渲染的 DWG 檔案（範例或自有檔案）。

## 匯入命名空間

在 Java 程式碼中，匯入必要的類別以使用 Aspose.CAD 功能：

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

現在，讓我們將範例程式碼分解為多個步驟，以便全面了解：

## 步驟 1：指定資源目錄

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

將 `"Your Document Directory"` 替換為實際存放 DWG 檔案的路徑。

## 步驟 2：載入 DWG 文件

```java
String srcFile = dataDir + "visualization_-_conference_room.dwg";
Image image = Image.load(srcFile);
```

此程式碼將 DWG 檔案載入為 Aspose.CAD 可處理的 `Image` 物件。

## 步驟 3：設定光柵化選項

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
rasterizationOptions.setLayouts(new String[] {"Layout1"});
```

在此我們定義圖紙的光柵化方式：頁面尺寸以及要渲染的特定版面。這是 **render dwg to image** 與 **export dwg layout pdf** 的關鍵步驟。

## 步驟 4：建立 PDF 選項

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

`PdfOptions` 將光柵化設定與 PDF 輸出格式結合。

## 步驟 5：匯出為 PDF

```java
image.save(dataDir + "ExportSpecificLayoutToPDF_out_.pdf", pdfOptions);
```

`save` 方法將渲染後的圖像寫入 PDF 檔案，實際上執行 **convert dwg to pdf**。

## 常見問題與解決方案

| 問題 | 解決方案 |
|-------|----------|
| **找不到檔案** | 確認 `dataDir` 指向正確的資料夾，且 DWG 檔名正確。 |
| **PDF 輸出為空白** | 確保版面名稱（`"Layout1"`）在 DWG 檔案中存在；可使用 `image.getAvailableLayouts()` 列出所有版面。 |
| **圖像品質低** | 增加 `PageWidth` 與 `PageHeight`，或設定 `rasterizationOptions.setResolution(300);`。 |

## 常見問答

### Q1：我可以從單一 DWG 檔案渲染多個版面嗎？

A1：可以，只要相應地修改 `setLayouts` 陣列中的版面名稱即可。

### Q2：Aspose.CAD 是否相容於不同的 Java IDE？

A2：是的，Aspose.CAD 相容於常見的 Java IDE，如 Eclipse、IntelliJ IDEA 等。

### Q3：我可以在哪裡取得更多協助與支援？

A3：請前往 [Aspose.CAD 論壇](https://forum.aspose.com/c/cad/19) 取得社群支援與討論。

### Q4：如何取得 Aspose.CAD 的臨時授權？

A4：您可從 [此處](https://purchase.aspose.com/temporary-license/) 取得臨時授權。

### Q5：Aspose.CAD 是否提供更多渲染選項？

A5：當然，請參閱完整的 [文件](https://reference.aspose.com/cad/java/) 以取得詳細資訊。

---

**最後更新：** 2025-12-28  
**測試環境：** Aspose.CAD for Java 24.11  
**作者：** Aspose

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
