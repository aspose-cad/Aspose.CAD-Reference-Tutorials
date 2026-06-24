---
date: 2026-03-29
description: 學習如何使用 Aspose.CAD for .NET 將 DGN 轉換為 PNG。本指南亦涵蓋 CAD 檔案格式支援以及完整的支援 DGN
  元素清單。
linktitle: Supported DGN Elements
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: 使用 Aspose.CAD for .NET 將 DGN 轉換為 PNG
url: /zh-hant/net/cad-features-and-support/supported-dgn-elements/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.CAD for .NET 將 DGN 轉換為 PNG

## 簡介

您是尋找無縫 **convert DGN to PNG** 的 .NET 開發人員嗎？Aspose.CAD for .NET 提供了強大的解決方案，可有效處理 DGN 檔案。在本教學中，我們將深入探討受支援的 DGN 元素，指導您使用 Aspose.CAD for .NET 的流程，並確切展示如何將這些元素匯出為 PNG 圖像。

## 快速解答
- **What does Aspose.CAD do?** 它可讀取、修改並將 CAD/BIM 檔案（包括 DGN）轉換為如 PNG 的點陣格式。  
- **Can I convert 2D and 3D DGN elements?** 是的——支援 2‑D 與 3‑D 兩種實體。  
- **Which .NET versions are required?** 需要 .NET Framework 4.5+、.NET Core 3.1+、.NET 5/6+。  
- **Do I need a license for testing?** 可使用免費試用版；正式環境需購買授權。  
- **Where do I get the library?** 從官方 Aspose 網站下載（連結如下）。

## 什麼是「convert DGN to PNG」？

將 DGN 轉換為 PNG 意味著將向量式 DGN 圖紙（2‑D 或 3‑D）渲染為點陣圖格式（PNG）。當您需要在網頁上顯示 CAD 圖紙、嵌入報告，或產生縮圖而不需 CAD 檢視器時，這非常有用。

## 為何使用 Aspose.CAD for .NET 來支援 CAD 檔案格式？

- **Full CAD file format support** – 支援 DGN、DWG、DXF、DWF 等多種格式。  
- **No external dependencies** – 純 .NET 函式庫，無需本機 CAD 安裝。  
- **High‑fidelity rendering** – 保留線寬、顏色與 3‑D 幾何形狀。  
- **Batch processing** – 可在伺服器端應用程式中輕鬆批次處理多個檔案。

## 先決條件

在開始之前，請確保您具備以下條件：

- 具備 .NET 程式設計的基本知識。  
- 電腦已安裝 Visual Studio。  
- Aspose.CAD for .NET 函式庫，您可從[此處](https://releases.aspose.com/cad/net/)下載。

## 匯入命名空間

為了快速啟動專案，請在 .NET 應用程式中匯入必要的命名空間。此步驟可確保您能使用 Aspose.CAD for .NET 提供的功能。

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Dgn;
using Aspose.CAD.FileFormats.Dgn.DgnElements;
```

## 如何將 DGN 轉換為 PNG

以下為逐步指南，說明如何載入 DGN 檔案、遍歷其元素、處理 2‑D 與 3‑D 實體，最後將結果匯出為 PNG 點陣圖。

### 步驟 1：載入 DGN 檔案

首先在 .NET 應用程式中將現有的 DGN 檔案載入為 `DgnImage`。

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Your code here
}
```

### 步驟 2：遍歷 DGN 元素

使用 `foreach` 迴圈遍歷 DGN 元素。Aspose.CAD for .NET 提供多種 DGN 元素類型供您使用。

```csharp
foreach (DgnDrawingElementBase element in dgnImage.Elements)
{
    // Your code here
}
```

### 步驟 3：處理先前支援的 2‑D 實體

這些實體現在亦支援 3‑D 渲染。switch 陳述式可根據元素類型分支處理邏輯。

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.Line:
    case DgnElementType.Ellipse:
    case DgnElementType.Curve:
    // Additional cases
        {
            // Your code here
            break;
        }
}
```

### 步驟 4：處理支援的 3‑D 實體

Aspose.CAD 為多個 3‑D DGN 元素提供完整支援。依需求擴充 switch 以處理這些元素。

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.SolidHeader3D:
    case DgnElementType.Cone:
    case DgnElementType.CellHeader:
        {
            // Your code here
            break;
        }
}
```

### 步驟 5：匯出並儲存為 PNG

完成必要的操作後，將 DGN 圖紙匯出為 PNG 點陣圖，並儲存至指定目錄。

```csharp
Console.WriteLine("\nThe DGN file exported successfully to raster image.\nFile saved at " + MyDir);
```

> **Pro tip:** 使用 `Image.Save` 搭配 `new PngOptions()` 以控制解析度、背景顏色及其他 PNG 專屬設定。

## CAD 檔案格式支援概覽

Aspose.CAD for .NET 不僅限於 DGN，亦支援 DWG、DXF、DWF 以及其他多種 CAD 格式，讓您只需一套 API 即可處理廣泛的工程圖紙。這使其成為需要跨多種標準提供 **CAD file format support** 的專案的理想選擇。

## 常見問題與解決方案

| 問題 | 原因 | 解決方案 |
|-------|--------|-----|
| **Image appears blank** | 以零 DPI 匯出 | 在 `PngOptions` 中指定 `ResolutionX` 和 `ResolutionY`。 |
| **Missing 3‑D geometry** | 在 switch 中未處理此元素類型 | 加入缺少的 `DgnElementType` case 並相應渲染。 |
| **Out‑of‑memory on large files** | 一次載入整個檔案 | 分批處理元素或在可能時使用串流方式。 |

## 常見問答

### Q1：在哪裡可以找到 Aspose.CAD for .NET 的文件？

A1：您可在[此處](https://reference.aspose.com/cad/net/)找到文件。

### Q2：如何下載 Aspose.CAD for .NET？

A2：您可從[此處](https://releases.aspose.com/cad/net/)下載函式庫。

### Q3：是否提供 Aspose.CAD for .NET 的免費試用？

A3：是的，您可在[此處](https://releases.aspose.com/)取得免費試用。

### Q4：在哪裡可以取得 Aspose.CAD for .NET 的臨時授權？

A4：臨時授權可在[此處](https://purchase.aspose.com/temporary-license/)取得。

### Q5：需要協助或有任何問題？

A5：請前往 Aspose.CAD for .NET 社群的[支援論壇](https://forum.aspose.com/c/cad/19)。

---

**最後更新：** 2026-03-29  
**測試環境：** Aspose.CAD for .NET 24.11  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}