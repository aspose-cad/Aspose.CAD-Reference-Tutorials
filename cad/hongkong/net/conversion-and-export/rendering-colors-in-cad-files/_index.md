---
title: 在 CAD 檔案中渲染顏色 - Aspose.CAD 指南
linktitle: 在 CAD 檔案中渲染顏色
second_title: Aspose.CAD .NET - CAD 和 BIM 檔案格式
description: 使用 Aspose.CAD 掌握 .NET 中 CAD 檔案渲染。按照我們的分步指南獲得鮮豔的色彩。
weight: 10
url: /zh-hant/net/conversion-and-export/rendering-colors-in-cad-files/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 CAD 檔案中渲染顏色 - Aspose.CAD 指南

## 介紹

您是否正在應對使用 .NET 在 CAD 檔案中渲染顏色的挑戰？別再猶豫了！在這份綜合指南中，我們將引導您使用強大的 Aspose.CAD 函式庫逐步完成流程。學完本教學後，您將掌握在 CAD 檔案中輕鬆渲染顏色的知識。

## 先決條件

在我們深入學習本教程之前，請確保您具備以下先決條件：

-  Aspose.CAD 函式庫：從下列位置下載並安裝 Aspose.CAD 函式庫：[這裡](https://releases.aspose.com/cad/net/).

- 開發環境：確保您已設定 .NET 開發環境。

- CAD 檔案：準備好範例 CAD 檔案以供測試。您可以在本教學中使用“test1.dwg”。

## 導入命名空間

在您的 .NET 專案中，匯入必要的命名空間以存取 Aspose.CAD 功能。在程式碼開頭新增以下行：

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

## 第 1 步：設定您的項目

建立一個新的 .NET 專案並設定所需的目錄。確保您的專案中引用了 Aspose.CAD 庫。

## 第 2 步：定義檔路徑

指定輸入 CAD 檔案和輸出 PNG 檔案的路徑。更新程式碼中的以下行：

```csharp
string MyDir = "Your Document Directory";
string inputFile = MyDir + "test1.dwg";
string outputFile = MyDir + "test1.png";
```

## 第 3 步：載入 CAD 文件

使用以下程式碼開啟並載入 CAD 檔案：

```csharp
using (FileStream fs = new FileStream(inputFile, FileMode.Open))
{
    using (FileStream output = new FileStream(outputFile, FileMode.Create))
    {
        Image document = Image.Load(fs);
```

## 步驟 4：配置光柵化選項

配置光柵化選項以自訂渲染過程。更新以下幾行：

```csharp
PngOptions saveOptions = new PngOptions();

CadRasterizationOptions options = new CadRasterizationOptions();
options.NoScaling = false;
options.PageHeight = document.Height * 10;
options.PageWidth = document.Width * 10;
options.DrawType = Aspose.CAD.FileFormats.Cad.CadDrawTypeMode.UseObjectColor;
saveOptions.VectorRasterizationOptions = options;
```

## 第5步：儲存渲染影像

使用指定選項儲存渲染影像：

```csharp
document.Save(output, saveOptions);
```

## 結論

恭喜！您已使用 Aspose.CAD for .NET 成功渲染了 CAD 檔案中的顏色。本逐步指南為您提供了增強 CAD 渲染能力的技巧。

## 常見問題解答

### Q1：我可以免費使用Aspose.CAD嗎？

 A1：Aspose.CAD提供免費試用版可用[這裡](https://releases.aspose.com/)。您可以在購買前探索其功能。

### Q2：哪裡可以找到Aspose.CAD的詳細文件？

A2：參考文檔[這裡](https://reference.aspose.com/cad/net/)有關 Aspose.CAD 功能的深入資訊。

### 問題 3：如何取得 Aspose.CAD 的臨時許可？

 A3：獲得臨時許可證[這裡](https://purchase.aspose.com/temporary-license/)用於測試目的。

### Q4：需要協助或有疑問嗎？

 A4：參觀 Aspose.CAD 社區[論壇](https://forum.aspose.com/c/cad/19)以尋求支持和討論。

### Q5：哪裡可以購買Aspose.CAD庫？

 A5：購買Aspose.CAD[這裡](https://purchase.aspose.com/buy)釋放其全部潛力。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
