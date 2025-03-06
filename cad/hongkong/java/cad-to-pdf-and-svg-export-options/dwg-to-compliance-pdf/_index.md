---
title: 使用 Aspose.CAD for Java 將 DWG 轉換為合規性 PDF
linktitle: DWG 到合規性 PDF
second_title: Aspose.CAD Java API
description: 使用 Aspose.CAD for Java 輕鬆將 DWG 繪圖轉換為 PDF/A1a 和 PDF/A1b 相容檔案。精確輕鬆地簡化您的工作流程。
weight: 11
url: /zh-hant/java/cad-to-pdf-and-svg-export-options/dwg-to-compliance-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.CAD for Java 將 DWG 轉換為合規性 PDF

## 介紹

在不斷發展的數位設計世界中，將 DWG 工程圖轉換為合規的 PDF 格式對於無縫協作和標準化文件至關重要。 Aspose.CAD for Java 成為了一個強大的工具，在此過程中提供了效率和精確度。在本教學中，我們將探討如何利用 Aspose.CAD for Java 輕鬆將 DWG 檔案轉換為相容的 PDF，確保遵守 PDF/A1a 和 PDF/A1b 標準。

## 先決條件

在深入學習本教程之前，請確保您具備以下先決條件：

- Java 開發環境：確保您的系統上設定了有效的 Java 開發環境。
-  Aspose.CAD 函式庫：從下列位置下載並安裝 Java 的 Aspose.CAD 函式庫：[下載連結](https://releases.aspose.com/cad/java/).
- 文件目錄：建立一個目錄來儲存 DWG 工程圖。

## 導入命名空間

在您的 Java 專案中，匯入必要的命名空間以存取 Aspose.CAD 的功能。在 Java 檔案的開頭新增以下行：

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfCompliance;
import com.aspose.cad.imageoptions.PdfDocumentOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## 第1步：設定資源目錄

定義儲存 DWG 工程圖的資源目錄的路徑。

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

## 步驟 2： 載入 DWG 文件

使用 Aspose.CAD 庫載入 DWG 檔案。

```java
String srcFile = dataDir + "Bottom_plate.dwg";
Image objImage = Image.load(srcFile);
```

## 第 3 步：建立 PDF 選項

建立 PdfOptions 的實例並設定向量光柵化選項。

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());
```

## 步驟 4： 設定核心 PDF 選項

設定核心 PDF 選項，指定合規性標準（PDF/A1a 或 PDF/A1b）。

```java
pdfOptions.setCorePdfOptions(new PdfDocumentOptions());
pdfOptions.getCorePdfOptions().setCompliance(PdfCompliance.PdfA1a);
```

## 步驟 5：依照合規性 A1a 儲存 PDF

儲存符合 A1a 標準的 PDF 檔案。

```java
objImage.save(dataDir + "Saved1.pdf", pdfOptions);
```

## 第 6 步：將合規性改為 A1b

將合規性變更為 PDF/A1b 並儲存 PDF。

```java
pdfOptions.getCorePdfOptions().setCompliance(PdfCompliance.PdfA1b);
objImage.save(dataDir + "Saved.pdf", pdfOptions);
```

對要轉換的每個 DWG 檔案重複這些步驟。

## 結論

總之，Aspose.CAD for Java 提供了將 DWG 檔案轉換為合規 PDF 的強大解決方案。透過遵循此逐步指南，您可以簡化轉換流程並確保您的文件符合行業標準。

## 常見問題解答

### Q1：Aspose.CAD 是否相容於所有版本的 DWG 檔案？

 A1：Aspose.CAD支援各種版本的DWG文件，包括最新的版本。請參閱[文件](https://reference.aspose.com/cad/java/)取得詳細的相容性資訊。

### Q2：我可以使用Aspose.CAD自訂PDF輸出設定嗎？

A2：當然！ Aspose.CAD 提供了一系列自訂選項，可讓您根據您的特定要求自訂 PDF 輸出。

### Q3：Aspose.CAD 是否有臨時授權？

 A3：是的，您可以從以下位置取得用於測試目的的臨時許可證：[這個連結](https://purchase.aspose.com/temporary-license/).

### 問題 4：我可以在哪裡尋求 Aspose.CAD 的支持或與社群互動？

 A4：訪問[Aspose.CAD論壇](https://forum.aspose.com/c/cad/19)以獲得社區支持和討論。

### Q5：我可以在購買前免費試用 Aspose.CAD 嗎？

 A5：當然！從以下位置下載免費試用版[這裡](https://releases.aspose.com/)在做出決定之前探索能力。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
