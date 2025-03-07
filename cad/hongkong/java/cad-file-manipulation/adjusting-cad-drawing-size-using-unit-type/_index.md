---
title: 使用 Aspose.CAD for Java 的單位類型調整 CAD 繪圖尺寸
linktitle: 使用單位類型調整 CAD 繪圖尺寸
second_title: Aspose.CAD Java API
description: 探索 Aspose.CAD for Java 輕鬆調整 CAD 繪圖尺寸的強大功能。請遵循我們的逐步指南，以實現精確性和適應性。
weight: 14
url: /zh-hant/java/cad-file-manipulation/adjusting-cad-drawing-size-using-unit-type/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.CAD for Java 的單位類型調整 CAD 繪圖尺寸

## 介紹

在不斷發展的電腦輔助設計 (CAD) 領域，精確度和適應性至關重要。一個常見的要求是根據特定的單元類型調整 CAD 圖紙的尺寸。 Aspose.CAD for Java 成為一個強大的盟友，提供以程式設計方式操作 CAD 檔案的無縫功能。

## 先決條件

在深入學習本教程之前，請確保您具備以下先決條件：

- Java 開發環境：確保您的電腦上設定了功能齊全的 Java 開發環境。

-  Aspose.CAD for Java 函式庫：下載 Aspose.CAD 函式庫並整合到您的 Java 專案中。您可以取得該庫[這裡](https://releases.aspose.com/cad/java/).

## 導入命名空間

在您的 Java 程式碼中，包含存取 Aspose.CAD 功能所需的命名空間。新增以下導入：

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

現在，讓我們將使用單位類型調整 CAD 繪圖尺寸的流程分解為易於管理的步驟：

## 第 1 步：定義資料目錄

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

設定 CAD 檔案所在目錄的路徑。

## 第 2 步：載入 CAD 圖紙

```java
String sourceFilePath = dataDir + "sample.dwg";
Image image = Image.load(sourceFilePath);
```

使用 Aspose.CAD 載入 CAD 繪圖`Image`班級。

## 第 3 步：建立 BMP 選項

```java
BmpOptions bmpOptions = new BmpOptions();
```

實例化`BmpOptions`用於將 CAD 佈局匯出為 BMP 格式的類別。

## 步驟 4：配置光柵化選項

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(cadRasterizationOptions);
```

建立一個實例`CadRasterizationOptions`並將其與`BmpOptions`用於向量光柵化。

## 第 5 步：設定單位類型

```java
cadRasterizationOptions.setUnitType(UnitType.Centimeter);
```

指定 CAD 繪圖所需的單位類型。在此範例中，我們將其設定為公分。

## 第 6 步：設定佈局

```java
cadRasterizationOptions.setLayouts(new String[] { "Model" });
```

定義匯出期間要考慮的佈局。在本例中，我們選擇了「模型」佈局。

## 第7步：匯出為BMP

```java
String outPath = sourceFilePath + ".bmp";
image.save(outPath, bmpOptions);
```

最後將修改後的CAD圖面儲存為BMP格式。

## 結論

透過 Aspose.CAD for Java，調整 CAD 繪圖尺寸變得輕而易舉。本教學將引導您完成整個過程，強調每個步驟對於獲得精確結果的重要性。

## 常見問題解答

### Q1：我可以將 Aspose.CAD for Java 與其他程式語言一起使用嗎？

A1：Aspose.CAD 主要支援 Java，但也有適用於其他語言（例如 .NET）的版本。

### 問題 2：Aspose.CAD 是否有任何授權選項？

 A2：是的，您可以探索授權選項並購買 Aspose.CAD[這裡](https://purchase.aspose.com/buy).

### Q3：Aspose.CAD 有免費試用版嗎？

 A3：當然，您可以免費試用[這裡](https://releases.aspose.com/).

### 問題 4：如何獲得 Aspose.CAD for Java 的支援？

 A4：造訪 Aspose.CAD 論壇[這裡](https://forum.aspose.com/c/cad/19)以獲得全面的支援。

### Q5：我可以獲得 Aspose.CAD 的臨時授權嗎？

 A5：是的，您可以獲得臨時許可證[這裡](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
