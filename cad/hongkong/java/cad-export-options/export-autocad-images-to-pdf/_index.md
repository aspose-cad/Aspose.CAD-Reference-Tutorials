---
date: 2026-10-19
description: 了解如何使用 Aspose.CAD for Java，將 AutoCAD 圖紙匯出為自訂 PDF 頁面大小。本分步指南涵蓋 DWG 轉 PDF、rasterization
  選項與 licensing。
keywords:
- custom pdf page size
- export autocad to pdf
- save cad as pdf
- generate pdf from dwg
- dwg to pdf java
lastmod: 2026-10-19
linktitle: 匯出 AutoCAD 圖像為 PDF
og_description: 在使用 Aspose.CAD for Java 匯出 AutoCAD 圖紙為 PDF 時設定自訂 PDF 頁面大小。快速學習 DWG
  轉 PDF、rasterization 設定與 licensing。
og_image_alt: Guide showing how to export AutoCAD drawings to PDF with custom page
  dimensions using Aspose.CAD for Java
og_title: 使用 Aspose.CAD 為 AutoCAD 匯出設定自訂 PDF 頁面大小
schemas:
- author: Aspose
  dateModified: '2026-10-19'
  description: Learn how to export AutoCAD drawings to PDF with a custom PDF page
    size using Aspose.CAD for Java. This step‑by‑step guide covers converting DWG
    to PDF, rasterization options, and licensing.
  headline: Set custom PDF page size for AutoCAD export with Aspose.CAD
  type: TechArticle
- description: Learn how to export AutoCAD drawings to PDF with a custom PDF page
    size using Aspose.CAD for Java. This step‑by‑step guide covers converting DWG
    to PDF, rasterization options, and licensing.
  name: Set custom PDF page size for AutoCAD export with Aspose.CAD
  steps:
  - name: set the resource directory path
    text: '> **Pro tip:** Replace `"Your Document Directory"` with the absolute path
      to the folder you created in the prerequisites.'
  - name: load the CAD image
    text: The `Image` class loads the CAD file and gives you access to Aspose.CAD’s
      rasterization engine. > **Why this matters:** Once the CAD file is loaded, you
      can manipulate rasterization options before rendering to PDF.
  - name: set rasterization options
    text: The `CadRasterizationOptions` class specifies how the CAD drawing is rasterized
      before being saved as PDF. Adjust `pageWidth` and `pageHeight` to define a **custom
      PDF page size**. You can also enable 3‑D rendering by uncommenting the `setTypeOfEntities`
      line. - `pageWidth` / `pageHeight` – measured
  - name: configure PDF options
    text: The `PdfOptions` class holds PDF‑specific settings and links the rasterization
      options to the output file, ensuring the custom page dimensions are applied
      correctly.
  - name: save the PDF
    text: The `save` method writes the rendered image to the specified PDF file. The
      resulting file, `Export3DImagestoPDF_out_.pdf`, is a **save cad as pdf** representation
      of your original AutoCAD drawing with the exact page dimensions you specified.
  type: HowTo
- questions:
  - answer: Yes, the library supports DWG, DXF, DWF, DGN, and many more, giving you
      flexibility across projects.
    question: Can I use Aspose.CAD for Java with other CAD file formats?
  - answer: Visit the [temporary license page](https://purchase.aspose.com/temporary-license/)
      to request a time‑limited license for evaluation.
    question: How do I obtain a temporary license for Aspose.CAD for Java?
  - answer: Absolutely. Use `setLayouts("Model")` or specify other layout names to
      control which view is rendered.
    question: Are there layout options for rasterization?
  - answer: Yes – modify `pageWidth` and `pageHeight` in the rasterization options
      to any dimensions you need.
    question: Can I customize the size of the output PDF file?
  - answer: The dedicated [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) offers
      community support and official responses from the Aspose team.
    question: Where can I get help or discuss issues related to Aspose.CAD for Java?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- custom pdf page size
- Aspose.CAD
- Java CAD conversion
- PDF generation
- DWG export
title: 使用 Aspose.CAD 為 AutoCAD 匯出設定自訂 PDF 頁面大小
url: /zh-hant/java/cad-export-options/export-autocad-images-to-pdf/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 匯出 AutoCAD PDF - 使用 Aspose.CAD for Java 匯出 AutoCAD 圖像為 PDF

## 簡介

如果您需要 **convert DWG to PDF** 並控制輸出檔案的精確尺寸，您來對地方了。本教學說明如何在使用 Aspose.CAD for Java 匯出 AutoCAD 圖像為 PDF 時設定 **custom PDF page size**。完成本指南後，您將了解如何載入 DWG、設定 DPI 與頁寬/頁高等光柵化選項、套用授權，並產生可投入生產的 PDF。

## 快速回答
- **我可以使用 Java 轉換 DWG 為 PDF 嗎？** 是的 – Aspose.CAD for Java 原生支援 DWG、DXF、DWF 以及許多其他 CAD 格式。  
- **我需要授權才能投入生產使用嗎？** 完整的 Aspose.CAD 授權會移除所有評估限制；亦提供臨時授權供測試使用。  
- **哪個 Java 版本相容？** 此函式庫相容於 Java 8 及之後的所有 JDK。  
- **如何變更 PDF 頁面尺寸？** 在 `PdfOptions.getRasterizationOptions()` 上設定 `pageWidth` 與 `pageHeight` 為您需要的任意尺寸。  
- **是否支援 3‑D 渲染？** 是的 – 啟用 `TypeOfEntities.Entities3D` 以光柵化 3‑D 實體。

## 什麼是匯出 AutoCAD PDF？
匯出 AutoCAD PDF 指的是將向量式 CAD 圖紙（DWG、DXF、DWF 等）轉換為可攜式 PDF 文件，同時保留圖層、線寬以及可選的 3‑D 幾何。這讓您能與客戶分享設計、存檔圖紙，或在未安裝 CAD 軟體的情況下直接列印。

## 為何使用 Aspose.CAD for Java 轉換 DWG 為 PDF？
Aspose.CAD for Java 是轉換 DWG 為 PDF 的理想選擇，因為它提供廣泛的格式支援、以純 Java 執行且無需原生相依性、提供高解析度光柵化且可完整控制 DPI 與頁面大小，並具彈性授權機制，讓您可從試用版開始，逐步擴展至正式生產環境。

- **廣泛的格式支援** – 支援 50 多種輸入與輸出格式，包括 DWG、DXF、DWF、DGN 以及 PDF。  
- **純 Java 實作** – 無需原生 DLL 或外部相依性，部署於任何平台皆相當簡單。  
- **高解析度光柵化** – 您可以指定 DPI、頁面大小與版面配置，完整掌控結果的 **custom PDF page size**。  
- **可擴充的授權** – 從免費試用開始，之後升級為永久的 **Aspose CAD license**。  

## 先決條件

- **Java Development Kit** – 已在機器上安裝 JDK 8 或更新版本。  
- **Aspose.CAD for Java** – 從 [download link](https://releases.aspose.com/cad/java/) 下載最新的 JAR。  
- **Working directory** – 包含來源 DWG 檔案並將接收產生的 PDF 的資料夾。  

## 匯入命名空間

`Image` 類別是 Aspose.CAD 的核心物件，代表記憶體中的 CAD 圖紙。請在開始編寫程式碼前匯入所需的套件。

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

現在讓我們一步一步走過程式碼。

## 如何在匯出 DWG 為 PDF 時設定自訂 PDF 頁面尺寸？

載入您的 DWG，定義所需的頁寬與頁高，然後將結果儲存為 PDF – 這就是建立具自訂頁面尺寸 PDF 所需的一切。以下步驟說明了精確的順序與最小化的程式碼需求。

### 步驟 1：設定資源目錄路徑

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
```

> **專業提示：** 將 `"Your Document Directory"` 替換為您在先決條件中建立的資料夾的絕對路徑。

### 步驟 2：載入 CAD 圖像

`Image` 類別載入 CAD 檔案，並讓您存取 Aspose.CAD 的光柵化引擎。

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

> **為什麼重要：** 一旦 CAD 檔案載入，您即可在渲染成 PDF 前調整光柵化選項。

### 步驟 3：設定光柵化選項

`CadRasterizationOptions` 類別指定 CAD 圖紙在儲存為 PDF 前的光柵化方式。調整 `pageWidth` 與 `pageHeight` 以定義 **custom PDF page size**。您亦可透過取消註解 `setTypeOfEntities` 行來啟用 3‑D 渲染。

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setPageHeight(500);
// rasterizationOptions.setTypeOfEntities(TypeOfEntities.Entities3D);

rasterizationOptions.setLayouts(new String[] {"Model"});
```

- `pageWidth` / `pageHeight` – 以像素為單位；變更這些值以符合 A4、Letter 或任何自訂尺寸。  
- `setTypeOfEntities(TypeOfEntities.Entities3D)` – 需要時渲染 3‑D 實體。  
- `setLayouts` – 選擇要光柵化的版面（Model、Layout1 等）。  

### 步驟 4：設定 PDF 選項

`PdfOptions` 類別保存 PDF 專屬設定，並將光柵化選項連結至輸出檔案，確保正確套用自訂頁面尺寸。

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### 步驟 5：儲存 PDF

`save` 方法將渲染後的圖像寫入指定的 PDF 檔案。

```java
cadImage.save(dataDir + "Export3DImagestoPDF_out_.pdf", pdfOptions);
```

產生的檔案 `Export3DImagestoPDF_out_.pdf` 為您原始 AutoCAD 圖紙的 **save cad as pdf** 表現，具備您指定的精確頁面尺寸。

## 常見問題與解決方案

| 症狀 | 可能原因 | 解決方法 |
|------|----------|----------|
| PDF 為空白 | 未設定光柵化選項或版面不匹配 | 確認 `setLayouts` 與 CAD 檔案中的版面名稱相符。 |
| 低解析度影像 | `pageWidth`/`pageHeight` 太小或 DPI 較低 | 增大尺寸或以較高 DPI 呼叫 `rasterizationOptions.setResolution(...)`。 |
| 授權例外 | 未套用有效授權 | 套用永久的 Aspose.CAD 授權，或使用臨時授權進行測試。 |

## 常見問與答

**Q: 我可以將 Aspose.CAD for Java 用於其他 CAD 檔案格式嗎？**  
A: 是的，函式庫支援 DWG、DXF、DWF、DGN 等多種格式，讓您在各種專案中具備彈性。

**Q: 我如何取得 Aspose.CAD for Java 的臨時授權？**  
A: 請前往 [temporary license page](https://purchase.aspose.com/temporary-license/) 申請限時評估授權。

**Q: 光柵化有版面選項嗎？**  
A: 當然有。使用 `setLayouts("Model")` 或指定其他版面名稱，即可控制要渲染的視圖。

**Q: 我可以自訂輸出 PDF 檔案的大小嗎？**  
A: 可以 – 在光柵化選項中修改 `pageWidth` 與 `pageHeight` 為您需要的任意尺寸。

**Q: 我可以在哪裡取得協助或討論與 Aspose.CAD for Java 相關的問題？**  
A: 專屬的 [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) 提供社群支援與 Aspose 團隊的官方回應。

## 其他常見問答（AI 友好格式）

**Q: Aspose.CAD 在 Windows 或 Linux 上需要任何原生函式庫嗎？**  
A: 不需要。Aspose.CAD for Java 為純 Java 函式庫，因而可在支援 JDK 的任何平台上執行，無需額外的原生 DLL。

**Q: 函式庫能處理多大的 DWG 檔案？**  
A: 該函式庫可處理多頁（最高至 500 MB）的圖紙，且不需將整個檔案載入記憶體，得益於其串流架構。

**Q: 是否能一次批次轉換多個 DWG 檔案為 PDF？**  
A: 可以。遍歷資料夾，使用 `Image.load()` 載入每個檔案，套用相同的光柵化選項，然後對每個輸出 PDF 呼叫 `save()`。

**Q: 在一般伺服器上可期待的效能如何？**  
A: 根據 Aspose 的基準測試，於標準 2.5 GHz CPU 上將 100 頁、300 DPI 的 DWG 轉換約需 12 秒。

**Q: 函式庫會在 PDF 中保留圖層資訊嗎？**  
A: 雖然輸出為光柵化，但圖層、線寬與顏色的視覺外觀會忠實再現。

**最後更新：** 2026-10-19  
**測試環境：** Aspose.CAD for Java 24.10  
**作者：** Aspose

## 相關教學

- [匯出 DWG 為 PDF 並啟用追蹤 (Aspose.CAD Java)](/cad/java/additional-features/enable-tracking/)
- [匯出 DWG 為 PDF：使用 Aspose.CAD Java 的特定版面](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [匯出 DWG 為 BMP 並使用單位類型調整 CAD 大小 (Aspose.CAD for Java)](/cad/java/cad-file-manipulation/adjusting-cad-drawing-size-using-unit-type/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}