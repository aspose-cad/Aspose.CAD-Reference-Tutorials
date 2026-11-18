---
date: 2026-11-18
description: 了解如何使用 Aspose.CAD for Java 匯出 DWG 為 PDF、啟用追蹤，並使用 custom error handler
  Java 類別。亦包含 DXF‑to‑PDF 轉換功能。
keywords:
- export dwg to pdf
- custom error handler java
- dwg to pdf java
lastmod: 2026-11-18
linktitle: 使用 Java 為 DWG 檔案啟用追蹤
og_description: 使用 Aspose.CAD for Java 匯出 DWG 為 PDF 並在 Java 中啟用完整追蹤。了解如何使用 custom
  error handler、將 DXF 轉換為 PDF，以及記錄 render warnings。
og_image_alt: Guide showing DWG to PDF conversion and tracking in Java with Aspose.CAD
og_title: 使用 Aspose.CAD for Java 匯出 DWG 為 PDF 並啟用追蹤
schemas:
- author: Aspose
  dateModified: '2026-11-18'
  description: Learn how to export DWG to PDF, enable tracking, and use a custom error
    handler Java class with Aspose.CAD for Java. Includes DXF‑to‑PDF conversion.
  headline: Export DWG to PDF and Enable Tracking with Aspose.CAD Java
  type: TechArticle
- questions:
  - answer: It activates Aspose.CAD’s render callbacks so you can see warnings and
      errors during export.
    question: What does “enable dwg tracking java” do?
  - answer: A trial works for testing; a commercial license is required for production
      use.
    question: Do I need a license?
  - answer: Yes – the same `PdfOptions` object used for DWG works for DXF, covering
      the *java convert dxf pdf* scenario.
    question: Can I also convert DXF to PDF?
  - answer: Java 8 or higher.
    question: Which JDK version is required?
  - answer: See the [Aspose.CAD Java Documentation](https://reference.aspose.com/cad/java/)
      linked below.
    question: Where can I find more examples?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- export dwg to pdf
- aspose.cad java
- custom error handler
- dxf to pdf
- java cad conversion
title: 使用 Aspose.CAD for Java 匯出 DWG 為 PDF 並啟用追蹤
url: /zh-hant/java/additional-features/enable-tracking/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 匯出 DWG 為 PDF 並啟用 Aspose.CAD Java 追蹤

## 介紹

匯出 DWG 為 PDF 同時保持對轉換過程的完整可見性，對於現代以 CAD 為核心的團隊至關重要。在本指南中，您將了解 **如何啟用追蹤** 在 DWG 工作流程中，於同一管線中將 DXF 轉換為 PDF，並使用 **自訂錯誤處理程式 Java** 類別捕獲每個渲染警告。完成後，您將擁有一段可直接投入生產的程式碼，不僅能產生高保真 PDF，還能記錄診斷資訊以供稽核與除錯。

## 快速解答
- **「enable dwg tracking java」的作用是什麼？** 它會啟動 Aspose.CAD 的渲染回呼，以便在匯出過程中看到警告和錯誤。  
- **我需要授權嗎？** 試用版可用於測試；正式環境需購買商業授權。  
- **我也可以將 DXF 轉換為 PDF 嗎？** 可以 — 用於 DWG 的相同 `PdfOptions` 物件亦適用於 DXF，涵蓋 *java convert dxf pdf* 情境。  
- **需要哪個版本的 JDK？** Java 8 或更高版本。  
- **在哪裡可以找到更多範例？** 請參閱下方連結的 [Aspose.CAD Java 文件說明](https://reference.aspose.com/cad/java/)。

## 什麼是匯出 DWG 為 PDF？

Export DWG to PDF 是將原生 AutoCAD 繪圖 (DWG) 轉換為可攜式 PDF 文件的過程，同時保留向量精度、圖層與註解。 **Aspose.CAD 以純 Java 方式將 DWG 轉換為 PDF，您永遠不需要授權的 AutoCAD 安裝。** 此轉換保留精確的線寬、文字樣式與版面幾何，使 PDF 適合客戶審閱、存檔或後續處理。

## 為什麼使用 Aspose.CAD for Java？

Aspose.CAD for Java 提供完整的純 Java CAD 轉換解決方案，支援超過 50 種格式，具備高效能，並透過渲染回呼提供內建追蹤。它不需任何外部相依，可整合至伺服器端管線。此函式庫亦具記憶體效能優化，可在不將整個文件載入 RAM 的情況下，處理多達 500 頁的檔案轉換。

## 前置條件

- **Java Development Kit (JDK)** 8 或更新版本已安裝於您的機器上。  
- **Aspose.CAD for Java** 從官方的 [下載連結](https://releases.aspose.com/cad/java/) 下載。  
- **Aspose.CAD 免費試用** 可從 [Aspose.CAD 免費試用](https://releases.aspose.com/) 頁面取得，若您需要快速評估。  
- 一個資料夾，內含您想要轉換的 DWG/DXF 檔案。  

## 如何匯出 DWG 為 PDF？

載入來源檔案，設定 `PdfOptions`，附加自訂的 `CadRenderHandler`，然後呼叫 `save`。此端對端流程會將 DWG（或 DXF）轉換為 PDF，同時為每個渲染步驟發出追蹤資訊，確保任何警告或錯誤皆被捕獲，並可供開發人員或自動化流程處理。

## 匯入命名空間

`CadRenderHandler` 介面在轉換期間接收渲染診斷資訊，例如警告與錯誤。  
```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.CadRenderResult;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.RenderResult;
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
```

## 步驟 1：載入 dwg/dxf 檔案  

`CadImage` 代表已載入記憶體的 CAD 繪圖，提供對其頁面與圖層的存取。  
```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
Image image = Image.load(dataDir + "conic_pyramid.dxf");
```

## 步驟 2：設定 PDF 匯出選項（如何將 dxf 轉換為 pdf）

`PdfOptions` 定義 PDF 輸出設定，而 `VectorRasterizationOptions` 控制光柵化參數，如 DPI 與背景顏色。  
```java
OutputStream stream = new FileOutputStream(dataDir + "output_conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);
cadRasterizationOptions.setPageHeight(600);
```

## 步驟 3：實作追蹤（custom error handler java）

`ErrorHandler` 繼承自 `CadRenderHandler`，用以捕獲並記錄轉換過程中發出的渲染訊息。  
```java
cadRasterizationOptions.RenderResult = new ErrorHandler();
```

## 步驟 4：匯出為 pdf  

呼叫 `CadImage` 實例的 `save` 方法，將渲染完成的 PDF 寫入指定的輸出路徑。  
```java
System.out.println("Exporting to pdf format");
image.save(stream, pdfOptions);
```

## 步驟 5：cadrenderhandler 類別  

`CadRenderHandler` 是基礎回呼類別，會在渲染完成後接收包含詳細訊息的 `RenderResult`。  
```java
public static class ErrorHandler extends CadRasterizationOptions.CadRenderHandler {
    @Override
    public void invoke(CadRenderResult result) {
        System.out.println("Tracking results of exporting");

        if (result.isRenderComplete())
            return;

        System.out.println("Have some problems:");

        int idxError = 1;
        for (RenderResult rr : result.getFailures()) {
            System.out.printf("{0}. {1}, {2}", idxError, rr.getRenderCode(), rr.getMessage());
            idxError++;
        }
    }
}
```

## 為什麼這很重要

啟用追蹤可建立稽核追蹤，滿足建築、工程與建設等受規範行業的合規需求。自訂錯誤處理程式亦讓您能將 CAD 轉換健康檢查整合至 CI/CD 管線，自動標記需人工審查的檔案。

## 常見問題與解決方案

- **`NullPointerException` on `RenderResult`** – 請確保使用 Aspose.CAD 23.10 或更新版本；較早的版本缺少 `RenderResult` API。  
- **File not found** – 請再次確認 `dataDir` 指向正確的資料夾，且檔名大小寫正確匹配。  
- **Missing tracking output** – 請確認您的 `ErrorHandler` 實例已正確指派給 `cadRasterizationOptions.setRenderHandler(new ErrorHandler())`。  

## 常見問答

**Q:** 我也可以將 DXF 轉換為 PDF 嗎？  
**A:** 可以 — 用於 DWG 的相同 `PdfOptions` 物件亦適用於 DXF，涵蓋 *java convert dxf pdf* 情境。

**Q:** 我可以為其他 CAD 檔案格式啟用追蹤嗎？  
**A:** 追蹤主要針對 DWG 與 DXF 開放。對於其他格式，請參閱官方文件以了解哪些 API 提供渲染回呼。

**Q:** 如何自訂其他匯出選項，例如設定 PDF 中繼資料？  
**A:** `PdfOptions` 提供 `setTitle`、`setAuthor`、`setSubject` 等屬性。於呼叫 `save` 前設定這些屬性，即可將中繼資料嵌入產生的 PDF。

**Q:** 試用版足以評估追蹤功能嗎？  
**A:** 是的，免費試用版包含完整 API 存取，讓您無限制測試 `CadRenderHandler` 與 PDF 匯出。

**Q:** 哪裡可以取得 Aspose.CAD for Java 的社群支援？  
**A:** 前往 [Aspose.CAD 論壇](https://forum.aspose.com/c/cad/19) 提問，與其他開發者分享經驗。

**Q:** 如何取得臨時授權以供自動化測試環境使用？  
**A:** 請依照 [臨時授權](https://purchase.aspose.com/temporary-license/) 的步驟產生時效性授權檔案。

## 結論

透過本教學，您現在已了解如何 **匯出 DWG 為 PDF**、啟用全端追蹤，並以 **自訂錯誤處理程式 Java** 類別處理 DXF‑to‑PDF 轉換。將這些程式碼片段整合至建置管線，可提升可見性、改善可靠性，並符合 CAD 文件處理的產業級合規要求。

**最後更新：** 2026-11-18  
**測試環境：** Aspose.CAD for Java 24.12  
**作者：** Aspose  

## 相關教學

- [匯出 DWG 為 PDF 並轉換 CAD 圖紙 – Aspose.CAD Java 教學](/cad/java/cad-drawing-conversion/)
- [使用 Aspose.CAD for Java 匯出 DWG 為 PDF 或光柵圖](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [使用 Aspose.CAD for Java 匯出特定 DWG 版面為 PDF](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}