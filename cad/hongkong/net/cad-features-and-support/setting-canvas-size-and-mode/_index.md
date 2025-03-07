---
title: 在 Aspose.CAD for .NET 中設定畫布大小和模式
linktitle: 設定畫布大小和模式
second_title: Aspose.CAD .NET - CAD 和 BIM 檔案格式
description: 探索在 Aspose.CAD for .NET 中設定畫布大小和模式的逐步指南。使用此綜合教學輕鬆優化您的 CAD 渲染。
weight: 16
url: /zh-hant/net/cad-features-and-support/setting-canvas-size-and-mode/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 Aspose.CAD for .NET 中設定畫布大小和模式

## 介紹

您準備好釋放 Aspose.CAD for .NET 的全部潛力並徹底改變您的 CAD 渲染體驗了嗎？在本逐步教程中，我們將深入研究使用強大的 Aspose.CAD 庫來設定畫布大小和模式的複雜性。無論您是經驗豐富的開發人員還是新手，本指南都將引導您完成整個過程，確保您有效地利用 Aspose.CAD 的功能。

## 先決條件

在我們深入學習本教程之前，請確保您具備以下先決條件：

-  Aspose.CAD 函式庫：從下列位置下載並安裝 Aspose.CAD 函式庫：[Aspose.CAD 網站](https://releases.aspose.com/cad/net/).

- 開發環境：確保您的電腦上設定了 .NET 開發環境。

- 範例 CAD 檔案：在本教學中，我們將使用範例 DXF 檔案。您可以在[Aspose.CAD 文檔](https://reference.aspose.com/cad/net/).

## 導入命名空間

首先，在 .NET 應用程式的開頭導入必要的命名空間：

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## 第 1 步：載入 CAD 文件

首先使用以下程式碼載入 CAD 檔案：

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (Image image = Image.Load(sourceFilePath))
{
    //您的進一步步驟的程式碼將位於此處
}
```

## 第 2 步：建立 CadRasterizationOptions

建立一個實例`CadRasterizationOptions`並設定其屬性：

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.AutomaticLayoutsScaling = true;
rasterizationOptions.NoScaling = false;
```

## 第 3 步：建立 PdfOptions

建立一個實例`PdfOptions`並設定其`VectorRasterizationOptions`財產：

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## 第 4 步：匯出為 PDF

使用配置的選項將 CAD 檔案匯出為 PDF：

```csharp
image.Save(MyDir + "result_out.pdf", pdfOptions);
```

## 第 5 步：建立 TiffOptions

建立一個實例`TiffOptions`並設定其`VectorRasterizationOptions`財產：

```csharp
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.VectorRasterizationOptions = rasterizationOptions;
```

## 第 6 步：導出為 TIFF

使用配置的選項將 CAD 檔案匯出為 TIFF：

```csharp
image.Save(MyDir + "result_out.tiff", tiffOptions);
```

## 結論

恭喜！您已在 Aspose.CAD for .NET 中成功設定畫布大小和模式。這項強大的功能為 CAD 渲染開啟了無限可能。嘗試不同的選項並發現 Aspose.CAD 在 .NET 應用程式中的全部潛力。

## 常見問題解答

### Q1：我可以將 Aspose.CAD 與其他 .NET 函式庫一起使用嗎？

A1：是的，Aspose.CAD 與其他 .NET 程式庫無縫集成，為 CAD 操作提供增強的功能。

### Q2：Aspose.CAD 可以免費試用嗎？

 A2：是的，您可以透過免費試用來探索 Aspose.CAD 的功能。訪問[這裡](https://releases.aspose.com/)開始。

### Q3：如何獲得 Aspose.CAD 的支援？

A3： 如需支援和討論，請訪問[Aspose.CAD論壇](https://forum.aspose.com/c/cad/19).

### 問題 4：在哪裡可以找到 Aspose.CAD 的綜合文件？

 A4：請參閱[Aspose.CAD 文檔](https://reference.aspose.com/cad/net/)取得詳細資訊和範例。

### Q5：如何購買 Aspose.CAD for .NET？

 A5：要購買 Aspose.CAD，請訪問[購買頁面](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
