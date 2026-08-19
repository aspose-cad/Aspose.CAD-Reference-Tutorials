---
date: 2026-03-19
description: 學習如何在 .NET 中使用 Aspose.CAD 將 CAD 轉換為 PNG，高效地將 CAD 儲存為 PNG，並簡化您的點陣圖像工作流程。
linktitle: Convert CAD Drawing to Raster Image
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: 在 Aspose.CAD for .NET 中將 CAD 轉換為 PNG
url: /zh-hant/net/cad-drawing-manipulation/convert-cad-drawing-to-raster-image/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 Aspose.CAD for .NET 中將 CAD 轉換為 PNG

## 介紹

在現代以 CAD 為核心的應用程式中，**將 CAD 轉換為 PNG** 是常見需求——無論是要產生縮圖、在網頁中嵌入圖紙，或是將設計存檔為點陣圖。本教學將帶您完整了解如何使用 Aspose.CAD for .NET 函式庫，將 CAD 繪圖（DXF、DWG 等）轉換為高品質 PNG 檔案。完成後，您即可 **將 CAD 儲存為 PNG**，並可完整掌控光柵化設定，讓工作流程更快速、更可靠。

## 快速答覆
- **哪個函式庫最適合 CAD 轉 PNG？** Aspose.CAD for .NET。  
- **哪些檔案格式可以匯出為 PNG？** DWG、DXF、DGN 以及其他受支援的 CAD 格式。  
- **正式環境需要授權嗎？** 需要商業授權；亦提供免費試用版。  
- **可以自訂影像尺寸與品質嗎？** 當然可以——光柵化選項允許您設定頁面寬度、高度、背景色等。  
- **程式碼是否相容於 .NET Core / .NET 6？** 相容，相同的 API 可在 .NET Framework、.NET Core 以及 .NET 5/6 上執行。

## 什麼是「convert CAD to PNG」？
將 CAD 轉換為 PNG 意指將向量式的 CAD 繪圖光柵化為像素式的影像格式（PNG）。此過程保留視覺忠實度，同時讓檔案能在瀏覽器、行動應用或任何不原生支援 CAD 格式的環境中輕鬆顯示。

## 為什麼使用 Aspose.CAD 來轉換 CAD 為 PNG？
- **無外部相依** – 完全 .NET 實作，不需原生 CAD 引擎。  
- **完整格式支援** – 支援 DWG、DXF、DGN 等多種格式。  
- **細緻的光柵化控制** – 頁面尺寸、解析度、背景、線寬等皆可自訂。  
- **高效能** – 為伺服器端批次處理優化。

## 前置作業

在開始之前，請確認您已具備：

1. **Aspose.CAD for .NET** – 從[下載頁面](https://releases.aspose.com/cad/net/)取得。  
2. 支援 .NET 的 IDE（Visual Studio、Rider 或 VS Code），且專案目標為 .NET Framework 4.6 以上或 .NET Core 3.1 以上。

## 匯入命名空間

在 .NET 專案中，匯入必要的命名空間以存取 Aspose.CAD 功能。於程式碼檔案開頭加入以下內容：

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## 步驟說明

### 步驟 1：定義檔案路徑
設定來源 CAD 檔案與目標 PNG 路徑。將佔位符替換為您機器上的實際目錄。

```csharp
// The path to the documents directory.
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";
```

### 步驟 2：載入 CAD 繪圖
使用 `Aspose.CAD.Image.Load` 開啟 CAD 檔案。此操作會在記憶體中建立繪圖的表示，供後續光柵化使用。

```csharp
using (Aspose.CAD.Image image = Aspose.CAD.Image.Load(sourceFilePath))
{
```

### 步驟 3：設定光柵化選項  
定義向量資料如何轉換為像素。此範例設定 1200 × 1200 像素的畫布，您可依需求調整 `PageWidth` 與 `PageHeight`（例如在 **convert dwg to png** 時使用特定 DPI）。

```csharp
// Create an instance of CadRasterizationOptions
Aspose.CAD.ImageOptions.CadRasterizationOptions rasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
// Set page width & height
rasterizationOptions.PageWidth = 1200;
rasterizationOptions.PageHeight = 1200;
```

> **專業提示：** 若要提升大型圖紙的渲染速度，可將 `rasterizationOptions.BackgroundColor` 設為單色，或啟用 `rasterizationOptions.DrawType` 以加速向量轉換。

### 步驟 4：建立 PNG 選項以產生最終影像  
將光柵化設定包裝於 `PngOptions` 物件中，告訴 Aspose.CAD 輸出 PNG 檔案。

```csharp
// Create an instance of PngOptions for the resultant image
ImageOptionsBase options = new Aspose.CAD.ImageOptions.PngOptions();
// Set rasterization options
options.VectorRasterizationOptions = rasterizationOptions;
```

### 步驟 5：儲存產生的 PNG  
將目錄路徑與欲輸出的檔名結合，將光柵化後的影像寫入磁碟。此步驟即 **將 CAD 儲存為 PNG**。

```csharp
MyDir = MyDir + "conic_pyramid_raster_image_out.png";
// Save resultant image
image.Save(MyDir, options);
```

### 步驟 6：顯示成功訊息  
確認轉換成功並顯示檔案儲存位置。

```csharp
//ExEnd:ConvertDrawingToRasterImage            
Console.WriteLine("\nCAD drawing converted successfully to raster image format.\nFile saved at " + MyDir);
```

> **注意：** 第 2 步的 `using` 區塊會自動釋放 `Image` 物件，確保所有資源皆被正確釋放。

## 常見問題與解決方案

| 問題 | 原因 | 解決方式 |
|------|------|----------|
| **產生空白 PNG** | 未設定光柵化選項（例如缺少 `PageWidth`/`PageHeight`）。 | 確認 `CadRasterizationOptions` 定義了非零的畫布大小。 |
| **顏色不正確** | 背景色預設為白色，且原圖使用透明圖層。 | 設定 `rasterizationOptions.BackgroundColor = Color.Transparent;` |
| **大型 DWG 檔案效能低落** | 高解析度未使用分割。 | 使用 `rasterizationOptions.LayoutOptions` 限制渲染區域或降低 DPI。 |
| **授權例外** | 生產環境未使用有效授權。 | 在載入影像前加入 `License license = new License(); license.SetLicense("Aspose.CAD.lic");` 以套用授權。 |

## 常見問答

### Q1：Aspose.CAD 是否相容所有 CAD 檔案格式？
A1：Aspose.CAD 支援多種 CAD 檔案格式，包括 DWG、DXF、DGN 等。完整清單請參考[文件說明](https://reference.aspose.com/cad/net/)。

### Q2：我可以為不同專案自訂光柵化選項嗎？
A2：可以，Aspose.CAD 提供廣泛的光柵化設定，讓開發者依專案需求調整輸出。

### Q3：Aspose.CAD 有提供免費試用嗎？
A3：有，您可使用免費試用版探索功能。前往[此處](https://releases.aspose.com/)下載。

### Q4：如何取得 Aspose.CAD 的技術支援？
A4：請造訪 Aspose.CAD 的[支援論壇](https://forum.aspose.com/c/cad/19)取得協助。

### Q5：是否有臨時授權可供使用？
A5：有，開發者可從[此連結](https://purchase.aspose.com/temporary-license/)取得臨時授權。

### Q6：此方法也能 **convert DWG to PNG** 嗎？
A6：當然可以。相同程式碼適用於 DWG 檔，只需將來源檔案副檔名改為 `.dwg`。

### Q7：如何 **export DXF to image** 並使用透明背景？
A7：在儲存 PNG 前設定 `rasterizationOptions.BackgroundColor = Color.Transparent;`。

---

**最後更新：** 2026-03-19  
**測試環境：** Aspose.CAD 24.11 for .NET（最新發行版）  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}