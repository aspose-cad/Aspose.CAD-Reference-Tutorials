---
title: 探索 DWG 檔案的底層標誌 - Aspose.CAD 教學課程
linktitle: 探索 DWG 檔案的參考底圖標記
second_title: Aspose.CAD .NET - CAD 和 BIM 檔案格式
description: 釋放 Aspose.CAD for .NET 在探索 DWG 檔案底層標記方面的強大功能。請遵循我們的逐步指南。
weight: 13
url: /zh-hant/net/dwg-file-manipulation/exploring-underlay-flags-of-dwg/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 探索 DWG 檔案的底層標誌 - Aspose.CAD 教學課程

## 介紹

如果您正在深入研究 CAD 檔案（特別是 DWG 檔案）的複雜世界，並且想要解開底層標誌的神秘面紗，那麼您來對地方了。本教學將引導您完成使用強大的 Aspose.CAD for .NET 程式庫探索 DWG 檔案中的底層標誌的過程。

## 先決條件

在我們深入學習本教學之前，請確保您具備以下條件：

- 對 C# 和 .NET 程式設計有基本了解。
- 安裝了 Aspose.CAD for .NET 函式庫。如果沒有的話可以下載[這裡](https://releases.aspose.com/cad/net/).
- 用於測試的 DWG 檔。您可以使用教程中提供的範例檔案“BlockRefDgn.dwg”。

## 導入命名空間

首先，您需要匯入必要的命名空間。這是一個可以幫助您的片段：

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;

```

## 步驟 1： 載入 DWG 檔案並轉換為 CadImage

首先載入現有的 DWG 檔案並將其轉換為 CadImage：

```csharp
string fileName = MyDir + "BlockRefDgn.dwg";

//載入 DWG 檔案並轉換為 CadImage
using (CadImage image = (CadImage)Image.Load(fileName))
{
    //您後續步驟的代碼將位於此處
}
```

## 第 2 步：迭代實體

接下來，迭代 DWG 檔案中的每個實體：

```csharp
foreach (CadBaseEntity entity in image.Entities)
{
    //您後續步驟的代碼將位於此處
}
```

## 步驟 3：檢查 CadDgnUnderlay 類型

檢查實體是否為 CadDgnUnderlay 類型：

```csharp
if (entity is CadDgnUnderlay)
{
    //您後續步驟的代碼將位於此處
}
```

## 第 4 步：訪問底層標誌

訪問不同的底層標誌並提取相關資訊：

```csharp
CadUnderlay underlay = entity as CadUnderlay;

Console.WriteLine(underlay.UnderlayPath);
Console.WriteLine(underlay.UnderlayName);
Console.WriteLine(underlay.InsertionPoint.X);
Console.WriteLine(underlay.InsertionPoint.Y);
Console.WriteLine(underlay.RotationAngle);
Console.WriteLine(underlay.ScaleX);
Console.WriteLine(underlay.ScaleY);
Console.WriteLine(underlay.ScaleZ);
Console.WriteLine((underlay.Flags & UnderlayFlags.UnderlayIsOn) == UnderlayFlags.UnderlayIsOn);
Console.WriteLine((underlay.Flags & UnderlayFlags.ClippingIsOn) == UnderlayFlags.ClippingIsOn);
Console.WriteLine((underlay.Flags & UnderlayFlags.Monochrome) != UnderlayFlags.Monochrome);
```

## 結論

恭喜！您已使用 Aspose.CAD for .NET 成功探索了 DWG 檔案的底層標記。本教程為您提供了導航實體和提取有關底層的重要資訊的知識。

## 常見問題解答

### Q1：我可以將 Aspose.CAD for .NET 與其他 CAD 檔案格式一起使用嗎？

A1：Aspose.CAD支援多種CAD格式，包括DWG、DXF、DGN等。檢查文件以取得完整清單。

### 問題 2：Aspose.CAD for .NET 是否有臨時授權？

 A2：是的，您可以獲得臨時許可證[這裡](https://purchase.aspose.com/temporary-license/).

### 問題 3：在哪裡可以找到對 Aspose.CAD for .NET 的支援？

 A3：造訪支援論壇[這裡](https://forum.aspose.com/c/cad/19)尋求幫助。

### Q4：如何購買 Aspose.CAD for .NET？

A4：購買圖書館[這裡](https://purchase.aspose.com/buy).

### Q5: 有免費試用嗎？

 A5：是的，您可以免費試用[這裡](https://releases.aspose.com/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
