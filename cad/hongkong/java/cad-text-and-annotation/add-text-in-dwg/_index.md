---
title: 使用 Aspose.CAD for Java 在 DWG 中新增文本
linktitle: 在 DWG 中加入文本
second_title: Aspose.CAD Java API
description: 使用 Aspose.CAD for Java 輕鬆增強您的 DWG 繪圖。使用我們的逐步指南無縫添加文字。
weight: 10
url: /zh-hant/java/cad-text-and-annotation/add-text-in-dwg/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.CAD for Java 在 DWG 中新增文本

## 介紹

在電腦輔助設計 (CAD) 領域，Aspose.CAD for Java 作為操作和轉換 DWG 繪圖的強大工具脫穎而出。其方便的功能之一是能夠將文字無縫添加到 DWG 檔案中。在本教程中，我們將引導您完成使用 Aspose.CAD for Java 將文字新增至 DWG 繪圖的過程。

## 先決條件

在深入學習本教程之前，請確保您具備以下先決條件：

-  Aspose.CAD for Java Library：從下列位置下載並安裝程式庫：[Aspose.CAD for Java 頁面](https://releases.aspose.com/cad/java/).

- Java 開發工具包 (JDK)：確保您的系統上安裝了最新的 JDK。

- DWG 繪圖：準備要新增文字的 DWG 繪圖檔案。

## 導入命名空間

在您的 Java 程式碼中，匯入 Aspose.CAD 所需的命名空間：

```java
import com.aspose.cad.Image;


import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadText;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

現在，讓我們將提供的程式碼片段分解為多個步驟：

## 步驟 1： 設定文件目錄和 DWG 檔案路徑

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String dwgPathToFile = dataDir + "SimpleEntites.dwg";
```

## 步驟 2： 載入 DWG 映像

```java
Image image = Image.load(dwgPathToFile);
```

## 第 3 步：建立 CadText 對象

```java
CadText cadText = new CadText();
cadText.setStyleType("Standard");
cadText.setDefaultValue("Some custom text");
cadText.setColorId(256);
cadText.setLayerName("0");
cadText.getFirstAlignment().setX(47.9);
cadText.getFirstAlignment().setY(5.56);
cadText.setTextHeight(0.8);
cadText.setScaleX(0);
```

## 步驟 4：將文字新增至 CadImage

```java
CadImage cadImage = ((CadImage)(image));
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(cadText);
```

## 第 5 步：設定 PDF 選項

```java
PdfOptions pdfOptions = new PdfOptions();
```

## 步驟 6：配置 CadRasterizationOptions

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
cadRasterizationOptions.setPageHeight(1600);
cadRasterizationOptions.setPageWidth(1600);
cadRasterizationOptions.setLayouts(new String[] {"Model"});
```

## 步驟 7：將修改後的 DWG 儲存為 PDF

```java
image.save(dataDir + "SimpleEntites_generated.dwg.pdf", pdfOptions);
```

透過執行這些步驟，您將能夠使用 Aspose.CAD for Java 將文字無縫地新增至 DWG 繪圖。

## 結論

Aspose.CAD for Java 使開發人員能夠以程式設計方式增強和修改 DWG 繪圖。本教學提供了為 DWG 檔案添加文字的清晰逐步指南，展示了 Aspose.CAD 的簡單性和強大功能。

## 常見問題解答

### Q1：Aspose.CAD 是否相容於所有版本的 DWG 檔案？

A1：Aspose.CAD支援各種版本的DWG文件，確保與各種CAD軟體相容。

### Q2：我可以自訂新增文字的字體和格式嗎？

A2：是的，您可以使用 Aspose.CAD 自訂新增至 DWG 檔案中的文字的字體、樣式和其他格式選項。

### 問題 3：Aspose.CAD for Java 是否有免費試用版？

 A3：是的，您可以透過取得免費試用版來探索 Aspose.CAD 的功能[這裡](https://releases.aspose.com/).

### Q4：在哪裡可以找到 Aspose.CAD for Java 的詳細文件？

A4：參考文檔[這裡](https://reference.aspose.com/cad/java/)獲取深入的資訊和範例。

### Q5：我如何獲得 Aspose.CAD 的支援或尋求協助？

A5：訪問[Aspose.CAD論壇](https://forum.aspose.com/c/cad/19)獲得協助並與社區建立聯繫。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
