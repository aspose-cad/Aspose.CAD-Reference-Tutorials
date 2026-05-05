---
date: 2026-04-03
description: 學習如何使用 Aspose.CAD for .NET 渲染 CAD 檔案並將 DWG 轉換為 PNG。一步一步的指南教您將 CAD 儲存為圖像。
keywords:
- how to render cad
- convert dwg to png
- export cad to png
- save cad as image
- load dwg in .net
linktitle: 在 CAD 檔案中渲染顏色
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: 如何以彩色渲染 CAD 檔案 – Aspose.CAD 指南
url: /zh-hant/net/conversion-and-export/rendering-colors-in-cad-files/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何使用顏色渲染 CAD 檔案 – Aspose.CAD 指南

## 簡介

您是否正為如何在 .NET 中使用鮮豔的顏色渲染 CAD 檔案而苦惱？在本完整的逐步指南中，我們將向您展示如何在 CAD 檔案中渲染顏色、將 DWG 轉換為 PNG，並使用 Aspose.CAD 函式庫將 CAD 圖紙儲存為高品質影像。

## 快速回答
- **哪個函式庫最適合渲染 CAD 顏色？** Aspose.CAD for .NET  
- **我可以一步完成 DWG 轉 PNG 嗎？** 是 – 將 DWG 光柵化後儲存為 PNG。  
- **我需要授權才能在正式環境使用嗎？** 臨時授權可用於測試；正式環境需購買完整授權。  
- **支援哪些 .NET 版本？** .NET Framework 4.5+、.NET Core 3.1+、.NET 5/6/7。  
- **此流程足夠快速以進行批次轉換嗎？** 渲染在記憶體中完成，適合大量操作。

## 什麼是 CAD 檔案的顏色渲染？
顏色渲染是指將 CAD 圖紙（DWG、DXF 等）中儲存的向量資訊轉換為點陣圖，同時保留原始物件的顏色。當您需要與沒有 CAD 軟體的相關人員分享 CAD 視覺內容時，這是必須的。

## 為何使用 Aspose.CAD 轉換 DWG 為 PNG？
- **無外部相依性** – 完全離線運作。  
- **完整保真度** – 物件顏色、線寬與圖層皆被保留。  
- **簡易 API** – 一行程式碼即可載入、設定與儲存。  
- **跨平台** – 可在 Windows、Linux 及 macOS .NET 執行環境上運作。

## 先決條件

- Aspose.CAD 函式庫：從[此處](https://releases.aspose.com/cad/net/)下載並安裝 Aspose.CAD 函式庫。  
- 開發環境：確保已設定 .NET 開發環境。  
- CAD 檔案：準備好測試用的 CAD 範例檔案。此教學可使用 “test1.dwg”。

## 匯入命名空間

在您的 .NET 專案中，匯入必要的命名空間以存取 Aspose.CAD 功能。於程式碼開頭加入以下行：

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

## 步驟 1：設定專案

建立新的 .NET 專案並設定所需目錄。確保在專案中已參考 Aspose.CAD 函式庫。

## 步驟 2：定義檔案路徑

指定輸入 CAD 檔案與輸出 PNG 檔案的路徑。於程式碼中更新以下行：

```csharp
string MyDir = "Your Document Directory";
string inputFile = MyDir + "test1.dwg";
string outputFile = MyDir + "test1.png";
```

## 步驟 3：載入 CAD 檔案

使用以下程式碼開啟並載入 CAD 檔案：

```csharp
using (FileStream fs = new FileStream(inputFile, FileMode.Open))
{
    using (FileStream output = new FileStream(outputFile, FileMode.Create))
    {
        Image document = Image.Load(fs);
```

## 步驟 4：設定光柵化選項

設定光柵化選項以自訂渲染流程。更新以下行：

```csharp
PngOptions saveOptions = new PngOptions();

CadRasterizationOptions options = new CadRasterizationOptions();
options.NoScaling = false;
options.PageHeight = document.Height * 10;
options.PageWidth = document.Width * 10;
options.DrawType = Aspose.CAD.FileFormats.Cad.CadDrawTypeMode.UseObjectColor;
saveOptions.VectorRasterizationOptions = options;
```

## 步驟 5：儲存渲染圖像

使用指定的選項儲存渲染後的影像：

```csharp
document.Save(output, saveOptions);
```

## 為什麼這很重要

將 CAD 儲存為影像（PNG、JPEG 等）是常見需求，尤其在需要將圖紙嵌入報告、網頁或電子郵件附件時。掌握**如何渲染 CAD**可免除第三方檢視器，確保在所有平台上都有一致的視覺輸出。

## 常見問題與解決方案

| 問題 | 原因 | 解決方案 |
|-------|-------|----------|
| 空白影像輸出 | `NoScaling` 設為 `true` 且尺寸為零 | 確保 `PageHeight` 與 `PageWidth` 依載入的圖像計算（如範例所示）。 |
| 顏色顯示錯誤 | 錯誤的 `DrawType` | 使用 `CadDrawTypeMode.UseObjectColor` 以保留原始物件顏色。 |
| 找不到檔案 | `MyDir` 路徑不正確 | 確認目錄路徑以斜線結尾，或使用 `Path.Combine`。 |
| 大型檔案記憶體不足 | 以極高 DPI 進行渲染 | 降低縮放係數（例如 `*5` 而非 `*10`）。 |

## 結論

恭喜！您已成功學會**如何渲染 CAD**檔案、將 DWG 轉換為 PNG，並使用 Aspose.CAD for .NET **將 CAD 儲存為影像**。此知識讓您能將 CAD 渲染直接整合至應用程式中，自動化報告產生、網頁預覽等功能。

## 常見問題

### Q1：我可以免費使用 Aspose.CAD 嗎？
A1：Aspose.CAD 提供免費試用版，請至[此處](https://releases.aspose.com/)下載。您可在購買前先試用其功能。

### Q2：在哪裡可以找到 Aspose.CAD 的詳細文件？
A2：請參閱[此處](https://reference.aspose.com/cad/net/)的文件，以取得 Aspose.CAD 功能的深入資訊。

### Q3：如何取得 Aspose.CAD 的臨時授權？
A3：可於[此處](https://purchase.aspose.com/temporary-license/)取得臨時授權，以供測試使用。

### Q4：需要協助或有任何問題？
A4：請前往 Aspose.CAD 社群[論壇](https://forum.aspose.com/c/cad/19)尋求支援與討論。

### Q5：在哪裡可以購買 Aspose.CAD 函式庫？
A5：可於[此處](https://purchase.aspose.com/buy)購買 Aspose.CAD，解鎖完整功能。

## 其他常見問題

**Q: 如何在不失去線寬的情況下 **convert DWG to PNG**？**  
A: 保持預設的 `PageHeight` 與 `PageWidth` 縮放（例如乘以 10），並將 `options.DrawType` 設為 `UseObjectColor`。此設定可保留線寬與顏色。

**Q: 是否可以在背景服務中 **export CAD to PNG**？**  
A: 可以。Aspose.CAD API 在唯讀操作下為執行緒安全，您可在背景工作程序中載入並光柵化檔案。

**Q: 我能從位元組陣列而非檔案 **load DWG in .NET** 嗎？**  
A: 完全可以。使用 `Image.Load(byteArray)` 取代 `FileStream`，並遵循相同的光柵化步驟。

**Q: 在 **saving CAD as image** 時，應選擇哪種格式以獲得最佳品質？**  
A: PNG 提供無損壓縮且保留顏色真實度，是技術圖紙的理想選擇。

**Q: Aspose.CAD 是否支援其他光柵格式，如 JPEG 或 BMP？**  
A: 支援，只需將 `PngOptions` 換成 `JpegOptions` 或 `BmpOptions`，並調整相應的格式設定即可。

**最後更新:** 2026-04-03  
**測試環境:** Aspose.CAD 24.11 for .NET  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}