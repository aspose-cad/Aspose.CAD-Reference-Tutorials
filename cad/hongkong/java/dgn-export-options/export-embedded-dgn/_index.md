---
date: 2026-01-07
description: 學習如何使用 Aspose.CAD for Java 將 CAD 匯出為 PDF，並將 DGN 轉換為 PDF。為 Java 開發人員提供的逐步指南。
linktitle: Export Embedded DGN
second_title: Aspose.CAD Java API
title: 將 CAD 匯出為 PDF – 使用 Aspose.CAD for Java 匯出嵌入式 DGN
url: /zh-hant/java/dgn-export-options/export-embedded-dgn/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 匯出 CAD 為 PDF – 使用 Aspose.CAD for Java 匯出內嵌 DGN

## 介紹

在本教學中，您將學會 **如何匯出 CAD 為 PDF**，透過將內嵌的 DGN 檔案轉換為高品質的 PDF 文件，使用 Aspose.CAD for Java。Aspose.CAD 是一套功能強大的函式庫，讓 Java 開發者能完整掌控 CAD 檔案的操作，無論您需要 **將 DGN 轉換為 PDF**、**將 DWG 轉換為 PDF**，或僅是將 CAD 圖面渲染為其他格式。依照以下步驟說明操作，即可在數分鐘內將此功能整合至您的應用程式。

## 快速回答
- **「匯出 CAD 為 PDF」是什麼意思？** 會將 CAD 圖面（DWG、DGN 等）轉換為 PDF 檔，同時保留向量品質。  
- **使用哪個函式庫？** Aspose.CAD for Java。  
- **需要授權嗎？** 正式環境必須使用授權，提供免費試用版。  
- **主要前置條件是什麼？** Java 開發環境與 Aspose.CAD for Java JAR。  
- **可以自訂輸出嗎？** 可以 – 您可以選擇版面、設定光柵化選項，並控制 PDF 參數。

## 什麼是「匯出 CAD 為 PDF」？
匯出 CAD 為 PDF 意指將原生 CAD 檔案（如 DWG 或 DGN）產生一個 PDF 文件，忠實呈現原始幾何圖形。PDF 可在任何平台上開啟，無需 CAD 軟體，非常適合分享、列印或保存。

## 為什麼使用 Aspose.CAD for Java 轉換 DGN 為 PDF？
- **無外部相依** – 完全在 Java 中執行。  
- **保留向量資料** – PDF 在任何縮放層級下皆保持清晰。  
- **細緻控制** – 可選擇特定版面、設定光柵化 DPI，並嵌入字型。  
- **企業級支援** – 支援大型檔案、批次處理與授權選項。

## 前置條件

在開始之前，請確保您已具備以下環境：

- **Java 開發環境** – 已安裝並設定 JDK 8 或以上版本。  
- **Aspose.CAD for Java** – 從 [此處](https://releases.aspose.com/cad/java/) 下載最新 JAR。

## 匯入套件

要開始使用，請在 Java 專案中匯入必要的類別。將以下 import 陳述加入您的原始檔案：

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

## 如何使用 Aspose.CAD for Java 匯出 DGN 為 PDF？

以下提供一個清晰、編號的步驟說明，示範如何將嵌入於 DWG 中的 DGN 檔案轉換為 PDF。

### 步驟 1：設定輸入與輸出路徑

定義包含來源檔案的目錄，並指定保存內嵌 DGN 的 DWG 檔案。

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
```

### 步驟 2：載入 DWG 檔案

將 DWG 檔案載入為 `Image` 物件。Aspose.CAD 會自動偵測內嵌的 DGN 資料。

```java
Image objImage = Image.load(fileName);
```

### 步驟 3：設定光柵化選項

選擇要匯入 PDF 的版面。本範例僅匯出 **Model** 版面。

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setLayouts(new String[] {"Model"});
```

### 步驟 4：設定 PDF 選項

將光柵化設定套用至 PDF 匯出選項。

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### 步驟 5：儲存 PDF 檔案

最後，使用先前設定的選項將 PDF 寫入磁碟。

```java
objImage.save(dataDir + "BlockRefDgn.pdf", pdfOptions);
```

## 轉換 DWG 為 PDF – 其他小技巧

如果您的來源檔案是純 DWG（未嵌入 DGN），只要將 `fileName` 改為目標 DWG 檔即可重複使用相同程式碼。光柵化與 PDF 設定保持不變，提供一致的 **將 DWG 轉換為 PDF** 工作流程。

## 常見問題與解決方案

| 問題 | 原因 | 解決方式 |
|------|------|----------|
| **PDF 輸出為空白** | 版面名稱不符 | 確認傳入 `setLayouts` 的版面名稱與來源檔案中的版面名稱完全相同（區分大小寫）。 |
| **授權例外** | 使用試用版未設定授權 | 在載入圖像前套用有效的 Aspose.CAD 授權 (`License license = new License(); license.setLicense("Aspose.CAD.lic");`)。 |
| **找不到檔案 | `dataDir` 路徑錯誤 | 使用絕對路徑或確認相對路徑相對於專案工作目錄正確。 |
| **圖形解析度低** | 預設光柵化 DPI 較低 | 設定 `rasterizationOptions.setPageWidth/Height` 或 `setResolution` 以提升 DPI。 |

## 常見問答

**Q: 可以在商業專案中使用 Aspose.CAD for Java 嗎？**  
A: 可以，Aspose.CAD for Java 為商業授權函式庫。您可從 [此處](https://purchase.aspose.com/buy) 取得授權。

**Q: 有提供免費試用嗎？**  
A: 有，您可在 [此處](https://releases.aspose.com/) 取得 Aspose.CAD for Java 的免費試用版。

**Q: 如何取得 Aspose.CAD for Java 的技術支援？**  
A: 可於 Aspose.CAD 社群的 [論壇](https://forum.aspose.com/c/cad/19) 尋求協助。

**Q: 若需要臨時授權該怎麼辦？**  
A: 您可在 [此處](https://purchase.aspose.com/temporary-license/) 取得臨時授權。

**Q: 文件說明在哪裡可以找到？**  
A: 文件說明位於 [此處](https://reference.aspose.com/cad/java/)。

## 結論

您現在已掌握 **匯出 CAD 為 PDF** 的完整流程，包含 **將 DGN 轉換為 PDF** 以及 **將 DWG 轉換為 PDF**，皆透過 Aspose.CAD for Java 完成。依照上述步驟，即可將無縫的 CAD 轉 PDF 功能整合至任何 Java 解決方案，為使用者提供高品質的 PDF，且無需額外的 CAD 軟體。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**最後更新：** 2026-01-07  
**測試版本：** Aspose.CAD for Java 24.12  
**作者：** Aspose