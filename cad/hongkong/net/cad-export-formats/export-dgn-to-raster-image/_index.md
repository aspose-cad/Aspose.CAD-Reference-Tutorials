---
title: 在 Aspose.CAD for .NET 中將 DGN 匯出為光柵影像
linktitle: 將 DGN 匯出為光柵影像
second_title: Aspose.CAD .NET - CAD 和 BIM 檔案格式
description: 使用 Aspose.CAD for .NET 輕鬆將 DGN 轉換為光柵影像。探索逐步指南並釋放 .NET 在 CAD 檔案操作方面的強大功能。
weight: 13
url: /zh-hant/net/cad-export-formats/export-dgn-to-raster-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 Aspose.CAD for .NET 中將 DGN 匯出為光柵影像

## 介紹

在 .NET 開發的動態領域中，Aspose.CAD 成為處理電腦輔助設計 (CAD) 檔案的強大工具。本教學深入介紹使用 Aspose.CAD for .NET 將 DGN 檔案匯出為光柵影像的過程。如果您熱衷於將 DGN 檔案無縫轉換為視覺上引人注目的光柵影像，那麼您來對地方了。

## 先決條件

在我們開始這趟旅程之前，請確保您具備以下先決條件：

-  Aspose.CAD for .NET：請確定您的 .NET 專案中安裝了 Aspose.CAD 程式庫。您可以在以下位置找到該庫和相關文檔[網站](https://reference.aspose.com/cad/net/).

- 範例 DGN 檔案：準備好轉換的 DGN 檔案。在我們的範例中，我們將使用「Nikon_D90_Camera.dgn」。

現在，讓我們深入了解逐步指南。

## 導入命名空間

在您的 .NET 專案中，首先匯入 Aspose.CAD 所需的命名空間。此步驟可讓您存取 DGN 到光柵影像轉換所需的類別和方法。

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## 第 1 步：載入 DGN 文件

首先將 DGN 檔案載入到`CadImage`目的。這為後續的操作提供了基礎。

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    //您用於進一步處理的程式碼位於此處
}
```

## 第 2 步：定義光柵化選項

創建一個`CadRasterizationOptions`物件並設定各種屬性以根據您的要求自訂光柵化過程。

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 600;
rasterizationOptions.PageHeight = 300;
rasterizationOptions.NoScaling = true;
rasterizationOptions.AutomaticLayoutsScaling = false;
```

## 第 3 步：建立 JpegOptions 對象

由於我們的目標是將 DGN 檔案轉換為 JPEG，因此建立一個`JpegOptions`物件並分配先前定義的`CadRasterizationOptions`到它。

```csharp
ImageOptionsBase options = new JpegOptions();
options.VectorRasterizationOptions = rasterizationOptions;
```

## 第四步：保存光柵影像

利用`Save`的方法`CadImage`類別將 DGN 檔案匯出為所需格式的光柵影像（在本例中為 JPEG）。

```csharp
cadImage.Save(MyDir + "ExportDGNToRasterImage_out.jpg", options);
```

## 結論

恭喜！您已成功完成使用 Aspose.CAD for .NET 將 DGN 檔案匯出為光柵影像的步驟。本教學為您提供了輕鬆將此功能整合到您的 .NET 專案中的基本知識。

## 常見問題解答

### 問題 1：我可以將 DGN 檔案匯出為 JPEG 以外的格式嗎？

A1：是的，Aspose.CAD for .NET 支援各種輸出格式。您可以在步驟 3 中相應修改選項。

### Q2 轉換過程中出現異常如何處理？

A2：確保您有正確的異常處理（如提供的程式碼所示），以解決潛在問題。

### 問題 3：Aspose.CAD for .NET 有試用版嗎？

 A3：是的，您可以透過免費試用來探索該產品。訪問[這裡](https://releases.aspose.com/)了解更多。

### 問題 4：我可以在哪裡尋求協助或討論與 Aspose.CAD for .NET 相關的問題？

 A4：前往[Aspose.CAD論壇](https://forum.aspose.com/c/cad/19)以獲得社區支持和討論。

### 問題 5：如何取得 Aspose.CAD for .NET 的臨時授權？

 A5：參觀[這個連結](https://purchase.aspose.com/temporary-license/)取得滿足您的開發需求的臨時許可證。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
