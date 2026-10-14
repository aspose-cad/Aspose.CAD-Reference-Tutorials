---
date: 2026-10-14
description: 了解如何使用 Java CAD 函式庫 Aspose.CAD for Java 快速且精確地將 DWG 匯出為 PDF 或點陣圖像。
keywords:
- export dwg pdf
- high quality pdf
- dwg to pdf tutorial
- aspose cad java
- java cad library
lastmod: 2026-10-14
linktitle: 匯出 DWG PDF 與點陣圖像
og_description: 使用 Aspose.CAD for Java 快速匯出 DWG 為 PDF。了解高品質 PDF 轉換、點陣圖選項與授權方式的逐步指南。
og_image_alt: Tutorial showing Java code to convert DWG drawings to PDF and raster
  formats with Aspose.CAD
og_title: 使用 Java CAD 函式庫 Aspose.CAD 匯出 DWG PDF 與點陣圖像
schemas:
- author: Aspose
  dateModified: '2026-10-14'
  description: Learn how the Java CAD library Aspose.CAD for Java can export DWG to
    PDF or raster images quickly and accurately.
  headline: Export DWG PDF and raster images using Java CAD library Aspose.CAD
  type: TechArticle
- description: Learn how the Java CAD library Aspose.CAD for Java can export DWG to
    PDF or raster images quickly and accurately.
  name: Export DWG PDF and raster images using Java CAD library Aspose.CAD
  steps:
  - name: Load the DWG file
    text: First, load your DWG drawing using the `Image` class. This creates an in‑memory
      representation that Aspose.CAD can work with.
  - name: Determine unit type
    text: Understanding whether the drawing uses metric or imperial units is essential
      for correct scaling. The helper method `IsMetric` (implementation omitted for
      brevity) returns a boolean flag.
  - name: Set rasterization options
    text: The `CadRasterizationOptions` class defines rasterization parameters such
      as DPI, page size, and unit conversion. Based on the unit system, configure
      page size, scaling, and the target unit type. These options drive how the DWG
      is rasterized before being wrapped into a PDF.
  - name: Configure PDF options (pdf options cad)
    text: The `PdfOptions` class specifies PDF‑specific settings, including compression
      and metadata. Create a `PdfOptions` instance and attach the rasterization settings.
      This tells Aspose.CAD how to embed the rasterized content into the final PDF.
  - name: Save as PDF
    text: The `save` method writes the image to the given file path using the supplied
      options. Finally, export the drawing to a PDF file. The `save` method takes
      the output path and the configured `PdfOptions`. When the code finishes, you’ll
      find **Saved.pdf** in your `DWGDrawings` folder, ready for distribu
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD for Java seamlessly integrates with popular Java frameworks
      such as Spring, Jakarta EE, and Android.
    question: Can I use Aspose.CAD for Java with other Java frameworks?
  - answer: Yes, you can obtain a temporary license **[obtain a temporary license](https://purchase.aspose.com/temporary-license/)**.
    question: Is a temporary license available for Aspose.CAD for Java?
  - answer: Visit the **[Aspose.CAD forum](https://forum.aspose.com/c/cad/19)** for
      assistance from the community and Aspose engineers.
    question: Where can I find support for Aspose.CAD for Java?
  - answer: You can purchase a license **[purchase a license](https://purchase.aspose.com/buy)**.
    question: How can I purchase a license for Aspose.CAD for Java?
  - answer: Aspose.CAD for Java supports both metric and imperial units, automatically
      detecting the drawing’s unit system.
    question: What units does Aspose.CAD for Java support?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- export dwg
- aspose.cad
- java cad conversion
title: 使用 Java CAD 函式庫 Aspose.CAD 匯出 DWG PDF 與點陣圖像
url: /zh-hant/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Java CAD 函式庫 Aspose.CAD 匯出 DWG PDF 與光柵影像

## 介紹

將 DWG 匯出為 PDF 是工程師、建築師以及任何需要在不暴露原始檔案格式的情況下分享 CAD 圖紙的常見需求。使用 **Aspose.CAD for Java**，您只需幾行 Java 程式碼即可 **export dwg pdf** — 或光柵影像 —，同時保持向量的忠實度與版面精確度。本教學將帶您逐步載入 DWG 檔案、設定光柵化參數，並將結果儲存為高品質的 PDF 或影像。您也會了解為何 Aspose.CAD 是可靠、跨平台轉換的首選 Java CAD 函式庫。

如需僅針對 PDF 轉換的專門指南，請參閱 [匯出 DWG 為 PDF 教程](/java/cad-drawing-conversion/export-dwg-to-pdf/)。

## 快速解答
- **本教學涵蓋什麼內容？** 使用 Aspose.CAD for Java 將 DWG 檔案匯出為 PDF 或光柵影像。  
- **我需要授權嗎？** 可取得免費的暫時授權供評估使用；正式環境需購買完整授權。  
- **支援哪個 Java 版本？** 任何 Java 8 以上的執行環境皆可搭配最新的 Aspose.CAD Java API 使用。  
- **我可以將 DWG 轉換為其他影像格式嗎？** 可以 — 相同的光柵化選項可輸出 PNG、JPEG、BMP 等格式。  
- **轉換需要多長時間？** 標準圖紙通常在一秒以內完成；較大的檔案可能需要數秒。

## 為何 Java CAD 函式庫是 DWG 轉換的最佳選擇？

Aspose.CAD for Java 是最佳選擇，因為它提供純 Java 實作，無需原生 DLL，能自動偵測公制或英制單位，提供最高 1200 DPI 的光柵輸出，且可產生保留向量的 PDF，無需外部相依性。此函式庫亦提供彈性的授權模式，讓您可從暫時授權開始，並擴展至企業級使用。

## 什麼是「export dwg to pdf」？

`Export dwg pdf` 是將原生 DWG 圖紙檔案轉換為 PDF 文件的過程，並保留向量資料、圖層與比例。此轉換產生與裝置無關的檔案，可在任何平台上檢視，無需 AutoCAD。由於 PDF 保留向量資訊，文字仍可搜尋，圖形在任何縮放層級下皆保持清晰，適合用於文件、客戶審閱與歸檔儲存。

## 為何在此轉換中使用 Aspose.CAD Java？

您應該使用 Aspose.CAD Java，因為此函式庫在內部處理單位轉換、光柵化與 PDF 嵌入，免除第三方工具或複雜指令列流程的需求。其 API 為開發者設計：單一 `Image` 物件即代表圖紙，少數設定物件即可微調 DPI、頁面尺寸與壓縮。最終在 Windows、Linux 與 macOS 環境中皆能產生一致且可重複的輸出。

## 前置需求

在深入程式碼之前，請確保您已具備：

- 基本的 Java 程式設計知識。  
- 已安裝 Aspose.CAD for Java 函式庫。若尚未下載，請取得 **[下載 Aspose.CAD for Java](https://releases.aspose.com/cad/java/)**。  
- 測試用的 DWG 檔案 — 本指南使用範例 **Bottom_plate.dwg**。

## 匯入命名空間

在您的 Java 專案中，匯入必要的類別以啟動轉換：

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.UnitType;
```

## 步驟說明

### 步驟 1：載入 DWG 檔案

首先，使用 `Image` 類別載入 DWG 圖紙。這會在記憶體中建立 Aspose.CAD 可處理的表示。

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Bottom_plate.dwg";
Image objImage = Image.load(srcFile);
```

### 步驟 2：判斷單位類型

了解圖紙使用公制或英制單位對於正確縮放至關重要。輔助方法 `IsMetric`（此處省略實作）會回傳布林值。

```java
Boolean currentUnitIsMetric = IsMetric(objImage.getUnitType());
int currentUnitCoefficient = objImage.getUnitType();
```

### 步驟 3：設定光柵化選項

`CadRasterizationOptions` 類別定義光柵化參數，如 DPI、頁面尺寸與單位轉換。根據單位系統，設定頁面尺寸、縮放與目標單位類型。這些選項決定 DWG 在包裝成 PDF 前的光柵化方式。

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();

if (currentUnitIsMetric) {
    // Metric units
    double metersCoeff = 1 / 1000.0;
    double scaleFactor = metersCoeff / currentUnitCoefficient;
    rasterizationOptions.setPageWidth((float)(210 * scaleFactor));
    rasterizationOptions.setPageHeight((float)(297 * scaleFactor));
    rasterizationOptions.setUnitType(UnitType.Millimeter);
} else {
    // Imperial units
    rasterizationOptions.setPageWidth((float)(8.27f / currentUnitCoefficient));
    rasterizationOptions.setPageHeight((float)(11.69f / currentUnitCoefficient));
    rasterizationOptions.setUnitType(UnitType.Inch);
}
```

### 步驟 4：設定 PDF 選項（pdf options cad）

`PdfOptions` 類別指定 PDF 專屬設定，包括壓縮與中繼資料。建立 `PdfOptions` 實例並附加光柵化設定。此設定告訴 Aspose.CAD 如何將光柵化內容嵌入最終 PDF。

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());
```

### 步驟 5：儲存為 PDF

`save` 方法使用提供的選項將影像寫入指定的檔案路徑。最後，將圖紙匯出為 PDF 檔案。`save` 方法接受輸出路徑與已設定的 `PdfOptions`。

```java
objImage.save(dataDir + "Saved.pdf", pdfOptions);
```

程式執行完畢後，您會在 `DWGDrawings` 資料夾中看到 **Saved.pdf**，即可用於分發或歸檔。

## 如何使用 Java CAD 函式庫將 DWG 轉換為光柵影像？

您可以透過將 `PdfOptions` 替換為光柵專用的選項類別（如 `PngOptions` 或 `JpegOptions`）來將 DWG 轉換為光柵格式。重複使用相同的 `CadRasterizationOptions` 實例，調整輸出格式，並以新的選項物件呼叫 `save` 方法。此方式只需一行程式碼變更，即可產生 PNG、JPEG、BMP 或 TIFF 檔案，保持工作流程一致。

## 如何使用 PDF options CAD 產生 PDF DWG？

上述範例已 **generates pdf dwg** 輸出。若要微調 PDF 大小，可呼叫 `pdfOptions.setCompress(true)` 以啟用壓縮。您亦可嵌入自訂中繼資料、設定 PDF 版本，或透過額外的 `PdfOptions` 屬性加入密碼保護。這些調整讓您在不離開 Java 程式碼的情況下，完整掌控最終 PDF。

## 常見問題與技巧

- **頁面尺寸不正確** — 請再次確認單位轉換邏輯；係數不匹配可能導致頁面過大。  
- **缺少字型或線寬** — 確保 DWG 在轉換前已參照所有外部資源。  
- **大型圖紙的效能** — 僅在需要更高品質時才提升 `CadRasterizationOptions` 中的 `DPI` 設定；降低 DPI 可加快處理速度。  
- **授權問題** — 評估時可使用 **temporary license Aspose**；正式部署需購買完整授權。

## 常見問答

**Q: 我可以將 Aspose.CAD for Java 與其他 Java 框架一起使用嗎？**  
A: 可以，Aspose.CAD for Java 可無縫整合於常見的 Java 框架，如 Spring、Jakarta EE 與 Android。

**Q: 是否提供 Aspose.CAD for Java 的暫時授權？**  
A: 可以，您可取得暫時授權 **[取得暫時授權](https://purchase.aspose.com/temporary-license/)**。

**Q: 哪裡可以找到 Aspose.CAD for Java 的支援？**  
A: 前往 **[Aspose.CAD 論壇](https://forum.aspose.com/c/cad/19)** 取得社群與 Aspose 工程師的協助。

**Q: 我該如何購買 Aspose.CAD for Java 的授權？**  
A: 您可以購買授權 **[購買授權](https://purchase.aspose.com/buy)**。

**Q: Aspose.CAD for Java 支援哪些單位？**  
A: Aspose.CAD for Java 同時支援公制與英制單位，會自動偵測圖紙的單位系統。

**Q: 我可以使用相同的 API 將 DWG 轉換為其他影像格式（例如 PNG、JPEG）嗎？**  
A: 當然可以。將 `PdfOptions` 替換為相應的光柵影像選項（例如 `PngOptions`），並重複使用相同的 `CadRasterizationOptions`。

## 結論

本教學示範了如何使用 **java cad library** Aspose.CAD for Java **export dwg pdf** 與光柵影像。依循步驟說明，您即可將可靠的 CAD 轉換整合至任何 Java 應用程式，無論是需要 PDF 作為文件，或光柵影像供網頁顯示。此函式庫的純 Java 特性、高品質輸出與彈性授權，使其成為小型工具與大型企業管線的理想選擇。

---

**最後更新：** 2026-10-14  
**測試環境：** Aspose.CAD for Java 24.10  
**作者：** Aspose

## 相關教學

- [使用 Aspose.CAD for Java 匯出 DWG 為 PDF：特定版面配置](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [在 Java 中匯出 DWG 為 PDF – 使用 Aspose.CAD 設定 PDF 頁面大小](/cad/java/cad-export-options/export-to-pdf/)
- [使用 Aspose.CAD for Java 匯出 DWG 為 PDF（含隱藏線）](/cad/java/cad-text-and-formatting/support-hidden-lines-in-dwg/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}