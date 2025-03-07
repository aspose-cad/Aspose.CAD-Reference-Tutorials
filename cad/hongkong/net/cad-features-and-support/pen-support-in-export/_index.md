---
title: 使用 Aspose.CAD for .NET 中的自訂筆選項提升 CAD 匯出功能
linktitle: 匯出中的筆支持
second_title: Aspose.CAD .NET - CAD 和 BIM 檔案格式
description: 了解如何使用 Aspose.CAD for .NET 增強 CAD 影像匯出功能。自訂筆選項，以 PDF、PNG、BMP 等格式呈現令人驚嘆的視覺效果。
weight: 12
url: /zh-hant/net/cad-features-and-support/pen-support-in-export/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.CAD for .NET 中的自訂筆選項提升 CAD 匯出功能

## 介紹

Aspose.CAD for .NET 提供了一套強大的工具來處理電腦輔助設計 (CAD) 文件，使開發人員能夠無縫地操作和匯出 CAD 影像。一項值得注意的功能是匯出過程中的筆支持，允許用戶在將CAD 影像匯出為PDF、PNG、BMP、GIF、JPEG2000、JPEG、PSD、TIFF 和WMF 等各種格式時自訂筆的起始和結束設定。

在本教程中，我們將深入研究使用 Aspose.CAD for .NET 匯出時筆支援的細節。我們將分解每個步驟，提供清晰的解釋和範例來引導您完成整個過程。

## 先決條件

在我們深入學習本教程之前，請確保您具備以下先決條件：

- Aspose.CAD for .NET 安裝在您的開發環境中。您可以從[發布頁面](https://releases.aspose.com/cad/net/).

- 對 CAD 檔案格式，特別是 DXF（繪圖交換格式）有基本的了解。

- C# 程式語言的應用知識。

## 導入命名空間

首先，請確保在 C# 專案中匯入必要的命名空間：

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Drawing;
using System.Drawing.Drawing2D;
```

## 第 1 步：設定您的文件目錄

定義 CAD 文檔所在的目錄：

```csharp
string MyDir = "Your Document Directory";
```

## 第 2 步：載入 CAD 映像

使用 Aspose.CAD 載入 CAD 影像：

```csharp
string sourceFilePath = MyDir + "conic_pyramid.dxf";
CadImage cadImage = (CadImage)Image.Load(sourceFilePath);
```

## 步驟 3：配置光柵化選項

建立光柵化和 PDF 選項來自訂匯出流程：

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
PdfOptions pdfOptions = new PdfOptions();
```

## 第 4 步：自訂筆選項

設定筆的開始和結束選項：

```csharp
rasterizationOptions.PenOptions = new PenOptions
{
   StartCap = LineCap.Flat,
   EndCap = LineCap.Flat
};
```

## 第 5 步：應用向量光柵化選項

將光柵化選項套用到 PDF 選項：

```csharp
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## 第6步：儲存匯出的PDF

將具有自訂筆選項的 CAD 影像儲存為 PDF 檔案：

```csharp
cadImage.Save(MyDir + "9LHATT-A56_generated.pdf", pdfOptions);
```

## 結論

在本教學中，我們探討了 Aspose.CAD for .NET 匯出功能中的筆支援。透過遵循逐步指南，您可以輕鬆自訂筆的起始端蓋設置，從而增強 CAD 影像匯出的靈活性。

請隨意嘗試不同的筆選項，以在匯出的影像中實現所需的視覺效果。

## 常見問題解答

### Q1：我可以將這些筆選項用於 PDF 以外的其他影像格式嗎？

A1：是的，筆選項可以應用於各種影像格式，例如 PNG、BMP、GIF、JPEG 等。

### 問題 2：在哪裡可以找到 Aspose.CAD for .NET 的附加文件？

 A2：請參閱[文件](https://reference.aspose.com/cad/net/)獲取全面的資訊和範例。

### 問題 3：Aspose.CAD for .NET 是否有免費試用版？

 A3：是的，您可以免費試用[這裡](https://releases.aspose.com/).

### 問題 4：如何取得 Aspose.CAD for .NET 的臨時授權？

 A4：訪問[臨時許可證頁面](https://purchase.aspose.com/temporary-license/)用於臨時許可選項。

### 問題 5：我可以在哪裡尋求 Aspose.CAD for .NET 的社群支援？

 A5：與社區互動[Aspose.CAD論壇](https://forum.aspose.com/c/cad/19).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
