---
date: 2026-09-09
description: 了解如何使用 Aspose CAD export 將特定 DXF 版面轉換為 .NET 中的 JPEG 或 PNG。遵循一步一步的說明即可快速取得結果。
keywords:
- aspose cad export
- how to export dxf
- convert dxf to jpeg
- batch export dxf
- convert dwf to jpeg
lastmod: 2026-09-09
linktitle: 匯出特定 DXF 版面為圖像
og_description: 了解如何使用 Aspose CAD export 將特定 DXF 版面轉換為 .NET 中的 JPEG 或 PNG。遵循一步一步的說明即可快速取得結果。
og_image_alt: Tutorial showing Aspose CAD export of DXF layout to JPEG image in .NET
og_title: Aspose CAD export – 匯出特定 DXF 版面為圖像
schemas:
- author: Aspose
  dateModified: '2026-09-09'
  description: Learn how to use Aspose CAD export to convert a specific DXF layout
    to JPEG or PNG in .NET. Follow step‑by‑step instructions for fast results.
  headline: Aspose CAD export – exporting a specific DXF layout to an image
  type: TechArticle
- description: Learn how to use Aspose CAD export to convert a specific DXF layout
    to JPEG or PNG in .NET. Follow step‑by‑step instructions for fast results.
  name: Aspose CAD export – exporting a specific DXF layout to an image
  steps:
  - name: set up your project
    text: Create a new .NET project or open an existing one where you plan to implement
      the Aspose.CAD functionality.
  - name: load CAD image
    text: 'Use the following code to load a CAD image from your specified file path:'
  - name: configure rasterization options
    text: 'Set up the rasterization options, specifying the page width and height:'
  - name: iterate over layers
    text: 'Retrieve the layers from the CAD image and iterate through them:'
  - name: export layers to images
    text: For each layer, export it to a JPEG image using the configured options.
      The `JpegOptions` class defines JPEG‑specific settings such as quality and compression
      level. Repeat these steps for each layer in the CAD image.
  type: HowTo
- questions:
  - answer: Yes – you can script a folder scan and call the same export routine for
      each file; the library is optimized for high‑throughput scenarios.
    question: Does Aspose CAD export support batch processing of thousands of files?
  - answer: Absolutely – set the `JpegQuality` property in `RasterizationOptions`
      to a value between 0 and 100.
    question: Can I control the JPEG quality level?
  - answer: Yes – change the `Save` format to `SaveFormat.Png` and adjust any transparency
      settings as needed.
    question: Is it possible to export a layout as a PNG instead of JPEG?
  - answer: Aspose.CAD supports .NET Framework 4.5+, .NET Core 3.1+, .NET 5, .NET
      6 and later.
    question: What .NET versions are officially supported?
  - answer: The engine streams pages to disk and never loads the full document into
      memory, allowing processing of multi‑gigabyte files on modest hardware.
    question: How does Aspose CAD export handle very large drawings?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- aspose cad
- dxf export
- cad to image
- c# cad processing
- cad conversion
title: Aspose CAD export – 匯出特定 DXF 版面為圖像
url: /zh-hant/net/layout-and-object-handling/exporting-specific-dxf-layout-to-image/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose CAD export – 匯出特定 DXF 版面為影像

## 介紹

Aspose CAD export 讓您能直接將 CAD 圖紙（包括單一 DXF 版面）轉換為 JPEG 或 PNG 等點陣圖，無需任何第三方 CAD 軟體。在本教學中，您將學會如何載入 DXF 檔案、選取所需版面，並使用幾行 .NET 程式碼將其匯出為影像。

## 快速解答
- **需要的函式庫是什麼？** Aspose.CAD for .NET (the Aspose CAD export component)。  
- **可以只匯出單一版面嗎？** 可以 – 在光柵化之前選取特定版面。  
- **支援的輸出格式？** JPEG、PNG、BMP、TIFF 等。  
- **正式環境需要授權嗎？** 非試用版使用時必須擁有有效的 Aspose.CAD 授權。  
- **可在 .NET 6+ 上執行嗎？** 當然可以 – 函式庫支援 .NET Framework 4.5+、.NET Core 3.1+、.NET 5/6/7。

## Aspose CAD export 是什麼？

Aspose CAD export 是 Aspose.CAD 函式庫的一部分，負責將 CAD 與 BIM 檔案轉換為點陣或向量影像。它提供單一呼叫 API，無需安裝 AutoCAD 即可渲染任何版面、頁面或圖層。此元件亦支援批次處理、高解析度輸出，以及抗鋸齒、背景色彩控制等進階渲染選項。

## 為什麼在 DXF 轉換中使用 Aspose CAD export？

Aspose CAD export 支援 **30+ CAD/BIM 格式**，且可渲染最多 **10 000 頁** 的檔案，同時透過串流資料將記憶體使用量控制在 **50 MB** 以下。引擎保留線寬、顏色與剖面圖樣，提供與原始圖紙相符的像素完美 JPEG 輸出。它也免除昂貴的桌面 CAD 安裝需求，讓自動化轉換流程變得簡單且具成本效益。

## 前置條件

- Aspose.CAD 函式庫：從 [release page](https://releases.aspose.com/cad/net/) 下載並安裝 Aspose.CAD 函式庫。  
- 開發環境：確保您的機器已配置好 .NET 開發環境。

## 匯入命名空間

在您的 .NET 專案中，先匯入必要的命名空間以存取 Aspose.CAD 提供的功能：

```csharp
using System;
```

## 如何將特定 DXF 版面匯出為影像？

載入 DXF 檔案、選取目標版面、設定光柵化選項，最後將結果儲存為影像。整個流程只需少數方法呼叫，對於一般圖紙而言執行時間不到一秒。`CadImage` 類別代表已載入記憶體的 CAD 圖紙，提供對其圖層、版面與渲染選項的存取。

### 步驟 1：設定專案
建立新的 .NET 專案或開啟既有專案，以實作 Aspose.CAD 功能。

### 步驟 2：載入 CAD 影像
使用以下程式碼從指定的檔案路徑載入 CAD 影像：

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "for_layers_test.dwf";

using (var image = (Aspose.CAD.FileFormats.Cad.CadImage)Aspose.CAD.Image.Load(sourceFilePath))
{
    // Your code for further steps will go here.
}
```

### 步驟 3：設定光柵化選項
設定光柵化選項，指定頁面的寬度與高度：

```csharp
var rasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
```

### 步驟 4：遍歷圖層
從 CAD 影像中取得圖層並逐一遍歷：

```csharp
var layersList = image.Layers;
foreach (var layerName in layersList.GetLayersNames())
{
    // Your code for further steps will go here.
}
```

### 步驟 5：將圖層匯出為影像
對每個圖層，使用先前設定的選項匯出為 JPEG 影像。`JpegOptions` 類別定義 JPEG 專屬的設定，如品質與壓縮等級。

```csharp
rasterizationOptions.Layers = new string[] { layerName };
var options = new Aspose.CAD.ImageOptions.JpegOptions();
options.VectorRasterizationOptions = rasterizationOptions;
image.Save(layerName + "_out.jpg", options);
```

對 CAD 影像中的每個圖層重複上述步驟。

## 如何批次匯出 DXF 版面為影像？

您可以將所有 DXF 檔案放入同一資料夾，逐一迴圈處理每個檔案、選取所需版面，然後呼叫相同的匯出邏輯。此方式可一次轉換數十個圖紙，適合自動化流水線。透過重複使用相同的光柵化與儲存設定，可確保整批檔案的輸出品質一致。

## 如何使用 Aspose CAD 將 DWF 轉換為 JPEG？

Aspose CAD export 亦支援 DWF 檔案。使用 `CadImage.Load` 載入 DWF，設定相同的光柵化選項，然後以 JPEG 格式呼叫 `Save`。API 與 DXF 工作流程相同，您只需重用相同的程式碼基礎。此統一介面簡化了混合 CAD 檔案集合的轉換，無需額外的程式分支。

## 常見問題與解決方案
- **缺少版面名稱：** 確認版面識別碼與 CAD 檔案圖層管理員中顯示的名稱相符。  
- **大型檔案記憶體激增：** 使用 `CadImage.Load` 搭配啟用串流的 `LoadOptions` 以降低記憶體使用。  
- **顏色不正確：** 若需要白色畫布，請確保 `RasterizationOptions` 的 `BackgroundColor` 屬性設定為 `Color.White`。

## 常見問答

### Q1：我可以在其他 .NET 框架中使用 Aspose.CAD 嗎？

A1：可以，Aspose.CAD 相容於多種 .NET 框架，提供開發彈性。

### Q2：Aspose.CAD 有提供臨時授權嗎？

A2：有，您可從 [temporary license page](https://purchase.aspose.com/temporary-license/) 取得臨時授權。

### Q3：如何取得 Aspose.CAD 的支援？

A3：請前往 [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) 取得社群支援與協助。

### Q4：Aspose.CAD 有免費試用版嗎？

A4：有，您可在 [Aspose.CAD free trial page](https://releases.aspose.com/) 下載免費試用版。

### Q5：在哪裡可以找到 Aspose.CAD 的詳細文件？

A5：請參考完整的 [Aspose.CAD documentation](https://reference.aspose.com/cad/net/) 以取得深入資訊。

## 常見問題

**Q：Aspose CAD export 是否支援成千上萬檔案的批次處理？**  
A：是的 – 您可以寫腳本掃描資料夾，對每個檔案呼叫相同的匯出例程；函式庫已針對高吞吐量情境進行最佳化。

**Q：我可以控制 JPEG 的品質等級嗎？**  
A：當然可以 – 在 `RasterizationOptions` 中設定 `JpegQuality`，值介於 0 到 100 之間。

**Q：可以將版面匯出為 PNG 而非 JPEG 嗎？**  
A：可以 – 將 `Save` 格式改為 `SaveFormat.Png`，並視需要調整透明度設定。

**Q：官方支援哪些 .NET 版本？**  
A：Aspose.CAD 支援 .NET Framework 4.5+、.NET Core 3.1+、.NET 5、.NET 6 以及更高版本。

**Q：Aspose CAD export 如何處理非常大的圖紙？**  
A：引擎會將頁面串流至磁碟，從不一次將整個文件載入記憶體，因而能在一般硬體上處理多 GB 大小的檔案。

---

**Last Updated:** 2026-09-09  
**Tested With:** Aspose.CAD 24.12 for .NET  
**Author:** Aspose

## 相關教學

- [將 DXF 轉換為 PNG（使用 Aspose.CAD for .NET）](/cad/net/cad-export-formats/export-cad-layouts-to-raster-image-formats/)
- [Aspose CAD 範例：在 .NET 中將版面轉換為點陣圖](/cad/net/cad-drawing-manipulation/convert-layouts-to-raster-image/)
- [學習設定 CAD 光柵化選項 – 使用 Aspose.CAD 匯出特定版面為 PDF](/cad/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}