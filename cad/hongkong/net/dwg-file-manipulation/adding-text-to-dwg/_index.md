---
date: 2026-04-06
description: 學習如何使用 C# 與 Aspose.CAD 將 DWG 轉換為 PDF 並加入自訂文字。本逐步指南涵蓋從 DWG 產生 PDF、插入文字實體以及變更
  DWG 文字字型。
keywords:
- convert dwg to pdf
- generate pdf from dwg
- insert text entity
- change dwg text font
- aspose cad dwg pdf
linktitle: 在 C# 中向 DWG 檔案加入文字
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: 將 DWG 轉換成 PDF 並於 C# 加入文字 – Aspose.CAD 教學
url: /zh-hant/net/dwg-file-manipulation/adding-text-to-dwg/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 將 DWG 轉換為 PDF 並在 C# 中新增文字 – Aspose.CAD 教程

## 介紹

在快速變化的 CAD 與 .NET 開發領域，**將 DWG 轉換為 PDF** 同時插入自訂註解是一項常見需求。無論是為客戶產生可列印的圖紙，或是直接在 DWG 中嵌入動態說明，Aspose.CAD 都能讓工作變得簡單。在本教學中，你將學會如何 **將 DWG 轉換為 PDF**、**新增文字實體**，以及使用 C# **變更 DWG 文字字型**。

## 快速回答
- **哪個函式庫最適合 DWG 轉 PDF？** Aspose.CAD for .NET  
- **轉換時可以加入自訂文字嗎？** 可以 – 建立 `CadText` 實體並在儲存前加入。  
- **生產環境需要授權嗎？** 需要商業授權；提供免費試用版。  
- **支援哪些 .NET 版本？** .NET Framework 4.5+、.NET Core 3.1+、.NET 5/6+。  
- **可以變更文字字型嗎？** 可以，調整 `CadText` 的 `StyleType` 與 `TextHeight` 等屬性。

## 什麼是「將 DWG 轉換為 PDF」？

將 DWG 檔案轉換為 PDF，會把向量式 CAD 圖面轉成一個可廣泛分享、與裝置無關的文件。PDF 會保留原始的幾何與圖層，同時允許你嵌入註解、文字或其他中繼資料。Aspose.CAD 會自動處理光柵化與向量渲染，無需在伺服器上安裝任何第三方 CAD 軟體。

## 為什麼要在轉換前先在 DWG 中加入文字？

直接將文字嵌入 DWG，可完整掌控其位置、樣式與圖層分配。當檔案稍後被轉換為 PDF 時，文字會精確出現在你設定的位置，保留設計意圖，且不必在 PDF 編輯器中再做後處理。

## 先決條件

在開始之前，請確保你已具備：

- **Aspose.CAD Library** – 從 [download link](https://releases.aspose.com/cad/net/) 下載。  
- **可運作的 .NET 環境**（Visual Studio 2022、.NET 6 或任何相容版本）。  
- **測試檔案資料夾** – 本教學全程會以 `MyDir` 作為範例路徑。

現在，讓我們一步步完成整個流程。

## 匯入命名空間

加入必要的 `using` 陳述式，以便存取 Aspose.CAD 類別。

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

## 步驟 1：載入 DWG 檔案

將來源 DWG 檔案載入為 `Image` 物件。此物件讓你可以存取底層的 CAD 實體。

```csharp
string dwgPathToFile = MyDir + "SimpleEntites.dwg";
using (Image image = Image.Load(dwgPathToFile))
{
    // Subsequent steps will be performed inside this block
}
```

## 步驟 2：建立 CadText 物件（插入文字實體）

`CadText` 類別代表 DWG 中的單行文字。此處設定其樣式、內容、顏色、圖層與位置。調整 `StyleType` 或 `TextHeight` 即可 **變更 DWG 文字字型**。

```csharp
CadText cadText = new CadText();
cadText.StyleType = "Standard";          // Font/style – change to alter DWG text font
cadText.DefaultValue = "Some custom text";
cadText.ColorId = 256;                    // 256 = ByLayer (you can use a specific ACI color)
cadText.LayerName = "0";
cadText.FirstAlignment.X = 47.90;
cadText.FirstAlignment.Y = 5.56;
cadText.TextHeight = 0.8;                 // Height influences visual size
cadText.ScaleX = 0.0;
```

## 步驟 3：將文字實體加入 Model Space

DWG 的 Model Space 包含大多數繪圖實體。將 `CadText` 加入 `*Model_Space` 區塊，即可讓文字成為圖面的一部份。

```csharp
CadImage cadImage = (CadImage)image;
cadImage.BlockEntities["*Model_Space"].AddEntity(cadText);
```

## 步驟 4：設定 PDF 選項（從 DWG 產生 PDF）

設定光柵化選項，以控制 DWG 轉 PDF 的渲染方式。你可以調整頁面大小、繪製類型與版面配置。

```csharp
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.VectorRasterizationOptions = cadRasterizationOptions;
cadRasterizationOptions.DrawType = CadDrawTypeMode.UseObjectColor;
cadRasterizationOptions.PageHeight = 1600;
cadRasterizationOptions.PageWidth = 1600;
cadRasterizationOptions.Layouts = new string[] { "Model" };
```

## 步驟 5：將修改後的 DWG 儲存為 PDF

最後，匯出已修改的圖面。產生的 PDF 會包含新加入的文字。

```csharp
image.Save(MyDir + "SimpleEntites_generated.pdf", pdfOptions);
```

> **專業提示：** 若需要更高解析度的 PDF，可成比例提升 `PageHeight` 與 `PageWidth`。

## 常見問題與解決方案

| 問題 | 原因 | 解決方法 |
|------|------|----------|
| 文字未出現在 PDF 中 | 圖層或顏色 ID 錯誤 | 確認 `LayerName` 已存在且 `ColorId` 設為可見顏色（例如 7 代表白色）。 |
| 文字位置錯位 | 對齊座標不正確 | 檢查 `FirstAlignment.X/Y` 值是否符合圖面的單位。 |
| PDF 為空白 | 未正確設定光柵化選項 | 將 `DrawType` 設為 `UseObjectColor` 或 `UseObjectLineWeight`。 |

## 常見問題 (現有)

### Q1: Aspose.CAD 是否相容所有版本的 DWG 檔案？

A1: Aspose.CAD 支援廣泛的 DWG 檔案版本，確保與各種 CAD 軟體相容。

### Q2: 我可以使用 Aspose.CAD 在單一 DWG 檔案中新增多個文字實體嗎？

A2: 可以，您只需重複本教學中的步驟，即可在 DWG 檔案中新增多個文字實體。

### Q3: 如何在 Aspose.CAD 中變更文字字型與樣式？

A3: 要修改文字字型與樣式，請在將 `CadText` 物件加入 DWG 檔案前調整其屬性。

### Q4: 在商業專案中使用 Aspose.CAD 有哪些授權考量？

A4: 是，請確保遵守 Aspose.CAD 的授權條款。詳情請參閱 [Aspose.CAD Purchase](https://purchase.aspose.com/buy)。

### Q5: 我可以在哪裡尋求協助或討論 Aspose.CAD 相關問題？

A5: 請前往 [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) 與社群交流並取得支援。

## 其他常見問題

**Q: 如何在不新增文字的情況下從 DWG 產生 PDF？**  
A: 跳過 `CadText` 建立步驟，直接設定 `PdfOptions` 後呼叫 `image.Save(...)` 即可。

**Q: 我可以以程式方式變更文字顏色嗎？**  
A: 可以，將 `cadText.ColorId` 設為特定的 ACI 顏色編號（例如 1 代表紅色）。

**Q: 是否可以插入多行文字？**  
A: 使用 `CadMText` 來處理多行文字區塊；使用方式與 `CadText` 類似。

**Q: Aspose.CAD 是否支援批次轉換多個 DWG 檔案？**  
A: 當然可以 – 迴圈處理 DWG 檔案目錄，套用相同步驟，並將每個檔案另存為 PDF。

## 結論

現在你已掌握完整、可投入生產的工作流程，能夠 **將 DWG 轉換為 PDF**、**新增自訂文字**，並使用 C# 與 Aspose.CAD **自訂文字外觀**。此技巧非常適合自動化圖紙產生、報表管線，或任何需要即時豐富 CAD 檔案的情境。

---

**最後更新：** 2026-04-06  
**測試環境：** Aspose.CAD 24.11 for .NET  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}