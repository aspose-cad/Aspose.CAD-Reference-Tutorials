---
date: 2026-03-29
description: 在本分步指南中，了解如何使用 Aspose.CAD for .NET 從 CAD 建立 PDF、設定畫布大小，以及將 CAD 匯出為 PDF
  或 TIFF。
linktitle: Setting Canvas Size and Mode
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: 如何從 CAD 產生 PDF：在 Aspose.CAD for .NET 中設定畫布大小與模式
url: /zh-hant/net/cad-features-and-support/setting-canvas-size-and-mode/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 設定 Aspose.CAD for .NET 中的畫布大小與模式

## 介紹

準備好在**從 CAD 建立 PDF**檔案的同時控制輸出尺寸了嗎？在本教學中，我們將逐步說明如何設定畫布大小與模式、載入 CAD 檔案，並使用 Aspose.CAD for .NET 匯出為 PDF 或 TIFF。無論您需要**將 DXF 轉換為 PDF**、產生高解析度圖紙，或只是調整光柵化區域，以下步驟都能提供穩定、可投入生產的解決方案。

## 快速解答
- **「create PDF from CAD」是什麼意思？** 將 CAD 圖紙（例如 DXF、DWG）轉換為保留向量與光柵細節的 PDF 文件。  
- **哪個選項控制輸出尺寸？** `CadRasterizationOptions.PageWidth` 與 `PageHeight`（畫布大小）。  
- **我也可以匯出為 TIFF 嗎？** 可以 – 使用 `TiffOptions` 並套用相同的光柵化設定。  
- **生產環境需要授權嗎？** 需要商業授權；亦提供免費試用版。  
- **支援的 .NET 版本？** .NET Framework 4.5 以上、.NET Core 3.1 以上、.NET 5/6/7。

## 什麼是「create PDF from CAD」？
從 CAD 建立 PDF 意指將 CAD 圖紙渲染成頁面導向的格式（PDF），可供檢視、列印或分享，而無需 CAD 軟體。Aspose.CAD 負責繁重的處理，讓您自行定義畫布大小、縮放比例與輸出格式。

## 為什麼在建立 PDF from CAD 時要設定畫布大小？
設定畫布大小可讓您精確控制最終 PDF 或 TIFF 的解析度與尺寸。此功能在以下情境中特別有用：
- 為特定紙張尺寸的列印作業做準備。  
- 為網站預覽產生縮圖或高解析度影像。  
- 確保多份文件之間的版面配置一致。

## 前置條件

- Aspose.CAD Library：從 [Aspose.CAD website](https://releases.aspose.com/cad/net/) 下載並安裝 Aspose.CAD 程式庫。  
- 開發環境：確保您的機器已設定好 .NET 開發環境。  
- 範例 CAD 檔案：本教學使用範例 DXF 檔案，可於 [Aspose.CAD documentation](https://reference.aspose.com/cad/net/) 取得。

## 匯入命名空間

首先，匯入處理 CAD 所需的命名空間：

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## 如何使用自訂畫布大小建立 PDF from CAD

### 步驟 1：載入 CAD 檔案

我們先**載入 CAD 檔案**（例如 DXF）至 `Image` 物件。這是將 CAD 檔案**載入記憶體**的階段。

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (Image image = Image.Load(sourceFilePath))
{
    // Your code for further steps will go here
}
```

### 步驟 2：建立 CadRasterizationOptions

建立 `CadRasterizationOptions` 實例並定義畫布大小。`PageWidth` 與 `PageHeight` 屬性讓您**設定畫布大小**為所需的精確尺寸。

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.AutomaticLayoutsScaling = true;
rasterizationOptions.NoScaling = false;
```

### 步驟 3：建立 PdfOptions（將 CAD 匯出為 PDF）

將光柵化設定連結至 `PdfOptions` 物件。此配置可讓您**將 CAD 匯出為 PDF**，並使用先前自訂的畫布。

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

### 步驟 4：匯出為 PDF（將 DXF 轉換為 PDF）

現在將影像儲存為 PDF。此步驟**從 CAD 建立 PDF**，使用我們先前設定的選項。

```csharp
image.Save(MyDir + "result_out.pdf", pdfOptions);
```

### 步驟 5：建立 TiffOptions（將 CAD 匯出為 TIFF）

若您同時需要光柵影像，請設定 `TiffOptions`。相同的光柵化選項會被重複使用，確保**將 CAD 匯出為 TIFF**時遵循相同的畫布大小。

```csharp
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.VectorRasterizationOptions = rasterizationOptions;
```

### 步驟 6：匯出為 TIFF

最後，將圖紙儲存為 TIFF 檔案。

```csharp
image.Save(MyDir + "result_out.tiff", tiffOptions);
```

## 常見問題與解決方案

- **畫布被裁切** – 請確認 `AutomaticLayoutsScaling` 設為 `true` 且 `NoScaling` 為 `false`，讓圖紙縮放以符合畫布。  
- **PDF 解析度過低** – 增加 `PageWidth`/`PageHeight` 或在 `CadRasterizationOptions` 上設定 `Resolution`。  
- **找不到檔案錯誤** – 確認 `MyDir` 指向有效目錄，且 DXF 檔名完全相符。

## 常見問答

### Q1：我可以將 Aspose.CAD 與其他 .NET 函式庫一起使用嗎？
A1：可以，Aspose.CAD 能與其他 .NET 函式庫無縫整合，提供更強大的 CAD 操作功能。

### Q2：Aspose.CAD 有免費試用版嗎？
A2：有，您可以使用免費試用版探索 Aspose.CAD 的功能。請前往 [here](https://releases.aspose.com/) 開始。

### Q3：如何取得 Aspose.CAD 的支援？
A3：欲取得支援與討論，請造訪 [Aspose.CAD forum](https://forum.aspose.com/c/cad/19)。

### Q4：哪裡可以找到 Aspose.CAD 的完整文件？
A4：請參考 [Aspose.CAD documentation](https://reference.aspose.com/cad/net/) 取得詳細資訊與範例。

### Q5：如何購買 Aspose.CAD for .NET？
A5：前往 [purchase page](https://purchase.aspose.com/buy) 進行購買。

**其他問答**

**Q：我可以將多頁 CAD 圖紙匯出為單一 PDF 嗎？**  
A：可以。於 `CadRasterizationOptions` 中設定 `PageCount`，程式庫會將多頁合併為一個 PDF。

**Q：畫布大小會影響向量資料的品質嗎？**  
A：向量資料本身保持解析度獨立；畫布大小僅影響光柵化元素與影像解析度。

**最後更新：** 2026-03-29  
**測試環境：** Aspose.CAD 24.11 for .NET  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}