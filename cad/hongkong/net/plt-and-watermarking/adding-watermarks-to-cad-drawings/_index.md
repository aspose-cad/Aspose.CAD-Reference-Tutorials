---
title: 在 CAD 繪圖中新增浮水印 - Aspose.CAD 指南
linktitle: 在 CAD 工程圖添加浮水印
second_title: Aspose.CAD .NET - CAD 和 BIM 檔案格式
description: 使用 Aspose.CAD for .NET 使用專業浮水印增強您的 CAD 繪圖。按照我們的逐步指南進行個性化和引人入勝的設計。
type: docs
weight: 11
url: /zh-hant/net/plt-and-watermarking/adding-watermarks-to-cad-drawings/
---
## 介紹

您是否希望透過添加專業浮水印來增強您的 CAD 繪圖？ Aspose.CAD for .NET 提供了一個強大的解決方案，可以將浮水印無縫整合到您的 CAD 檔案中。在本逐步指南中，我們將引導您完成使用 Aspose.CAD 新增浮水印的過程，確保您的繪圖不僅傳達關鍵訊息，而且帶有您獨特的標記。

## 先決條件

在深入學習本教學之前，請確保您具備以下條件：
-  Aspose.CAD for .NET：確保您已安裝 Aspose.CAD 程式庫。你可以下載它[這裡](https://releases.aspose.com/cad/net/).
- 您的文件目錄：設定目錄來儲存您的 CAD 圖面。
現在，讓我們開始為 CAD 繪圖添加浮水印！

## 導入命名空間

首先將必要的命名空間匯入到您的 .NET 專案中：

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## 第 1 步：載入 CAD 圖紙

```csharp
//文檔目錄的路徑。
string MyDir = "Your Document Directory";
using (CadImage cadImage = (CadImage)Image.Load(MyDir + "Drawing11.dwg")) {
```

## 第 2 步：添加浮水印作為 MTEXT

```csharp
//新增的多行文本
CadMText watermark = new CadMText();
watermark.Text = "Watermark message";
watermark.InitialTextHeight = 40;
watermark.InsertionPoint = new Cad3DPoint(300, 40);
watermark.LayerName = "0";
cadImage.BlockEntities["*Model_Space"].AddEntity(watermark);
```

## 第 3 步：或添加浮水印作為文本

```csharp
//或者，添加一個更簡單的實體，例如文本
CadText text = new CadText();
text.DefaultValue = "Watermark text";
text.TextHeight = 40;
text.FirstAlignment = new Cad3DPoint(300, 40);
text.LayerName = "0";
cadImage.BlockEntities["*Model_Space"].AddEntity(text);
```

## 第 4 步：匯出為 PDF

```csharp
//將帶有浮水印的CAD圖紙匯出為PDF
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.Layouts = new[] { "Model" };
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
cadImage.Save(MyDir + "AddWatermark_out.pdf", pdfOptions);
```

對不同的繪圖重複這些步驟，您很快就會擁有專業外觀的帶有浮水印的 CAD 檔案！

## 結論

恭喜！您已成功學習如何使用 Aspose.CAD for .NET 將浮水印新增至 CAD 繪圖。這個簡單而強大的過程可讓您個性化您的設計，同時保持技術圖的完整性。

## 常見問題解答

### Q1：我可以自訂浮水印的外觀嗎？

A1: 是的，您可以根據您的喜好自訂浮水印的文字、字體、大小和位置。

### Q2: Aspose.CAD 是否相容於不同的 CAD 檔案格式？

A2：Aspose.CAD支援各種CAD檔案格式，包括DWG和DXF，確保廣泛的兼容性。

### Q3：我可以在一張CAD圖紙上添加多個浮水印嗎？

A3：當然！您可以根據需要添加任意數量的浮水印，為不同的用例提供靈活性。

### Q4：Aspose.CAD 提供免費試用嗎？

A4：是的，您可以透過免費試用來探索 Aspose.CAD 的功能。得到它[這裡](https://releases.aspose.com/).

### Q5：在哪裡可以找到對 Aspose.CAD 的支援？

 A5：如有任何疑問或幫助，請訪問[Aspose.CAD論壇](https://forum.aspose.com/c/cad/19).