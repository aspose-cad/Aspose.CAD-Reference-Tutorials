---
date: 2025-12-21
description: 學習如何使用 Aspose.CAD for Java 將 CAD 版面匯出為 PDF —— 一種快速、可靠的從 CAD 檔案生成 PDF
  的方法。
linktitle: Export CAD Layouts to PDF
second_title: Aspose.CAD Java API
title: 如何使用 Aspose.CAD for Java 將 CAD 版面匯出為 PDF
url: /zh-hant/java/cad-export-options/export-cad-layouts-to-pdf/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何使用 Aspose.CAD for Java 將 CAD 版面匯出為 PDF

## Introduction

在本教學中，我們將示範 **如何使用 Aspose.CAD for Java 將 CAD** 版面匯出為 PDF。無論您是處理 DWG、DXF 或其他 CAD 格式，本指南將帶領您以乾淨、程式化的方式快速且可靠地從 CAD 檔案產生 PDF。

## Quick Answers
- **此函式庫的功能是什麼？** 它將 CAD 圖紙（DWG、DXF、DWF 等）轉換為 PDF、點陣圖像及其他格式。  
- **使用哪種語言？** Java – 程式碼可在任何相容 JVM‑compatible 平台上執行。  
- **需要授權嗎？** 提供免費試用版；正式環境需購買商業授權。  
- **可以在 Java 中將 DWG 轉換為 PDF 嗎？** 可以 – 同一 API 支援 **dwg to pdf java** 轉換。  
- **主要步驟是什麼？** 載入 CAD 檔案、設定光柵化選項、配置 PDF 選項，最後儲存結果。

## Prerequisites

在開始教學之前，請確保您已具備以下前置條件：

- Aspose.CAD for Java：確保已安裝此函式庫。您可從 Aspose 官方網站[此處](https://releases.aspose.com/cad/java/)下載。  
- Java 開發環境：確保您的機器已設置 Java 開發環境。

完成上述設定後，讓我們開始本教學。

## What is “how to export cad”?

什麼是「如何匯出 CAD」？

匯出 CAD 指的是將原生 CAD 圖紙資料（如 DWG、DXF 或 DWF）轉換為更普遍可讀的格式，例如 PDF。此流程對於與可能未安裝 CAD 軟體的利害關係人分享設計圖尤為重要。

## Why Use Aspose.CAD for Java to Export CAD to PDF?

- **高保真度** – 向量圖形得以保留，且光柵化選項可微調品質。  
- **無外部相依性** – 純 Java，無需本機 DLL 或 COM 元件。  
- **支援多種格式** – 您亦可 **generate pdf from cad** 由 DWG、DWF 或其他格式產生的檔案。  
- **適用於批次作業** – 非常適合伺服器端自動化、CI 流程或桌面工具。

## Import Namespaces

在您的 Java 程式碼中，首先匯入必要的命名空間。這些匯入提供了使用 Aspose.CAD for Java 所需的類別與方法。

```java
import com.aspose.cad.Image;
import com.aspose.cad.InterpolationMode;
import com.aspose.cad.SmoothingMode;
import com.aspose.cad.TextRenderingHint;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

## Step 1: Load the CAD File

### 步驟 1：載入 CAD 檔案

首先使用 `Image.load` 方法將 CAD 檔案載入您的 Java 應用程式。將 `"conic_pyramid.dxf"` 替換為您的 CAD 檔案路徑。

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

## Step 2: Set Rasterization Options

### 步驟 2：設定光柵化選項

建立 `CadRasterizationOptions` 的實例，以定義 CAD 實體的光柵化方式。根據需求調整頁寬、頁高與版面縮放等參數。

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(false);
rasterizationOptions.setContentAsBitmap(true);
rasterizationOptions.setLayouts(new String[]{"Model"});
```

## Step 3: Set PDF Options

### 步驟 3：設定 PDF 選項

建立 `PdfOptions` 的實例，並將其與光柵化選項關聯。此外，為 PDF 匯出設定圖形選項，例如平滑模式、文字渲染提示與插值模式。

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
rasterizationOptions.getGraphicsOptions().setSmoothingMode(SmoothingMode.HighQuality);
rasterizationOptions.getGraphicsOptions().setTextRenderingHint(TextRenderingHint.AntiAliasGridFit);
rasterizationOptions.getGraphicsOptions().setInterpolationMode(InterpolationMode.HighQualityBicubic);
```

## Step 4: Export to PDF

### 步驟 4：匯出為 PDF

最後，使用 `cadImage` 物件的 `save` 方法將 CAD 版面匯出為 PDF 檔案。

```java
cadImage.save(dataDir + "CADLayoutsToPDF_out_.pdf", pdfOptions);
```

## Common Issues and Solutions

### 常見問題與解決方案

| Issue | Reason | Fix |
|-------|--------|-----|
| **PDF 輸出空白** | 光柵化選項設定不正確（例如版面名稱不匹配） | 確認 `rasterizationOptions.setLayouts()` 與 CAD 檔案中的版面名稱相符。 |
| **低解析度影像** | `PageWidth`/`PageHeight` 設定過小 | 增大頁面尺寸或透過 `rasterizationOptions.setResolution()` 設定更高的 DPI。 |
| **不支援的 CAD 版本** | 較舊的 DWG/DXF 版本可能需要更新的 Aspose.CAD 版本 | 從 Aspose 官方網站下載最新的函式庫版本。 |

## Frequently Asked Questions

### 常見問答

### Q1：我可以在 Aspose.CAD for Java 中使用其他 CAD 檔案格式嗎？

**A1：** 是的，Aspose.CAD 支援多種 CAD 格式，包括 DWG、DXF、DWF 等。完整列表請參閱文件[此處](https://reference.aspose.com/cad/java/)。

### Q2：是否提供 Aspose.CAD for Java 的免費試用？

**A2：** 是的，您可透過[此處](https://releases.aspose.com/)的免費試用來體驗 Aspose.CAD 功能。

### Q3：如何取得 Aspose.CAD for Java 的支援？

**A3：** 請前往 Aspose.CAD 論壇[此處](https://forum.aspose.com/c/cad/19)尋求社群支援。若需高階支援，請考慮在[此處](https://purchase.aspose.com/buy)購買授權。

### Q4：自動與手動版面縮放有何差異？

**A4：** 自動版面縮放會根據指定的頁面尺寸調整版面大小；手動縮放則允許您自行設定縮放值。

### Q5：我可以自訂匯出 PDF 檔案的外觀嗎？

**A5：** 可以，您可在程式碼中自訂圖形選項，以控制匯出 PDF 的品質與外觀。

### Q6：Aspose.CAD 是否直接支援 **dwg to pdf java** 轉換？

**A6：** 當然支援。相同的光柵化與 PDF 選項適用於 DWG 檔案，實現無縫的 **dwg to pdf java** 轉換。

### Q7：有沒有方法在不光柵化為點陣圖的情況下 **generate pdf from cad**？

**A7：** 透過設定 `rasterizationOptions.setContentAsBitmap(false)`，可在可能的情況下保留向量資料，產生真正的向量式 PDF。

---

**最後更新：** 2025-12-21  
**測試環境：** Aspose.CAD for Java 24.10  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}