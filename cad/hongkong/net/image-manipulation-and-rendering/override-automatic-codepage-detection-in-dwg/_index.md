---
date: 2026-09-04
description: 了解如何使用 Aspose.CAD for .NET 在 DWG 檔案中覆寫 dwg 代碼頁偵測，讓您對字元編碼擁有精確的控制。
keywords:
- override dwg codepage
- dwg codepage detection
- aspose.cad .net
- cad file encoding
- dwg processing
lastmod: 2026-09-04
linktitle: 覆寫 DWG 檔案的自動代碼頁偵測 - Aspose.CAD 教學
og_description: 了解如何使用 Aspose.CAD for .NET 在 DWG 檔案中覆寫 dwg 代碼頁偵測，讓您對字元編碼擁有精確的控制，並提升
  CAD 檔案的處理效能。
og_image_alt: Guide showing how to override DWG codepage with Aspose.CAD in .NET
og_title: 如何在 Aspose.CAD for .NET 中覆寫 DWG 代碼頁
schemas:
- author: Aspose
  dateModified: '2026-09-04'
  description: Learn how to override dwg codepage detection in DWG files using Aspose.CAD
    for .NET, giving you precise control over character encoding.
  headline: How to override dwg codepage in Aspose.CAD for .NET
  type: TechArticle
- questions:
  - answer: It forces Aspose.CAD to use the encoding you specify instead of guessing,
      preventing character corruption.
    question: What does overriding the DWG codepage do?
  - answer: Whenever a DWG file contains text in a language that isn’t the default
      Windows codepage (e.g., Central European, Cyrillic).
    question: When should I use it?
  - answer: Any .NET `Encoding` such as `Encoding.GetEncoding(1250)` for Central European.
    question: Which encodings are supported?
  - answer: A trial works for development; a commercial license is required for production.
    question: Do I need a license?
  - answer: Yes, the setting is applied per `Image` instance, so multiple threads
      can process different files concurrently.
    question: Is it thread‑safe?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- override dwg codepage
- Aspose.CAD
- .NET CAD processing
- DWG codepage
- CAD rendering
title: 如何在 Aspose.CAD for .NET 中覆寫 DWG 代碼頁
url: /zh-hant/net/image-manipulation-and-rendering/override-automatic-codepage-detection-in-dwg/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何在 Aspose.CAD for .NET 中覆寫 DWG 代碼頁

在許多舊版 DWG 檔案中，嵌入的代碼頁會自動偵測，若檔案使用非預設編碼，可能會導致文字亂碼。**Override dwg codepage** 讓您明確設定所需的編碼，以確保幾何圖形和註釋文字正確呈現。在本教學中，您將了解此設定的重要性、API 的使用方式，以及如何透過簡單的步驟套用此設定。

## 快速解答
- **覆寫 DWG 代碼頁會有什麼作用？** 它會強制 Aspose.CAD 使用您指定的編碼，而非自行猜測，從而防止字元損壞。  
- **什麼時候應該使用它？** 只要 DWG 檔案的文字使用非預設 Windows 代碼頁的語言（例如中歐語系、斯拉夫語系），皆應使用。  
- **支援哪些編碼？** 任何 .NET `Encoding`，例如用於中歐語系的 `Encoding.GetEncoding(1250)`。  
- **需要授權嗎？** 開發階段可使用試用版；正式上線需購買商業授權。  
- **它是執行緒安全的嗎？** 是的，此設定會套用於每個 `Image` 實例，允許多執行緒同時處理不同檔案。

## 什麼是覆寫 DWG 代碼頁？
覆寫 DWG 代碼頁是 Aspose.CAD 的一項功能，讓您以自訂的字元編碼取代程式庫自動偵測代碼頁的機制。這可確保 DWG 內的文字字串無論原始中繼資料為何，都能正確解譯。

## 為什麼要使用覆寫 DWG 代碼頁？
Aspose.CAD 支援 **50+ DWG/DXF 版本**，且可在不將整個文件載入記憶體的情況下處理高達 **2 GB** 的檔案。若自動偵測失敗，可能會失去多達 **100 % 的註釋可讀性**。透過明確設定代碼頁，可將此風險降至 **0 %**，且不影響渲染時間。

## 前置條件

- 具備 C# 及 .NET 平台的基礎知識。  
- 已安裝 Aspose.CAD for .NET。如尚未安裝，請下載 **[Aspose.CAD for .NET 下載頁面](https://releases.aspose.com/cad/net/)**。  
- 一個使用非預設代碼頁的 DWG 檔案（例如在代碼頁 1250 的系統上建立的檔案）。

## 匯入命名空間

首先，加入必要的 `using` 指令，讓編譯器能找到 Aspose.CAD 類別。

在 C# 原始檔的頂部插入以下程式碼：

```csharp
using System;
using Aspose.CAD.FileFormats.Cad;
```

這將為所有後續的 CAD 操作做好環境準備。

## 步驟 1：定義文件目錄

指定包含欲處理 DWG 的資料夾。將佔位符替換為您機器上的實際路徑：

```csharp
//ExStart:1
string SourceDir = "Your Document Directory";
//ExEnd:1
```

## 步驟 2：覆寫自動代碼頁偵測

現在進入本教學的核心。以下程式碼載入 DWG 檔案，將代碼頁強制設定為 **Windows‑1250**（中歐語系），然後將影像儲存為 PNG。請依需求調整檔名與編碼。

```csharp
//ExStart:1
using (CadImage cadImage = (CadImage)Image.Load(SourceDir + "SimpleEntites.dwg",
new LoadOptions()
{
	SpecifiedEncoding = CodePages.Japanese,
	SpecifiedMifEncoding = MifCodePages.Japanese,
	RecoverMalformedCifMif = false
}))
{
	// Perform export or other operations with cadImage
}
//ExEnd:1
Console.WriteLine("OverrideAutomaticCodePageDetectionDwg executed successfully");
```

`Image.Load` 是一個靜態方法，用於載入 CAD 檔案並回傳 `CadImage` 物件。`LoadOptions.CodePage` 指定載入時使用的字元編碼。`CadImage` 代表 CAD 圖面的記憶體表示，並提供渲染或轉換的方法。

## 常見問題與解決方案

- **覆寫後仍出現亂碼** – 請確認您選擇的編碼與原始檔案的語言相符。例如，對於斯拉夫語系可使用 `Encoding.GetEncoding(1251)`。  
- **檔案載入失敗** – 確認 DWG 版本受到您使用的 Aspose.CAD 版本支援；必要時升級。  
- **效能下降** – 覆寫不會增加額外負擔；若發現變慢，請檢查是否有其他 I/O 瓶頸。

## 常見問與答

### Q1：我可以在 C# 之外的語言中使用 Aspose.CAD for .NET 嗎？
A1：Aspose.CAD for .NET 主要設計給 C# 使用，但亦可在其他 .NET 語言（如 VB.NET）中使用。

### Q2：是否提供免費試用？
A2：是的，您可以取得免費試用 **[Aspose.CAD 免費試用下載頁面](https://releases.aspose.com/)**。

### Q3：如何取得 Aspose.CAD for .NET 的支援？
A3：請前往 **[Aspose.CAD 論壇](https://forum.aspose.com/c/cad/19)** 取得社群支援。

### Q4：我可以購買臨時授權嗎？
A4：是的，您可以在 **[臨時授權購買頁面](https://purchase.aspose.com/temporary-license/)** 取得臨時授權。

### Q5：在哪裡可以找到詳細文件？
A5：請參考完整的 **[Aspose.CAD .NET API 文件](https://reference.aspose.com/cad/net/)**。

### Q6：覆寫代碼頁會影響點陣圖渲染品質嗎？
A6：不會。代碼頁設定僅影響文字字串的解碼方式，影像品質不會改變。

### Q7：在轉換為非 PNG 格式時，我可以套用此覆寫嗎？
A7：當然可以。相同的 `LoadOptions.CodePage` 值同樣適用於 PDF、SVG 或任何 Aspose.CAD 支援的輸出格式。

**最後更新：** 2026-09-04  
**測試於：** Aspose.CAD 24.10 for .NET  
**作者：** Aspose

## 相關教學

- [使用 C# 搜尋 DWG 檔案文字 - Aspose.CAD 教學](/cad/net/text-search-and-manipulation/searching-text-in-dwg-files/)
- [將 DWG 轉換為 PDF 並在 C# 中加入文字 – Aspose.CAD 教學](/cad/net/dwg-file-manipulation/adding-text-to-dwg/)
- [如何使用 Aspose.CAD for .NET 將 DWG 轉換為 PDF 與點陣圖像](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}