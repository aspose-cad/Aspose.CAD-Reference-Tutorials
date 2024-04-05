---
title: 使用 Aspose.CAD for Java 將 CAD 佈局匯出為 PDF
linktitle: 將 CAD 佈局匯出為 PDF
second_title: Aspose.CAD Java API
description: 探索 Aspose.CAD for Java，輕鬆將 CAD 佈局匯出為 PDF。高效、可靠且對開發人員友善。
type: docs
weight: 11
url: /zh-hant/java/cad-export-options/export-cad-layouts-to-pdf/
---
## 介紹

在不斷發展的電腦輔助設計 (CAD) 領域，Aspose.CAD for Java 作為操作和轉換 CAD 檔案的強大工具脫穎而出。在本教學中，我們將引導您完成使用 Aspose.CAD for Java 將 CAD 佈局匯出為 PDF 的過程。無論您是經驗豐富的開發人員還是剛進入 CAD 世界，本逐步指南都將幫助您充分利用這個多功能 Java 程式庫的潛力。

## 先決條件

在我們深入學習本教程之前，請確保您具備以下先決條件：

-  Aspose.CAD for Java：確保您已安裝該程式庫。您可以從Aspose網站下載它[這裡](https://releases.aspose.com/cad/java/).

- Java 開發環境：確保您的電腦上設定了 Java 開發環境。

現在您已完成所有設置，讓我們開始本教學。

## 導入命名空間

在 Java 程式碼中，首先匯入必要的名稱空間。這些導入提供了對使用 Aspose.CAD for Java 所需的類別和方法的存取。

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

首先使用以下命令將 CAD 檔案載入到您的 Java 應用程式中`Image.load`方法。代替`"conic_pyramid.dxf"`以及 CAD 檔案的路徑。

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

## 第 2 步：設定光柵化選項

建立一個實例`CadRasterizationOptions`定義 CAD 實體應如何柵格化。根據您的需求調整頁面寬度、頁面高度、佈局縮放等參數。

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(false);
rasterizationOptions.setContentAsBitmap(true);
rasterizationOptions.setLayouts(new String[]{"Model"});
```

## 步驟 3：設定 PDF 選項

建立一個實例`PdfOptions`並將其與光柵化選項相關聯。此外，還可以設定 PDF 匯出的圖形選項，例如平滑模式、文字渲染提示和內插模式。

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
rasterizationOptions.getGraphicsOptions().setSmoothingMode(SmoothingMode.HighQuality);
rasterizationOptions.getGraphicsOptions().setTextRenderingHint(TextRenderingHint.AntiAliasGridFit);
rasterizationOptions.getGraphicsOptions().setInterpolationMode(InterpolationMode.HighQualityBicubic);
```

## 第 4 步：匯出為 PDF

最後，使用以下命令將 CAD 佈局匯出為 PDF 檔案：`save`的方法`cadImage`目的。

```java
cadImage.save(dataDir + "CADLayoutsToPDF_out_.pdf", pdfOptions);
```

恭喜！您已使用 Aspose.CAD for Java 成功將 CAD 版面配置匯出為 PDF。請隨意探索 Aspose.CAD 提供的其他特性和功能，以增強您的 CAD 檔案操作體驗。

## 結論

在本教程中，我們演練了使用 Aspose.CAD for Java 將 CAD 佈局匯出為 PDF 的過程。憑藉其強大的功能和易於使用的 API，Aspose.CAD 使開發人員能夠在其 Java 應用程式中有效地處理 CAD 檔案。

## 常見問題解答

### Q1：我可以將 Aspose.CAD for Java 與其他 CAD 檔案格式一起使用嗎？

 A1：是的，Aspose.CAD支援各種CAD格式，包括DWG、DXF、DWF等。檢查文檔[這裡](https://reference.aspose.com/cad/java/)以獲得完整清單。

### 問題 2：Aspose.CAD for Java 是否有免費試用版？

 A2：是的，您可以透過免費試用來探索 Aspose.CAD 的功能[這裡](https://releases.aspose.com/).

### 問題 3：如何獲得 Aspose.CAD for Java 的支援？

 A3：造訪 Aspose.CAD 論壇[這裡](https://forum.aspose.com/c/cad/19)以獲得社區支持。如需高級支持，請考慮購買許可證[這裡](https://purchase.aspose.com/buy).

### Q4：自動佈局縮放和手動佈局縮放有什麼區別？

A4：自動佈局縮放會根據指定的頁面尺寸調整佈局大小，而手動縮放則可讓您設定自訂縮放值。

### Q5：我可以自訂匯出的PDF檔案的外觀嗎？

A5：是的，您可以自訂程式碼中的圖形選項來控制匯出的 PDF 的品質和外觀。