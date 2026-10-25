---
date: 2026-10-25
description: 了解如何使用 Aspose.CAD for Java 將 DWG 轉換為 PNG 並將 CAD 儲存為 PNG，支援 DWG、DXF、DWF
  等 CAD 檔案，具備高效能光柵化功能。
keywords:
- convert dwg to png
- save cad as png
- cad to png conversion
- how to rasterize cad
- convert dwg raster image
lastmod: 2026-10-25
linktitle: 將 CAD 圖紙轉換為光柵圖像格式
og_description: 使用 Aspose.CAD for Java 快速將 DWG 轉換為 PNG。本指南說明如何將 CAD 儲存為 PNG、設定光柵選項，以及批次轉換——適用於網頁預覽與報告。
og_image_alt: 'Developer guide: convert DWG to PNG using Aspose.CAD Java API'
og_title: 如何使用 Aspose.CAD for Java 將 DWG 轉換為 PNG
schemas:
- author: Aspose
  dateModified: '2026-10-25'
  description: Learn how to convert DWG to PNG and save CAD as PNG using Aspose.CAD
    for Java, handling DWG, DXF, DWF and other CAD files with high‑performance rasterization.
  headline: How to convert DWG to PNG using Aspose.CAD for Java
  type: TechArticle
- description: Learn how to convert DWG to PNG and save CAD as PNG using Aspose.CAD
    for Java, handling DWG, DXF, DWF and other CAD files with high‑performance rasterization.
  name: How to convert DWG to PNG using Aspose.CAD for Java
  steps:
  - name: '**Java Development Kit** – JDK 8 or later installed and configured.'
    text: '**Java Development Kit** – JDK 8 or later installed and configured.'
  - name: '**Aspose.CAD for Java** – download the latest JAR from the official Aspose.CAD
      for Java releases page [ Aspose.CAD for Java download page ](https://releases.aspose.com/cad/java/).'
    text: '**Aspose.CAD for Java** – download the latest JAR from the official Aspose.CAD
      for Java releases page [ Aspose.CAD for Java download page ](https://releases.aspose.com/cad/java/).'
  - name: '**A DWG file** – any valid DWG, DXF or DWF drawing you want to rasterize.'
    text: '**A DWG file** – any valid DWG, DXF or DWF drawing you want to rasterize.'
  type: HowTo
- questions:
  - answer: Set the `backgroundColor` property on `CadRasterizationOptions` before
      creating the `PngOptions` instance.
    question: How do I convert a DWG file to PNG with a custom background color?
  - answer: Yes—wrap the loading, rasterization, and saving steps inside a loop that
      iterates over your file collection.
    question: Can I process multiple CAD files in one batch operation?
  - answer: The default DPI of 96 produces screen‑quality PNGs; raise the DPI to 300
      for high‑resolution print output.
    question: What image quality can I expect from the default settings?
  - answer: Absolutely. PNGs are saved with an alpha channel by default, and you can
      explicitly set a transparent background in the rasterization options.
    question: Does Aspose.CAD support transparent backgrounds in PNG output?
  - answer: Yes—replace `PngOptions` with `JpegOptions` or `BmpOptions` while reusing
      the same `CadRasterizationOptions`.
    question: Can I convert CAD files to other raster formats like JPEG or BMP?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- convert dwg
- Aspose.CAD
- Java CAD processing
- raster image conversion
title: 如何使用 Aspose.CAD for Java 將 DWG 轉換為 PNG
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何使用 Aspose.CAD for Java 將 DWG 轉換為 PNG

## 介紹

在本教學中，您將學習如何使用 Aspose.CAD for Java **將 DWG 轉換為 PNG**。將 CAD 圖紙轉換為 PNG 等光柵影像格式是常見需求，無論是要在網頁中嵌入圖紙、產生縮圖，或是放入 PDF 報告中。Aspose.CAD 提供純 Java 解決方案，能處理 DWG、DXF、DWF 以及超過 50 種其他 CAD 格式，且不需任何原生相依性，對於一般圖紙的轉換時間可在一秒內完成。

## 快速解答
- **什麼函式庫負責轉換？** Aspose.CAD for Java。  
- **我可以將 DWG 轉換為 PNG 嗎？** 可以 — 相同的 API 可用於 DWG、DXF、DWF 以及許多其他格式。  
- **生產環境需要授權嗎？** 非評估用途必須使用商業授權。  
- **光柵尺寸可否自訂？** 當然可以 — 您可以透過光柵化選項設定頁面寬度、高度、DPI 與背景顏色。  
- **轉換需要多長時間？** 標準圖紙通常在一秒內完成；較大的多頁檔案可能需要幾秒鐘。

## 如何使用 Aspose.CAD 將 DWG 轉換為 PNG

載入 CAD 檔案、設定光柵化選項、建立 PNG 專屬選項，最後儲存光柵影像。此端對端流程將向量式 DWG 資料轉換為像素式 PNG，同時保留線條粗細、圖層與顏色。

## 為何使用 Aspose.CAD for Java？

Aspose.CAD 支援 **50+** 種輸入與輸出格式，包括 DWG、DXF、DWF、SVG 以及 PNG、JPEG、BMP 等光柵格式。它可處理高達 **500 MB** 的檔案而無需將整個文件載入記憶體，非常適合批次流水線。此函式庫可在任何 Java 8+ 執行環境上執行，無需外部 DLL，且提供對解析度、背景顏色與渲染品質的細緻控制，僅需幾行程式碼即可完成。

## 前置條件

在開始之前，請確保您已具備：

1. **Java Development Kit** – 已安裝並設定 JDK 8 或更新版本。  
2. **Aspose.CAD for Java** – 從官方 Aspose.CAD for Java 釋出頁面下載最新的 JAR [ Aspose.CAD for Java download page ](https://releases.aspose.com/cad/java/)。  
3. **DWG 檔案** – 任意有效的 DWG、DXF 或 DWF 圖紙，您想要光柵化的檔案。  

將 Aspose.CAD JAR 加入專案的 classpath（Maven、Gradle 或手動加入）。

## 匯入命名空間

`com.aspose.cad` 套件包含載入、光柵化與儲存 CAD 圖紙所需的所有類別。

`Image` 類別是 Aspose.CAD 用於將任何支援的 CAD 檔案載入記憶體的入口點。  
`CadRasterizationOptions` 類別讓您定義向量資料如何轉換為像素（尺寸、DPI、背景等）。  
`PngOptions` 類別則指定 PNG 專屬的輸出設定，例如壓縮等級與透明度處理。

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

現在，讓我們將將 CAD 圖紙轉換為光柵影像的過程細分為以下步驟：

## 步驟 1：載入 CAD 圖紙

`Image.load()` 方法讀取來源檔案，並建立可供稍後光柵化的記憶體表示。

```java
String dataDir = "Your Document Directory" + "CADConversion/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

## 步驟 2：設定光柵化選項

建立 `CadRasterizationOptions` 實例，並設定頁面寬度、高度、DPI 與背景顏色。這些設定決定最終 PNG 的品質與尺寸。

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1200);
rasterizationOptions.setPageHeight(1200);
```

## 步驟 3：建立影像選項

實例化 `PngOptions`，並將先前設定好的光柵化選項指派給它。這樣即可將向量轉光柵的參數與 PNG 輸出格式關聯起來。

```java
ImageOptionsBase options = new PngOptions();
options.setVectorRasterizationOptions(rasterizationOptions);
```

## 步驟 4：儲存光柵影像

使用 `PngOptions` 實例與目標檔案路徑呼叫 `image.save()`。此方法將光柵化的 PNG 寫入磁碟，完成轉換。

```java
image.save(dataDir + "conic_pyramid_raster_image_out.png", options);
```

對每個需要處理的 CAD 檔案重複上述步驟，即可建立可靠的 **cad to png conversion** 流程。

## 常見使用情境與技巧

- **網頁預覽產生** – 將大型 DWG 檔案轉換為輕量級 PNG 縮圖，即時在瀏覽器中顯示。  
- **報告嵌入** – 在 PDF 或 Word 報告中使用 PNG 輸出，因為原生 CAD 格式不受支援。  
- **批次轉換** – 迭代資料夾中的 CAD 檔案，套用相同的光柵化設定以取得一致結果。  
- **專業提示：** 將 `rasterizationOptions.setResolution()` 提升至 300 DPI 以產生列印品質的影像；預設的 96 DPI 最適合螢幕顯示。  
- **如何將 DWG 轉換為其他格式** – 將 `PngOptions` 替換為 `JpegOptions` 或 `BmpOptions`，同時保留相同的光柵化設定。

## 結論

依照上述步驟操作，即可有效 **將 DWG 轉換為 PNG**、**將 CAD 儲存為 PNG**，或執行應用程式所需的任何 **cad to png conversion**。Aspose.CAD for Java 讓您完整掌控解析度、背景顏色與輸出格式，是網頁預覽、文件流水線以及大規模批次處理的首選解決方案。

## 常見問題

**Q: 如何使用自訂背景顏色將 DWG 檔案轉換為 PNG？**  
A: 在建立 `PngOptions` 實例之前，於 `CadRasterizationOptions` 設定 `backgroundColor` 屬性。

**Q: 我可以在一次批次操作中處理多個 CAD 檔案嗎？**  
A: 可以 — 將載入、光柵化與儲存步驟包在迴圈中，對您的檔案集合逐一處理。

**Q: 預設設定下的影像品質如何？**  
A: 預設 96 DPI 可產生螢幕品質的 PNG；若需高解析度列印輸出，請將 DPI 提升至 300。

**Q: Aspose.CAD 是否支援 PNG 輸出的透明背景？**  
A: 當然支援。PNG 預設以 alpha 通道儲存，您亦可在光柵化選項中明確設定透明背景。

**Q: 我可以將 CAD 檔案轉換為其他光柵格式，如 JPEG 或 BMP 嗎？**  
A: 可以 — 將 `PngOptions` 替換為 `JpegOptions` 或 `BmpOptions`，同時重用相同的 `CadRasterizationOptions`。

**Last Updated:** 2026-10-25  
**Tested With:** Aspose.CAD for Java 24.12 (latest)  
**Author:** Aspose

## 相關教學

- [自動調整 CAD 圖紙尺寸並使用 Aspose.CAD for Java 將 DWG 轉換為 BMP](/cad/java/cad-file-manipulation/auto-adjusting-cad-drawing-size/)
- [使用 Aspose.CAD 在 Java 中將 DWG 儲存為支援圖層的 JPEG](/cad/java/advanced-cad-features/support-of-layers-in-cad/)
- [將 CAD 儲存為 PNG – 使用 Aspose.CAD for Java 匯出 OLE 物件](/cad/java/cad-to-pdf-and-svg-export-options/export-ole-objects-from-cad/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}