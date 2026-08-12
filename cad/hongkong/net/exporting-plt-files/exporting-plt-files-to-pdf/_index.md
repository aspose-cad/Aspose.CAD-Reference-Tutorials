---
date: 2026-08-12
description: 了解如何使用 Aspose.CAD for .NET 將 PLT 轉換為 PDF – 這是一種快速將 CAD 另存為 PDF 並完整支援格式的方法。
keywords:
- convert plt to pdf
- save cad as pdf
- cad file to pdf
- export plt as pdf
- cad plt to pdf
lastmod: 2026-08-12
linktitle: 將 PLT 檔案匯出為 PDF
og_description: 了解如何使用 Aspose.CAD for .NET 將 PLT 轉換為 PDF – 這是一種快速將 CAD 另存為 PDF 並完整支援格式的方法。
og_image_alt: Guide showing how to convert PLT files to PDF using Aspose.CAD for .NET
og_title: 使用 Aspose.CAD for .NET 將 PLT 轉換為 PDF – 教學
schemas:
- author: Aspose
  dateModified: '2026-08-12'
  description: Learn how to convert PLT to PDF using Aspose.CAD for .NET – a fast
    way to save CAD as PDF with full format support.
  headline: Convert PLT to PDF with Aspose.CAD for .NET – tutorial
  type: TechArticle
- questions:
  - answer: '`CadImage` loads and rasterizes PLT files.'
    question: What is the primary class?
  - answer: Only two lines are needed for the actual conversion.
    question: How many lines of code?
  - answer: A free trial works for development; a commercial license is required for
      production.
    question: Do I need a license?
  - answer: .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.
    question: Supported .NET versions?
  - answer: Yes—loop through files and reuse the same rasterization options.
    question: Can I batch convert?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- convert plt
- Aspose.CAD
- .NET CAD conversion
title: 使用 Aspose.CAD for .NET 將 PLT 轉換為 PDF – 教學
url: /zh-hant/net/exporting-plt-files/exporting-plt-files-to-pdf/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.CAD for .NET 將 PLT 轉換為 PDF – 教學

在本教學中，您將學習如何使用 Aspose.CAD .NET 程式庫 **將 PLT 轉換為 PDF**。無論是建立桌面工具還是伺服器端服務，以下步驟將帶您完成載入 PLT 圖紙、設定光柵化，並將結果儲存為 PDF 檔案的全過程，並提供清晰說明與最佳實踐建議。

## 快速解答
- **主要類別是什麼？** `CadImage` 會載入並光柵化 PLT 檔案。  
- **需要多少行程式碼？** 實際轉換只需兩行程式碼。  
- **需要授權嗎？** 免費試用版可用於開發；正式環境需購買商業授權。  
- **支援的 .NET 版本？** .NET Framework 4.5+、.NET Core 3.1+、.NET 5/6+。  
- **可以批次轉換嗎？** 可以——迴圈處理檔案並重複使用相同的光柵化選項。

## 什麼是將 PLT 轉換為 PDF？
「將 PLT 轉換為 PDF」指的是將基於 HPGL 的繪圖檔案（PLT）轉換成可在任何裝置上檢視的可攜式文件格式（PDF）的過程。Aspose.CAD 提供單一呼叫 API，無需外部 CAD 軟體即可完成此轉換。

## 為什麼使用 Aspose.CAD 進行此轉換？
Aspose.CAD 支援 **30+** 種 CAD 與 BIM 格式，且可在不將整個文件載入記憶體的情況下匯出高達 **2 GB** 的檔案，為企業工作負載提供高效能的批次處理能力。

## 前置條件

在深入教學之前，請確保已具備以下前置條件：

1. Aspose.CAD for .NET Library：確保已安裝 Aspose.CAD 程式庫。您可以在此處下載 Aspose.CAD for .NET 程式庫 [here](https://releases.aspose.com/cad/net/)。
2. Development Environment：具備可運作的 .NET 開發環境。

## 匯入命名空間

在您的 .NET 專案中，首先匯入必要的命名空間：

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

這些命名空間將提供處理 CAD 操作所需的關鍵類別與功能。

## 如何使用 Aspose.CAD 轉換 PLT 為 PDF？

`CadImage` 類別代表一個 CAD 圖紙，並提供載入與儲存影像的方法。使用 `CadImage.Load("input.plt")` 載入 PLT 檔案，然後呼叫 `image.Save("output.pdf", pdfOptions)`——此單一呼叫即可完成完整轉換，同時保留向量精度與光柵品質。對於大型圖紙，請在儲存前調整 `RasterizationOptions` 以控制 DPI 與頁面大小。

## 步驟 1：設定文件目錄

在程式碼中定義文件目錄的路徑：

```csharp
string MyDir = "Your Document Directory";
```

將「Your Document Directory」替換為實際的文件路徑。

## 步驟 2：載入 PLT 檔案

使用以下程式碼片段將 PLT 檔案載入 CAD 影像：

```csharp
string sourceFilePath = MyDir + "50states.plt";

using (Image cadImage = Image.Load(sourceFilePath))
{
    // Your code goes here
}
```

**Definition anchor:** `CadImage` 類別代表一個 CAD 圖紙，並提供光柵化功能。

## 步驟 3：設定光柵化選項

`CadRasterizationOptions` 定義 CAD 圖紙的光柵化方式，包括頁面大小、DPI 與背景顏色。

```csharp
CadRasterizationOptions options = new CadRasterizationOptions
{
    PageHeight = 1600,
    PageWidth = 1600,
    DrawType = CadDrawTypeMode.UseObjectColor,
    BackgroundColor = Color.White
};
```

## 步驟 4：設定 PDF 選項

`PdfOptions` 指定 PDF 輸出設定，並連結到光柵化選項以完成轉換。

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = options;
```

## 步驟 5：儲存為 PDF

將 CAD 影像儲存為 PDF 檔案：

```csharp
cadImage.Save(MyDir + "50states.pdf", pdfOptions);
```

## 常見問題與故障排除技巧

- **File not found error:** 請確認傳遞給 `CadImage.Load` 的路徑指向現有的 PLT 檔案，且應用程式具備讀取權限。  
- **Blank pages in PDF:** 確保 `RasterizationOptions.PageWidth` 與 `PageHeight` 與來源圖紙的長寬比相符，或將 `LayoutOptions` 設為 `LayoutOptions.AutoFit`。  
- **Memory consumption on large files:** 使用 `image.Save` 搭配參考共享 `RasterizationOptions` 實例的 `PdfOptions`，可避免多次將整個影像載入記憶體。

## 常見問答

### Q1：我可以在 Web 應用程式中使用 Aspose.CAD for .NET 嗎？
A: 可以，Aspose.CAD for .NET 相容於桌面與 Web 應用程式，包括 ASP.NET Core 與 MVC 專案。

### Q2：是否提供 Aspose.CAD for .NET 的免費試用？
A: 當然，您可以在此處探索 Aspose 免費試用頁面 [here](https://releases.aspose.com/)。

### Q3：如何取得 Aspose.CAD for .NET 的支援？
A: 前往 [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) 取得社群支援與指導。

### Q4：Aspose.CAD 支援哪些檔案格式？
A: Aspose.CAD 支援多種 CAD 格式，包括 DWG、DXF 與 PLT。

### Q5：在哪裡可以找到 Aspose.CAD for .NET 的詳細文件？
A: 請參考 [Aspose.CAD documentation](https://reference.aspose.com/cad/net/) 以取得深入資訊。

### Q6：我可以一次批次轉換多個 PLT 檔案為 PDF 嗎？
A: 可以——遍歷 PLT 檔案目錄，重複使用相同的 `RasterizationOptions`，並對每個影像呼叫 `Save`。

### Q7：轉換為 PDF 時，程式庫會保留向量資料嗎？
A: 轉換會將圖紙光柵化，但您可以透過設定 `PdfOptions.VectorRasterization = true` 來啟用 PDF 向量輸出。

---

**最後更新：** 2026-08-12  
**測試環境：** Aspose.CAD 24.11 for .NET  
**作者：** Aspose

## 相關教學

- [匯出 PLT 檔案為影像 - Aspose.CAD 教學](/cad/net/exporting-plt-files/exporting-plt-files-to-image/)
- [Aspose.CAD 中的 PLT 格式支援 - 完整教學](/cad/net/plt-and-watermarking/plt-format-support-in-aspose-cad/)
- [匯出 DXF 為 PDF 格式 - Aspose.CAD 教學](/cad/net/export-techniques/exporting-dxf-to-pdf-format/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}