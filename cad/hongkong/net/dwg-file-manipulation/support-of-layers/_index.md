---
date: 2026-04-09
description: 學習如何使用 C# 及 Aspose.CAD for .NET 匯出 DWG 圖層、轉換 DWG 圖像並儲存 DWG 為 JPEG。一步一步的指南，助您高效操作
  CAD 檔案。
keywords:
- export dwg layers
- convert dwg image
- dwg layer visibility
- save dwg jpeg
linktitle: 使用 C# 處理 DWG 檔案中的圖層
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: 使用 C# 匯出 DWG 圖層 – Aspose.CAD 教學
url: /zh-hant/net/dwg-file-manipulation/support-of-layers/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 C# 匯出 DWG 圖層 – Aspose.CAD 教程

## 介紹

在本完整指南中，您將學習 **如何使用 C# 及 Aspose.CAD 函式庫匯出 DWG 圖層**。無論您需要 **轉換 DWG 圖像** 格式、控制 **DWG 圖層可見性**，或只是 **儲存 DWG JPEG** 檔案，以下步驟都會向您展示如何有效執行。完成本教學後，您將擁有一段可直接執行的程式碼，能夠挑選特定圖層並將其渲染為高品質 JPEG。

## 快速解答
- **「匯出 dwg 圖層」是什麼意思？** 代表將 DWG 檔案中選取的圖層光柵化為 JPEG 或 PNG 等影像格式。  
- **哪個函式庫最適合此任務？** Aspose.CAD for .NET 提供完整支援，且不需 AutoCAD。  
- **可以一次匯出多個圖層嗎？** 可以 – 只要將圖層名稱陣列傳入光柵化選項。  
- **正式環境需要授權嗎？** 需要商業授權；亦提供免費試用版供評估。  
- **支援哪些輸出格式？** JPEG、PNG、BMP、TIFF 以及透過 ImageOptions 類別支援的其他格式。

## 什麼是匯出 dwg 圖層？
匯出 DWG 圖層是指將 DWG 繪圖中一個或多個圖層的向量資料光柵化為點陣圖影像。當您想在不公開完整 CAD 檔案的情況下，分享繪圖中特定部分的視圖時，這非常有用。

## 為什麼要控制 DWG 圖層可見性？
控制圖層可見性可讓您：

- 為簡報或文件建立乾淨的視覺資產。  
- 只匯出所需的幾何圖形，減少檔案大小。  
- 透過隱藏機密圖層，保護專有設計細節。  

## 前置條件

在開始之前，請確認您已具備：

- 基本的 C# 程式語言知識。  
- 已在電腦上安裝 Visual Studio。  
- Aspose.CAD for .NET 函式庫，可從 [Aspose.CAD website](https://releases.aspose.com/cad/net/) 下載。

## 匯入命名空間

首先，匯入可使用光柵化與影像匯出功能的命名空間。

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

## 步驟 1：載入 DWG 檔案

將來源 DWG（或 DWF）檔案載入 `Image` 物件。此物件在記憶體中代表整個繪圖。

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "for_layers_test.dwf";

using (Aspose.CAD.Image image = Aspose.CAD.Image.Load(sourceFilePath))
{
    // Your code for subsequent steps goes here
}
```

*為什麼這很重要：* 只載入一次檔案，即可在多次圖層特定匯出時重複使用相同的 `image` 實例，提升效能。

## 步驟 2：設定光柵化選項

建立 `CadRasterizationOptions` 實例，告訴 Aspose.CAD 如何渲染繪圖。此處我們設定高解析度 (1600 × 1600) 以確保匯出的 JPEG 清晰銳利。

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions rasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
```

如有需要，也可以調整背景色、線寬縮放或抗鋸齒設定。

## 步驟 3：指定圖層（DWG 圖層可見性）

加入您想 **匯出 dwg 圖層** 的圖層名稱。此範例僅匯出 “LayerA”。若要匯出多個圖層，只需在陣列中列出它們。

```csharp
rasterizationOptions.Layers = new string[] { "LayerA" };
```

*小技巧：* 使用繪圖中顯示的完整圖層名稱；圖層名稱區分大小寫。

## 步驟 4：設定影像匯出選項

選擇您想建立的影像格式。我們使用 `JpegOptions`，因為 JPEG 在品質與檔案大小之間取得良好平衡，適合在網頁預覽時 **儲存 dwg jpeg** 檔案。

```csharp
JpegOptions jpegOptions = new JpegOptions();
jpegOptions.VectorRasterizationOptions = rasterizationOptions;
```

若需 **轉換 dwg 圖像** 為 PNG 或 TIFF，只要將 `JpegOptions` 替換為相應的選項類別即可。

## 步驟 5：儲存匯出影像

定義輸出檔案路徑並呼叫 `Save`。光柵化引擎會遵循您提供的圖層清單，最終 JPEG 只會顯示 “LayerA”。

```csharp
MyDir = MyDir + "for_layers_test.jpg";
image.Save(MyDir, jpegOptions);
```

此行程式碼執行完畢後，您會在文件目錄中看到 `for_layers_test.jpg`，其中僅包含選取的圖層。

## 常見問題與解決方案

| 問題 | 解決方式 |
|-------|------------|
| **找不到圖層名稱** | 核對原始 DWG 中圖層的拼寫與大小寫。可使用 CAD 檢視器列出圖層名稱。 |
| **輸出影像為空白** | 確認光柵化選項的背景色非透明，且所選圖層確實包含幾何圖形。 |
| **輸出解析度過低** | 增加 `PageWidth` 與 `PageHeight`，或在 `CadRasterizationOptions` 中設定 `Resolution`。 |
| **不支援的 DWG 版本** | 更新至最新的 Aspose.CAD 版本；新版已加入對較新 AutoCAD 版本的支援。 |

## 常見問答

### Q1：可以同時處理多個圖層嗎？
A1：可以。只需將圖層名稱加入 `rasterizationOptions.Layers` 陣列。

### Q2：Aspose.CAD 有提供試用版嗎？
A2：有，您可從 [here](https://releases.aspose.com/) 取得免費試用版。

### Q3：文件在哪裡可以找到？
A3：文件可於 [here](https://reference.aspose.com/cad/net/) 取得。

### Q4：如何取得 Aspose.CAD 的支援？
A4：可在 [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) 上尋求協助。

### Q5：Aspose.CAD 的授權方案有哪些？
A5：您可於 [here](https://purchase.aspose.com/buy) 探索授權選項與購買細節。

**其他問答**

**Q：可以將圖形匯出為 PNG 而非 JPEG 嗎？**  
A：當然可以。將 `JpegOptions` 換成 `PngOptions`，並相應調整檔案副檔名。

**Q：函式庫會保留線條樣式與顏色嗎？**  
A：會的。所有向量屬性在光柵化過程中都會忠實呈現。

---

**最後更新：** 2026-04-09  
**測試環境：** Aspose.CAD for .NET（最新發行版）  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}