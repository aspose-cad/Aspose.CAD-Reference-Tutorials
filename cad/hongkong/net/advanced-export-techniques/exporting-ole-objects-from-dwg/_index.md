---
title: 從 DWG 檔案匯出 OLE 物件 - Aspose.CAD 教學課程
linktitle: 從 DWG 檔案匯出 OLE 對象
second_title: Aspose.CAD .NET - CAD 和 BIM 檔案格式
description: 探索使用 Aspose.CAD for .NET 從 DWG 檔案匯出 OLE 物件的逐步指南。輕鬆提升您的 CAD 檔案操作技能。
weight: 12
url: /zh-hant/net/advanced-export-techniques/exporting-ole-objects-from-dwg/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 從 DWG 檔案匯出 OLE 物件 - Aspose.CAD 教學課程

## 介紹

您是否希望輕鬆從 DWG 檔案中提取 OLE 物件？ Aspose.CAD for .NET 旨在為您簡化流程。在本教程中，我們將引導您逐步匯出 OLE 對象，確保您充分利用這個強大的 .NET 程式庫。 

## 先決條件

在我們深入學習本教程之前，請確保您具備以下先決條件：

-  Aspose.CAD for .NET Library：確保您已安裝該程式庫。您可以從[Aspose.CAD for .NET 下載頁面](https://releases.aspose.com/cad/net/).

- 文件目錄：設定儲存 DWG 檔案的目錄。代替`"Your Document Directory"`在提供的程式碼片段中使用實際路徑。

## 導入命名空間

在您的 .NET 專案中，您需要匯入必要的命名空間以利用 Aspose.CAD 功能。使用以下程式碼片段：

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## 步驟1：設定文檔目錄

```csharp
string MyDir = "Your Document Directory";
```

代替`"Your Document Directory"`與 DWG 檔案所在的路徑。

## 步驟 2：指定 DWG 文件

```csharp
string[] files = new string[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

列出陣列中要處理的 DWG 檔案。

## 第 3 步：配置匯出選項

```csharp
PngOptions pngOptions = new PngOptions { };
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.VectorRasterizationOptions = rasterizationOptions;
rasterizationOptions.Layouts = new string[] { "Layout1" };
```

根據您的要求自訂匯出選項。在此範例中，我們使用指定的佈局來配置 PNG 匯出。

## 第 4 步：遍歷文件並匯出

```csharp
foreach (string file in files)
{
    using (CadImage cadImage = (CadImage)Image.Load(MyDir + file))
    {
        cadImage.Save(MyDir + file + "_out.png", pngOptions);
    }
}
```

迭代指定的 DWG 文件，載入每個文件，並使用定義的選項儲存匯出的 PNG 檔案。

## 結論

恭喜！您已使用 Aspose.CAD for .NET 成功從 DWG 檔案匯出 OLE 物件。這個強大的程式庫簡化了複雜的任務，提高了 CAD 檔案操作的效率和靈活性。

## 常見問題解答

### Q1：Aspose.CAD for .NET 是否適合初級和進階 CAD 檔案？

A1：是的，Aspose.CAD for .NET 用途廣泛，可以處理各種 CAD 文件，包括初級和高級變體。

### Q2：我可以自訂不同佈局的匯出選項嗎？

A2：當然！如教程中所示，您可以自訂匯出選項（包括佈局）以滿足您的特定需求。

### 問題 3：在哪裡可以找到 Aspose.CAD for .NET 的詳細文件？

 A3：探索[Aspose.CAD for .NET 文檔](https://reference.aspose.com/cad/net/)獲取深入的資訊和範例。

### Q4：有免費試用嗎？

A4：是的，您可以透過免費試用體驗 Aspose.CAD for .NET 的功能。訪問[這個連結](https://releases.aspose.com/)開始。

### Q5：我如何獲得支持或與社群建立連結？

 A5：如需支持和社區參與，請訪問[Aspose.CAD論壇](https://forum.aspose.com/c/cad/19).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
