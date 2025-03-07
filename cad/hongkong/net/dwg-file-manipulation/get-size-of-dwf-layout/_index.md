---
title: 在 C# 中處理 DWG 檔案 - 取得 DWF 佈局的大小
linktitle: 在 C# 中處理 DWG 檔案 - 取得 DWF 佈局的大小
second_title: Aspose.CAD .NET - CAD 和 BIM 檔案格式
description: 探索 Aspose.CAD for .NET 在處理 DWG 檔案方面的強大功能。了解使用 C# 輕鬆擷取 DWF 佈局尺寸。
weight: 10
url: /zh-hant/net/dwg-file-manipulation/get-size-of-dwf-layout/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 C# 中處理 DWG 檔案 - 取得 DWF 佈局的大小

## 介紹

在電腦輔助設計 (CAD) 和 .NET 開發領域，Aspose.CAD 是處理 DWG 檔案的強大工具。本教學將引導您完成在 C# 中處理 DWG 檔案並提取 DWF 佈局大小的過程。在我們深入研究程式碼之前，讓我們確保您已做好開始此旅程的一切準備。

## 先決條件

要無縫地遵循本教程，請確保您具備以下先決條件：

-  Aspose.CAD for .NET：確保您已安裝 Aspose.CAD for .NET。您可以從[Aspose.CAD for .NET 下載頁面](https://releases.aspose.com/cad/net/).

現在您已經擁有了必要的工具，讓我們進入程式設計領域。

## 導入命名空間

在開始使用程式碼之前，讓我們先匯入所需的命名空間：

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Dwf;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

這些命名空間將提供在 C# 應用程式中使用 Aspose.CAD 處理 CAD 檔案的基本類別和方法。

## 第 1 步：設定您的環境

首先確保您為您的專案設定了正確的環境。在 C# 專案中引用 Aspose.CAD 庫。

## 第 2 步：定義檔路徑

定義 DWG 檔案的路徑以及產生的 JPG 檔案的輸出目錄：

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "blocks_and_tables.dwf";
```

## 步驟 3：載入 DWF 映像

使用 Aspose.CAD 載入 DWF 圖像：

```csharp
using (DwfImage image = (DwfImage)Aspose.CAD.Image.Load(sourceFilePath))
{
    //進一步步驟的程式碼將在此處
}
```

## 第 4 步：遍歷頁面

遍歷 DWF 圖像的頁面：

```csharp
foreach (var page in image.Pages)
{
    //進一步步驟的程式碼將在此處
}
```

## 步驟5：取得佈局信息

取得每個頁面的佈局資訊：

```csharp
var layout = page.Name;
System.Console.WriteLine("Layout= " + layout);
```

## 第 6 步：設定 JPG 選項

設定將佈局儲存為 JPG 檔案的選項：

```csharp
using (FileStream fs = new FileStream(MyDir + "layout_" + layout + ".jpg", FileMode.Create))
{
    JpegOptions jpegOptions = new JpegOptions();
    CadRasterizationOptions options = new CadRasterizationOptions();
    options.Layouts = new string[] { layout };
    //進一步步驟的程式碼將在此處
}
```

## 第 7 步：確定頁面大小

確定 DWF 佈局的尺寸：

```csharp
double sizeExtX = page.MaxPoint.X - page.MinPoint.X;
double sizeExtY = page.MaxPoint.Y - page.MinPoint.Y;
//進一步步驟的程式碼將在此處
```

## 第 8 步：設定頁面尺寸

根據單位類型設定頁面尺寸：

```csharp
if (page.UnitType == UnitType.Inch)
{
    options.PageHeight = CommonHelper.INtoPixels(sizeExtY, CommonHelper.DPI);
    options.PageWidth = CommonHelper.INtoPixels(sizeExtX, CommonHelper.DPI);
}
else if (page.UnitType == UnitType.Millimeter)
{
    options.PageHeight = CommonHelper.MMtoPixels(sizeExtY, CommonHelper.DPI);
    options.PageWidth = CommonHelper.MMtoPixels(sizeExtX, CommonHelper.DPI);
}
else
{
    options.PageHeight = (float)sizeExtY;
    options.PageWidth = (float)sizeExtX;
}
```

## 步驟9：儲存JPG文件

使用指定選項儲存 JPG 檔案：

```csharp
jpegOptions.VectorRasterizationOptions = options;
image.Save(fs, jpegOptions);
}
```

現在，您已使用 C# 中的 Aspose.CAD 成功從 DWG 檔案中提取了 DWF 佈局的尺寸。請隨意探索 Aspose.CAD 為 .NET 開發提供的更多特性和功能。

## 結論

在本教程中，我們演練了使用 Aspose.CAD 在 C# 中處理 DWG 檔案的過程。透過執行這些步驟，您不僅可以獲得 DWF 佈局的大小，還可以利用 Aspose.CAD 的功能來執行 .NET 專案中的各種 CAD 相關任務。

## 常見問題解答

### Q1：Aspose.CAD 與最新的 DWG 檔案格式相容嗎？

 A1：Aspose.CAD支援各種DWG檔案格式，包括最新版本。請參閱[文件](https://reference.aspose.com/cad/net/)有關特定相容性詳細資訊。

### Q2：我可以將 Aspose.CAD 用於商業和個人專案嗎？

 A2：是的，Aspose.CAD 為商業和個人用途提供靈活的授權選項。參觀[購買頁面](https://purchase.aspose.com/buy)更多細節。

### Q3：如何取得 Aspose.CAD 的臨時授權？

A3：您可以從以下地點獲得臨時許可證：[這裡](https://purchase.aspose.com/temporary-license/)出於評估目的。

### Q4：在哪裡可以找到對 Aspose.CAD 的支援？

A4：如有任何疑問或幫助，請訪問[Aspose.CAD論壇](https://forum.aspose.com/c/cad/19).

### Q5：Aspose.CAD 有免費試用版嗎？

A5：是的，您可以存取 Aspose.CAD 的免費試用版[這裡](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
