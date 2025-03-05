---
title: 將 3D 影像匯出為 PDF - Aspose.CAD 教學課程
linktitle: 將 3D 影像匯出為 PDF
second_title: Aspose.CAD .NET - CAD 和 BIM 檔案格式
description: 使用 Aspose.CAD for .NET 輕鬆將 3D CAD 影像轉換為 PDF。請按照我們的逐步教學進行無縫 PDF 匯出。
type: docs
weight: 10
url: /zh-hant/net/3d-image-export/exporting-3d-images-to-pdf/
---
## 介紹

您是否希望使用 Aspose.CAD for .NET 將 3D 影像無縫匯出為 PDF？本逐步教學將引導您完成整個過程，確保您利用 Aspose.CAD 的強大功能輕鬆將 3D 影像轉換為 PDF 格式。

## 先決條件

在深入學習本教程之前，請確保您具備以下先決條件：

-  Aspose.CAD for .NET：確保您已安裝 Aspose.CAD for .NET 程式庫。如果沒有，您可以從以下位置下載[Aspose.CAD for .NET 下載頁面](https://releases.aspose.com/cad/net/).

- 文件目錄：設定儲存 CAD 檔案的目錄，並記下路徑。

## 導入命名空間

在您的 .NET 專案中，匯入使用 Aspose.CAD 所需的命名空間。將以下行新增至程式碼檔案的頂部：

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
```

## 第 1 步：載入 CAD 映像

首先載入要匯出為 PDF 的 CAD 影像。使用`Load`Aspose.CAD 庫中的方法。代替`"conic_pyramid.dxf"`以及 CAD 檔案的路徑。

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";
using (Image cadImage = Image.Load(sourceFilePath))
{
    //用於載入 CAD 圖像的程式碼位於此處
}
```

## 第 2 步：配置光柵化選項

配置 CAD 影像的光柵化選項。設定頁面寬度、頁面高度和佈局等參數。取消註解相關行`TypeOfEntities`如果您的實體是 3D 的。

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
// rasterizationOptions.TypeOfEntities = TypeOfEntities.Entities3D;

rasterizationOptions.Layouts = new string[] { "Model" };
```

## 步驟 3：設定 PDF 選項

建立 PDF 選項並將其與光柵化選項關聯。

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## 第 4 步：另存為 PDF

使用配置的選項將 CAD 影像儲存為 PDF 檔案。指定 PDF 檔案的輸出路徑。

```csharp
MyDir = MyDir + "Export3DImagestoPDF_out.pdf";
cadImage.Save(MyDir, pdfOptions);
```

## 結論

恭喜！您已使用 Aspose.CAD for .NET 成功將 3D 影像匯出為 PDF。這個簡單的教學可確保您輕鬆地將 CAD 檔案轉換為更易於存取的格式。

## 常見問題解答

### Q1：Aspose.CAD 是否相容於所有 CAD 檔案格式？

A1：是的，Aspose.CAD 支援多種 CAD 格式，確保處理各種文件類型的靈活性。

### Q2：匯出PDF時可以自訂頁面尺寸嗎？

A2：當然。本教學課程示範如何根據您的要求配置頁面寬度和高度。

### 問題 3：Aspose.CAD 是否提供臨時授權？

 A3：是的，您可以透過存取取得 Aspose.CAD 的臨時許可證[臨時執照](https://purchase.aspose.com/temporary-license/).

### 問題 4：我可以在哪裡找到其他支持或社區討論？

A4：前往[Aspose.CAD論壇](https://forum.aspose.com/c/cad/19)以尋求社區的支持和參與。

### Q5：Aspose.CAD 有免費試用版嗎？

 A5：是的，您可以透過存取 Aspose.CAD 的功能來探索[免費試用](https://releases.aspose.com/).