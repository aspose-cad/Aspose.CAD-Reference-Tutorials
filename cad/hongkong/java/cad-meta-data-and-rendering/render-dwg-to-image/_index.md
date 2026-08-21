---
date: 2026-04-23
description: 學習如何使用 Aspose.CAD for Java 將 DWG 轉換為 PDF，從 CAD 建立 PDF。遵循逐步說明將 DWG 版面匯出為
  PDF 並產生圖像。
keywords:
- create pdf from cad
- convert dwg to pdf
- render dwg to image
- export dwg layout pdf
- dwg to png conversion
linktitle: 使用 Java 將 DWG 文件渲染為圖像
second_title: Aspose.CAD Java API
title: 使用 Aspose.CAD for Java 從 CAD 建立 PDF - DWG 轉圖像
url: /zh-hant/java/cad-meta-data-and-rendering/render-dwg-to-image/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.CAD for Java 將 DWG 文件渲染為圖像

## 介紹

在充滿活力的 Java 開發領域，Aspose.CAD 脫穎而出，成為處理電腦輔助設計（CAD）檔案的強大工具。**本教學示範如何從 CAD 建立 PDF**，透過將 DWG 文件渲染成圖像再匯出為 PDF。無論您是資深開發者或剛踏入程式碼世界，本步驟式指南都會清晰且輕鬆地帶領您完成整個流程。

## 快速解答
- **需要哪個函式庫？** Aspose.CAD for Java.  
- **可以將 DWG 轉換為 PDF 嗎？** 可以 – 範例示範了將 DWG 版面轉換為 PDF。  
- **正式環境需要授權嗎？** 非評估使用需具備有效的 Aspose.CAD 授權。  
- **支援哪些 IDE？** Eclipse、IntelliJ IDEA、NetBeans，以及任何支援 Java 的 IDE。  
- **提供哪些輸出格式？** PDF、PNG、JPEG、BMP 以及其他點陣格式。

## 什麼是從 CAD 建立 PDF？
從 CAD 建立 PDF 意指將向量繪圖（例如 DWG 檔案）轉換為點陣或向量的 PDF 文件。這讓技術圖紙能輕鬆分享、列印與保存，而無需原始 CAD 應用程式。

## 為什麼使用 Aspose.CAD for Java？
- **無外部相依性** – 函式庫即開箱即用。  
- **高保真渲染** – 保持線寬、圖層與版面配置。  
- **批次處理** – 可在一次執行中轉換多個圖紙。  
- **跨平台** – 支援 Windows、Linux 與 macOS。

## 常見使用情境
- 產生可列印的建築藍圖 PDF。  
- 將 DWG 檔案轉換為 PNG/JPEG 以供網站預覽。  
- 自動批量將 DWG 版面轉換為 PDF，以作為存檔用途。  

## 前置條件

- **Java 開發環境** – 已安裝 JDK 8 或以上版本。  
- **Aspose.CAD for Java 函式庫** – 從[下載連結](https://releases.aspose.com/cad/java/)下載。  
- **DWG 文件** – 您想要渲染的 DWG 檔案（範例或自有檔案）。

## 匯入命名空間

在 Java 程式碼中，匯入必要的類別以使用 Aspose.CAD 功能：

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

現在，讓我們將範例程式碼拆解為多個步驟，以便全面了解：

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

此步驟會將 DWG 檔案載入為 Aspose.CAD 可處理的 `Image` 物件。

## 步驟 3：設定點陣化選項

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
rasterizationOptions.setLayouts(new String[] {"Layout1"});
```

在此我們定義圖紙的點陣化方式：頁面大小與要渲染的特定版面。這是 **render dwg to image** 與 **export dwg layout pdf** 的關鍵步驟。

## 步驟 4：建立 PDF 選項

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

`PdfOptions` 將點陣化設定與 PDF 輸出格式結合。

## 步驟 5：匯出為 PDF

```java
image.save(dataDir + "ExportSpecificLayoutToPDF_out_.pdf", pdfOptions);
```

`save` 方法會將渲染後的圖像寫入 PDF 檔案，實際上完成 **convert dwg to pdf**。

## 如何將 dwg 轉換為 png（可選）

如果需要點陣圖像而非 PDF，只需將 `PdfOptions` 替換為 `PngOptions`（或 `JpegOptions`）。相同的 `rasterizationOptions` 物件可重複使用，為您提供快速的 **dwg to png conversion** 路徑。

## 常見問題與解決方案
| 問題 | 解決方案 |
|-------|----------|
| **找不到檔案** | 確認 `dataDir` 指向正確的資料夾，且 DWG 檔名正確。 |
| **PDF 輸出空白** | 確保版面名稱（`"Layout1"`）在 DWG 檔案中存在；使用 `image.getAvailableLayouts()` 列出所有版面。 |
| **圖像品質低** | 增加 `PageWidth` 與 `PageHeight`，或設定 `rasterizationOptions.setResolution(300);`。 |

## 提示與最佳實踐
- **專業提示：** 在設定版面陣列前呼叫 `image.getAvailableLayouts()`，以避免版面名稱拼寫錯誤。  
- **效能提示：** 處理大量檔案時重複使用單一 `CadRasterizationOptions` 實例，可減少物件建立的開銷。  
- **品質提示：** 對於向量 PDF，保持解析度在中等（150‑200 DPI）即可，讓 Aspose.CAD 處理線條縮放。

## 常見問答

### Q1：我可以從單一 DWG 檔案渲染多個版面嗎？

A1：可以。只需相應地修改 `setLayouts` 陣列中的版面名稱即可。

### Q2：Aspose.CAD 相容於不同的 Java IDE 嗎？

A2：可以，Aspose.CAD 相容於常見的 Java IDE，例如 Eclipse、IntelliJ IDEA 等。

### Q3：我可以在哪裡取得更多協助與支援？

A3：前往 [Aspose.CAD 論壇](https://forum.aspose.com/c/cad/19) 取得社群支援與討論。

### Q4：如何取得 Aspose.CAD 的臨時授權？

A4：您可從[此處](https://purchase.aspose.com/temporary-license/)取得臨時授權。

### Q5：Aspose.CAD 是否提供更多渲染選項？

A5：當然，請參考完整的[文件說明](https://reference.aspose.com/cad/java/)以取得詳細資訊。

## 結論

現在您已掌握使用 Aspose.CAD for Java 的完整端對端 **create pdf from cad** 工作流程。透過調整點陣化設定，亦可產生 PNG、JPEG 或 BMP 檔案，使此方法成為任何基於 Java 的 CAD 處理管線的多功能 **dwg to pdf guide**。歡迎嘗試批次轉換、不同版面與更高解析度，以符合您的專案需求。

---

**最後更新：** 2026-04-23  
**測試環境：** Aspose.CAD for Java 24.12  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}