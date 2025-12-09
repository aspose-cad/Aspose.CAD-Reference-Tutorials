---
date: 2025-12-04
description: 了解如何使用 Aspose.CAD for Java 將 DXF 檔案匯出為 PDF、從 DXF 建立 PDF，並在 Java 中設定頁面大小，以實現精確的
  CAD 轉換。
linktitle: Export Specific DXF Layout to PDF with Java
second_title: Aspose.CAD Java API
title: 如何使用 Aspose.CAD for Java 將 DXF 版面匯出為 PDF
url: /zh-hant/java/additional-features/export-specific-layout-to-pdf/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何使用 Aspose.CAD for Java 將 DXF 版面匯出為 PDF

## 介紹

如果你是使用 CAD 圖紙的 Java 開發者，你一定知道 **如何正確匯出 dxf** 檔案對專案成敗至關重要。無論是產生工程報告、與客戶共享設計，或是自動化批次轉換，都離不開可靠的 Java PDF 轉換函式庫。本教學將示範如何使用 **Aspose.CAD for Java**，將特定的 DXF 版面匯出為 PDF，說明 **如何從 dxf 建立 pdf**、設定頁面尺寸，以及保持向量品質。

## 快速回答
- **主要使用的函式庫是什麼？** Aspose.CAD for Java，專為 CAD 設計的 Java PDF 轉換函式庫。  
- **可以選擇特定版面嗎？** 可以 – 使用 `CadRasterizationOptions.setLayouts()` 指定版面名稱。  
- **如何設定頁面大小？** 在光柵化選項中調整 `setPageWidth()` 與 `setPageHeight()`（例如 1600 × 1600）。  
- **正式環境需要授權嗎？** 生產環境必須購買商業授權，亦提供免費試用版。  
- **支援哪個 Java 版本？** 支援 Java 8 以上（JDK 1.8+）。

## 在 Java 中「如何匯出 dxf」是什麼？

將 DXF 檔案匯出即是把其向量資料轉換成其他格式（最常見為 PDF），同時保留圖層、線寬與版面資訊。Aspose.CAD 負責繁重的解析工作，讓你能專注於業務邏輯，而不必處理底層檔案解析。

## 為什麼選擇 Aspose.CAD for Java？

- **完整的 CAD 支援** – 支援 DWG、DXF、DWF 等多種格式。  
- **無外部相依** – 純 Java 實作，無需本機 DLL。  
- **精確的光柵化** – 可選向量或點陣輸出，設定 DPI、頁面大小與版面。  
- **高效能** – 為批次處理與伺服器端情境進行最佳化。

## 前置條件

開始之前，請確保已具備以下項目：

1. **Java Development Kit (JDK)** – Java 8 或更新版本。可從 [Oracle](https://www.oracle.com/java/technologies/javase-downloads.html) 下載。  
2. **Aspose.CAD for Java** – 從 [Aspose.CAD 下載頁面](https://releases.aspose.com/cad/java/) 取得最新 JAR。  
3. 任一 IDE 或建置工具（Maven/Gradle），將 Aspose.CAD JAR 加入專案的 classpath。

## 匯入命名空間

首先匯入所需的類別，這些匯入讓你能使用圖像載入、光柵化選項與 PDF 輸出設定。

```java
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

### 步驟說明

### 步驟 1：設定資源目錄

指定存放 DXF 檔案的資料夾。將佔位符替換為實際路徑。

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
```

> **小技巧：** 使用 `System.getProperty("user.dir")` 取得相對路徑，確保在不同環境下皆可正常運作。

### 步驟 2：載入 DXF 檔案

使用 `Image.load()` 載入來源 DXF，該方法會將 CAD 檔案讀取為 Aspose.CAD 的 `Image` 物件。

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile); 
```

### 步驟 3：設定光柵化選項（Set Page Size Java）

在此建立 `CadRasterizationOptions`，並定義輸出頁面大小。依需求調整寬度與高度，以符合目標 PDF 尺寸。

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);   
rasterizationOptions.setLayouts(new String[] {"Model"});
```

- `setPageWidth` / `setPageHeight` – 控制 PDF 的 **set page size java**。  
- `setLayouts` – 指定要渲染的版面；多數 DXF 檔的預設模型空間名稱為 `"Model"`。

### 步驟 4：建立 PDF 選項（Java Convert CAD PDF）

將光柵化設定關聯至 `PdfOptions` 實例，告訴 Aspose.CAD 輸出為 PDF 而非點陣圖。

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### 步驟 5：匯出 DXF 為 PDF（Create PDF from DXF）

最後，將圖像儲存為 PDF。輸出檔名以 `_layout_out_.pdf` 結尾，表示此為版面特定的轉換結果。

```java
image.save(dataDir + "conic_pyramid_layout_out_.pdf", pdfOptions);
```

執行完畢後，你會在相同目錄下看到 `conic_pyramid_layout_out_.pdf`，其中僅渲染 **Model** 版面，且尺寸已依設定調整。

## 常見問題與解決方案

| 問題 | 原因 | 解決方式 |
|------|------|----------|
| **PDF 為空白** | 版面名稱不符 | 確認 DXF 中的版面名稱（可使用 CAD 檢視器）。 |
| **頁面尺寸不正確** | `setPageWidth/Height` 未生效 | 確保在建立 `PdfOptions` 前先設定光柵化選項。 |
| **大型檔案記憶體不足** | 一次載入過大的 DXF | 使用串流方式或提升 JVM 堆積大小（`-Xmx2g`）。 |
| **缺少字型** | 文字使用的字型未安裝 | 在伺服器上安裝所需字型，或透過 `CadRasterizationOptions` 嵌入字型。 |

## 常見問答

**Q: Aspose.CAD for Java 適合新手與資深開發者嗎？**  
A: 絕對適合。API 對新手友好，同時提供深度客製化給進階使用者。

**Q: 我可以為不同版面自訂光柵化選項嗎？**  
A: 可以。依需求在每個版面上調整 `CadRasterizationOptions`（頁面大小、DPI、背景色等）。

**Q: 哪裡可以找到 Aspose.CAD for Java 的完整文件？**  
A: 詳細文件請參閱 [此處](https://reference.aspose.com/cad/java/)。

**Q: 有免費試用版嗎？**  
A: 有，請在 [此處](https://releases.aspose.com/) 下載試用版。

**Q: 如何取得 Aspose.CAD for Java 的技術支援？**  
A: 可前往支援論壇 [此處](https://forum.aspose.com/c/cad/19) 與社群或官方人員交流。

## 結論

本指南示範了 **如何匯出 dxf** 版面為 PDF，使用 Aspose.CAD for Java，涵蓋從環境建置到頁面尺寸微調的完整流程。藉由這個 **java pdf conversion library**，你可以自動化 CAD 到 PDF 的工作流程，保持向量完整性，並將無縫的 PDF 產生整合至 Java 應用程式中。

---

**最後更新：** 2025-12-04  
**測試環境：** Aspose.CAD for Java 24.12（撰寫時最新版本）  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}