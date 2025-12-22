---
date: 2025-12-22
description: 了解如何在 Java 中使用 Aspose.CAD 匯出 CAD 圖紙並將 DWG 轉換為 BMP。請遵循此一步一步的指南，以高效操作 CAD
  檔案。
linktitle: Auto Adjusting CAD Drawing Size
second_title: Aspose.CAD Java API
title: 如何使用 Aspose.CAD for Java 將 CAD 繪圖匯出為 BMP
url: /zh-hant/java/cad-file-manipulation/auto-adjusting-cad-drawing-size/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何使用 Aspose.CAD for Java 將 CAD 圖紙匯出為 BMP

## 介紹

如果您正在尋找一種清晰、可靠的 **how to export cad** 方法，從 Java 匯出 CAD 檔案，您來對地方了。使用 Aspose.CAD for Java，您不僅可以自動調整圖紙尺寸，還能在幾行程式碼內 **convert DWG to BMP**。本教學將帶您完成整個流程，從環境設定到產生保留原始 CAD 版面的 BMP 圖像。

## 快速解答
- **「how to export cad」是什麼意思？** 它指的是將 CAD 檔案（DWG、DXF 等）轉換為其他格式，如 BMP、PNG 或 PDF。  
- **哪個函式庫負責轉換？** Aspose.CAD for Java 提供簡易的 API 完成此任務。  
- **需要授權嗎？** 測試時可使用臨時授權；正式上線則需購買正式授權。  
- **可以一次匯出多個版面嗎？** 可以——設定 `Layouts` 屬性即可指定要渲染的版面。  
- **BMP 是唯一的輸出格式嗎？** 不是——您也可以匯出為 PNG、JPEG、TIFF 等多種格式。

## 什麼是使用 Aspose.CAD 的 **how to export cad**？
匯出 CAD 意味著將原生 CAD 圖紙（例如 DWG 檔）渲染成點陣圖或其他向量格式。Aspose.CAD 會處理所有繁重工作：解析 CAD 結構、光柵化向量實體，並將結果寫入您選擇的圖像格式。

## 為什麼要使用 Aspose.CAD for Java 來 **convert DWG to BMP**？
- **無外部相依** – 純 Java，無需本機 DLL。  
- **完整支援 DWG、DXF、DGN 等格式**。  
- **細緻的光柵化控制**，如版面選擇、縮放與背景顏色。  
- **高效能**，適合在伺服器上批次處理。

## 前置條件

在開始之前，請確保您已具備以下項目：

1. **Java Development Kit** – 前往 [此處](https://www.java.com/en/download/) 下載。  
2. **Aspose.CAD for Java 函式庫** – 從 [此處](https://releases.aspose.com/cad/java/) 取得最新 JAR。  
3. **範例 CAD 檔案** – 放置於專案的 document 目錄下的 DWG 檔（例如 `sample.dwg`）。

## 匯入命名空間

在 Java 應用程式中，加入必要的命名空間以使用 Aspose.CAD 功能。範例如下：

```java

import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

現在，讓我們將 **how to export cad** 的流程拆解為可管理的步驟。

## 步驟說明

### 步驟 1：載入 CAD 圖紙

```java
String dataDir = "Your Document Directory" + "CADConversion/";
String sourceFilePath = dataDir + "sample.dwg";
Image objImage = Image.load(sourceFilePath);
```

我們將來源 DWG 檔載入為 `Image` 物件，作為後續所有操作的入口。

### 步驟 2：建立 `BmpOptions`

```java
BmpOptions bmpOptions = new BmpOptions();
```

`BmpOptions` 用來保存 BMP 輸出的光柵化設定。

### 步驟 3：設定光柵化選項

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(cadRasterizationOptions);
```

在此將光柵化選項連結至 BMP 選項，讓您能控制 CAD 實體的渲染方式。

### 步驟 4：指定要匯出的版面

```java
cadRasterizationOptions.setLayouts(new String[]{"Model"});
```

`Layouts` 屬性告訴 Aspose.CAD 要匯出哪些圖紙版面。大多數情況下，`"Model"` 為主要版面。

### 步驟 5：匯出為 BMP 格式

```java
String outPath = sourceFilePath + ".bmp";
objImage.save(outPath, bmpOptions);
```

呼叫 `save` 並傳入已設定好的 `BmpOptions`，即可將 BMP 檔寫入磁碟。至此 **convert DWG to BMP** 工作流程完成。

## 常見問題與解決方案

| 問題 | 原因 | 解決方式 |
|------|------|----------|
| 輸出影像為空白 | 版面名稱錯誤或缺少版面 | 確認版面名稱與 CAD 檔相符（例如 `"Model"`）。 |
| 解析度過低 | 預設 DPI 較低 | 在儲存前設定 `cadRasterizationOptions.setResolution(300);`。 |
| 大檔案記憶體不足 | 大型圖紙需要更多堆疊空間 | 增加 JVM 堆疊大小（`-Xmx2g`）或分頁處理。 |

## 常見問答

**Q: Aspose.CAD 是否支援多種 CAD 檔案格式？**  
A: 是，支援 DWG、DXF、DGN 以及其他多種格式。

**Q: 我可以在商業專案中使用 Aspose.CAD 嗎？**  
A: 當然可以。請於 [此處](https://purchase.aspose.com/buy) 購買正式授權以供正式使用。

**Q: 如何取得測試用的臨時授權？**  
A: 可於 [此處](https://purchase.aspose.com/temporary-license/) 取得臨時授權。

**Q: 有哪裡可以取得社群支援？**  
A: 加入 Aspose.CAD 社群論壇 [forum](https://forum.aspose.com/c/cad/19)。

**Q: 有提供 Aspose.CAD for Java 的免費試用嗎？**  
A: 有，請至 [此處](https://releases.aspose.com/) 下載免費試用版。

## 結論

本指南示範了如何在 Java 中 **how to export cad** 並使用 Aspose.CAD **convert DWG to BMP**。依循上述五個步驟，即可將 CAD 轉換為影像，無論是桌面工具、Web 服務或批次處理流程皆適用。若需其他輸出格式（PNG、JPEG、PDF），只要更換對應的 Options 類別，即可利用 Aspose.CAD 豐富的功能滿足所有 CAD 操作需求。

---

**最後更新：** 2025-12-22  
**測試環境：** Aspose.CAD for Java 24.12  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}