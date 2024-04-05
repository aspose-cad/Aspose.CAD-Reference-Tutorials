---
title: 設定畫布大小和模式
linktitle: 設定畫布大小和模式
second_title: Aspose.CAD Java API
description: 透過我們設定畫布大小和模式的逐步指南，探索 Aspose.CAD for Java 的強大功能。輕鬆將 CAD 檔案轉換為 PDF 和 TIFF 格式。
type: docs
weight: 16
url: /zh-hant/java/advanced-cad-features/set-canvas-size-and-mode/
---
## 介紹

您是否希望利用 Aspose.CAD for Java 的強大功能來增強您的 CAD 轉換過程？本綜合指南將引導您完成使用 Aspose.CAD for Java 設定畫布大小和模式的步驟。無論您是經驗豐富的開發人員還是剛剛入門，本教學都將為您提供所需的見解。

## 先決條件

在深入學習本教程之前，請確保您具備以下先決條件：

-  Aspose.CAD for Java：確保您的 Java 環境中安裝了 Aspose.CAD 函式庫。你可以下載它[這裡](https://releases.aspose.com/cad/java/).

- 文檔目錄：設定文檔目錄來儲存 CAD 檔案。該目錄將在教程步驟中引用。

現在，讓我們開始使用逐步指南。

## 導入命名空間

在此步驟中，我們將匯入必要的命名空間來啟動您的 Aspose.CAD 專案。
```java
import java.awt.Image;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## 步驟1：導入Aspose.CAD類

```java
//資源目錄的路徑。
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
com.aspose.cad.Image objImage = com.aspose.cad.Image.load(srcFile);
```

在此程式碼片段中，我們設定資源目錄的路徑並使用 Aspose.CAD 載入 DXF 檔案`Image`班級。

## 步驟 2：設定 CadRasterizationOptions 屬性

```java
//建立 CadRasterizationOptions 的實例並設定其各種屬性
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

在這裡，我們建立一個實例`CadRasterizationOptions`並配置頁面寬度、頁面高度和縮放選項等屬性。

## 步驟 3：建立 PdfOptions 並設定 VectorRasterizationOptions

```java
//建立 PdfOptions 的實例
PdfOptions pdfOptions = new PdfOptions();

//設定 VectorRasterizationOptions 屬性
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

現在，我們創建一個`PdfOptions`實例並設定其`VectorRasterizationOptions`屬性改為之前配置的`CadRasterizationOptions`.

## 第 4 步：匯出為 PDF

```java
//將 CAD 匯出為 PDF
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

最後，我們使用指定的選項將 CAD 影像儲存到 PDF 檔案。

## 步驟 5：建立 TiffOptions 並設定 VectorRasterizationOptions

```java
//建立 TiffOptions 的實例
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);

//設定 VectorRasterizationOptions 屬性
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
```

在這一步驟中，我們設定了一個`TiffOptions`實例並配置其`VectorRasterizationOptions`財產。

## 第 6 步：導出為 TIFF

```java
//將 CAD 匯出為 TIFF
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

最後，我們使用指定的選項將 CAD 影像儲存到 TIFF 檔案。

## 結論

恭喜！您已使用 Aspose.CAD for Java 成功設定了畫布大小和模式。本教學為您的 CAD 轉換專案提供了堅實的基礎。探索更多功能和可能性[Aspose.CAD 文檔](https://reference.aspose.com/cad/java/).

## 常見問題解答

### Q1：我可以將 Aspose.CAD for Java 與其他 Java 框架一起使用嗎？

A1：是的，Aspose.CAD 旨在與各種 Java 框架無縫整合。

### Q2：Aspose.CAD 是否有臨時授權？

 A2：是的，您可以獲得臨時許可證[這裡](https://purchase.aspose.com/temporary-license/).

### 問題 3：我可以在哪裡獲得 Aspose.CAD 的社群支持？

 A3：訪問[Aspose.CAD論壇](https://forum.aspose.com/c/cad/19)以獲得社區支持和討論。

### Q4：我可以免費試用Aspose.CAD嗎？

 A4：當然！獲得免費試用[這裡](https://releases.aspose.com/).

### Q5: 如何購買 Aspose.CAD for Java？

A5：購買產品[這裡](https://purchase.aspose.com/buy).