---
title: 使用 ACAD 代理實體 - Aspose.CAD 指南
linktitle: 使用 ACAD 代理實體
second_title: Aspose.CAD .NET - CAD 和 BIM 檔案格式
description: 探索 Aspose.CAD for .NET 並簡化您的 CAD 工作流程。輕鬆轉換、編輯和管理 ACAD 代理實體。
type: docs
weight: 13
url: /zh-hant/net/layout-and-object-handling/working-with-acad-proxy-entities/
---
## 介紹

在 .NET 開發的動態世界中，建立和管理 CAD 繪圖是一項關鍵任務。 Aspose.CAD for .NET 為使用 AutoCAD 代理實體提供了強大的解決方案。本指南將引導您完成利用 Aspose.CAD 的強大功能並簡化 CAD 相關工作流程的基本步驟。

## 先決條件

在深入學習本教學之前，請確保您已具備以下條件：

-  Aspose.CAD 函式庫：從下列位置下載並安裝適用於 .NET 的 Aspose.CAD 函式庫：[下載頁面](https://releases.aspose.com/cad/net/).

- 開發環境：在您的電腦上設定一個有效的 .NET 開發環境。

-  CAD 檔案：準備用於測試的範例 CAD 檔案。在本指南中，我們將使用位於變數指定的目錄中名為「conic_pyramid.dxf」的文件`MyDir`.

## 導入命名空間

首先，請確保在 .NET 專案中包含必要的命名空間。這些命名空間提供對使用 Aspose.CAD 所需的類別和方法的存取。

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## 第 1 步：載入 CAD 文件

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    //您的進一步步驟的程式碼將位於此處。
}
```

## 第 2 步：配置光柵化選項

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.UnitType = UnitType.Inch;
rasterizationOptions.DrawType = CadDrawTypeMode.UseObjectColor;
rasterizationOptions.BackgroundColor = Color.Black;
rasterizationOptions.Layouts = new string[] { "Model" };
```

## 步驟 3：設定 PDF 轉換選項

```csharp
PdfOptions pdfOptions = new PdfOptions
{
    VectorRasterizationOptions = rasterizationOptions
};
```

## 步驟 4：將輸出另存為 PDF

```csharp
cadImage.Save(MyDir + "output.pdf", pdfOptions);
```

透過執行下列步驟，您可以使用 Aspose.CAD for .NET 有效率地處理 ACAD 代理實體。請隨意根據您的具體要求自訂程式碼並探索[文件](https://reference.aspose.com/cad/net/)了解更多詳情。

## 結論

總而言之，掌握 Aspose.CAD for .NET 可讓您無縫處理 CAD 文件，從而增強您的 .NET 開發工作流程。提供的指南簡化了使用 ACAD 代理實體的過程，確保開發人員獲得流暢的體驗。

## 常見問題解答

### Q1：我可以將 Aspose.CAD for .NET 與其他 CAD 檔案格式一起使用嗎？

A1：是的，Aspose.CAD支援各種CAD格式，包括DWG和DXF。

### 問題 2：Aspose.CAD for .NET 有試用版嗎？

 A2：是的，您可以透過免費試用來探索這些功能[這裡](https://releases.aspose.com/).

### 問題 3：在哪裡可以獲得 Aspose.CAD for .NET 的支援？

 A3：訪問[Aspose.CAD論壇](https://forum.aspose.com/c/cad/19)任何與支援相關的查詢。

### 問題 4：如何取得 Aspose.CAD for .NET 的臨時授權？

 A4：您可以獲得臨時許可證[這裡](https://purchase.aspose.com/temporary-license/).

### 問題 5：在哪裡可以購買 Aspose.CAD for .NET 的完整授權？

A5：您可以從[購買頁面](https://purchase.aspose.com/buy).