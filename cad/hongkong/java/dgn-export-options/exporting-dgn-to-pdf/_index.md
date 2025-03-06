---
title: 使用 Aspose.CAD for Java 輕鬆將 DGN 匯出為 AutoCAD PDF
linktitle: 將 AutoCAD 格式的 DGN 匯出為 PDF
second_title: Aspose.CAD Java API
description: 探索使用 Aspose.CAD for Java 將 DGN 檔案匯出為 PDF 中的 AutoCAD 格式的逐步指南。輕鬆提升 Java 應用程式的 CAD 處理能力。
weight: 12
url: /zh-hant/java/dgn-export-options/exporting-dgn-to-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.CAD for Java 輕鬆將 DGN 匯出為 AutoCAD PDF

## 介紹

歡迎閱讀這個關於使用 Aspose.CAD for Java 將 AutoCAD 格式的 DGN 檔案匯出為 PDF 的綜合教學。如果您希望增強 Java 應用程式處理 CAD 檔案的能力，Aspose.CAD 是一個很好的選擇。在本教程中，我們將指導您逐步完成匯出 DGN 檔案的過程。


## 先決條件
在我們深入學習本教程之前，請確保您具備以下先決條件：
-  Aspose.CAD 程式庫：確保您已安裝適用於 Java 的 Aspose.CAD 程式庫。你可以下載它[這裡](https://releases.aspose.com/cad/java/).
- 文檔目錄：設定將儲存輸入和輸出檔案的文檔目錄。

## 導入包

在您的 Java 專案中，匯入必要的套件以存取 Aspose.CAD 功能：

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

現在，讓我們將範例程式碼分解為多個步驟：

## 第 1 步：定義檔路徑

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "Nikon_D90_Camera.dgn";
String outFile  = dataDir + "Nikon_D90_Camera.pdf";
```

確保將“您的文件目錄”替換為文件所在的實際路徑。

## 步驟 2：載入 DGN 影像

```java
DgnImage objImage = (DgnImage) Image.load(fileName);
```

使用 Aspose.CAD 載入 DGN 檔案。

## 第 3 步：設定 PDF 匯出選項

```java
PdfOptions options = new PdfOptions();
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
vectorOptions.setAutomaticLayoutsScaling(true);
vectorOptions.setLayouts(new String[] { "1", "2", "3", "9" }); //匯出特定視圖
options.setVectorRasterizationOptions(vectorOptions);
```

定義 PDF 匯出選項，包括頁面尺寸和版面設定首選項。

## 第 4 步：儲存 PDF 文件

```java
objImage.save(outFile, options);
```

儲存匯出的 PDF 檔案。

對要轉換的任何其他 DGN 檔案重複這些步驟。恭喜！您已使用 Aspose.CAD for Java 成功將 DGN 檔案匯出為 AutoCAD 格式的 PDF。

## 結論

在本教學中，我們探討如何利用 Aspose.CAD for Java 來增強應用程式的 CAD 檔案處理功能。透過易於遵循的步驟和程式碼範例，現在您可以將 DGN 檔案無縫匯出為 PDF 格式的 AutoCAD 格式。

## 常見問題解答

### Q1：Aspose.CAD 是否相容於所有 CAD 檔案格式？

A1：是的，Aspose.CAD 支援多種 CAD 格式，確保處理各種檔案類型的多功能性。

### Q2：我可以自訂 PDF 匯出設定嗎？

A2：當然。如教程中所示，您可以調整頁面尺寸和佈局等選項以滿足您的要求。

### 問題 3：我可以在哪裡找到額外的支援或協助？

 A3：訪問[Aspose.CAD論壇](https://forum.aspose.com/c/cad/19)以獲得社區支持和討論。

### Q4：有免費試用嗎？

 A4：是的，您可以免費試用[這裡](https://releases.aspose.com/).

### Q5：如何取得臨時駕照？

 A5：獲得臨時許可證[這裡](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
