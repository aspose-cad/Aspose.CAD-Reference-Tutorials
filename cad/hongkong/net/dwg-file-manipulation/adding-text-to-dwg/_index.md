---
title: 在 C# 中將文字新增至 DWG 檔案 - Aspose.CAD 教學課程
linktitle: 在 C# 中向 DWG 文件添加文本
second_title: Aspose.CAD .NET - CAD 和 BIM 檔案格式
description: 了解如何使用 C# 和 Aspose.CAD 將文字新增至 DWG 檔案。請按照此逐步教學進行無縫整合。瀏覽 Aspose.CAD 文件以獲得全面的指導。
weight: 14
url: /zh-hant/net/dwg-file-manipulation/adding-text-to-dwg/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 C# 中將文字新增至 DWG 檔案 - Aspose.CAD 教學課程

## 介紹

在電腦輔助設計 (CAD) 和 .NET 開發的動態領域中，Aspose.CAD 作為操作 DWG 檔案的強大工具脫穎而出。在 DWG 檔案中新增文字是一項常見要求，在本教學中，我們將探討如何使用 C# 和 Aspose.CAD 來實現此目的。

## 先決條件

在深入學習本教學之前，請確保您已具備以下條件：

-  Aspose.CAD 函式庫：從下列位置下載並安裝 Aspose.CAD 函式庫：[下載連結](https://releases.aspose.com/cad/net/).

- 文檔目錄：為您的文件設定一個目錄，並將其路徑記為`MyDir`.

現在，讓我們將該流程分解為可管理的步驟。

## 導入命名空間

在您的 C# 程式碼中，包含存取 Aspose.CAD 功能所需的命名空間。

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects.AttEntities;
using Aspose.CAD.ImageOptions;
```

## 步驟 1： 載入 DWG 文件

將 DWG 檔案載入到`Image`使用 Aspose.CAD 庫的物件。

```csharp
string dwgPathToFile = MyDir + "SimpleEntites.dwg";
using (Image image = Image.Load(dwgPathToFile))
{
    //您後續步驟的代碼位於此處
}
```

## 第 2 步：建立 CadText 對象

實例化一個`CadText`物件來表示要新增到 DWG 檔案的文字。

```csharp
CadText cadText = new CadText();
cadText.StyleType = "Standard";
cadText.DefaultValue = "Some custom text";
cadText.ColorId = 256;
cadText.LayerName = "0";
cadText.FirstAlignment.X = 47.90;
cadText.FirstAlignment.Y = 5.56;
cadText.TextHeight = 0.8;
cadText.ScaleX = 0.0;
```

## 步驟 3：將文字加入 DWG

新增創建的`CadText`使用 Aspose.CAD 將物件轉換為 DWG 檔案。

```csharp
CadImage cadImage = (CadImage)image;
cadImage.BlockEntities["*Model_Space"].AddEntity(cadText);
```

## 步驟 4：配置 PDF 選項

配置 PDF 選項以將修改後的 DWG 檔案儲存為 PDF。

```csharp
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.VectorRasterizationOptions = cadRasterizationOptions;
cadRasterizationOptions.DrawType = CadDrawTypeMode.UseObjectColor;
cadRasterizationOptions.PageHeight = 1600;
cadRasterizationOptions.PageWidth = 1600;
cadRasterizationOptions.Layouts = new string[] { "Model" };
```

## 第 5 步：另存為 PDF

將修改後的 DWG 檔案儲存為具有新增文字的 PDF。

```csharp
image.Save(MyDir + "SimpleEntites_generated.pdf", pdfOptions);
```

現在，您已使用 C# 和 Aspose.CAD 成功將文字新增至 DWG 檔案。請隨意探索 Aspose.CAD 的更多特性和功能，以滿足您的 CAD 操作需求。

## 結論

在本教程中，我們介紹了使用 C# 和 Aspose.CAD 將文字新增至 DWG 檔案的基本步驟。這種強大的組合為動態和自訂 CAD 文檔產生提供了可能性。

## 常見問題解答

### Q1：Aspose.CAD 是否相容於所有版本的 DWG 檔案？

A1：Aspose.CAD支援多種DWG檔案版本，確保與各種CAD軟體的兼容性。

### 問題 2：我可以使用 Aspose.CAD 將多個文字實體新增到單一 DWG 檔案中嗎？

A2：是的，您可以透過重複教學中概述的過程將多個文字實體新增至 DWG 檔案中。

### Q3：如何更改Aspose.CAD中的文字字體和樣式？

 A3：若要修改文字字體和樣式，請調整文字的屬性`CadText`對象，然後將其新增至 DWG 檔案。

### Q4：在商業專案中使用 Aspose.CAD 是否有任何許可注意事項？

 A4：是的，確保遵守 Aspose.CAD 授權條款。參考[Aspose.CAD 購買](https://purchase.aspose.com/buy)了解詳情。

### Q5：我可以在哪裡尋求協助或討論與 Aspose.CAD 相關的問題？

A5：訪問[Aspose.CAD論壇](https://forum.aspose.com/c/cad/19)與社區聯繫並獲得支持。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
