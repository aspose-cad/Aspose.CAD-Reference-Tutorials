---
title: 匯出為 BMP 格式 - Aspose.CAD 教學課程
linktitle: 匯出為 BMP 格式
second_title: Aspose.CAD .NET - CAD 和 BIM 檔案格式
description: 使用 Aspose.CAD for .NET 探索將 3D 影像匯出為 BMP 的無縫世界。按照我們的教程獲得無憂的體驗。
weight: 11
url: /zh-hant/net/file-format-conversion/exporting-to-bmp-format/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 匯出為 BMP 格式 - Aspose.CAD 教學課程

## 介紹

在軟體開發的動態世界中，Aspose.CAD for .NET 作為處理電腦輔助設計 (CAD) 檔案的強大工具脫穎而出。如果您希望將 CAD 影像匯出為廣泛使用的 BMP 格式，本教學是您的首選指南。在本逐步演練中，我們將探索使用 Aspose.CAD for .NET 將 3D 影像匯出為 BMP 的過程。讓我們深入了解吧！

## 先決條件

在開始本教學之前，請確保您具備以下先決條件：

-  Aspose.CAD for .NET：從下列位置下載並安裝 Aspose.CAD 函式庫：[這裡](https://releases.aspose.com/cad/net/).
- 開發環境：建置.NET開發環境。
- CAD 檔案：準備好用於匯出的 CAD 檔案。在此範例中，我們將使用“18-12-11 9644 - site.dwf”。

## 導入命名空間

在您的 .NET 專案中，確保導入必要的命名空間：

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
```

## 第 1 步：載入 CAD 映像

首先將 CAD 圖像載入到您的專案中。將“您的文檔目錄”替換為實際目錄路徑。

```csharp
string MyDir = "Your Document Directory";
string inputFile = MyDir + "18-12-11 9644 - site.dwf";

using (Image image = Image.Load(inputFile))
{
    //您載入圖片的程式碼位於此處
}
```

## 步驟 2：配置 BMP 匯出選項

設定 BMP 匯出選項，包括 CAD 檔案的向量光柵化選項。

```csharp
BmpOptions bmpOptions = new BmpOptions();
var dwfRasterizationOptions = new CadRasterizationOptions();
bmpOptions.VectorRasterizationOptions = dwfRasterizationOptions;

dwfRasterizationOptions.PageHeight = 500;
dwfRasterizationOptions.PageWidth = 500;
```

## 第 3 步：匯出為 BMP

執行匯出過程，指定 BMP 檔案的輸出路徑。

```csharp
string outPath = MyDir + "18-12-11 9644 - site.bmp";
image.Save(outPath, bmpOptions);
```

## 結論

恭喜！您已使用 Aspose.CAD for .NET 成功將 3D 影像匯出為 BMP。本教學讓您了解 Aspose.CAD 的多功能性，讓複雜的任務變得輕而易舉。

## 常見問題解答

### Q1：我可以將 Aspose.CAD for .NET 與任何 CAD 檔案格式一起使用嗎？

A1：是的，Aspose.CAD 支援各種 CAD 檔案格式，為您的專案提供靈活性。

### Q2：臨時許可證是否可用於測試目的？

 A2：當然！您可以獲得臨時許可證[這裡](https://purchase.aspose.com/temporary-license/)進行評估。

### 問題 3：在哪裡可以找到 Aspose.CAD 的綜合文件？

 A3：參考文檔[這裡](https://reference.aspose.com/cad/net/)取得詳細資訊和範例。

### Q4：我如何尋求支持或與社區連結？

 A4：造訪 Aspose.CAD 論壇[這裡](https://forum.aspose.com/c/cad/19)提出問題並與社區互動。

### Q5：我可以購買 Aspose.CAD for .NET 嗎？

 A5: 是的，您可以購買Aspose.CAD[這裡](https://purchase.aspose.com/buy)為您的專案釋放其全部潛力。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
