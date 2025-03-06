---
title: Java 中 Aspose.CAD 對圖層的支持
linktitle: CAD 中圖層的支持
second_title: Aspose.CAD Java API
description: 使用 Aspose.CAD 進行 Java CAD 開發的主控層支援。輕鬆組織和匯出圖紙。
weight: 18
url: /zh-hant/java/advanced-cad-features/support-of-layers-in-cad/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java 中 Aspose.CAD 對圖層的支持

## 介紹

透過掌握圖層的支持，釋放 Java 中 Aspose.CAD 的全部潛力。圖層在 CAD 繪圖中起著至關重要的作用，可以有效地組織和操作圖形元素。在這個綜合教程中，我們將深入研究使用 Aspose.CAD 的圖層支援的複雜性，為您提供利用這項強大功能的逐步指南。

## 先決條件

在深入學習本教程之前，請確保您具備以下先決條件：

1.  Aspose.CAD for Java Library：從下列位置下載並安裝程式庫：[網站](https://releases.aspose.com/cad/java/)。按照安裝說明在您的 Java 環境中設定該庫。

2. Java 開發環境：確保您的電腦上安裝了 Java 開發環境。您可以從網站下載最新版本的 Java。

現在，讓我們探討一下在 Java 中利用 Aspose.CAD 的圖層支援的過程。

## 導入命名空間

首先匯入必要的命名空間來啟動您的專案：

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import java.util.ArrayList;
import java.util.Arrays;
import java.util.List;
```

現在，讓我們分解每個步驟以確保清晰的理解。

## 第 1 步：設定檔案路徑

定義 DWF 原始檔和所需輸出檔的路徑。確保指定目錄存在。

```java
String dataDir = "Your Document Directory" + "DWFDrawings/";
String srcFile = dataDir + "for_layers_test.dwf";
String outFile = dataDir + "for_layers_test.jpg";
```

## 第 2 步：載入 DWF 映像

使用 Aspose.CAD 載入 DWF 圖像`Image.load`方法。

```java
Image image = Image.load(srcFile);
```

## 步驟 3：配置光柵化選項

建立一個實例`CadRasterizationOptions`並自訂其屬性以滿足您的需求。

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
```

## 第 4 步：指定圖層

定義要包含在輸出中的圖層。在此範例中，我們將“LayerA”新增至清單中。

```java
List<String> stringList = new ArrayList<>(Arrays.asList("LayerA"));
rasterizationOptions.setLayers(stringList);
```

## 步驟 5：配置 JPEG 選項

設定 JPEG 選項，包括向量光柵化選項。

```java
JpegOptions jpegOptions = new JpegOptions();
jpegOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## 第 6 步：匯出為 JPG

使用以下命令將修改後的圖像儲存為 JPG 文件`image.save`方法。

```java
image.save(outFile, jpegOptions);
```

透過執行這些步驟，您已成功利用 Java 中的 Aspose.CAD 圖層支持，讓您可以操作和匯出具有特定圖層的 CAD 繪圖。

## 結論

恭喜！您現在已經掌握了 Java 中 Aspose.CAD 的圖層支援藝術。本教學為您提供了利用 Aspose.CAD 提供的強大圖層功能有效組織和匯出 CAD 繪圖的知識。

## 常見問題解答

### Q1：我可以在光柵化選項中新增多個圖層嗎？

 A1：當然！只需擴展`stringList`以及您想要包含的其他圖層的名稱。

### Q2: Aspose.CAD 是否相容於不同的 CAD 格式？

A2：是的，Aspose.CAD支援多種CAD格式，確保處理各種類型繪圖的多功能性。

### Q3：如何調整輸出影像尺寸？

 A3：修改`setPageWidth`和`setPageHeight`光柵化選項中的屬性可自訂輸出尺寸。

### 問題 4：Aspose.CAD 有可用的授權選項嗎？

 A4：是的，探索授權選項[這裡](https://purchase.aspose.com/buy)解鎖附加功能和支援。

### Q5：我可以在哪裡尋求協助或分享我使用 Aspose.CAD 的經驗？

A5：加入 Aspose.CAD 社區[論壇](https://forum.aspose.com/c/cad/19)支持和協作討論。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
