---
date: 2026-02-17
description: 學習如何使用 Aspose.CAD for Java 將 dwg 轉換為 png，並將 cad 匯出為 png 或其他點陣圖格式。快速獲得高品質結果。
linktitle: Convert CAD Layout to Raster Image Format
second_title: Aspose.CAD Java API
title: 使用 Aspose.CAD for Java 將 DWG 轉換為 PNG 及其他點陣圖格式
url: /zh-hant/java/cad-drawing-conversion/convert-cad-layout-to-raster-image/
weight: 12
---

 heading.

We'll translate.

Now produce final answer.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.CAD for Java 將 DWG 轉換為 PNG 及其他點陣格式

## 介紹

將 DWG 轉換為 PNG（或其他點陣圖像格式）是當您需要與沒有 CAD 檢視器的同事分享 CAD 圖紙、在文件中嵌入設計，或為網站相簿產生縮圖時的常見需求。**在本指南中，您將學會快速且可靠地將 dwg 轉換為 png**，無論是處理完整圖紙檔案或僅針對特定版面。您也可能需要**將 CAD 轉換為點陣圖**以供網頁預覽、報表工具或行動應用程式使用。Aspose.CAD for Java 讓此轉換變得簡單，且提供對解析度、版面選擇與輸出格式的完整控制。

## 快速答覆
- **哪個函式庫負責 DWG 轉 PNG？** Aspose.CAD for Java  
- **可以匯出哪些格式？** PNG、JPEG、TIFF、PDF、BMP 等更多  
- **測試需要授權嗎？** 開發階段可使用免費試用版；正式環境需購買授權  
- **可以選擇特定版面嗎？** 可以，使用 `setLayouts` 目標 “Model”、 “Layout1” 等  
- **能產生高解析度輸出嗎？** 當然可以——調整 `setPageWidth` 與 `setPageHeight` 以控制 DPI  

## 什麼是「convert dwg to png」？

「convert dwg to png」指的是將向量式 DWG 檔案（許多 CAD 應用程式的原生格式）光柵化為像素式 PNG 圖像的過程。點陣圖非常適合於網頁顯示、電子郵件分享以及整合到非 CAD 軟體中。

## 為什麼要將 CAD 匯出為 PNG（或其他點陣格式）？

- **通用相容性：** PNG 與 JPEG 幾乎被所有圖像檢視器與瀏覽器支援。  
- **載入快速：** 相較於開啟龐大的 DWG 檔，點陣圖可即時載入。  
- **易於嵌入：** 可直接將 PNG 插入 Word、PowerPoint 或 HTML，無需額外外掛。  
- **外觀一致：** 您可自行控制解析度、背景與版面，確保每位利害關係人看到相同的視覺效果。  

## 常見使用情境

| 情境 | 點陣輸出帶來的好處 |
|----------|------------------------|
| **專案文件** | 在 PDF 或 Word 文件中嵌入 PNG，可免除審閱者安裝 CAD 軟體的需求。 |
| **網站入口** | 從 DWG 產生的縮圖可即時載入，提升使用者體驗。 |
| **行動應用程式** | 點陣圖能在缺乏 CAD 檢視器的裝置上正確顯示。 |
| **自動化報表** | 批次將多個版面轉為 PNG/JPEG，以便插入圖表或儀表板。 |

## 前置條件

開始之前，請確保您已具備：

1. **Java 開發環境** – 已安裝並設定 JDK 8 或更新版本。  
2. **Aspose.CAD for Java** – 從 [Aspose.CAD for Java 文件](https://reference.aspose.com/cad/java/) 下載最新 JAR。  

## 匯入命名空間

首先，匯入您需要的類別。這些匯入讓您可以存取圖像載入、光柵化選項以及 TIFF/PNG 輸出設定。

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

> **小技巧：** 若您打算**將 CAD 匯出為 PNG**而非 TIFF，只需將 `TiffOptions` 換成 `PngOptions`（位於 `com.aspose.cad.imageoptions.PngOptions`）。

## 步驟說明

### 步驟 1：設定資源目錄

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";
```

將 `"Your Document Directory"` 替換為 CAD 檔案所在的絕對路徑。

### 步驟 2：載入 CAD 檔案

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

您可以載入任何支援的格式（DWG、DXF、DGN 等）。這就是**如何將 cad 轉換**的部分——只要指向檔案，Aspose 便會負責解析。

### 步驟 3：設定光柵化選項

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1200);
rasterizationOptions.setPageHeight(1200);
rasterizationOptions.setLayouts(new String[] {"Model", "Layout1"});
```

- `setPageWidth` / `setPageHeight` 控制輸出解析度（數值越大 DPI 越高）。  
- `setLayouts` 讓您**將 CAD 轉為點陣圖**時只針對特定版面；若省略則光柵化整個圖紙。

### 步驟 4：設定圖像選項

```java
ImageOptionsBase options = new TiffOptions(TiffExpectedFormat.Default);
options.setVectorRasterizationOptions(rasterizationOptions);
```

若想輸出 PNG，請實例化 `PngOptions` 取代 `TiffOptions`。這裡就是**將 CAD 匯出為 PNG**的設定位置。

### 步驟 5：儲存結果圖像

```java
image.save(dataDir + "conic_pyramid_layoutstorasterimage_out_.tiff", options);
```

將檔案副檔名改為 `.png`（同時將 options 物件改為 `PngOptions`）即可**將 CAD 儲存為 JPEG/PNG**。

> **常見陷阱：** 若檔案副檔名與 options 類別不匹配，會拋出 `UnsupportedFormatException`。請務必保持一致。

## 常見問題與解決方案

| 問題 | 解決方案 |
|-------|----------|
| **輸出圖像為空白** | 確認 `setLayouts` 中的版面名稱與來源 CAD 檔案完全相同。 |
| **PNG 解析度過低** | 增加 `setPageWidth` / `setPageHeight`，或在光柵化選項上設定 `setResolution`。 |
| **不支援的 DWG 版本** | 確認使用最新的 Aspose.CAD 版本；舊版可能無法支援較新的 DWG 釋出。 |
| **大型檔案記憶體錯誤** | 逐頁處理或增加 JVM 堆積大小（`-Xmx2g`）。 |

## 常見問答

**Q: Aspose.CAD 是否相容不同的 CAD 檔案格式？**  
A: 是的，支援 DWG、DXF、DGN 等多種格式。

**Q: 我可以自訂輸出點陣圖的解析度嗎？**  
A: 當然可以。調整 `setPageWidth`、`setPageHeight` 或 `setResolution` 即可。

**Q: 如何在一次執行中轉換多個 CAD 版面？**  
A: 為 `setLayouts` 提供包含所有版面名稱的陣列，例如 `new String[]{"Model","Layout1","Layout2"}`。

**Q: 除了 TIFF，還有其他輸出格式嗎？**  
A: 有——PNG、JPEG、BMP、PDF 等皆可透過各自的 `*Options` 類別取得。

**Q: 我可以在哪裡取得協助或分享使用 Aspose.CAD 的經驗？**  
A: 前往 [Aspose.CAD 論壇](https://forum.aspose.com/c/cad/19) 取得社群支援與官方協助。

## 結論

依循上述步驟，您即可**將 DWG 轉換為 PNG**、**將 CAD 匯出為 PNG**、**將 CAD 儲存為 JPEG**，或產生任何其他所需的點陣格式。Aspose.CAD for Java 負責繁重的轉換工作，讓您專注於將高品質圖像整合至應用程式、文件或網站入口。

---

**最後更新：** 2026-02-17  
**測試環境：** Aspose.CAD for Java 24.12  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}