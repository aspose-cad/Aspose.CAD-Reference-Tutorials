---
date: 2026-07-09
description: 了解如何使用 Aspose.CAD for .NET 將 IGES 轉換為 PDF。按照此一步一步的指南，快速且精確地將 IGES 檔案匯出為
  PDF。
keywords:
- convert iges to pdf
- export iges as pdf
- create pdf from iges
- convert cad file to pdf
- generate pdf from cad
lastmod: 2026-07-09
linktitle: 將 IGES 檔案匯出為 PDF
og_description: 使用 Aspose.CAD for .NET 將 IGES 轉換為 PDF。本教學示範如何透過免寫程式碼的步驟，高效地將 IGES
  檔案匯出為 PDF。
og_image_alt: Guide showing conversion of IGES files to PDF with Aspose.CAD in .NET
og_title: 將 IGES 轉換為 PDF – Aspose.CAD 快速指南
schemas:
- author: Aspose
  dateModified: '2026-07-09'
  description: Learn how to convert IGES to PDF using Aspose.CAD for .NET. Follow
    this step‑by‑step guide to export IGES files as PDF quickly and accurately.
  headline: Convert IGES to PDF with Aspose.CAD – Quick Guide
  type: TechArticle
- description: Learn how to convert IGES to PDF using Aspose.CAD for .NET. Follow
    this step‑by‑step guide to export IGES files as PDF quickly and accurately.
  name: Convert IGES to PDF with Aspose.CAD – Quick Guide
  steps:
  - name: Set up Your Project
    text: Create a new .NET console or class‑library project, or open an existing
      one where you want to add the conversion feature.
  - name: Add Aspose.CAD Reference
    text: Add the downloaded Aspose.CAD DLL to your project references. In Visual
      Studio, right‑click **References → Add Reference → Browse** and select the DLL.
  - name: Initialize the Path
    text: Define the folder that contains your IGES file and the output location.
  - name: Load the CAD Image
    text: '`Image.Load` reads the IGES file and creates an in‑memory representation.
      The `Image` class is Aspose.CAD''s primary entry point for any CAD format.'
  - name: Configure Rasterization Options
    text: '`PdfOptions` (derived from `CadRasterizationOptions`) lets you set page
      size, resolution, and vector‑preserving flags. The `PdfOptions` class defines
      how the CAD drawing is rasterized and saved as PDF.'
  - name: Save as PDF
    text: Finally, write the PDF file to disk. With these six straightforward steps,
      you have successfully **convert iges to pdf** using Aspose.CAD for .NET.
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD works in ASP.NET, ASP.NET Core, and other web frameworks,
      providing server‑side conversion without UI dependencies.
    question: Can I use Aspose.CAD for .NET in a web application?
  - answer: Explore the comprehensive documentation [here](https://reference.aspose.com/cad/net/)
      for detailed insights into all supported features.
    question: Where can I find additional documentation for Aspose.CAD?
  - answer: Yes, you can access a free trial [here](https://releases.aspose.com/)
      to evaluate the library before purchasing.
    question: Is there a free trial available?
  - answer: For temporary licenses, visit [this link](https://purchase.aspose.com/temporary-license/)
      to get the required licensing information.
    question: How can I obtain a temporary license?
  - answer: Join the Aspose.CAD community on the [support forum](https://forum.aspose.com/c/cad/19)
      for prompt help and discussions.
    question: Need assistance or have questions?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- convert iges to pdf
- Aspose.CAD
- .NET CAD conversion
title: 使用 Aspose.CAD 將 IGES 轉換為 PDF – 快速指南
url: /zh-hant/net/exporting-to-image-formats/exporting-iges-files-to-pdf/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 將 IGES 轉換為 PDF（使用 Aspose.CAD）

## 簡介

在快速變化的電腦輔助設計領域，**將 IGES 轉換為 PDF** 是工程師與建築師每天執行的例行工作。無論您需要可列印的文件供客戶審閱，或是為版本控制而製作輕量化的存檔，將 IGES 檔案匯出為 PDF 能保留原始幾何形狀，同時讓檔案在任何平台上皆可存取。本教學將逐步說明如何使用 Aspose.CAD for .NET 將 IGES 轉換為 PDF，讓您能在任何 .NET 應用程式中自動化此流程。

## 快速答覆
- **什麼函式庫負責轉換？** Aspose.CAD for .NET。  
- **需要多少行程式碼？** 通常兩行：載入 IGES 檔案並呼叫 `Save`。  
- **我可以控制頁面大小和品質嗎？** 可以，透過 `CadRasterizationOptions`。  
- **生產環境是否需要授權？** 需要商業授權；亦提供免費試用。您可在[此連結](https://purchase.aspose.com/temporary-license/)取得臨時授權。  
- **支援哪些 .NET 版本？** .NET Framework 4.5+、.NET Core 3.1+、.NET 5/6/7。

## 什麼是「將 IGES 轉換為 PDF」？
*將 IGES 轉換為 PDF* 意指將中立的 CAD 交換檔（IGES）渲染為可在任何裝置上開啟的可攜式文件格式（PDF），無需 CAD 軟體。此轉換會保留向量幾何、圖層與註解，同時將它們平面化為固定版面的文件。

## 為什麼在此轉換中使用 Aspose.CAD？
Aspose.CAD 支援 **30+ CAD 與 BIM 格式**，且可在不將整個文件載入記憶體的情況下處理高達 **2 GB** 的檔案，提供快速的伺服器端轉換且無需任何第三方相依性。此量化效能使其非常適合批次處理管線與雲端服務。

## 先決條件

在開始之前，請確保您具備以下項目：

1. **Aspose.CAD for .NET Library** – 從[此處](https://releases.aspose.com/cad/net/)下載。您亦可在[此處](https://reference.aspose.com/cad/net/)檢視 API 參考。  
2. **.NET 開發環境** – Visual Studio、Rider，或任何支援 .NET 5+ 的 IDE。

先決條件確認完畢後，讓我們匯入轉換所需的命名空間。

## 匯入命名空間

`Image` 類別是代表 CAD 圖面於記憶體中的主要類別。`CadRasterizationOptions` 定義了 CAD 圖面向向量輸出時的光柵化方式。`PdfOptions` 類別則指定 PDF 檔案的輸出設定。

``` 
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
```

這些命名空間提供了載入、光柵化與儲存 CAD 圖面的核心功能。

## 如何使用 Aspose.CAD 將 IGES 轉換為 PDF？

使用 `Image.Load` 載入 IGES 檔案，接著以 PDF 光柵化選項呼叫 `Save`——只需兩行程式碼即可完成完整轉換。函式庫會自動處理向量渲染、字型嵌入與頁面縮放，為您產生與原始 IGES 模型相符的 PDF 複本。

### 步驟 1：設定專案

建立新的 .NET 主控台或類別庫專案，或在現有專案中加入轉換功能。

### 步驟 2：加入 Aspose.CAD 參考

將下載好的 Aspose.CAD DLL 加入專案參考。於 Visual Studio 中，右鍵點選 **References → Add Reference → Browse**，選取該 DLL。

### 步驟 3：初始化路徑

定義存放 IGES 檔案的資料夾以及輸出位置。

``` 
string sourceDir = @"C:\CAD\Source";
string outputDir = @"C:\CAD\Output";
string igesFile = Path.Combine(sourceDir, "sample.iges");
string pdfFile = Path.Combine(outputDir, "sample.pdf");
```

### 步驟 4：載入 CAD 圖像

`Image.Load` 讀取 IGES 檔案並在記憶體中建立對應的表示。

``` 
Image cadImage = Image.Load(igesFile);
```

`Image` 類別是 Aspose.CAD 針對任何 CAD 格式的主要入口點。

### 步驟 5：設定光柵化選項

`PdfOptions`（繼承自 `CadRasterizationOptions`）讓您設定頁面大小、解析度與向量保留旗標。

``` 
PdfOptions pdfOptions = new PdfOptions
{
    VectorRasterizationOptions = new CadRasterizationOptions
    {
        PageWidth = 842,      // A4 width in points
        PageHeight = 595,     // A4 height in points
        Resolution = 300      // 300 DPI for high‑quality output
    }
};
```

`PdfOptions` 類別定義了 CAD 圖面如何被光柵化並儲存為 PDF。

### 步驟 6：儲存為 PDF

最後，將 PDF 檔寫入磁碟。

``` 
cadImage.Save(pdfFile, pdfOptions);
```

透過上述六個簡易步驟，您已成功 **將 IGES 轉換為 PDF**，使用 Aspose.CAD for .NET。

## 常見陷阱與技巧

- **大型檔案：** 僅在需要更細緻的細節時才提升 `Resolution`，較高的 DPI 會佔用更多記憶體。  
- **缺少字型：** 確保 IGES 檔案使用的自訂字型已安裝於伺服器，否則會被替代。  
- **批次轉換：** 可將載入‑儲存邏輯包在 `foreach` 迴圈中，以自動處理多個 IGES 檔案。

## 常見問題

**Q: 我可以在 Web 應用程式中使用 Aspose.CAD for .NET 嗎？**  
A: 可以，Aspose.CAD 可在 ASP.NET、ASP.NET Core 以及其他 Web 框架中執行，提供無 UI 相依的伺服器端轉換。

**Q: 我在哪裡可以找到 Aspose.CAD 的其他文件？**  
A: 前往[此處](https://reference.aspose.com/cad/net/)探索完整文件，了解所有支援功能的細節。

**Q: 有免費試用版嗎？**  
A: 有，您可在[此處](https://releases.aspose.com/)取得免費試用版，以評估函式庫功能。

**Q: 如何取得臨時授權？**  
A: 前往[此連結](https://purchase.aspose.com/temporary-license/)取得臨時授權資訊。

**Q: 需要協助或有其他問題？**  
A: 加入 Aspose.CAD 社群於[支援論壇](https://forum.aspose.com/c/cad/19)取得即時協助與討論。

---

**最後更新：** 2026-07-09  
**測試環境：** Aspose.CAD 24.11 for .NET  
**作者：** Aspose

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using static Aspose.CAD.Examples.CSharp.DWG_Drawings.SupportMLeaderEntityForDWGFormat;
using Aspose.CAD.ImageOptions;
```

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "figa2.igs";
```

```csharp
using (Image cadImage = Image.Load(sourceFilePath))
{
    // Your code goes here
}
```

```csharp
CadRasterizationOptions options = new CadRasterizationOptions
{
    PageHeight = 1000,
    PageWidth = 1000,
};

PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = options;
```

```csharp
cadImage.Save(MyDir + "figa2.pdf", pdfOptions);
```

如需其他資源，請參閱主要發行頁面[此處](https://releases.aspose.com/)。若需要協助，請造訪[支援論壇](https://forum.aspose.com/c/cad/19)。

## 相關教學

- [Exporting DWG to PDF or Raster Images - Aspose.CAD Guide](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)
- [Exporting DXF to PDF Format - Aspose.CAD Tutorial](/cad/net/export-techniques/exporting-dxf-to-pdf-format/)
- [Export DGN to PDF in Aspose.CAD for .NET](/cad/net/cad-export-formats/export-dgn-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}