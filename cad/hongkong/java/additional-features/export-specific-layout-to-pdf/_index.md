---
date: 2026-02-04
description: 學習如何使用 Aspose.CAD for Java 從 DXF 建立 PDF、將 DXF 匯出為 PDF、設定 PDF 頁寬，並以精確控制產生
  CAD PDF。
linktitle: Export Specific DXF Layout to PDF with Java
second_title: Aspose.CAD Java API
title: 使用 Aspose.CAD for Java 從 DXF 版面建立 PDF
url: /zh-hant/java/additional-features/export-specific-layout-to-pdf/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.CAD for Java 從 dxf 版面建立 PDF

## 介紹

如果你是使用 CAD 圖面的 Java 開發人員，你一定知道 **如何正確匯出 dxf** 檔案對專案成敗關鍵重大。無論是產生工程報告、與客戶分享設計，或是自動化批次轉換，都離不開可靠的 Java PDF 轉換函式庫。本教學將手把手示範 **從 dxf 版面建立 pdf**，說明如何控制頁面尺寸，並在 **Aspose.CAD for Java** 中保持向量品質。

## 快速答覆
- **主要使用的函式庫是什麼？** Aspose.CAD for Java，專為 CAD 的 Java PDF 轉換而設計。
- **可以選擇特定版面嗎？** 可以 – 使用 `CadRasterizationOptions.setLayouts()` 來指定版面名稱。
- **如何設定頁面大小？** 在光柵化選項中調整 `setPageWidth()` 與 `setPageHeight()`（例如 1600 × 1600）。
- **正式環境需要授權嗎？** 生產環境必須使用商業授權；亦提供免費試用版。
- **支援哪個 Java 版本？** 支援 Java 8 以上（JDK 1.8+）。

## 如何從 dxf 版面建立 pdf？

匯出 DXF 檔案即是將其向量資料轉換為其他格式（最常見為 PDF），同時保留圖層、線寬與版面資訊。Aspose.CAD 負責繁重的處理工作，讓你只需專注於業務邏輯，而不必關心底層檔案解析。

## 為什麼選擇 Aspose.CAD for Java？

- **完整的 CAD 支援** – 支援 DWG、DXF、DWF 等多種格式。
- **無外部相依** – 純 Java 實作，無需本機 DLL。
- **精確的光柵化** – 可選向量或光柵輸出，設定 DPI、頁面大小與版面。
- **高效能** – 為批次處理與伺服器端情境優化。
- **只需一行程式碼即可 export dxf to pdf**，非常適合 **java convert cad pdf** 工作流程。

## 前置條件

在開始之前，請確保已具備以下項目：

1. **Java Development Kit (JDK)** – Java 8 或更新版本。可從 [Oracle](https://www.oracle.com/java/technologies/javase-downloads.html) 下載。
2. **Aspose.CAD for Java** – 從 [Aspose.CAD 下載頁面](https://releases.aspose.com/cad/java/) 取得最新 JAR。
3. 具備 IDE 或建置工具（Maven/Gradle），以將 Aspose.CAD JAR 加入專案 classpath。

## 匯入命名空間

首先匯入所需的類別。這些匯入讓你能使用圖像載入、光柵化選項與 PDF 輸出設定。

```java
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## 步驟說明

### 步驟 1：設定資源目錄

定義存放 DXF 檔案的資料夾。將佔位符替換為實際路徑。

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
```

> **小技巧：** 使用 `System.getProperty("user.dir")` 建立相對路徑，可在不同環境間保持一致。

### 步驟 2：載入 DXF 檔案

使用 `Image.load()` 載入來源 DXF。此方法會將 CAD 檔案讀入 Aspose.CAD 的 `Image` 物件。

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile); 
```

### 步驟 3：設定光柵化選項（在 Java 中設定 PDF 頁寬）

在此建立 `CadRasterizationOptions` 並定義輸出頁面大小。依需求調整寬度與高度，以符合目標 PDF 尺寸。

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);   
rasterizationOptions.setLayouts(new String[] {"Model"});
```

- `setPageWidth` / `setPageHeight` – 控制 **set pdf page width**（以及高度）以產生 PDF。
- `setLayouts` – 指定要渲染的版面；多數 DXF 檔的預設模型空間名稱為 `"Model"`。

### 步驟 4：建立 PDF 選項（Java Convert CAD PDF）

將光柵化設定連結至 `PdfOptions` 實例。這告訴 Aspose.CAD 輸出 PDF 而非光柵圖像。

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### 步驟 5：匯出 DXF 為 PDF（Create PDF from DXF）

最後，將圖像儲存為 PDF。輸出檔名以 `_layout_out_.pdf` 結尾，表示此為版面專屬的轉換結果。

```java
image.save(dataDir + "conic_pyramid_layout_out_.pdf", pdfOptions);
```

執行完畢後，你會在相同目錄中看到 `conic_pyramid_layout_out_.pdf`，其中僅渲染 **Model** 版面，且尺寸已依設定調整。

## 常見使用情境

| 情境 | 為何此方法有幫助 |
|----------|-----------------------|
| **自動化報告產生** | 確保每張圖都有相同頁面大小，批次 PDF 版面保持一致。 |
| **客戶設計預覽** | 匯出單一版面（例如 “Model” 或 “Sheet1”）可減少檔案大小，同時保留向量精度。 |
| **舊版 DWG 轉 PDF** | 雖然本例使用 DXF，相同 API 也能 **convert dwg to pdf**，只需少量程式碼變更。 |
| **在 Web 入口嵌入 CAD 圖** | 產生的 PDF 可直接串流至瀏覽器，無需額外轉換工具。 |

## 常見問題與解決方案

| 問題 | 原因 | 解決方式 |
|-------|--------|-----|
| **PDF 為空白** | 版面名稱不符 | 確認 DXF 中的版面名稱（可使用 CAD 檢視器檢查）。 |
| **頁面尺寸不正確** | `setPageWidth/Height` 未生效 | 確保在建立 `PdfOptions` 前先設定光柵化選項。 |
| **大型檔案記憶體不足** | DXF 載入時佔用過多記憶體 | 使用串流或提升 JVM 堆積大小（`-Xmx2g`）。 |
| **缺少字型** | 文字使用的字型未安裝 | 在伺服器上安裝所需字型，或透過 `CadRasterizationOptions` 嵌入字型。 |
| **需要匯出多個版面** | 只呼叫單一版面 | 使用 `setLayouts` 傳入版面名稱陣列，並為每個版面重複 `save` 步驟。 |

## 常見問答

**Q: Aspose.CAD for Java 是否適合新手與資深開發者？**  
A: 絕對適合。API 對新手友好，同時提供深度客製化給進階使用者。

**Q: 可以為不同版面自訂光柵化選項嗎？**  
A: 可以。依需求在每個版面調整 `CadRasterizationOptions`（頁面大小、DPI、背景色）即可。

**Q: 哪裡可以找到 Aspose.CAD for Java 的完整文件？**  
A: 詳細文件請參考 [here](https://reference.aspose.com/cad/java/)。

**Q: 有免費試用版嗎？**  
A: 有，請在 [here](https://releases.aspose.com/) 下載試用版本。

**Q: 如何取得 Aspose.CAD for Java 的支援？**  
A: 前往支援論壇 [here](https://forum.aspose.com/c/cad/19) 與社群或官方人員交流。

## 結論

本指南示範了 **如何使用 Aspose.CAD for Java 從 dxf 版面建立 PDF**，涵蓋環境設定到頁面尺寸微調的完整流程。藉由這個 **java pdf conversion library**，你可以自動化 CAD 到 PDF 的工作流程，保持向量完整性，並將 PDF 產生無縫整合至 Java 應用程式。無論是 **export dxf to pdf**、**convert dwg to pdf**，或是 **generate pdf from cad**，上述步驟都提供了堅實的基礎。

---

**最後更新：** 2026-02-04  
**測試環境：** Aspose.CAD for Java 24.12（撰寫時最新版本）  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}