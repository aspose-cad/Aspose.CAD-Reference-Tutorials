---
date: 2026-02-23
description: 了解如何使用 Aspose.CAD for Java 將 DWFX 轉換為 PDF，並將 CAD 儲存為 PDF。快速指南：開啟 DWFX
  檔案並產生 PDF。
linktitle: Open DWFX File
second_title: Aspose.CAD Java API
title: 使用 Aspose.CAD for Java 將 DWFX 轉換為 PDF
url: /zh-hant/java/cad-file-manipulation/open-dwfx-file/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.CAD for Java 將 DWFX 轉換為 PDF

## 介紹

在當今快速變化的設計領域，開發人員常常需要 **將 DWFX 轉換為 PDF**，以便將 CAD 圖紙與非技術相關人員共享。Aspose.CAD for Java 讓這項工作變得簡單，只需幾行程式碼即可開啟 DWFX 檔案、光柵化，並 **將 CAD 儲存為 PDF**。本教學將逐步說明整個流程——從環境設定到驗證最終 PDF——讓您能在 Java 應用程式中自信地處理 DWFX 檔案。

## 快速解答
- **此指南的主要目的為何？** 示範如何使用 Aspose.CAD for Java 將 DWFX 轉換為 PDF。  
- **需要哪個函式庫？** Aspose.CAD for Java（從官方 Aspose 網站下載）。  
- **是否需要授權？** 開發時可使用免費試用版；正式上線需購買商業授權。  
- **能直接開啟 DWFX 檔案嗎？** 可以，使用 `Image.load` 開啟 DWFX 檔案。  
- **範例產生的輸出格式為何？** 產生 PDF 檔案，儲存於指定的輸出目錄。

## 什麼是「將 DWFX 轉換為 PDF」？

將 DWFX 轉換為 PDF 即是把常見於 Autodesk 產品的向量式 DWFX 圖紙，渲染成可攜帶且廣受支援的 PDF 文件。這讓接收者無需安裝 CAD 軟體即可輕鬆檢視、列印與分享。

## 為何使用 Aspose.CAD for Java **將 CAD 儲存為 PDF**？

- **無外部相依性：** 純 Java API，無需本機 CAD 引擎。  
- **高保真渲染：** 保留線寬、顏色與圖層。  
- **適合批次處理：** 非常適用於伺服器端自動化或雲端服務。  
- **跨平台：** 可在 Windows、Linux 與 macOS 上執行。

## 前置條件

在深入程式碼之前，請確保您已具備以下項目：

- **Aspose.CAD for Java 函式庫** – 從 [Aspose.CAD for Java 下載頁面](https://releases.aspose.com/cad/java/) 下載。  
- **Java 開發環境** – JDK 8 或更新版本，搭配您喜愛的 IDE 或建置工具。  
- **DWFX 檔案** – 用於測試轉換的範例 DWFX 檔案（例如 `Tyrannosaurus.dwfx`）。

## 匯入命名空間

首先，匯入我們需要的類別：

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## 使用 Aspose.CAD for Java 轉換 DWFX 為 PDF 的步驟

以下為逐步說明。每一步都包含簡短解說與您將執行的完整程式碼。

### 步驟 1：載入 DWFX 檔案  

```java
String SourceDir = Utils.getDataDir_DWFXDrawings();
String OutputDir = Utils.getDataDir_Output();
String filePath = SourceDir + "Tyrannosaurus.dwfx";

Image cadImageDwf = Image.load(filePath);
```

`Image.load` 方法會將 DWFX 檔案讀入記憶體，產生可供光柵化的 `CadImage` 物件。

### 步驟 2：設定光柵化選項  

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(cadImageDwf.getSize().getWidth());
rasterizationOptions.setPageHeight(cadImageDwf.getSize().getHeight());
```

這些選項定義輸出頁面的尺寸，確保 PDF 與原始圖紙的尺寸相符。

### 步驟 3：設定 PDF 選項  

```java
PdfOptions CADf = new PdfOptions();
CADf.setVectorRasterizationOptions(rasterizationOptions);
```

在此將光柵化設定綁定至 PDF 匯出配置。

### 步驟 4：儲存為 PDF  

```java
cadImageDwf.save(OutputDir + "OpenDwfxFile_out.pdf", CADf);
```

呼叫 `save` 後，會將渲染後的影像寫入輸出資料夾中的 PDF 檔案。

### 步驟 5：驗證成功  

```java
System.out.println("OpenDwfxFile executed successfully");
```

簡單的主控台訊息會確認轉換已順利完成且未發生錯誤。

## 常見問題與解決方案

| 問題 | 可能原因 | 解決方案 |
|-------|--------------|----------|
| **PDF 空白** | 光柵化寬度/高度設定為 0 | 確認在設定選項前 `cadImageDwf.getSize()` 取得有效的尺寸。 |
| **記憶體不足錯誤** | DWFX 檔案過大 | 增加 JVM 堆積大小（`-Xmx2g`）或將檔案分段處理。 |
| **缺少字型** | 原始 DWFX 未嵌入字型 | 在伺服器上安裝所需字型，或使用 `CadRasterizationOptions.setFontName` 指定備用字型。 |

## 常見問答

### Q1: 我可以在 Aspose.CAD for Java 中使用其他 CAD 檔案格式嗎？  
A1: 可以，Aspose.CAD for Java 支援多種 CAD 格式，為開發者提供多功能的解決方案。

### Q2: Aspose.CAD for Java 有提供免費試用嗎？  
A2: 有，您可透過免費試用體驗 Aspose.CAD for Java 的功能。請前往 [此連結](https://releases.aspose.com/) 開始使用。

### Q3: 我該如何取得 Aspose.CAD for Java 的支援？  
A3: 加入 Aspose.CAD 社群的 [支援論壇](https://forum.aspose.com/c/cad/19) 以獲得協助與交流。

### Q4: Aspose.CAD for Java 有提供臨時授權嗎？  
A4: 有，您可取得 Aspose.CAD for Java 的臨時授權。詳情請見 [此連結](https://purchase.aspose.com/temporary-license/)。

### Q5: 我在哪裡可以找到 Aspose.CAD for Java 的文件？  
A5: 完整文件可於 [此處](https://reference.aspose.com/cad/java/) 取得。

---

**最後更新：** 2026-02-23  
**測試環境：** Aspose.CAD for Java 24.11  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}