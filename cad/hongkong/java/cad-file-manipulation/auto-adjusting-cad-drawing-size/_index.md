---
title: 使用 Aspose.CAD for Java 自動調整 CAD 圖面尺寸
linktitle: 自動調整 CAD 圖紙尺寸
second_title: Aspose.CAD Java API
description: 探索使用 Aspose.CAD 在 Java 中自動調整 CAD 繪圖尺寸的無縫過程。請按照我們的逐步指南進行高效率的 CAD 檔案操作。
type: docs
weight: 13
url: /zh-hant/java/cad-file-manipulation/auto-adjusting-cad-drawing-size/
---
## 介紹

在 CAD（電腦輔助設計）領域，調整繪圖尺寸是一項常見要求，而使用 Aspose.CAD for Java，它成為一個無縫過程。這個功能強大的程式庫提供了在 Java 應用程式中處理 CAD 檔案的綜合工具。在本教學中，我們將探索使用 Aspose.CAD 自動調整 CAD 繪圖尺寸的逐步過程。

## 先決條件

在深入學習本教程之前，請確保您具備以下先決條件：

1.  Java 開發環境：確保您的電腦上安裝了 Java。你可以下載它[這裡](https://www.java.com/en/download/).

2. Aspose.CAD 函式庫：下載並安裝適用於 Java 的 Aspose.CAD 函式庫[這裡](https://releases.aspose.com/cad/java/).

3. 範例 CAD 檔案：在文件目錄中提供一個範例 CAD 檔案（例如，sample.dwg）。

## 導入命名空間

在您的 Java 應用程式中，包含必要的命名空間以利用 Aspose.CAD 功能。這是一個例子：

```java

import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

現在，讓我們將自動調整 CAD 繪圖尺寸的流程分解為可管理的步驟。

## 第 1 步：載入 CAD 圖紙

```java
String dataDir = "Your Document Directory" + "CADConversion/";
String sourceFilePath = dataDir + "sample.dwg";
Image objImage = Image.load(sourceFilePath);
```

此步驟涉及從指定檔案路徑載入 CAD 繪圖。

## 步驟2：建立BmpOptions

```java
BmpOptions bmpOptions = new BmpOptions();
```

實例化`BmpOptions`類，它將用於設定 BMP 格式的各種選項。

## 步驟 3：建立 CadRasterizationOptions

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(cadRasterizationOptions);
```

建立一個實例`CadRasterizationOptions`自訂 CAD 檔案的光柵化設定。

## 步驟4：設定佈局屬性

```java
cadRasterizationOptions.setLayouts(new String[]{"Model"});
```

指定要包含在輸出中的佈局。在本例中，我們使用“模型”佈局。

## 步驟5：匯出為BMP格式

```java
String outPath = sourceFilePath + ".bmp";
objImage.save(outPath, bmpOptions);
```

最後將調整後的CAD圖以BMP格式儲存到指定的輸出路徑。

在 Java 應用程式中重複這些步驟，您就可以使用 Aspose.CAD for Java 成功自動調整 CAD 繪圖尺寸。

## 結論

在本教學中，我們介紹了使用 Aspose.CAD for Java 自動調整 CAD 繪圖尺寸的過程。該程式庫簡化了 CAD 檔案操作，為開發人員提供了強大的解決方案。

## 常見問題解答

### Q1: Aspose.CAD 是否相容於不同的 CAD 檔案格式？

A1：是的，Aspose.CAD支援各種CAD格式，包括DWG、DXF、DGN等。

### Q2：我可以將Aspose.CAD用於商業專案嗎？

 A2：當然！訪問[這裡](https://purchase.aspose.com/buy)探索許可證選項。

### Q3：如何取得測試目的的臨時許可證？

 A3：獲得臨時許可證[這裡](https://purchase.aspose.com/temporary-license/)用於測試和評估。

### Q4：在哪裡可以找到對 Aspose.CAD 的支援？

A4：加入 Aspose.CAD 社區[論壇](https://forum.aspose.com/c/cad/19)尋求幫助和討論。

### Q5：Aspose.CAD for Java 有免費試用版嗎？

 A5：是的，您可以免費試用[這裡](https://releases.aspose.com/)探索圖書館的能力。