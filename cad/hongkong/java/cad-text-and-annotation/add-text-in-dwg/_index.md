---
date: 2026-02-28
description: 學習如何使用 Aspose.CAD for Java 從 DWG 產生 PDF、將 DWG 另存為 PDF，並在 DWG 圖面中加入文字——一步步教學指南。
linktitle: Add Text in DWG
second_title: Aspose.CAD Java API
title: 使用 Aspose.CAD for Java 從 DWG 產生 PDF 並加入文字
url: /zh-hant/java/cad-text-and-annotation/add-text-in-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.CAD for Java 從 DWG 建立 PDF 並加入文字

## 介紹

如果您需要 **從 DWG 建立 PDF** 並同時插入自訂文字，您來對地方了。在本教學中，我們將完整示範整個流程——載入 DWG 圖紙、加入文字註解，最後使用 Aspose.CAD for Java 將結果儲存為 PDF。完成後，您將了解如何 **將 DWG 儲存為 PDF**、自訂文字高度，甚至加入基本註解。

## 快速解答
- **我可以在 Java 中將 DWG 轉換為 PDF 嗎？** 是的，Aspose.CAD for Java 提供簡單的 API。  
- **我需要商業授權才能在正式環境使用嗎？** 需要商業授權；亦提供免費試用版。  
- **哪個方法可在 DWG 中加入文字？** 使用 `CadText` 物件並將其加入模型空間。  
- **我可以設定文字高度嗎？** 當然可以——在 `CadText` 實例上使用 `setTextHeight()`。  
- **輸出是向量格式嗎？** 當光柵化選項設定為 `UseObjectColor` 時，PDF 會保留高品質向量資料。

## 什麼是「從 DWG 建立 PDF」？
將 DWG 圖紙轉換為 PDF 意味著把原生 CAD 格式轉成一種廣泛支援、唯讀的文件，同時保留原始幾何形狀。當您需要與沒有 CAD 軟體的利害關係人分享設計時，這種轉換是必不可少的。

## 為什麼使用 Aspose.CAD for Java 轉換 DWG 為 PDF？
Aspose.CAD 提供純 Java 解決方案，無需額外安裝 CAD 軟體。它支援 **convert DWG to PDF**，保持向量忠實度，且允許您在轉換前以程式方式加入文字、尺寸或自訂圖形等註解。

## 前置條件

在開始教學之前，請確保已具備以下條件：

- Aspose.CAD for Java 程式庫：從 [Aspose.CAD for Java page](https://releases.aspose.com/cad/java/) 下載並安裝程式庫。

- Java Development Kit (JDK)：確保系統已安裝最新的 JDK。

- DWG 圖紙：準備要加入文字的 DWG 圖檔。

## 匯入命名空間

在您的 Java 程式碼中，匯入 Aspose.CAD 所需的命名空間：

```java
import com.aspose.cad.Image;


import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadText;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

現在，讓我們將提供的程式碼片段拆解成多個步驟：

## 步驟 1：設定文件目錄與 DWG 檔案路徑

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String dwgPathToFile = dataDir + "SimpleEntites.dwg";
```

## 步驟 2：載入 DWG 圖像

```java
Image image = Image.load(dwgPathToFile);
```

## 步驟 3：建立 CadText 物件（在 DWG 中加入文字）

```java
CadText cadText = new CadText();
cadText.setStyleType("Standard");
cadText.setDefaultValue("Some custom text");
cadText.setColorId(256);
cadText.setLayerName("0");
cadText.getFirstAlignment().setX(47.9);
cadText.getFirstAlignment().setY(5.56);
cadText.setTextHeight(0.8);          // set text height in DWG units
cadText.setScaleX(0);
```

## 步驟 4：將文字加入 CadImage（插入註解）

```java
CadImage cadImage = ((CadImage)(image));
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(cadText);
```

## 步驟 5：設定 PDF 選項（準備從 DWG 建立 PDF）

```java
PdfOptions pdfOptions = new PdfOptions();
```

## 步驟 6：配置 CadRasterizationOptions（控制 PDF 渲染）

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
cadRasterizationOptions.setPageHeight(1600);
cadRasterizationOptions.setPageWidth(1600);
cadRasterizationOptions.setLayouts(new String[] {"Model"});
```

## 步驟 7：將修改後的 DWG 儲存為 PDF（dwg to pdf java）

```java
image.save(dataDir + "SimpleEntites_generated.dwg.pdf", pdfOptions);
```

按照這些步驟，您即可 **從 DWG 建立 PDF**，加入自訂文字，並控制文字高度——只需幾行 Java 程式碼。

## 如何在 Java 中大規模轉換 DWG 為 PDF？
如果您需要 **批次轉換 DWG PDF** 檔案，請將上述程式碼包在迴圈中，遍歷 DWG 圖紙資料夾。僅在必要時調整 `pageHeight`/`pageWidth` 以降低記憶體使用，並為每個檔案重複使用同一個 `PdfOptions` 實例以提升效能。

## 常見問題與技巧

- **文字未顯示？** 請確認 X/Y 座標位於圖紙範圍內且圖層可見。  
- **文字高度不正確？** 調整 `setTextHeight()`；數值使用圖紙的單位系統。  
- **PDF 看起來是光柵化的？** 確認已設定 `CadDrawTypeMode.UseObjectColor` 以保留向量資訊。  
- **大型檔案的效能？** 僅在必要時增加 `pageHeight`/`pageWidth`；較大的值會佔用更多記憶體。

## 常見問答

**Q: Aspose.CAD 是否相容所有版本的 DWG 檔案？**  
A: Aspose.CAD 支援多種 DWG 版本，確保與廣泛的 CAD 軟體相容。

**Q: 我可以自訂加入文字的字型與格式嗎？**  
A: 可以，您可使用 Aspose.CAD 自訂字型、樣式及其他格式設定。

**Q: 是否提供 Aspose.CAD for Java 的免費試用？**  
A: 有的，您可從 [here](https://releases.aspose.com/) 取得免費試用版以探索功能。

**Q: 哪裡可以找到 Aspose.CAD for Java 的詳細文件？**  
A: 請參考文件 [here](https://reference.aspose.com/cad/java/) 以取得深入資訊與範例。

**Q: 我要如何取得 Aspose.CAD 的支援或協助？**  
A: 前往 [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) 取得協助，並與社群互動。

---

**最後更新：** 2026-02-28  
**測試環境：** Aspose.CAD for Java 24.12  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}