---
title: 在 CAD 繪圖中新增浮水印 - Aspose.CAD for Java 教學課程
linktitle: 加浮水印
second_title: Aspose.CAD Java API
description: 使用 Aspose.CAD for Java 透過個人化浮水印增強您的 CAD 繪圖。請按照我們的逐步指南進行無縫整合。
type: docs
weight: 12
url: /zh-hant/java/other-cad-operations/add-watermark/
---
## 介紹

歡迎閱讀這份使用 Aspose.CAD for Java 為 CAD 繪圖新增浮水印的綜合指南。在本教程中，您將學習如何有效地整合浮水印，透過個人化訊息或品牌增強您的 CAD 文件。 Aspose.CAD for Java 提供了一組強大的功能，讓水印新增過程變得簡單。

## 先決條件

在我們深入學習本教程之前，請確保您符合以下先決條件：

-  Aspose.CAD for Java：確保您的 Java 環境中安裝了 Aspose.CAD 函式庫。你可以下載它[這裡](https://releases.aspose.com/cad/java/).
- Java 開發工具包 (JDK)：確保您的系統上安裝了最新版本的 JDK。

## 導入包

在您的 Java 專案中，匯入必要的 Aspose.CAD 套件以開始使用：

```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.Cad3DPoint;
import com.aspose.cad.fileformats.cad.cadobjects.CadMText;
import com.aspose.cad.fileformats.cad.cadobjects.CadText;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## 第 1 步：新增新的多行文本

```java
//新增的多行文本
CadMText watermark = new CadMText();
watermark.setText("Watermark message");
watermark.setInitialTextHeight(40);
watermark.setInsertionPoint(new Cad3DPoint(300, 40));
watermark.setLayerName("0");
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(watermark);
```

## 第 2 步：新增簡單實體（例如文字）

您也可以新增更簡單的實體，例如文字：

```java
//或添加更簡單的實體，例如文本
CadText text = new CadText();
text.setDefaultValue("Watermark text");
text.setTextHeight(40);
text.setFirstAlignment(new Cad3DPoint(300, 40));
text.setLayerName("0") ;
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(text);
```

## 第 3 步：匯出為 PDF

將新增浮水印的 CAD 繪圖匯出到 PDF 檔案：

```java
//導出為 pdf
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
rasterizationOptions.setLayouts(new String[]{"Model"});
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
cadImage.save(dataDir + "AddWatermark_out.pdf", pdfOptions);

```

## 結論

恭喜！您已使用 Aspose.CAD for Java 成功為 CAD 繪圖新增浮水印。這個簡單而強大的過程允許您個性化您的設計或透過品牌保護它們。

## 常見問題解答

### Q1：Aspose.CAD 是否相容於所有 CAD 檔案格式？

A1：Aspose.CAD支援多種CAD格式，包括DWG、DXF、DWT和DWF。

### Q2：我可以自訂浮水印文字的外觀嗎？

A2：是的，您可以完全控制浮水印的外觀，包括文字大小、顏色和位置。

### Q3：Aspose.CAD for Java 有試用版嗎？

 A3：是的，您可以下載試用版[這裡](https://releases.aspose.com/).

### Q4：如何獲得 Aspose.CAD 的支援？

 A4：訪問[Aspose.CAD論壇](https://forum.aspose.com/c/cad/19)以獲得社區支持。

### Q5：在哪裡可以找到 Aspose.CAD for Java 的完整文件？

 A5：請參閱[文件](https://reference.aspose.com/cad/java/)獲取詳細資訊。