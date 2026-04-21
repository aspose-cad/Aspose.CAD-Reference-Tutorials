---
date: 2026-03-29
description: 了解如何設定 CAD 光柵化選項，並使用 Aspose.CAD for .NET 將 DGN 匯出為具備 3D 支援的 PDF。
linktitle: Support of 3D for DGN V7
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: 為 DGN V7 3D 設定 CAD 光柵化選項
url: /zh-hant/net/cad-features-and-support/support-of-3d-for-dgn-v7/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 設定 DGN V7 3D 的 CAD 光柵化選項

## 介紹

在本完整教學中，您將學習 **如何設定 CAD 光柵化選項**，以使用 Aspose.CAD for .NET 將 3‑D DGN V7 檔案匯出為 PDF。無論您是構建 CAD 檢視器、報告工具，或自動化轉換管線，精通這些設定即可讓您精確控制頁面大小、版面縮放、背景顏色以及想要渲染的特定視圖。讓我們一步一步完成此過程。

## 快速解答
- **什麼是「設定 CAD 光柵化選項」？**  
  它指的是在將 CAD 檔案轉換為光柵格式（例如 PDF）之前，設定頁面尺寸、縮放、背景顏色與版面選擇等屬性。
- **如何在支援 3‑D 的情況下將 DGN 匯出為 PDF？**  
  使用 `DgnImage` 載入 DGN，定義 `PdfOptions` + `CadRasterizationOptions`，然後呼叫 `Save`。
- **生產環境是否需要授權？**  
  是的——部署時需要商業授權；亦提供免費試用版。
- **支援哪些 .NET 版本？**  
  .NET Framework 4.5 以上、.NET Core 3.1 以上、.NET 5/6/7。
- **我可以選擇特定視圖匯出嗎？**  
  當然可以——在光柵化選項中設定 `Layouts` 陣列。

## 什麼是「設定 CAD 光柵化選項」？

設定 CAD 光柵化選項是指自訂 CAD 圖紙的光柵化方式（將向量轉換為點陣圖或 PDF）。透過調整這些設定，您可以控制最終文件的視覺輸出、效能與檔案大小。

## 為何使用 Aspose.CAD 進行 3‑D DGN V7 匯出？

- **完整的 .NET 整合** – 無需 COM 或原生 DLL。  
- **支援 3‑D 幾何** – 在渲染至 PDF 時保留深度資訊。  
- **細緻的控制** – 可精確選擇版面、縮放與背景顏色。  
- **跨平台** – 可於 Windows、Linux 與 macOS 上搭配 .NET Core 使用。

## 前置條件

在開始之前，請確保您已擁有：

- **Aspose.CAD for .NET** – 從 [here](https://releases.aspose.com/cad/net/) 下載。  
- **Visual Studio** 或任何相容的 .NET IDE。  
- **範例 DGN 檔案** – 本教學將使用 `Nikon_D90_Camera.dgn`（包含於 Aspose 範例套件中）。  

所有準備就緒後，讓我們深入程式碼。

## 匯入命名空間

在您的 .NET 專案中，匯入所需的命名空間：

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Dgn;
using Aspose.CAD.ImageOptions;
```

## 步驟 1：設定文件目錄

建立一個變數，指向存放來源 DGN 與輸出檔案的資料夾。

```csharp
string MyDir = "Your Document Directory";
```

## 步驟 2：載入 DGN 檔案

將 DGN 檔案載入為 `DgnImage`。此物件讓您存取 CAD 資料與光柵化流程。

```csharp
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";
string outFile = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Your code for further processing goes here
}
```

## 步驟 3：設定 PDF 匯出選項（設定 CAD 光柵化選項）

在此我們 **設定 CAD 光柵化選項**，決定 3‑D 模型如何渲染為 PDF。您可以調整頁面大小、啟用自動版面縮放、設定背景顏色，並挑選要匯出的精確版面（視圖）。

```csharp
var options = new PdfOptions
{
    VectorRasterizationOptions = new CadRasterizationOptions
    {
        PageWidth = 1500,
        PageHeight = 1500,
        AutomaticLayoutsScaling = true,
        BackgroundColor = Color.Black,
        Layouts = new string[] { "1", "2", "3", "9" } // Only export specified views
    }
};
```

## 步驟 4：儲存光柵圖像

最後，使用剛才設定的選項將 DGN 匯出為 PDF 檔案。

```csharp
dgnImage.Save(outFile, options);
```

## 常見問題與解決方案

| 問題 | 解決方案 |
|-------|----------|
| **PDF 輸出空白** | 驗證 `Layouts` 陣列包含 DGN 檔案中存在的正確視圖識別碼。 |
| **顏色不正確** | 確保 `BackgroundColor` 設為所需的值；若需淺色背景，使用 `Color.White`。 |
| **大型檔案的效能瓶頸** | 啟用 `AutomaticLayoutsScaling`，並考慮減少 `PageWidth/PageHeight` 以降低光柵解析度。 |
| **授權例外** | 在載入影像前安裝有效的 Aspose.CAD 授權，以避免試用水印。 |

## 常見問答

**Q: 我可以在 .NET 使用 Aspose.CAD 處理其他 CAD 檔案格式嗎？**  
A: 可以，Aspose.CAD 支援 DWG、DXF、DWF、DGN 等多種格式。

**Q: 在使用 Aspose.CAD 時，如何處理例外情況？**  
A: 將程式碼包在 `try‑catch` 區塊中，並檢查 `Aspose.CAD.CADException` 以取得詳細錯誤資訊。

**Q: Aspose.CAD 適合商業專案嗎？**  
A: 絕對適合。您可於 [here](https://purchase.aspose.com/buy) 購買授權。

**Q: 我可以在購買前試用 Aspose.CAD for .NET 嗎？**  
A: 可以，免費試用版可在 [here](https://releases.aspose.com/) 取得。

**Q: 我該去哪裡取得 Aspose.CAD 的社群支援？**  
A: 前往討論論壇 [here](https://forum.aspose.com/c/cad/19) 加入討論。

**最後更新：** 2026-03-29  
**測試版本：** Aspose.CAD 24.11 for .NET  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}