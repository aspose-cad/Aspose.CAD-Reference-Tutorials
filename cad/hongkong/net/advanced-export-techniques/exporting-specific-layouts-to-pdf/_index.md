---
date: 2026-03-13
description: 學習如何設定 CAD 光柵化選項，並使用 Aspose.CAD for .NET 將特定 DWG 版面匯出為 PDF —— 從 CAD 檔案生成
  PDF 的終極指南。
linktitle: Exporting Specific Layouts to PDF
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: 設定 CAD 點陣化選項 – 匯出特定圖面至 PDF - Aspose.CAD 指南
url: /zh-hant/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 將特定版面匯出為 PDF - Aspose.CAD 指南

## 簡介

在本教學中，您將了解 **如何設定 CAD 光柵化選項**，以便直接將 DWG 檔案中的單一版面或多個版面匯出為 PDF。Aspose.CAD for .NET 讓 *dwg to pdf conversion c#* 流程變得簡單，讓您完整掌控頁面大小、解析度與版面選擇。完成本指南後，您只需幾行程式碼即可 **從 CAD 檔案建立 PDF**。

## 快速解答
- **「設定 CAD 光柵化選項」的作用是什麼？**  
  它告訴 Aspose.CAD 如何將向量資料（版面、圖層、線寬）渲染成光柵化的 PDF 頁面。  
- **哪個方法可將 DWG 版面匯出為 PDF？**  
  使用帶有已設定 `CadRasterizationOptions` 的 `PdfOptions`，呼叫 `Image.Save`。  
- **我可以一次匯出多個版面嗎？**  
  可以——在 `Layouts` 屬性中提供版面名稱陣列。  
- **正式環境需要授權嗎？**  
  需要商業授權；亦提供免費試用供評估。  
- **支援哪些 .NET 版本？**  
  .NET Framework 4.5 以上、.NET Core 3.1 以上、.NET 5/6 及更高版本。

## 什麼是「設定 CAD 光柵化選項」？

`CadRasterizationOptions` 是用來控制 CAD 實體在轉換為光柵格式（如 PDF）時的光柵化方式的類別。透過設定其屬性——頁面尺寸、版面選擇、背景顏色等——您即可決定 **export dwg layout to pdf** 操作的視覺結果。

## 為什麼要設定 CAD 光柵化選項？

- **精確度** – 完全保留原始 CAD 圖紙中的線寬與比例。  
- **效能** – 僅渲染所需的版面，減少檔案大小與處理時間。  
- **彈性** – 調整頁寬/頁高、DPI 與背景，以符合您的報告標準。  

## 先決條件

在深入程式碼之前，請確保您已具備：

- 已安裝 **Aspose.CAD for .NET**。您可在[此處](https://releases.aspose.com/cad/net/)下載。  
- .NET 開發環境（Visual Studio、VS Code 或任何您偏好的 IDE）。  
- 包含至少一個版面的 DWG 檔案（此處使用的範例檔案為 `visualization_-_conference_room.dwg`）。

## 匯入命名空間

在您的 .NET 專案中，匯入 Aspose.CAD 所需的命名空間：

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## 逐步指南

### 步驟 1：載入 DWG 檔案

首先，將 Aspose.CAD 指向您要轉換的來源 DWG 檔案。

```csharp
// The path to the documents directory.
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";

using (Image image = Image.Load(sourceFilePath))
{
    // Your code for further steps goes here.
}
```

### 步驟 2：設定 **CadRasterizationOptions**

在此我們設定決定 PDF 頁面大小與解析度的光柵化參數。

```csharp
// Create an instance of CadRasterizationOptions and set its various properties
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
```

> **專業提示：** 調整 `PageWidth` 與 `PageHeight` 以符合目標 PDF 版面的尺寸。較大的數值會提升細節，但同時也會增加檔案大小。

### 步驟 3：指定版面名稱

告訴 Aspose.CAD 要渲染哪個版面（或哪些版面）。將 `"Layout1"` 替換為 DWG 檔案中實際的版面名稱。

```csharp
// Specify desired layout name
rasterizationOptions.Layouts = new string[] { "Layout1" };
```

> **為什麼重要：** 限制 `Layouts` 陣列可避免匯出不需要的圖紙，使 **dwg to pdf conversion c#** 操作更快，且產生的 PDF 更乾淨。

### 步驟 4：建立 `PdfOptions`

將光柵化設定連結至 PDF 匯出選項。

```csharp
// Create an instance of PdfOptions
PdfOptions pdfOptions = new PdfOptions();
// Set the VectorRasterizationOptions property
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

### 步驟 5：匯出為 PDF

最後，將渲染好的版面儲存為 PDF 檔案。

```csharp
MyDir = MyDir + "ExportSpecificLayoutToPDF_out.pdf";
// Export the DWG to PDF
image.Save(MyDir, pdfOptions);
```

### 步驟 6：顯示成功訊息

簡短的主控台輸出可確認操作已成功。

```csharp
// Display success message
Console.WriteLine("\nThe DWG file with a specific layout exported successfully to PDF.\nFile saved at " + MyDir);
```

## 常見問題與解決方案

| Issue | Cause | Fix |
|-------|-------|-----|
| **未產生 PDF** | `Layouts` 陣列與 DWG 中的任何版面名稱不匹配。 | 使用 CAD 檢視器確認版面名稱，並更新 `Layouts` 屬性。 |
| **空白頁面** | `PageWidth`/`PageHeight` 設為 0 或極小值。 | 使用合理的尺寸（例如 1600 × 1600），或省略這些屬性讓 Aspose 自動計算。 |
| **縮放不正確** | 需要高解析度輸出時未設定 DPI。 | 在匯出前設定 `rasterizationOptions.Resolution = 300;`（或所需 DPI）。 |

## 常見問答

**Q: 我可以同時匯出多個版面嗎？**  
A: 可以，只需在第 3 步修改 `Layouts` 陣列，包含所有需要的版面名稱，例如 `new string[] { "Layout1", "Layout2" }`。

**Q: Aspose.CAD 是否相容其他 CAD 檔案格式？**  
A: 當然。它支援 DWG、DXF、DWF、DGN 等多種格式。

**Q: 如何調整 PDF 輸出設定（除頁面大小外）？**  
A: 可探索 `CadRasterizationOptions` 的其他屬性，如 `Resolution`、`BackgroundColor`、`DrawType`，以微調結果。

**Q: 在哪裡可以找到更多 Aspose.CAD 文件？**  
A: 前往[文件說明](https://reference.aspose.com/cad/net/)取得深入的 API 參考與範例。

**Q: 是否提供免費試用？**  
A: 有，您可在[此處](https://releases.aspose.com/)取得免費試用。

## 結論

您現在已學會如何 **設定 CAD 光柵化選項**，並使用它們 **將特定 DWG 版面匯出為 PDF**，搭配 Aspose.CAD for .NET。此方法讓您對轉換過程擁有精確的控制，能快速且可靠地將 CAD 轉 PDF 功能整合至任何 C# 應用程式中。

---

**最後更新：** 2026-03-13  
**測試版本：** Aspose.CAD 24.11 for .NET  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}