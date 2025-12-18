---
date: 2025-12-18
description: 了解如何使用 Aspose.CAD for Java 將 DWG 轉換為 PNG 以及其他點陣圖像格式。將 CAD 匯出為 PNG，獲得高品質的結果。
linktitle: Convert CAD Layout to Raster Image Format
second_title: Aspose.CAD Java API
title: 使用 Aspose.CAD for Java 將 DWG 轉換為 PNG 及其他光柵格式
url: /zh-hant/java/cad-drawing-conversion/convert-cad-layout-to-raster-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.CAD for Java 將 DWG 轉換為 PNG 及其他點陣格式

## 簡介

將 DWG 轉換為 PNG（或其他點陣影像格式）是常見需求，尤其在需要與沒有 CAD 檢視器的同事共享圖紙、在文件中嵌入設計，或為網站相簿產生縮圖時。Aspose.CAD for Java 讓此轉換變得簡單，無論是處理完整圖檔或僅針對特定圖面。本教學將逐步說明 **將 CAD 圖面轉換為點陣影像** 的完整流程——同樣的技巧也可產生 PNG、JPEG、TIFF 或 PDF 等輸出。

## 快速答覆
- **什麼函式庫負責 DWG 轉 PNG？** Aspose.CAD for Java  
- **可以匯出哪些格式？** PNG、JPEG、TIFF、PDF、BMP 等  
- **測試需要授權嗎？** 免費試用版可用於開發；正式環境需購買授權  
- **可以選擇特定圖面嗎？** 可以，使用 `setLayouts` 針對 “Model”、 “Layout1”等  
- **能產生高解析度輸出嗎？** 當然可以——調整 `setPageWidth` 與 `setPageHeight` 以控制 DPI  

## 什麼是「convert dwg to png」？

「convert dwg to png」指的是將向量式 DWG 檔（多數 CAD 應用程式的原生格式）轉換為像素式 PNG 影像的過程。點陣影像適合於網頁展示、電子郵件分享，以及整合至非 CAD 軟體中。

## 為什麼要將 CAD 匯出為 PNG（或其他點陣格式）？

- **通用相容性：** PNG 與 JPEG 幾乎被所有影像檢視器與瀏覽器支援。  
- **快速載入：** 點陣圖相較於開啟大型 DWG 檔案可即時載入。  
- **輕鬆嵌入：** 可直接將 PNG 插入 Word、PowerPoint 或 HTML，無需額外外掛。  
- **外觀一致性：** 您可自行控制解析度、背景與圖面，確保所有利害關係人看到相同的視覺效果。  

## 先決條件

在開始之前，請確保您已具備以下環境：

1. **Java 開發環境** – 已安裝並設定 JDK 8 或更新版本。  
2. **Aspose.CAD for Java** – 從 [Aspose.CAD for Java 文件](https://reference.aspose.com/cad/java/) 下載最新 JAR。  

## 匯入命名空間

首先匯入所需的類別。這些匯入讓您能存取影像載入、點陣化選項以及 TIFF/PNG 輸出設定。

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

> **專業提示：** 如果您打算匯出為 PNG 而非 TIFF，請將 `TiffOptions` 換成 `PngOptions`（位於 `com.aspose.cad.imageoptions.PngOptions`）。

## 逐步指南

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

您可以載入任何支援的格式（DWG、DXF、DGN 等）。這就是 **how to convert cad** 的部分——只要指向檔案即可讓 Aspose 處理解析。

### 步驟 3：設定點陣化選項

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1200);
rasterizationOptions.setPageHeight(1200);
rasterizationOptions.setLayouts(new String[] {"Model", "Layout1"});
```

- `setPageWidth` / `setPageHeight` 控制輸出解析度（數值越大 DPI 越高）。  
- `setLayouts` 讓您 **convert cad to raster** 指定圖面；若省略則會點陣化整個圖紙。

### 步驟 4：設定影像選項

```java
ImageOptionsBase options = new TiffOptions(TiffExpectedFormat.Default);
options.setVectorRasterizationOptions(rasterizationOptions);
```

如果您偏好 PNG，請實例化 `PngOptions` 取代 `TiffOptions`。這裡就是 **export cad as png** 的地方。

### 步驟 5：儲存產生的影像

```java
image.save(dataDir + "conic_pyramid_layoutstorasterimage_out_.tiff", options);
```

將檔案副檔名改為 `.png`（同時將選項物件改為 `PngOptions`）即可 **save CAD as JPEG/PNG**。

> **常見陷阱：** 忘記讓檔案副檔名與選項類別相符會導致 `UnsupportedFormatException`。請務必保持一致。

## 常見問題與解決方案

| 問題 | 解決方案 |
|-------|----------|
| **Blank output image** | 確認 `setLayouts` 中的圖面名稱與原始 CAD 檔案完全相同。 |
| **Low‑resolution PNG** | 增加 `setPageWidth` / `setPageHeight`，或在點陣化選項上設定 `setResolution`。 |
| **Unsupported DWG version** | 確認使用最新的 Aspose.CAD 版本；舊版可能不支援較新的 DWG 版本。 |
| **Memory errors on large files** | 逐頁處理或增加 JVM 堆積大小（例如 `-Xmx2g`）。 |

## 常見問答

**Q: Aspose.CAD 是否相容於不同的 CAD 檔案格式？**  
A: 是的，支援 DWG、DXF、DGN 等多種格式。

**Q: 我可以自訂輸出點陣圖的解析度嗎？**  
A: 當然可以。調整 `CadRasterizationOptions` 中的 `setPageWidth`、`setPageHeight` 或 `setResolution`。

**Q: 如何在一次執行中轉換多個 CAD 圖面？**  
A: 將所有圖面名稱組成陣列傳給 `setLayouts`，例如 `new String[]{"Model","Layout1","Layout2"}`。

**Q: 除了 TIFF，還支援其他輸出格式嗎？**  
A: 有的——透過各自的 `*Options` 類別可使用 PNG、JPEG、BMP、PDF 等。

**Q: 我該去哪裡取得協助或分享使用 Aspose.CAD 的經驗？**  
A: 前往 [Aspose.CAD 論壇](https://forum.aspose.com/c/cad/19) 獲得社群支援與官方協助。

## 結論

依照上述步驟，您即可 **convert DWG to PNG**、**export CAD as PNG**、**save CAD as JPEG**，或產生任何其他所需的點陣格式。Aspose.CAD for Java 負責繁重的轉換工作，讓您專注於將高品質影像整合至應用程式、文件或網站入口。

---

**最後更新：** 2025-12-18  
**測試環境：** Aspose.CAD for Java 24.12  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}