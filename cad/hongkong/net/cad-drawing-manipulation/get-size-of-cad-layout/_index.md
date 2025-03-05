---
title: 在 Aspose.CAD for .NET 中取得 CAD 佈局的大小
linktitle: 取得 CAD 佈局的尺寸
second_title: Aspose.CAD .NET - CAD 和 BIM 檔案格式
description: 了解如何使用 Aspose.CAD 在 .NET 中擷取 CAD 佈局尺寸。請按照我們的逐步指南進行高效率的 CAD 檔案操作。
type: docs
weight: 14
url: /zh-hant/net/cad-drawing-manipulation/get-size-of-cad-layout/
---
## 介紹

歡迎閱讀這份關於使用 Aspose.CAD for .NET 取得 CAD 佈局尺寸的綜合指南。 Aspose.CAD 是一個功能強大的程式庫，可讓開發人員無縫地使用 CAD 檔案。在本教學中，我們將使用實際範例和逐步說明引導您完成檢索 CAD 佈局尺寸的過程。

## 先決條件

在我們深入學習本教程之前，請確保您具備以下先決條件：

-  Aspose.CAD for .NET：確保您已安裝 Aspose.CAD 程式庫。您可以從[Aspose.CAD for .NET 下載頁面](https://releases.aspose.com/cad/net/).

- 文件檔案：準備您要使用的 CAD 檔案。本教學使用「conic_pyramid.dxf」和「Bottom_plate.dwg」作為範例。

現在，讓我們開始吧！

## 導入命名空間

在您的 .NET 專案中，首先匯入必要的命名空間：

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

## 第 1 步：設定文檔目錄

設定文檔目錄的路徑。代替`"Your Document Directory"`與實際路徑。

```csharp
string MyDir = "Your Document Directory";
```

## 步驟 2：指定 CAD 檔案路徑

定義要分析的 CAD 檔案路徑數組。在此範例中，我們使用“conic_pyramid.dxf”和“Bottom_plate.dwg”。

```csharp
string[] sourceFilePaths = new[]
{
    MyDir + "conic_pyramid.dxf",
    MyDir + "Bottom_plate.dwg"
};
```

## 第 3 步：迭代 CAD 文件

迭代每個 CAD 檔案並檢索佈局資訊。

```csharp
foreach (var sourceFilePath in sourceFilePaths)
{
    string extension = Path.GetExtension(sourceFilePath);
    using (CadImage cadImage = (CadImage)Aspose.CAD.Image.Load(sourceFilePath))
    {
        // ……（繼續下一步）
    }
}
```

## 第 4 步：取得非空佈局

定義一個輔助方法以根據 CAD 檔案類型取得非空佈局。

```csharp
private static List<string> GetNotEmptyLayouts(Image cadImage, string extension)
{
    // ……（繼續下一步）
}
```

## 步驟 5：取得 DWG 檔案的佈局

實作邏輯以檢索 DWG 檔案的非空佈局。

```csharp
private static List<string> GetNotEmptyLayoutsForDwg(CadImage cadImage)
{
    // ……（繼續下一步）
}
```

## 第 6 步：取得 DXF 檔案的佈局

實作邏輯以檢索 DXF 檔案的非空佈局。

```csharp
private static List<string> GetNotEmptyLayoutsForDxf(CadImage cadImage)
{
    // ……（繼續下一步）
}
```

## 第 7 步：檢索佈局尺寸並另存為影像

完成取得佈局尺寸並將其儲存為影像的過程。

```csharp
foreach (string layout in layouts)
{
    // ……（繼續下一步）
}
```

## 結論

恭喜！您已經成功學習如何使用 Aspose.CAD for .NET 取得 CAD 佈局的大小。本教程涵蓋了從設定項目到檢索佈局資訊並將其另存為圖像的基本步驟。現在，您可以將這些知識合併到您的 .NET 應用程式中，以實現高效的 CAD 檔案操作。

## 常見問題解答

### Q1：Aspose.CAD 是否相容於所有 CAD 檔案格式？

A1：是的，Aspose.CAD支援各種CAD檔案格式，包括DWG和DXF。

### Q2：我可以自訂圖像儲存選項嗎？

A2：當然！您可以調整影像選項，例如格式和分辨率，以滿足您的特定要求。

### Q3：在哪裡可以找到其他文件？

 A3：請參閱[Aspose.CAD 文檔](https://reference.aspose.com/cad/net/)取得詳細資訊和範例。

### Q4：有免費試用嗎？

A4：是的，您可以使用[免費試用](https://releases.aspose.com/).

### Q5；我如何獲得技術支援？

 A5：如需技術支持，請訪問[Aspose.CAD論壇](https://forum.aspose.com/c/cad/19).