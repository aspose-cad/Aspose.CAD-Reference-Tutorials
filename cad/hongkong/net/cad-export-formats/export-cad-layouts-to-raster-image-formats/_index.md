---
date: 2026-03-21
description: 了解如何使用 Aspose.CAD for .NET 將 DXF 轉換為 PNG 及其他點陣圖格式。請依照我們的逐步指南，輕鬆完成 CAD
  圖層的無縫匯出。
linktitle: Export CAD Layouts to Raster Image Formats
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: 使用 Aspose.CAD for .NET 將 DXF 轉換為 PNG
url: /zh-hant/net/cad-export-formats/export-cad-layouts-to-raster-image-formats/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 Aspose.CAD for .NET 中將 CAD 版面匯出為點陣圖格式

## 介紹

您是否想要使用 Aspose.CAD for .NET 高效地 **convert dxf to png** 以及其他點陣圖格式？本步驟說明指南將帶您逐步完成整個流程，提供詳細說明與程式碼片段，讓任務變得順暢。無論您是資深開發者還是 Aspose.CAD 的新手，本教學皆適用於各種程度。

### 快速回答
- **哪個函式庫負責轉換？** Aspose.CAD for .NET  
- **預設支援的主要格式？** JPEG、PNG、BMP 與 TIFF 點陣圖  
- **可以匯出特定 CAD 圖層嗎？** 可以 – 使用 `CadRasterizationOptions.Layers` 針對單一圖層  
- **正式環境需要授權嗎？** 非試用使用時必須擁有有效的 Aspose.CAD 授權  
- **支援的 .NET 版本？** .NET Framework 4.5 以上、.NET Core 3.1 以上、.NET 5/6/7  

## 什麼是 **convert dxf to png**？

將 DXF（Drawing Exchange Format）檔案轉換為 PNG，即將向量式 CAD 資料光柵化為像素圖像。當您需要在網頁、報告或任何僅支援點陣圖的環境中嵌入 CAD 圖紙時，這項功能非常實用。

## 為什麼要分別匯出 CAD 圖層？

個別匯出 CAD 圖層可讓您對視覺輸出擁有更細緻的控制，減少每張圖像的檔案大小，並能針對特定圖層套用樣式或後處理。對於大型工程圖紙，僅有部分圖層對特定觀眾有意義時，此方式尤為便利。

## 前置需求

在開始教學之前，請確保您已具備以下項目：

- **Aspose.CAD for .NET Library** – 從 [Aspose.CAD website](https://releases.aspose.com/cad/net/) 下載。  
- **CAD 圖紙檔案** – 例如 `conic_pyramid.dxf`，即您想要轉換為點陣圖的 DXF 檔案。  

## 匯入命名空間

在 .NET 專案中，匯入必要的命名空間以使用 Aspose.CAD 功能。請在程式碼開頭加入以下命名空間：

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## 如何 **convert dxf to png** – 步驟說明

### 步驟 1：載入 CAD 圖紙

先將 DXF 檔案載入至 `Image` 物件。此物件在記憶體中代表整個 CAD 圖紙。

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

// Load a CAD drawing in an instance of Image
using (var image = Image.Load(sourceFilePath))
{
    // Your code for loading the CAD drawing goes here
}
```

### 步驟 2：建立 `CadRasterizationOptions`

設定光柵化選項，例如輸出尺寸與解析度。這些選項決定向量資料如何被光柵化。

```csharp
// Create an instance of CadRasterizationOptions
var rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
```

### 步驟 3：指定圖層（匯出 CAD 圖層）

若只需要特定圖層，請在此列出其名稱。此範例示範 **export cad layers** 的個別匯出方式。

```csharp
// Add the layer name to the CadRasterizationOptions's layer list
rasterizationOptions.Layers = new string[] { "LayerA" };
```

### 步驟 4：選擇影像格式 – 將 CAD 儲存為 PNG（或 JPEG）

建立針對影像格式的選項物件。當您想要 **save cad as png** 時，將 `JpegOptions` 換成 `PngOptions`。

```csharp
// Create an instance of JpegOptions (or any ImageOptions for raster formats)
var options = new JpegOptions();
options.VectorRasterizationOptions = rasterizationOptions;
```

> **專業提示：** 若要產生 PNG 檔案，只需實例化 `new PngOptions()`，不必使用 `JpegOptions`。

### 步驟 5：匯出為 JPEG（或 PNG）格式

最後，將光柵化後的影像儲存至磁碟。副檔名會決定輸出格式。

```csharp
// Export each layer to Jpeg format
MyDir = MyDir + "CADLayersToRasterImageFormats_out.jpg";
image.Save(MyDir, options);
```

當您將 `JpegOptions` 換成 `PngOptions`，相同程式碼即可 **convert dxf to png**，並產生 `.png` 檔案。

### 其他步驟：匯出所有圖層

如果您需要 **convert cad to raster** 每一個圖層，請呼叫下方的輔助方法。它會遍歷所有圖層，並將每個圖層另存為獨立影像。

```csharp
ConvertAllLayersToRasterImageFormats();
```

> *注意：* `ConvertAllLayersToRasterImageFormats` 的實作屬於完整的 Aspose.CAD 範例套件，示範圖層的批次處理。

## 常見問題與疑難排解

| 症狀 | 可能原因 | 解決方式 |
|------|----------|----------|
| 影像全白或空白 | 未設定光柵化選項（例如 `PageWidth`/`PageHeight` 為 0） | 確認 `PageWidth` 與 `PageHeight` 為正值 |
| 缺少圖層 | `Layers` 陣列中的圖層名稱錯誤 | 核對 CAD 檔案中的圖層名稱（區分大小寫） |
| PNG 解析度低 | 預設 DPI 較低 | 設定 `rasterizationOptions.Resolution = 300;` 提升品質 |

## 常見問答（原文）

### Q1：可以使用其他影像格式匯出嗎？

A1：可以。只要將 `JpegOptions` 換成目標格式的選項，例如 `PngOptions` 或 `BmpOptions`。

### Q2：有提供試用版嗎？

A2：有，您可在此下載 Aspose.CAD 試用版 [here](https://releases.aspose.com/)。

### Q3：如何取得 Aspose.CAD 的支援？

A3：前往 Aspose.CAD [forum](https://forum.aspose.com/c/cad/19) 取得社群支援，或購買授權以獲得專屬技術支援。

### Q4：是否提供臨時授權？

A4：有，您可在此取得臨時授權 [here](https://purchase.aspose.com/temporary-license/)。

### Q5：文件在哪裡可以找到？

A5：請參考詳細文件 [here](https://reference.aspose.com/cad/net/)。

## 其他 FAQ

**Q：可以一次指令匯出所有圖層嗎？**  
A：可以，使用上方示範的 `ConvertAllLayersToRasterImageFormats` 方法。

**Q：Aspose.CAD 支援向量格式如 SVG 嗎？**  
A：主要針對點陣圖格式，但您可以匯出為保留向量資料的 PDF。

**Q：如何控制匯出 PNG 的背景顏色？**  
A：在儲存前將 `rasterizationOptions.BackgroundColor` 設為所需的 `Color`。

**Q：能否只匯出單一版面而非整個圖紙？**  
A：可以，設定 `rasterizationOptions.Layouts` 以指定要光柵化的版面名稱。

## 結論

您現在已學會如何 **convert dxf to png**、**export cad layers**，以及使用 Aspose.CAD for .NET **save cad as png** 或 JPEG。只要調整 `CadRasterizationOptions` 並切換影像格式選項，即可依需求客製化任意點陣圖輸出。探索 Aspose.CAD API 中的其他格式選項，擴展您的 CAD 轉點陣工作流程。

---

**最後更新：** 2026-03-21  
**測試環境：** Aspose.CAD for .NET 24.11（撰寫時最新版本）  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}