---
title: 在 Aspose.CAD for .NET 中將 DGN 匯出為 PDF
linktitle: 將 DGN 匯出為 PDF
second_title: Aspose.CAD .NET - CAD 和 BIM 檔案格式
description: 了解如何使用 Aspose.CAD for .NET 將 DGN 檔案輕鬆匯出為 PDF。無縫 CAD 檔案操作的逐步指南。
weight: 12
url: /zh-hant/net/cad-export-formats/export-dgn-to-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 Aspose.CAD for .NET 中將 DGN 匯出為 PDF

## 介紹

在 .NET 開發領域，Aspose.CAD 是一個功能強大的程式庫，可促進 CAD 檔案的操作和轉換。開發人員經常遇到的常見任務是將 DGN 檔案匯出為 PDF 格式。在本教學中，我們將使用 Aspose.CAD for .NET 逐步完成此過程。

## 先決條件

在深入學習本教學之前，請確保您已具備以下條件：

- C# 和 .NET 架構的應用知識。
- 安裝了 Aspose.CAD for .NET 函式庫。你可以下載它[這裡](https://releases.aspose.com/cad/net/).
- 範例 DGN 文件，例如本教學的「Nikon_D90_Camera.dgn」。

## 導入命名空間

在您的 C# 專案中，首先匯入必要的命名空間：

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## 第 1 步：載入 DGN 文件

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage cadImage = (DgnImage)Image.Load(sourceFilePath))
{
    //你的程式碼在這裡...
}
```

## 第 2 步：配置光柵化選項

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 600;
rasterizationOptions.PageHeight = 300;
rasterizationOptions.NoScaling = true;
rasterizationOptions.AutomaticLayoutsScaling = false;
```

## 第 3 步：建立 PDF 選項

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## 第 4 步：另存為 PDF

```csharp
cadImage.Save(MyDir + "ExportDGNToPdf_out.pdf", pdfOptions);
```

## 結論

恭喜！您已使用 Aspose.CAD for .NET 成功將 DGN 檔案匯出為 PDF。本教學涵蓋了從載入 DGN 檔案到配置光柵化選項以及將輸出儲存為 PDF 的基本步驟。

## 常見問題解答

### Q1：如果沒有 CAD 知識，我可以使用 Aspose.CAD for .NET 嗎？

A1：當然！ Aspose.CAD 簡化了複雜的 CAD 任務，使具有不同背景的開發人員都可以使用它。

### Q2：在哪裡可以找到更多 Aspose.CAD 範例和文件？

 A2：探索[文件](https://reference.aspose.com/cad/net/)取得全面的指南和範例。

### Q3：Aspose.CAD 有免費試用版嗎？

A3：是的，您可以獲得免費試用[這裡](https://releases.aspose.com/).

### Q4：如何取得 Aspose.CAD 的臨時授權？

 A4：取得臨時許可證[這裡](https://purchase.aspose.com/temporary-license/).

### Q5: 需要協助或有疑問嗎？

A5：訪問[Aspose.CAD論壇](https://forum.aspose.com/c/cad/19)以獲得社區支持。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
