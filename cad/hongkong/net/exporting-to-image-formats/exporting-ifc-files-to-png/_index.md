---
date: 2026-07-18
description: 使用 Aspose.CAD for .NET 將 CAD 匯出為 PNG 的方法。快速且可靠地將 IFC 檔案轉換為高品質 PNG 圖像。
keywords:
- how to export cad to png
- Aspose.CAD IFC conversion
- CAD to PNG .NET
lastmod: 2026-07-18
linktitle: 匯出 IFC 檔案為 PNG
og_description: 使用 Aspose.CAD for .NET 將 CAD 匯出為 PNG 的方法。了解無需編碼設定的逐步 IFC 檔案轉換為 PNG
  圖像流程。
og_image_alt: Guide showing IFC to PNG conversion with Aspose.CAD for .NET
og_title: 如何將 CAD 匯出為 PNG – Aspose.CAD .NET 指南
schemas:
- author: Aspose
  dateModified: '2026-07-18'
  description: How to export CAD to PNG using Aspose.CAD for .NET. Convert IFC files
    to high‑quality PNG images quickly and reliably.
  headline: How to Export CAD to PNG – Exporting IFC Files with Aspose.CAD
  type: TechArticle
- questions:
  - answer: No, Aspose.CAD for .NET is specifically designed for Windows environments.
    question: Can I use Aspose.CAD for .NET on macOS or Linux?
  - answer: Yes, you can obtain a temporary license from [here](https://purchase.aspose.com/temporary-license/)
      for evaluation.
    question: Is a temporary license available for testing purposes?
  - answer: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for community
      support and discussions.
    question: How can I get support for Aspose.CAD?
  - answer: Refer to the [Aspose.CAD documentation](https://reference.aspose.com/cad/net/)
      for detailed information and examples.
    question: Where can I find comprehensive documentation?
  - answer: Check the documentation or seek assistance on the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19).
    question: What if I encounter issues during installation?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- export cad
- Aspose.CAD
- IFC to PNG
- .NET image conversion
title: 如何將 CAD 匯出為 PNG – 使用 Aspose.CAD 匯出 IFC 檔案
url: /zh-hant/net/exporting-to-image-formats/exporting-ifc-files-to-png/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何將 CAD 匯出為 PNG – 使用 Aspose.CAD 匯出 IFC 檔案

## 簡介

如果您需要 **how to export cad to png**，Aspose.CAD for .NET 提供可靠、免編碼的方式，將 IFC（Industry Foundation Classes）模型轉換為清晰的 PNG 點陣圖像。在本教學中，我們將逐步說明完整工作流程——從安裝函式庫到儲存最終 PNG——讓您能自信地將轉換整合到任何 .NET 應用程式中。

## 快速答案
- **什麼函式庫負責轉換？** Aspose.CAD for .NET.
- **支援的來源格式？** IFC (Industry Foundation Classes) files.
- **目標影像格式？** PNG, with full control over size and resolution.
- **最低 .NET 版本？** .NET Framework 4.5+ or .NET Core 3.1+.
- **授權需求？** A valid Aspose.CAD license for production use.

## 什麼是「how to export cad to png」？

此詞語指的是將基於 CAD 的檔案格式（如 IFC）轉換為可攜式網路圖形（PNG）點陣圖像的過程。此轉換可讓 CAD 視覺內容在網頁、文件或報告中輕鬆檢視、分享與嵌入，提供一種輕量且廣受支援的格式，能在不需要專業 CAD 檢視器的情況下保留視覺真實度。

## 為什麼要使用 Aspose.CAD 進行此轉換？

Aspose.CAD 支援 **50+ CAD and BIM formats**，且能在不將整個檔案載入記憶體的情況下處理多百頁的 IFC 模型。它在標準伺服器硬體上提供快速且記憶體效率高的轉換，會自動處理圖層、線寬與顏色映射，同時提供廣泛的設定選項以調整輸出品質與大小。

## 先決條件

### 1. Aspose.CAD 安裝
確保您已安裝 Aspose.CAD for .NET。您可以從發行頁面 [here](https://releases.aspose.com/cad/net/) 下載。

### 2. 文件目錄
建立一個指定的目錄來存放您的文件。在提供的範例中，變數 `MyDir` 代表文件目錄。

## 匯入命名空間
現在先決條件已備妥，請在您的 .NET 專案中匯入使用 Aspose.CAD 所需的命名空間。

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using Aspose.CAD.FileFormats.Ifc;
```

## 如何將 CAD 匯出為 PNG？

`IfcImage` 代表一個可被光柵化為 PNG 等點陣格式的 IFC CAD 影像。使用 `new IfcImage("source.ifc")` 載入您的 IFC 檔案，透過 `RasterizationOptions` 設定光柵化參數，使用 `PngOptions` 設定 PNG 專屬選項，最後呼叫 `Save(outputPath, pngOptions)`。此端對端流程僅需幾行程式碼即可將 CAD 模型轉換為高解析度 PNG，並自動處理圖層、顏色與線寬。

## 步驟 1：載入 IFC 檔案
`IfcImage` 類別載入 IFC 模型並為光柵化做準備。

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "example.ifc";
using (IfcImage cadImage = (IfcImage)Image.Load(sourceFilePath))
{
```

在此步驟中，我們初始化 Aspose.CAD 的 `IfcImage` 物件並將 IFC 檔案載入其中。

## 步驟 2：設定光柵化選項
`RasterizationOptions` 類別定義向量資料如何轉換為點陣圖像，包括頁面寬度、高度與背景顏色。

```csharp
    CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
   
    rasterizationOptions.PageWidth = 100;
    rasterizationOptions.PageHeight = 100;
```

定義光柵化選項以設定 PNG 輸出的頁面寬度與高度。

## 步驟 3：設定 PNG 選項
`PngOptions` 類別保存 PNG 輸出的特定設定，例如壓縮等級與色彩深度。

```csharp
    PngOptions pngOptions = new PngOptions();
    pngOptions.VectorRasterizationOptions = rasterizationOptions;
```

建立 PNG 選項並關聯先前定義的光柵化選項。

## 步驟 4：指定輸出路徑
輸出路徑決定產生的 PNG 檔案將儲存於何處。

```csharp
    // Set output path as well
    string outPath = sourceFilePath + ".png";
    cadImage.Save(outPath, pngOptions);
}
```

為 PNG 檔案定義輸出路徑，確保其名稱與來源檔案相同且附加「.png」副檔名。最後，儲存轉換後的影像。

## 常見問題與解決方案
- **缺少字型或線條樣式：** 確保來源 IFC 參考了所有必需的資源；Aspose.CAD 在可能的情況下會嵌入缺失的資產。
- **大型檔案導致記憶體激增：** 使用 `RasterizationOptions` 的 `MemoryLimit` 屬性來限制記憶體使用量。
- **顏色不正確：** 核對來源 IFC 的顏色定義是否符合 IFC 規範；Aspose.CAD 會遵循標準的顏色映射。

## 常見問答

**Q: 我可以在 macOS 或 Linux 上使用 Aspose.CAD for .NET 嗎？**  
A: 不行，Aspose.CAD for .NET 專為 Windows 環境設計。

**Q: 是否提供臨時授權供測試使用？**  
A: 是的，您可從 [here](https://purchase.aspose.com/temporary-license/) 取得臨時授權以供評估。

**Q: 如何取得 Aspose.CAD 的支援？**  
A: 請造訪 [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) 以獲得社群支援與討論。

**Q: 哪裡可以找到完整的文件說明？**  
A: 請參考 [Aspose.CAD documentation](https://reference.aspose.com/cad/net/) 以取得詳細資訊與範例。

**Q: 若在安裝過程中遇到問題該怎麼辦？**  
A: 請檢查文件或在 [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) 尋求協助。

---

**最後更新：** 2026-07-18  
**測試版本：** Aspose.CAD 24.11 for .NET  
**作者：** Aspose

## 相關教學

- [在 Aspose.CAD for .NET 中將 CAD 繪圖轉換為點陣圖像](/cad/net/cad-drawing-manipulation/convert-cad-drawing-to-raster-image/)
- [使用 Aspose.CAD for .NET 輕鬆將 STL 轉換為 PNG](/cad/net/stl-file-export/exporting-stl-files-to-png/)
- [在 Aspose.CAD for .NET 中將 CAD 版面匯出為點陣圖格式](/cad/net/cad-export-formats/export-cad-layouts-to-raster-image-formats/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}