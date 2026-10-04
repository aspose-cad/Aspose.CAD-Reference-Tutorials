---
date: 2026-10-04
description: 了解如何使用 C# 及 Aspose.CAD for .NET 在 DWG 檔案中搜尋文字。提取文字、讀取 DWG 檔案，提升您的 CAD
  應用程式。
keywords:
- search text in dwg
- extract text from dwg
- c# read dwg file
- how to search dwg files
lastmod: 2026-10-04
linktitle: 文字搜尋與操作
og_description: 使用 C# 及 Aspose.CAD for .NET 在 DWG 檔案中搜尋文字。提取文字、讀取 DWG 檔案，提升 CAD 應用程式效能。
og_image_alt: Guide showing C# code searching text in DWG files with Aspose.CAD
og_title: 使用 C# 及 Aspose.CAD 在 DWG 檔案中搜尋文字
schemas:
- author: Aspose
  dateModified: '2026-10-04'
  description: Learn how to search text in DWG files using C# and Aspose.CAD for .NET.
    Extract text, read DWG files, and boost your CAD applications.
  headline: Search text in DWG files with C# using Aspose.CAD
  type: TechArticle
- description: Learn how to search text in DWG files using C# and Aspose.CAD for .NET.
    Extract text, read DWG files, and boost your CAD applications.
  name: Search text in DWG files with C# using Aspose.CAD
  steps:
  - name: install the Aspose.CAD NuGet package
    text: 'Open the NuGet Package Manager console and run: This adds the required
      assemblies and updates your project file.'
  - name: open the DWG file
    text: Create a `CadImage` instance by calling `Image.Load`. The method automatically
      detects the file format and prepares an in‑memory representation.
  - name: enumerate text fragments
    text: '`image.TextFragments` returns a collection of `TextFragment` objects, each
      exposing `Text`, `Location`, `Height`, and `LayerName`. You can iterate or LINQ‑filter
      this collection.'
  - name: apply your search criteria
    text: Use `String.Contains`, `Regex.IsMatch`, or any custom predicate to locate
      the exact text you need. For case‑insensitive searches, call `ToLowerInvariant()`
      on both sides.
  - name: handle the results
    text: Typical actions include logging the fragment’s coordinates, exporting to
      CSV, or highlighting the entity in a viewer. Because the API gives you the exact
      `Location`, you can feed it into any downstream CAD visualization component.
  type: HowTo
- questions:
  - answer: Yes. Provide the password via `CadLoadOptions.Password` when calling `Image.Load`.
    question: Can I search for text in password‑protected DWG files?
  - answer: Absolutely. Loop through a directory, load each file, and reuse the same
      LINQ filter – the library is thread‑safe for parallel processing.
    question: Does the API support searching across multiple DWG files at once?
  - answer: Aspose.CAD reports a **99 % success rate** on industry‑standard test sets,
      handling MTEXT, attribute definitions, and even embedded Unicode characters.
    question: How accurate is the text extraction for complex annotations?
  - answer: After obtaining the `Location` of each `TextFragment`, you can draw a
      temporary overlay using any CAD viewer that accepts geometry primitives.
    question: Is there a way to highlight found text in a viewer?
  - answer: The product uses a per‑developer or per‑server license model; a free evaluation
      license is available for 30 days.
    question: What licensing model applies to Aspose.CAD?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- CAD processing
- Aspose.CAD
- .NET
- DWG text search
title: 使用 C# 及 Aspose.CAD 在 DWG 檔案中搜尋文字
url: /zh-hant/net/text-search-and-manipulation/
weight: 28
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 C# 及 Aspose.CAD 在 DWG 檔案中搜尋文字

## 簡介

在本教學中，您將學習如何使用功能強大的 Aspose.CAD for .NET 函式庫，透過 C# **搜尋 DWG 文字**。無論您需要定位註解、提取屬性值，或建立可搜尋的索引，以下步驟將指引您完成一個可靠且高效能的解決方案，且可在 .NET Framework 與 .NET Core 上執行。

## 快速回答
- **哪個函式庫處理 DWG 文字搜尋？** Aspose.CAD for .NET.
- **我可以從 DWG 提取文字嗎？** 是 — API 會回傳任何找到的實體的純文字字串。
- **支援哪些 .NET 版本？** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.
- **開發時需要授權嗎？** 免費的暫時授權可用於評估；正式環境需購買完整授權。
- **此操作是否節省記憶體？** 是，Aspose.CAD 以串流方式處理檔案，允許處理多百頁的 DWG 而無需將整個檔案載入記憶體。

## 什麼是 DWG 文字搜尋？

CadImage 是 Aspose.CAD 的物件，代表已載入的 CAD 圖紙，並公開其實體（例如文字片段）。  
TextFragment 代表單一的已提取文字片段，包含其內容與幾何位置。

*搜尋 DWG 文字* 指的是以程式方式定位字串資料——例如圖層名稱、屬性值或註解文字——於 DWG 圖紙檔案中。Aspose.CAD 透過其 `CadImage` 物件與 `TextFragment` 集合提供此功能，讓開發者能有效地取得與操作文字。

## 為何使用 Aspose.CAD 來搜尋 DWG 文字？

Aspose.CAD 支援 **30+ CAD 與 BIM 格式**（包括 DWG、DXF、DGN、DWF），且可處理高達 **500 MB** 的檔案而無需完整載入記憶體。此函式庫在複雜圖紙上保證 **99 % 文字提取準確度**，相較於許多開源解析器常遺漏嵌入的 MTEXT 或區塊屬性，這是一項量化的改進。

## 如何使用 C# 在 DWG 檔案中搜尋文字？

Image.Load 是一個靜態方法，用於讀取 CAD 檔案並回傳 CadImage 實例。  

使用 `Image.Load` 載入 DWG，取得 `TextFragments` 集合，並依搜尋關鍵字以 LINQ 進行篩選。此簡潔模式的執行時間與文字實體數量呈線性關係，無需額外函式庫，且在 .NET Framework 與 .NET Core 環境中皆能一致運作。

### 步驟 1：安裝 Aspose.CAD NuGet 套件
開啟 NuGet 套件管理員主控台並執行：

```
Install-Package Aspose.CAD
```

### 步驟 2：開啟 DWG 檔案
透過呼叫 `Image.Load` 建立 `CadImage` 實例。此方法會自動偵測檔案格式，並建立記憶體中的表示。

### 步驟 3：列舉文字片段
`image.TextFragments` 會回傳 `TextFragment` 物件的集合，每個物件皆提供 `Text`、`Location`、`Height` 與 `LayerName`。您可以遍歷或以 LINQ 篩選此集合。

### 步驟 4：套用搜尋條件
使用 `String.Contains`、`Regex.IsMatch` 或任何自訂謂詞來定位您需要的精確文字。若要執行不區分大小寫的搜尋，請對雙方皆呼叫 `ToLowerInvariant()`。

### 步驟 5：處理結果
常見的操作包括記錄片段座標、匯出為 CSV，或在檢視器中突顯該實體。由於 API 提供了精確的 `Location`，您可將其傳入任何後續的 CAD 可視化元件。

## 如何從 DWG 提取文字？

TextFragment 是保存已提取文字及其相關中繼資料（如位置與圖層）的物件。  

提取文字的方式與搜尋相同；只需列舉 `TextFragment` 集合並讀取每個 `TextFragment.Text` 屬性。您可以將字串串接成單一文件、寫入 CSV 檔，或輸入搜尋索引，以便在多個圖紙間快速檢索。

## 常見陷阱與疑難排解
- **缺少 MTEXT：** 某些較舊的 DWG 版本將多行文字存於區塊屬性中。請確保同時檢查 `image.Blocks` 中的 `Attribute` 物件。  
- **編碼問題：** DWG 檔案可能使用非 Unicode 代碼頁。載入前請將 `image.LoadOptions.Encoding` 設為相應的 `System.Text.Encoding`。  
- **大型檔案：** 若檔案大於 200 MB，請啟用 `image.LoadOptions.Streaming = true`，以將記憶體使用量控制在 100 MB 以下。

## 常見問答

**Q: 我可以在受密碼保護的 DWG 檔案中搜尋文字嗎？**  
A: 可以。呼叫 `Image.Load` 時，透過 `CadLoadOptions.Password` 提供密碼。

**Q: API 是否支援一次搜尋多個 DWG 檔案？**  
A: 當然支援。遍歷目錄、載入每個檔案，並重複使用相同的 LINQ 篩選——此函式庫具備執行緒安全性，可進行平行處理。

**Q: 複雜註解的文字提取準確度如何？**  
A: Aspose.CAD 在業界標準測試集上報告 **99 % 成功率**，能處理 MTEXT、屬性定義，甚至嵌入的 Unicode 字元。

**Q: 有沒有方法在檢視器中突顯找到的文字？**  
A: 取得每個 `TextFragment` 的 `Location` 後，您可使用任何接受幾何基元的 CAD 檢視器繪製暫時的覆蓋層。

**Q: Aspose.CAD 採用什麼授權模式？**  
A: 本產品採用每位開發人員或每台伺服器授權模式；提供 30 天的免費評估授權。

---

**最後更新：** 2026-10-04  
**測試環境：** Aspose.CAD 24.11 for .NET  
**作者：** Aspose  

## 文字搜尋與操作教學
### [使用 C# 搜尋 DWG 檔案文字 - Aspose.CAD 教學](./searching-text-in-dwg-files/)

```csharp
using Aspose.CAD;
using Aspose.CAD.ImageOptions;

// Load the DWG file
using var image = (CadImage)Image.Load("sample.dwg");

// Retrieve all text fragments
var fragments = image.TextFragments;

// Filter fragments that contain the target string
var matches = fragments.Where(t => t.Text.Contains("TargetString"));
```

## 相關教學

- [將 DWG 轉換為 PDF 並在 C# 中加入文字 – Aspose.CAD 教學](/cad/net/dwg-file-manipulation/adding-text-to-dwg/)
- [如何使用 Aspose.CAD for .NET 將 DWG 轉換為 PDF 與點陣圖像](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)
- [如何渲染 CAD 並轉換 DWG – Aspose.CAD .NET](/cad/net/conversion-and-export/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}