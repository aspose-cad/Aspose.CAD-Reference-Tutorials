---
date: 2026-03-26
description: 學習如何使用 Aspose.CAD for .NET 從 CAD 建立 PDF，並將 DXF 轉換為 PDF。自訂筆刷選項，以在 PDF、PNG、BMP
  等格式中呈現驚豔的視覺效果。
linktitle: Pen Support in Export
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: 使用自訂筆選項從 CAD 建立 PDF – Aspose.CAD for .NET
url: /zh-hant/net/cad-features-and-support/pen-support-in-export/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 提升 Aspose.CAD for .NET 中自訂筆選項的 CAD 匯出

## 簡介

如果您需要快速且完整視覺控制地 **create PDF from CAD** 檔案，Aspose.CAD for .NET 正好提供此功能。透過利用函式庫的筆支援功能，您可以定義起點與終點帽、線段接合方式以及其他繪圖屬性，產生外觀完全符合需求的 PDF。本教學將帶您完成整個流程——從載入 DXF 檔案到匯出精緻的 PDF——同時說明如何在 **export CAD to PNG** 或 **rasterize CAD image** 以供其他格式使用時，重複使用相同的設定。

## 快速答覆
- **「create PDF from CAD」是什麼意思？** 它將基於向量的 CAD 繪圖（例如 DXF）轉換為 PDF 文件，同時保留幾何形狀和樣式。  
- **哪些格式支援筆選項？** PDF, PNG, BMP, GIF, JPEG2000, JPEG, PSD, TIFF, and WMF.  
- **開發是否需要授權？** 免費試用可用於測試；正式環境需商業授權。  
- **可以為其他格式變更線端帽嗎？** 可以——筆選項適用於 Aspose.CAD 支援的任何光柵化目標。  
- **支援哪些 .NET 版本？** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## 什麼是 CAD 匯出中的筆支援？

筆支援讓您在 CAD 繪圖被光柵化或向量光柵化時，自訂線條的繪製方式。您可以設定 `StartCap`、`EndCap`、`LineJoin`、`DashStyle` 等屬性。這些設定會影響匯出圖像或 PDF 的最終外觀，讓您對視覺品質擁有精細的控制。

## 為什麼在 **create PDF from CAD** 時使用自訂筆選項？

- **Consistent branding** – 在所有文件中匹配企業線條樣式。  
- **Improved readability** – 更粗的端帽與接合使技術圖紙在螢幕與列印時更清晰。  
- **Cross‑format flexibility** – 相同的筆配置可用於 PNG、BMP 及其他光柵格式，為您節省時間。

## 先決條件

- 已安裝 Aspose.CAD for .NET（從[發佈頁面](https://releases.aspose.com/cad/net/)下載）。  
- 具備 DXF（繪圖交換格式）的基本知識。  
- 熟悉 C# 程式設計。

## 匯入命名空間

開始之前，請確保在 C# 專案中匯入必要的命名空間：

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Drawing;
using System.Drawing.Drawing2D;
```

## 步驟 1：設定文件目錄

定義包含來源 CAD 檔案的資料夾：

```csharp
string MyDir = "Your Document Directory";
```

## 步驟 2：載入 CAD 圖像

將 CAD 繪圖（例如 DXF 檔案）載入至 `Aspose.CAD.Image` 物件：

```csharp
string sourceFilePath = MyDir + "conic_pyramid.dxf";
CadImage cadImage = (CadImage)Image.Load(sourceFilePath);
```

## 步驟 3：設定光柵化選項

建立光柵化與 PDF 選項物件。這些物件讓您控制 CAD 資料如何轉換為光柵圖像或 PDF 頁面：

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
PdfOptions pdfOptions = new PdfOptions();
```

## 步驟 4：自訂筆選項

這裡是 **customize the pen** 的地方。您可以將起點與終點帽設定為 `Flat`、`Round`、`Square` 等。這就是「如何匯出 CAD」並具備所需視覺樣式的核心：

```csharp
rasterizationOptions.PenOptions = new PenOptions
{
   StartCap = LineCap.Flat,
   EndCap = LineCap.Flat
};
```

*小技巧：* 在 **export CAD to PNG** 時，可嘗試使用 `LineCap.Round` 以獲得更平滑的線端。

## 步驟 5：套用向量光柵化選項

將光柵化設定附加至 PDF 選項，讓匯出過程知道使用哪個筆配置：

```csharp
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## 步驟 6：儲存匯出的 PDF

最後，產生 PDF 檔案。此步驟 **creates PDF from CAD** 並套用自訂筆設定：

```csharp
cadImage.Save(MyDir + "9LHATT-A56_generated.pdf", pdfOptions);
```

您可以將 `PdfOptions` 替換為 `PngOptions`、`BmpOptions` 等，以 **export CAD to PNG** 或其他光柵格式，同時保留相同的筆配置。

## 常見使用情境

- **Technical documentation** – 在工程 PDF 中嵌入精確的線條樣式。  
- **Automated report generation** – 使用單一筆設定批次處理多個 DXF 檔案為 PDF。  
- **Web services** – 提供 API 即時將上傳的 DXF 檔案轉換為 PDF，確保樣式一致。

## 故障排除與常見問題

| 問題 | 原因 | 解決方案 |
|-------|--------|----------|
| 匯出的線條比預期更粗 | DPI 高於預期 | 設定 `rasterizationOptions.PageWidth` / `PageHeight` 或調整 `Resolution`。 |
| PNG 輸出時忽略筆選項 | 使用 `ImageOptions` 而非 `VectorRasterizationOptions` | 確保在儲存前指派 `rasterizationOptions.PenOptions`。 |
| PDF 檔案為空 | 來源 DXF 路徑不正確或檔案已損毀 | 驗證 `sourceFilePath` 並確認 DXF 能正常載入且未拋出例外。 |

## 常見問答

### Q1：我可以將這些筆選項用於 PDF 之外的其他影像格式嗎？

A1：可以，筆選項可套用於多種影像格式，例如 PNG、BMP、GIF、JPEG 等。

### Q2：在哪裡可以找到 Aspose.CAD for .NET 的其他文件？

A2：請參閱[文件](https://reference.aspose.com/cad/net/)以取得完整資訊與範例。

### Q3：是否提供 Aspose.CAD for .NET 的免費試用？

A3：可以，您可在[此處](https://releases.aspose.com/)取得免費試用。

### Q4：如何取得 Aspose.CAD for .NET 的臨時授權？

A4：請前往[臨時授權頁面](https://purchase.aspose.com/temporary-license/)了解臨時授權選項。

### Q5：在哪裡可以尋求 Aspose.CAD for .NET 的社群支援？

A5：可於[Aspose.CAD 論壇](https://forum.aspose.com/c/cad/19)與社群互動。

## 其他常見問答

**Q: 如何以程式方式 **convert DXF to PDF**？**  
A: 使用 `Image.Load` 載入 DXF，設定 `CadRasterizationOptions` 與 `PdfOptions`，然後如上述步驟呼叫 `Save`。

**Q: 可以在不建立 PDF 的情況下光柵化 CAD 圖像嗎？**  
A: 可以——使用 `PngOptions`、`BmpOptions` 或其他光柵格式類別，並指派相同的 `rasterizationOptions` 以達成高品質光柵化。

**Q: 在從 CAD 建立 PDF 時能否變更線寬？**  
A: 在儲存前調整 `rasterizationOptions.CustomLineWidth` 或修改 `PenOptions.Width` 屬性。

**Q: 此函式庫支援 3D DXF 檔案嗎？**  
A: Aspose.CAD 專注於 2D 向量資料；光柵化時會忽略 3D 實體。

**Q: 需要哪個版本的 Aspose.CAD 才能使用這些功能？**  
A: 筆支援自 20.9 版起即已提供，任何更新的版本皆可使用。

---

**最後更新：** 2026-03-26  
**測試環境：** Aspose.CAD for .NET 24.12  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}