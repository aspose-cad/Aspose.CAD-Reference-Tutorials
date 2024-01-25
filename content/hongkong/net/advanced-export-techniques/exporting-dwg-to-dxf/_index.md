---
title: 在 C# 中將 DWG 匯出為 DXF 格式 - Aspose.CAD 教學課程
linktitle: 在 C# 中將 DWG 匯出為 DXF 格式
second_title: Aspose.CAD .NET - CAD 和 BIM 檔案格式
description: 使用 Aspose.CAD 解鎖 C# 中的 CAD 檔案操作。了解如何輕鬆將 DWG 匯出為 DXF。請按照我們的逐步指南進行無縫整合。
type: docs
weight: 10
url: /zh-hant/net/advanced-export-techniques/exporting-dwg-to-dxf/
---
## 介紹

如果您是 .NET 開發人員，並且正在尋求強大的 CAD 檔案操作解決方案，那麼 Aspose.CAD 是您的首選工具。在本逐步教學中，我們將引導您完成使用 C# 和 Aspose.CAD 將 DWG 檔案匯出為 DXF 格式的過程。

## 先決條件

在深入學習本教程之前，請確保您具備以下先決條件：

1.  Aspose.CAD 函式庫：從下列位置下載並安裝 Aspose.CAD 函式庫：[這個連結](https://releases.aspose.com/cad/net/).

2. 開發環境：建置C#開發環境，例如Visual Studio。

3. 範例 DWG 檔案：準備要匯出的範例 DWG 檔案。在本教學中，我們將使用「您的文件目錄」目錄中名為「Line.dwg」的檔案。

## 導入命名空間

在您的 C# 專案中，包含使用 Aspose.CAD 所需的命名空間：

```csharp
using Aspose.CAD.FileFormats.Cad;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## 步驟 1： 載入 DWG 文件

首先將 DWG 檔案載入到 C# 應用程式中。這是實現此目的的程式碼片段：

```csharp
string MyDir = "Your Document Directory";
string inputFile = MyDir + "Line.dwg";
using (var cadImage = (CadImage)Image.Load(inputFile))
{
    //您的進一步步驟的程式碼將位於此處
}
```

## 第 2 步：另存為 DXF

載入 DWG 檔案後，下一步是將其另存為 DXF 檔案。在之前的 using 區塊中加入以下程式碼：

```csharp
string outFile = MyDir + "Line_19.2.dxf";
cadImage.Save(outFile);
```

## 結論

恭喜！您已在 C# 中使用 Aspose.CAD 成功將 DWG 檔案匯出為 DXF 格式。這個簡單而強大的過程為您的應用程式中的 CAD 檔案操作開闢了無限可能。

## 常見問題解答

### Q1：Aspose.CAD 與最新的 CAD 檔案格式相容嗎？

A1：是的，Aspose.CAD 會定期更新，以確保與最新的 CAD 檔案格式相容。

### Q2：我可以在我的商業專案中使用Aspose.CAD嗎？

 A2：當然！ Aspose.CAD 附帶個人和商業用途的授權選項。訪問[這個連結](https://purchase.aspose.com/buy)了解詳情。

### Q3：有免費試用嗎？

 A3：是的，您可以免費試用 Aspose.CAD。訪問[這個連結](https://releases.aspose.com/)開始。

### Q4：哪裡可以找到Aspose.CAD的詳細文件？

A4：請參閱文檔[這個連結](https://reference.aspose.com/cad/net/)進行全面指導。

### Q5：需要幫助或有具體問題？

 A5：造訪 Aspose.CAD 社群論壇[這裡](https://forum.aspose.com/c/cad/19)尋求專家協助和社區支持。