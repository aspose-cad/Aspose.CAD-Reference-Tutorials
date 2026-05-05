---
date: 2026-04-09
description: 學習如何在 C# 中載入 DWFX 檔案，並使用 Aspose.CAD for .NET 將 CAD 轉換為 PDF。一步一步的指南，實現無縫整合。
keywords:
- load dwfx file c#
- c# convert cad to pdf
- aspose.cad dwfx
linktitle: 在 C# 中開啟與存取 DWFX 檔案
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: 如何在 C# 中使用 Aspose.CAD 載入 DWFX 檔案指南
url: /zh-hant/net/dwg-file-manipulation/opening-and-accessing-dwfx-files/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何在 C# 中使用 Aspose.CAD 載入 DWFX 檔案指南

## 介紹

如果您需要 **load DWFX file C#** 並將其轉換為 PDF，您來對地方了。在本教學中，我們將逐步說明如何使用 Aspose.CAD for .NET 開啟 DWFX 圖紙、設定光柵化，最後 **c# convert CAD to PDF**。無論您是開發桌面工具還是 Web 服務，方法皆相同，且適用於 Aspose.CAD 支援的任何 .NET 版本。

## 快速解答
- **需要哪個函式庫？** Aspose.CAD for .NET  
- **我可以將 DWFX 轉換為 PDF 嗎？** 是 – 只需設定 `CadRasterizationOptions` 並使用 `PdfOptions`。  
- **支援哪些 .NET 版本？** .NET Framework 4.5+、.NET Core 3.1+、.NET 5/6+。  
- **測試需要授權嗎？** 免費試用版可用於開發；正式環境需購買永久授權。  
- **程式執行需要多久？** 在現代 CPU 上，載入並轉換一般 DWFX 檔案通常在一秒內完成。

## 什麼是 DWFX 檔案？

DWFX（Design Web Format XPS）是一種基於 XML 的 CAD 圖紙表示法，可在瀏覽器及其他檢視器中呈現。由於它儲存向量資料，因而非常適合在不失真的情況下高品質轉換為 PDF。

## 為何在 C# 中使用 Aspose.CAD 載入 DWFX 檔案？

* **完整格式支援** – Aspose.CAD 能理解 DWFX 以及其他數十種 CAD 格式。  
* **無外部相依性** – 純 .NET，無需 AutoCAD 或其他原生元件。  
* **簡易光柵轉向量** – 只需幾行程式碼即可在光柵圖像與向量 PDF 之間切換。  

## 前置條件

在深入程式碼之前，請確保您已具備以下條件：

1. 已安裝 **Aspose.CAD for .NET**。您可於 [here](https://releases.aspose.com/cad/net/) 下載。  
2. 一個包含欲處理 DWFX 檔案的資料夾。請記下來源與輸出位置的完整路徑。

## 如何在 C# 中載入 DWFX 檔案

以下為逐步指南。每一步皆附有簡短說明，並提供您需要複製的完整程式碼區塊。

### 匯入命名空間

```csharp
using Aspose.CAD.ImageOptions;
using System;
```

這些命名空間讓您可以存取用於載入 CAD 檔案的 `Image` 類別，以及光柵化與 PDF 輸出的相關選項。

### 步驟 1：設定來源與輸出目錄

```csharp
string SourceDir = "Your Document Directory";
string OutputDir = "Your Document Directory";
```

將 `"Your Document Directory"` 替換為 DWFX 檔案所在的路徑，以及您希望儲存 PDF 的目錄。

### 步驟 2：載入 DWFX 檔案

```csharp
using (Image cadDrawing = Image.Load(SourceDir + "Tyrannosaurus.dwfx"))
```

`Image.Load` 會將 DWFX 檔案讀入 Aspose.CAD 可操作的 `Image` 物件。將 `"Tyrannosaurus.dwfx"` 改為您自己的圖紙名稱。

### 步驟 3：設定光柵化選項

```csharp
var rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = cadDrawing.Size.Width;
rasterizationOptions.PageHeight = cadDrawing.Size.Height;
```

光柵化選項告訴 Aspose.CAD 最終頁面的尺寸。使用原始圖紙尺寸可保留精確比例。

### 步驟 4：另存為 PDF（c# convert CAD to PDF）

```csharp
PdfOptions CADf = new PdfOptions();
CADf.VectorRasterizationOptions = rasterizationOptions;
cadDrawing.Save(OutputDir + "OpenDwfxFile_out.pdf", CADf);
```

此處我們透過將光柵化設定附加至 `PdfOptions` 物件並呼叫 `Save`，**c# convert CAD to PDF**。輸出檔案會存放在您指定的資料夾中。

### 步驟 5：顯示成功訊息

```csharp
Console.WriteLine("OpenDwfxFile executed successfully");
```

簡單的主控台訊息會告訴您轉換已順利完成，且未發生錯誤。

## 常見問題與技巧

* **找不到檔案** – 請再次確認 `SourceDir` 路徑，並確保檔名完全相符（包括大小寫）。  
* **空白 PDF** – 請確認 DWFX 檔案確實包含向量資料；某些匯出工具可能產生空白圖紙。  
* **效能** – 對於非常大的圖紙，建議縮小 `PageWidth`/`PageHeight` 或在 `CadRasterizationOptions` 中設定較低的 `Resolution`。

## 常見問答

### Q1：Aspose.CAD for .NET 是否相容所有 DWFX 檔案？

A1：Aspose.CAD for .NET 支援多種 CAD 格式，包括 DWFX。但建議您查閱文件以取得特定相容性細節。

### Q2：在哪裡可以找到 Aspose.CAD for .NET 的文件？

A2：文件可於 [here](https://reference.aspose.com/cad/net/) 取得。

### Q3：購買前可以試用 Aspose.CAD for .NET 嗎？

A3：可以，您可於 [here](https://releases.aspose.com/) 下載免費試用版。

### Q4：如何取得 Aspose.CAD for .NET 的臨時授權？

A4：可於 [here](https://purchase.aspose.com/temporary-license/) 取得臨時授權。

### Q5：需要支援或有其他問題？

A5：請前往 [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) 取得協助。

### Q6：可以批次處理多個 DWFX 檔案嗎？

A6：當然可以。將載入與儲存的邏輯包在 `foreach` 迴圈中，遍歷目錄內的檔案即可。

### Q7：轉換是否保留圖層與顏色？

A7：若來源 DWFX 含有圖層與顏色等向量資訊，轉換後的 PDF 會保留這些資訊。

---

**最後更新：** 2026-04-09  
**測試環境：** Aspose.CAD for .NET 24.11  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}