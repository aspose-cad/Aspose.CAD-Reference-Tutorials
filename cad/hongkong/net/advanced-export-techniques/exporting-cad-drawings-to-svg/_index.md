---
date: 2026-03-07
description: 了解如何使用 Aspose.CAD for .NET 將 CAD 匯出為 SVG、客製化 SVG 顏色，並高效地將 DWG 轉換為 SVG。
linktitle: Exporting CAD Drawings to SVG Format
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: 將 CAD 匯出為 SVG – 將 CAD 圖紙匯出為 SVG 格式 - Aspose.CAD 指南
url: /zh-hant/net/advanced-export-techniques/exporting-cad-drawings-to-svg/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 匯出 CAD 為 SVG – 將 CAD 圖紙匯出為 SVG 格式

## 簡介

將 CAD 圖紙匯出為 SVG 是在需要解析度無關的圖形以用於網頁、報告或互動視覺化時的常見需求。在本教學中，您將學習 **如何將 CAD 匯出為 SVG**，使用 Aspose.CAD for .NET，探索 **自訂 SVG 顏色** 的選項，並了解如何僅用幾行程式碼 **將 DWG 轉換為 SVG**（或 DXF 轉換為 SVG）。步驟簡潔，API 直觀，產生的 SVG 檔案可在任何裝置上完美縮放。

## 快速答覆
- **什麼函式庫負責轉換？** Aspose.CAD for .NET.  
- **我可以更改顏色模式嗎？** 可以 – 使用 `SvgColorMode` 設定灰階、黑白或全彩。  
- **支援哪些 CAD 格式？** DWG、DXF 以及其他多種（請參閱 Aspose.CAD 文件）。  
- **開發時需要授權嗎？** 可取得臨時授權以進行測試。  
- **轉換需要多長時間？** 標準圖紙通常在一秒內完成。

## 什麼是「匯出 CAD 為 SVG」？

匯出 CAD 為 SVG 指的是將原生 CAD 檔案（如 DWG 或 DXF）渲染成可縮放向量圖形（Scalable Vector Graphics）格式。SVG 基於 XML、輕量且可使用 CSS 進行樣式設定——非常適合現代網頁與行動應用程式。

## 為什麼使用 Aspose.CAD 來匯出 CAD 為 SVG？

- **無外部相依性** – 純 .NET API，無需安裝 AutoCAD。  
- **細緻的控制** – 您可以 **自訂 SVG 顏色**，決定文字是否保留為圖形，並選擇光柵化選項。  
- **廣泛的格式支援** – 同一段程式碼即可 **將 DWG 轉換為 SVG**、**將 DXF 轉換為 SVG** 以及其他格式，簡化程式碼基礎。  
- **高效能** – 為速度與低記憶體使用量優化，適合批次處理。

## 先決條件

在開始之前，請確保您已具備：

- 已安裝 **Aspose.CAD for .NET**。您可在此處下載函式庫 [here](https://releases.aspose.com/cad/net/)。  
- .NET 開發環境（Visual Studio、Rider 或 .NET CLI）。  
- 您想要轉換的 CAD 檔案（DWG 或 DXF）。

## 匯入命名空間

首先，將所需的命名空間加入專案，以便使用相關類別。

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## 逐步指南

### 步驟 1：設定文件目錄  
定義來源 CAD 檔案所在的資料夾，以及 SVG 輸出要儲存的資料夾。

```csharp
// The path to the documents directory.
string MyDir = "Your Document Directory";
```

### 步驟 2：載入 CAD 圖紙  
使用 `Image.Load` 讀取 DWG（或 DXF）檔案。此方式適用於 **load DWG .NET** 情境。

```csharp
using (Image image = Image.Load(MyDir + "sample.dwg"))
{
```

### 步驟 3：設定 SVG 匯出選項  
調整匯出設定以符合需求。此處將顏色模式設定為灰階，並強制所有文字以向量圖形方式呈現。

```csharp
    var options = new SvgOptions();
    options.ColorType = SvgColorMode.Grayscale;   // customize SVG color mode
    options.TextAsShapes = true;                  // ensures text appears as shapes
```

### 步驟 4：儲存 SVG 檔案  
最後，將 SVG 檔案寫入磁碟。此步驟 **將 CAD 儲存為 SVG**，完成轉換。

```csharp
    image.Save(MyDir + "sample.svg", options);
}
```

遵循這四個簡潔步驟，即可 **將 DWG 轉換為 SVG**（或 **將 DXF 轉換為 SVG**），並完整掌控輸出外觀。

## 常見問題與解決方案

| 問題 | 原因 | 解決方法 |
|-------|-------|-----|
| **空白 SVG 輸出** | 來源檔案路徑不正確或檔案已損毀。 | 確認 `MyDir` 並確保 CAD 檔案能正常開啟，無錯誤。 |
| **顏色顯示異常** | `SvgColorMode` 不小心被設定為灰階。 | 將 `options.ColorType` 改為 `SvgColorMode.FullColor` 以保留原始顏色。 |
| **文字遺失** | `TextAsShapes` 被設定為 `false`，且檢視器不支援嵌入字型。 | 將 `TextAsShapes = true`，或在 SVG 中嵌入所需字型。 |

## 常見問答

### Q1：Aspose.CAD 是否相容所有 CAD 格式？

A1：Aspose.CAD 支援多種 CAD 格式，包括 DWG 與 DXF，確保廣泛相容性。

### Q2：匯出為 SVG 時，我可以自訂顏色模式嗎？

A2：可以，Aspose.CAD 允許您選擇顏色模式，提供輸出上的彈性。

### Q3：是否提供臨時授權供測試使用？

A3：可以，您可在此取得臨時授權 [here](https://purchase.aspose.com/temporary-license/) 以供評估。

### Q4：在哪裡可以找到 Aspose.CAD 的詳細文件？

A4：文件可於此取得 [here](https://reference.aspose.com/cad/net/)。

### Q5：如何取得支援或提出與 Aspose.CAD 相關的問題？

A5：請前往社群論壇 [here](https://forum.aspose.com/c/cad/19) 取得支援與討論。

## 常見問題集

**Q: 我可以在 .NET Core 或 .NET 6 上使用此程式碼嗎？**  
A: 當然可以。Aspose.CAD for .NET 相容於 .NET Framework、.NET Core 以及 .NET 5/6 以上。

**Q: 是否能只匯出特定的版面或圖層？**  
A: 可以。使用 `SvgOptions` 設定 `PageIndex` 或在儲存前過濾圖層。

**Q: 如何將自訂 CSS 樣式嵌入產生的 SVG？**  
A: 儲存後，您可對 SVG XML 進行後處理以注入 `<style>` 元素，或在較新版本中使用 `options.CustomCss`（若支援）。

**Q: 原始 CAD 檔案的大小有何限制？**  
A: 函式庫能處理大型檔案，但記憶體使用量會隨複雜度增加。對於極大圖紙，建議逐頁處理。

**Q: 轉換是否保留線寬與線型？**  
A: 預設會保留線寬。您可在 `SvgOptions` 中調整渲染選項以取得更細緻的控制。

---

**最後更新:** 2026-03-07  
**測試環境:** Aspose.CAD for .NET 24.12  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}