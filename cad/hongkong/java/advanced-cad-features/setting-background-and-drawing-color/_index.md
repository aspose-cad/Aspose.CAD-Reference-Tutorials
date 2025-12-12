---
date: 2025-12-12
description: 學習如何在使用 Aspose.CAD for Java 轉換 CAD 為 PDF 與 TIFF 時設定背景顏色。自訂繪圖顏色，獲得專業效果。
linktitle: Setting Background and Drawing Color
second_title: Aspose.CAD Java API
title: 使用 Aspose.CAD for Java 設定背景顏色
url: /zh-hant/java/advanced-cad-features/setting-background-and-drawing-color/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.CAD for Java 設定背景顏色

## 介紹

在現代 CAD 工作流程中，能夠在轉換過程中 **設定背景顏色** 是產出清晰、可直接展示文件的關鍵。Aspose.CAD for Java 讓將 CAD 檔案轉換為 PDF 或 TIFF 變得簡單，同時讓您完整掌控背景色與繪圖色彩。本教學將逐步說明整個流程——從載入 DXF 檔案到匯出 PDF 與 TIFF 檔案，並使用您自訂的顏色。

## 快速解答
- **哪個函式庫在 Java 中處理 CAD 轉換？** Aspose.CAD for Java.
- **我可以在轉換過程中更改背景顏色嗎？** 可以，使用 `CadRasterizationOptions.setBackgroundColor`.
- **支援哪些輸出格式？** PDF 與 TIFF（皆為光柵化）。
- **生產環境需要授權嗎？** 需要商業授權；亦提供免費試用版。
- **是否支援批次轉換？** 當然可以——在迴圈中使用相同設定處理多個檔案。

## 在 CAD 轉換中「設定背景顏色」是什麼意思？

在 Java 中設定背景顏色是指配置光柵化選項，使渲染出的影像（PDF 或 TIFF）使用您指定的顏色，而非預設的白色畫布。這可提升視覺對比度，尤其當 CAD 圖面包含淡色線條時。

## 為何使用 Aspose.CAD for Java 轉換 CAD 為 PDF 或 TIFF？

- **高保真** – 保留線寬、圖層與顏色。
- **無外部相依性** – 純 Java，無需本機函式庫。
- **彈性渲染** – 可控制頁面尺寸、DPI、背景與繪圖顏色。
- **批次處理** – 適合自動化工作流程。

## 前置條件

在開始之前，請確保您已具備以下項目：

- **Aspose.CAD for Java Library** – 前往 [此處](https://releases.aspose.com/cad/java/) 下載。
- **存放 CAD 檔案的資料夾** – 將 `"Your Document Directory" + "CADConversion/"` 替換為您機器上的實際路徑。

## 匯入命名空間

首先，匯入您需要的類別。這些匯入讓您能使用顏色處理、光柵化選項以及輸出格式。

```java
import java.awt.Color;
import java.awt.Image;

import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## 步驟說明

### 步驟 1：載入 CAD 檔案

我們將來源 DXF（或任何支援的 CAD 格式）載入至 `Image` 物件中。

```java
String dataDir = "Your Document Directory" + "CADConversion/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image objImage = Image.load(srcFile);
```

### 步驟 2：設定背景與繪圖顏色

在此我們設定頁面尺寸、選擇背景顏色，並指示渲染器使用特定的繪圖顏色取代原始 CAD 顏色。

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
rasterizationOptions.setBackgroundColor(com.aspose.cad.Color.getBeige());   // example background
rasterizationOptions.setDrawType(CadDrawTypeMode.UseDrawColor);
rasterizationOptions.setBackgroundColor(com.aspose.cad.Color.getBlue());   // overwrite with blue if needed
```

> **專業提示：** 若想保留 CAD 原生顏色同時套用自訂背景，可嘗試 `CadDrawTypeMode.UseOriginalColors`。

### 步驟 3：建立 PDF 並儲存

我們將光柵化選項綁定至 `PdfOptions`，並將結果儲存為 PDF 檔案。

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

### 步驟 4：建立 TIFF 並儲存

相同的光柵化設定可重複用於 TIFF 輸出。

```java
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

## 常見問題與解決方案

| 問題 | 解決方案 |
|-------|----------|
| **背景顏色未變更** | 確保在設定繪圖類型之後再呼叫 `setBackgroundColor`。第二次呼叫會覆寫第一次，因此請將欲使用的顏色作為最後一次呼叫。 |
| **輸出模糊** | 增加 `PageWidth`/`PageHeight` 或透過 `rasterizationOptions.setResolution(...)` 設定更高的 DPI。 |
| **找不到檔案例外** | 確認 `dataDir` 路徑以分隔符號 (`/` 或 `\\`) 結尾，且檔案確實存在。 |

## 常見問答

**Q: Aspose.CAD for Java 是否適合批次轉換？**  
A: 當然可以。您可以將程式碼放入迴圈中，以相同的光柵化設定處理數十個檔案。

**Q: 我可以自訂產生檔案的背景顏色嗎？**  
A: 可以。教學示範了如何為 PDF 與 TIFF 輸出設定任意 `com.aspose.cad.Color`。

**Q: 在哪裡可以找到 Aspose.CAD for Java 的完整文件？**  
A: 請參考 [文件說明](https://reference.aspose.com/cad/java/) 以取得深入細節與其他範例。

**Q: 是否提供免費試用？**  
A: 有，您可透過 [免費試用](https://releases.aspose.com/) 體驗功能。

**Q: 如何取得 Aspose.CAD for Java 的支援？**  
A: 請前往 [Aspose.CAD 論壇](https://forum.aspose.com/c/cad/19) 提問並與社群分享使用經驗。

---

**最後更新：** 2025-12-12  
**測試環境：** Aspose.CAD for Java 24.11  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}