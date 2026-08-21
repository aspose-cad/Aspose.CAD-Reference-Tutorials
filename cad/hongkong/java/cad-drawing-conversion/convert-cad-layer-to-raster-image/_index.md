---
date: 2026-04-13
description: 學習如何使用 Aspose.CAD for Java 在 Java 中光柵化 CAD 圖層。本逐步指南展示了圖層層級的光柵圖像轉換。
keywords:
- java rasterize cad layer
- Aspose CAD Java
- convert CAD layer to raster
linktitle: 將 CAD 圖層轉換為點陣圖格式
second_title: Aspose.CAD Java API
title: Java 光柵化 CAD 圖層 – Aspose CAD 教學
url: /zh-hant/java/cad-drawing-conversion/convert-cad-layer-to-raster-image/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose CAD Java 教學：將 CAD 圖層轉換為點陣圖格式

## 簡介

如果您需要 **java rasterize cad layer** 檔案以便更容易分享、列印或後續影像處理，您來對地方了。在本教學中，我們將說明 Aspose.CAD for Java 如何讓您從 CAD 圖面中挑選單一圖層，並將其匯出為高品質的點陣圖，例如 JPEG、PNG 或 BMP。完成後，您將了解為何選擇性點陣化很重要、如何設定點陣化選項，以及如何僅用幾行程式碼儲存結果。

## 快速解答
- **本教學涵蓋什麼內容？** 使用 Aspose.CAD for Java 將選取的 CAD 圖層轉換為點陣圖。  
- **支援哪些格式？** 任何 Aspose 支援的點陣格式（JPEG、PNG、BMP 等）。  
- **需要授權嗎？** 免費試用可用於開發；正式環境需購買授權。  
- **先決條件是什麼？** Java 開發環境與 Aspose.CAD Java 函式庫。  
- **實作需要多長時間？** 基本轉換大約需要 10–15 分鐘。

## 什麼是「java rasterize cad layer」？

將 CAD 圖層點陣化是指將該圖層的向量資料轉換為像素圖像。此過程保留圖層的視覺外觀，同時使其能在任何支援標準影像格式的系統上顯示。

## 為何使用此方法？

- **Selective Export** – 只渲染您需要的圖層，減少檔案大小與處理時間。  
- **Format Flexibility** – 將 `JpegOptions` 換成 `PngOptions`、`BmpOptions` 等，無需更改核心邏輯。  
- **High‑Quality Rendering** – Aspose.CAD 完全保留線寬、顏色與文字，與原始 CAD 檔案一致。

## 先決條件

在開始編寫程式碼之前，請確保您具備以下條件：

- **Java Development Environment** – 已安裝並設定 JDK 8 或以上版本。  
- **Aspose.CAD Library** – 從 [download link](https://releases.aspose.com/cad/java/) 下載並安裝 Aspose.CAD Java 函式庫。

## 匯入命名空間

在此步驟中，我們將匯入必要的類別，以開始處理 CAD 檔案。

### 匯入 Aspose.CAD 類別

在您的 Java 原始檔中，加入所需的 Aspose.CAD 匯入語句：

```java
import com.aspose.cad.Image;


import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import java.util.ArrayList;
import java.util.Arrays;
import java.util.List;
```

## 將 CAD 圖層轉換為點陣圖格式

以下為完整的逐步流程。每個步驟在程式碼區塊前都有簡單說明，讓您清楚了解發生的事情。

### 步驟 1：設定 CAD 檔案

首先，指定您的 CAD 檔案路徑，並將其載入 `Image` 物件。

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

### 步驟 2：設定點陣化選項

建立 `CadRasterizationOptions` 實例，以定義輸出影像的尺寸與品質。

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setPageHeight(500);
```

### 步驟 3：指定 CAD 圖層

加入您想要點陣化的圖層名稱。本例中，我們匯出預設圖層 `"0"`。

```java
List<String> stringList = new ArrayList<>(Arrays.asList("0"));
rasterizationOptions.setLayers(stringList);
```

### 步驟 4：設定 JPEG 選項

建立 `JpegOptions` 物件（或其他點陣影像選項），並將其與點陣化設定關聯。

```java
JpegOptions options = new JpegOptions();
options.setVectorRasterizationOptions(rasterizationOptions);
```

### 步驟 5：匯出為 JPEG

最後，將點陣化的圖層儲存為 JPEG 檔案。

```java
image.save(dataDir + "CADLayersToRasterImageFormats_out_.jpg", options);
```

對其他圖層重複上述步驟，或調整點陣化參數（解析度、背景顏色等），以符合您的特定需求。

## 常見問題與疑難排解

| 症狀 | 可能原因 | 解決方法 |
|---------|--------------|-----|
| 輸出空白影像 | 未指定圖層或圖層名稱錯誤 | 確認 CAD 檔案中存在該圖層名稱；使用 `image.getLayers()` 列出圖層。 |
| 解析度低 | 預設 DPI 較低 | 在儲存前設定 `rasterizationOptions.setResolution(300);`（或更高）。 |
| 不支援的 CAD 格式 | 使用較舊的 Aspose.CAD 版本 | 升級至最新的 Aspose.CAD for Java 版本。 |

## 常見問與答

**Q: 我可以將 Aspose.CAD for Java 與其他程式語言一起使用嗎？**  
A: Aspose.CAD 主要支援 Java，但亦提供 .NET、C++ 以及其他語言的版本。

**Q: 我可以在哪裡取得額外的支援或協助？**  
A: 如有任何問題或需要協助，請前往 [Aspose.CAD forum](https://forum.aspose.com/c/cad/19)。

**Q: 是否提供免費試用？**  
A: 有，您可從 [here](https://releases.aspose.com/) 取得 Aspose.CAD 的免費試用。

**Q: 我該如何取得 Aspose.CAD 的臨時授權？**  
A: 可從 [this link](https://purchase.aspose.com/temporary-license/) 取得臨時授權。

**Q: Aspose.CAD for Java 有特定的系統需求嗎？**  
A: 請確保您具備相容的 Java 開發環境；詳情請參考文件中的系統需求說明。

---

**最後更新：** 2026-04-13  
**測試環境：** Aspose.CAD for Java 24.12（撰寫時的最新版本）  
**作者：** Aspose

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}