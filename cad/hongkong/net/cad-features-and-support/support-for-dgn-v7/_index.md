---
date: 2026-03-29
description: 學習如何使用 Aspose.CAD for .NET 將 DGN 轉換為 JPEG，全面支援 DGN V7，讓您輕鬆將 CAD 轉換為點陣圖像。
linktitle: Support for DGN V7
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: 使用 Aspose.CAD for .NET 將 DGN 轉換為 JPEG – V7 支援
url: /zh-hant/net/cad-features-and-support/support-for-dgn-v7/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.CAD for .NET 轉換 DGN 為 JPEG – 支援 V7

## 介紹

在本教學中，您將學習如何使用 Aspose.CAD for .NET **將 DGN 轉換為 JPEG**，充分利用該函式庫完整的 DGN V7 支援。將 DGN 檔案轉換為 JPEG 等點陣圖像是常見需求，尤其在需要將 CAD 圖紙嵌入網頁、行動應用程式或報告工具時。Aspose.CAD 亦可高效 **將 CAD 轉換為點陣圖** 格式，讓您在呈現設計資料時更具彈性。

## 快速解答
- **本教學涵蓋什麼內容？** 使用 Aspose.CAD for .NET 將 DGN V7 檔案轉換為 JPEG 點陣圖像。  
- **需要哪個函式庫版本？** 任何包含 DGN V7 支援的近期 Aspose.CAD for .NET 版本皆可。  
- **我需要授權嗎？** 開發階段可使用免費試用版；正式上線需購買商業授權。  
- **我可以更改輸出尺寸嗎？** 是 – 點陣化選項允許您設定頁面寬度、高度與縮放比例。  
- **JPEG 是唯一的輸出格式嗎？** 否 – Aspose.CAD 支援多種點陣格式（PNG、BMP、TIFF 等）。

## 什麼是 DGN V7？
DGN（Design）是一種最初由 Bentley Systems 為 MicroStation 開發的檔案格式。第 7 版加入了更豐富的幾何資訊與中繼資料，因而在土木工程與基礎建設專案中廣受青睞。Aspose.CAD for .NET 能直接讀取 DGN V7 檔案，將其內容以 `CadImage` 物件呈現，您可以將其點陣化或轉換為其他格式。

## 為什麼要將 DGN 轉換為 JPEG？
- **適合網頁使用：** JPEG 圖片檔案輕巧，能即時在瀏覽器中顯示，無需額外插件。  
- **跨平台：** JPEG 可在任何裝置上檢視，適合將 CAD 圖紙分享給非技術相關人員。  
- **簡化工作流程：** 轉換為點陣格式後，後續流程不再需要 CAD 專用檢視器。

## 前置條件

在開始實作之前，請確保您已具備以下項目：

- **Aspose.CAD for .NET** – 從 [website](https://releases.aspose.com/cad/net/) 下載。  
- **開發環境** – Visual Studio（或任何支援 .NET 的 IDE）。  

具備上述條件即可順利依照步驟操作，不會中斷。

## 匯入命名空間

首先匯入處理 CadImage 與點陣化所需的命名空間。

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## 步驟 1：載入 DGN 檔案

將來源 DGN 檔案載入為 `CadImage` 物件。請將佔位路徑替換為實際存放 DGN 檔案的資料夾路徑。

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Subsequent steps will be placed here.
}
```

## 步驟 2：設定點陣化選項

定義 DGN 圖紙的點陣化方式。您可以控制輸出尺寸與縮放行為。

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions
{
    PageWidth = 600,
    PageHeight = 300,
    NoScaling = true,
    AutomaticLayoutsScaling = false
};
```

## 步驟 3：設定向量點陣化選項

建立 `JpegOptions` 物件（或其他點陣格式選項），並套用點陣化設定。

```csharp
ImageOptionsBase options = new JpegOptions
{
    VectorRasterizationOptions = rasterizationOptions
};
```

## 步驟 4：儲存點陣化圖像

最後，使用 `Save` 方法將 DGN 圖紙匯出為 JPEG 檔案。

```csharp
cadImage.Save(MyDir + "ExportDGNToRasterImage_out.jpeg", options);
```

程式執行成功後，您會在指定的資料夾中看到原始 DGN V7 圖紙的 JPEG 版本。

## 常見問題與解決方案

| 問題 | 解決方案 |
|-------|----------|
| **找不到檔案** | 確認 `MyDir` 以路徑分隔符（`\\` 或 `/`）結尾，且檔名正確。 |
| **輸出圖像為空白** | 確保 `NoScaling` 設定正確；若希望圖紙填滿頁面，請將其設為 `false`。 |
| **不支援的實體** | Aspose.CAD 支援大多數 DGN 實體，但極舊或自訂物件可能會被忽略。請檢查轉換日誌以取得警告訊息。 |

## 常見問答

### Q1：Aspose.CAD 是否相容於最新的 DGN V7 規範？

**A：** 是，Aspose.CAD 完全支援 DGN V7，能依照最新標準處理幾何與中繼資料。

### Q2：我可以自訂 DGN 檔案轉換的點陣化選項嗎？

**A：** 當然可以。`CadRasterizationOptions` 類別允許您調整頁面大小、縮放、線寬、背景顏色等設定。

### Q3：除了 JPEG，還支援其他輸出格式嗎？

**A：** 是，Aspose.CAD 可匯出為 PNG、BMP、TIFF 以及其他多種點陣格式。只需使用相對應的 `*Options` 類別（例如 `PngOptions`）。

### Q4：我如何取得 Aspose.CAD 相關問題的協助？

**A：** 前往 [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) 取得社群支援與官方回覆。

### Q5：是否提供 Aspose.CAD for .NET 的免費試用？

**A：** 是，您可從 [here](https://releases.aspose.com/) 下載試用版。

---

**最後更新：** 2026-03-29  
**測試版本：** Aspose.CAD 24.12 for .NET  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}