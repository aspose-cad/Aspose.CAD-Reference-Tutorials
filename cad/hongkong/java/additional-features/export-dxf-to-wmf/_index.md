---
date: 2025-11-29
description: 學習如何使用 Aspose.CAD for Java 將 DXF 轉換為 WMF、載入 DXF 圖紙，並可選擇使用 Aspose 匯出為
  PDF。一步一步的指南，附有程式碼範例。
language: zh-hant
linktitle: Export DXF to WMF Format Using Java
second_title: Aspose.CAD Java API
title: 使用 Aspose.CAD 在 Java 中將 DXF 轉換為 WMF
url: /java/additional-features/export-dxf-to-wmf/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 將 DXF 轉換為 WMF（使用 Aspose.CAD for Java）

## 介紹

在本教學中，您將學會如何使用 Aspose.CAD for Java **將 DXF 轉換為 WMF**。無論是需要在 Windows 報表中嵌入 CAD 圖紙，或是僅想取得輕量的向量格式，DXF 轉 WMF 都是常見需求。我們將逐步說明如何載入 DXF 圖紙、設定光柵化選項、將結果儲存為 WMF，並可選擇使用 Aspose 匯出為 PDF 的步驟。

## 快速解答
- **我可以使用免費試用版將 DXF 轉換為 WMF 嗎？** 可以 – Aspose 提供功能完整的 30 天試用版。  
- **需要哪個 Java 版本？** Java 8 或更新版本。  
- **執行程式碼是否需要授權？** 生產環境必須使用授權；試用版可用於開發與測試。  
- **轉換是否無損？** 向量資料會被保留；光柵化選項可讓您控制解析度。  
- **我也可以將相同圖紙匯出為 PDF 嗎？** 當然可以 – 請參考下方「匯出為 PDF」步驟。

## 什麼是「將 DXF 轉換為 WMF」？

將 DXF 轉換為 WMF 意指把 Drawing Exchange Format（DXF）檔案——一種廣泛使用的 CAD 格式——轉換成 Windows Metafile（WMF）。WMF 是向量圖像格式，可順利整合至 Microsoft Office、Windows 應用程式以及多種報表工具。

## 為什麼使用 Aspose.CAD for Java？

- **無外部相依性** – 純 Java，無需本機 DLL。  
- **高保真度** – 保留圖層、顏色與線條樣式。  
- **內建光柵化** – 可微調頁面大小、解析度與背景。  
- **一站式解決方案** – 同一套 API 亦支援匯出為 PDF、PNG、SVG 等格式。

## 前置條件

開始之前，請確保您已具備：

- **Aspose.CAD for Java** 已整合至您的專案。可從官方網站下載：[Aspose.CAD Java download](https://releases.aspose.com/cad/java/)。  
- **文件目錄** 用於存放 DXF 檔案（例如 `Your Document Directory/DXFDrawings/`）。

## 匯入命名空間

在 Java 原始檔中，匯入您需要的 Aspose.CAD 類別：

```java
import com.aspose.cad.Color;
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.WmfOptions;
```

## 步驟指南

### 步驟 1：載入 DXF 圖紙

首先，**載入您要轉換的 DXF 圖紙**。`Image.load` 方法會將檔案讀入記憶體。

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DXFDrawings/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

### 步驟 2：設定光柵化選項

設定控制輸出 WMF 大小的光柵化參數。本範例使用 100 × 100 單位的頁面。

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(100);
rasterizationOptions.setPageHeight(100);
WmfOptions wmfOptions = new WmfOptions();
```

### 步驟 3：儲存為 WMF

使用上述選項，將載入的圖紙儲存為 WMF 檔案。

```java
cadImage.save(dataDir+" example.ifc.wmf", wmfOptions);
```

### 步驟 4：釋放資源

正確釋放資源可防止記憶體洩漏，特別是在處理大量圖紙時。

```java
finally
{
  cadImage.dispose();
}
```

### 步驟 5：可選 – Aspose 匯出為 PDF

如果您同時需要相同圖紙的 PDF 版本，Aspose.CAD 只需一行程式碼即可完成。

```java
image.save(dataDir + "conic_pyramid_out_.pdf"); 
```

> **專業提示：** 您可以將相同的 `CadRasterizationOptions` 物件傳遞給 `PdfOptions` 實例，以便用於 PDF 匯出。

## 常見問題與解決方案

| 問題 | 原因 | 解決方案 |
|------|------|----------|
| **`NullPointerException` on `cadImage.save`** | 變數 `cadImage` 未定義（應為 `image`）。 | 將 `cadImage` 替換為 `image`，或一致性地重新命名變數。 |
| **Output WMF is blank** | 光柵化頁面尺寸過小或背景色設為透明。 | 增加 `PageWidth`/`PageHeight`，或透過 `rasterizationOptions.setBackgroundColor(Color.getWhite());` 設定背景顏色。 |
| **License exception** | 在生產環境未使用有效的 Aspose 授權。 | 在應用程式啟動時套用授權檔：`License license = new License(); license.setLicense("Aspose.Total.Java.lic");`。 |

## 結論

現在您已掌握使用 Aspose.CAD for Java **將 DXF 轉換為 WMF** 的完整生產流程，並可選擇 **匯出為 PDF**。此方法可產生高品質的向量輸出，輕鬆整合至 Windows 報表與文件工具。

## 常見問答

### Q1：在哪裡可以找到 Aspose.CAD 文件？

A1：您可以在此處取得文件說明 [here](https://reference.aspose.com/cad/java/)。

### Q2：如何下載 Aspose.CAD for Java？

A2：請在此處下載程式庫 [here](https://releases.aspose.com/cad/java/)。

### Q3：是否提供免費試用？

A3：是的，您可以在此取得免費試用版 [here](https://releases.aspose.com/)。

### Q4：需要臨時授權選項嗎？

A4：請在此探索臨時授權方案 [here](https://purchase.aspose.com/temporary-license/)。

### Q5：哪裡可以取得支援？

A5：請前往 Aspose.CAD 支援論壇 [here](https://forum.aspose.com/c/cad/19)。

## 常見問題

**Q：我可以在不耗盡記憶體的情況下轉換大型 DXF 檔案（數百 MB）嗎？**  
A：可以。將檔案放在 `try‑with‑resources` 區塊中載入，並及時釋放 `Image` 物件。調整 `CadRasterizationOptions.setPageWidth/Height` 為合理大小，以降低記憶體使用量。

**Q：WMF 輸出會保留圖層資訊嗎？**  
A：WMF 為平面向量格式，圖層層級會被展平，但線條樣式與顏色會被保留。

**Q：是否可以為 WMF 設定自訂 DPI？**  
A：可以，在儲存前使用 `rasterizationOptions.setResolution(300);` 來定義 DPI。

**Q：我能一次批次轉換多個 DXF 檔案嗎？**  
A：當然可以。遍歷目錄，載入每個檔案，套用相同的光柵化與儲存邏輯即可。

**Q：支援哪些 Java 版本？**  
A：Aspose.CAD for Java 支援 Java 8 及以上版本（包括 Java 11、17 以及更新的 LTS 版本）。

**最後更新：** 2025-11-29  
**測試環境：** Aspose.CAD for Java 24.11  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}