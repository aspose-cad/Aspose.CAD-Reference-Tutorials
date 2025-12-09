---
date: 2025-12-09
description: 學習如何使用 Aspose.CAD for Java 從 DWG 檔案建立 PDF。輕鬆將 DWG 轉換為 PDF，支援網格。
linktitle: Mesh Support in CAD
second_title: Aspose.CAD Java API
title: 使用 Aspose.CAD for Java 從 DWG 產生 PDF
url: /zh-hant/java/advanced-cad-features/mesh-support-in-cad/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.CAD for Java 從 DWG 建立 PDF

## 介紹

在本教學中，您將學習 **從 DWG 建立 PDF** 檔案，使用 Aspose.CAD for Java。該函式庫的網格支援可讓您直接將複雜的 CAD 圖紙（包括含有 3‑D 網格的圖紙）轉換為 PDF，且不會遺失細節。無論您是為了報告、歸檔或後續處理而需要 **將 DWG 轉換為 PDF**，以下步驟都會為您提供可靠、可投入生產的解決方案。

## 快速回答
- **本教學涵蓋什麼內容？** 使用 Aspose.CAD for Java 將包含網格的 DWG 檔案轉換為 PDF。  
- **我需要授權嗎？** 臨時授權可用於測試；商業使用則需正式授權。  
- **支援哪個 Java 版本？** Java 8 或更新版本。  
- **我可以匯出其他格式嗎？** 可以 – Aspose.CAD 亦支援 PNG、JPEG、BMP 等格式。  
- **轉換需要多久？** 標準尺寸圖紙通常在一秒內完成。

## 如何從 DWG 建立 PDF？

以下提供簡潔的逐步指南，帶您完成整個流程——從專案設定到最終 PDF 的儲存。

## 前置條件

- **Java 開發環境：** 已在機器上安裝 JDK 8 或更新版本。  
- **Aspose.CAD for Java 函式庫：** 從 [download link](https://releases.aspose.com/cad/java/) 下載最新的 JAR。  
- **含有網格的文件：** 包含網格資料的 DWG 檔案（例如 `meshes.dwg`）。  

## 匯入命名空間

在您的 Java 原始碼檔案中，加入所需的 Aspose.CAD 類別：

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## 步驟 1：設定專案

建立一個新的 Java 專案（或在現有專案中加入），並將 Aspose.CAD JAR 加入專案的 classpath。定義一個基礎目錄，用於存放來源 DWG 檔案與產生的 PDF。

## 步驟 2：定義檔案路徑

指定輸入 DWG 檔案的位置以及輸出 PDF 檔案的寫入路徑。

```java
String dataDir = "Your Document Directory" + "CADConversion/";
String sourceFilePath = dataDir + "meshes.dwg";
String outPath = dataDir + "meshes.pdf";
```

## 步驟 3：載入 CAD 圖像

將 DWG 檔案載入至 `CadImage` 物件，以便 Aspose.CAD 能夠處理其內部結構。

```java
CadImage cadImage = (CadImage)Image.load(sourceFilePath);
```

## 步驟 4：設定點陣化選項

設定點陣化選項，以控制產生的 PDF 頁面的尺寸與版面配置。`Layouts` 陣列指示 Aspose.CAD 於 **Model** 空間進行渲染，該空間包含網格實體。

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
rasterizationOptions.setLayouts(new String[] { "Model" });
```

## 步驟 5：設定 PDF 選項

將點陣化設定附加至 `PdfOptions` 實例。這告訴函式庫在產生 PDF 時使用先前定義的選項。

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## 步驟 6：儲存 PDF

最後，將載入的 CAD 圖像儲存為 PDF 檔案。產生的文件將忠實呈現原始 DWG，包括所有網格幾何形狀。

```java
cadImage.save(outPath, pdfOptions);
```

### 為何此方法適用於 **convert CAD to PDF**

Aspose.CAD 採用向量式點陣化，保留線條粗細、顏色與 3‑D 網格細節。透過設定點陣化選項，您可以控制解析度與版面配置，確保 **export CAD drawing** 在 PDF 中呈現的效果與預期完全一致。

## 常見使用情境

- **自動化報告：** 即時從工程圖紙產生 PDF 報告。  
- **文件歸檔：** 將 CAD 圖紙以 PDF 形式保存，以供長期保存。  
- **Web 服務：** 提供接受 DWG 上傳並回傳 PDF 的 API，適用於 SaaS 平台。  

## 疑難排解技巧

- **輸出缺少網格：** 確認 `Layouts` 屬性包含 `"Model"`；網格通常儲存在模型空間。  
- **比例不正確：** 調整 `PageWidth` 與 `PageHeight` 以符合圖紙的原始單位。  
- **授權錯誤：** 確保在載入圖像前已呼叫 `License.setLicense()` 並提供有效的授權檔案。  

## 結論

遵循上述步驟，即可可靠地 **convert DWG to PDF**，並充分利用 Aspose.CAD 的網格支援。此功能簡化了需要將複雜 CAD 圖紙高品質匯出為 PDF 的工作流程，無論是內部使用或面向客戶的文件。

## 常見問題

### Q1：Aspose.CAD for Java 是否適用於商業使用？

A1：是的，Aspose.CAD for Java 旨在同時支援個人與商業使用。您可在 [purchase page](https://purchase.aspose.com/buy) 查看授權細節。

### Q2：如何取得測試用的臨時授權？

A2：可從 [here](https://purchase.aspose.com/temporary-license/) 取得臨時授權，用於測試與評估。

### Q3：在哪裡可以找到 Aspose.CAD for Java 的社群支援？

A3：請前往 Aspose.CAD 專屬論壇 [https://forum.aspose.com/c/cad/19](https://forum.aspose.com/c/cad/19) 取得社群支援。

### Q4：除了 PDF，還支援其他輸出格式嗎？

A4：是的，Aspose.CAD for Java 支援多種輸出格式，包括 PNG、JPEG、BMP 等。詳情請參考文件說明。

### Q5：可以免費試用 Aspose.CAD for Java 嗎？

A5：可以，您可於 [here](https://releases.aspose.com/) 下載 Aspose.CAD for Java 的免費試用版。

**最後更新：** 2025-12-09  
**測試環境：** Aspose.CAD for Java 24.11  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}