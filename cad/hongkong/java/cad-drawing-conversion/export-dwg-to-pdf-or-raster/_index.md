---
date: 2026-02-17
description: 了解 Java CAD 函式庫 Aspose.CAD for Java 如何快速且精確地將 DWG 匯出為 PDF 或點陣圖像。
linktitle: Export DWG to PDF or Raster
second_title: Aspose.CAD Java API
title: 使用 Java CAD 函式庫 Aspose.CAD for Java 匯出 DWG 為 PDF 或點陣圖
url: /zh-hant/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 java cad library Aspose.CAD for Java 將 DWG 匯出為 PDF 或點陣圖

## 介紹

在電腦輔助設計（CAD）這個充滿變化的領域中，圖紙的高效處理至關重要。使用 **java cad library** **Aspose.CAD for Java**，您只需幾行程式碼即可 **export dwg to pdf** — 或點陣圖 — 。本教學將帶您完整了解從載入 DWG 檔案到產生高品質 PDF 的全過程，同時說明為何 Aspose.CAD Java 是 CAD 轉換任務的首選函式庫。

## 快速回答
- **本教學涵蓋什麼內容？** 使用 Aspose.CAD for Java 將 DWG 檔案匯出為 PDF 或點陣圖。  
- **需要授權嗎？** 可取得免費的暫時授權供評估使用；正式上線需購買完整授權。  
- **支援哪個 Java 版本？** 任意 Java 8+ 執行環境皆可搭配最新的 Aspose.CAD Java API。  
- **可以將 DWG 轉成其他影像格式嗎？** 可以 — 相同的點陣化選項可輸出 PNG、JPEG、BMP 等格式。  
- **轉換需要多長時間？** 標準圖紙通常在一秒以內完成；較大的檔案可能需要數秒。

## 為什麼 java cad library 是 DWG 轉換的最佳選擇？

- **Pure Java implementation** – 無需原生 DLL 或外部工具。  
- **Accurate unit handling** – 會自動偵測公制與英制單位。  
- **High‑quality raster output** – 可細緻調整 DPI 與頁面大小。  
- **Full PDF support** – 產生保留向量的 PDF，無需額外相依性。  
- **Flexible licensing** – 可先使用 **temporary license aspose** 進行測試，正式上線再升級。

## 什麼是「export dwg to pdf」？

將 DWG 匯出為 PDF 意指將原生 AutoCAD 圖紙轉換成可攜、與裝置無關的 PDF 文件。產生的 PDF 會保留向量資料、圖層與比例，適合分享、列印或存檔。

## 為什麼要使用 Aspose.CAD Java 進行此轉換？

因為 **java cad library** 內部已處理單位轉換與點陣化等所有細節，您不必依賴第三方工具，即可在各平台上取得一致的轉換結果。

## 前置條件

在開始撰寫程式碼前，請確保您已具備：

- 基本的 Java 程式設計知識。  
- 已安裝 Aspose.CAD for Java 函式庫。若尚未下載，請前往 **[here](https://releases.aspose.com/cad/java/)** 取得。  
- 用於測試的 DWG 檔案 — 本教學使用範例 **Bottom_plate.dwg**。

## 匯入命名空間

在您的 Java 專案中匯入必要的類別以啟動轉換：

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.UnitType;
```

## 步驟說明

### 步驟 1：載入 DWG 檔案

首先，使用 `Image` 類別載入 DWG 圖紙。這會在記憶體中建立 Aspose.CAD 可操作的圖形表示。

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Bottom_plate.dwg";
Image objImage = Image.load(srcFile);
```

### 步驟 2：判斷單位類型

了解圖紙使用的是公制還是英制單位對正確縮放至關重要。輔助方法 `IsMetric`（此處省略實作）會回傳布林值。

```java
Boolean currentUnitIsMetric = IsMetric(objImage.getUnitType());
int currentUnitCoefficient = objImage.getUnitType();
```

### 步驟 3：設定點陣化選項

根據單位系統，設定頁面大小、縮放比例與目標單位類型。這些選項決定 DWG 在被包裝成 PDF 前的點陣化方式。

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();

if (currentUnitIsMetric) {
    // Metric units
    double metersCoeff = 1 / 1000.0;
    double scaleFactor = metersCoeff / currentUnitCoefficient;
    rasterizationOptions.setPageWidth((float)(210 * scaleFactor));
    rasterizationOptions.setPageHeight((float)(297 * scaleFactor));
    rasterizationOptions.setUnitType(UnitType.Millimeter);
} else {
    // Imperial units
    rasterizationOptions.setPageWidth((float)(8.27f / currentUnitCoefficient));
    rasterizationOptions.setPageHeight((float)(11.69f / currentUnitCoefficient));
    rasterizationOptions.setUnitType(UnitType.Inch);
}
```

### 步驟 4：設定 PDF 選項 (pdf options cad)

建立 `PdfOptions` 實例並附加點陣化設定。這告訴 Aspose.CAD 如何將點陣化內容嵌入最終的 PDF。

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());
```

### 步驟 5：儲存為 PDF

最後，將圖紙匯出為 PDF 檔案。`save` 方法接受輸出路徑與先前設定好的 `PdfOptions`。

```java
objImage.save(dataDir + "Saved.pdf", pdfOptions);
```

程式執行完畢後，您會在 `DWGDrawings` 資料夾中看到 **Saved.pdf**，即可用於發佈或存檔。

## 如何使用 java cad library 轉換 dwg 為點陣圖

若需要點陣圖而非 PDF，只需將 `PdfOptions` 替換為相應的點陣圖選項（例如 `PngOptions`、`JpegOptions`）。同一個 `CadRasterizationOptions` 例項即可重複使用，讓您以最少的程式碼變更 **convert dwg raster**。

## 如何使用 pdf options cad 產生 pdf dwg

上述範例已 **generates pdf dwg** 輸出。透過調整 `pdfOptions`（例如設定 `pdfOptions.setCompress(true)`），即可控制 PDF 的大小與品質，展示 **pdf options cad** API 的彈性。

## 常見問題與技巧

- **Incorrect page size** – 請再次確認單位轉換邏輯；係數不匹配可能導致頁面過大。  
- **Missing fonts or lineweights** – 轉換前請確保 DWG 已正確引用所有外部資源。  
- **Performance on large drawings** – 僅在需要更高品質時提升 `CadRasterizationOptions` 的 `DPI` 設定；較低的 DPI 可加速處理。  
- **License concerns** – 評估階段可使用 **temporary license aspose**；正式上線則必須購買完整授權。

## 常見問答

**Q: 可以在其他 Java 框架中使用 Aspose.CAD for Java 嗎？**  
A: 可以，Aspose.CAD for Java 可無縫整合至常見的 Java 框架，如 Spring、Jakarta EE 與 Android。

**Q: Aspose.CAD for Java 是否提供暫時授權？**  
A: 有，您可在 **[here](https://purchase.aspose.com/temporary-license/)** 取得暫時授權。

**Q: 在哪裡可以取得 Aspose.CAD for Java 的支援？**  
A: 請前往 **[Aspose.CAD forum](https://forum.aspose.com/c/cad/19)**，由社群與 Aspose 工程師提供協助。

**Q: 如何購買 Aspose.CAD for Java 的授權？**  
A: 您可在 **[here](https://purchase.aspose.com/buy)** 購買授權。

**Q: Aspose.CAD for Java 支援哪些單位？**  
A: Aspose.CAD for Java 同時支援公制與英制單位，會自動偵測圖紙的單位系統。

**Q: 能否使用相同的 API 將 DWG 轉成其他影像格式（例如 PNG、JPEG）？**  
A: 完全可以。只要將 `PdfOptions` 替換為相應的點陣圖選項（如 `PngOptions`），並重用相同的 `CadRasterizationOptions`。

## 結論

本教學示範了如何使用 **java cad library** Aspose.CAD for Java **export dwg to pdf** 以及點陣圖。依循步驟說明，您即可在任何 Java 應用程式中整合可靠的 CAD 轉換功能，無論是需要 PDF 供文件使用，或是點陣圖供網頁顯示。

---

**最後更新：** 2026-02-17  
**測試環境：** Aspose.CAD for Java 24.10  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}