---
title: 使用 Aspose.CAD for Java 匯出為 BMP
linktitle: 匯出為 BMP
second_title: Aspose.CAD Java API
description: 使用 Aspose.CAD for Java 探索 CAD 到 BMP 的無縫轉換。遵循我們的逐步指南，實現高效、精確的導出。
weight: 12
url: /zh-hant/java/cad-export-options/export-to-bmp/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.CAD for Java 匯出為 BMP

## 介紹

在不斷發展的數位設計領域，將電腦輔助設計 (CAD) 檔案無縫匯出為各種格式的能力至關重要。 Aspose.CAD for Java 是一款功能強大的解決方案，為開發人員提供了將 CAD 檔案高效匯出為 BMP 格式所需的工具。本教學將逐步引導您完成整個過程，確保每次匯出順利成功。

## 先決條件

在深入學習本教程之前，請確保您具備以下先決條件：

- Aspose.CAD for Java 函式庫：從下列位置下載並安裝 Aspose.CAD for Java 函式庫：[這裡](https://releases.aspose.com/cad/java/).

- Java 開發環境：確保您的系統上設定了 Java 開發環境。

- 基本 Java 知識：熟悉基本 Java 程式設計概念。

## 導入命名空間

在您的 Java 專案中，匯入必要的命名空間以存取 Aspose.CAD 功能：

```java
import com.aspose.cad.Image;
import com.aspose.cad.InterpolationMode;
import com.aspose.cad.SmoothingMode;
import com.aspose.cad.TextRenderingHint;

import com.aspose.cad.imageoptions.BmpOptions;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//導入 com.aspose.cad.imageoptions.TypeOfEntities;
```

## 第1步：設定資源目錄路徑

首先定義 CAD 檔案所在資源目錄的路徑。

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
```

## 第 2 步：載入 CAD 文件

將 CAD 檔案載入到 Aspose.CAD 中`Image`目的。

```java
String fileName = (dataDir + "site.dwf");
Image image = Image.load(fileName);
```

## 步驟 3：配置 BMP 匯出選項

建立和配置 BMP 匯出選項，包括光柵化設定。

```java
BmpOptions bmpOptions = new BmpOptions();
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## 步驟 4：設定光柵化參數

定義頁面高度、頁面寬度和光柵化佈局等參數。

```java
rasterizationOptions.setPageHeight(500);
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setLayouts(new String[] { "Model" });
```

## 第5步：匯出為BMP

指定輸出路徑並儲存BMP檔。

```java
String outPath = dataDir + "site.bmp";
image.save(outPath, bmpOptions);
```

對您希望使用 Aspose.CAD for Java 匯出為 BMP 的每個 CAD 檔案重複這些步驟。

## 結論

使用 Aspose.CAD for Java 可以輕鬆將 CAD 檔案匯出為 BMP 格式。透過遵循此逐步指南，您可以將此功能無縫整合到您的 Java 應用程式中，確保高效且精確的轉換。

## 常見問題解答

### Q1：Aspose.CAD for Java適合批次處理嗎？

A1：當然！ Aspose.CAD for Java 支援批次，讓您可以同時有效率地處理多個 CAD 檔案。

### Q2：我可以為不同的佈局自訂光柵化選項嗎？

A2：是的，您可以根據您的特定要求自訂光柵化選項，例如頁面尺寸和佈局。

### 問題 3：在哪裡可以找到 Aspose.CAD for Java 的其他支援？

 A3：訪問[Aspose.CAD論壇](https://forum.aspose.com/c/cad/19)以獲得社區支持和討論。

### Q4：有免費試用嗎？

 A4：是的，您可以探索 Aspose.CAD for Java 的免費試用版[這裡](https://releases.aspose.com/).

### Q5：如何取得臨時駕照？

A5：取得 Aspose.CAD for Java 的臨時許可證[這裡](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
