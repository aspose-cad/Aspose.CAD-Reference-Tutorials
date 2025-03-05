---
title: DGN 到 PDF 轉換指南 - Aspose.CAD for Java
linktitle: 支持 DGN V7
second_title: Aspose.CAD Java API
description: 使用 Aspose.CAD for Java 輕鬆將 DGN 檔案轉換為 PDF。請遵循我們的逐步指南，以實現無縫整合和高效的工作流程。
type: docs
weight: 11
url: /zh-hant/java/other-cad-operations/support-for-dgn-v7/
---
## 介紹

在 CAD（電腦輔助設計）的動態世界中，將 DGN（設計）文件有效率地轉換為 PDF（可攜式文件格式）是一項至關重要的要求。 Aspose.CAD for Java 作為一個強大的解決方案出現，提供無縫整合和強大的功能。本逐步指南旨在引導您完成使用 Aspose.CAD for Java 將 DGN 檔案匯出為 PDF 的流程，確保工作流程順利且有效率。

## 先決條件

在深入學習本教程之前，請確保您具備以下先決條件：
-  Aspose.CAD for Java Library：從下列位置下載並安裝程式庫：[Aspose.CAD for Java 下載頁面](https://releases.aspose.com/cad/java/).
- Java 開發環境：確保您的電腦上設定了 Java 開發環境。

## 導入包

首先將必要的套件匯入到您的 Java 專案中：

## 步驟1：導入必要的套件

在您的 Java 專案中，匯入 Aspose.CAD for Java 所需的套件。
```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadRasterizationOptions;
import com.aspose.cad.fileformats.cad.cadobjects.DgnImage;
import com.aspose.cad.imageoptions.PdfOptions;
import java.awt.Color;
```

## 第2步：設定檔案路徑

定義輸入 DGN 檔案和輸出 PDF 檔案的路徑。

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "Nikon_D90_Camera.dgn";
String outFile  = dataDir + "Nikon_D90_Camera.pdf";
```

## 步驟 3：載入 DGN 影像

使用 Aspose.CAD 庫載入 DGN 圖像。

```java
DgnImage objImage = (DgnImage)Image.load(fileName);
```

## 步驟 4：設定 PDF 匯出選項

設定匯出為 PDF 的選項，包括頁面尺寸、自動佈局縮放、背景顏色和要匯出的特定佈局。

```java
PdfOptions options = new PdfOptions();
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
vectorOptions.setAutomaticLayoutsScaling(true);
vectorOptions.setBackgroundColor(Color.getBlack());
vectorOptions.setLayouts(new String[] { "1", "2", "3", "9" }); //僅匯出 4 個（1、2、3 和 9）視圖
options.setVectorRasterizationOptions(vectorOptions);
```

## 第5步：儲存PDF文件

使用指定選項將 DGN 影像儲存為 PDF 檔案。

```java
objImage.save(outFile, options);
```

對不同的 DGN 檔案重複這些步驟，根據需要調整檔案路徑和選項。

## 結論

透過 Aspose.CAD for Java，將 DGN 檔案轉換為 PDF 成為一個簡單的過程。本指南為您提供了將該程式庫無縫整合到 Java 專案中的知識，從而促進高效的 CAD 檔案轉換。

## 常見問題解答

### Q1：我可以將 Aspose.CAD for Java 與其他 CAD 檔案格式一起使用嗎？

A1：是的，Aspose.CAD 支援各種 CAD 格式，提供 DGN 到 PDF 轉換之外的多種功能。

### 問題 2：Aspose.CAD for Java 是否有臨時授權？

 A2：是的，您可以獲得臨時許可證[這裡](https://purchase.aspose.com/temporary-license/)用於測試目的。

### 問題 3：如何尋求有關 Aspose.CAD for Java 的支援或提出問題？

 A3：訪問[Aspose.CAD論壇](https://forum.aspose.com/c/cad/19)與社區聯繫並尋求協助。

### 問題 4：將 DGN 轉換為 PDF 時可以匯出哪些佈局？

 A4：您可以透過自訂來指定要匯出的佈局`setLayouts`程式碼中的數組。

### 問題 5：在哪裡可以找到 Aspose.CAD for Java 的綜合文件？

 A5：請參閱[Aspose.CAD for Java 文檔](https://reference.aspose.com/cad/java/)獲取詳細資訊。