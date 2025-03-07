---
title: 使用 Aspose.CAD for Java 將 DWG 匯出為 PDF 或光柵
linktitle: 將 DWG 匯出為 PDF 或光柵
second_title: Aspose.CAD Java API
description: 探索使用 Aspose.CAD 將 DWG 檔案匯出為 PDF 或 Java 光柵影像的無縫過程。本逐步指南可確保精度和效率。
weight: 13
url: /zh-hant/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.CAD for Java 將 DWG 匯出為 PDF 或光柵

## 介紹

在電腦輔助設計 (CAD) 的動態世界中，高效處理圖面至關重要。 Aspose.CAD for Java 提供了將 DWG 檔案匯出為 PDF 或光柵影像的強大解決方案。本教學將引導您完成整個過程，確保您充分利用 Aspose.CAD for Java 的潛力。

## 先決條件

在深入學習本教學之前，請確保您具備以下條件：

- 對 Java 程式設計有基本的了解。
- 安裝了 Aspose.CAD for Java 函式庫。如果沒有，請下載[這裡](https://releases.aspose.com/cad/java/).
- 用於測試目的的 DWG 檔。您可以使用提供的“Bottom_plate.dwg”檔案。

## 導入命名空間

在您的 Java 專案中，匯入必要的命名空間以啟動該過程：

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.UnitType;
```

## 步驟 1： 載入 DWG 文件

首先使用 Aspose.CAD 載入 DWG 文件`Image`班級：

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Bottom_plate.dwg";
Image objImage = Image.load(srcFile);
```

## 第 2 步：確定單位類型

接下來，檢查載入的 DWG 檔案的單位類型：

```java
Boolean currentUnitIsMetric = IsMetric(objImage.getUnitType());
int currentUnitCoefficient = objImage.getUnitType();
```

## 第 3 步：設定光柵化選項

根據單位類型，配置光柵化選項：

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();

if (currentUnitIsMetric) {
    //公制單位
    double metersCoeff = 1 / 1000.0;
    double scaleFactor = metersCoeff / currentUnitCoefficient;
    rasterizationOptions.setPageWidth((float)(210 * scaleFactor));
    rasterizationOptions.setPageHeight((float)(297 * scaleFactor));
    rasterizationOptions.setUnitType(UnitType.Millimeter);
} else {
    //英制單位
    rasterizationOptions.setPageWidth((float)(8.27f / currentUnitCoefficient));
    rasterizationOptions.setPageHeight((float)(11.69f / currentUnitCoefficient));
    rasterizationOptions.setUnitType(UnitType.Inch);
}
```

## 步驟 4：配置 PDF 選項

設定 PDF 匯出選項：

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());
```

## 第 5 步：另存為 PDF

最後，將 DWG 檔案儲存為 PDF：

```java
objImage.save(dataDir + "Saved.pdf", pdfOptions);
```

現在你就擁有了！您已使用 Aspose.CAD for Java 成功將 DWG 檔案匯出為 PDF。

## 結論

本教學提供了利用 Aspose.CAD for Java 將 DWG 檔案匯出為 PDF 或光柵影像的逐步指南。該程式庫簡化了流程，使您能夠在 Java 應用程式中有效地處理 CAD 繪圖。

## 常見問題解答

### Q1：我可以將 Aspose.CAD for Java 與其他 Java 框架一起使用嗎？

A1：是的，Aspose.CAD for Java 與流行的 Java 框架無縫整合。

### 問題 2：Aspose.CAD for Java 是否有臨時授權？

 A2：是的，您可以獲得臨時許可證[這裡](https://purchase.aspose.com/temporary-license/).

### 問題 3：在哪裡可以找到 Aspose.CAD for Java 的支援？

 A3：訪問[Aspose.CAD論壇](https://forum.aspose.com/c/cad/19)尋求社區的幫助。

### Q4：如何購買 Aspose.CAD for Java 的授權？

 A4：您可以購買許可證[這裡](https://purchase.aspose.com/buy).

### Q5：Aspose.CAD for Java 支援哪些單位？

A5：Aspose.CAD for Java 支援公制和英制單位。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
