---
date: 2026-08-12
description: 使用 Aspose.CAD for .NET 從 DWG 中擷取文字並在 C# 中將特定 DWG 轉換為圖像。透過程式碼範例一步步學習。
keywords:
- extract text from dwg
- convert specific dwg to image
- Aspose.CAD .NET
lastmod: 2026-08-12
linktitle: 在 C# 中將特定 DWG 轉換為圖像
og_description: 使用 Aspose.CAD 在 C# 中從 DWG 擷取文字並將特定 DWG 轉換為圖像。遵循此簡明指南即可快速實作。
og_image_alt: Guide showing DWG to image conversion and text extraction using Aspose.CAD
  in C#
og_title: 從 DWG 中擷取文字並在 C# 中將特定 DWG 轉換為圖像
schemas:
- author: Aspose
  dateModified: '2026-08-12'
  description: Extract text from DWG and convert specific DWG to image in C# using
    Aspose.CAD for .NET. Learn step‑by‑step with code snippets.
  headline: Extract text from DWG and convert specific DWG to image in C#
  type: TechArticle
- questions:
  - answer: Aspose.CAD supports DWG releases from AutoCAD 2000 up to the latest 2024
      version, covering over 90 % of files created in the field.
    question: Is Aspose.CAD compatible with all versions of DWG files?
  - answer: Yes – you can change resolution, image format, anti‑aliasing, and background
      color to suit PNG, JPEG, or PDF targets.
    question: Can I customize the rasterization options for different outputs?
  - answer: Explore the comprehensive [Aspose.CAD documentation](https://reference.aspose.com/cad/net/)
      for more code samples and API details.
    question: Where can I find additional examples and documentation?
  - answer: Absolutely – you can download a trial version on the **[Aspose trial download
      page](https://releases.aspose.com/)** and evaluate all features without restrictions
      for 30 days.
    question: Is there a free trial available for Aspose.CAD?
  - answer: Join the active [Aspose.CAD forum](https://forum.aspose.com/c/cad/19)
      where developers share solutions and the Aspose team answers questions.
    question: How can I get support or connect with the community?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- extract text from dwg
- Aspose.CAD
- C# CAD processing
title: 從 DWG 中擷取文字並在 C# 中將特定 DWG 轉換為圖像
url: /zh-hant/net/image-manipulation-and-rendering/converting-particular-dwg-to-image/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 C# 中將特定 DWG 轉換為影像 - Aspose.CAD 指南

## 介紹

在現代工程應用中，您常常需要 **從 DWG 檔案提取文字** 並 **將特定 DWG 轉換為影像** 格式，以便於報告或可視化。Aspose.CAD for .NET 為您提供完整功能的 API，無需任何外部 CAD 軟體即可同時完成這兩項工作。在本教學中，您將學習如何載入 DWG、篩選文字實體、將圖紙光柵化，最後將結果儲存為 PDF 影像——全部使用簡潔的 C# 程式碼。

## 快速回答
- **第一步是什麼？** 使用 `new CadImage("file.dwg")` 載入 DWG 檔案。  
- **哪個類別負責篩選文字？** 使用 `CadEntityFilter` 來選取 `Text` 實體。  
- **如何定義影像尺寸？** 在 `CadRasterizationOptions` 上設定 `Width` 與 `Height`。  
- **使用什麼輸出格式？** 範例儲存為 PDF，並在其中嵌入光柵影像。  
- **生產環境是否需要授權？** 需要 – 商業版 Aspose.CAD 授權會移除評估限制。

## 如何從 DWG 中提取文字？

載入 DWG，套用僅選取文字實體的篩選器，然後讀取每個實體的 `TextString` 屬性。此方法會返回圖紙中所有的註解、標籤或尺寸文字，讓您可以將其用於搜尋、索引或報告。

## 為什麼要將特定 DWG 轉換為影像？

將 DWG 轉換為光柵影像可讓您在無法直接呈現原生 CAD 格式的文件、網頁或行動應用程式中嵌入圖紙。Aspose.CAD 支援 **超過 50 種 CAD 格式**，且能在使用低於 200 MB 記憶體的情況下光柵化多百頁的圖紙，這使其適用於高吞吐量的伺服器情境。

## 前置條件

- Visual Studio（任何近期版本）用於編譯與執行 C# 專案。  
- Aspose.CAD for .NET – 請確保已安裝此函式庫。您可在 **[Aspose.CAD for .NET 下載頁面](https://releases.aspose.com/cad/net/)** 找到下載連結。  
- 您想要處理的 DWG 檔案；範例檔案 *visualization_-_conference_room.dwg* 於程式碼片段中使用。

## 匯入命名空間

以下命名空間可讓您存取核心 CAD 類別、光柵化選項以及 PDF 輸出輔助工具：

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## 步驟 1：載入 DWG 檔案

透過傳入 DWG 檔案路徑建立 `CadImage` 實例。`CadImage` 物件在記憶體中表示整個圖紙，並提供對其圖層、實體與中繼資料的存取。

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";
var cadImage = (CadImage)Aspose.CAD.Image.Load(sourceFilePath);
```

## 步驟 2：篩選實體

`CadEntityFilter` 讓您只挑選所需的實體。在本指南中，我們將其設定為保留 **文字** 物件，並剔除線條、圓形及其他您不希望出現在最終影像中的幾何圖形。

```csharp
CadBaseEntity[] entities = cadImage.Entities;
List<CadBaseEntity> filteredEntities = new List<CadBaseEntity>();

foreach (CadBaseEntity baseEntity in entities)
{
    // Selection or filtration of entities
    if (baseEntity.TypeName == CadEntityTypeName.TEXT)
    {
        filteredEntities.Add(baseEntity);
    }
}

cadImage.Entities = filteredEntities.ToArray();
```

## 步驟 3：設定光柵化選項

`CadRasterizationOptions` 控制圖紙如何轉換為點陣圖。您可以定義輸出尺寸、背景顏色與解析度（DPI）。以下的定義錨點說明此類別：

`CadRasterizationOptions` 類別指定影像尺寸、解析度以及將 CAD 圖紙轉換為光柵格式的渲染設定。

在將選項傳遞給 PDF 匯出器之前，先設定所需的寬度、高度與背景顏色。

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions rasterizationOptions =
    new Aspose.CAD.ImageOptions.CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.AutomaticLayoutsScaling = true;
```

## 步驟 4：設定 PDF 選項

`PdfOptions` 將光柵化設定與 PDF 專屬功能（如壓縮）結合。以下的定義錨點首先說明此類別：

`PdfOptions` 包含 PDF 產生參數，包含決定 CAD 資料在 PDF 文件中如何呈現的光柵化選項。

將先前建立的 `CadRasterizationOptions` 實例指派給 `VectorRasterizationOptions` 屬性。

```csharp
Aspose.CAD.ImageOptions.PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## 步驟 5：另存為 PDF

最後，對 `CadImage` 物件呼叫 `Save` 方法，傳入目標檔名與已設定好的 `PdfOptions`。PDF 內將包含篩選後圖紙的高品質影像。

```csharp
string outFile = MyDir + "result_out_generated.pdf";
cadImage.Save(outFile, pdfOptions);
```

## 常見問題與疑難排解

- **篩選後文字缺失** – 確認 DWG 確實包含 `Text` 實體；有些圖紙會以 `MText` 形式儲存註解。如有需要，請調整篩選器以包含 `MText`。  
- **輸出影像為空白** – 確認光柵化 DPI 足夠高（300 DPI 為安全預設），且在檢視 PDF 時背景顏色未設定為透明。  
- **大型檔案發生記憶體不足錯誤** – 使用支援串流的 `LoadOptions` 重載，避免一次將整個檔案載入記憶體。

## 常見問答

**Q: Aspose.CAD 是否相容所有版本的 DWG 檔案？**  
A: Aspose.CAD 支援從 AutoCAD 2000 到最新 2024 版的 DWG 版本，覆蓋超過 90 % 的現場產生檔案。

**Q: 我可以為不同的輸出自訂光柵化選項嗎？**  
A: 可以 – 您可以調整解析度、影像格式、抗鋸齒以及背景顏色，以符合 PNG、JPEG 或 PDF 目標。

**Q: 我可以在哪裡找到更多範例與文件？**  
A: 瀏覽完整的 [Aspose.CAD 文件](https://reference.aspose.com/cad/net/) 以取得更多程式碼範例與 API 細節。

**Q: 是否提供 Aspose.CAD 的免費試用？**  
A: 當然可以 – 您可在 **[Aspose 試用下載頁面](https://releases.aspose.com/)** 下載試用版，且可在 30 天內無限制評估所有功能。

**Q: 我該如何取得支援或與社群互動？**  
A: 加入活躍的 [Aspose.CAD 論壇](https://forum.aspose.com/c/cad/19)，開發者會在此分享解決方案，Aspose 團隊也會回覆問題。

**最後更新：** 2026-08-12  
**測試環境：** Aspose.CAD 24.11 for .NET  
**作者：** Aspose

## 相關教學

- [使用 C# 搜尋 DWG 檔案文字 - Aspose.CAD 教學](/cad/net/text-search-and-manipulation/searching-text-in-dwg-files/)
- [在 Aspose.CAD for .NET 中將 CAD 圖紙轉換為光柵影像](/cad/net/cad-drawing-manipulation/convert-cad-drawing-to-raster-image/)
- [在 C# 中渲染 DWG 文件 - Aspose.CAD 指南](/cad/net/image-manipulation-and-rendering/rendering-dwg-documents/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< blocks/products/products-backtop-button >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}