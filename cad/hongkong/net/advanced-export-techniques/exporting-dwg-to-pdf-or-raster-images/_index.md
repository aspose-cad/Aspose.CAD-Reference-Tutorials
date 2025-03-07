---
title: 將 DWG 匯出為 PDF 或光柵影像 - Aspose.CAD 指南
linktitle: 將 DWG 匯出為 PDF 或光柵影像
second_title: Aspose.CAD .NET - CAD 和 BIM 檔案格式
description: 探索使用 Aspose.CAD for .NET 將 DWG 匯出為 PDF 或光柵影像的綜合指南。了解步驟、先決條件，並親身體驗這個強大的函式庫。
weight: 11
url: /zh-hant/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 將 DWG 匯出為 PDF 或光柵影像 - Aspose.CAD 指南

## 介紹

您是否希望在 .NET 應用程式中將 DWG 檔案無縫轉換為 PDF 或光柵影像？別再猶豫了！本逐步指南將引導您完成使用強大的 Aspose.CAD for .NET 程式庫的過程。無論您是經驗豐富的開發人員還是新手，本教學都適合所有技能水平。

## 先決條件

在我們深入學習本教學之前，請確保您已準備好以下內容：

- 對 .NET 程式設計有基本的了解。
- 安裝了 Aspose.CAD for .NET 函式庫。如果沒有，請下載[這裡](https://releases.aspose.com/cad/net/).
- 您最喜歡的用於 .NET 開發的整合開發環境 (IDE)。

## 導入命名空間

讓我們先在 .NET 專案中導入必要的命名空間。這可確保您可以在程式碼中存取 Aspose.CAD 功能。

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

## 步驟 1： 載入 DWG 文件

首先載入您想要轉換的 DWG 檔案。將「您的文件目錄」替換為 DWG 檔案的路徑。

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    //您的載入 DWG 代碼位於此處
}
```

## 第 2 步：設定 PDF 匯出

現在，讓我們配置 PDF 導出設定。此範例示範如何設定佈局和處理單位轉換。

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new string[] { "Model" };

//檢查並定義單位制
bool currentUnitIsMetric = false;
double currentUnitCoefficient = 1.0;
DefineUnitSystem(cadImage.UnitType, out currentUnitIsMetric, out currentUnitCoefficient);

//設定 PDF 匯出的程式碼位於此處
```

## 第 3 步：匯出為 PDF

使用配置的設定執行匯出為 PDF。

```csharp
PdfOptions pdfOptions = new PdfOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath, pdfOptions);
```

## 第 4 步：匯出為光柵影像

擴充功能以匯出為光柵影像，例如 PNG。

```csharp
// A4 尺寸，300 DPI - 2480 x 3508
rasterizationOptions.PageHeight = 3508;
rasterizationOptions.PageWidth = 2480;

PngOptions pngOptions = new PngOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath.Replace("pdf", "png"), pngOptions);
```

## 結論

恭喜！您已成功學習如何使用 Aspose.CAD for .NET 將 DWG 檔案匯出為 PDF 和光柵影像。這個強大的程式庫簡化了流程，使其高效且對開發人員友好。

## 常見問題解答

### Q1：我可以在我的商業專案中使用 Aspose.CAD for .NET 嗎？

 A1: 是的，可以。訪問[buy.aspose.com/buy](https://purchase.aspose.com/buy)了解許可詳細資訊。

### Q2: 有免費試用嗎？

 A2：當然！取得免費試用[這裡](https://releases.aspose.com/).

### 問題 3：如何獲得 Aspose.CAD for .NET 支援？

A3：前往[Aspose.CAD論壇](https://forum.aspose.com/c/cad/19)以獲得社區支持。

### Q4：我可以獲得臨時許可證用於測試目的嗎？

 A4：是的，您可以獲得臨時許可證[這裡](https://purchase.aspose.com/temporary-license/).

### Q5：在哪裡可以找到詳細的文件？

 A5：該文件可在以下位置取得：[CAD軟體](https://reference.aspose.com/cad/net/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
