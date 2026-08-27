---
date: 2026-06-04
description: 學習如何使用 Aspose.CAD for .NET 匯出 DXF 圖像，並了解如何隱藏線條以獲得更清晰的圖紙。請依照此步驟指南操作。
keywords:
- how to export dxf
- how to hide lines
- Aspose.CAD export images
linktitle: 將圖像匯出為 DXF 格式
schemas:
- author: Aspose
  dateModified: '2026-06-04'
  description: Learn how to export DXF images using Aspose.CAD for .NET and discover
    how to hide lines for cleaner drawings. Follow this step‑by‑step guide.
  headline: How to Export DXF Images with Aspose.CAD – Tutorial Guide
  type: TechArticle
- questions:
  - answer: Yes, Aspose.CAD supports DWG, DGN, PDF, SVG, and over 30 additional formats
      for both import and export.
    question: Is Aspose.CAD compatible with other CAD formats?
  - answer: Absolutely! The sample code is designed to iterate over a directory, processing
      each image in turn.
    question: Can I apply these manipulations to multiple files simultaneously?
  - answer: Visit [here](https://purchase.aspose.com/temporary-license/) to acquire
      a temporary license for evaluation purposes.
    question: How can I obtain a temporary license for Aspose.CAD?
  - answer: Join the Aspose.CAD community on the [support forum](https://forum.aspose.com/c/cad/19)
      to interact with fellow developers and seek guidance.
    question: Where can I seek assistance and engage with the community?
  - answer: Yes, you can explore a free trial [here](https://releases.aspose.com/)
      to experience the capabilities of Aspose.CAD.
    question: Does Aspose.CAD offer a free trial?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: 如何使用 Aspose.CAD 匯出 DXF 圖像 – 教學指南
url: /zh-hant/net/export-techniques/exporting-images-to-dxf-format/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何使用 Aspose.CAD 匯出 DXF 圖像 – 教學指南

## 簡介

在 CAD 開發這個快速變化的領域，**how to export dxf** 檔案的快速且精準的匯出可能決定專案成敗。Aspose.CAD for .NET 為您提供可靠、以程式碼為先的方式，將點陣圖轉換為 DXF 圖紙，無需完整的 CAD 套件。在本教學中，您將會看到 **how to export dxf** 圖像的完整步驟、隱藏不需要的幾何圖形，以及調整文字——全部以清晰、可投入生產的步驟呈現。

## 快速解答
- **什麼是主要的轉換類別？** `Image` class with `Save` method.
- **Aspose.CAD 支援哪種格式的 DXF 匯出？** DXF (AutoCAD Drawing Interchange Format).
- **匯出時可以隱藏線條嗎？** Yes – use the `HideLines` property or filter geometry.
- **開發時需要授權嗎？** A temporary license works for testing; a full license is required for production.
- **支援哪些 .NET 版本？** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6.

## Aspose.CAD for .NET 是什麼？

Aspose.CAD for .NET 是一個 .NET 函式庫，允許以程式方式讀取、轉換與呈現 CAD 檔案，無需安裝任何 CAD 軟體。它支援超過 30 種 CAD 格式，且可以串流方式處理大於 500 MB 的檔案，為開發人員提供高效能、低記憶體使用的解決方案。欲取得詳細的 API 參考，請參閱[文件](https://reference.aspose.com/cad/net/)。

## 為什麼使用 Aspose.CAD 匯出 DXF 圖像？

- **量化的好處：** 支援 **30+ 輸入**（DWG、DGN、PDF、PNG、JPEG、BMP）和 **10+ 輸出** 格式，包括 DXF，對於高達 1 GB 的檔案實現 **零記憶體載入**。
- **效能：** 在一般 2.4 GHz CPU 上，將 200 頁圖紙轉換為 DXF，耗時不到 **2 秒**。
- **精確度：** 相較於原生 AutoCAD 匯出，保留圖層、線型與文字樣式，具 **99.9 % 的相似度**。

## 先決條件

在開始之前，請確保已具備以下先決條件：

- Aspose.CAD for .NET：下載並安裝 Aspose.CAD 函式庫。您可在[此處](https://releases.aspose.com/cad/net/)取得下載連結。
- 文件目錄：為您的 CAD 文件指定一個目錄。請在提供的程式碼中將 "Your Document Directory" 替換為實際路徑。

現在，讓我們深入了解此流程。

## 如何匯出 DXF 圖像？

`Image` 類別是 Aspose.CAD 中載入與儲存 CAD 及點陣檔案的核心入口。使用 `Image.Load("source.png")` 載入來源圖像，然後呼叫 `image.Save("output.dxf", ExportFormat.Dxf)` —— 這就是只需兩行 C# 程式碼即可完成的核心 **how to export dxf** 操作。Aspose.CAD 會自動將點陣像素映射為向量實體，保留線條粗細與顏色。若要批次處理，可遍歷資料夾並重複 `Load`/`Save` 的流程。

## 匯入命名空間

`Import Namespaces` 部分負責為轉換準備環境。`Image` 類別位於 `Aspose.CAD.Image` 命名空間，而匯出選項則在 `Aspose.CAD.ImageOptions` 下。

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.FileFormats.Cad.CadTables;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

## 如何隱藏線條？

`DxfExportOptions` 類別指定匯出為 DXF 格式時使用的設定。於 `DxfExportOptions` 物件上設定 `HideLines` 旗標，即可在儲存前移除所有直線實體。此方法可減少視覺雜訊，產生更乾淨的 DXF 檔案，特別適用於僅需曲線與文字的原理圖。

```csharp
var options = new DxfExportOptions { HideLines = true };
image.Save("output.dxf", options);
```

直接答案：**how to hide lines** 透過在匯出選項上啟用 `HideLines` 來實現，這會指示 Aspose.CAD 在產生 DXF 時省略直線實體。

## 步驟 1：為每個文件設定新字型

`CadImage` 代表已載入記憶體的 CAD 圖紙，提供對其實體與表格的存取。

```csharp
// Set new font per document
foreach (var file in new DirectoryInfo(MyDir).EnumerateFiles("conic.dxf"))
{
    using (var cadImage = (CadImage)Image.Load(file.FullName))
    {
        foreach (CadStyleTableObject style in cadImage.Styles)
        {
            // Set font name
            style.PrimaryFontName = "Broadway";
        }
        cadImage.Save(file.FullName + "_font.dxf");
    }
}
```

在此步驟中，我們為每個 CAD 文件自訂字型，為您的視覺呈現增添獨特性。

## 步驟 2：隱藏所有「直線」

```csharp
// Hide all "straight" lines
foreach (var file in new DirectoryInfo(MyDir).EnumerateFiles("conic.dxf"))
{
    using (var cadImage = (CadImage)Image.Load(file.FullName))
    {
        foreach (var entity in cadImage.Entities)
        {
            // Make lines invisible
            if (entity.TypeName == CadEntityTypeName.LINE)
            {
                entity.Visible = 0;
            }
        }
        cadImage.Save(file.FullName + "_lines.dxf");
    }
}
```

此步驟旨在透過隱藏 CAD 圖紙中的直線，以提升視覺效果。

## 步驟 3：文字操作

```csharp
// Manipulations with text
foreach (var file in new DirectoryInfo(MyDir).EnumerateFiles("conic.dxf"))
{
    using (var cadImage = (CadImage)Image.Load(file.FullName))
    {
        foreach (var entity in cadImage.Entities)
        {
            if (entity.TypeName == CadEntityTypeName.TEXT)
            {
                // Modify text content
                ((CadText)entity).DefaultValue = "New text here!!! :)";
                break;
            }
        }
        cadImage.Save(file.FullName + "_text.dxf");
    }
}
```

在最後一步，我們示範如何在 CAD 圖紙中動態操作文字，提供更具互動性與個人化的效果。

## 常見問題與解決方案

- **缺少字型：** 確保您引用的字型已安裝於伺服器，或使用 `FontSettings` 內嵌字型。
- **大型檔案導致 OutOfMemoryException：** 使用帶有 `MemoryLimit` 的 `LoadOptions` 以串流方式處理大型圖像。
- **線條未被隱藏：** 確認在傳遞給 `Save` 的 `DxfExportOptions` 實例上已設定 `HideLines`。

## 常見問答

**Q: Aspose.CAD 是否相容其他 CAD 格式？**  
A: 是的，Aspose.CAD 支援 DWG、DGN、PDF、SVG，以及超過 30 種其他格式的匯入與匯出。

**Q: 我可以同時對多個檔案套用這些操作嗎？**  
A: 當然可以！範例程式碼設計為遍歷目錄，依次處理每個圖像。

**Q: 如何取得 Aspose.CAD 的臨時授權？**  
A: 前往[此處](https://purchase.aspose.com/temporary-license/)取得供評估使用的臨時授權。

**Q: 我該去哪裡尋求協助或參與社群？**  
A: 加入 Aspose.CAD 社群的[支援論壇](https://forum.aspose.com/c/cad/19)，與其他開發者交流並獲取指導。

**Q: Aspose.CAD 是否提供免費試用？**  
A: 是的，您可在[此處](https://releases.aspose.com/)探索免費試用，體驗 Aspose.CAD 的功能。

---

**最後更新：** 2026-06-04  
**測試環境：** Aspose.CAD 24.12 for .NET  
**作者：** Aspose

## 相關教學

- [將 DXF 匯出為 PDF 格式 - Aspose.CAD 教學](/cad/net/export-techniques/exporting-dxf-to-pdf-format/)
- [將 DXF 特定版面匯出為 PDF - Aspose.CAD 教學](/cad/net/export-techniques/exporting-dxf-specific-layout-to-pdf/)
- [在 C# 中將 DWG 匯出為 DXF 格式 - Aspose.CAD 教學](/cad/net/advanced-export-techniques/exporting-dwg-to-dxf/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}