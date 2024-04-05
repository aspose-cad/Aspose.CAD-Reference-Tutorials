---
title: 在 C# 中使用座標將 DWG 轉換為 PDF - Aspose.CAD 教學課程
linktitle: 在 C# 中使用座標將 DWG 轉換為 PDF
second_title: Aspose.CAD .NET - CAD 和 BIM 檔案格式
description: 了解如何使用 Aspose.CAD 在 C# 中將 DWG 轉換為具有特定座標的 PDF。按照我們的逐步指南進行精確且有效率的 CAD 檔案轉換。
type: docs
weight: 11
url: /zh-hant/net/conversion-and-export/converting-dwg-to-pdf-with-coordinates/
---
## 介紹

歡迎閱讀這個關於使用 Aspose.CAD for .NET 將 DWG 檔案轉換為具有指定座標的 PDF 的綜合教學。 Aspose.CAD 是一個功能強大的程式庫，允許開發人員在其 .NET 應用程式中無縫地使用 CAD 檔案格式。在本教程中，我們將引導您完成將 DWG 檔案轉換為 PDF 的過程，同時提供特定座標以提高精確度。

## 先決條件

在我們開始之前，請確保您具備以下先決條件：

- Aspose.CAD 函式庫：下載並安裝適用於 .NET 的 Aspose.CAD 函式庫。你可以找到圖書館[這裡](https://releases.aspose.com/cad/net/).

- 開發環境：確保您設定了相容的開發環境，包括 Visual Studio 或任何其他首選 IDE。

- DWG 檔：準備好 DWG 檔以轉換。您可以使用提供的範例檔案或自訂 DWG 檔案。

## 導入命名空間

在您的 C# 專案中，匯入必要的命名空間：

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadParameters;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.ImageOptions;
```

讓我們將程式碼分解為逐步指南，以便更好地理解：

## 第 1 步：定義文檔目錄

```csharp
string MyDir = "Your Document Directory";
```

## 步驟 2：設定來源 DWG 檔案路徑

```csharp
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";
```

## 步驟 3：載入 DWG 檔案並配置光柵化選項

```csharp
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
    rasterizationOptions.Layouts = new string[] { "Model" };
    rasterizationOptions.NoScaling = true;
```

## 第 4 步：定義座標和視口

```csharp
    Point topLeft = new Point(500, 1000);
    double width = 3108;
    double height = 2489;

    CadVportTableObject newView = new CadVportTableObject();
    newView.Name = new CadStringParameter();
    newView.Name.Init("*Active");
    newView.CenterPoint.X = topLeft.X + width / 2f;
    newView.CenterPoint.Y = topLeft.Y - height / 2f;
    newView.ViewHeight.Value = height;
    newView.ViewAspectRatio.Value = width / height;
```

## 第 5 步：應用視窗設置

```csharp
    for (int i = 0; i < cadImage.ViewPorts.Count; i++)
    {
        CadVportTableObject currentView = (CadVportTableObject)(cadImage.ViewPorts[i]);
        if (cadImage.ViewPorts.Count == 1 || string.Equals(currentView.Name.Value.ToLowerInvariant(), "*active"))
        {
            cadImage.ViewPorts[i] = newView;
            break;
        }
    }
```

## 第 6 步：配置 PDF 選項並匯出

```csharp
    Aspose.CAD.ImageOptions.PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions();
    pdfOptions.VectorRasterizationOptions = rasterizationOptions;

    MyDir = MyDir + "ConvertDWGToPDFBySupplyingCoordinates_out.pdf";
    cadImage.Save(MyDir, pdfOptions);
}
```

## 步驟7：顯示成功訊息

```csharp
Console.WriteLine("\nThe DWG file exported successfully to PDF.\nFile saved at " + MyDir);
```

## 結論

恭喜！您已使用 Aspose.CAD for .NET 成功將 DWG 檔案轉換為具有指定座標的 PDF。本教程涵蓋了基本步驟，並為開發人員提供了清晰的指南。

## 常見問題解答

### Q1：我可以將 Aspose.CAD 與其他 CAD 檔案格式一起使用嗎？

A1：是的，Aspose.CAD支援各種CAD格式，包括DWG、DXF、DWF等。

### Q2：轉換過程中出現錯誤如何處理？

A2：使用 try-catch 區塊實作錯誤處理機制來擷取和管理異常。

### Q3：Aspose.CAD同時適用於Windows和Linux環境嗎？

A3：是的，Aspose.CAD 相容於 Windows 和 Linux 平台。

### Q4：我可以進一步客製化PDF輸出嗎？

A4：當然！探索 Aspose.CAD 提供的廣泛選項，根據您的特定要求自訂 PDF 輸出。

### 問題 5：我可以在哪裡找到其他支持或社區討論？

A5：訪問[Aspose.CAD論壇](https://forum.aspose.com/c/cad/19)以獲得社區支持和討論。