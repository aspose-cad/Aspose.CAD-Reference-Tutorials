---
date: 2026-03-21
description: 了解如何在 .NET 中使用 Aspose.CAD 獲取 CAD 版面大小。請遵循我們的逐步指南，以高效操作 CAD 檔案。
linktitle: Get Size of CAD Layout
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: 在 Aspose.CAD for .NET 中取得 CAD 版面尺寸
url: /zh-hant/net/cad-drawing-manipulation/get-size-of-cad-layout/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 Aspose.CAD for .NET 中取得 CAD 版面大小

## 簡介

## 快速答案
- **「取得 CAD 版面大小」是什麼意思？** 它指的是取得 CAD 檔案中每個非空版面的寬度與高度（以圖形單位表示）。  
- **哪個函式庫支援此功能？** Aspose.CAD for .NET 提供簡易的 API 以存取版面資訊。  
- **需要授權嗎？** 免費試用版可用於評估；正式使用則需購買商業授權。  
- **支援的格式？** 完全支援 DWG、DXF 以及其他多種 CAD/BIM 格式。  
- **一般實作時間？** 基本的大小取得例程大約需要 10‑15 分鐘。

## 什麼是「取得 CAD 版面大小」？
取得 CAD 版面大小是指擷取 CAD 圖面中每個版面（紙張空間）的幾何範圍。這些範圍以圖面的原生單位（通常為毫米或英吋）表示，對於縮放、列印或產生預覽圖等工作非常有用。

## 為什麼使用 Aspose.CAD 取得 CAD 版面大小？
- **不需要 CAD 軟體** – 完全在伺服器端執行。  
- **跨平台** – 支援 .NET Framework、.NET Core 以及 .NET 5/6+。  
- **精確測量** – 直接回傳檔案中儲存的實際範圍，避免手動解析。  
- **易於整合** – 簡單的 API 呼叫可自然嵌入現有的 C# 專案。

## 前置條件

在開始撰寫程式碼之前，請先確保具備以下項目：

- 已安裝 Aspose.CAD for .NET。可從 [Aspose.CAD for .NET 下載頁面](https://releases.aspose.com/cad/net/) 下載。  
- 一個或多個欲分析的 CAD 檔案（DWG、DXF 等）。本教學示範使用 `conic_pyramid.dxf` 與 `Bottom_plate.dwg` 作為範例檔案。

## 匯入命名空間

在 .NET 專案中，先匯入所需的命名空間：

```csharp
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.ImageOptions;
```

## 步驟 1：設定文件目錄

定義存放 CAD 檔案的資料夾。將佔位字串替換為您機器上的實際路徑。

```csharp
string MyDir = "Your Document Directory";
```

## 步驟 2：指定 CAD 檔案路徑

建立一個陣列，指向每個要處理的 CAD 檔案。

```csharp
string[] sourceFilePaths = new[]
{
    MyDir + "conic_pyramid.dxf",
    MyDir + "Bottom_plate.dwg"
};
```

## 步驟 3：遍歷 CAD 檔案

載入每個檔案，偵測其格式，並準備擷取版面資訊。

```csharp
foreach (var sourceFilePath in sourceFilePaths)
{
    string extension = Path.GetExtension(sourceFilePath);
    using (CadImage cadImage = (CadImage)Aspose.CAD.Image.Load(sourceFilePath))
    {
        // ... (continue to the next step)
    }
}
```

## 步驟 4：取得非空版面

我們需要一個輔助方法，只回傳實際包含繪圖實體的版面。空版面會被忽略，因為它們沒有可報告的大小。

```csharp
private static List<string> GetNotEmptyLayouts(Image cadImage, string extension)
{
    // ... (continue to the next step)
}
```

## 步驟 5：取得 DWG 檔案的版面

DWG 檔案將版面資訊儲存在 `HeaderVariables` 表格中。以下方法可擷取 DWG 圖面中所有非空版面的名稱。

```csharp
private static List<string> GetNotEmptyLayoutsForDwg(CadImage cadImage)
{
    // ... (continue to the next step)
}
```

## 步驟 6：取得 DXF 檔案的版面

DXF 檔案使用不同的結構。此方法會解析 `Tables` 集合，以找出包含實體的紙張空間版面。

```csharp
private static List<string> GetNotEmptyLayoutsForDxf(CadImage cadImage)
{
    // ... (continue to the next step)
}
```

## 步驟 7：取得版面大小並儲存為影像

最後，遍歷每個已發現的版面，讀取其範圍，並可選擇將版面渲染為影像檔案以供視覺驗證。

```csharp
foreach (string layout in layouts)
{
    // ... (continue to the next step)
}
```

## 常見問題與技巧

- **缺少版面名稱**：確認 CAD 檔案實際包含紙張空間版面；有些檔案僅有模型空間。  
- **單位不正確**：大小以圖面的原生單位回傳，必要時請轉換為毫米或英吋。  
- **效能**：載入極大型的 DWG/DXF 檔案可能佔用大量記憶體；建議以非同步或批次方式處理檔案。

## 常見問答

**Q: Aspose.CAD 是否相容所有 CAD 檔案格式？**  
A: 是的，Aspose.CAD 支援多種格式，包括 DWG、DXF、DGN 以及許多 BIM 檔案類型。

**Q: 我可以自訂影像儲存選項嗎？**  
A: 當然可以！您可以調整 `CadRasterizationOptions`（格式、解析度、背景顏色等）以符合您的需求。

**Q: 我在哪裡可以找到更多文件？**  
A: 請參考 [Aspose.CAD 文件](https://reference.aspose.com/cad/net/)，內含詳細的 API 參考與更多範例。

**Q: 有提供免費試用嗎？**  
A: 有，您可以透過 [免費試用](https://releases.aspose.com/) 來體驗 Aspose.CAD。

**Q: 我要如何取得技術支援？**  
A: 請前往 [Aspose.CAD 論壇](https://forum.aspose.com/c/cad/19) 獲得技術支援。

---

**最後更新：** 2026-03-21  
**測試環境：** Aspose.CAD 24.11 for .NET  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}