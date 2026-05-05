---
date: 2026-03-21
description: 了解如何使用 Aspose.CAD for .NET 從 DWG 建立 PDF，並將 DGN 匯出為 DWG 的一部分。本指南亦示範如何將
  DWG 轉換為 PDF 以及設定 PDF 選項。
linktitle: Export DGN as Part of DWG
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: 從 DWG 建立 PDF 並將 DGN 匯出為 DWG 的一部份 – Aspose.CAD for .NET
url: /zh-hant/net/cad-export-formats/export-dgn-as-part-of-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 從 DWG 建立 PDF 並將 DGN 作為 DWG 的一部分匯出 – Aspose.CAD for .NET

## 簡介

如果您需要 **create PDF from DWG** 檔案，同時將 DGN 設計嵌入為 DWG 的一部分，Aspose.CAD for .NET 讓這個過程變得簡單。在本教學中，我們將完整示範工作流程：載入 DWG、定位嵌入的 DGN underlay、設定光柵化選項，最後將結果匯出為 PDF 文件。無論您是建立批次轉換工具、報表引擎，或是 CAD‑BIM 整合服務，以下步驟都能提供堅實、可投入生產的基礎。

## 快速答覆
- **What library handles DWG → PDF conversion?** Aspose.CAD for .NET  
- **Can I export a DGN underlay while creating the PDF?** Yes – the underlay is accessed via `CadDgnUnderlay`.  
- **Which method sets PDF options?** `PdfOptions` together with `CadRasterizationOptions`.  
- **Do I need a license for commercial use?** Yes, a valid Aspose.CAD license is required.  
- **Supported .NET versions?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## 什麼是「從 DWG 建立 PDF」？

從 DWG 檔案建立 PDF 意味著將向量圖形渲染成光柵或向量式的 PDF 文件。此過程適用於與沒有 CAD 軟體的利害關係人分享圖紙、歸檔或產生可列印報告。Aspose.CAD 透過解析 DWG 實體並提供 `PdfOptions` 讓您細緻控制輸出，簡化了此任務。

## 為什麼要將 DGN 作為 DWG 的一部分匯出？

DGN underlay 通常代表來自 MicroStation 專案的參考幾何。將 DGN 與 DWG 一起匯出可保留原始設計的上下文，確保下游使用者看到完整的圖紙集合。這在 DWG 與 DGN 同時存在的多學科專案中特別有價值。

## 先決條件

- **Aspose.CAD for .NET** – 下載請點選 [here](https://releases.aspose.com/cad/net/)。  
- **Development Environment** – Visual Studio（任何近期版本）或您偏好的 .NET IDE。  
- **Basic C# knowledge** – 您應該熟悉 C# 語法與 .NET 專案結構。

## 匯入命名空間

在 C# 原始檔的最上方加入所需的 `using` 指令：

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## 逐步指南

### 步驟 1：定義檔案路徑

設定輸入的 DWG 檔案與輸出的 PDF 名稱。

```csharp
// Input and Output file paths
string fileName = "BlockRefDgn.dwg";
string outPath = fileName + ".pdf";
```

### 步驟 2：建立 `PdfOptions` 實例（設定 PDF 選項）

`PdfOptions` 讓您控制 PDF 的產生方式，例如頁面大小、壓縮與中繼資料。

```csharp
// Create an instance of PdfOptions class for exporting DWG to PDF
PdfOptions exportOptions = new PdfOptions();
```

### 步驟 3：載入 DWG 檔案

將 DWG 載入為 `CadImage`，以便檢查其實體。

```csharp
// Load the existing DWG file as an image and convert it to CadImage type
using (CadImage cadImage = (CadImage)Image.Load(fileName))
```

### 步驟 4：遍歷實體

走訪圖紙中的每個實體，以定位 DGN underlay。

```csharp
// Iterate through each entity inside the DWG file
foreach (CadBaseEntity baseEntity in cadImage.Entities)
```

### 步驟 5：檢查實體類型（如何匯出 DGN）

判斷目前的實體是否為 DGN underlay。

```csharp
// Check if the entity is an image definition
if (baseEntity.TypeName == CadEntityTypeName.DGNUNDERLAY)
```

### 步驟 6：取得 Underlay 路徑

取得 DGN 檔案的外部參考路徑。

```csharp
// If it's an image definition, get the external reference to the object
CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
Console.WriteLine(dgnFile.UnderlayPath);
```

### 步驟 7：定義光柵化選項（將 DWG 轉換為 PDF）

設定 DWG 在放入 PDF 前的光柵化方式。

```csharp
// Define settings for CadRasterizationOptions object
exportOptions.VectorRasterizationOptions = new CadRasterizationOptions()
{
    PageWidth = 1600,
    PageHeight = 1600,
    Layouts = new string[] { "Model" },
    AutomaticLayoutsScaling = false,
    NoScaling = true,
    BackgroundColor = Color.Black,
    DrawType = CadDrawTypeMode.UseObjectColor
};
```

### 步驟 8：將 DWG 匯出為 PDF

最後，將渲染後的影像儲存為 PDF 檔案。

```csharp
// Export the DWG to PDF by calling Save method
cadImage.Save(outPath, exportOptions);
```

## 常見問題與解決方案

| 問題 | 原因 | 解決方法 |
|-------|--------|-----|
| **`Image.Load` throws “File not found”** | 路徑不正確或檔案遺失。 | 使用絕對路徑或確保 DWG 已複製至輸出資料夾。 |
| **Underlay path is empty** | DGN underlay 未嵌入或參考斷裂。 | 確認 DWG 確實包含 DGN underlay，且外部 DGN 檔案可存取。 |
| **PDF output is blank** | 光柵化選項設定為零尺寸。 | 調整 `PageWidth`/`PageHeight` 或將 `NoScaling = false`。 |
| **License exception** | 未使用有效的 Aspose.CAD 授權。 | 在載入影像前套用授權：`License lic = new License(); lic.SetLicense("Aspose.CAD.lic");` |

## 常見問答

### Q1：我可以在商業項目中使用 Aspose.CAD for .NET 嗎？
A1：可以。請前往 [here](https://purchase.aspose.com/buy) 了解授權方案。

### Q2：處理 DWG 檔案的大小有任何限制嗎？
A2：Aspose.CAD 支援處理大型 DWG 檔案，但仍受硬體限制影響。

### Q3：是否提供試用版？
A3：有，您可在 [here](https://releases.aspose.com/) 取得免費試用。

### Q4：如何取得臨時授權？
A4：可於 [here](https://purchase.aspose.com/temporary-license/) 取得臨時授權。

### Q5：若遇到問題，我該向哪裡尋求協助？
A5：您可以前往 Aspose.CAD 論壇 [here](https://forum.aspose.com/c/cad/19) 尋求支援。

**Q: 如何設定額外的 PDF 中繼資料（作者、標題等）？**  
A: 在呼叫 `Save` 前使用 `exportOptions.Metadata` 屬性。

**Q: 能否將多個版面匯出為不同的 PDF 頁面？**  
A: 可以 – 在 `CadRasterizationOptions` 中設定 `Layouts = new string[] { "Layout1", "Layout2" }`。

**Q: Aspose.CAD 是否支援將 DWG 轉換為其他影像格式？**  
A: 當然。您可以使用相對應的 `Image.Save` 重載匯出為 PNG、JPEG、SVG 等格式。

**最後更新：** 2026-03-21  
**測試環境：** Aspose.CAD 24.11 for .NET  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}