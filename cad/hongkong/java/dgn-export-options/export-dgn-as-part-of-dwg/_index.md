---
title: 使用 Aspose.CAD for Java 將 DGN 匯出為 DWG
linktitle: 將 DGN 匯出為 DWG 的一部分
second_title: Aspose.CAD Java API
description: 探索如何使用 Aspose.CAD for Java 將 DGN 匯出為 DWG 的一部分。請按照我們的逐步指南進行高效率的 CAD 檔案操作。
weight: 10
url: /zh-hant/java/dgn-export-options/export-dgn-as-part-of-dwg/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.CAD for Java 將 DGN 匯出為 DWG

## 介紹

在本教學中，我們將探討如何使用 Aspose.CAD for Java 將 DGN (MicroStation Design) 檔案匯出為 DWG (AutoCAD Drawing) 檔案的一部分。 Aspose.CAD 是一個功能強大的函式庫，提供了處理 CAD 檔案格式的全面功能。本逐步指南將幫助您了解使用 Java 將 DGN 匯出為 DWG 的一部分的過程。

## 先決條件

在我們深入學習本教程之前，請確保您具備以下先決條件：
1. Aspose.CAD 函式庫：下載並安裝適用於 Java 的 Aspose.CAD 函式庫。你可以找到圖書館[這裡](https://releases.aspose.com/cad/java/).
2. Java 開發工具包 (JDK)：確保您的系統上安裝了 Java。
3. 整合開發環境 (IDE)：選擇 Eclipse 或 IntelliJ 等 Java IDE，以獲得更流暢的開發體驗。

## 導入包

在您的 Java 專案中，匯入必要的 Aspose.CAD 套件以啟用 CAD 檔案操作。這是一個例子：

```java
import com.aspose.cad;
import com.aspose.cad.imageoptions;
import com.aspose.cad.fileformats.cad.cadconsts;
import com.aspose.cad.fileformats.cad;
import com.aspose.cad.fileformats.cad.cadobjects;
```

## 第1步：設定檔案路徑

定義 DWG 檔案的輸入和輸出檔案路徑。更新`dataDir`, `fileName`， 和`outPath`對應的變數。

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
String outPath = dataDir + "BlockRefDgn.dwg.pdf";
```

## 步驟2：建立PdfOptions實例

建立一個實例`PdfOptions`類，因為我們要將 DWG 檔案匯出為 PDF 格式。

```java
PdfOptions exportOptions = new PdfOptions();
```

## 步驟 3： 載入 DWG 文件

將現有 DWG 檔案作為映像載入並將其轉換為`CadImage`類型。

```java
CadImage cadImage = (CadImage) Image.load(fileName);
```

## 第 4 步：迭代實體

瀏覽 DWG 檔案中的每個實體並檢查它是否為圖像定義。如果是，則檢索該物件的外部參考。

```java
for (CadBaseEntity baseEntity : cadImage.getEntities()) {
    if (baseEntity.getTypeName() == CadEntityTypeName.DGNUNDERLAY) {
        CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
        System.out.println(dgnFile.getUnderlayPath());
    }
}
```

## 第 5 步：定義光柵化選項

定義設定`CadRasterizationOptions`對象，包括頁面寬度、高度、佈局和背景顏色。

```java
CadRasterizationOptions vectorRasterizationOptions = new CadRasterizationOptions();
vectorRasterizationOptions.setPageWidth(1600);
vectorRasterizationOptions.setPageHeight(1600);
vectorRasterizationOptions.setLayouts(new String[] { "Model" });
vectorRasterizationOptions.setAutomaticLayoutsScaling(false);
vectorRasterizationOptions.setNoScaling(true);
vectorRasterizationOptions.setBackgroundColor(Color.getBlack());
vectorRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
```

## 第 6 步：設定向量光柵化選項

設定導出的向量光柵化選項。

```java
exportOptions.setVectorRasterizationOptions(vectorRasterizationOptions);
```

## 步驟 7：將 DWG 匯出為 PDF

最後，透過呼叫將 DWG 匯出為 PDF`save`方法。

```java
cadImage.save(outPath, exportOptions);
```

## 結論

恭喜！您已成功學習如何使用 Aspose.CAD for Java 將 DGN 檔案匯出為 DWG 檔案的一部分。這個強大的程式庫提供了處理 CAD 檔案的廣泛功能，使您的 CAD 檔案操作任務高效且簡單。

## 常見問題解答

### Q1：在哪裡可以找到 Aspose.CAD for Java 的文檔？

 A1：文件可以找到[這裡](https://reference.aspose.com/cad/java/).

### Q2：如何下載 Java 版 Aspose.CAD 函式庫？

 A2：您可以從以下位置下載該庫：[這個連結](https://releases.aspose.com/cad/java/).

### 問題 3：Aspose.CAD for Java 是否有免費試用版？

 A3：是的，您可以找到免費試用版[這裡](https://releases.aspose.com/).

### 問題 4：在哪裡可以獲得 Aspose.CAD for Java 的臨時授權？

 A4：取得臨時許可證[這裡](https://purchase.aspose.com/temporary-license/).

### Q5: 需要協助或有疑問嗎？

 A5：造訪 Aspose.CAD 社群支援論壇[這裡](https://forum.aspose.com/c/cad/19).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
