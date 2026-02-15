---
date: 2026-02-15
description: 學習如何在使用 Aspose.CAD for Java 轉換 CAD 為 PDF 和 TIFF 時設定背景顏色。探索如何變更 CAD 背景顏色、將
  CAD 轉換為 PDF，以及將 CAD 轉換為 TIFF，並全面掌控繪圖顏色。
linktitle: Setting Background and Drawing Color
second_title: Aspose.CAD Java API
title: 使用 Aspose.CAD for Java 設定背景顏色
url: /zh-hant/java/advanced-cad-features/setting-background-and-drawing-color/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 Java 中設定背景顏色與 Aspose.CAD for Java

## 介紹

在現代 CAD 工作流程中，能夠在轉換過程中 **設定背景顏色（Java）** 是產出清晰、可直接用於簡報的文件的關鍵。Aspose.CAD for Java 讓將 CAD 檔案轉換為 PDF 或 TIFF 變得簡單，同時讓您完整掌控背景與繪圖顏色。本教學將逐步說明整個流程——從載入 DXF 檔案到匯出 PDF 與 TIFF 檔案並套用您選擇的顏色。您也會了解為何更改 CAD 背景顏色能提升可讀性，以及如何將此步驟整合至更大的批次處理流程。

## 快速回答
- **哪個函式庫負責在 Java 中的 CAD 轉換？** Aspose.CAD for Java.  
- **我可以在轉換過程中更改背景顏色嗎？** 是，使用 `CadRasterizationOptions.setBackgroundColor`.  
- **支援哪些輸出格式？** PDF 與 TIFF（皆為點陣化）.  
- **正式使用是否需要授權？** 需要商業授權；亦提供免費試用.  
- **是否支援批次轉換？** 當然可以——在迴圈中使用相同設定處理多個檔案.

## 「設定背景顏色（Java）」在 CAD 轉換中的意義是什麼？
在 CAD 轉換的情境下，「設定背景顏色（Java）」指的是配置點陣化選項，使產生的圖像（PDF 或 TIFF）使用您指定的顏色，而非預設的白色畫布。這可提升視覺對比，特別是當 CAD 圖面包含淡色線條時。

## 為什麼在 CAD 轉換時設定背景顏色（Java）很重要？
- **提升視覺清晰度** — 深色或彩色背景能讓細微幾何圖形更突出。  
- **品牌一致性** — 讓背景與公司色彩相匹配，以符合報告需求。  
- **列印就緒的輸出** — 某些印表機對非白色背景的處理較佳，可減少白色區域的墨水使用。  
- **自動化友好** — 同一設定可在批次作業中套用於數百個檔案。

## 前置條件

在開始之前，請確保您已具備：

- **Aspose.CAD for Java Library** – 在此下載 [here](https://releases.aspose.com/cad/java/).  
- **存放 CAD 檔案的資料夾** – 請將 `"Your Document Directory" + "CADConversion/"` 替換為您機器上的實際路徑。

## 匯入命名空間

首先，匯入您需要的類別。這些匯入讓您能使用顏色處理、點陣化選項以及輸出格式。

```java
import java.awt.Color;
import java.awt.Image;

import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## 步驟說明

### 步驟 1：載入 CAD 檔案

我們將載入來源 DXF（或任何支援的 CAD 格式）至 `Image` 物件。

```java
String dataDir = "Your Document Directory" + "CADConversion/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image objImage = Image.load(srcFile);
```

### 步驟 2：設定背景與繪圖顏色

在此我們設定頁面尺寸、選擇背景顏色，並告訴渲染器使用特定的繪圖顏色取代原始 CAD 顏色。

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
rasterizationOptions.setBackgroundColor(com.aspose.cad.Color.getBeige());   // example background
rasterizationOptions.setDrawType(CadDrawTypeMode.UseDrawColor);
rasterizationOptions.setBackgroundColor(com.aspose.cad.Color.getBlue());   // overwrite with blue if needed
```

> **專業提示：** 若想保留 CAD 原始顏色同時套用自訂背景，可嘗試 `CadDrawTypeMode.UseOriginalColors`。

### 步驟 3：建立 PDF 並儲存

我們將點陣化選項綁定至 `PdfOptions`，並將結果儲存為 PDF 檔案。

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

### 步驟 4：建立 TIFF 並儲存

相同的點陣化設定也可用於 TIFF 輸出。

```java
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

## 更改 CAD 背景顏色的常見使用情境
- **簡報投影片** – 深色背景能讓線條在投影片上更突出。  
- **技術文件** – 背景與文件主題相匹配可提升一致性。  
- **自動化報告** – 產生符合公司配色方案的 PDF，免除手動後處理。  
- **檔案保存** – 使用中性背景的 TIFF 可減少壓縮雜訊。

## 常見問題與解決方案

| 問題 | 解決方案 |
|-------|----------|
| **背景顏色未變更** | 確保在設定繪圖類型之後呼叫 `setBackgroundColor`。第二次呼叫會覆寫第一次，因此請將欲使用的顏色作為最後一次呼叫。 |
| **輸出模糊** | 增加 `PageWidth`/`PageHeight` 或透過 `rasterizationOptions.setResolution(...)` 設定更高的 DPI。 |
| **找不到檔案例外** | 確認 `dataDir` 路徑以分隔符（`/` 或 `\\`）結尾，且檔案確實存在。 |

## 疑難排解與最佳實踐
- **始終釋放資源** – 完成儲存後呼叫 `objImage.dispose()` 以釋放原生記憶體。  
- **批次處理技巧** – 只建立一次 `CadRasterizationOptions`，在迴圈中重複使用以提升效能。  
- **顏色選擇** – 使用 `com.aspose.cad.Color` 常數取得常見顏色，或使用 `new Color(r, g, b)` 建立自訂顏色。  
- **DPI 考量** – 列印品質的 PDF 建議使用 300–600 DPI；螢幕顯示則 96–150 DPI 足夠。

## 常見問答

**Q: Aspose.CAD for Java 是否適合批次轉換？**  
A: 當然可以。您可以將程式碼放入迴圈中，以相同的點陣化設定處理數十個檔案。

**Q: 我可以自訂產生檔案的背景顏色嗎？**  
A: 可以。本教學示範如何為 PDF 與 TIFF 輸出設定任意 `com.aspose.cad.Color`。

**Q: 我在哪裡可以找到 Aspose.CAD for Java 的完整文件？**  
A: 請參考 [documentation](https://reference.aspose.com/cad/java/) 以取得深入說明與更多範例。

**Q: 是否提供免費試用？**  
A: 有，您可透過 [free trial](https://releases.aspose.com/) 體驗功能。

**Q: 我要如何取得 Aspose.CAD for Java 的支援？**  
A: 前往 [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) 提問並與社群分享使用經驗。

## 結論與後續步驟

現在您已掌握在將 CAD 圖面轉換為 PDF 或 TIFF 時 **設定背景顏色（Java）** 的完整、可投入生產的做法。您可以嘗試更換背景顏色、調整 DPI，或將此方法與其他 Aspose.CAD 功能（如圖層過濾或向量轉點陣）結合。準備好後，可進一步探索 **如何使用自訂頁面尺寸將 CAD 轉換為 PDF** 或 **為大型工程檔案優化 TIFF 壓縮** 等相關主題。

---

**最後更新：** 2026-02-15  
**測試環境：** Aspose.CAD for Java 24.11  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}