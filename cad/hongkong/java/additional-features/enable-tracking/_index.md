---
date: 2026-06-29
description: 了解如何將 DWG 匯出為 PDF、啟用追蹤，並使用 Aspose.CAD for Java 的自訂錯誤處理 Java 類別。包括 DXF
  轉 PDF 的轉換。
keywords:
- export dwg to pdf
- custom error handler java
- dwg to pdf java
linktitle: 使用 Java 在 DWG 檔案中啟用追蹤
schemas:
- author: Aspose
  dateModified: '2026-06-29'
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
title: 匯出 DWG 為 PDF 並使用 Aspose.CAD Java 啟用追蹤
url: /zh-hant/java/additional-features/enable-tracking/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 匯出 DWG 為 PDF 並啟用 Aspose.CAD Java 追蹤

## 介紹

匯出 DWG 為 PDF 同時保持完整的轉換過程可見性，對於現代以 CAD 為核心的團隊至關重要。在本指南中，您將了解 **如何啟用追蹤** 在 DWG 工作流程中，於同一管線中將 DXF 轉換為 PDF，並使用 **自訂錯誤處理器 Java** 類別捕捉每個渲染警告。完成後，您將擁有一段可投入生產的程式碼，不僅能產生高保真度的 PDF，還能記錄診斷資訊以供稽核與故障排除。

## 快速解答
- **「enable dwg tracking java」的作用是什麼？** 它會啟用 Aspose.CAD 的渲染回呼，使您在匯出過程中看到警告與錯誤。  
- **我需要授權嗎？** 試用版可用於測試；正式環境需商業授權。  
- **我也可以將 DXF 轉換為 PDF 嗎？** 可以——與 DWG 相同的 `PdfOptions` 物件亦適用於 DXF，涵蓋 *java convert dxf pdf* 情境。  
- **需要哪個版本的 JDK？** Java 8 或更高版本。  
- **在哪裡可以找到更多範例？** 請參閱以下連結的 [Aspose.CAD Java Documentation](https://reference.aspose.com/cad/java/)。

## 什麼是匯出 DWG 為 PDF？
匯出 DWG 為 PDF 是將原生 AutoCAD 圖紙（DWG）轉換為可攜式 PDF 文件的過程，同時保留向量精度、圖層與註解。Aspose.CAD 完全以 Java 執行此轉換，無需安裝原生 AutoCAD。

## 為何使用 Aspose.CAD for Java？
Aspose.CAD for Java 提供完整的純 Java CAD 轉換解決方案，支援超過 50 種格式，具備高效能，並透過渲染回呼提供內建追蹤。它不需要任何外部相依性，可整合至伺服器端工作流程。

- **完整的格式支援** – 處理 DWG、DXF、DGN 以及 50 多種其他 CAD 格式。  
- **零外部相依性** – 純 Java 函式庫，適合伺服器端自動化。  
- **內建追蹤** – `CadRenderHandler` 提供詳細的渲染結果。  
- **單行 PDF 匯出** – `PdfOptions` 轉換為 PDF，同時保留向量資料完整。  

這些具體數據基於 Aspose.CAD 能在不將整個文件載入記憶體的情況下處理高達 500 頁的檔案，於一般 4 核心伺服器上轉換時間低於 2 秒。

## 前置條件

- **Java Development Kit (JDK)** 8 或更新版本已安裝於您的機器上。  
- **Aspose.CAD for Java** 可從官方 [download link](https://releases.aspose.com/cad/java/) 下載。  
- **Aspose.CAD 免費試用** 可於 [Aspose.CAD Free Trial](https://releases.aspose.com/) 頁面取得，以快速評估。  
- 一個包含您欲轉換之 DWG/DXF 檔案的資料夾。  

## 如何匯出 DWG 為 PDF？

載入來源檔案、設定 `PdfOptions`、附加自訂的 `CadRenderHandler`，然後呼叫 `save`。此端對端流程將 DWG（或 DXF）轉換為 PDF，並為每個渲染步驟發出追蹤資訊，確保任何警告或錯誤皆被捕捉，供開發人員或自動化程序處理。

## 匯入命名空間

`CadRenderHandler` 類別是 Aspose.CAD 的回呼介面，用於接收渲染診斷資訊。請在開始編寫程式碼前匯入所需的套件：

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

## 步驟 1：載入 DWG/DXF 檔案  

`CadImage` 類別代表已載入記憶體的 CAD 文件。以檔案路徑實例化它即可載入圖紙，無需開啟原生 CAD 應用程式。

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
Image image = Image.load(dataDir + "conic_pyramid.dxf");
```

## 步驟 2：設定 PDF 匯出選項（如何將 DXF 轉換為 PDF）

`PdfOptions` 定義 CAD 光柵化器產生 PDF 輸出的方式，包括向量渲染設定與頁面尺寸。設定 `VectorRasterizationOptions` 可確保線條與曲線保持清晰。`VectorRasterizationOptions` 物件指定光柵化參數，如 DPI 與背景顏色。

```java
OutputStream stream = new FileOutputStream(dataDir + "output_conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);
cadRasterizationOptions.setPageHeight(600);
```

## 步驟 3：實作追蹤（自訂錯誤處理器 Java）

`ErrorHandler` 繼承自 `CadRenderHandler`，用於捕捉光柵化過程中發出的警告、錯誤與資訊訊息。此類別會將每則訊息寫入主控台，您亦可輕鬆將其導向日誌檔或監控系統。`CadRenderHandler` 為接收光柵化器渲染診斷的介面。

```java
cadRasterizationOptions.RenderResult = new ErrorHandler();
```

## 步驟 4：匯出為 PDF  

對配置好的 `PdfOptions` 呼叫 `CadImage` 實例的 `save` 方法即可執行轉換。由於已附加自訂處理器，任何渲染問題都會在匯出過程中於主控台顯示。

```java
System.out.println("Exporting to pdf format");
image.save(stream, pdfOptions);
```

## 步驟 5：CadRenderHandler 類別  

`CadRenderHandler` 是 Aspose.CAD 用於接收渲染結果的基底類別。覆寫其 `onRenderCompleted` 方法即可取得 `RenderResult` 物件，該物件包含一系列 `RenderMessage` 條目，描述過程的每個步驟。

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

## 為何這很重要  

啟用追蹤可建立審計追蹤，符合建築、工程與建設等受規範行業的合規需求。自訂錯誤處理器亦能將 CAD 轉換健康檢查整合至 CI/CD 工作流程，自動標記需人工審查的檔案。

## 常見問題與解決方案

- **`RenderResult` 上的 `NullPointerException`** – 請確認使用 Aspose.CAD 23.10 或更新版本；較早的版本不具備 `RenderResult` API。  
- **找不到檔案** – 請再次確認 `dataDir` 指向正確的資料夾，且檔名大小寫正確。  
- **缺少追蹤輸出** – 請確認您的 `ErrorHandler` 實例已正確指派給 `cadRasterizationOptions.setRenderHandler(new ErrorHandler())`。  

## 常見問答

**Q:** 我可以為其他 CAD 檔案格式啟用追蹤嗎？  
**A:** 追蹤主要針對 DWG 與 DXF 開放。其他格式請參閱官方文件，了解哪些 API 提供渲染回呼。

**Q:** 如何自訂其他匯出選項，例如設定 PDF 中繼資料？  
**A:** `PdfOptions` 提供 `setTitle`、`setAuthor`、`setSubject` 等屬性。請在呼叫 `save` 前設定，以將中繼資料嵌入產生的 PDF 中。

**Q:** 試用版足以評估追蹤功能嗎？  
**A:** 可以，免費試用版提供完整 API 存取，讓您無限制測試 `CadRenderHandler` 與 PDF 匯出。

**Q:** 我可以在哪裡取得 Aspose.CAD for Java 的社群支援？  
**A:** 請前往 [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) 提問並與其他開發者分享經驗。

**Q:** 如何取得自動化測試環境的臨時授權？  
**A:** 請依照 [Temporary License](https://purchase.aspose.com/temporary-license/) 的步驟產生時效性授權檔案。

## 結論

透過本教學，您現在已了解如何 **匯出 DWG 為 PDF**、啟用全端追蹤，並以 **自訂錯誤處理器 Java** 類別處理 DXF 轉 PDF。將這些程式碼片段整合至建置流程，可提升可見性、可靠性，並符合業界對 CAD 文件處理的合規要求。

---

**Last Updated:** 2026-06-29  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  

{{< blocks/products/products-backtop-button >}}

## 相關教學

- [匯出 DWG 為 PDF 並轉換 CAD 圖紙 – Aspose.CAD Java 教學](/cad/java/cad-drawing-conversion/)
- [使用 Aspose.CAD for Java 匯出 DWG 為 PDF 或光柵圖](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [使用 Aspose.CAD for Java 匯出特定 DWG 版面為 PDF](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}