---
title: 使用 Aspose.CAD for .NET 輕鬆實現 STL 到 PNG 的轉換
linktitle: 將 STL 檔案匯出為 PNG
second_title: Aspose.CAD .NET - CAD 和 BIM 檔案格式
description: 使用 Aspose.CAD for .NET 輕鬆將 STL 檔案轉換為 PNG。請按照我們的逐步指南進行無縫整合。現在下載！
weight: 10
url: /zh-hant/net/stl-file-export/exporting-stl-files-to-png/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.CAD for .NET 輕鬆實現 STL 到 PNG 的轉換

## 介紹
在電腦輔助設計 (CAD) 的動態世界中，高效的文件轉換至關重要。 Aspose.CAD for .NET 是一個功能強大的工具包，它簡化了將 STL 檔案匯出為 PNG 的過程，為開發人員提供了所需的靈活性和功能。本教學將逐步引導您完成整個過程，確保使用 Aspose.CAD 從 STL 順利過渡到 PNG。
## 先決條件
在我們深入學習本教學之前，請確保您已準備好以下內容：
1.  Aspose.CAD for .NET：下載並安裝 Aspose.CAD 函式庫。你可以找到它[這裡](https://releases.aspose.com/cad/net/).
2. 開發環境：設定您首選的 .NET 開發環境。
3. STL 檔案：準備好用於轉換的 STL 檔案。在本教程中，我們將使用名為“galeon.stl”的範例檔案。
## 導入命名空間
若要開始此過程，請在 .NET 應用程式中匯入必要的命名空間。這可確保您能夠存取 STL 到 PNG 轉換所需的類別和方法。
```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```
## 步驟1：定義目錄和來源檔案路徑
```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "galeon.stl";
```
確保將“您的文件目錄”替換為 STL 檔案所在的實際目錄路徑。
## 第 2 步：載入 CAD 映像
```csharp
using (var cadImage = (CadImage)Image.Load(sourceFilePath))
{
    //進一步的步驟將在此區塊內執行
}
```
此步驟將 STL 檔案載入為 CAD 映像，以便您對其進行操作和匯出。
## 第 3 步：設定光柵化選項
```csharp
var rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 100;
rasterizationOptions.PageHeight = 100;
```
根據您的喜好和要求調整頁面寬度和高度。這些設定決定導出的 PNG 的尺寸。
## 第 4 步：配置 PNG 選項
```csharp
PngOptions pngOptions = new PngOptions();
pngOptions.VectorRasterizationOptions = rasterizationOptions;
```
建立 PNG 選項，合併上一個步驟中定義的光柵化設定。
## 第5步：儲存PNG文件
```csharp
string outPath = sourceFilePath + ".png";
cadImage.Save(outPath, pngOptions);
```
指定 PNG 檔案的輸出路徑，並使用提供的選項將 CAD 影像儲存為 PNG 格式。
根據您的特定用例的需要重複這些步驟，您將成功使用 Aspose.CAD for .NET 將 STL 檔案匯出為 PNG。
## 結論
Aspose.CAD for .NET 簡化了將 STL 檔案轉換為 PNG 的複雜任務，為開發人員提供了可靠的工具包。透過遵循此逐步指南，您可以將此功能無縫整合到您的應用程式中。
## 常見問題解答
### Q：我可以自訂導出的 PNG 尺寸嗎？
絕對地！在步驟 3 中，調整`PageWidth`和`PageHeight`值以滿足您的特定要求。
### Q：臨時許可證是否可用於測試目的？
是的，您可以獲得臨時許可證[這裡](https://purchase.aspose.com/temporary-license/)用於測試和評估。
### Q：我可以在哪裡找到其他支持或社區討論？
參觀[Aspose.CAD論壇](https://forum.aspose.com/c/cad/19)支持和協作討論。
### Q：是否支援轉換其他文件格式？
是的，Aspose.CAD 支援 STL 以外的各種 CAD 格式。請參閱[文件](https://reference.aspose.com/cad/net/)以獲得完整的清單。
### Q：我可以批次處理多個STL檔案嗎？
當然！根據提供的步驟實作循環來批次處理多個 STL 檔案。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
