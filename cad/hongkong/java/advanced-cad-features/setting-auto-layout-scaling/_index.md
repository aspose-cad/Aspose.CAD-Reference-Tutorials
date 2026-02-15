---
date: 2026-02-15
description: 學習如何設定自訂頁面大小，並使用 Aspose.CAD for Java 從 CAD 產生 PDF。本分步指南說明如何使用自動版面縮放將
  CAD 匯出為 PDF。
linktitle: Setting Auto Layout Scaling
second_title: Aspose.CAD Java API
title: 設定自訂頁面大小 – 從 CAD 產生 PDF，使用自動版面縮放
url: /zh-hant/java/advanced-cad-features/setting-auto-layout-scaling/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 設定自訂頁面尺寸 – 使用自動版面縮放從 CAD 建立 PDF

## 介紹

如果您需要在**設定自訂頁面尺寸**的同時**快速且完美縮放地從 CAD 建立 PDF**，Aspose.CAD for Java 能滿足您的需求。Auto Layout Scaling 會自動調整版面尺寸，確保產生的 PDF 完全符合預期，無論原始 CAD 的頁面尺寸為何。在本教學中，我們將完整示範從載入 DXF 檔案到匯出 PDF 的流程，同時強調本函式庫的**export CAD to PDF** 功能，並說明如何在需要時**convert DWG to PDF**或**increase PDF resolution**。

## 快速解答
- **Auto Layout Scaling 會做什麼？** 它會在光柵化時自動調整 CAD 版面大小，使其符合目標頁面尺寸。  
- **可以轉換哪些格式？** 任何 Aspose.CAD 支援的格式（例如 DXF、DWG、DWF）皆可轉換為 PDF。  
- **生產環境需要授權嗎？** 是的，非評估使用必須取得商業授權。  
- **轉換需要多久？** 在現代硬體上，標準檔案通常在一秒內完成。  
- **可以更改頁面尺寸嗎？** 可以，您可透過 `CadRasterizationOptions` 設定自訂頁面尺寸。

## 什麼是「從 CAD 建立 PDF」？

從 CAD 建立 PDF，即是將向量式工程圖（DXF、DWG 等）光柵化為 PDF 文件。PDF 保留原始圖紙的視覺精度，且可在任何平台上廣泛檢視。

## 為何使用 Auto Layout Scaling？

- **一致的輸出**：保證所有版面填滿 PDF 頁面，無需手動計算尺寸。  
- **節省時間**：免除為每張圖紙手動調整縮放比例的需求。  
- **高品質**：在轉換過程中保持線寬與幾何精度。  
- **彈性**：支援 **convert dxf to pdf**、**convert dwg to pdf**，以及在需要**increase PDF resolution** 以供列印的情況。

## 前置條件

1. **Aspose.CAD for Java Library** – 從[下載頁面](https://releases.aspose.com/cad/java/)下載最新版本。  
2. **Resource Directory** – 在本機建立資料夾以存放 CAD 檔案；於程式碼中將 `"Your Document Directory"` 替換為該路徑。  
3. **Sample CAD File** – 本教學使用 `conic_pyramid.dxf`，此檔案已包含於 Aspose 範例資料集中。

## 匯入命名空間

首先，匯入所需的類別。這樣即可使用影像載入、光柵化與 PDF 匯出功能。

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## 如何為 PDF from CAD 設定自訂頁面尺寸

在深入逐步程式碼之前，我們先了解為何設定自訂頁面尺寸很重要。當您**設定自訂頁面尺寸**時，即可控制產生 PDF 的實體尺寸（例如 A4、Letter 或自訂尺寸）。這對於圖紙必須符合紙張標準的工程流程，或需要將 PDF 嵌入較大文件時，都是必不可少的。

### 步驟 1：載入 CAD 檔案

載入來源檔案是**how to export CAD** 為 PDF 文件的第一步。

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

### 步驟 2：建立光柵化選項

定義目標頁面尺寸。若您想使用自訂版面，也可以在此區塊手動**set CAD page size**。

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
```

### 步驟 3：設定 Auto Layout Scaling

啟用自動縮放功能。這是**how to set scaling** 在 CAD 轉 PDF 轉換中的核心。

```java
rasterizationOptions.setAutomaticLayoutsScaling(true);
```

### 步驟 4：建立 PDF 選項

將光柵化設定連結至 PDF 匯出選項。

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### 步驟 5：匯出為 PDF

最後，將渲染的影像儲存為 PDF 檔案。此步驟完成 **convert dxf to pdf** 工作流程。

```java
image.save(dataDir + "result_out_.pdf", pdfOptions);
```

對於任何其他需要處理的 CAD 檔案，請重複上述步驟，無論是 **DWG**、**DWF** 或其他支援的格式。

## 常見使用情境

| 情境 | 為何要設定自訂頁面尺寸？ |
|----------|-----------------------------|
| **建築圖紙提交** | 使 PDF 與監管機構要求的標準 A1/A2 紙張尺寸相符。 |
| **嵌入技術手冊** | 確保圖紙在手冊的預設版面中完整呈現，無需額外縮放。 |
| **高解析度列印** | 可在保持頁面尺寸一致的前提下提升 DPI（例如 `rasterizationOptions.setResolution(300)`）。 |

## 常見問題與疑難排解

| 現象 | 可能原因 | 解決方法 |
|---------|--------------|-----|
| PDF 為空白 | 未設定光柵化選項或檔案路徑不正確 | 確認 `srcFile` 路徑，並確保 `setPageWidth/Height` 為非零值 |
| 縮放失真 | `setAutomaticLayoutsScaling` 保持為 `false` | 啟用自動縮放或手動計算縮放係數 |
| 圖層缺失 | 來源 DXF 包含不支援的實體 | 查閱 Aspose.CAD 發行說明以了解支援的實體類型 |

## 常見問答

**Q: Aspose.CAD for Java 是否相容所有 CAD 檔案格式？**  
A: Aspose.CAD for Java 支援多種 CAD 格式，包括 DWG、DXF 與 DWF。

**Q: 我可以進一步自訂縮放選項嗎？**  
A: 可以，`CadRasterizationOptions` 類別提供屬性以微調縮放、DPI 以及其他光柵化設定。

**Q: 我在哪裡可以找到 Aspose.CAD for Java 的其他文件？**  
A: 請參考[文件說明](https://reference.aspose.com/cad/java/)，內含深入資訊與範例。

**Q: Aspose.CAD for Java 有提供免費試用嗎？**  
A: 有，您可透過[免費試用](https://releases.aspose.com/)體驗 Aspose.CAD for Java 的功能。

**Q: 我該如何取得協助或參與 Aspose.CAD for Java 的討論？**  
A: 前往[Aspose.CAD 論壇](https://forum.aspose.com/c/cad/19)與社群交流並取得支援。

### 其他常見問題

**Q: 如何將 DWG 檔案轉為 PDF 而非 DXF？**  
A: 同樣的程式碼即可，只需將 `srcFile` 的副檔名改為 `.dwg`。

**Q: 我可以設定自訂 DPI 以產生更高解析度的 PDF 嗎？**  
A: 可以，使用 `rasterizationOptions.setResolution(300);`（或任何您需要的 DPI）。

**Q: 能否在產生的 PDF 中嵌入字型？**  
A: Aspose.CAD 會將圖紙光柵化，字型會以向量方式呈現，無需額外嵌入字型。

## 結論

透過本指南，您現在已了解如何使用 Aspose.CAD for Java 搭配 Auto Layout Scaling **設定自訂頁面尺寸** 並 **從 CAD 建立 PDF**。此流程簡化了 **export CAD to PDF** 工作流程，確保縮放一致，並為您節省寶貴的開發時間。歡迎嘗試不同的頁面尺寸、解析度與 CAD 格式，以符合專案需求，無論是 **converting DWG to PDF**、**increasing PDF resolution**，或是建置 **java CAD to PDF** 批次處理器。

---

**最後更新：** 2026-02-15  
**測試環境：** Aspose.CAD for Java 24.12（最新）  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}