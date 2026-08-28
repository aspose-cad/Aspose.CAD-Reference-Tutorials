---
date: 2026-06-14
description: 了解如何使用 Aspose.CAD for Java 將 CAD 匯出為 PDF 以及將 DGN 轉換為 PDF。為 Java 開發人員提供的逐步指南。
keywords:
- export cad to pdf
- convert dwg to pdf
- convert dgn to pdf
- java convert cad pdf
- batch convert dgn pdf
linktitle: 匯出嵌入式 DGN
schemas:
- author: Aspose
  dateModified: '2026-06-14'
  description: Learn how to export CAD to PDF and convert DGN to PDF using Aspose.CAD
    for Java. Step‑by‑step guide for Java developers.
  headline: Export CAD to PDF – Export Embedded DGN with Aspose.CAD for Java
  type: TechArticle
- description: Learn how to export CAD to PDF and convert DGN to PDF using Aspose.CAD
    for Java. Step‑by‑step guide for Java developers.
  name: Export CAD to PDF – Export Embedded DGN with Aspose.CAD for Java
  steps:
  - name: Set Up Input and Output Paths
    text: Define the directory that contains your source file and specify the DWG
      that holds the embedded DGN.
  - name: Load DWG File
    text: '`Image` loads the DWG and automatically detects any embedded DGN data,
      exposing it for further processing.'
  - name: Configure Rasterization Options
    text: Select which layout(s) you want to include in the PDF. In this example we
      export only the **Model** layout, which is the most common view for engineering
      drawings.
  - name: Configure PDF Options
    text: Attach the rasterization settings to the PDF export options so that the
      final document respects the chosen layout and DPI.
  - name: Save PDF File
    text: Finally, write the PDF to disk using the configured options. The `save`
      method writes the configured image to the target file format on disk.
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD for Java is a commercial library. You can obtain a license
      from [here](https://purchase.aspose.com/buy).
    question: Can I use Aspose.CAD for Java in a commercial project?
  - answer: Yes, you can access a free trial of Aspose.CAD for Java [here](https://releases.aspose.com/).
    question: Is there a free trial available?
  - answer: You can seek support from the Aspose.CAD community on the [forum](https://forum.aspose.com/c/cad/19).
    question: How can I get support for Aspose.CAD for Java?
  - answer: You can obtain a temporary license [here](https://purchase.aspose.com/temporary-license/).
    question: What if I need a temporary license?
  - answer: The documentation is available [here](https://reference.aspose.com/cad/java/).
    question: Where can I find the official documentation?
  type: FAQPage
second_title: Aspose.CAD Java API
title: 將 CAD 匯出為 PDF – 使用 Aspose.CAD for Java 匯出嵌入式 DGN
url: /zh-hant/java/dgn-export-options/export-embedded-dgn/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 匯出 CAD 為 PDF – 使用 Aspose.CAD for Java 匯出內嵌 DGN

## 簡介

在本教學中，您將了解 **如何將 CAD 匯出為 PDF**，方法是將內嵌的 DGN 檔案轉換為高品質的 PDF 文件，使用 Aspose.CAD for Java。  
Aspose.CAD 是一個功能強大的函式庫，為 Java 開發人員提供對 CAD 檔案操作的完整控制，無論您需要 **將 DGN 轉換為 PDF**、**將 DWG 轉換為 PDF**，或僅僅將 CAD 圖面渲染為其他格式。  
請依照以下逐步指南操作，您即可在數分鐘內將此功能整合至您的應用程式中。

## 快速解答
- **「export CAD to PDF」是什麼意思？** 它將 CAD 圖面（如 DWG、DGN 等）轉換為 PDF 檔案，同時保留向量品質。  
- **使用哪個函式庫？** Aspose.CAD for Java。  
- **需要授權嗎？** 正式環境需要授權；可使用免費試用版。  
- **主要前置條件是什麼？** Java 開發環境以及 Aspose.CAD for Java 的 JAR 檔案。  
- **可以自訂輸出嗎？** 可以 — 您可以選擇版面配置、設定光柵化選項，並控制 PDF 設定。

## 什麼是「export CAD to PDF」？

Export CAD to PDF 會將原生 CAD 圖面（DWG、DGN 等）轉換為 PDF 檔案，保留原始的向量幾何、圖層與版面配置，使任何人即使沒有 CAD 軟體也能檢視、列印或分享設計。此轉換產生的文件與平台無關，於任何縮放層級皆保持相同外觀，十分適合協作與存檔。

## 為什麼使用 Aspose.CAD for Java 來將 DGN 轉換為 PDF？

Aspose.CAD for Java 提供純 Java 解決方案，免除外部 CAD 工具的需求，確保產生的 PDF 在向量精度上完全一致，並提供廣泛的設定選項，如版面選擇、DPI 控制與字型嵌入，適用於簡單或企業級的轉換任務。

- **無外部相依性** – 完全以 Java 執行，支援任何作業系統。  
- **保留向量資料** – PDF 在任何縮放層級皆保持清晰。  
- **細緻的控制** – 可選擇特定版面、設定光柵化 DPI，並嵌入字型。  
- **企業級支援** – 支援最高 **2 GB** 的檔案，批次處理上千張圖面，且授權彈性。  

## 前置條件

在開始之前，請確保您已具備以下項目：

- **Java 開發環境** – 已安裝並設定 JDK 8 或以上版本。  
- **Aspose.CAD for Java** – 從 [here](https://releases.aspose.com/cad/java/) 下載最新的 JAR 檔案。  

## 匯入套件

`import` 陳述式將所需的 Aspose.CAD 類別匯入作用域。  
`Image` 是代表任何可光柵化 CAD 檔案的核心類別，而 `PdfOptions` 與 `RasterizationOptions` 讓您微調 PDF 輸出。  
`CadRasterizationOptions` 指定光柵化參數，如 DPI、頁面尺寸與版面配置，用於 CAD 渲染。

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## 如何使用 Aspose.CAD for Java 匯出 CAD 為 PDF？

此流程先載入包含內嵌 DGN 的 DWG 檔案，接著設定光柵化參數以定義輸出解析度與版面配置，將這些參數附加至 PdfOptions 物件，最後呼叫 save 方法產生 PDF。此方法以最少的程式碼即可確保高品質、保留向量的結果。  

以下是一個清晰的編號步驟說明，展示如何將內嵌於 DWG 中的 DGN 檔案轉換為 PDF。

### 步驟 1：設定輸入與輸出路徑

定義包含來源檔案的目錄，並指定含有內嵌 DGN 的 DWG 檔案。

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
```

### 步驟 2：載入 DWG 檔案

`Image` 載入 DWG，並自動偵測任何內嵌的 DGN 資料，供後續處理使用。

```java
Image objImage = Image.load(fileName);
```

### 步驟 3：設定光柵化選項

選擇要包含於 PDF 的版面配置。本範例僅匯出 **Model** 版面，這是工程圖最常見的視圖。

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setLayouts(new String[] {"Model"});
```

### 步驟 4：設定 PDF 選項

將光柵化設定附加至 PDF 匯出選項，使最終文件遵循所選的版面與 DPI。

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### 步驟 5：儲存 PDF 檔案

最後，使用已設定的選項將 PDF 寫入磁碟。`save` 方法會將設定好的影像寫入目標檔案格式。

```java
objImage.save(dataDir + "BlockRefDgn.pdf", pdfOptions);
```

## 將 DWG 轉換為 PDF – 其他提示

如果您的來源檔案是純 DWG（未內嵌 DGN），您可以重複使用相同程式碼——只需將 `fileName` 改為指向要轉換的 DWG。光柵化與 PDF 選項保持相同，為您提供一致的 **convert DWG to PDF** 工作流程。

## 常見問題與解決方案

| 問題 | 原因 | 解決方案 |
|-------|--------|----------|
| **PDF 輸出空白** | 版面名稱不匹配 | 確認傳遞給 `setLayouts` 的版面名稱與來源檔案中的版面名稱完全相同（區分大小寫）。 |
| **授權例外** | 使用試用版卻未提供授權 | 在載入影像前套用有效的 Aspose.CAD 授權 (`License license = new License(); license.setLicense("Aspose.CAD.lic");`). |
| **找不到檔案** | `dataDir` 路徑不正確 | 使用絕對路徑，或確保相對路徑相對於專案的工作目錄正確。 |
| **低解析度圖形** | 預設光柵化 DPI 較低 | 設定 `rasterizationOptions.setResolution(300)` 或調整 `setPageWidth/Height` 以提升 DPI。 |

## 常見問答

**Q: 我可以在商業專案中使用 Aspose.CAD for Java 嗎？**  
A: 是的，Aspose.CAD for Java 為商業函式庫。您可從 [here](https://purchase.aspose.com/buy) 取得授權。

**Q: 是否提供免費試用？**  
A: 是的，您可在 [here](https://releases.aspose.com/) 取得 Aspose.CAD for Java 的免費試用版。

**Q: 如何取得 Aspose.CAD for Java 的支援？**  
A: 您可在 Aspose.CAD 社群的 [forum](https://forum.aspose.com/c/cad/19) 尋求協助。

**Q: 若需要臨時授權該怎麼辦？**  
A: 您可在 [here](https://purchase.aspose.com/temporary-license/) 取得臨時授權。

**Q: 官方文件在哪裡可以找到？**  
A: 文件可於 [here](https://reference.aspose.com/cad/java/) 取得。

## 結論

您現在已學會如何 **匯出 CAD 為 PDF**，特別是使用 Aspose.CAD for Java **將 DGN 轉換為 PDF**，甚至 **將 DWG 轉換為 PDF**。依照上述步驟，您即可將無縫的 CAD 轉 PDF 功能整合至任何基於 Java 的解決方案，為使用者提供高品質的 PDF，且無需額外的 CAD 軟體。

---

**最後更新：** 2026-06-14  
**測試環境：** Aspose.CAD for Java 24.12  
**作者：** Aspose

{{< blocks/products/products-backtop-button >}}

## 相關教學

- [使用 Aspose.CAD for Java 匯出 DGN 為 DWG – 教學](/cad/java/dgn-export-options/)
- [使用 Aspose.CAD for Java 輕鬆將 DGN 匯出為 AutoCAD PDF](/cad/java/dgn-export-options/exporting-dgn-to-pdf/)
- [dwg 轉 pdf java – 使用 Aspose.CAD 匯出 CAD 為 PDF](/cad/java/cad-export-options/export-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}