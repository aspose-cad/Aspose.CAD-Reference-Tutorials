---
date: 2026-10-04
description: 了解如何使用 Aspose.CAD for Java 快速將 DWG 轉換為 PNG，並將 CAD 匯出為 PNG 或其他點陣格式。快速獲得高品質結果。
keywords:
- convert dwg to png
- dwg to raster image
- convert cad to pdf
- export cad as png
- convert dwg to jpeg
lastmod: 2026-10-04
linktitle: 將 CAD 版面轉換為點陣圖像格式
og_description: 使用 Aspose.CAD for Java 快速將 DWG 轉換為 PNG。了解一步一步的操作方法，將 CAD 匯出為 PNG、JPEG、TIFF
  等格式。
og_image_alt: 'Developer guide: Convert DWG to PNG and other raster formats using
  Aspose.CAD for Java'
og_title: 使用 Aspose.CAD for Java 將 DWG 轉換為 PNG 及其他點陣格式
schemas:
- author: Aspose
  dateModified: '2026-10-04'
  description: Learn how to quickly convert dwg to png and export cad as png or other
    raster formats using Aspose.CAD for Java. Get high‑quality results fast.
  headline: Convert DWG to PNG and other raster formats using Aspose.CAD for Java
  type: TechArticle
- description: Learn how to quickly convert dwg to png and export cad as png or other
    raster formats using Aspose.CAD for Java. Get high‑quality results fast.
  name: Convert DWG to PNG and other raster formats using Aspose.CAD for Java
  steps:
  - name: set up the resource directory
    text: Replace `"Your Document Directory"` with the absolute path where your CAD
      files reside. This directory will be used for both input and output files.
  - name: load the CAD file
    text: '`Image.load` parses the source file and creates an in‑memory representation
      that you can rasterize. You can load any supported format (DWG, DXF, DGN, etc.)
      – this is the **how to convert cad** part.'
  - name: configure rasterization options
    text: '`CadRasterizationOptions` defines how the vector data is turned into pixels.
      `setPageWidth` and `setPageHeight` control output resolution (larger values
      = higher DPI). `setLayouts` lets you **convert CAD to raster** for specific
      layouts; omit it to rasterize the whole drawing.'
  - name: set image options
    text: '`TiffOptions` (or `PngOptions` for PNG) tells Aspose which raster format
      to generate and lets you fine‑tune compression, color depth, and other format‑specific
      settings. Choose the options class that matches your desired output.'
  - name: save the resultant image
    text: Call `save` on the `Image` instance, passing the output file name and the
      options object. Change the file extension to `.png` (and use `PngOptions`) to
      **save CAD as PNG**. The same pattern works for JPEG, BMP, or PDF. > **Common
      pitfall:** Forgetting to match the file extension with the options cla
  type: HowTo
- questions:
  - answer: Yes, it supports over 30 CAD and raster formats, including DWG, DXF, DGN,
      and SVG.
    question: Is Aspose.CAD compatible with different CAD file formats?
  - answer: Absolutely. Adjust `setPageWidth`, `setPageHeight`, or `setResolution`
      in `CadRasterizationOptions` to achieve the desired DPI.
    question: Can I customize the resolution of the output raster image?
  - answer: Provide an array with all layout names to `setLayouts`, e.g., `new String[]{"Model","Layout1","Layout2"}`.
    question: How can I convert multiple CAD layouts in a single run?
  - answer: Yes—PNG, JPEG, BMP, PDF, and more are available via their respective `*Options`
      classes.
    question: Are there output formats besides TIFF supported?
  - answer: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for community
      support and official assistance.
    question: Where can I get help or share my experience with Aspose.CAD?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- convert dwg
- Aspose.CAD
- Java raster conversion
- CAD image processing
title: 使用 Aspose.CAD for Java 將 DWG 轉換為 PNG 及其他點陣格式
url: /zh-hant/java/cad-drawing-conversion/convert-cad-layout-to-raster-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.CAD for Java 將 DWG 轉換為 PNG 及其他點陣格式

## 簡介

`Aspose.CAD for Java` 是一個函式庫，可程式化地將 CAD 檔案轉換為點陣圖像，例如 PNG、JPEG 和 TIFF。將 DWG 轉換為 PNG（或其他點陣圖像格式）是常見需求，當您需要與沒有 CAD 檢視器的同事分享圖紙、在文件中嵌入設計，或為網站相簿產生縮圖時，都會用到此功能。在本指南中，您將學會如何快速且可靠地將 dwg 轉換為 png，無論是處理完整圖紙檔案或僅針對特定版面。您也可能需要 **將 CAD 轉換為點陣圖** 以供網頁預覽、報表工具或行動應用程式使用。

## 快速答覆
- **哪個函式庫負責 DWG 轉 PNG？** Aspose.CAD for Java 提供轉換引擎。  
- **可以匯出哪些點陣格式？** PNG、JPEG、TIFF、PDF、BMP，以及超過 30 種其他格式。  
- **測試需要授權嗎？** 開發階段可使用免費試用版；正式上線需購買商業授權。  
- **可以選擇特定版面嗎？** 可以 – 使用 `setLayouts` 針對 “Model”、 “Layout1” 等版面。  
- **是否支援高解析度輸出？** 當然可以 – 調整 `setPageWidth`、`setPageHeight`（或 `setResolution`）即可控制 DPI。

## 什麼是「convert dwg to png」？

Convert dwg to png 指的是將 DWG 向量圖形轉換為像素為基礎的 PNG 圖像，讓任何標準圖像檢視器都能顯示。此過程會將向量實體光柵化，保留線寬、顏色與圖層，同時轉換成固定解析度的點陣圖。產生的圖像非常適合嵌入 PDF、Word 文件或網頁中，因為向量支援有限。

## 為何要將 CAD 匯出為 PNG（或其他點陣格式）？

將 CAD 匯出為 PNG 可提供通用相容性、快速載入以及在所有主流平台上輕鬆嵌入。相較於開啟龐大的 DWG 檔案，點陣圖可即時載入，而 PNG 的無損壓縮則確保視覺忠實度。透過控制解析度、背景顏色與版面，您能保證每位利害關係人看到的外觀一致，無論是在桌面、行動裝置或瀏覽器中。

## 常見使用情境

| 情境 | 為何點陣輸出有幫助 |
|----------|------------------------|
| **專案文件** | 在 PDF 或 Word 文件中嵌入 PNG，可免除審閱者安裝 CAD 軟體的需求。 |
| **網站入口** | 從 DWG 產生的縮圖可即時載入，提升使用者體驗。 |
| **行動應用程式** | 點陣圖在缺乏 CAD 檢視器的裝置上亦能正確顯示。 |
| **自動化報表** | 批次將多個版面轉為 PNG/JPEG，方便嵌入圖表或儀表板。 |

## 前置條件

開始之前，請確保您已具備：

1. **Java 開發環境** – 已安裝並設定 JDK 8 或更新版本。  
2. **Aspose.CAD for Java** – 從 [Aspose.CAD for Java 文件](https://reference.aspose.com/cad/java/) 下載最新 JAR。

## 匯入命名空間

`com.aspose.cad.Image` 是代表任何 CAD 檔案於記憶體中的核心類別。`com.aspose.cad.imageoptions.*` 提供每種點陣格式的選項物件。匯入您需要的類別，以載入圖紙、設定光柵化參數，並儲存輸出。

> **專業提示：** 若您打算 **將 CAD 匯出為 PNG** 而非 TIFF，請將 `TiffOptions` 換成 `PngOptions`（位於 `com.aspose.cad.imageoptions.PngOptions`）。

## 步驟說明

### 步驟 1：設定資源目錄

將 `"Your Document Directory"` 替換為 CAD 檔案所在的絕對路徑。此目錄同時用於輸入與輸出檔案。

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

### 步驟 2：載入 CAD 檔案

`Image.load` 會解析來源檔案，並建立可供光柵化的記憶體表示。您可以載入任何支援的格式（DWG、DXF、DGN 等）——這就是 **如何將 cad 轉換** 的部分。

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";
```

### 步驟 3：設定光柵化選項

`CadRasterizationOptions` 定義向量資料如何轉為像素。`setPageWidth` 與 `setPageHeight` 控制輸出解析度（數值越大 DPI 越高）。`setLayouts` 讓您 **將 CAD 轉換為點陣圖** 針對特定版面；若不設定，則會光柵化整個圖紙。

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

### 步驟 4：設定影像選項

`TiffOptions`（或 PNG 時的 `PngOptions`）告訴 Aspose 要產生哪種點陣格式，並讓您微調壓縮、色深等格式專屬設定。選擇與目標輸出相符的 Options 類別即可。

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1200);
rasterizationOptions.setPageHeight(1200);
rasterizationOptions.setLayouts(new String[] {"Model", "Layout1"});
```

### 步驟 5：儲存產生的影像

對 `Image` 物件呼叫 `save`，傳入輸出檔名與選項物件。將副檔名改為 `.png`（同時使用 `PngOptions`）即可 **將 CAD 儲存為 PNG**。相同模式亦適用於 JPEG、BMP 或 PDF。

```java
ImageOptionsBase options = new TiffOptions(TiffExpectedFormat.Default);
options.setVectorRasterizationOptions(rasterizationOptions);
```

> **常見陷阱：** 若檔案副檔名與 Options 類別不匹配，會拋出 `UnsupportedFormatException`。務必保持一致。

## 常見問題與解決方案

| 問題 | 解決方式 |
|-------|----------|
| **輸出影像為空白** | 確認 `setLayouts` 中的版面名稱與原始 CAD 檔案完全相符。 |
| **PNG 解析度過低** | 增加 `setPageWidth` / `setPageHeight`，或在光柵化選項上設定 `setResolution`。 |
| **不支援的 DWG 版本** | 確認使用最新的 Aspose.CAD 版本；舊版可能無法處理較新的 DWG。 |
| **大型檔案記憶體錯誤** | 逐頁處理或增加 JVM 堆疊大小（`-Xmx2g`）。 |

## 常見問答

**Q: Aspose.CAD 是否相容於不同的 CAD 檔案格式？**  
A: 是的，支援超過 30 種 CAD 與點陣格式，包括 DWG、DXF、DGN 與 SVG。

**Q: 我可以自訂輸出點陣圖的解析度嗎？**  
A: 當然可以。調整 `CadRasterizationOptions` 的 `setPageWidth`、`setPageHeight` 或 `setResolution` 即可達到所需 DPI。

**Q: 如何在一次執行中轉換多個 CAD 版面？**  
A: 將所有版面名稱組成陣列傳給 `setLayouts`，例如 `new String[]{"Model","Layout1","Layout2"}`。

**Q: 除了 TIFF，還有其他支援的輸出格式嗎？**  
A: 有——PNG、JPEG、BMP、PDF 等皆可透過對應的 `*Options` 類別使用。

**Q: 我可以在哪裡取得支援或分享使用心得？**  
A: 前往 [Aspose.CAD 論壇](https://forum.aspose.com/c/cad/19) 取得社群支援與官方協助。

## 結論

依照上述步驟，您即可 **將 DWG 轉換為 PNG**、**將 CAD 匯出為 PNG**、**將 CAD 儲存為 JPEG**，或產生任何其他點陣格式。Aspose.CAD for Java 負責繁重的轉換工作，讓您專注於將高品質影像整合至應用程式、文件或網站。此函式庫支援 30+ 格式，且能在不將整個檔案載入記憶體的情況下渲染上百頁圖紙，是企業級 CAD 點陣化的可靠選擇。

---

**最後更新：** 2026-10-04  
**測試環境：** Aspose.CAD for Java 24.12  
**作者：** Aspose  







```java
image.save(dataDir + "conic_pyramid_layoutstorasterimage_out_.tiff", options);
```

```bash
java -jar aspose-cad.jar -i input.dwg -o output.png -w 1200 -h 1200
```

## 相關教學

- [快速使用 java cad 函式庫 Aspose.CAD for Java 匯出 DWG 為 PDF 或點陣圖](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [使用 Aspose.CAD for Java 將 DWG 轉換為 BMP](/cad/java/cad-export-options/export-to-bmp/)
- [匯出 DWG 為 PDF：指定版面使用 Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}