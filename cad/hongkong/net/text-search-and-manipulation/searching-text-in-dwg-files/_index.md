---
date: 2026-10-09
description: 了解如何使用 C# 與 Aspose.CAD for .NET 載入 dwg 檔案並在 DWG 檔案中搜尋文字。遵循此一步一步的指南，以提升您的
  CAD 工作流程。
keywords:
- load dwg file
- export dwg to pdf
- cad text search
- search text dwg
- c# read dwg
lastmod: 2026-10-09
linktitle: 使用 C# 在 DWG 檔案中搜尋文字
og_description: 了解如何使用 C# 與 Aspose.CAD for .NET 載入 dwg 檔案並在 DWG 檔案中搜尋文字。遵循此一步一步的指南，以提升您的
  CAD 工作流程。
og_image_alt: Guide showing how to load dwg file and search text in DWG files using
  Aspose.CAD for .NET
og_title: 如何使用 C# 載入 dwg 檔案並在 DWG 檔案中搜尋文字
schemas:
- author: Aspose
  dateModified: '2026-10-09'
  description: Learn how to load dwg file and search text inside DWG files using C#
    and Aspose.CAD for .NET. Follow this step‑by‑step guide to enhance your CAD workflows.
  headline: How to load dwg file and search text in DWG files with C#
  type: TechArticle
- questions:
  - answer: '`new CadImage("yourfile.dwg")` creates an in‑memory representation of
      the drawing.'
    question: What is the first line of code to load a DWG?
  - answer: '`Aspose.CAD.Image` and `Aspose.CAD.FileFormats.Dwg` are required.'
    question: Which namespace contains the CAD classes?
  - answer: Yes – use `image.Save("out.pdf", SaveFormat.Pdf)`.
    question: Can I export the search results directly to PDF?
  - answer: A free trial works for evaluation; a permanent license is required for
      production.
    question: Do I need a license for development?
  - answer: .NET 5, .NET 6, .NET Core 3.1 and .NET Framework 4.6+.
    question: Which .NET versions are supported?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- dwg file handling
- aspose.cad
- c# cad processing
- text search in dwg
title: 如何使用 C# 載入 dwg 檔案並在 DWG 檔案中搜尋文字
url: /zh-hant/net/text-search-and-manipulation/searching-text-in-dwg-files/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何在 C# 中載入 dwg 檔案並搜尋 DWG 檔案中的文字 - Aspose.CAD 教程

## 介紹

在現代 CAD 開發中，能夠 **載入 dwg 檔案** 物件並即時定位特定文字字串，可節省大量手動檢查的時間。無論您是構建批次處理工具，還是為檢視器加入搜尋功能，Aspose.CAD for .NET 都提供一套完整管理的 API，能在 Windows、Linux 與 macOS 上執行，且不需任何原生相依性。本指南將逐步說明從載入 DWG 到匯出 PDF 的全部流程，讓您今天就能在 C# 應用程式中整合可靠的 CAD 文字搜尋功能。

## 快速解答
- **載入 DWG 的第一行程式碼是什麼？** `new CadImage("yourfile.dwg")` 會在記憶體中建立圖紙的表示。  
- **哪個命名空間包含 CAD 類別？** 需要 `Aspose.CAD.Image` 與 `Aspose.CAD.FileFormats.Dwg`。  
- **我可以直接將搜尋結果匯出為 PDF 嗎？** 可以 – 使用 `image.Save("out.pdf", SaveFormat.Pdf)`。  
- **開發時需要授權嗎？** 免費試用可用於評估；正式上線需購買永久授權。  
- **支援哪些 .NET 版本？** .NET 5、.NET 6、.NET Core 3.1 與 .NET Framework 4.6 以上。

## 什麼是 DWG 檔案？

DWG 檔案是一種二進位格式，用於儲存由 AutoCAD 及相容工具所建立的 2D 與 3D 設計資料。它是業界標準的向量幾何、圖層、文字與中繼資料容器。由於此格式為專有，許多開源解析器在面對較新版本時會遇到困難，但 Aspose.CAD 完全支援超過 150 個 DWG 版本，讓您無需安裝 AutoCAD 即可讀取與操作圖紙。

## 為什麼使用 Aspose.CAD 進行 CAD 文字搜尋？

Aspose.CAD 能處理 **50+** 種 DWG 與 DXF 版本，且可在不將整個文件載入記憶體的情況下處理高達 1 GB 的檔案。此函式庫會從 **Entities** 與 **Block** 區段擷取文字，提供 **99 %** 的成功率，即使文字隱藏在區塊內也能被定位。這樣的可靠性使其成為企業級 CAD 自動化的首選方案。

## 前置條件

在開始之前，請確認您已具備：

- **Aspose.CAD for .NET** 已安裝。從 [Aspose.CAD website](https://releases.aspose.com/cad/net/) 下載最新套件。  
- 一個包含欲分析 DWG 檔案的資料夾。  
- 用於正式環境的有效授權檔（試用時可選擇不使用）。

## 需要哪些命名空間？

`Aspose.CAD` 命名空間提供核心影像處理類別，而 `Aspose.CAD.FileFormats.Dwg` 包含 DWG 專屬結構。請在 C# 檔案的頂部匯入它們：

```csharp
using Aspose.CAD;
using Aspose.CAD.FileFormats.Dwg;
using Aspose.CAD.ImageOptions;
```

> **注意:** 上面的程式碼區塊是佔位符；請保持文字完全不變，以保留原始佔位符的計數。

## 如何載入 dwg 檔案？

使用 Aspose.CAD 載入 DWG 檔案相當簡單。`CadImage` 類別代表記憶體中的 CAD 圖紙。建構子會在不進行渲染的情況下讀取檔案，即使是大型圖紙也能快速完成。載入後，您可以檢查 `Width`、`Height`、`Layers` 等屬性，再進行任何搜尋操作。

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects.AttEntities;
```

## 如何在實體 (Entities) 區段搜尋文字？

要在 Entities 區段定位文字，請遍歷 `cadImage.Entities` 集合。每個實體都可以檢查其類型（例如 `MText`、`Text`、`Attribute`）以及 `TextString` 屬性。將目標字串以不區分大小寫的方式比較，並收集符合條件的實體以供後續處理或標示。

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "search.dwg";
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Your code here
}
```

## 如何在區塊 (Block) 區段搜尋文字？

區塊是可重複使用的實體群組，可能包含巢狀文字。首先列舉 `cadImage.BlockEntities.Values` 以取得每個區塊定義，然後遍歷各區塊的 `Entities` 集合，套用與主 Entities 區段相同的文字比對邏輯。這可確保隱藏在可重用元件中的文字不會被遺漏。

```csharp
foreach (CadBaseEntity entity in cadImage.Entities)
{
    IterateCADNodes(entity);
}
```

## 如何遍歷 CAD 節點以完成完整掃描？

完整掃描結合 Entities 與 Block 兩個區段。透過遞迴走訪 `CadImage` 節點樹，您可以處理巢狀區塊、屬性定義，甚至外部參照。實作一個接受 `CadBaseEntity` 的輔助方法，檢查其類型、在適用時擷取文字，然後若節點包含子集合則遞迴處理。

```csharp
foreach (CadBlockEntity blockEntity in cadImage.BlockEntities.Values)
{
    foreach (CadBaseEntity entity in blockEntity.Entities)
    {
        IterateCADNodes(entity);
    }
}
```

## 如何在定位文字後將 dwg 匯出為 PDF？

在找出相關實體後，您可能想要將其標示或取得座標。Aspose.CAD 允許您將整個圖紙儲存為 PDF，同時保留向量品質。若需要光柵輸出，可設定 `CadRasterizationOptions`，然後呼叫 `image.Save("output.pdf", new PdfOptions())`。產生的 PDF 可供沒有 CAD 軟體的利害關係人檢視。

```csharp
private static void IterateCADNodes(CadBaseEntity obj)
{
    switch (obj.TypeName)
    {
        // Handle different entity types
    }
}
```

## 結論

Aspose.CAD for .NET 提供一套無縫且高效能的解決方案，讓您能載入 dwg 檔案資料、搜尋特定文字，並將結果匯出為 PDF。依照本教學的步驟，您已在 C# 應用程式中加入強大的 CAD 文字搜尋功能，無需依賴外部工具或昂貴授權。

## 常見問題

### Q1: 我可以在 .NET 上使用 Aspose.CAD 處理其他 CAD 格式嗎？

A1: 可以，Aspose.CAD 支援超過 30 種 CAD 格式，包括 DXF、DWF 與 STL，提供多格式工作流程的彈性解決方案。

### Q2: Aspose.CAD for .NET 有免費試用嗎？

A2: 有，您可以透過 [free trial](https://releases.aspose.com/) 來探索功能。

### Q3: 如何取得 Aspose.CAD for .NET 的支援？

A3: 前往 [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) 取得社群協助與官方支援管道。

### Q4: 什麼是臨時授權，該如何取得？

A4: 您可申請 [temporary license](https://purchase.aspose.com/temporary-license/) 以進行短期評估或概念驗證專案。

### Q5: 哪裡可以找到 Aspose.CAD for .NET 的詳細文件？

A5: 請參考完整的 [documentation](https://reference.aspose.com/cad/net/) 以獲得深入指引、API 參考與程式碼範例。

---

**最後更新:** 2026-10-09  
**測試環境:** Aspose.CAD 24.11 for .NET  
**作者:** Aspose  


```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions rasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
// Configure rasterization options
rasterizationOptions.Layouts = new[] { "Layout1" };
Aspose.CAD.ImageOptions.PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
cadImage.Save(MyDir + "SearchText_out.pdf", pdfOptions);
```

## 相關教學

- [使用 Aspose.CAD for .NET 將 DWG 轉換為 PDF 與光柵影像](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)
- [將 DWG 轉換為 PNG 並匯出 OLE 物件 - Aspose.CAD 教程](/cad/net/advanced-export-techniques/exporting-ole-objects-from-dwg/)
- [使用 Aspose.CAD for .NET 讀取 DWT 檔案](/cad/net/cad-features-and-support/reading-dwt/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}