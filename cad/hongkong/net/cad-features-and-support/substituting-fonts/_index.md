---
date: 2026-03-29
description: 快速學習如何在 Aspose.CAD for .NET 中替換字型。此一步一步的指南會向您展示如何設定主要字型名稱以及有效地自訂 CAD
  圖紙。
linktitle: Substituting Fonts
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: 如何在 Aspose.CAD for .NET 中更換字型
url: /zh-hant/net/cad-features-and-support/substituting-fonts/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何在 Aspose.CAD for .NET 中取代字型

## 介紹

在使用 .NET 進行 CAD 開發的領域中，學習**如何取代字型**是一項關鍵技能，能顯著提升圖紙的視覺品質。Aspose.CAD for .NET 提供簡易的 API，讓您**設定主要字型名稱**於任何樣式，輕鬆完成全域或針對特定樣式的字型取代。在本教學中，我們將逐步說明整個流程——從載入圖紙到全域或依樣式名稱替換字型。

## 快速解答
- **CAD 操作的主要類別是什麼？** `Aspose.CAD.Image` (or its derived `CadImage`).
- **哪個屬性會變更字型？** `PrimaryFontName` on `CadStyleTableObject`.
- **可以一次取代所有樣式的字型嗎？** 可以，遍歷 `cadImage.Styles` 並設定該屬性。
- **生產環境需要授權嗎？** 非試用使用需具備有效的 Aspose.CAD 授權。
- **支援的 .NET 版本？** .NET Framework 4.5+、.NET Core 3.1+、.NET 5/6/7。

## CAD 中的字型取代是什麼？
字型取代指的是將 CAD 圖紙中原本使用的字型，以目標系統上可用的其他字型取代。當原始字型缺失、需要統一企業風格，或在僅支援有限字型的列印設備上列印圖紙時，此功能特別有用。

## 為什麼要使用 Aspose.CAD 取代字型？
- **無外部相依** – 函式庫內部自行處理字型對應。
- **支援多種格式** – DXF、DWG、DGN 等。
- **程式化控制** – 可自動化批次轉換或 CI 流程。
- **保留圖形幾何** – 僅變更文字的視覺呈現。

## 前置條件

- 具備 .NET 程式設計的基本知識。
- 已安裝 Aspose.CAD for .NET。如尚未安裝，請於 [here](https://releases.aspose.com/cad/net/) 下載。
- 用於實驗的 CAD 圖紙檔案（DXF、DWG 等）。

## 匯入命名空間

在開始之前，匯入必要的命名空間以在 .NET 應用程式中存取 Aspose.CAD 功能。

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad.CadTables;
```

## 步驟 1：載入 CAD 圖紙

將 CAD 圖紙載入 `CadImage` 實例。請確保提供正確的文件目錄路徑。

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (CadImage cadImage = (CadImage)Aspose.CAD.Image.Load(sourceFilePath))
{
    // Your code for further actions goes here
}
```

## 步驟 2：遍歷樣式

使用 `foreach` 迴圈遍歷 CAD 圖紙中的樣式，以便存取與操作各個字型樣式。

```csharp
foreach (CadStyleTableObject style in cadImage.Styles)
{
    // Your code for style manipulation goes here
}
```

## 如何設定 PrimaryFontName 以進行字型取代

每個 `CadStyleTableObject` 的 `PrimaryFontName` 屬性決定圖紙渲染時使用的字型。設定此屬性即可有效取代原始字型。

### 步驟 3：全域取代字型

若要為**所有**樣式取代字型，將每個樣式的 `PrimaryFontName` 屬性設定為目標字型名稱，例如 `"Arial"`。

```csharp
foreach (CadStyleTableObject style in cadImage.Styles)
{
    style.PrimaryFontName = "Arial";
}
```

### 步驟 4：依樣式名稱取代字型

若只需為特定樣式（例如名稱為 `"Roman"` 的樣式）取代字型，可在迴圈內加入條件判斷。

```csharp
foreach (CadStyleTableObject style in cadImage.Styles)
{
    if (style.StyleName == "Roman")
    {
        style.PrimaryFontName = "Arial";
    }
}
```

## 常見問題與疑難排解

| 問題 | 原因 | 解決方案 |
|-------|-------|-----|
| 執行程式碼後字型未變更 | 圖紙被快取或以唯讀模式開啟 | 確保在修改後儲存影像 (`cadImage.Save(...)`) 或重新載入檔案以驗證。 |
| 系統上找不到所需字型 | 執行程式碼的機器未安裝該字型 | 安裝所需的 TrueType/OpenType 字型或將其嵌入應用程式資源中。 |
| 文字顯示亂碼 | 編碼不正確或缺少 Unicode 支援 | 使用支援所需字元集的字型（例如 Arial Unicode MS）。 |

## 常見問答

**Q: 我可以在 Aspose.CAD for .NET 中還原字型變更嗎？**  
A: 是的，您可以透過重新載入原始 CAD 圖紙或在修改前保留備份來還原。

**Q: 還有其他字型屬性可以修改嗎？**  
A: 當然可以。除了 `PrimaryFontName`，您還可以使用 `SecondaryFontName`、`FontFamily` 以及其他與樣式相關的屬性進行進階客製化。

**Q: Aspose.CAD 是否相容於不同的 CAD 格式？**  
A: 是的，Aspose.CAD 支援廣泛的格式，如 DXF、DWG、DGN、DWF 等，讓您在各種專案中都有彈性。

**Q: 我可以在批次處理中自動化字型取代嗎？**  
A: 當然可以。將載入與取代的邏輯包在迴圈中，遍歷資料夾內的 CAD 檔案，或整合至 CI/CD 流程。

**Q: 在哪裡可以找到 Aspose.CAD for .NET 的其他支援？**  
A: 欲取得更多支援與社群討論，請造訪 [Aspose.CAD forum](https://forum.aspose.com/c/cad/19)。

---

**最後更新：** 2026-03-29  
**測試環境：** Aspose.CAD for .NET（最新版本）  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}