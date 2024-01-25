---
title: 在 Aspose.CAD for .NET 中將 DGN 匯出為 DWG 的一部分
linktitle: 將 DGN 匯出為 DWG 的一部分
second_title: Aspose.CAD .NET - CAD 和 BIM 檔案格式
description: 了解如何在 Aspose.CAD for .NET 中將 DGN 匯出為 DWG 的一部分。請按照我們的逐步指南進行無縫整合。
type: docs
weight: 11
url: /zh-hant/net/cad-export-formats/export-dgn-as-part-of-dwg/
---
## 介紹

在 .NET 開發領域，Aspose.CAD 作為處理電腦輔助設計 (CAD) 檔案的強大程式庫而脫穎而出。本教學將引導您完成使用 Aspose.CAD for .NET 將 DGN（設計）檔案匯出為 DWG（圖面）檔案的一部分的流程。無論您是經驗豐富的開發人員還是新手，本逐步指南都將幫助您利用 Aspose.CAD 的功能有效率地完成此特定任務。

## 先決條件

在深入學習本教程之前，請確保您具備以下先決條件：

-  Aspose.CAD for .NET：確保您已安裝 Aspose.CAD for .NET 程式庫。你可以下載它[這裡](https://releases.aspose.com/cad/net/).

- 開發環境：設定您首選的 .NET 開發環境，例如 Visual Studio。

- C# 基礎知識：熟悉 C# 程式語言。

## 導入命名空間

在您的 C# 專案中，包含存取 Aspose.CAD 功能所需的命名空間。在程式碼檔案的開頭加入以下 using 指令：

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

現在，讓我們將提供的程式碼分解為多個步驟：

## 第 1 步：定義檔路徑

```csharp
//輸入和輸出檔案路徑
string fileName = "BlockRefDgn.dwg";
string outPath = fileName + ".pdf";
```

## 步驟2：建立PdfOptions實例

```csharp
//建立 PdfOptions 類別的實例以將 DWG 匯出為 PDF
PdfOptions exportOptions = new PdfOptions();
```

## 步驟 3： 載入 DWG 文件

```csharp
//將現有 DWG 檔案作為映像載入並將其轉換為 CadImage 類型
using (CadImage cadImage = (CadImage)Image.Load(fileName))
```

## 第 4 步：迭代實體

```csharp
//迭代 DWG 檔案中的每個實體
foreach (CadBaseEntity baseEntity in cadImage.Entities)
```

## 第 5 步：檢查實體類型

```csharp
//檢查實體是否為影像定義
if (baseEntity.TypeName == CadEntityTypeName.DGNUNDERLAY)
```

## 第6步：取得底層路徑

```csharp
//如果是影像定義，則取得物件的外部引用
CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
Console.WriteLine(dgnFile.UnderlayPath);
```

## 第 7 步：定義光柵化選項

```csharp
//定義 CadRasterizationOptions 物件的設置
exportOptions.VectorRasterizationOptions = new CadRasterizationOptions()
{
    PageWidth = 1600,
    PageHeight = 1600,
    Layouts = new string[] { "Model" },
    AutomaticLayoutsScaling = false,
    NoScaling = true,
    BackgroundColor = Color.Black,
    DrawType = CadDrawTypeMode.UseObjectColor
};
```

## 步驟 8：將 DWG 匯出為 PDF

```csharp
//透過呼叫 Save 方法將 DWG 匯出為 PDF
cadImage.Save(outPath, exportOptions);
```

## 結論

恭喜！您已成功完成使用 Aspose.CAD for .NET 將 DGN 檔案匯出為 DWG 檔案的一部分的過程。本教學為您提供了無縫完成此特定任務的基本步驟和程式碼片段。

## 常見問題解答

### Q1：我可以在我的商業專案中使用 Aspose.CAD for .NET 嗎？
 A1: 是的，可以。訪問[這裡](https://purchase.aspose.com/buy)探索許可證選項。

### 問題 2：我可以處理的 DWG 檔案的大小有限制嗎？
A2：Aspose.CAD 支援處理大型 DWG 文件，但可能有硬體限制。

### Q3：有試用版嗎？
A3：是的，您可以獲得免費試用[這裡](https://releases.aspose.com/).

### Q4：如何取得臨時許可證？
 A4：可以獲得臨時許可證[這裡](https://purchase.aspose.com/temporary-license/).

### Q5：如果遇到問題，我可以到哪裡尋求協助？
 A5：您可以造訪Aspose.CAD論壇[這裡](https://forum.aspose.com/c/cad/19)為了支持。