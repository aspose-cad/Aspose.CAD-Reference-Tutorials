---
title: 在 Aspose.CAD for .NET 中調整 CAD 繪圖尺寸
linktitle: 調整 CAD 繪圖尺寸
second_title: Aspose.CAD .NET - CAD 和 BIM 檔案格式
description: 了解如何使用 Aspose.CAD 在 .NET 中輕鬆調整 CAD 繪圖尺寸。請按照我們的逐步指南進行無縫調整大小。
type: docs
weight: 10
url: /zh-hant/net/cad-drawing-manipulation/adjust-cad-drawing-size/
---
## 介紹

您是否希望在 .NET 應用程式中無縫調整 CAD 繪圖的尺寸？ Aspose.CAD for .NET 提供了強大的解決方案，讓您可以輕鬆處理 CAD 繪圖大小調整。在本教程中，我們將引導您完成整個過程，分解每個步驟，以確保您掌握使用 Aspose.CAD 調整 CAD 繪圖大小的複雜性。

## 先決條件

在我們深入學習本教程之前，請確保您具備以下先決條件：

- Aspose.CAD for .NET 函式庫：從下列位置下載並安裝程式庫：[Aspose.CAD for .NET 下載頁面](https://releases.aspose.com/cad/net/).
- 範例 CAD 圖面：確保文件目錄中有範例 CAD 繪圖檔案（例如「sample.dwg」）。

## 導入命名空間

首先將必要的命名空間匯入到您的 .NET 應用程式中。此步驟對於存取 Aspose.CAD for .NET 提供的功能至關重要。

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## 第 1 步：載入 CAD 圖紙

首先將 CAD 繪圖載入到 Aspose.CAD.Image 類別的實例中。確保您的範例繪圖具有正確的檔案路徑。

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "sample.dwg";

//在 Image 實例中載入 CAD 繪圖
using (var image = Aspose.CAD.Image.Load(sourceFilePath))
{
    //你的程式碼在這裡...
}
```

## 步驟2：建立BmpOptions

建立 BmpOptions 類別的實例，該類別負責在將 CAD 圖形儲存為 BMP 檔案時指定選項。

```csharp
Aspose.CAD.ImageOptions.BmpOptions bmpOptions = new Aspose.CAD.ImageOptions.BmpOptions();
```

## 步驟 3：設定 CadRasterizationOptions

實例化 CadRasterizationOptions 類別並配置其屬性以進行向量光柵化。

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions cadRasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
bmpOptions.VectorRasterizationOptions = cadRasterizationOptions;
```

## 步驟 4：設定 UnitType 屬性

設定 CadRasterizationOptions 的 UnitType 屬性以指定調整大小的單位類型。在此範例中，它設定為公分。

```csharp
cadRasterizationOptions.UnitType = Aspose.CAD.ImageOptions.UnitType.Centimeter;
```

## 步驟5：設定佈局屬性

透過設定 Layouts 屬性來指定要包含在調整大小的繪圖中的佈局。

```csharp
cadRasterizationOptions.Layouts = new string[] { "Model" };
```

## 第 6 步：匯出為 BMP

最後，使用 Save 方法將調整大小的佈局儲存為 BMP 檔案。

```csharp
string outPath = sourceFilePath + ".bmp";
image.Save(outPath, bmpOptions);
```

現在您已經使用 Aspose.CAD for .NET 成功調整了 CAD 繪圖的尺寸！

## 結論

在本教學中，我們示範了使用 Aspose.CAD 在 .NET 中調整 CAD 繪圖大小的過程。透過執行以下步驟，您可以將此功能無縫整合到您的應用程式中，從而提供流暢的用戶體驗。

## 常見問題解答

### Q1：Aspose.CAD for .NET 是否與所有 CAD 格式相容？

 A1：Aspose.CAD for .NET 支援多種 CAD 格式，包括 DWG、DXF、DWF 等。檢查[文件](https://reference.aspose.com/cad/net/)取得完整清單。

### Q2：我可以同時調整多個佈局的大小嗎？

A2：是的，您可以透過調整 CadRasterizationOptions 中的佈局陣列來調整多個佈局的大小。

### 問題 3：在哪裡可以獲得 Aspose.CAD for .NET 的支援？

 A3：訪問[Aspose.CAD論壇](https://forum.aspose.com/c/cad/19)以獲得社區的支持和幫助。

### Q4：有免費試用嗎？

 A4：是的，您可以探索[免費試用](https://releases.aspose.com/)評估 Aspose.CAD for .NET 的功能。

### 問題 5：如何取得 Aspose.CAD for .NET 的臨時授權？

 A5：取得用於測試目的的臨時許可證[這裡](https://purchase.aspose.com/temporary-license/).