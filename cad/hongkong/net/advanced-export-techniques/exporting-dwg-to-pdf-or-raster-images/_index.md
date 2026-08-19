---
date: 2026-03-16
description: 學習如何使用 Aspose.CAD for .NET 將 DWG 轉換為 PDF 或點陣圖像。此一步一步的 CAD 轉 PDF 教程涵蓋將
  DWG 匯出為 PNG 等圖像格式，並示範如何高效地將 DWG 匯出為圖像檔案。
linktitle: Exporting DWG to PDF or Raster Images
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: 如何使用 Aspose.CAD for .NET 將 DWG 轉換為 PDF 與光柵圖像
url: /zh-hant/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 將 DWG 匯出為 PDF 或點陣圖像 - Aspose.CAD 指南

## Introduction

如果您需要直接在 .NET 應用程式中 **將 DWG 轉換為 PDF**（或轉換為 PNG 等點陣格式），您來對地方了。在本教學中，我們將逐步說明使用 Aspose.CAD for .NET 執行轉換的具體步驟，解釋為何此函式庫是可靠的選擇，並示範僅用幾行程式碼即可同時處理 PDF 與影像輸出。

## Quick Answers
- **什麼函式庫負責 DWG 轉換？** Aspose.CAD for .NET  
- **我可以同時將 DWG 匯出為 PNG 以及 PDF 嗎？** 可以 – 相同的光柵化選項適用於兩種格式。  
- **開發時需要授權嗎？** 免費試用版可用於測試；正式環境需購買商業授權。  
- **支援哪些 .NET 版本？** .NET Framework 4.5+、.NET Core 3.1+、.NET 5/6+。  
- **單位換算會自動處理嗎？** 您可以如程式碼所示手動定義單位系統（公制或英制）。

## What is “convert DWG to PDF”?

將 DWG 轉換為 PDF 意指將 CAD 圖紙（DWG）渲染成可攜帶、僅供檢視的文件（PDF）。此作法適用於與沒有 CAD 軟體的利害關係人共享設計、製作可列印文件，或以通用可讀格式保存圖紙。

## Why use Aspose.CAD for this conversion?
- **無外部相依性** – 此函式庫完全以受管理程式碼執行。  
- **高保真度** – 保留圖層、線寬及版面資訊。  
- **內建光柵化選項** – 可使用單一設定物件匯出為 PNG、JPEG、BMP 等格式。  
- **跨平台** – 在 Windows、Linux 及 macOS 上以 .NET Core 執行皆可。

## Prerequisites

在開始教學之前，請確保已具備以下條件：

- 基本的 .NET 程式設計知識。  
- 已安裝 Aspose.CAD for .NET 函式庫。如未安裝，請於 [此處](https://releases.aspose.com/cad/net/) 下載。  
- 已設定好您慣用的 .NET 開發整合環境 (IDE)。

## Import Namespaces

首先在 .NET 專案中匯入必要的命名空間，以確保程式碼能使用 Aspose.CAD 功能。

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
```

## Step 1: Load DWG File

首先載入欲轉換的 DWG 檔案。將 `"Your Document Directory"` 替換為 DWG 檔案的實際路徑。

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Your code for loading DWG goes here
}
```

## Step 2: Set up PDF Export (How to export DWG to PDF)

接著設定 PDF 匯出參數。此範例示範如何指定版面配置並處理單位換算。

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new string[] { "Model" };

// Check and define the unit system
bool currentUnitIsMetric = false;
double currentUnitCoefficient = 1.0;
DefineUnitSystem(cadImage.UnitType, out currentUnitIsMetric, out currentUnitCoefficient);

// Your code for setting up PDF export goes here
```

## Step 3: Export to PDF

使用先前設定的參數執行 PDF 匯出。

```csharp
PdfOptions pdfOptions = new PdfOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath, pdfOptions);
```

## Step 4: Export to Raster Images (export dwg to image)

擴充功能以匯出點陣圖像，例如 PNG。

```csharp
// A4 size at 300 DPI - 2480 x 3508
rasterizationOptions.PageHeight = 3508;
rasterizationOptions.PageWidth = 2480;

PngOptions pngOptions = new PngOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath.Replace("pdf", "png"), pngOptions);
```

## Common Issues and Solutions

| 問題 | 發生原因 | 解決方法 |
|-------|----------------|------------|
| **PDF 出現空白頁** | 版面未正確指定 | 確保 `rasterizationOptions.Layouts` 包含正確的版面名稱（例如 `"Model"`）。 |
| **尺寸不正確** | DPI 或頁面尺寸不匹配 | 調整 `CadRasterizationOptions` 中的 `PageHeight`、`PageWidth` 以及 DPI 值。 |
| **單位顯示錯誤** | 未定義單位換算 | 使用 `DefineUnitSystem` 依據 `cadImage.UnitType` 設定 `currentUnitIsMetric` 與 `currentUnitCoefficient`。 |
| **授權例外** | 試用版限制 | 在呼叫 `Image.Load` 前套用臨時或永久授權。 |

## Frequently Asked Questions

### Q1: 我可以在商業專案中使用 Aspose.CAD for .NET 嗎？
A1: 可以。請前往 [purchase.aspose.com/buy](https://purchase.aspose.com/buy) 了解授權細節。

### Q2: 是否提供免費試用？
A2: 當然！請於 [此處](https://releases.aspose.com/) 取得免費試用。

### Q3: 如何取得 Aspose.CAD for .NET 的支援？
A3: 請前往 [Aspose.CAD 論壇](https://forum.aspose.com/c/cad/19) 獲取社群支援。

### Q4: 我可以取得測試用的臨時授權嗎？
A4: 可以，請於 [此處](https://purchase.aspose.com/temporary-license/) 取得臨時授權。

### Q5: 在哪裡可以找到詳細文件？
A5: 文件可於 [Aspose.CAD](https://reference.aspose.com/cad/net/) 取得。

### Q6: 如何以高品質 **將 CAD 儲存為 PNG**？
A6: 在 `CadRasterizationOptions` 中將 `PageHeight` 與 `PageWidth` 設為所需的像素尺寸，並選擇 300 DPI 或更高。

### Q7: 當來源檔案包含多個版面時，**如何最佳地轉換 dwg**？
A7: 將欲匯出的所有版面名稱填入 `rasterizationOptions.Layouts`，然後對每個版面迴圈呼叫 `Save` 以產生相應的輸出格式。

---

**最後更新：** 2026-03-16  
**測試環境：** Aspose.CAD 24.11 for .NET  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}