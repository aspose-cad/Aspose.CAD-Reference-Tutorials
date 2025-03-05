---
title: 使用 C# 將圖像匯入 DWG 檔案 - Aspose.CAD 指南
linktitle: 使用 C# 將圖像導入 DWG 文件
second_title: Aspose.CAD .NET - CAD 和 BIM 檔案格式
description: 了解使用 C# 和 Aspose.CAD for .NET 將圖片匯入 DWG 檔案。請按照我們的逐步指南進行無縫整合。
type: docs
weight: 11
url: /zh-hant/net/image-manipulation-and-rendering/importing-images-into-dwg/
---
## 介紹

在電腦輔助設計 (CAD) 領域，將影像合併到 DWG 檔案中是一項常見且關鍵的任務。 Aspose.CAD for .NET 提供了一組強大的工具來簡化此流程，使其可供 C# 開發人員使用。在本教程中，我們將逐步探索如何將圖像匯入 DWG 檔案。

## 先決條件

在深入了解本指南之前，請確保您具備以下條件：

- C# 程式設計基礎知識。
- 已安裝 Aspose.CAD for .NET。你可以下載它[這裡](https://releases.aspose.com/cad/net/).
- 開發環境建置完畢。

## 導入命名空間

確保在您的 C# 專案中包含必要的命名空間：

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## 第 1 步：設定您的文件目錄

```csharp
string MyDir = "Your Document Directory";
```

## 步驟 2： 載入 DWG 文件

```csharp
string dwgPathToFile = MyDir + "Drawing11.dwg";
CadImage cadImage1 = (CadImage)Image.Load(dwgPathToFile);
```

## 第 3 步：定義圖像屬性

```csharp
CadRasterImageDef cadRasterImageDef = new CadRasterImageDef("road-sign-custom.png", 640, 562);
cadRasterImageDef.ObjectHandle = "A3B4";
```

## 第 4 步：設定插入點和向量

```csharp
Cad3DPoint insertionPoint = new Cad3DPoint(26.77, 22.35);
Cad3DPoint uVector = new Cad3DPoint(0.0061565450840500831, 0);
Cad3DPoint vVector = new Cad3DPoint(0, 0.0061565450840500822);
```

## 第 5 步：建立並配置光柵影像

```csharp
CadRasterImage cadRasterImage = new CadRasterImage(cadRasterImageDef, insertionPoint, uVector, vVector);
cadRasterImage.ImageDefReference = "A3B4";
cadRasterImage.DisplayFlags = 7;
cadRasterImage.ClippingState = 0;
cadRasterImage.ClipBoundaryVertexList.Add(new Cad2DPoint(-0.5, 0.5));
cadRasterImage.ClipBoundaryVertexList.Add(new Cad2DPoint(639.5, 561.5));
```

## 第 6 步：將圖像新增至 DWG 文件

```csharp
CadImage cadImage = (CadImage)cadImage1;
cadImage.BlockEntities["*Model_Space"].AddEntity(cadRasterImage);

List<CadBaseObject> list = new List<CadBaseObject>(cadImage.Objects);
list.Add(cadRasterImageDef);
cadImage.Objects = list.ToArray();
```

## 第7步：另存為PDF

```csharp
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.VectorRasterizationOptions = cadRasterizationOptions;
cadRasterizationOptions.DrawType = CadDrawTypeMode.UseObjectColor;

cadRasterizationOptions.PageHeight = 1600;
cadRasterizationOptions.PageWidth = 1600;
cadRasterizationOptions.Layouts = new string[] { "Model" };
cadImage1.Save(MyDir + "export2.pdf", pdfOptions);
```

## 結論

使用 C# 和 Aspose.CAD for .NET 將圖像整合到 DWG 檔案中是一個無縫過程，使開發人員能夠輕鬆地使用視覺元素增強其 CAD 專案。

## 常見問題解答

### Q1：我可以將 Aspose.CAD for .NET 與其他程式語言一起使用嗎？

A1：Aspose.CAD 主要是為.NET 設計的，但Aspose 提供了各種程式語言的函式庫。

### 問題 2：Aspose.CAD for .NET 可以免費試用嗎？

 A2：是的，您可以探索免費試用[這裡](https://releases.aspose.com/).

### Q3：哪裡可以找到Aspose.CAD的詳細文件？

 A3：文檔可用[這裡](https://reference.aspose.com/cad/net/).

### 問題 4：如何取得 Aspose.CAD for .NET 的臨時授權？

 A4：參觀[這個連結](https://purchase.aspose.com/temporary-license/)獲得臨時許可證。

### Q5：有 Aspose.CAD 支援的社群論壇嗎？

 A5：是的，您可以尋求支持並參與社區[這裡](https://forum.aspose.com/c/cad/19).