---
date: 2026-05-25
description: 了解如何使用 Aspose.CAD for Java 將 dgn 檔案匯出為 JPEG 圖像。本分步指南將向您展示如何高效地將 dgn 轉換為
  jpeg。
keywords:
- how to export dgn
- convert dgn to jpeg
- java convert cad to image
linktitle: 將 AutoCAD 格式的 DGN 匯出為點陣圖像格式
schemas:
- author: Aspose
  dateModified: '2026-05-25'
  description: Learn how to export dgn files to JPEG images with Aspose.CAD for Java.
    This step‑by‑step guide shows you how to convert dgn to jpeg efficiently.
  headline: How to Export DGN to JPEG with Aspose.CAD for Java
  type: TechArticle
- description: Learn how to export dgn files to JPEG images with Aspose.CAD for Java.
    This step‑by‑step guide shows you how to convert dgn to jpeg efficiently.
  name: How to Export DGN to JPEG with Aspose.CAD for Java
  steps:
  - name: '**Aspose.CAD Library** – download the latest JAR from the official site [here](https://releases.aspose.com/cad/java/).
      You can also explore other product releases [here](https://releases.aspose.com/).'
    text: '**Aspose.CAD Library** – download the latest JAR from the official site [here](https://releases.aspose.com/cad/java/).
      You can also explore other product releases [here](https://releases.aspose.com/).'
  - name: '**Java Development Kit (JDK)** – Java 8 or newer installed on your machine.'
    text: '**Java Development Kit (JDK)** – Java 8 or newer installed on your machine.'
  - name: '**IDE** – IntelliJ IDEA, Eclipse, or any Java‑compatible editor you prefer.'
    text: '**IDE** – IntelliJ IDEA, Eclipse, or any Java‑compatible editor you prefer.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD supports over 30 vector formats, including DWG, DXF, DWF,
      and SVG, enabling a single API for many conversion scenarios.
    question: Can I use Aspose.CAD for Java with other CAD file formats?
  - answer: Yes, you can access a free trial [here](https://releases.aspose.com/).
    question: Is there a free trial available for Aspose.CAD for Java?
  - answer: Refer to the official docs [here](https://reference.aspose.com/cad/java/).
    question: Where can I find documentation for Aspose.CAD for Java?
  - answer: Visit the support forum [here](https://forum.aspose.com/c/cad/19).
    question: How can I get support for Aspose.CAD for Java?
  - answer: You can buy a license [here](https://purchase.aspose.com/buy).
    question: Where can I purchase a license for Aspose.CAD for Java?
  type: FAQPage
second_title: Aspose.CAD Java API
title: 如何使用 Aspose.CAD for Java 將 DGN 匯出為 JPEG
url: /zh-hant/java/dgn-export-options/exporting-dgn-to-raster-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java DGN 轉 JPEG 教學（使用 Aspose.CAD）

## 介紹

在本完整指南中，您將了解如何使用 Aspose.CAD for Java 將 **how to export dgn** 檔案匯出為 JPEG 圖像。無論您是建立批次處理服務，或是為 CAD 檢視器加入即時預覽產生功能，本教學都會一步步帶您完成，從載入來源檔案到儲存點陣輸出。您亦會看到實用技巧，讓程式碼保持乾淨且效能良好。

## 快速解答
- **需要哪個函式庫？** Aspose.CAD for Java（下載 [here](https://releases.aspose.com/cad/java/)）。
- **我可以一行程式碼將 DGN 轉換為 JPEG 嗎？** 可以 – 使用 `CadImage.load` 載入，然後以 `JpegOptions` 呼叫 `save`。
- **正式環境需要授權嗎？** 需要，商業授權會移除評估水印。
- **支援哪個 Java 版本？** 完全支援 Java 8 至 17。
- **我能處理多大的 DGN 檔案？** 可處理高達 2 GB 的檔案，且不需將整個檔案載入記憶體。

## 什麼是「how to export dgn」？
*「How to export dgn」* 指的是將 MicroStation DGN 設計檔轉換為其他格式的過程，通常是 JPEG 等點陣圖像，以便更容易檢視或分享。此轉換讓沒有 CAD 軟體的相關人員也能檢查設計、在文件中嵌入影像，或為網站畫廊產生縮圖，提升可存取性與團隊協作。

## 為何使用 Aspose.CAD for Java？
Aspose.CAD 支援 **30+ CAD 格式**（包括 DGN、DWG、DXF），且可在不需原始 CAD 應用程式的情況下渲染 **高達 2 GB** 的檔案。其點陣引擎在一般伺服器硬體上可以 **> 50 fps** 處理多頁圖紙，僅透過一次 API 呼叫即可產生高品質 JPEG 輸出。

## 前置條件

1. **Aspose.CAD 函式庫** – 從官方網站下載最新的 JAR [here](https://releases.aspose.com/cad/java/)。您亦可在此處 [here](https://releases.aspose.com/) 探索其他產品發行版。  
2. **Java Development Kit (JDK)** – 在您的機器上安裝 Java 8 或更新版本。  
3. **IDE** – 您偏好的 IntelliJ IDEA、Eclipse，或任何相容 Java 的編輯器。

## 匯入套件

在您的 Java 專案中，匯入必要的 Aspose.CAD 類別：

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
```

## 如何使用 Aspose.CAD 在 Java 中將 dgn 匯出為 JPEG？

`CadImage` 類別代表已載入記憶體的 CAD 文件，提供渲染與儲存的方法。

使用 `CadImage.load("source.dgn")` 載入 DGN 檔案，設定 `JpegOptions`（包括品質與解析度），再設定適當的 `RasterizationOptions` 如頁面尺寸與背景顏色，最後呼叫 `image.save("output.jpg", jpegOptions)`。此三步流程處理向量轉點陣的轉換，保留線寬，並在一般圖紙下於一秒內寫入高品質 JPEG 檔案。

## 步驟 1：載入 DGN 檔案

`CadImage` 類別代表已載入記憶體的 CAD 文件。

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
DgnImage dgnImage = (DgnImage) Image.load(dataDir + "Nikon_D90_Camera.dgn");
```

## 步驟 2：建立 JpegOptions 物件

`JpegOptions` 定義 JPEG 輸出的特定設定，例如壓縮品質與解析度。

```java
ImageOptionsBase options = new JpegOptions();
```

## 步驟 3：指定 Rasterization Options

`RasterizationOptions` 決定向量圖形的點陣化方式，包括頁面大小、DPI、背景顏色與抗鋸齒。

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(600);
vectorOptions.setPageHeight(400);
vectorOptions.setNoScaling(true);
vectorOptions.setAutomaticLayoutsScaling(false);
options.setVectorRasterizationOptions(vectorOptions);
```

## 步驟 4：儲存轉換後的影像

呼叫 `save` 會使用您提供的選項將點陣圖寫入磁碟。

```java
OutputStream outStream = new FileOutputStream(dataDir + "ExportDGNToRasterImage_Out.jpg");
dgnImage.save(outStream, options);
```

### 常見使用情境

- **Web 預覽產生** – 將工程圖轉換為輕量級 JPEG 縮圖，以便在瀏覽器中快速顯示。  
- **批次存檔** – 自動將數千個 DGN 檔案轉換為 JPEG，以便長期保存，且不需 MicroStation。  
- **報告產生** – 從 Java 程式碼直接將 CAD 快照嵌入 PDF 或 HTML 報告中。

### 常見問題與解決方案

| 問題 | 解決方案 |
|-------|----------|
| **影像顯示空白** | 確保 `RasterizationOptions.setPageWidth/Height` 與圖紙範圍相符，並設定非透明的背景。 |
| **輸出品質低** | 將 `JpegOptions.setQuality(100)` 提高，並設定更高的 DPI（例如 `RasterizationOptions.setResolution(300)`）。 |
| **記憶體不足錯誤** | 使用 `CadImage.load` 搭配 `loadOptions.setLoadMode(LoadMode.Memory)` 以串流方式處理大型檔案。 |

## 常見問與答

**Q: 我可以在 Java 中使用 Aspose.CAD 處理其他 CAD 檔案格式嗎？**  
A: 可以，Aspose.CAD 支援超過 30 種向量格式，包括 DWG、DXF、DWF 與 SVG，讓單一 API 可應對多種轉換情境。

**Q: 是否提供 Aspose.CAD for Java 的免費試用？**  
A: 有，您可在此取得免費試用 [here](https://releases.aspose.com/).

**Q: 在哪裡可以找到 Aspose.CAD for Java 的文件？**  
A: 請參考官方文件 [here](https://reference.aspose.com/cad/java/).

**Q: 如何取得 Aspose.CAD for Java 的支援？**  
A: 前往支援論壇 [here](https://forum.aspose.com/c/cad/19)。

**Q: 在哪裡可以購買 Aspose.CAD for Java 的授權？**  
A: 您可在此購買授權 [here](https://purchase.aspose.com/buy)。

**最後更新：** 2026-05-25  
**測試環境：** Aspose.CAD 24.11 for Java  
**作者：** Aspose

## 相關教學

- [輕鬆將 DGN 匯出為 AutoCAD PDF（使用 Aspose.CAD for Java）](/cad/java/dgn-export-options/exporting-dgn-to-pdf/)
- [使用 Aspose.CAD for Java 匯出 DGN 為 DWG – 教學](/cad/java/dgn-export-options/)
- [將 CAD 儲存為 PNG – 使用 Aspose.CAD for Java 轉換 CAD 圖紙為點陣圖格式](/cad/java/cad-drawing-conversion/convert-cad-drawing-to-raster-image/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}