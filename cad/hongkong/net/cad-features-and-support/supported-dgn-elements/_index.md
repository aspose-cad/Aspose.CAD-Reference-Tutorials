---
title: Aspose.CAD for .NET 支援的 DGN 元素
linktitle: 支持的 DGN 元素
second_title: Aspose.CAD .NET - CAD 和 BIM 檔案格式
description: 探索 Aspose.CAD for .NET 處理 DGN 檔案的強大功能。按照我們的逐步指南無縫處理 2D 和 3D 元素。
weight: 18
url: /zh-hant/net/cad-features-and-support/supported-dgn-elements/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for .NET 支援的 DGN 元素

## 介紹

您是一位希望無縫使用 DGN 檔案的 .NET 開發人員嗎？ Aspose.CAD for .NET 提供了一個強大的解決方案來有效處理 DGN 檔案。在本教學中，我們將深入研究支援的 DGN 元素，引導您完成使用 Aspose.CAD for .NET 的流程。

## 先決條件

在我們開始之前，請確保您具備以下條件：

- .NET 程式設計的基礎知識。
- Visual Studio 安裝在您的電腦上。
-  Aspose.CAD for .NET 函式庫，您可以下載[這裡](https://releases.aspose.com/cad/net/).

## 導入命名空間

要啟動您的項目，請將必要的命名空間匯入到您的 .NET 應用程式中。此步驟可確保您可以存取 Aspose.CAD for .NET 提供的功能。

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Dgn;
using Aspose.CAD.FileFormats.Dgn.DgnElements;
```

## 步驟 1：載入 DGN 文件

首先將現有 DGN 檔案作為 CadImage 載入到 .NET 應用程式中。

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    //你的程式碼在這裡
}
```

## 步驟 2：迭代 DGN 元素

使用 foreach 迴圈迭代 DGN 元素。 Aspose.CAD for .NET 提供了多種可供您使用的 DGN 元素類型。

```csharp
foreach (DgnDrawingElementBase element in dgnImage.Elements)
{
    //你的程式碼在這裡
}
```

## 第 3 步：處理先前支援的實體

處理以前支援的 2D 實體，現在也支援 3D。

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.Line:
    case DgnElementType.Ellipse:
    case DgnElementType.Curve:
    //其他案例
        {
            //你的程式碼在這裡
            break;
        }
}
```

## 第 4 步：處理支援的 3D 實體

處理 Aspose.CAD for .NET 提供的支援的 3D 實體。

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.SolidHeader3D:
    case DgnElementType.Cone:
    case DgnElementType.CellHeader:
        {
            //你的程式碼在這裡
            break;
        }
}
```

## 步驟5：導出並儲存

最後將修改後的DGN檔案匯出為光柵影像並儲存到指定目錄。

```csharp
Console.WriteLine("\nThe DGN file exported successfully to raster image.\nFile saved at " + MyDir);
```

## 結論

在本教學中，我們探討了 Aspose.CAD for .NET 在處理和操作 DGN 檔案方面的功能。透過遵循逐步指南，您可以有效地使用支援的 DGN 元素，無論它們是 2D 還是 3D 實體。 Aspose.CAD for .NET 可讓您將 DGN 檔案處理無縫整合到您的 .NET 應用程式中。

## 常見問題解答

### Q1：在哪裡可以找到 Aspose.CAD for .NET 的文件？

 A1：你可以找到文檔[這裡](https://reference.aspose.com/cad/net/).

### 問題 2：如何下載 Aspose.CAD for .NET？

 A2：您可以下載該程式庫[這裡](https://releases.aspose.com/cad/net/).

### 問題 3：Aspose.CAD for .NET 是否有免費試用版？

A3：是的，您可以免費試用[這裡](https://releases.aspose.com/).

### 問題 4：在哪裡可以取得 Aspose.CAD for .NET 的臨時授權？

 A4：可以使用臨時許可證[這裡](https://purchase.aspose.com/temporary-license/).

### Q5: 需要協助或有疑問嗎？

A5：造訪 Aspose.CAD for .NET 社區[支援論壇](https://forum.aspose.com/c/cad/19).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
