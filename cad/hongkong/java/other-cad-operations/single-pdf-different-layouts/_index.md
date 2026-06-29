---
date: 2026-06-29
description: 了解如何使用 Aspose.CAD for Java 從 DWG 建立 PDF 並自訂 PDF 版面配置。為 Java 開發人員提供簡易整合。
keywords:
- create pdf from dwg
- convert cad to pdf
- pdf different page sizes
- export dwg to pdf
- customize pdf layout
linktitle: 單一 PDF 具備不同版面配置
schemas:
- author: Aspose
  dateModified: '2026-06-29'
  description: Learn how to create PDF from DWG and customize PDF layout using Aspose.CAD
    for Java. Easy integration for Java developers.
  headline: Create PDF from DWG with Aspose.CAD for Java
  type: TechArticle
- questions:
  - answer: Yes, Aspose.CAD for Java integrates seamlessly with libraries such as
      Apache POI, Jackson, or Spring Boot.
    question: Can I use Aspose.CAD for Java with other Java libraries?
  - answer: Absolutely! You can access a free trial version [here](https://releases.aspose.com/).
    question: Is there a trial version available?
  - answer: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for community
      support and discussions.
    question: Where can I find additional support?
  - answer: You can obtain a temporary license [here](https://purchase.aspose.com/temporary-license/).
    question: How do I obtain a temporary license?
  - answer: Purchase the full version of Aspose.CAD for Java [here](https://purchase.aspose.com/buy).
    question: Where can I purchase the full version?
  type: FAQPage
second_title: Aspose.CAD Java API
title: 使用 Aspose.CAD for Java 從 DWG 建立 PDF
url: /zh-hant/java/other-cad-operations/single-pdf-different-layouts/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.CAD for Java 從 DWG 建立 PDF

## 簡介

在本教學中，您將 **從 DWG 建立 PDF**，並使用 Aspose.CAD for Java 套用多種頁面尺寸版面。無論您需要產生建築藍圖、工程圖或行銷用 PDF，以下步驟將示範如何將 CAD 圖面轉換為 PDF、自訂每個版面的尺寸，並產生單一多頁文件，全部在 Java 環境中完成。

## 快速解答
- **本教學涵蓋什麼？** 將 DWG 圖面轉換為單一 PDF，並支援多種頁面尺寸。  
- **需要哪個函式庫？** Aspose.CAD for Java（最新版本）。  
- **我需要授權嗎？** 免費試用可用於開發；正式上線需購買商業授權。  
- **我可以匯出其他格式嗎？** 可以——API 亦支援匯出為 PNG、JPEG 與 SVG。  
- **Java 8 足夠嗎？** 此函式庫相容於 Java 8 及更新的執行環境。

## 「從 DWG 建立 PDF」是什麼？

**從 DWG 建立 PDF** 意指將原生 AutoCAD DWG 檔案轉換為 PDF 文件，同時保留向量精度、圖層與線寬，並允許版面自訂。Aspose.CAD 完全在記憶體中執行此轉換，無需外部 CAD 軟體，且產生的 PDF 可直接編輯或列印。

## 為何要自訂 DWG 的 PDF 版面？

Aspose.CAD 支援 **30+ CAD 格式**，且可產生最高 **500 MB** 的 PDF 而不必將整個檔案載入記憶體。透過為每個版面定義個別頁面尺寸，您可以產出符合 ISO、ANSI 或自訂尺寸的可列印圖紙——此量化效益可節省時間並消除手動後處理。

## 前置條件

在開始之前，請確保具備以下前置條件：
- Java 環境：確保您的機器已安裝 Java。  
- Aspose.CAD 函式庫：從 [download link](https://releases.aspose.com/cad/java/) 下載並安裝 Aspose.CAD for Java 函式庫。  
- 文件目錄：為您的 DWG 圖面建立一個目錄。

## 匯入套件

`CadImage` 類別是 Aspose.CAD 的核心物件，代表記憶體中的 CAD 圖面。請在開始前匯入所需的命名空間：

```java
import com.aspose.cad.Image;
import com.aspose.cad.SizeF;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.VectorRasterizationOptions;
```

## 步驟 1：載入 CAD 圖面

`CadImage` 載入 DWG 檔案並提供向量資料存取。首先將 CAD 圖面載入至 `CadImage` 物件：

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
CadImage cadImage = (CadImage)Image.load(dataDir + "City skyway map.dwg");
```

## 步驟 2：設定光柵化選項

`RasterizationOptions` 定義在放入 PDF 前，CAD 向量如何被光柵化。為 CAD 圖像設定光柵化選項：

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1000);
rasterizationOptions.setPageHeight(1000);
```

## 步驟 3：自訂版面頁面尺寸

`PdfOptions` 讓您為 DWG 內的每個版面指派不同的頁面尺寸。為 CAD 圖面的多個版面定義自訂尺寸：

```java
rasterizationOptions.getLayoutPageSizes().addItem("ANSI C Plot", new SizeF(500, 1000));
rasterizationOptions.getLayoutPageSizes().addItem("8.5 x 11 Plot", new SizeF(1000, 100));
```

## 步驟 4：設定 PDF 選項

`PdfOptions` 是結合光柵化設定與版面定義的容器。設定 PDF 選項，並納入光柵化設定：

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## 步驟 5：另存為 PDF

`PdfSaveOptions` 完成轉換並寫入輸出檔案。將處理過的 CAD 圖像另存為 PDF：

```java
cadImage.save(dataDir + "singlePDF_out.pdf", pdfOptions);
```

恭喜！您已成功使用 Aspose.CAD for Java，透過不同頁面尺寸 **從 DWG 建立 PDF**。

## 常見問題與解決方案

- **輸出 PDF 出現空白頁** – 請確認 `PageSize` 值與 DWG 檔案中實際版面尺寸相符。  
- **大型圖面記憶體不足錯誤** – 使用 `CadImage.load(..., LoadOptions)` 並搭配 `LoadOptions.setLoadMode(LoadMode.Memory)` 以串流方式讀取檔案，而非一次載入全部。  
- **縮放不正確** – 調整 `RasterizationOptions.setPageWidth` 與 `setPageHeight` 以符合目標 DPI（每英吋點數）。

## 常見問與答

**Q: 我可以將 Aspose.CAD for Java 與其他 Java 函式庫一起使用嗎？**  
A: 可以，Aspose.CAD for Java 可與 Apache POI、Jackson 或 Spring Boot 等函式庫無縫整合。

**Q: 有提供試用版嗎？**  
A: 當然！您可在此取得免費試用版 [此處](https://releases.aspose.com/)。

**Q: 我可以在哪裡取得額外支援？**  
A: 您可前往 [Aspose.CAD 論壇](https://forum.aspose.com/c/cad/19) 取得社群支援與討論。

**Q: 我該如何取得臨時授權？**  
A: 您可在 [此處](https://purchase.aspose.com/temporary-license/) 取得臨時授權。

**Q: 我可以在哪裡購買完整版本？**  
A: 您可在 [此處](https://purchase.aspose.com/buy) 購買 Aspose.CAD for Java 完整版本。

**最後更新：** 2026-06-29  
**測試環境：** Aspose.CAD for Java 24.10  
**作者：** Aspose

## 相關教學

- [使用 Aspose.CAD for Java 匯出 DWG 為 PDF 或光柵圖像](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [使用 Aspose.CAD for Java 匯出 CAD 版面為 PDF](/cad/java/cad-export-options/export-cad-layouts-to-pdf/)
- [使用 Aspose.CAD for Java 匯出特定 DWG 版面為 PDF](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< blocks/products/products-backtop-button >}}
{{< /blocks/products/pf/main-wrap-class >}}