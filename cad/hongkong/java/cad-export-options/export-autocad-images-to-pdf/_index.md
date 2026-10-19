---
date: 2026-10-19
description: 了解如何在 Java 中使用 Aspose.CAD 將 DWG 轉換為 PDF。本分步指南示範如何匯出 AutoCAD PDF、將 CAD
  儲存為 PDF，並套用授權。
keywords:
- dwg to pdf java
- export autocad pdf
- java pdf export library
- aspose cad license
- save cad pdf
- customize pdf page size
lastmod: 2026-10-19
linktitle: 將 AutoCAD 圖像匯出為 PDF
og_description: 了解如何在 Java 中使用 Aspose.CAD 將 DWG 轉換為 PDF。本指南說明匯出 AutoCAD PDF、儲存 CAD
  為 PDF 以及授權步驟。
og_image_alt: 'Tutorial: convert DWG to PDF in Java with Aspose.CAD'
og_title: 使用 Aspose.CAD 在 Java 中將 DWG 轉換為 PDF
schemas:
- author: Aspose
  dateModified: '2026-10-19'
  description: Learn how to convert DWG to PDF in Java with Aspose.CAD. This step‑by‑step
    guide shows you how to export AutoCAD PDF, save CAD as PDF, and apply a license.
  headline: Convert DWG to PDF in Java using Aspose.CAD
  type: TechArticle
- description: Learn how to convert DWG to PDF in Java with Aspose.CAD. This step‑by‑step
    guide shows you how to export AutoCAD PDF, save CAD as PDF, and apply a license.
  name: Convert DWG to PDF in Java using Aspose.CAD
  steps:
  - name: set the resource directory path
    text: Replace `"Your Document Directory"` with the absolute path to the folder
      you created in the prerequisites. > **Pro tip:** Use `Paths.get(...).toAbsolutePath()`
      to avoid path‑related errors on different operating systems.
  - name: load the CAD image
    text: Loading the CAD file into an `Image` object gives you full access to Aspose.CAD’s
      rasterization engine. The `Image` class loads the DWG file and prepares it for
      conversion. > **Why this matters:** Once the drawing is in memory, you can query
      its layouts, layers, and metadata before rasterizing.
  - name: set rasterization options
    text: Adjust `pageWidth` and `pageHeight` to **customize PDF page size**. Enabling
      `setTypeOfEntities(TypeOfEntities.Entities3D)` allows full 3‑D rendering when
      needed. The `RasterizationOptions` object controls DPI, page dimensions, and
      entity types for the output. - `pageWidth` / `pageHeight` are measur
  - name: configure PDF options
    text: Tie the rasterization settings to the PDF output, ensuring the vector data
      is correctly transformed. The `PdfOptions` class links the rasterization configuration
      with the final PDF file.
  - name: save the PDF
    text: The resulting file, `Export3DImagestoPDF_out_.pdf`, is a **save cad as pdf**
      representation of your original AutoCAD drawing. The `save` method writes the
      rasterized image to a PDF file on disk.
  type: HowTo
- questions:
  - answer: Yes – the library supports DWG, DXF, DWF, DGN, and over 30 additional
      formats, giving you flexibility across projects.
    question: Can I use Aspose.CAD for Java with other CAD file formats?
  - answer: Visit the [temporary license page](https://purchase.aspose.com/temporary-license/)
      to request a time‑limited license for evaluation.
    question: How do I obtain a temporary license for Aspose.CAD for Java?
  - answer: Absolutely. Use `setLayouts("Model")`, `setLayouts("Layout1")`, etc.,
      to choose which view is rendered into the PDF.
    question: Are there layout options for rasterization?
  - answer: Yes – modify `pageWidth` and `pageHeight` in the rasterization options
      to match any required page dimensions.
    question: Can I change the size of the output PDF file?
  - answer: The dedicated community is available at the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19)
      where you can ask questions and share solutions.
    question: Where can I get help if I run into problems?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- dwg to pdf
- aspose.cad
- java cad conversion
- export autocad pdf
title: 使用 Aspose.CAD 在 Java 中將 DWG 轉換為 PDF
url: /zh-hant/java/cad-export-options/export-autocad-images-to-pdf/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 匯出 AutoCAD PDF – 使用 Aspose.CAD for Java 匯出 AutoCAD 圖像為 PDF

## 介紹

如果您需要在 Java 中 **將 DWG 轉換為 PDF**，您來對地方了。本教學示範如何使用 Aspose.CAD for Java 匯出 AutoCAD 圖像為 PDF，這是一個純 Java 函式庫，可處理 DWG、DXF、DWF 以及其他許多 CAD 格式，且不需要原生相依性。完成後，您將能夠 **將 CAD 儲存為 PDF**，調整光柵化選項如頁面大小，並正確套用 **Aspose CAD 授權** 以供正式使用。

## 快速答案
- **我可以使用 Java 轉換 DWG 為 PDF 嗎？** 是 – Aspose.CAD for Java 原生支援 DWG、DXF 以及數十種其他 CAD 格式。  
- **我需要授權嗎？** 永久的 **Aspose CAD 授權** 可移除所有評估限制；亦提供臨時授權供測試使用。  
- **支援哪些 Java 版本？** 完全支援 Java 8 及以上版本。  
- **我可以控制 PDF 頁面尺寸嗎？** 當然可以 – 在光柵化選項中設定 `pageWidth` 和 `pageHeight`。  
- **是否支援 3‑D 渲染？** 是 – 啟用 `TypeOfEntities.Entities3D` 即可光柵化 3‑D 實體。

## 什麼是匯出 AutoCAD PDF？
匯出 AutoCAD PDF 是將向量 CAD 圖紙轉換為可攜式 PDF 文件的過程。它會保留圖層、線寬、顏色，並可選擇性保留 3‑D 幾何，讓您輕鬆與客戶分享設計或在不需 CAD 軟體的情況下存檔。

## 為什麼要使用 Aspose.CAD for Java 轉換 DWG 為 PDF？
Aspose.CAD 支援 **50+ 輸入與輸出格式**，可在不將整個檔案載入記憶體的情況下處理上百頁的圖紙，且可在任何支援 Java 8+ 的平台上執行。此函式庫讓您完整掌控 DPI、頁面大小與版面配置，您可以 **自訂 PDF 頁面尺寸** 以符合精確的專案規格，且無需安裝原生 DLL。

## 前置條件

- **Java Development Kit** – 工作站上已安裝 JDK 8 或更新版本。  
- **Aspose.CAD for Java** – 從 [download link](https://releases.aspose.com/cad/java/) 下載最新 JAR。  
- **Working directory** – 用於存放來源 DWG 檔案與產生的 PDF 的資料夾。

## 匯入命名空間

`Image` 類別代表任何可光柵化的 CAD 圖紙，而 `RasterizationOptions` 與 `PdfOptions` 讓您微調轉換流程。

`Image` 類別是 Aspose.CAD 的頂層物件，負責在記憶體中保存 CAD 圖紙。  
`RasterizationOptions` 類別定義向量資料在寫入 PDF 前的光柵化方式。  
`PdfOptions` 類別將光柵化設定與 PDF 特定的輸出參數捆綁在一起。

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

現在讓我們一步一步走過程式碼。

## 如何使用 Aspose.CAD for Java 轉換 DWG 為 PDF？

要使用 Aspose.CAD for Java 將 DWG 檔案轉換為 PDF，先以 `Image` 類別載入圖紙，設定 `CadRasterizationOptions`（如 DPI、頁面大小與實體類型），再將這些選項包裝於 `PdfOptions`，最後呼叫 `save` 方法並指定 .pdf 檔名。此流程確保向量資料正確光柵化，且產生的 PDF 符合您的版面需求。

### 步驟 1：設定資源目錄路徑

將 `"Your Document Directory"` 替換為您在前置條件中建立的資料夾的絕對路徑。

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
```

> **專業提示：** 使用 `Paths.get(...).toAbsolutePath()` 可避免在不同作業系統上出現路徑相關錯誤。

### 步驟 2：載入 CAD 圖像

將 CAD 檔案載入 `Image` 物件，即可完整存取 Aspose.CAD 的光柵化引擎。

`Image` 類別會載入 DWG 檔案並為轉換做準備。

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

> **為什麼重要：** 圖紙載入記憶體後，您可以在光柵化前查詢其版面、圖層與中繼資料。

### 步驟 3：設定光柵化選項

調整 `pageWidth` 與 `pageHeight` 以 **自訂 PDF 頁面尺寸**。啟用 `setTypeOfEntities(TypeOfEntities.Entities3D)` 可在需要時完整支援 3‑D 渲染。

`RasterizationOptions` 物件控制 DPI、頁面尺寸與輸出實體類型。

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setPageHeight(500);
// rasterizationOptions.setTypeOfEntities(TypeOfEntities.Entities3D);

rasterizationOptions.setLayouts(new String[] {"Model"});
```

- `pageWidth` / `pageHeight` 以點為單位測量 (1 pt = 1/72 in)。  
- 取消註解 `setTypeOfEntities` 行以啟用 3‑D 光柵化。  
- `setLayouts` 用於選擇要渲染的版面 (Model、Layout1 等)。

### 步驟 4：設定 PDF 選項

將光柵化設定與 PDF 輸出關聯，確保向量資料正確轉換。

`PdfOptions` 類別將光柵化配置與最終 PDF 檔案連結。

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### 步驟 5：儲存 PDF

產生的檔案 `Export3DImagestoPDF_out_.pdf` 為您原始 AutoCAD 圖紙的 **save cad as pdf** 表現。

`save` 方法將光柵化後的圖像寫入磁碟上的 PDF 檔案。

```java
cadImage.save(dataDir + "Export3DImagestoPDF_out_.pdf", pdfOptions);
```

## 常見問題與解決方案

| 症狀 | 可能原因 | 解決方法 |
|------|----------|----------|
| 空白 PDF 輸出 | 未設定光柵化選項或版面不匹配 | 確認 `setLayouts` 與 CAD 檔案中的版面名稱相符。 |
| 低解析度圖像 | `pageWidth`/`pageHeight` 設定過小 | 增加尺寸或透過 `rasterizationOptions.setResolution(...)` 設定更高 DPI。 |
| 授權例外 | 未套用有效授權 | 套用 **Aspose CAD 授權** 或使用臨時授權進行測試。 |

## 常見問答

**Q: 我可以使用 Aspose.CAD for Java 處理其他 CAD 檔案格式嗎？**  
A: 可以 – 此函式庫支援 DWG、DXF、DWF、DGN 以及超過 30 種其他格式，讓您在不同專案中具備彈性。

**Q: 如何取得 Aspose.CAD for Java 的臨時授權？**  
A: 前往 [temporary license page](https://purchase.aspose.com/temporary-license/) 申請限時授權以供評估使用。

**Q: 是否有版面選項可供光柵化？**  
A: 當然有。使用 `setLayouts("Model")`、`setLayouts("Layout1")` 等，可選擇要渲染至 PDF 的視圖。

**Q: 我可以變更輸出 PDF 檔案的大小嗎？**  
A: 可以 – 在光柵化選項中修改 `pageWidth` 與 `pageHeight`，即可符合任何所需的頁面尺寸。

**Q: 若遇到問題，我該向哪裡尋求協助？**  
A: 可前往 [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) 與社群交流，提出問題並分享解決方案。

**最後更新：** 2026-10-19  
**測試環境：** Aspose.CAD for Java 24.10  
**作者：** Aspose

## 相關教學

- [Export DWG to PDF in Java – Set PDF Page Size with Aspose.CAD](/cad/java/cad-export-options/export-to-pdf/)
- [Export DWG to PDF: Specific Layout Using Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [Export DWG to PDF and Enable Tracking with Aspose.CAD Java](/cad/java/additional-features/enable-tracking/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}