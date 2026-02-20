---
date: 2026-02-20
description: 學習如何使用 Aspose.CAD for Java 將 STL 轉換為 PNG。此逐步指南展示如何高效匯出 STL 檔案。
linktitle: Export STL to PNG
second_title: Aspose.CAD Java API
title: 如何使用 Aspose.CAD for Java 將 STL 轉換為 PNG
url: /zh-hant/java/cad-export-options/export-stl-to-png/
weight: 20
---

 exactly.

Let's craft final answer.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 將 STL 轉換為 PNG（使用 Aspose.CAD for Java）

## 介紹

如果您需要在 Java 應用程式中 **將 STL 轉換為 PNG**，Aspose.CAD for Java 能快速且可靠地完成此工作。在本教學中，我們將逐步說明整個流程——從設定專案到儲存最終的 PNG 圖片——讓您能自信地將 STL 轉換整合到工作流程中。

## 快速回答
- **此函式庫的功能是什麼？** 它將 CAD 格式（包括 STL）轉換為 PNG 等點陣圖像。  
- **使用哪種語言？** Java，搭配 Aspose.CAD API。  
- **需要授權嗎？** 生產環境需要臨時或正式授權。  
- **實作需要多長時間？** 基本轉換大約需要 10‑15 分鐘。  
- **可以自訂影像尺寸嗎？** 可以，透過 `CadRasterizationOptions`。

## 什麼是將 STL 轉換為 PNG？

將 STL 轉換為 PNG 是將 3‑D 網格檔案（STL）轉換為 2‑D 點陣圖（PNG）。當您需要快速的視覺預覽、產生縮圖，或在網頁中嵌入模型而不需 3‑D 檢視器時，這非常有用。

## 為什麼使用 Aspose.CAD for Java？

- **完整功能的 API** – 支援多種 CAD 格式，不僅限於 STL。  
- **無外部相依性** – 純 Java，易於加入任何 Maven/Gradle 專案。  
- **高品質點陣輸出** – 可控制解析度、背景與抗鋸齒。  
- **支援「如何匯出 STL」情境** – 非常適合批次處理或即時轉換。

## 前置條件

在開始之前，請確保您已具備以下條件：

- 已在機器上安裝 Java Development Kit（JDK）。  
- 已下載 Aspose.CAD for Java 程式庫。您可於 [此處](https://releases.aspose.com/cad/java/) 取得。  
- 擁有有效授權或可從 [此處](https://purchase.aspose.com/temporary-license/) 取得臨時授權。

## 匯入命名空間

在您的 Java 專案中，匯入必要的類別：

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

現在，讓我們將範例分解為多個步驟。

## 步驟 1：設定您的專案

建立一個新的 Java 專案，並將 Aspose.CAD for Java 程式庫加入專案的相依性（Maven、Gradle，或手動加入 JAR）。

## 步驟 2：指定您的 STL 檔案

定義您要轉換的 STL 檔案路徑：

```java
String dataDir = "Your Document Directory" + "ExportingSTL/";
String fileName = dataDir + "example.stl";
```

## 步驟 3：載入 STL 檔案

使用 `Image.load` 方法載入 STL 檔案。此方法會建立一個 **CAD image** 物件，供您進行點陣化：

```java
CadImage cadImage = (CadImage)Image.load(fileName);
```

## 步驟 4：設定點陣化選項

設定點陣化選項，以控制輸出 PNG 的尺寸與品質。這些選項屬於 **cad image to png** 轉換流程的一部份：

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
```

## 步驟 5：設定 PNG 選項

建立 `PngOptions` 實例。若要套用點陣化設定，請取消註解以下程式行：

```java
PngOptions pngOptions = new PngOptions();
// Uncomment the line below if you want to set vector rasterization options
// pngOptions.setVectorRasterizationOptions(vectorOptions);
```

## 步驟 6：儲存為 PNG

最後，將 CAD 圖像匯出為 PNG 檔案——這就是 **save PNG Java** 步驟：

```java
String outPath = dataDir + "galeon.stl.png";
cadImage.save(outPath, pngOptions);
```

> **專業提示：** 調整 `PageWidth` 與 `PageHeight` 以符合目標縮圖尺寸，可加快處理速度。

恭喜！您已成功使用 Aspose.CAD for Java **將 STL 檔案轉換為 PNG**。

## 常見問題與解決方案

| 問題 | 原因 | 解決方案 |
|------|------|----------|
| 空白 PNG 輸出 | 未設定點陣化選項 | 取消註解 `pngOptions.setVectorRasterizationOptions(vectorOptions);` 或指定背景顏色 |
| 大型 STL 檔案發生 OutOfMemoryError | 堆積記憶體不足 | 增加 JVM 堆積大小（`-Xmx2g`）或分段處理檔案 |
| LicenseException | 沒有有效授權 | 在載入圖像前套用臨時或正式授權 |

## 常見問答

### Q1: Aspose.CAD for Java 是否相容所有 STL 檔案版本？

A1: Aspose.CAD for Java 支援多種 STL 檔案版本，確保與大多數常見格式相容。

### Q2: 我可以在商業專案中使用 Aspose.CAD for Java 嗎？

A2: 可以。只需從 [此處](https://purchase.aspose.com/buy) 取得有效授權。

### Q3: 免費試用需要臨時授權嗎？

A3: 不需要，免費試用不需臨時授權。您可立即從 [此處](https://releases.aspose.com/) 取得試用版。

### Q4: 我可以在哪裡取得額外支援或提問？

A4: 請前往 Aspose.CAD 論壇 [此處](https://forum.aspose.com/c/cad/19) 獲得支援或詢問。

### Q5: 有完整的文件可供參考嗎？

A5: 有，文件可於 [此處](https://reference.aspose.com/cad/java/) 找到。

## 結論

本指南示範了如何使用 Aspose.CAD for Java 高效地 **將 STL 轉換為 PNG**。依照上述步驟，您即可將 STL 轉 PNG 轉換整合至任何基於 Java 的工作流程，無論是桌面工具、網路服務，或自動化報表工具。

---

**最後更新:** 2026-02-20  
**測試環境:** Aspose.CAD for Java 24.12 (latest at time of writing)  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}