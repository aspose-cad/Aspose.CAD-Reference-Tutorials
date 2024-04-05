---
title: 使用 Aspose.CAD 教學將 Java DGN 轉換為 JPEG
linktitle: 將 AutoCAD 格式的 DGN 匯出為光柵影像格式
second_title: Aspose.CAD Java API
description: 了解如何使用 Aspose.CAD 將 DGN 檔案匯出為 Java 中的 JPEG 影像。本逐步教學將引導您輕鬆完成整個過程。
type: docs
weight: 13
url: /zh-hant/java/dgn-export-options/exporting-dgn-to-raster-image/
---
## 介紹

歡迎閱讀使用 Aspose.CAD for Java 將 DGN（設計）檔案匯出為光柵圖像格式的綜合教學。 Aspose.CAD 是一個功能強大的函式庫，可讓 Java 開發人員無縫地處理 CAD 檔案。在本教程中，我們將引導您完成將 DGN 檔案轉換為 JPEG 影像的過程，並為您提供逐步說明和程式碼範例。

## 先決條件

在深入學習本教程之前，請確保您具備以下先決條件：
1.  Aspose.CAD 函式庫：確保您已安裝 Aspose.CAD for Java 函式庫。你可以下載它[這裡](https://releases.aspose.com/cad/java/).
2. Java 開發工具包 (JDK)：確保您的電腦上安裝了 Java。
3. 整合開發環境 (IDE)：使用與 Java 相容的 IDE，例如 IntelliJ 或 Eclipse。

## 導入包

在您的 Java 專案中，匯入 Aspose.CAD 所需的套件。將以下行加入您的程式碼：

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
```

## 第 1 步：載入 DGN 文件

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
DgnImage dgnImage = (DgnImage) Image.load(dataDir + "Nikon_D90_Camera.dgn");
```

## 步驟2：建立JpegOptions對象

```java
ImageOptionsBase options = new JpegOptions();
```

## 第 3 步：分配光柵化選項

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(600);
vectorOptions.setPageHeight(400);
vectorOptions.setNoScaling(true);
vectorOptions.setAutomaticLayoutsScaling(false);
options.setVectorRasterizationOptions(vectorOptions);
```

## 第四步：儲存轉換後的影像

```java
OutputStream outStream = new FileOutputStream(dataDir + "ExportDGNToRasterImage_Out.jpg");
dgnImage.save(outStream, options);
```

對特定 DGN 檔案重複這些步驟，並相應地調整檔案路徑。

## 結論

恭喜！您已成功學習如何使用 Aspose.CAD for Java 將 DGN 檔案匯出為光柵影像格式。本教學為您提供了將此功能合併到 Java 應用程式中的知識。

## 常見問題解答

### Q1：我可以將 Aspose.CAD for Java 與其他 CAD 檔案格式一起使用嗎？

A1：是的，Aspose.CAD支援各種CAD格式，為Java開發人員提供了多功能的解決方案。

### 問題 2：Aspose.CAD for Java 是否有免費試用版？

 A2：是的，您可以免費試用[這裡](https://releases.aspose.com/).

### 問題 3：在哪裡可以找到 Aspose.CAD for Java 的文檔？

 A3：參考文檔[這裡](https://reference.aspose.com/cad/java/).

### 問題 4：如何獲得 Aspose.CAD for Java 的支援？

 A4：造訪支援論壇[這裡](https://forum.aspose.com/c/cad/19).

### Q5：在哪裡可以購買 Aspose.CAD for Java 的授權？

 A5：您可以購買許可證[這裡](https://purchase.aspose.com/buy).