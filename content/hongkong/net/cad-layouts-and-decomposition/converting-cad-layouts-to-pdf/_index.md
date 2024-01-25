---
title: 將 CAD 版面配置轉換為 PDF - Aspose.CAD 教學課程
linktitle: 將 CAD 版面配置轉換為 PDF
second_title: Aspose.CAD .NET - CAD 和 BIM 檔案格式
description: 使用 Aspose.CAD for .NET 輕鬆將 CAD 版面配置轉換為 PDF。請按照我們的逐步指南進行無縫整合。
type: docs
weight: 10
url: /zh-hant/net/cad-layouts-and-decomposition/converting-cad-layouts-to-pdf/
---
## 介紹

您是否希望將 CAD 版面配置無縫轉換為 PDF？ Aspose.CAD for .NET 提供了一個強大的解決方案，使流程高效且簡單。在本教程中，我們將引導您完成使用 Aspose.CAD 的步驟，這是一個功能強大的 API，可讓開發人員輕鬆使用 CAD 檔案。

## 先決條件

在深入學習本教程之前，請確保您具備以下先決條件：

-  Aspose.CAD for .NET：下載並安裝該程式庫。你可以找到它[這裡](https://releases.aspose.com/cad/net/).

- .NET 環境：確保您有一個有效的 .NET 開發環境。

- 範例 CAD 檔案：準備好範例 CAD 檔案以供轉換。在本教程中，我們將使用“conic_pyramid.dxf”。

## 導入命名空間

首先將必要的命名空間匯入到您的 .NET 專案中。此步驟可確保您可以存取 Aspose.CAD 功能。

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
using Aspose.CAD.FileFormats.Cad;
```

## 第 1 步：設定您的項目

首先設定您的 .NET 專案。建立一個新專案或開啟要在其中實作 CAD 到 PDF 轉換的現有專案。

## 步驟 2：定義來源 CAD 檔案路徑

指定 CAD 檔案的路徑。在我們的範例中，原始檔案是“conic_pyramid.dxf”。

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";
```

## 第 3 步：載入 CAD 文件

建立 CadImage 類別的實例並將 CAD 檔案載入到應用程式中。

```csharp
using (Aspose.CAD.Image cadImage = (Aspose.CAD.Image)Image.Load(sourceFilePath))
```

## 步驟 4：配置光柵化選項

配置光柵化選項以自訂 PDF 輸出。設定頁面尺寸、佈局縮放和其他相關參數。

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
//其他配置選項...
```

## 第 5 步：設定佈局

指定要包含在 PDF 中的佈局。在此範例中，我們使用“模型”佈局。

```csharp
rasterizationOptions.Layouts = new string[] { "Model" };
```

## 第 6 步：定義 PDF 選項

建立 PdfOptions 類別的實例並將其與光柵化選項關聯。

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## 第 7 步：設定圖形選項

配置 PDF 的圖形選項，包括平滑模式、文字渲染和插值。

```csharp
rasterizationOptions.GraphicsOptions.SmoothingMode = SmoothingMode.HighQuality;
rasterizationOptions.GraphicsOptions.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
rasterizationOptions.GraphicsOptions.InterpolationMode = InterpolationMode.HighQualityBicubic;
```

## 第 8 步：儲存為 PDF

指定 PDF 檔案的輸出路徑，並將 CAD 佈局儲存為 PDF。

```csharp
MyDir = MyDir + "CADLayoutsToPDF_out.pdf";
cadImage.Save(MyDir, pdfOptions);
```

## 結論

恭喜！您已使用 Aspose.CAD for .NET 成功將 CAD 版面配置轉換為 PDF。本教程為希望在應用程式中簡化此流程的開發人員提供了全面的指南。

## 常見問題解答

### Q1：我可以一次轉換多個 CAD 佈局嗎？

 A1：是的，您可以在`Layouts`數組以將它們包含在 PDF 中。

### Q2: 支援的 CAD 檔案格式有限制嗎？

A2：Aspose.CAD for .NET 支援各種 CAD 格式，包括 DWG 和 DXF。

### 問題 3：如何自訂 PDF 輸出的外觀？

A3：使用提供的光柵化和圖形選項根據您的喜好自訂 PDF 輸出。

### 問題 4：Aspose.CAD for .NET 有試用版嗎？

 A4：是的，您可以透過[免費試用版](https://releases.aspose.com/).

### Q5：我可以在哪裡尋求支持或提問？

A5：訪問[Aspose.CAD論壇](https://forum.aspose.com/c/cad/19)尋求幫助和討論。