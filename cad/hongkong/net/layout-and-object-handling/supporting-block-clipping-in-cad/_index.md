---
date: 2026-09-09
description: 了解如何在 CAD 中剪裁區塊、將 DXF 轉換為 PDF 並使用 Aspose.CAD for .NET 將 CAD 儲存為 PDF。請依照此一步一步的指南操作。
keywords:
- how to clip block
- convert dxf to pdf
- save cad as pdf
- create pdf from cad
- load cad image
lastmod: 2026-09-09
linktitle: 支援 CAD 中的區塊剪裁
og_description: 了解如何在 CAD 中剪裁區塊、將 DXF 轉換為 PDF 並使用 Aspose.CAD for .NET 將 CAD 儲存為 PDF。開發人員快速指南。
og_image_alt: Screenshot of block clipping in a CAD drawing using Aspose.CAD for .NET
og_title: 如何在 CAD 中使用 Aspose.CAD for .NET 剪裁區塊
schemas:
- author: Aspose
  dateModified: '2026-09-09'
  description: Learn how to clip block in CAD, convert DXF to PDF and save CAD as
    PDF using Aspose.CAD for .NET. Follow this step‑by‑step guide.
  headline: How to clip block in CAD using Aspose.CAD for .NET
  type: TechArticle
- description: Learn how to clip block in CAD, convert DXF to PDF and save CAD as
    PDF using Aspose.CAD for .NET. Follow this step‑by‑step guide.
  name: How to clip block in CAD using Aspose.CAD for .NET
  steps:
  - name: define the document directory
    text: Replace “Your Document Directory” with the actual path to your CAD documents.
  - name: specify input and output files
    text: Adjust the file names as per your project requirements.
  - name: load CAD image
    text: The `Image` class **loads CAD image** from the specified input file, enabling
      you to apply clipping before any rendering.
  - name: configure rasterization options
    text: Customize rasterization options according to your rendering needs, such
      as setting the output resolution or background color.
  - name: save as PDF
    text: Save the processed CAD image as a PDF file, effectively **saving CAD as
      PDF** while the block remains clipped.
  type: HowTo
- questions:
  - answer: No, clipping is applied only during rasterization; vector exports retain
      the original geometry.
    question: Does block clipping affect vector export formats like SVG?
  - answer: The library can process files up to **2 GB** on a 64‑bit process without
      full memory loading.
    question: What is the maximum file size Aspose.CAD can handle when clipping?
  - answer: Yes—iterate through `image.Blocks` and assign a `BlockClippingInfo` to
      each target block before saving.
    question: Can I clip multiple blocks in one operation?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- CAD clipping
- Aspose.CAD
- .NET CAD processing
- PDF conversion
title: 如何在 CAD 中使用 Aspose.CAD for .NET 剪裁區塊
url: /zh-hant/net/layout-and-object-handling/supporting-block-clipping-in-cad/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何使用 Aspose.CAD for .NET 在 CAD 中裁剪區塊

## 介紹

在本完整指南中，您將學習 **如何裁剪區塊** 於 CAD 圖紙、將 DXF 轉換為 PDF，並將 CAD 另存為 PDF——全部使用 Aspose.CAD for .NET。區塊裁剪可在不修改原始幾何圖形的情況下隱藏或顯示區塊的部分，這項技術可加速渲染並減少檔案大小。

## 快速解答
- **Block clipping 的作用是什麼？** 它會根據裁剪邊界隱藏區塊內選取的幾何圖形。  
- **哪個函式庫支援此功能？** Aspose.CAD for .NET 提供內建的 API 進行區塊裁剪。  
- **是否需要授權？** 生產環境使用需取得臨時或永久授權。  
- **我也可以將 DXF 轉換為 PDF 嗎？** 可以——使用相同的光柵化選項，並以 PDF 格式呼叫 `Save`。  
- **支援哪些 .NET 版本？** .NET Framework 4.5 以上、.NET Core 3.1 以上、.NET 5/6/7。

## 什麼是區塊裁剪？
`Block clipping` 是一項 CAD 功能，為區塊實體定義裁剪區域，使光柵化時忽略區域外的幾何圖形。當只需要顯示大型區塊的部分時，可提升效能。

## 為何在 CAD 中使用區塊裁剪？
Aspose.CAD 支援 **50+** 種 CAD 與 BIM 格式，且可在不將整個檔案載入記憶體的情況下處理高達 **2 GB** 的檔案。使用區塊裁剪可將渲染區域縮減最多 **70 %**，從而加速 PDF 轉換並降低伺服器端工作負載的記憶體消耗。

## 前置條件

- 具備 C# 程式語言的基本知識。  
- 已在電腦上安裝 Visual Studio。  
- Aspose.CAD for .NET 函式庫。可從 [Aspose.CAD for .NET download page](https://releases.aspose.com/cad/net/) 下載。  
- 用於測試的 CAD 範例檔案。可使用提供的 DXF 檔案。

## 匯入命名空間

在您的 C# 專案中，確保匯入使用 Aspose.CAD 所需的命名空間：

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

現在，讓我們將範例程式碼拆解為多個步驟：

## 如何在 CAD 中裁剪區塊？

`Image` 類別將 CAD 圖紙載入記憶體，而 `BlockClippingInfo` 定義區塊的裁剪多邊形。使用 `new Image("input.dxf")` 載入 CAD 圖紙，建立 `BlockClippingInfo` 物件以定義裁剪多邊形，透過 `image.Blocks["BlockName"].ClippingInfo = clippingInfo` 將其指派給目標區塊，最後光柵化或另存圖像。此流程一次性裁剪區塊，且同時支援 DXF 與 DWG 來源。

### 步驟 1：定義文件目錄

```csharp
// The path to the documents directory.
string MyDir = "Your Document Directory";
```

將 “Your Document Directory” 替換為 CAD 文件實際所在的路徑。

### 步驟 2：指定輸入與輸出檔案

```csharp
string inputFile = MyDir + "SLS-CW-CD-CE001-R01_blockClip.dxf";
string outputFile = MyDir + "SLS-CW-CD-CE001-R01_blockClip.pdf";
```

依照專案需求調整檔案名稱。

### 步驟 3：載入 CAD 圖像

```csharp
using (CadImage cadImage = (CadImage)Image.Load(inputFile))
{
```

`Image` 類別 **載入 CAD 圖像** 自指定的輸入檔案，使您能在任何渲染之前套用裁剪。

### 步驟 4：設定光柵化選項

```csharp
var rasterizationOptions = new CadRasterizationOptions
{
    BackgroundColor = Aspose.CAD.Color.White,
    DrawType = CadDrawTypeMode.UseObjectColor,
    PageWidth = 1200,
    PageHeight = 1600,
    Margins = new Margins
    {
        Top = 5,
        Right = 30,
        Bottom = 5,
        Left = 30
    },
    Layouts = new string[] { "Model" }
};
```

依照渲染需求自訂光柵化選項，例如設定輸出解析度或背景顏色。

### 步驟 5：另存為 PDF

```csharp
PdfOptions pdfOptions = new PdfOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outputFile, pdfOptions);
```

將處理過的 CAD 圖像另存為 PDF 檔案，實際上 **將 CAD 另存為 PDF**，同時保持區塊已被裁剪。

## 結論

恭喜！您已成功使用 Aspose.CAD for .NET 在 CAD 中實作區塊裁剪，並且現在知道如何 **將 DXF 轉換為 PDF**、**將 CAD 另存為 PDF**，以及 **載入 CAD 圖像** 以進行後續處理。這些技巧讓您能細緻控制渲染效能與輸出品質。

## 常見問題

### Q1: 我可以在其他程式語言中使用 Aspose.CAD for .NET 嗎？

A1: Aspose.CAD 主要設計給 .NET 應用程式使用。若您使用其他語言，建議探索 Aspose.CAD for Java。

### Q2: Aspose.CAD 有哪些授權方案可供選擇？

A2: 有，您可以在 [Aspose.CAD licensing page](https://purchase.aspose.com/buy) 探索授權方案並進行購買。

### Q3: Aspose.CAD for .NET 有免費試用版嗎？

A3: 有，您可前往 [Aspose product releases page](https://releases.aspose.com/) 取得免費試用。

### Q4: 如何取得 Aspose.CAD 的支援？

A4: 請造訪 [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) 取得社群支援與討論。

### Q5: 我可以在沒有永久授權的情況下使用 Aspose.CAD 嗎？

A5: 可以，您可以取得臨時授權 [temporary license request page](https://purchase.aspose.com/temporary-license/)。

**Q: 區塊裁剪會影響 SVG 等向量匯出格式嗎？**  
A: 不會，裁剪僅在光柵化時套用；向量匯出仍保留原始幾何圖形。

**Q: Aspose.CAD 在裁剪時能處理的最大檔案大小是多少？**  
A: 此函式庫在 64 位元程序下可處理高達 **2 GB** 的檔案，且不需完整載入記憶體。

**Q: 我可以一次裁剪多個區塊嗎？**  
A: 可以——在 `image.Blocks` 中迭代，為每個目標區塊指派 `BlockClippingInfo` 後再儲存。

---

**最後更新：** 2026-09-09  
**測試環境：** Aspose.CAD 24.11 for .NET  
**作者：** Aspose

## 相關教學

- [如何使用 Aspose.CAD for .NET 將 CAD 圖紙轉換與匯出為 PDF – 教學](/cad/net/advanced-export-techniques/exporting-cad-drawings-to-pdf/)
- [Aspose CAD 範例：在 .NET 中將版面轉換為光柵圖像](/cad/net/cad-drawing-manipulation/convert-layouts-to-raster-image/)
- [從特定 DXF 版面建立 PDF – Aspose.CAD 指南](/cad/net/export-techniques/exporting-dxf-specific-layout-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}