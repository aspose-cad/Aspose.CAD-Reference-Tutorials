---
title: Aspose.CAD for .NET 支援 DGN V7
linktitle: 支持 DGN V7
second_title: Aspose.CAD .NET - CAD 和 BIM 檔案格式
description: 探索 Aspose.CAD for .NET 對 DGN V7 的無縫支援。透過逐步指導，輕鬆將 DGN 檔案轉換為光柵影像。
weight: 19
url: /zh-hant/net/cad-features-and-support/support-for-dgn-v7/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for .NET 支援 DGN V7

## 介紹

在 .NET 開發領域，Aspose.CAD 作為處理電腦輔助設計 (CAD) 檔案的強大函式庫脫穎而出。本教學深入探討 Aspose.CAD for .NET 的特定功能 — 對 DGN V7 檔案的支援。 DGN 是 Design 的縮寫，是 CAD 領域廣泛使用的檔案格式。 Aspose.CAD 簡化了使用 DGN V7 檔案的流程，為開發人員提供無縫體驗。

## 先決條件

在我們深入實施之前，請確保您具備以下先決條件：

-  Aspose.CAD for .NET：確保您已安裝 Aspose.CAD 程式庫。您可以從[網站](https://releases.aspose.com/cad/net/).

- 開發環境：設定有效的 .NET 開發環境，包括 Visual Studio 或任何其他首選 IDE。

現在我們已經滿足了先決條件，讓我們探討如何利用 Aspose.CAD for .NET 中對 DGN V7 的支援。

## 導入命名空間

首先匯入必要的命名空間以存取 Aspose.CAD 的功能：

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## 第 1 步：載入 DGN 文件

首先載入現有的 DGN 檔案作為`CadImage`。代替`"Your Document Directory"`和`"Nikon_D90_Camera.dgn"`具有適當的目錄路徑和檔案名稱。

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    //進一步步驟的程式碼位於此處...
}
```

## 第 2 步：配置光柵化選項

創建一個`CadRasterizationOptions`物件來定義和設定與光柵化相關的各種屬性。

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions
{
    PageWidth = 600,
    PageHeight = 300,
    NoScaling = true,
    AutomaticLayoutsScaling = false
};
```

## 步驟 3：設定向量光柵化選項

創建一個`JpegOptions`對象，因為我們打算將 DGN 檔案轉換為 JPEG。分配之前創建的`CadRasterizationOptions`反對它。

```csharp
ImageOptionsBase options = new JpegOptions
{
    VectorRasterizationOptions = rasterizationOptions
};
```

## 步驟 4：保存光柵化影像

致電`Save`的方法`CadImage`類別物件將 DGN 檔案匯出為光柵影像（在本例中為 JPEG）。

```csharp
cadImage.Save(MyDir + "ExportDGNToRasterImage_out.jpeg", options);
```

完成這些步驟後，DGN 檔案已成功匯出為光柵影像。

## 結論

在本教程中，我們探索了 Aspose.CAD for .NET 中對 DGN V7 的無縫支援。透過遵循逐步指南，開發人員可以輕鬆地將 DGN 檔案轉換為光柵影像，從而擴展其 .NET 應用程式的功能。

## 常見問題解答

### Q1：Aspose.CAD 是否相容於最新的 DGN V7 規範？

A1：是的，Aspose.CAD 旨在無縫處理 DGN V7 文件，確保與最新規範的兼容性。

### 問題 2：我可以自訂 DGN 檔案轉換的光柵化選項嗎？

 A2：當然。本教學課程示範如何建立和配置`CadRasterizationOptions`定制轉換過程。

### Q3：除了JPEG之外，還有其他支援的輸出格式嗎？

A3：是的，Aspose.CAD支援各種輸出格式。您可以瀏覽文件以獲得完整的清單。

### Q4：如何獲得 Aspose.CAD 相關查詢的支援？

 A4：訪問[Aspose.CAD論壇](https://forum.aspose.com/c/cad/19)以獲得社區支持和討論。

### 問題 5：Aspose.CAD for .NET 是否有免費試用版？

 A5：是的，您可以免費試用[這裡](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
