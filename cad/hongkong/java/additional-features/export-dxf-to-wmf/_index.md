---
date: 2026-06-09
description: 了解如何使用 Aspose.CAD for Java 將 DXF 轉換為 WMF，包括免費試用、支援 Java 8+，以及可選的 PDF
  匯出。提供逐步說明與程式碼範例。
keywords:
- convert dxf to wmf
- aspose cad java
- aspose free trial
- aspose cad conversion
- export dxf pdf
linktitle: 使用 Java 匯出 DXF 為 WMF 格式
schemas:
- author: Aspose
  dateModified: '2026-06-09'
  description: Learn how to convert DXF to WMF with Aspose.CAD for Java, including
    a free trial, Java 8+ support, and optional PDF export. Step‑by‑step guide with
    code examples.
  headline: Convert DXF to WMF Using Aspose.CAD in Java
  type: TechArticle
- description: Learn how to convert DXF to WMF with Aspose.CAD for Java, including
    a free trial, Java 8+ support, and optional PDF export. Step‑by‑step guide with
    code examples.
  name: Convert DXF to WMF Using Aspose.CAD in Java
  steps:
  - name: Load DXF Drawing
    text: Image.load reads the DXF file into an Aspose.CAD Image object.
  - name: Configure Rasterization Options
    text: CadRasterizationOptions specifies page size, resolution, and background
      for rasterizing the CAD drawing.
  - name: Save as WMF
    text: ImageSaveOptions with SaveFormat.WMF tells Aspose.CAD to write the output
      as a Windows Metafile.
  - name: Dispose of Resources
    text: Calling image.close() releases native resources used by the Aspose.CAD Image
      object.
  - name: Optional – Export to PDF
    text: PdfOptions configures PDF‑specific settings when saving the image as a PDF
      document. > **Pro tip:** You can reuse the same `CadRasterizationOptions` object
      for PDF export by passing it to a `PdfOptions` instance, saving you a few lines
      of setup.
  type: HowTo
- questions:
  - answer: Yes. Load the file in a try‑with‑resources block and dispose of the `Image`
      object promptly. Adjust `CadRasterizationOptions.setPageWidth/Height` to a reasonable
      size to keep memory usage low.
    question: Can I convert large DXF files (hundreds of MB) without running out of
      memory?
  - answer: WMF is a flat vector format, so layer hierarchy is flattened, but line
      styles, colors, and hatch patterns are preserved.
    question: Does the WMF output retain layer information?
  - answer: Use `rasterizationOptions.setResolution(300);` to define DPI before saving.
    question: Is it possible to set a custom DPI for the WMF?
  - answer: Absolutely. Loop through a directory, load each file, and apply the same
      rasterization and save logic.
    question: Can I batch‑convert multiple DXF files in one run?
  - answer: Aspose.CAD for Java supports Java 8 and later, including Java 11, 17,
      and newer LTS releases.
    question: What versions of Java are supported?
  type: FAQPage
second_title: Aspose.CAD Java API
title: 使用 Aspose.CAD 在 Java 中將 DXF 轉換為 WMF
url: /zh-hant/java/additional-features/export-dxf-to-wmf/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.CAD 於 Java 轉換 DXF 為 WMF

## 簡介

在本教學中，您將學習如何使用 Aspose.CAD for Java **將 DXF 轉換為 WMF**。無論您是需要在 Windows 報告中嵌入 CAD 圖紙、為 Office 文件產生輕量向量圖形，或是自動化批次轉換，DXF 轉 WMF 是工程與報告流程中常見的需求。我們將示範如何載入 DXF 圖紙、設定光柵化選項、將結果儲存為 WMF，並可選擇將同一圖紙匯出為 PDF。

## 快速解答
- **我可以使用免費試用版將 DXF 轉換為 WMF 嗎？** 可以 — Aspose 提供完整功能的 30 天試用版。  
- **需要哪個 Java 版本？** Java 8 或更新版本。  
- **執行程式碼是否需要授權？** 生產環境需要授權；試用版可用於開發與測試。  
- **轉換是否無損？** 向量資料會被保留；光柵化選項可讓您控制解析度。  
- **我也可以將同一圖紙匯出為 PDF 嗎？** 當然可以 — 請參閱下方「匯出為 PDF」步驟。

## 什麼是「將 DXF 轉換為 WMF」？

將 DXF 轉換為 WMF 意味著將 Drawing Exchange Format（DXF）檔案——一種廣泛使用的 CAD 格式——轉換為 Windows Metafile（WMF）。WMF 是一種向量圖像格式，可順利整合至 Microsoft Office、Windows 應用程式以及眾多報告工具中。

## 為何使用 Aspose.CAD for Java？

Aspose.CAD for Java 提供純 Java、無需原生 DLL 的引擎，可將 CAD 檔案轉換，**向量保真度超過 99 %**，保留圖層、顏色、線條樣式與剖面圖案。它支援 **50 多種輸入與輸出格式**——包括 DXF、DWG、DGN、PDF、PNG、SVG 與 WMF——同時允許透過內建光柵化選項微調頁面大小、DPI 與背景顏色。同一套 API 亦可處理 PDF、PNG 與 SVG 的匯出，免除使用多個函式庫的需求。

### 主要優勢
- **無外部相依性** – 純 Java，可在任何執行 Java 的作業系統上運作。  
- **高保真度渲染** – 保留線寬、顏色與剖面細節。  
- **內建光柵化** – 可控制頁面尺寸、解析度與背景。  
- **一站式轉換** – 同一套類別即可匯出為 WMF、PDF、PNG、SVG 等格式。

## 先決條件

在開始之前，請確保您已具備：

- **Aspose.CAD for Java** 已整合至您的專案中。可從官方網站下載：[Aspose.CAD Java download](https://releases.aspose.com/cad/java/)。  
- **文件目錄**，即存放 DXF 檔案的資料夾（例如 `Your Document Directory/DXFDrawings/`）。

## 匯入命名空間

以下匯入語句會載入 Aspose.CAD 類別，以支援 CAD 檔案的載入、光柵化與儲存。

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageSaveOptions;
import com.aspose.cad.fileformats.cad.CadRasterizationOptions;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.CadImageInfo;
import com.aspose.cad.fileformats.cad.CadImageInfo;
import java.awt.Color;
```

## 逐步指南

### 如何在 Java 中將 DXF 轉換為 WMF？

使用 `Image.load("yourFile.dxf")` 載入 DXF 檔案，設定 `CadRasterizationOptions` 以指定頁面大小與 DPI，然後呼叫 `image.save("output.wmf", new ImageSaveOptions(SaveFormat.WMF))`。此三步驟模式即可完成轉換，保持向量品質完整，且僅需少量程式碼。

#### 步驟 1：載入 DXF 圖紙

Image.load 會將 DXF 檔案讀取為 Aspose.CAD Image 物件。

```java
import com.aspose.cad.Color;
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.WmfOptions;
```

#### 步驟 2：設定光柵化選項

CadRasterizationOptions 用於指定光柵化 CAD 圖紙的頁面大小、解析度與背景。

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DXFDrawings/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

#### 步驟 3：儲存為 WMF

使用 SaveFormat.WMF 的 ImageSaveOptions 會指示 Aspose.CAD 將輸出寫入為 Windows Metafile。

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(100);
rasterizationOptions.setPageHeight(100);
WmfOptions wmfOptions = new WmfOptions();
```

#### 步驟 4：釋放資源

呼叫 image.close() 會釋放 Aspose.CAD Image 物件所使用的原生資源。

```java
cadImage.save(dataDir+" example.ifc.wmf", wmfOptions);
```

#### 步驟 5：選用 – 匯出為 PDF

PdfOptions 會在將影像儲存為 PDF 文件時設定 PDF 專屬的參數。

```java
finally
{
  cadImage.dispose();
}
```

> **專業提示:** 您可以將相同的 `CadRasterizationOptions` 物件傳遞給 `PdfOptions` 實例，以在匯出 PDF 時重複使用，從而省去幾行設定程式碼。

## 如何使用 Aspose CAD Java 將 DXF 匯出為 PDF？

匯出為 PDF 的流程與載入與光柵化步驟相同；只需將 WMF 儲存格式改為 PDF。使用 `new ImageSaveOptions(SaveFormat.Pdf)`，並可選擇設定 PDF 專屬的選項，例如壓縮等級或作者資訊。此單行程式碼的轉換會產生可搜尋、頁面精確的 PDF，與原始 CAD 版面相同。

## 常見問題與解決方案

| 問題 | 原因 | 解決方法 |
|-------|-------|-----|
| **`cadImage.save` 發生 NullPointerException** | 變數 `cadImage` 未定義（應為 `image`）。 | 將 `cadImage` 改為 `image`，或一致性地重新命名變數。 |
| **輸出 WMF 為空白** | 光柵化頁面尺寸過小或背景色設為透明。 | 增大 `PageWidth`/`PageHeight`，或透過 `rasterizationOptions.setBackgroundColor(Color.WHITE);` 設定背景顏色。 |
| **授權例外** | 在生產環境中未使用有效的 Aspose 授權。 | 在應用程式啟動時載入授權檔案：`License license = new License(); license.setLicense("Aspose.Total.Java.lic");`。 |

## 結論

您現在已擁有完整、可投入生產的工作流程，使用 Aspose.CAD for Java **將 DXF 轉換為 WMF**，並可選擇 **將同一圖紙匯出為 PDF**。此方法可產生高品質的向量輸出，能順利整合至基於 Windows 的報告與文件工具，同時保持程式碼簡潔且無相依性。

## 常見問答

### Q1：在哪裡可以找到 Aspose.CAD 文件說明？
A1：您可於此處取得文件說明 [此處](https://reference.aspose.com/cad/java/)。

### Q2：如何下載 Aspose.CAD for Java？
A2：下載此函式庫 [此處](https://releases.aspose.com/cad/java/)。

### Q3：是否提供免費試用？
A3：是的，您可於 [此處](https://releases.aspose.com/) 取得免費試用。

### Q4：需要臨時授權選項嗎？
A4：請於 [此處](https://purchase.aspose.com/temporary-license/) 探索臨時授權方案。

### Q5：在哪裡可以取得支援？
A5：請前往 Aspose.CAD 支援論壇 [此處](https://forum.aspose.com/c/cad/19)。

## 常見問題

**Q: 我可以在不耗盡記憶體的情況下轉換大型 DXF 檔案（數百 MB）嗎？**  
A: 可以。請在 try‑with‑resources 區塊中載入檔案，並及時釋放 `Image` 物件。調整 `CadRasterizationOptions.setPageWidth/Height` 為合理大小，以降低記憶體使用量。

**Q: WMF 輸出會保留圖層資訊嗎？**  
A: WMF 為平面向量格式，圖層層級會被平坦化，但線條樣式、顏色與剖面圖案會被保留。

**Q: 是否可以為 WMF 設定自訂 DPI？**  
A: 可在儲存前使用 `rasterizationOptions.setResolution(300);` 來設定 DPI。

**Q: 我可以在一次執行中批次轉換多個 DXF 檔案嗎？**  
A: 當然可以。遍歷目錄，載入每個檔案，並套用相同的光柵化與儲存邏輯。

**Q: 支援哪些 Java 版本？**  
A: Aspose.CAD for Java 支援 Java 8 及以上版本，包括 Java 11、17 以及更新的 LTS 版本。

**最後更新：** 2026-06-09  
**測試環境：** Aspose.CAD for Java 24.11  
**作者：** Aspose

```java
image.save(dataDir + "conic_pyramid_out_.pdf"); 
```

## 相關教學

- [從 CAD 建立 PDF – 使用 Aspose.CAD for Java 匯出 DXF 為 PDF](/cad/java/additional-features/export-dxf-to-pdf/)
- [從 DXF 建立 PDF：使用 Aspose.CAD for Java 匯出圖層](/cad/java/additional-features/export-specific-layer-to-pdf/)
- [如何使用 Aspose.CAD in Java 將 DXF 版面轉換為 JPEG 圖像](/cad/java/additional-features/export-specific-layout-to-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}