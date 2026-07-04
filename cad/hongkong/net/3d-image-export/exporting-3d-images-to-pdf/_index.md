---
date: 2026-07-04
description: 了解如何使用 Aspose.CAD for .NET 設定 PDF 頁面尺寸並從 3D CAD 圖像匯出 PDF – 逐步說明如何將 DWG
  轉換為 PDF 以及將 CAD 儲存為 PDF。
keywords:
- set pdf page size
- export pdf from cad
- convert dwg to pdf
- save cad as pdf
- cad to pdf tutorial
linktitle: 匯出 3D 圖像至 PDF
schemas:
- author: Aspose
  dateModified: '2026-07-04'
  description: Learn how to set PDF page size and export PDF from 3D CAD images using
    Aspose.CAD for .NET – a step‑by‑step guide to convert DWG to PDF and save CAD
    as PDF.
  headline: Set PDF page size – Export 3D Images to PDF with Aspose.CAD
  type: TechArticle
- description: Learn how to set PDF page size and export PDF from 3D CAD images using
    Aspose.CAD for .NET – a step‑by‑step guide to convert DWG to PDF and save CAD
    as PDF.
  name: Set PDF page size – Export 3D Images to PDF with Aspose.CAD
  steps:
  - name: Load the CAD Image
    text: '`Image` class represents a CAD drawing loaded into memory, ready for rasterization.'
  - name: Configure Rasterization Options (Save CAD as PDF)
    text: '`RasterizationOptions` class defines how the CAD data is rasterized, including
      page size, DPI, and whether 3‑D entities are rendered.'
  - name: Set PDF Options (Create PDF from CAD)
    text: '`PdfOptions` class holds the output format settings and links the rasterization
      options to PDF generation.'
  - name: Save as PDF (Generate PDF from 3D Model)
    text: '`Save` method on the `Image` object writes the rasterized content to the
      specified PDF file, producing a ready‑to‑share document.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD supports more than 50 input and output formats, including
      DWG, DXF, DGN, STL, and IFC, ensuring flexibility for any project.
    question: Is Aspose.CAD compatible with all CAD file formats?
  - answer: Absolutely. Set `PageWidth` and `PageHeight` in `RasterizationOptions`
      to any size in points, inches, or millimetres before calling `Save`.
    question: Can I customize the page dimensions when exporting to PDF?
  - answer: Yes, you can obtain temporary licenses for Aspose.CAD by visiting [Temporary
      License](https://purchase.aspose.com/temporary-license/).
    question: Are temporary licenses available for Aspose.CAD?
  - answer: Head to the [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19) for
      expert help and peer‑to‑peer advice.
    question: Where can I find additional support or community discussions?
  - answer: Yes, you can explore the features of Aspose.CAD by accessing the [free
      trial](https://releases.aspose.com/).
    question: Is there a free trial version of Aspose.CAD?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: 設定 PDF 頁面尺寸 – 使用 Aspose.CAD 匯出 3D 圖像至 PDF
url: /zh-hant/net/3d-image-export/exporting-3d-images-to-pdf/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 匯出 3D 圖像至 PDF - Aspose.CAD 教學

## 介紹

如果您需要在將 3‑D CAD 圖紙轉換為 PDF 時 **設定 PDF 頁面大小**，您來對地方了。本教學將一步一步示範如何載入 CAD 檔案、設定光柵化選項（包括自訂頁面尺寸），並使用 Aspose.CAD for .NET 產生高保真度的 PDF。完成後，您將能夠 **從 CAD 匯出 PDF**、**將 CAD 儲存為 PDF**，且無需安裝 AutoCAD 即可掌控每個版面細節。

## 快速解答
- **「從 CAD 匯出 PDF」是什麼意思？** 它會將 CAD 圖紙（DWG、DXF、DGN 等）轉換為可在任何裝置上開啟的 PDF。  
- **哪個函式庫執行轉換？** Aspose.CAD for .NET 提供光柵化與 PDF 匯出，且不需要外部相依性。  
- **我需要授權嗎？** 生產環境需要臨時或正式授權；亦提供免費試用版。  
- **我可以設定自訂頁面尺寸嗎？** 可以——在 `RasterizationOptions` 中使用 `PageWidth` 和 `PageHeight`。  
- **3‑D 幾何會被保留嗎？** 3‑D 實體會被光柵化；若要完整支援 3‑D，請啟用 `TypeOfEntities.Entities3D`。  

## 在 CAD 中「匯出 PDF」是什麼意思？

從 CAD 匯出 PDF 意指將 CAD 圖紙（DWG、DXF、DGN 等）轉換為 PDF 檔案，該檔案可包含向量圖形、光柵化的 3‑D 觀景以及精確的頁面版面資訊，方便與未安裝 CAD 軟體的任何人分享。

## 為什麼使用 Aspose.CAD 匯出 PDF？

Aspose.CAD 讓您 **設定 PDF 頁面大小**，並完全以受管理的 .NET 程式碼匯出 PDF。它支援超過 50 種 CAD 格式，能處理高達 2 GB 的檔案而不需將整個文件載入記憶體，並保留線寬、顏色，以及可選的 3‑D 實體渲染，光柵化 DPI 可達 1200。此函式庫可在 Windows、Linux 與 macOS 上執行，產生的 PDF 可在任何平台使用。

## 前置條件

- **已安裝 Aspose.CAD for .NET**。從 [Aspose.CAD for .NET 下載頁面](https://releases.aspose.com/cad/net/) 下載。  
- 包含您欲轉換之 CAD 檔案的資料夾（例如 `C:\CAD\`）。  
- .NET 6.0 或更新版本（或 .NET Framework 4.7.2）。  

## 匯入命名空間

`using` 陳述式會匯入使用光柵化與 PDF 選項所需的 Aspose.CAD 命名空間。  

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
```

## 步驟指南

### 如何在將 CAD 匯出為 PDF 時設定 PDF 頁面大小？

載入 CAD 檔案，在 `RasterizationOptions` 中設定頁面尺寸，將這些選項附加至 `PdfOptions` 實例，然後呼叫 `Save`。此四步流程讓您完整掌控輸出尺寸與品質，同時保持程式碼簡潔。

### 步驟 1：載入 CAD 圖像

`Image` 類別代表已載入記憶體、可供光柵化的 CAD 圖紙。  

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";
using (Image cadImage = Image.Load(sourceFilePath))
{
    // Your code for loading the CAD image goes here
}
```

### 步驟 2：設定光柵化選項（將 CAD 儲存為 PDF）

`RasterizationOptions` 類別定義 CAD 資料的光柵化方式，包括頁面大小、DPI 以及是否渲染 3‑D 實體。  

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
// rasterizationOptions.TypeOfEntities = TypeOfEntities.Entities3D;

rasterizationOptions.Layouts = new string[] { "Model" };
```

### 步驟 3：設定 PDF 選項（從 CAD 建立 PDF）

`PdfOptions` 類別保存輸出格式設定，並將光柵化選項連結至 PDF 產生。  

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

### 步驟 4：儲存為 PDF（從 3D 模型產生 PDF）

`Image` 物件的 `Save` 方法會將光柵化內容寫入指定的 PDF 檔案，產生可直接分享的文件。  

```csharp
MyDir = MyDir + "Export3DImagestoPDF_out.pdf";
cadImage.Save(MyDir, pdfOptions);
```

## 常見問題與解決方案

| 問題 | 原因 | 解決方案 |
|-------|--------|-----|
| **輸出 PDF 為空白** | 版面名稱錯誤或缺少 `Model` 版面。 | 確認 `rasterizationOptions.Layouts` 與 CAD 檔案中存在的版面相符。 |
| **解析度低** | 預設光柵化 DPI 較低。 | 在儲存前設定 `rasterizationOptions.Resolution = 300;`。 |
| **3‑D 實體未顯示** | `TypeOfEntities` 被註解掉。 | 取消註解 `rasterizationOptions.TypeOfEntities = TypeOfEntities.Entities3D;`。 |
| **授權例外** | 使用未授權的試用版。 | 透過 `License license = new License(); license.SetLicense("Aspose.CAD.lic");` 套用臨時或永久授權。 |

## 常見問答

**Q: Aspose.CAD 是否相容所有 CAD 檔案格式？**  
A: 是的，Aspose.CAD 支援超過 50 種輸入與輸出格式，包括 DWG、DXF、DGN、STL 與 IFC，確保任何專案的彈性。

**Q: 匯出為 PDF 時我可以自訂頁面尺寸嗎？**  
A: 當然可以。在呼叫 `Save` 前於 `RasterizationOptions` 中設定 `PageWidth` 與 `PageHeight`，可使用點、英吋或毫米作為單位。

**Q: Aspose.CAD 有提供臨時授權嗎？**  
A: 有，您可前往 [Temporary License](https://purchase.aspose.com/temporary-license/) 取得 Aspose.CAD 的臨時授權。

**Q: 我可以在哪裡找到其他支援或社群討論？**  
A: 請前往 [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19) 取得專家協助與同儕交流。

**Q: 有免費試用版的 Aspose.CAD 嗎？**  
A: 有，您可透過 [free trial](https://releases.aspose.com/) 來體驗 Aspose.CAD 的功能。

## 結論

您現在已擁有完整、可投入生產的方式，使用 Aspose.CAD for .NET **設定 PDF 頁面大小** 並 **從 3D CAD 圖像匯出 PDF**。透過調整光柵化選項，您可以微調解析度、頁面版面與 3‑D 實體渲染，以符合任何文件需求。嘗試不同的 DPI 設定與頁面尺寸，以取得檔案大小與視覺保真度之間的最佳平衡。

{{< blocks/products/products-backtop-button >}}

## 相關教學

- [匯出特定版面至 PDF - Aspose.CAD 指南](/cad/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/)
- [匯出 DWG 至 PDF 或光柵圖像 - Aspose.CAD 指南](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)
- [在 Aspose.CAD for .NET 中匯出 DGN 至 PDF](/cad/net/cad-export-formats/export-dgn-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

--- 

**最後更新：** 2026-07-04  
**測試環境：** Aspose.CAD 24.11 for .NET  
**作者：** Aspose