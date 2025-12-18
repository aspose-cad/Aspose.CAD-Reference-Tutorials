---
date: 2025-12-18
description: 學習如何執行 Aspose CAD Java 教學，輕鬆將 CAD 圖層轉換為點陣圖像。跟隨我們的逐步指南，實現無縫的文件可視化。
linktitle: Convert CAD Layer to Raster Image Format
second_title: Aspose.CAD Java API
title: Aspose CAD Java 教學 – 將 CAD 圖層轉換為點陣圖像格式
url: /zh-hant/java/cad-drawing-conversion/convert-cad-layer-to-raster-image/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose CAD Java 教學：將 CAD 圖層轉換為點陣圖格式

## 簡介

在電腦輔助設計（CAD）的領域中，將單一 CAD 圖層轉換為點陣圖格式對於輕鬆分享、列印或進一步的影像處理相當重要。本 **aspose cad java tutorial** 將示範如何利用 **Aspose.CAD for Java** 取出特定圖層並儲存為 JPEG（或其他任何點陣圖格式）。閱讀完本指南後，您將了解為何圖層級別的轉換很重要、如何設定點陣化選項，以及如何僅用幾行程式碼匯出結果。

## 快速答案
- **本教學涵蓋什麼內容？** 使用 Aspose.CAD for Java 將選取的 CAD 圖層轉換為點陣圖。  
- **支援哪些格式？** 任何 Aspose 支援的點陣圖格式（JPEG、PNG、BMP 等）。  
- **需要授權嗎？** 開發階段可使用免費試用版；正式上線需購買授權。  
- **先決條件是什麼？** Java 開發環境與 Aspose.CAD Java 函式庫。  
- **實作需要多久？** 基本轉換大約 10–15 分鐘即可完成。

## 先決條件

在開始撰寫程式碼之前，請確保您已具備以下條件：

- **Java 開發環境** – 已安裝並設定 JDK 8 或以上版本。  
- **Aspose.CAD 函式庫** – 從 [download link](https://releases.aspose.com/cad/java/) 下載並安裝 Aspose.CAD for Java。

## 匯入命名空間

在此步驟中，我們將匯入處理 CAD 檔案所需的類別。

### 匯入 Aspose.CAD 類別

在您的 Java 原始檔案中加入必要的 Aspose.CAD 匯入語句：

```java
import com.aspose.cad.Image;


import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import java.util.ArrayList;
import java.util.Arrays;
import java.util.List;
```

## 將 CAD 圖層轉換為點陣圖格式

以下為完整的逐步流程。每個步驟都以簡明文字說明，讓您清楚了解每一步的作用。

### 步驟 1：設定 CAD 檔案

首先，指定 CAD 檔案的路徑並將其載入 `Image` 物件。

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

加入您想要點陣化的圖層名稱。本例中我們匯出預設圖層 `"0"`。

```java
List<String> stringList = new ArrayList<>(Arrays.asList("0"));
rasterizationOptions.setLayers(stringList);
```

### 步驟 4：設定 JPEG 選項

建立 `JpegOptions` 物件（或其他點陣圖選項），並將其與點陣化設定關聯。

```java
JpegOptions options = new JpegOptions();
options.setVectorRasterizationOptions(rasterizationOptions);
```

### 步驟 5：匯出為 JPEG

最後，將點陣化後的圖層儲存為 JPEG 檔案。

```java
image.save(dataDir + "CADLayersToRasterImageFormats_out_.jpg", options);
```

如需處理其他圖層，只需重複上述步驟或調整點陣化參數（解析度、背景色等），以符合您的特定需求。

## 為什麼使用此方法？

- **選擇性匯出** – 只渲染所需圖層，減少檔案大小與處理時間。  
- **格式彈性** – 可將 `JpegOptions` 換成 `PngOptions`、`BmpOptions` 等，核心程式碼不需變更。  
- **高品質渲染** – Aspose.CAD 能完整保留線寬、顏色與文字，與原始 CAD 檔案一致。

## 常見問題與疑難排解

| 症狀 | 可能原因 | 解決方式 |
|---------|--------------|-----|
| 輸出影像為空白 | 未指定圖層或圖層名稱錯誤 | 確認圖層名稱在 CAD 檔案中存在；可使用 `image.getLayers()` 列出圖層。 |
| 解析度低 | 預設 DPI 較低 | 在儲存前設定 `rasterizationOptions.setResolution(300);`（或更高）。 |
| 不支援的 CAD 格式 | 使用較舊的 Aspose.CAD 版本 | 更新至最新的 Aspose.CAD for Java 版本。 |

## 常見問答

**Q: 我可以在其他程式語言中使用 Aspose.CAD for Java 嗎？**  
A: Aspose.CAD 主要支援 Java，但亦提供 .NET、C++ 及其他語言的版本。

**Q: 我可以在哪裡取得更多支援或協助？**  
A: 如有任何問題或需要協助，請前往 [Aspose.CAD forum](https://forum.aspose.com/c/cad/19)。

**Q: 是否提供免費試用？**  
A: 有的，您可從 [here](https://releases.aspose.com/) 取得免費試用版。

**Q: 如何取得 Aspose.CAD 的臨時授權？**  
A: 請從 [this link](https://purchase.aspose.com/temporary-license/) 取得臨時授權。

**Q: Aspose.CAD for Java 有特定的系統需求嗎？**  
A: 請確保您擁有相容的 Java 開發環境；詳細需求請參考官方文件。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**最後更新：** 2025-12-18  
**測試環境：** Aspose.CAD for Java 24.12（撰寫時的最新版本）  
**作者：** Aspose