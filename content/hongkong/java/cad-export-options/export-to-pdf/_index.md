---
title: 使用 Aspose.CAD for Java 匯出為 PDF
linktitle: 匯出為 PDF
second_title: Aspose.CAD Java API
description: 了解如何使用 Aspose.CAD for Java 輕鬆將 CAD 檔案匯出為 PDF。請按照我們的逐步指南進行無縫整合。
type: docs
weight: 13
url: /zh-hant/java/cad-export-options/export-to-pdf/
---
## 介紹

歡迎閱讀使用 Aspose.CAD for Java 將 CAD 檔案匯出為 PDF 的綜合教學課程。如果您希望將 CAD 繪圖無縫轉換為廣泛支援的 PDF 格式，那麼您來對地方了。在本逐步指南中，我們將分解該過程，確保您了解成功匯出 PDF 的每個步驟。

## 先決條件

在深入學習本教程之前，請確保您具備以下先決條件：

-  Aspose.CAD for Java：確保您的 Java 環境中安裝了 Aspose.CAD 函式庫。你可以下載它[這裡](https://releases.aspose.com/cad/java/).

- 資源目錄：設定儲存 CAD 檔案的目錄。將提供的程式碼片段中的「您的文件目錄」替換為實際路徑。

現在，讓我們繼續主要步驟。

## 導入命名空間

在您的 Java 專案中，首先匯入必要的命名空間以啟用 Aspose.CAD 功能。

```java
import com.aspose.cad.Image;
import com.aspose.cad.InterpolationMode;
import com.aspose.cad.SmoothingMode;
import com.aspose.cad.TextRenderingHint;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//導入 com.aspose.cad.imageoptions.TypeOfEntities;
```

## 第 1 步：載入 CAD 文件

將 CAD 檔案載入到 Aspose.CAD Image 物件中。將“site.dwf”替換為您的實際 CAD 檔案名稱。

```java
String fileName = (dataDir + "site.dwf");
Image image = Image.load(fileName);
```

## 第 2 步：配置 PDF 選項

設定 PDF 匯出選項，包括向量光柵化選項，例如頁面高度、寬度和佈局。

```java
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);

rasterizationOptions.setPageHeight(500);
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setLayouts(new String[] { "Model" });
```

## 第 3 步：匯出為 PDF

指定產生的 PDF 檔案的輸出路徑，並使用配置的 PDF 選項儲存影像。

```java
String outPath = dataDir + "site.pdf";
image.save(outPath, pdfOptions);
```

恭喜！您已使用 Aspose.CAD for Java 成功將 CAD 檔案匯出為 PDF。

## 結論

在本教程中，我們探索了使用 Aspose.CAD for Java 將 CAD 檔案匯出為 PDF 的逐步過程。透過遵循這些簡單而有效的步驟，您可以將此功能無縫整合到您的 Java 應用程式中。

## 常見問題解答

### Q1：Aspose.CAD 是否相容於所有 CAD 檔案格式？

A1：是的，Aspose.CAD支援多種CAD格式，確保與各種設計軟體的相容性。

### Q2: 我可以自訂 PDF 輸出設定嗎？

A2：當然。本教程簡要介紹了自訂選項，但您可以進一步探索以根據您的需求自訂輸出。

### 問題 3：在哪裡可以找到對 Aspose.CAD 的額外支援？

 A3：如有任何疑問或問題，請訪問[Aspose.CAD論壇](https://forum.aspose.com/c/cad/19)向社區尋求協助。

### Q4：有免費試用嗎？

 A4：是的，您可以免費試用 Aspose.CAD[這裡](https://releases.aspose.com/).

### Q5：如何取得Aspose.CAD的臨時授權？

 A5：如需臨時許可，請訪問[這個連結](https://purchase.aspose.com/temporary-license/).