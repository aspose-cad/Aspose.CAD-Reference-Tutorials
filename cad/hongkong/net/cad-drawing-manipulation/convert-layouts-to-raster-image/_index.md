---
title: 在 Aspose.CAD for .NET 中將佈局轉換為光柵影像
linktitle: 將佈局轉換為光柵影像
second_title: Aspose.CAD .NET - CAD 和 BIM 檔案格式
description: 使用 Aspose.CAD for .NET 輕鬆將 CAD 佈局轉換為光柵影像。利用強大的 CAD 操作功能增強您的開發。
weight: 12
url: /zh-hant/net/cad-drawing-manipulation/convert-layouts-to-raster-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 Aspose.CAD for .NET 中將佈局轉換為光柵影像

## 介紹

您是否希望在 .NET 應用程式中輕鬆地將佈局轉換為光柵圖像？別再猶豫了！本逐步指南將引導您完成使用 Aspose.CAD for .NET 的流程，這是一個功能強大的程式庫，可簡化電腦輔助設計 (CAD) 任務。

## 先決條件

在深入學習本教程之前，請確保您具備以下先決條件：

- Aspose.CAD for .NET 函式庫：從下列位置下載並安裝程式庫：[Aspose.CAD for .NET 下載頁面](https://releases.aspose.com/cad/net/).

- 開發環境：確保您的電腦上設定了有效的 .NET 開發環境。

- 要轉換的文件：準備包含要轉換為光柵影像的佈局的 CAD 文件。

- 您的文件目錄：將程式碼中的佔位符「您的文件目錄」替換為您的文件目錄的路徑。

## 導入命名空間

首先，讓我們匯入必要的命名空間，以使 Aspose.CAD 功能可以在您的程式碼中存取。

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## 第 1 步：載入 CAD 文檔

首先使用 Aspose.CAD 庫載入 CAD 文件。

```csharp
string sourceFilePath = MyDir + "conic_pyramid.dxf";
using (Image image = Image.Load(sourceFilePath))
{
    //您的進一步步驟的程式碼將位於此處
}
```

## 第 2 步：配置光柵化選項

建立一個實例`CadRasterizationOptions`設定頁面寬度、高度並指定要轉換的佈局。

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1200;
rasterizationOptions.PageHeight = 1200;
rasterizationOptions.Layouts = new string[] { "Model", "Layout1" };
```

## 步驟 3：為結果影像設定 TiffOptions

建立一個實例`TiffOptions`定義結果影像的格式。

```csharp
ImageOptionsBase options = new TiffOptions(TiffExpectedFormat.Default);
options.VectorRasterizationOptions = rasterizationOptions;
```

## 第 4 步：儲存結果影像

指定輸出路徑並儲存轉換後的影像。

```csharp
string outputFilePath = MyDir + "conic_pyramid_layoutstorasterimage_out.tiff";
image.Save(outputFilePath, options);
```

## 結論

恭喜！您已使用 Aspose.CAD for .NET 成功將 CAD 佈局轉換為光柵影像格式。可能性是巨大的，本指南可以作為您進行 CAD 相關工作的起點。

## 常見問題解答

### Q1：Aspose.CAD 是否相容於所有 CAD 格式？

 A1：Aspose.CAD支援多種CAD格式，包括DWG、DXF、DWF、STL等。檢查[文件](https://reference.aspose.com/cad/net/)以獲得完整的清單。

### Q2：如何取得Aspose.CAD的臨時授權？

 A2：訪問[臨時許可證頁面](https://purchase.aspose.com/temporary-license/)獲得用於測試和評估目的的臨時許可證。

### Q3：在哪裡可以找到對 Aspose.CAD 的支援？

 A3：論壇是尋求幫助的好地方。參觀[Aspose.CAD論壇](https://forum.aspose.com/c/cad/19)與社區聯繫並獲得協助。

### Q4：我可以免費試用Aspose.CAD嗎？

A4：當然！抓住你的[免費試用](https://releases.aspose.com/)探索 Aspose.CAD 的特性和功能。

### Q5：哪裡可以購買 Aspose.CAD 的授權？

 A5：導航至[購買頁面](https://purchase.aspose.com/buy)購買許可證並釋放 Aspose.CAD 的全部潛力。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
