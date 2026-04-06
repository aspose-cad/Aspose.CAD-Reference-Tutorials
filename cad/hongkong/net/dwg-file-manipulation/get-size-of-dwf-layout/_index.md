---
date: 2026-04-06
description: 學習如何在 C# 中使用 Aspose.CAD 將 DWF 轉換為 JPG，並了解如何從 DWG 檔案中提取 DWF 版面尺寸。
keywords:
- convert dwf to jpg
- how to extract dwf
- convert dwg to jpg
linktitle: 在 C# 中處理 DWG 檔案 - 取得 DWF 版面尺寸
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: 在 C# 中將 DWF 轉換為 JPG – 從 DWG 取得 DWF 版面尺寸
url: /zh-hant/net/dwg-file-manipulation/get-size-of-dwf-layout/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 C# 中將 DWF 轉換為 JPG – 從 DWG 取得 DWF 版面尺寸

## 介紹

如果您需要 **convert DWF to JPG** 同時找出精確的版面尺寸，您來對地方了。在本教學中，我們將示範一個完整的端對端範例，使用 Aspose.CAD for .NET 開啟由 DWG 產生的 DWF 檔案，讀取每個版面的尺寸，並將版面儲存為高品質的 JPG 圖像。完成後，您不僅會知道如何提取 DWF 版面資訊，還能取得可直接放入任何 C# 專案的可重用程式碼片段。

## 快速解答
- **What does “convert DWF to JPG” mean?** 它表示將向量 DWF 版面光柵化為位圖 JPEG 圖像。  
- **Why read layout size first?** 瞭解精確的範圍可讓您設定正確的頁面尺寸，避免圖像被拉伸或裁切。  
- **Which library handles this?** Aspose.CAD for .NET 提供對 DWG、DWF 以及光柵圖像轉換的完整支援。  
- **Do I need a license?** 評估期間可使用臨時授權；正式上線需購買完整授權。  
- **What .NET versions are supported?** .NET Framework 4.5+、.NET Core 3.1+、.NET 5/6/7。

## 什麼是「convert DWF to JPG」以及為何重要？

將 DWF（Design Web Format）檔案轉換為 JPG 可產生可在瀏覽器顯示、嵌入報告或與沒有 CAD 軟體的利害關係人共享的可攜式圖像。此轉換亦讓您能使用標準影像處理工具（調整大小、壓縮、加浮水印）靈活操作圖像。

## 為何提取 DWF 版面尺寸？

DWF 檔案可能包含多個版面，每個版面都有自己的座標系統與單位（英吋、毫米等）。提取版面尺寸可讓您：

1. 在光柵化時保留原始長寬比。  
2. 為高解析度輸出選擇正確的 DPI。  
3. 在大量版面上自動化批次處理，免除手動調整。

## 前置條件

為了順利完成本教學，請確保已具備以下前置條件：

- Aspose.CAD for .NET：確保已安裝 Aspose.CAD for .NET。您可以從 [Aspose.CAD for .NET 下載頁面](https://releases.aspose.com/cad/net/) 取得。

準備好函式庫後，您即可專注於程式碼本身，而不必再搜尋相依性。

## 匯入命名空間

在開始編寫程式碼之前，先匯入所需的命名空間。這些命名空間提供了操作 CAD 檔案、光柵化選項以及檔案 I/O 所需的類別。

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Dwf;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

## 步驟 1：設定環境

建立一個新的 C# 主控台或類別庫專案，加入對 **Aspose.CAD.dll** 的參考，並確保專案目標為相容的 .NET 版本。

## 步驟 2：定義檔案路徑（如何提取 DWF）

指定來源 DWF 檔案所在位置以及產生的 JPG 檔案要寫入的目錄。

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "blocks_and_tables.dwf";
```

> **Pro tip:** 使用 `Path.Combine(MyDir, "blocks_and_tables.dwf")` 可在不同作業系統上安全處理路徑。

## 步驟 3：載入 DWF 圖像

將 DWF 檔案載入至 `Aspose.CAD.Image` 物件。我們將其轉型為 `DwfImage`，以便存取頁面相關屬性。

```csharp
using (DwfImage image = (DwfImage)Aspose.CAD.Image.Load(sourceFilePath))
{
    // Code for further steps will go here
}
```

## 步驟 4：遍歷頁面

DWF 可能包含多個頁面（版面）。使用迴圈逐一處理每個頁面。

```csharp
foreach (var page in image.Pages)
{
    // Code for further steps will go here
}
```

## 步驟 5：取得版面資訊

在迴圈內取得版面名稱。此名稱將用於日誌記錄以及命名輸出的 JPG 檔案。

```csharp
var layout = page.Name;
System.Console.WriteLine("Layout= " + layout);
```

## 步驟 6：設定 JPG 選項

建立 `JpegOptions` 實例並設定光柵化選項。`Layouts` 屬性告訴 Aspose.CAD 要渲染哪個版面。

```csharp
using (FileStream fs = new FileStream(MyDir + "layout_" + layout + ".jpg", FileMode.Create))
{
    JpegOptions jpegOptions = new JpegOptions();
    CadRasterizationOptions options = new CadRasterizationOptions();
    options.Layouts = new string[] { layout };
    // Code for further steps will go here
}
```

## 步驟 7：確定頁面尺寸（將 dwg 轉換為 jpg）

計算版面在其原始單位下的寬度與高度。此資訊對正確設定光柵頁面尺寸至關重要。

```csharp
double sizeExtX = page.MaxPoint.X - page.MinPoint.X;
double sizeExtY = page.MaxPoint.Y - page.MinPoint.Y;
// Code for further steps will go here
```

## 步驟 8：設定頁面尺寸

使用 Aspose.CAD 提供的輔助方法，將原始單位（英吋或毫米）轉換為像素。若單位類型不屬於上述兩者，則直接使用原始數值。

```csharp
if (page.UnitType == UnitType.Inch)
{
    options.PageHeight = CommonHelper.INtoPixels(sizeExtY, CommonHelper.DPI);
    options.PageWidth = CommonHelper.INtoPixels(sizeExtX, CommonHelper.DPI);
}
else if (page.UnitType == UnitType.Millimeter)
{
    options.PageHeight = CommonHelper.MMtoPixels(sizeExtY, CommonHelper.DPI);
    options.PageWidth = CommonHelper.MMtoPixels(sizeExtX, CommonHelper.DPI);
}
else
{
    options.PageHeight = (float)sizeExtY;
    options.PageWidth = (float)sizeExtX;
}
```

## 步驟 9：儲存 JPG 檔案

最後，將光柵化選項綁定至 JPEG 選項，並將圖像寫入磁碟。

```csharp
jpegOptions.VectorRasterizationOptions = options;
image.Save(fs, jpegOptions);
}
```

當迴圈結束後，您將會得到每個版面的 JPG 檔案，且尺寸與原始 DWF 完全相符。

## 常見問題與解決方案

| 症狀 | 可能原因 | 解決方式 |
|---------|--------------|-----|
| JPG 輸出為空白 | `options.Layouts` 未正確設定 | 確認版面名稱與 `page.Name` 相符。 |
| 圖像變形 | DPI 轉換錯誤 | 在轉換前設定 `CommonHelper.DPI = 300`（或您目標的 DPI）。 |
| 找不到檔案 | `MyDir` 路徑錯誤 | 使用絕對路徑或 `Path.Combine`。 |
| 授權例外 | 未套用授權 | 在呼叫 `Image.Load` 前載入臨時或永久授權。 |

## 常見問答

### Q1：Aspose.CAD 是否相容最新的 DWG 檔案格式？

A1：Aspose.CAD 支援多種 DWG 檔案格式，包括最新版本。請參考 [文件說明](https://reference.aspose.com/cad/net/) 取得具體相容性資訊。

### Q2：我可以在商業與個人專案中使用 Aspose.CAD 嗎？

A2：可以，Aspose.CAD 提供彈性的授權方案，適用於商業與個人使用。詳情請見 [購買頁面](https://purchase.aspose.com/buy)。

### Q3：如何取得 Aspose.CAD 的臨時授權？

A3：您可從 [此處](https://purchase.aspose.com/temporary-license/) 取得臨時授權，用於評估目的。

### Q4：在哪裡可以取得 Aspose.CAD 的支援？

A4：如有任何問題或需要協助，請前往 [Aspose.CAD 論壇](https://forum.aspose.com/c/cad/19)。

### Q5：Aspose.CAD 是否提供免費試用？

A5：是的，您可在 [此處](https://releases.aspose.com/) 下載免費試用版。

### Q6：如何直接將 DWG 檔案轉換為 JPG，而不先提取 DWF？

A6：您可以使用 `Aspose.CAD.Image.Load` 載入 DWG，然後使用相同的光柵化流程；只需將 `options.Layouts` 設為 DWG 中欲渲染的版面名稱即可。

### Q7：轉換後的圖像是否保留向量品質？

A7：轉換為 JPG 後，圖像會變成位圖，向量的可伸縮性將不復存在。如需無損縮放，建議匯出為 PNG 或 SVG。

---

**Last Updated:** 2026-04-06  
**Tested With:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}