---
title: 將 DWG 轉換為Compliance PDF - Aspose.CAD 教學課程
linktitle: 將 DWG 轉換為合規性 PDF
second_title: Aspose.CAD .NET - CAD 和 BIM 檔案格式
description: 使用 Aspose.CAD for .NET 將 DWG 轉換為合規性 PDF。請按照我們的教程獲取逐步指導。
weight: 13
url: /zh-hant/net/conversion-and-export/converting-dwg-to-compliance-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 將 DWG 轉換為Compliance PDF - Aspose.CAD 教學課程

## 介紹

歡迎使用我們的逐步教學，了解如何使用 Aspose.CAD for .NET 將 DWG 檔案轉換為合規性 PDF。 Aspose.CAD 是一個功能強大的 .NET API，讓開發人員能夠輕鬆使用 CAD 檔案格式。在本教程中，我們將透過詳細的範例和說明來指導您完成將 DWG 檔案轉換為Compliance PDF 的過程。

## 先決條件

在我們開始之前，請確保您具備以下先決條件：

-  Aspose.CAD for .NET：確保您已將 Aspose.CAD 庫整合到您的 .NET 專案中。你可以下載它[這裡](https://releases.aspose.com/cad/net/).

- 開發環境：安裝有效的 .NET 開發環境，並確保其配置正確。

- 範例 DWG 檔案：下載要轉換為Compliance PDF 的範例DWG 檔案。

## 導入命名空間

在您的 .NET 專案中，匯入必要的命名空間以利用 Aspose.CAD 功能。

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
```

現在，讓我們將 DWG 檔案轉換為Compliance PDF 的過程分解為多個步驟。

## 步驟 1： 載入 DWG 文件

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";

Aspose.CAD.Image cadImage = Aspose.CAD.Image.Load(sourceFilePath);
```

## 第 2 步：設定光柵化選項

建立一個實例`CadRasterizationOptions`並配置其屬性，例如背景顏色、頁面寬度和頁面高度。

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions
{
    BackgroundColor = Aspose.CAD.Color.White,
    PageWidth = 1600,
    PageHeight = 1600
};
```

## 第 3 步：建立 PDF 選項

建立一個實例`PdfOptions`並設定向量光柵化選項。

```csharp
PdfOptions pdfOptions = new PdfOptions
{
    VectorRasterizationOptions = rasterizationOptions,
    CorePdfOptions = new PdfDocumentOptions { Compliance = PdfCompliance.PdfA1a }
};
```

## 步驟 4： 另存為 PDF（A1a 合規性）

將 CAD 影像儲存為符合 A1a 規範的合規性 PDF。

```csharp
cadImage.Save(MyDir + "PDFA1_A.pdf", pdfOptions);
```

## 第 5 步：另存為 PDF（A1b 合規性）

將合規類型變更為 A1b 並將 CAD 影像儲存為合規 PDF。

```csharp
pdfOptions.CorePdfOptions.Compliance = PdfCompliance.PdfA1b;
cadImage.Save(MyDir + "PDFA1_B.pdf", pdfOptions);
```

## 結論

恭喜！您已使用 Aspose.CAD for .NET 成功將 DWG 檔案轉換為Compliance PDF。本教學為希望將 CAD 轉換功能整合到其應用程式中的開發人員提供了全面的指南。

## 常見問題解答

### Q1：我可以使用 Aspose.CAD 將其他 CAD 格式轉換為Compliance PDF 嗎？

A1：是的，Aspose.CAD 支援各種 CAD 格式，可以轉換為Compliance PDF。

### Q2：Aspose.CAD 與.NET Core 相容嗎？

A2：是的，Aspose.CAD 與 .NET Framework 和 .NET Core 相容。

### 問題 3：Aspose.CAD 是否有任何授權選項？

 A3：是的，您可以探索授權選項[這裡](https://purchase.aspose.com/buy).

### Q4：有免費試用嗎？

A4：是的，您可以獲得免費試用[這裡](https://releases.aspose.com/).

### Q5：我可以在哪裡獲得 Aspose.CAD 的支援？

A5：訪問[Aspose.CAD論壇](https://forum.aspose.com/c/cad/19)任何與支援相關的查詢。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
