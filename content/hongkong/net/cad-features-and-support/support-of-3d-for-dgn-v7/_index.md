---
title: Aspose.CAD for .NET 中對 DGN V7 的 3D 支持
linktitle: DGN V7 支援 3D
second_title: Aspose.CAD .NET - CAD 和 BIM 檔案格式
description: 釋放 Aspose.CAD for .NET 中對 DGN V7 的 3D 支援的強大功能。請按照我們的逐步教學進行操作。
type: docs
weight: 20
url: /zh-hant/net/cad-features-and-support/support-of-3d-for-dgn-v7/
---
## 介紹

歡迎來到我們關於在 Aspose.CAD for .NET 中利用 3D for DGN V7 支援的綜合教學！ Aspose.CAD 是一個功能強大的程式庫，使開發人員能夠在其 .NET 應用程式中無縫地使用 CAD 檔案。在本教程中，我們將探討利用 DGN V7 的 3D 支援的步驟，為您提供增強 CAD 相關專案的知識。

## 先決條件

在深入學習本教程之前，請確保您具備以下先決條件：

-  Aspose.CAD for .NET：確保您已安裝 Aspose.CAD for .NET。如果沒有，您可以從以下位置下載[這裡](https://releases.aspose.com/cad/net/).

- 開發環境：為.NET應用程式開發設定合適的開發環境，例如Visual Studio。

- 範例 DGN 檔案：準備好範例 DGN 檔案以供測試。您可以使用提供的範例檔案“Nikon_D90_Camera.dgn”。

現在，讓我們開始使用 Aspose.CAD for .NET 實現對 DGN V7 的 3D 支援的步驟！

## 導入命名空間

在您的 .NET 應用程式中，首先導入必要的命名空間：

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

## 第 1 步：設定您的文件目錄

確保您的專案中設定了文件目錄。代替`"Your Document Directory"`與文檔目錄的實際路徑。

```csharp
string MyDir = "Your Document Directory";
```

## 步驟 2：載入 DGN 文件

使用以下程式碼將現有 DGN 檔案載入為 CadImage：

```csharp
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";
string outFile = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    //您用於進一步處理的程式碼位於此處
}
```

## 步驟 3：設定 PDF 匯出選項

設定匯出為 PDF 的選項，指定向量光柵化選項，例如頁面尺寸、自動佈局縮放、背景顏色和要匯出的佈局。

```csharp
var options = new PdfOptions
{
    VectorRasterizationOptions = new CadRasterizationOptions
    {
        PageWidth = 1500,
        PageHeight = 1500,
        AutomaticLayoutsScaling = true,
        BackgroundColor = Color.Black,
        Layouts = new string[] { "1", "2", "3", "9" } //僅匯出指定視圖
    }
};
```

## 第四步：保存光柵影像

使用配置的選項將 DGN 檔案另存為光柵影像。

```csharp
dgnImage.Save(outFile, options);
```

## 結論

恭喜！您已成功利用 Aspose.CAD for .NET 將支援 3D 的 DGN 檔案匯出為光柵影像。本教學課程為您提供了將此功能整合到 CAD 專案中的基本步驟。

## 常見問題解答

### Q1：我可以將 Aspose.CAD for .NET 與其他 CAD 檔案格式一起使用嗎？

A1：是的，Aspose.CAD支援各種CAD檔案格式，包括DWG和DXF。

### Q2：使用Aspose.CAD時如何處理異常？

A2：將程式碼包裝在 try-catch 區塊中，如提供的範例所示，以優雅地處理異常。

### Q3：Aspose.CAD適合商業項目嗎？

 A3：當然！您可以購買 Aspose.CAD for .NET[這裡](https://purchase.aspose.com/buy).

### Q4：我可以在購買前試用 Aspose.CAD for .NET 嗎？

A4：當然！探索免費試用[這裡](https://releases.aspose.com/).

### 問題 5：在哪裡可以找到 Aspose.CAD for .NET 的社群支援？

 A5：造訪社群論壇[這裡](https://forum.aspose.com/c/cad/19).