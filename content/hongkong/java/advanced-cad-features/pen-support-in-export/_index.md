---
title: 匯出中的筆支持
linktitle: 匯出中的筆支持
second_title: Aspose.CAD Java API
description: 使用 Aspose.CAD for Java 掌握 CAD 匯出中的筆自訂。請按照我們的逐步指南進行無縫整合。
type: docs
weight: 13
url: /zh-hant/java/advanced-cad-features/pen-support-in-export/
---
## 介紹

在不斷發展的 CAD（電腦輔助設計）轉換領域，Aspose.CAD for Java 成為一個強大的工具，提供了操作 CAD 檔案的廣泛功能。在其多功能功能中，匯出期間對筆自訂的支援非常突出，允許使用者自訂匯出影像的外觀。本教學將引導您完成在匯出功能中利用筆支援的過程，並專注於使用 Java 的實際實作。

## 先決條件

在深入研究本教程之前，請確保您具備以下先決條件：

- Java 開發環境：確保您的電腦上設定了功能齊全的 Java 開發環境。

-  Aspose.CAD 函式庫：下載 Aspose.CAD 函式庫並將其整合到您的 Java 專案中。你可以找到圖書館[這裡](https://releases.aspose.com/cad/java/).

現在，讓我們進入教學課程並探索在 CAD 匯出期間利用筆支援的步驟。

## 導入命名空間

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.PenOptions;
import com.aspose.cad.internal.imaging.LineCap;
```

## 第 1 步：定義您的文件目錄

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

確保將「您的文件目錄」替換為 CAD 文件的實際路徑。

## 第 2 步：載入 CAD 文件

```java
String srcFile = dataDir + "conic_pyramid.dxf";
CadImage cadImage = (CadImage) Image.load(srcFile);
```

此步驟涉及使用 Aspose.CAD 庫載入 CAD 檔案（在本例中為「conic_pyramid.dxf」）。

## 步驟 3：配置光柵化選項

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(cadImage.getWidth() * 100);
rasterizationOptions.setPageHeight(cadImage.getHeight() * 100);
```

根據您的具體要求調整頁面寬度和高度。這些值決定導出影像的尺寸。

## 第 4 步：自訂筆選項

```java
PenOptions penOts = new PenOptions();
penOts.setStartCap(LineCap.Flat);
penOts.setEndCap(LineCap.Flat);
```

根據需要訂製筆的起始端蓋和端蓋。將 CadImage 物件匯出為各種影像格式時適用此自訂。

## 步驟 5：設定 PDF 匯出選項

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

指定向量光柵化選項，包括先前配置的光柵化選項。

## 第6步：儲存匯出的PDF

```java
cadImage.save((dataDir + "9LHATT-A56_generated.pdf"), pdfOptions);
```

使用指定的檔案名稱（本例中為「9LHATT-A56_ generated.pdf」）和設定的選項儲存匯出的 PDF。

## 結論

總之，在 CAD 匯出過程中利用 Aspose.CAD for Java 的筆支援使用戶能夠自訂匯出影像的外觀。透過遵循此逐步指南，您已了解如何將筆自訂無縫整合到 CAD 轉換工作流程中。

## 常見問題解答

### Q1：我可以為 PDF 以外的格式自訂筆選項嗎？

A1：是的，本教學中示範的筆自訂適用於各種影像格式，包括 PDF、PNG、BMP、GIF、JPEG2000、JPEG、PSD、TIFF 和 WMF。

### Q2: 如何處理不同的筆頭和尾蓋？

 A2：利用`PenOptions`類別來設定所需的起始端蓋和結束端蓋，為定義線條的外觀提供了靈活性。

### Q3：如果我不指定筆選項怎麼辦？

A3：如果沒有明確設定筆選項，系統將使用預設筆，在不同的上下文中，預設筆可能會有所不同。

### Q4：光柵化選項有具體的考量嗎？

A4：在光柵化選項中調整頁面寬度和高度，以控制匯出影像的尺寸。

### 問題 5：我可以在哪裡找到其他支持或社區討論？

 A5：探索 Aspose.CAD 社群論壇：[這裡](https://forum.aspose.com/c/cad/19)以尋求支持和討論。