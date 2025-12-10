---
date: 2025-12-10
description: 學習如何使用 Aspose.CAD for Java 及筆刷自訂功能，將 CAD 轉換為 PDF。本分步說明指南展示了高效匯出 CAD 為
  PDF 的方法。
linktitle: Pen Support in Export
second_title: Aspose.CAD Java API
title: 如何在匯出時使用筆支援從 CAD 產生 PDF
url: /zh-hant/java/advanced-cad-features/pen-support-in-export/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 匯出時的筆支援

## 介紹

在 CAD 轉換這個快速變化的領域，開發者常常需要 **create PDF from CAD** 檔案，同時保留視覺忠實度。Aspose.CAD for Java 讓這個過程變得簡單，提供豐富的選項，例如筆的自訂功能，讓您在匯出過程中微調線條樣式。本文將手把手示範完整範例，說明如何 **export CAD to PDF** 並使用自訂筆設定，讓您直接從 DXF 圖面產生精緻的 PDF。

## 快速解答
- **「create PDF from CAD」是什麼意思？** 將 CAD 圖面（例如 DXF）轉換為 PDF 文件，同時保留向量品質。  
- **哪個類別負責筆的自訂？** Aspose.CAD for Java 的 `PenOptions` 類別。  
- **可以套用到其他格式嗎？** 可以——相同的筆設定也適用於 PNG、BMP、TIFF 等格式。  
- **需要授權嗎？** 生產環境必須使用有效的 Aspose.CAD 授權。  
- **最低需要哪個 Java 版本？** Java 8 或更高。

## 「create PDF from CAD」是什麼意思？
將 CAD 圖面匯出為 PDF，意指將 CAD 圖形以向量或點陣方式渲染成 PDF 檔案。這樣可以輕鬆分享、列印與保存工程設計，而不需要收件者安裝 CAD 軟體。

## 為什麼在匯出 CAD 為 PDF 時要使用筆支援？
筆支援讓您能控制線條的端點、接合方式與粗細，從而符合企業品牌或技術圖面標準。當預設的線條渲染無法滿足視覺需求時，這項功能特別有用。

## 前置條件

- **Java 開發環境** – 已安裝 JDK（8 版或更新）以及您慣用的 IDE 或建置工具。  
- **Aspose.CAD 程式庫** – 從官方網站 [here](https://releases.aspose.com/cad/java/) 下載最新的 JAR。  
- **範例 DXF 檔案** – 本教學使用 `conic_pyramid.dxf`。

現在已完成前置設定，讓我們進入程式碼部分。

## 匯入命名空間

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.PenOptions;
import com.aspose.cad.internal.imaging.LineCap;
```

## 步驟 1：定義文件目錄

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

> **專業提示：** 請將 `"Your Document Directory"` 替換為存放 DXF 檔案的絕對路徑。

## 步驟 2：載入 CAD 檔案

```java
String srcFile = dataDir + "conic_pyramid.dxf";
CadImage cadImage = (CadImage) Image.load(srcFile);
```

`Image.load` 方法會讀取 DXF 檔案，並建立可供操作的 `CadImage` 物件。

## 步驟 3：設定點陣化選項

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(cadImage.getWidth() * 100);
rasterizationOptions.setPageHeight(cadImage.getHeight() * 100);
```

調整頁面尺寸即可控制最終 PDF 的解析度。將尺寸乘以 100 可產生適合列印的高解析度輸出。

## 步驟 4：自訂筆選項

```java
PenOptions penOts = new PenOptions();
penOts.setStartCap(LineCap.Flat);
penOts.setEndCap(LineCap.Flat);
```

此處將筆的起始與結束端點皆設定為 `Flat`。您也可以嘗試其他 `LineCap` 值（例如 `Round`、`Square`）以取得不同的視覺效果。

## 步驟 5：設定 PDF 匯出選項

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

`PdfOptions` 物件將點陣化設定與 PDF 匯出流程結合。

## 步驟 6：儲存匯出的 PDF

```java
cadImage.save((dataDir + "9LHATT-A56_generated.pdf"), pdfOptions);
```

執行此行程式碼後，會在 `dataDir` 資料夾中產生名為 `9LHATT-A56_generated.pdf` 的 PDF，並套用您先前定義的筆樣式。

## 常見使用情境

- **技術文件** – 在 PDF 手冊中嵌入精確的工程圖面。  
- **自動化報表** – 在 Web 服務中即時從 CAD 資料產生 PDF。  
- **品質管控** – 使用自訂線端點突顯測量線或公差。

## 疑難排解與技巧

- **檔案路徑錯誤** – 請確保 `dataDir` 以檔案分隔符（`/` 或 `\\`）結尾。  
- **缺少授權** – 未授權時程式會以評估模式執行，可能會加入浮水印。  
- **線條樣式異常** – 請再次確認在呼叫 `save` 前已設定 `PenOptions`，否則會使用預設筆。

## 常見問題

### Q1：可以為 PDF 以外的格式自訂筆選項嗎？

A1：可以，本文示範的筆自訂同樣適用於多種影像格式，包括 PDF、PNG、BMP、GIF、JPEG2000、JPEG、PSD、TIFF 與 WMF。

### Q2：如何為筆設定不同的起始與結束端點？

A2：使用 `PenOptions` 類別分別設定 `StartCap` 與 `EndCap`，即可靈活定義線條外觀。

### Q3：如果不指定筆選項會發生什麼？

A3：若未明確設定筆選項，系統會使用預設筆，且在不同情境下可能會有差異。

### Q4：點陣化選項有什麼需要特別注意的地方？

A4：可透過調整點陣化選項中的頁寬與頁高，來控制匯出影像的尺寸。

### Q5：在哪裡可以取得更多支援或社群討論？

A5：請前往 Aspose.CAD 社群論壇 [here](https://forum.aspose.com/c/cad/19) 獲取支援與討論。

---

**最後更新：** 2025-12-10  
**測試環境：** Aspose.CAD 24.11 for Java  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}