---
date: 2026-08-23
description: 了解如何使用 Aspose.CAD 在 C# 中建立 viewport DWG。本指南涵蓋載入 DWG 檔案、設定光柵化、定義 viewport，以及將結果儲存為
  PDF。
keywords:
- create viewport dwg c#
- render dwg c#
- aspose.cad .net
lastmod: 2026-08-23
linktitle: 在 C# 中渲染 DWG 文件
og_description: 了解如何在 .NET 中使用 Aspose.CAD 於 C# 建立 viewport DWG。此逐步指南說明載入、光柵化、定義 viewport
  以及儲存為 PDF 的流程。
og_image_alt: Guide showing how to create viewport dwg c# with Aspose.CAD in .NET
og_title: 如何在 C# 中使用 Aspose.CAD for .NET 建立 viewport DWG
schemas:
- author: Aspose
  dateModified: '2026-08-23'
  description: Learn how to create viewport dwg c# using Aspose.CAD. This guide covers
    loading a DWG file, configuring rasterization, defining a viewport, and saving
    the result as PDF.
  headline: How to create viewport dwg c# with Aspose.CAD for .NET
  type: TechArticle
- questions:
  - answer: Load the DWG file with `CadImage.Load`.
    question: What is the first step?
  - answer: '`Viewport` inside `CadRasterizationOptions`.'
    question: Which class defines the view area?
  - answer: Yes, using `PdfOptions` after rasterization.
    question: Can I output to PDF?
  - answer: A commercial license is required; a free trial works for evaluation.
    question: Do I need a license for production?
  - answer: Absolutely – Aspose.CAD works with .NET Framework, .NET Core, and .NET 5/6.
    question: Is .NET Core supported?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- create viewport dwg c#
- Aspose.CAD
- C# CAD rendering
- DWG to PDF
- CAD viewports
title: 如何在 C# 中使用 Aspose.CAD for .NET 建立 viewport DWG
url: /zh-hant/net/image-manipulation-and-rendering/rendering-dwg-documents/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 C# 中渲染 DWG 文件 – 建立視口 dwg c# 教程

## 介紹

在本完整教學中，您將學習如何使用 Aspose.CAD **create viewport dwg c#** 並將 DWG 檔案轉換為 PDF。無論您是需要提取特定版面、產生可列印的圖紙，或在報告中嵌入 CAD 視圖，控制視口都能提供精確的渲染控制。Aspose.CAD 支援 **20+ CAD formats**，且能在不將整個文件載入記憶體的情況下處理含有數千個實體的檔案，十分適合高效能 .NET 應用程式。

## 快速回答
- **第一步是什麼？** Load the DWG file with `CadImage.Load`.
- **哪個類別定義視圖區域？** `Viewport` inside `CadRasterizationOptions`.
- **我可以輸出為 PDF 嗎？** Yes, using `PdfOptions` after rasterization.
- **生產環境需要授權嗎？** A commercial license is required; a free trial works for evaluation.
- **支援 .NET Core 嗎？** Absolutely – Aspose.CAD works with .NET Framework, .NET Core, and .NET 5/6.

## 前置條件

在深入程式碼之前，請確保您已具備：

- 基本的 C# 程式設計知識。
- 已安裝 Visual Studio（任何近期版本）。
- 已將 Aspose.CAD 函式庫加入您的專案。您可以從 [Aspose.CAD download page](https://releases.aspose.com/cad/net/) 下載。
- 一個範例 DWG 檔案，例如 **Bottom_plate.dwg**，以便跟隨教學。

## 匯入命名空間

在 C# 檔案的頂部加入所需的 `using` 指令，讓編譯器能找到 Aspose.CAD 類型。

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.FileFormats.Cad;
```

現在環境已就緒，讓我們一步一步走過實作流程。

## 如何建立 viewport dwg c#？

要建立自訂視口，首先將 DWG 檔案載入 `CadImage` 物件，接著以所需的版面與縮放設定 `CadRasterizationOptions`。定義要顯示的區域，使用計算出的中心、高度與長寬比實例化 `CadVportTableObject`，取代目前的視口，設定 PDF 選項，最後儲存結果。

## 步驟 1：載入 dwg 檔案

`CadImage.Load` 會將 DWG 檔案載入為 `CadImage` 物件，該物件在記憶體中代表 CAD 圖面。

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Your code for loading the DWG file goes here.
}
```

## 步驟 2：設定光柵化選項

`CadRasterizationOptions` 指定 CAD 圖面的光柵化方式，包括版面選擇、縮放與輸出尺寸。

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new string[] { "Model" };
rasterizationOptions.NoScaling = true;
// Additional rasterization configurations can be added here.
```

## 步驟 3：定義繪製區域

`Point` 定義要渲染區域左上角的 X 與 Y 座標。

```csharp
Point topLeft = new Point(6156, 7053);
double width = 3108;
double height = 2489;
```

## 步驟 4：建立新視口

`CadVportTableObject` 代表一個視口物件，控制渲染圖面的可見區域與長寬比。

```csharp
CadVportTableObject newView = new CadVportTableObject();
newView.Name.Value = "*Active";
newView.CenterPoint.X = topLeft.X + width / 2f;
newView.CenterPoint.Y = topLeft.Y - height / 2f;
newView.ViewHeight.Value = height;
newView.ViewAspectRatio.Value = width / height;
```

## 步驟 5：取代活動視口

此迴圈將活動視口取代為新建立的視口，以套用自訂的檢視設定。

```csharp
for (int i = 0; i < cadImage.ViewPorts.Count; i++)
{
    CadVportTableObject currentView = (CadVportTableObject)(cadImage.ViewPorts[i]);
    if ((currentView.Name.Value == null && cadImage.ViewPorts.Count == 1) ||
    string.Equals(currentView.Name.Value.ToLowerInvariant(), "*active"))
    {
        cadImage.ViewPorts[i] = newView;
        break;
    }
}
```

## 步驟 6：設定 PDF 選項

`PdfOptions` 設定 PDF 輸出的參數，例如壓縮與中繼資料。

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## 步驟 7：將渲染的 dwg 儲存為 PDF

`image.Save` 依指定的格式選項將渲染後的圖像寫入檔案。

```csharp
cadImage.Save(MyDir, pdfOptions);
```

## 為何在渲染 DWG 時使用自訂視口？

自訂視口可讓您聚焦於特定版面或區域，減少檔案大小並提升渲染速度。使用聚焦視口時，Aspose.CAD 能在 2 秒內渲染 300 頁的 DWG，而完整圖面渲染則可能多耗數秒。

## 常見問題與解決方案

- **空白輸出** – 確保視口座標位於圖紙範圍內；使用 `CadImage.Size` 來驗證邊界。
- **缺少圖層** – 設定 `CadRasterizationOptions.Layouts` 為正確的版面名稱；否則預設版面可能為空。
- **效能下降** – 若只需要快速預覽，請在 `CadRasterizationOptions` 中停用 anti‑aliasing。

## 常見問答

### Q1：我可以將 Aspose.CAD 用於其他 CAD 檔案格式嗎？

A1: Yes, Aspose.CAD supports various formats, including DWG, DXF, DWF, and more than 20 additional CAD types.

### Q2：Aspose.CAD 相容於 .NET Core 嗎？

A2: Yes, Aspose.CAD works with .NET Framework, .NET Core, and the latest .NET releases.

### Q3：如何處理 DWG 檔案中的不同版面？

A3: Specify the desired layout using the `Layouts` property of `CadRasterizationOptions` before rendering.

### Q4：使用 Aspose.CAD 有哪些授權考量？

A4: For licensing details, visit [Aspose.CAD licensing page](https://purchase.aspose.com/buy).

### Q5：我可以在哪裡取得額外支援？

A5: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for community help and discussions.

### Q6：我可以直接渲染成 PNG 而非 PDF 嗎？

A6: Yes, change the `PdfOptions` to `PngOptions` and call `image.Save("output.png", pngOptions)`.

### Q7：如何將渲染的圖像嵌入 Windows Forms 應用程式？

A7: Load the saved image into a `PictureBox` control using `Image.FromFile("output.png")`.

## 結論

您現在已掌握如何 **create viewport dwg c#** 並使用 Aspose.CAD 將 DWG 檔案渲染為 PDF（或其他光柵格式）。透過熟悉視口操作，您可以對視覺輸出取得細緻的控制，這對於產生精確的工程圖、報告或縮圖至關重要。探索更多光柵化設定、嘗試不同的輸出格式，並將程式碼整合至更大的 .NET 服務或桌面工具中。

---

**最後更新：** 2026-08-23  
**測試環境：** Aspose.CAD 24.11 for .NET  
**作者：** Aspose

## 相關教學

- [如何在 C# 中使用座標將 DWG 轉換為 PDF 時設定視口 - Aspose.CAD 教程](/cad/net/conversion-and-export/converting-dwg-to-pdf-with-coordinates/)
- [學習設定 CAD 光柵化選項 – 使用 Aspose.CAD 匯出特定版面至 PDF](/cad/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/)
- [如何使用 Aspose.CAD for .NET 將 DWG 轉換為 PDF 與光柵圖像](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}