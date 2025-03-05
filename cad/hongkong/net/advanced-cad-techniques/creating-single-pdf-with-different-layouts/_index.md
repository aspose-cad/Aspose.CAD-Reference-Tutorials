---
title: 建立具有不同佈局的單一 PDF - Aspose.CAD 指南
linktitle: 建立具有不同佈局的單一 PDF
second_title: Aspose.CAD .NET - CAD 和 BIM 檔案格式
description: 使用 Aspose.CAD for .NET 建立具有不同佈局的單一 PDF。請按照我們的逐步指南進行無縫整合和高效 PDF 生成。
type: docs
weight: 13
url: /zh-hant/net/advanced-cad-techniques/creating-single-pdf-with-different-layouts/
---
## 介紹

您是否希望使用 Aspose.CAD for .NET 從具有不同佈局的 CAD 繪圖產生單一 PDF 文件？本逐步指南將引導您完成整個過程，幫助您實現無縫整合和高效的 PDF 創建。 Aspose.CAD for .NET 提供了強大的功能來以程式設計方式操作 CAD 繪圖，在本教程中，我們將專注於建立具有不同佈局的單一 PDF。

## 先決條件

在深入學習本教程之前，請確保您具備以下先決條件：

-  Aspose.CAD for .NET：確保您已安裝 Aspose.CAD for .NET。您可以從以下位置下載：[這裡](https://releases.aspose.com/cad/net/).

- 開發環境：建置.NET開發環境，對C#程式設計有基本了解。

## 導入命名空間

在您的 C# 專案中，包含必要的命名空間以利用 Aspose.CAD for .NET 的功能：

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## 第 1 步：載入 CAD 映像

```csharp
//文檔目錄的路徑。
string MyDir = "Your Document Directory";

using (CadImage cadImage = (CadImage)Image.Load(MyDir + "City skyway map.dwg"))
{
    //步驟 1 的代碼位於此處
}
```

## 第 2 步：自訂光柵化選項

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1000;
rasterizationOptions.PageHeight = 1000;

//多種佈局的自訂尺寸
rasterizationOptions.LayoutPageSizes.Add("ANSI C Plot", new SizeF(500, 1000));
rasterizationOptions.LayoutPageSizes.Add("8.5 x 11 Plot", new SizeF(1000, 100));
```

## 第 3 步：定義 PDF 選項

```csharp
PdfOptions pdfOptions = new PdfOptions() { VectorRasterizationOptions = rasterizationOptions };
```

## 第 4 步：另存為 PDF

```csharp
cadImage.Save(MyDir + "singlePDF_out.pdf", pdfOptions);
```

現在您已經使用 Aspose.CAD for .NET 成功建立了具有不同佈局的單一 PDF 文件。請隨意探索更多功能並根據您的特定要求自訂程式碼。

## 結論

在本教程中，我們介紹了使用 Aspose.CAD for .NET 從具有不同佈局的 CAD 繪圖建立單一 PDF 的過程。這個強大的程式庫簡化了 CAD 操作任務，並為各種場景提供了靈活性。

## 常見問題解答

### Q1：我可以將 Aspose.CAD for .NET 與其他 CAD 格式一起使用嗎？

A1：是的，Aspose.CAD for .NET 支援各種 CAD 格式，例如 DWG、DXF、DGN 等。

### Q2: 有免費試用嗎？

 A2：是的，您可以探索免費試用[這裡](https://releases.aspose.com/).

### 問題 3：如何獲得 Aspose.CAD for .NET 支援？

 A3：訪問[Aspose.CAD論壇](https://forum.aspose.com/c/cad/19)以獲得社區支持。

### Q4：哪裡可以找到詳細的文件？

A4：參考文檔[這裡](https://reference.aspose.com/cad/net/).

### Q5：我可以購買 Aspose.CAD for .NET 的授權嗎？

 A5：是的，您可以購買許可證[這裡](https://purchase.aspose.com/buy).