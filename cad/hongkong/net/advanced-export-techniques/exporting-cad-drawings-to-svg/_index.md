---
title: 將 CAD 繪圖匯出為 SVG 格式 - Aspose.CAD Guide
linktitle: 將 CAD 繪圖匯出為 SVG 格式
second_title: Aspose.CAD .NET - CAD 和 BIM 檔案格式
description: 探索使用 Aspose.CAD for .NET 將 CAD 繪圖匯出為 SVG 的無縫流程。透過靈活性和自訂增強您的 CAD 開發。
weight: 15
url: /zh-hant/net/advanced-export-techniques/exporting-cad-drawings-to-svg/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 將 CAD 繪圖匯出為 SVG 格式 - Aspose.CAD Guide

## 介紹

在 CAD（電腦輔助設計）的動態世界中，將圖面匯出為各種格式的能力是一項至關重要的技能。 SVG（可擴展向量圖形）就是這樣一種格式，由於其可擴展性和多功能性而廣受歡迎。在本教學中，我們將探討如何使用強大的 Aspose.CAD for .NET 函式庫將 CAD 繪圖匯出為 SVG。

## 先決條件

在深入學習本教程之前，請確保您具備以下先決條件：

-  Aspose.CAD for .NET 函式庫：下載並安裝 Aspose.CAD for .NET 函式庫。你可以找到圖書館[這裡](https://releases.aspose.com/cad/net/).

- 開發環境：使用 Visual Studio 或任何其他 .NET 開發工具設定適當的開發環境。

## 導入命名空間

首先，將必要的命名空間匯入到您的專案中：

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## 步驟1：設定文檔目錄

```csharp
//文檔目錄的路徑。
string MyDir = "Your Document Directory";
```

## 第 2 步：載入 CAD 圖紙

```csharp
using (Image image = Image.Load(MyDir + "sample.dwg"))
{
```

## 步驟 3：設定 SVG 匯出選項

```csharp
    var options = new SvgOptions();
    options.ColorType = SvgColorMode.Grayscale;
    options.TextAsShapes = true;
```

## 步驟 4：儲存 SVG 文件

```csharp
    image.Save(MyDir + "sample.svg", options);
}
```

透過遵循這些簡單的步驟，您可以使用 Aspose.CAD for .NET 將 CAD 繪圖無縫匯出為 SVG。該庫提供靈活性和自訂選項，可讓您根據您的要求自訂輸出。

## 結論

總之，Aspose.CAD for .NET 簡化了將 CAD 繪圖匯出為 SVG 的過程。其直覺的 API 和強大的功能使其成為使用 CAD 應用程式的開發人員的寶貴工具。

## 常見問題解答

### Q1：Aspose.CAD 是否相容於所有 CAD 格式？

A1：Aspose.CAD支援多種CAD格式，包括DWG和DXF，確保廣泛的兼容性。

### Q2：匯出為SVG時可以自訂顏色模式嗎？

A2：是的，Aspose.CAD允許您選擇顏色模式，提供輸出的靈活性。

### Q3：臨時許可證是否可用於測試目的？

 A3：是的，您可以獲得臨時許可證[這裡](https://purchase.aspose.com/temporary-license/)進行評估。

### Q4：哪裡可以找到Aspose.CAD的詳細文件？

 A4：文檔可用[這裡](https://reference.aspose.com/cad/net/).

### Q5：我如何獲得與 Aspose.CAD 相關的支援或提出問題？

 A5：造訪社群論壇[這裡](https://forum.aspose.com/c/cad/19)以尋求支持和討論。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
