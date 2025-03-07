---
title: 在 Aspose.CAD for .NET 中將 CAD 佈局匯出為光柵影像格式
linktitle: 將 CAD 佈局匯出為光柵影像格式
second_title: Aspose.CAD .NET - CAD 和 BIM 檔案格式
description: 了解如何使用 Aspose.CAD for .NET 將 CAD 佈局匯出為光柵影像。請按照我們的逐步指南進行無縫轉換。
weight: 10
url: /zh-hant/net/cad-export-formats/export-cad-layouts-to-raster-image-formats/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 Aspose.CAD for .NET 中將 CAD 佈局匯出為光柵影像格式

## 介紹

您是否希望使用 Aspose.CAD for .NET 有效率地將 CAD 佈局轉換為光柵影像格式？本逐步指南將引導您完成整個過程，提供詳細的說明和程式碼片段，使任務順利進行。無論您是經驗豐富的開發人員還是 Aspose.CAD 新手，本教學都適合各個層面的專業知識。

## 先決條件

在深入學習本教學之前，請確保您具備以下條件：

- Aspose.CAD for .NET 函式庫：確保您已安裝 Aspose.CAD 函式庫。如果沒有，您可以從以下位置下載[Aspose.CAD 網站](https://releases.aspose.com/cad/net/).

- CAD 圖面檔案：準備要轉換為光柵影像格式的 CAD 圖面檔案（例如 conic_pyramid.dxf）。

## 導入命名空間

在您的 .NET 專案中，匯入必要的命名空間以利用 Aspose.CAD 功能。在程式碼開頭包含以下命名空間：

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## 第 1 步：載入 CAD 圖紙

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

//在 Image 實例中載入 CAD 繪圖
using (var image = Image.Load(sourceFilePath))
{
    //載入 CAD 繪圖的程式碼位於此處
}
```

## 第 2 步：建立 CadRasterizationOptions

```csharp
//建立 CadRasterizationOptions 的實例
var rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
```

## 第 3 步：指定圖層

```csharp
//將圖層名稱加入到 CadRasterizationOptions 的圖層清單中
rasterizationOptions.Layers = new string[] { "LayerA" };
```

## 第 4 步：建立 JpegOptions

```csharp
//建立 JpegOptions 的實例（或任何用於光柵格式的 ImageOptions）
var options = new JpegOptions();
options.VectorRasterizationOptions = rasterizationOptions;
```

## 第 5 步：匯出為 Jpeg 格式

```csharp
//將每個圖層匯出為 Jpeg 格式
MyDir = MyDir + "CADLayersToRasterImageFormats_out.jpg";
image.Save(MyDir, options);
```

## 附加步驟：轉換所有圖層

如果要轉換所有圖層，請使用下列方法：

```csharp
ConvertAllLayersToRasterImageFormats();
```

此方法迭代 CAD 繪圖中的所有圖層，將每個圖層匯出到單獨的 Jpeg 檔案。

## 結論

恭喜！您已成功學習如何使用 Aspose.CAD for .NET 將 CAD 佈局匯出為光柵影像格式。本教學為尋求高效可靠的 CAD 轉換解決方案的開發人員提供了全面的指南。

## 常見問題解答

### Q1：我可以使用其他影像格式匯出嗎？

 A1: 是的，可以。只需更換`JpegOptions`具有所需格式的選項，例如`PngOptions`或者`BmpOptions`.

### Q2：有試用版嗎？

A2：是的，您可以透過下載試用版來探索Aspose.CAD的功能[這裡](https://releases.aspose.com/).

### Q3：如何獲得 Aspose.CAD 的支援？

A3：訪問Aspose.CAD[論壇](https://forum.aspose.com/c/cad/19)以獲得社區支持或考慮購買許可證以獲得專門支持。

### Q4：可以使用臨時許可證嗎？

 A4：是的，您可以獲得臨時許可證[這裡](https://purchase.aspose.com/temporary-license/).

### Q5：在哪裡可以找到文件？

 A5：參考詳細文檔[這裡](https://reference.aspose.com/cad/net/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
