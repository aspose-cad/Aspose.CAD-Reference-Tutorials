---
date: 2026-02-23
description: 學習如何在 Java 中使用 Aspose.CAD 將 DWG 轉換為 BMP，內容包括如何匯出 CAD 檔案、批次轉換 CAD、渲染 CAD
  版面以及高效匯出多個 CAD 版面。
linktitle: Auto Adjusting CAD Drawing Size
second_title: Aspose.CAD Java API
title: 如何使用 Aspose.CAD for Java 將 DWG 轉換為 BMP
url: /zh-hant/java/cad-file-manipulation/auto-adjusting-cad-drawing-size/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何使用 Aspose.CAD for Java 將 DWG 轉換為 BMP

## 簡介

## 快速答案
- **「convert dwg to bmp」是什麼意思？** 它指的是將 DWG（或其他 CAD）檔案渲染為 BMP 點陣圖像。  
- **哪個函式庫負責轉換？** Aspose.CAD for Java 提供簡單、純 Java 的 API 來完成此任務。  
- **我需要授權嗎？** 測試時可使用臨時授權；正式環境需購買正式授權。  
- **我可以一次匯出多個版面嗎？** 可以 — 透過設定 `Layouts` 屬性即可指定要渲染的版面。  
- **BMP 是唯一的輸出格式嗎？** 不是 — 您也可以匯出為 PNG、JPEG、TIFF、PDF 等格式。

## 如何使用 Aspose.CAD for Java 將 DWG 轉換為 BMP
在本節中，我們直接回答核心問題，並為接下來的逐步指南鋪路。

### 使用 Aspose.CAD 的「convert dwg to bmp」是什麼？
將 DWG 轉換為 BMP 意味著將原生 CAD 圖紙（例如 DWG 檔）光柵化為點陣圖像。Aspose.CAD 負責所有繁重工作：解析 CAD 結構、渲染向量實體，並將結果寫入與原始版面尺寸與顏色相符的 BMP 檔案。

### 為什麼使用 Aspose.CAD for Java 來 **convert DWG to BMP**？
- **純 Java 實作** – 無需原生 DLL 或外部工具。  
- **廣泛的格式支援** – 原生讀取 DWG、DXF、DGN 以及許多其他 CAD 格式。  
- **細緻的控制** – 您可以選擇特定版面、設定 DPI、背景顏色等。  
- **可擴展的效能** – 適合在伺服器或桌面工具上批次轉換 CAD 檔案。  

## 前置條件

1. **Java Development Kit** – 前往[此處](https://www.java.com/en/download/)下載。  
2. **Aspose.CAD for Java library** – 從[此處](https://releases.aspose.com/cad/java/)取得最新 JAR。  
3. **範例 CAD 檔案** – 一個 DWG 檔（例如 `sample.dwg`），放置於專案的文件目錄中。

## 匯入命名空間

在 Java 應用程式中，加入必要的命名空間以使用 Aspose.CAD 功能。以下為範例：

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

現在，讓我們將 **convert dwg to bmp** 的流程拆解為可管理的步驟。

## 步驟指南

### 步驟 1：載入 CAD 圖紙

```java
String dataDir = "Your Document Directory" + "CADConversion/";
String sourceFilePath = dataDir + "sample.dwg";
Image objImage = Image.load(sourceFilePath);
```

我們將來源 DWG 檔載入 `Image` 物件，作為所有後續操作的入口點。

### 步驟 2：建立 `BmpOptions`

```java
BmpOptions bmpOptions = new BmpOptions();
```

### 步驟 3：設定光柵化選項

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(cadRasterizationOptions);
```

### 步驟 4：設定要匯出的版面

```java
cadRasterizationOptions.setLayouts(new String[]{"Model"});
```

`Layouts` 屬性告訴 Aspose.CAD 要包含哪些圖紙版面。大多數情況下，`"Model"` 是您想要轉換的主要版面，但您也可以透過傳遞版面名稱陣列來 **匯出多個 CAD 版面**。

### 步驟 5：匯出為 BMP 格式

```java
String outPath = sourceFilePath + ".bmp";
objImage.save(outPath, bmpOptions);
```

呼叫 `save` 並傳入已設定好的 `BmpOptions` 即可將 BMP 檔寫入磁碟。這樣就完成了 **convert dwg to bmp** 工作流程。

## 常見問題與解決方案

| 問題 | 原因 | 解決方法 |
|-------|--------|-----|
| 輸出圖像為空白 | 版面名稱不正確或缺少版面 | 確認版面名稱與 CAD 檔相符（例如 `"Model"`）。 |
| 解析度低 | 預設 DPI 較低 | 在儲存前設定 `cadRasterizationOptions.setResolution(300);`。 |
| 大型檔案記憶體不足錯誤 | 大型圖紙需要更多堆疊記憶體 | 增加 JVM 堆疊大小（`-Xmx2g`）或逐頁處理。 |

## 常見問答

**Q: Aspose.CAD 是否相容於不同的 CAD 檔案格式？**  
A: 是的，Aspose.CAD 支援 DWG、DXF、DGN 以及許多其他格式。

**Q: 我可以在商業專案中使用 Aspose.CAD 嗎？**  
A: 當然可以。請於[此處](https://purchase.aspose.com/buy)購買授權以供正式使用。

**Q: 如何取得測試用的臨時授權？**  
A: 您可於[此處](https://purchase.aspose.com/temporary-license/)取得臨時授權。

**Q: 我可以在哪裡取得社群支援？**  
A: 加入 Aspose.CAD 社群論壇，網址為[forum](https://forum.aspose.com/c/cad/19)。

**Q: 是否提供 Aspose.CAD for Java 的免費試用？**  
A: 有，請於[此處](https://releases.aspose.com/)下載免費試用版。

## 批次轉換 CAD 檔案的額外提示

- **遍歷目錄**，對每個 DWG 檔套用相同步驟；這可實現 **batch convert CAD** 情境。  
- **重複使用 `CadRasterizationOptions`**（若可能），以減少物件建立的開銷。  
- **記錄每次轉換**，包括來源檔名與輸出路徑，以簡化除錯。

## 結論

在本指南中，我們示範了如何使用 Aspose.CAD for Java **convert dwg to bmp**，並說明了 **export CAD**、**render CAD layout**，甚至在一次執行中 **export multiple CAD layouts** 的關鍵步驟。遵循上述五個步驟，即可將 CAD 轉圖功能整合至任何 Java 應用程式——無論是桌面工具、Web 服務或批次處理管線。透過切換選項類別即可探索其他輸出格式（PNG、JPEG、PDF），並善用 Aspose.CAD 豐富的功能滿足所有 CAD 操作需求。

---

**最後更新：** 2026-02-23  
**測試環境：** Aspose.CAD for Java 24.12  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}