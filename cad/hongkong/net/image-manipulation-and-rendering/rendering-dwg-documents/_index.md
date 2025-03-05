---
title: 在 C# 中渲染 DWG 文件 - Aspose.CAD 指南
linktitle: 在 C# 渲染 DWG 文檔
second_title: Aspose.CAD .NET - CAD 和 BIM 檔案格式
description: 了解如何使用 Aspose.CAD 在 C# 中渲染 DWG 文件。本逐步指南涵蓋了匯入、設定和儲存程式碼範例。
type: docs
weight: 17
url: /zh-hant/net/image-manipulation-and-rendering/rendering-dwg-documents/
---
## 介紹

歡迎閱讀有關使用 Aspose.CAD 在 C# 中渲染 DWG 文件的綜合指南。無論您是經驗豐富的開發人員還是剛開始使用 .NET，本教學都會引導您完成利用 Aspose.CAD 高效渲染 DWG 檔案的過程。 Aspose.CAD 是一個強大的 API，提供了處理 CAD 檔案格式的強大功能，使其成為處理 DWG 檔案的開發人員的首選。

## 先決條件

在深入學習本教程之前，請確保您符合以下先決條件：

- C# 程式語言的基礎知識。
- Visual Studio 安裝在您的電腦上。
-  Aspose.CAD 庫整合到您的專案中。您可以從以下位置下載：[這裡](https://releases.aspose.com/cad/net/).
- 範例 DWG 文件，例如“Bottom_plate.dwg”，與範例一起使用。

## 導入命名空間

首先，請確保在 C# 程式碼的開頭匯入必要的命名空間：

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.FileFormats.Cad;
```

現在，讓我們將提供的範例分解為多個步驟：

## 步驟 1： 載入 DWG 文件

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    //用於載入 DWG 檔案的程式碼位於此處。
}
```

## 第 2 步：配置光柵化選項

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new string[] { "Model" };
rasterizationOptions.NoScaling = true;
//可以在此處新增其他光柵化配置。
```

## 第 3 步：定義要繪製的區域

```csharp
Point topLeft = new Point(6156, 7053);
double width = 3108;
double height = 2489;
```

## 第 4 步：建立新視口

```csharp
CadVportTableObject newView = new CadVportTableObject();
newView.Name.Value = "*Active";
newView.CenterPoint.X = topLeft.X + width / 2f;
newView.CenterPoint.Y = topLeft.Y - height / 2f;
newView.ViewHeight.Value = height;
newView.ViewAspectRatio.Value = width / height;
```

## 第 5 步：替換活動視口

```csharp
for (int i = 0; i < cadImage.ViewPorts.Count; i++)
{
    CadVportTableObject currentView = (CadVportTableObject)(cadImage.ViewPorts[i]);
    if ((currentView.Name.Value == null && cadImage.ViewPorts.Count == 1) ||
    string.Equals(currentView.Name.Value.ToLowerInvariant(), "*active"))
    {
        cadImage.ViewPorts[i] = newView;
        break;
    }
}
```

## 步驟 6：配置 PDF 選項

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## 步驟 7：將已渲染的 DWG 儲存為 PDF

```csharp
cadImage.Save(MyDir, pdfOptions);
```

## 結論

恭喜！您已使用 C# 中的 Aspose.CAD 成功將 DWG 文件渲染為 PDF。請隨意探索更多功能並根據您的特定要求自訂程式碼。

## 常見問題解答

### Q1：我可以將 Aspose.CAD 與其他 CAD 檔案格式一起使用嗎？

A1：是的，Aspose.CAD支援各種CAD格式，包括DWG、DXF、DWF等。

### Q2：Aspose.CAD 與.NET Core 相容嗎？

A2：是的，Aspose.CAD 與 .NET Framework 和 .NET Core 相容。

### 問題 3：如何處理 DWG 檔案中的不同版面？

 A3：您可以在中指定所需的佈局`Layouts`的財產`CadRasterizationOptions`.

### 問題 4：使用 Aspose.CAD 是否有任何許可注意事項？

 A4：有關許可詳細信息，請訪問[這裡](https://purchase.aspose.com/buy).

### Q5：我可以在哪裡找到額外的支援？

A5：訪問[Aspose.CAD論壇](https://forum.aspose.com/c/cad/19)以獲得社區支持和討論。