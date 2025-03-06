---
title: 使用 Aspose.CAD for Java 將嵌入式 DGN 匯出為 PDF
linktitle: 匯出嵌入式 DGN
second_title: Aspose.CAD Java API
description: 探索使用 Aspose.CAD for Java 將嵌入式 DGN 檔案匯出為 PDF 的逐步指南。透過無縫 CAD 檔案操作增強您的 Java 應用程式。
weight: 11
url: /zh-hant/java/dgn-export-options/export-embedded-dgn/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.CAD for Java 將嵌入式 DGN 匯出為 PDF

## 介紹

歡迎閱讀使用 Aspose.CAD for Java 匯出嵌入式 DGN 檔案的綜合教學。 Aspose.CAD 是一個功能強大的函式庫，可讓 Java 開發人員無縫地處理 CAD 檔案。在本教學中，我們將按照逐步說明指導您完成將嵌入式 DGN 檔案匯出為 PDF 的過程。無論您是經驗豐富的開發人員還是新手，本教學都將協助您利用 Aspose.CAD 的功能來增強您的 Java 應用程式。

## 先決條件

在我們深入學習本教程之前，請確保您具備以下先決條件：
- Java 開發環境：確保您的電腦上設定有 Java 開發環境。
-  Aspose.CAD for Java：從下列位置下載並安裝 Aspose.CAD for Java 函式庫[這裡](https://releases.aspose.com/cad/java/).

## 導入包

首先，您需要在 Java 專案中匯入必要的套件。將以下導入語句加入您的程式碼：

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

現在，讓我們將範例程式碼分解為多個步驟：

## 第 1 步：設定輸入和輸出路徑

定義文件所在的目錄路徑並指定輸入 DWG 檔名。

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
```

## 步驟 2： 載入 DWG 文件

將 DWG 檔案載入到`Image`使用 Aspose.CAD 的物件。

```java
Image objImage = Image.load(fileName);
```

## 步驟 3：配置光柵化選項

配置光柵化選項，例如要包含在匯出中的佈局。

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setLayouts(new String[] {"Model"});
```

## 步驟 4：配置 PDF 選項

設定 PDF 選項，包括向量光柵化選項。

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## 第5步：儲存PDF文件

使用配置的選項儲存 PDF 檔案。
```java
objImage.save(dataDir + "BlockRefDgn.pdf", pdfOptions);
```

## 結論

恭喜！您已使用 Aspose.CAD for Java 成功將嵌入的 DGN 檔案匯出為 PDF。本教學介紹了將 Aspose.CAD 整合到 Java 應用程式中以實現高效 CAD 檔案操作的基本步驟。

## 常見問題解答

### Q1：我可以在商業專案中使用Aspose.CAD for Java嗎？

 A1：是的，Aspose.CAD for Java 是一個商業函式庫。您可以從以下位置取得許可證[這裡](https://purchase.aspose.com/buy).

### Q2: 有免費試用嗎？

 A2：是的，您可以免費試用 Aspose.CAD for Java[這裡](https://releases.aspose.com/).

### 問題 3：如何獲得 Aspose.CAD for Java 的支援？

A3：您可以向 Aspose.CAD 社群尋求支持[論壇](https://forum.aspose.com/c/cad/19).

### Q4：如果我需要臨時許可證怎麼辦？

 A4：您可以獲得臨時許可證[這裡](https://purchase.aspose.com/temporary-license/).

### Q5：在哪裡可以找到文件？

 A5：文檔可用[這裡](https://reference.aspose.com/cad/java/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
