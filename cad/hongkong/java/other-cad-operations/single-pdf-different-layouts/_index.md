---
title: 使用 Aspose.CAD for Java 製作動態 PDF
linktitle: 具有不同佈局的單一 PDF
second_title: Aspose.CAD Java API
description: 使用 Aspose.CAD for Java 從 CAD 繪圖建立具有不同佈局的精美 PDF。為 Java 開發人員提供輕鬆整合和強大的功能。
weight: 16
url: /zh-hant/java/other-cad-operations/single-pdf-different-layouts/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.CAD for Java 製作動態 PDF

## 介紹

歡迎來到 Aspose.CAD for Java 的世界，這是一個功能強大的函式庫，讓開發人員能夠輕鬆操作 CAD 繪圖。在本教程中，我們將深入研究使用 Aspose.CAD for Java 建立具有不同佈局的單一 PDF。無論您是經驗豐富的開發人員還是新手，本逐步指南都將引導您完成整個過程。

## 先決條件

在我們開始這趟旅程之前，請確保您具備以下先決條件：
- Java 環境：確保您的電腦上安裝了 Java。
-  Aspose.CAD 函式庫：從下列位置下載並安裝 Java 的 Aspose.CAD 函式庫：[下載連結](https://releases.aspose.com/cad/java/).
- 文件目錄：為 DWG 工程圖設定目錄。

## 導入包

在您的 Java 專案中，匯入必要的套件：

```java
import com.aspose.cad.Image;
import com.aspose.cad.SizeF;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.VectorRasterizationOptions;
```

## 第 1 步：載入 CAD 圖紙

首先將 CAD 繪圖載入到`CadImage`目的：

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
CadImage cadImage = (CadImage)Image.load(dataDir + "City skyway map.dwg");
```

## 第 2 步：配置光柵化選項

設定 CAD 影像的光柵化選項：

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1000);
rasterizationOptions.setPageHeight(1000);
```

## 第 3 步：自訂佈局頁面大小

為 CAD 繪圖中的多個佈局定義自訂尺寸：

```java
rasterizationOptions.getLayoutPageSizes().addItem("ANSI C Plot", new SizeF(500, 1000));
rasterizationOptions.getLayoutPageSizes().addItem("8.5 x 11 Plot", new SizeF(1000, 100));
```

## 步驟 4：設定 PDF 選項

配置 PDF 選項，合併光柵化設定：

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## 第 5 步：另存為 PDF

將處理後的 CAD 影像儲存為 PDF：

```java
cadImage.save(dataDir + "singlePDF_out.pdf", pdfOptions);
```

恭喜！您已使用 Aspose.CAD for Java 成功建立了具有不同佈局的單一 PDF。

## 結論

在本教程中，我們探索了 Aspose.CAD for Java 的無縫集成，以從 CAD 繪圖生成具有不同佈局的 PDF。該程式庫的靈活性和強大功能使其成為 CAD 操作任務的首選。

## 常見問題解答

### Q1：我可以將 Aspose.CAD for Java 與其他 Java 函式庫一起使用嗎？

A1：是的，Aspose.CAD for Java 旨在與其他 Java 程式庫無縫集成，提供廣泛的功能。

### Q2：有試用版嗎？

 A2：當然！您可以存取免費試用版[這裡](https://releases.aspose.com/).

### Q3：我可以在哪裡找到額外的支援？

 A3：訪問[Aspose.CAD論壇](https://forum.aspose.com/c/cad/19)以獲得社區支持和討論。

### Q4：如何取得臨時駕照？

 A4：您可以獲得臨時許可證[這裡](https://purchase.aspose.com/temporary-license/).

### Q5：哪裡可以購買完整版？

A5：購買完整版的 Aspose.CAD for Java[這裡](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
