---
date: 2026-03-24
description: 學習如何使用 Aspose.CAD for .NET 將 dgn 轉換為 png，並將 cad 儲存為 jpeg——CAD 轉圖像的快速指南。
linktitle: Export DGN to Raster Image
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: 如何在 Aspose.CAD for .NET 中將 DGN 轉換為 PNG
url: /zh-hant/net/cad-export-formats/export-dgn-to-raster-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 將 DGN 轉換為 PNG（使用 Aspose.CAD for .NET）

在現代 .NET 開發中，**convert dgn to png** 是在網頁上顯示 CAD 圖紙或將其嵌入報告時的常見需求。Aspose.CAD for .NET 讓此轉換變得簡單，只需幾行程式碼即可將 DGN 檔案轉換為高品質的點陣圖像。本指南將從專案設定說明到最終儲存 PNG（或 JPEG）檔案的完整流程。

## 快速解答
- **可以使用 Aspose.CAD 將 DGN 轉換為 PNG 嗎？** 可以 – 只需設定光柵化選項並選擇 PNG 或 JPEG 輸出。  
- **生產環境需要授權嗎？** 非試用部署必須使用有效的 Aspose.CAD 授權。  
- **支援哪些 .NET 版本？** .NET Framework 4.6 以上、.NET Core 3.1 以上、.NET 5/6/7。  
- **提供哪些影像格式？** PNG、JPEG、BMP、GIF、TIFF 等。  
- **需要例外處理嗎？** 必須 – 請將轉換程式碼包在 try/catch 中，以處理檔案存取問題。

## 什麼是 “convert dgn to png”？
將 DGN（MicroStation）檔案轉換為 PNG，即將向量 CAD 資料光柵化為像素圖像。此功能適用於產生預覽圖、在 HTML 電子郵件中嵌入圖紙，或為文件管理系統建立縮圖。

## 為什麼選擇 Aspose.CAD 進行 CAD 轉影像？
- **無外部相依性** – 完全以受管理程式碼執行。  
- **高保真度** – 保留線寬、圖層與顏色。  
- **彈性輸出** – 只需更改一個選項即可在 PNG、JPEG、BMP 等之間切換。  
- **效能優化** – 即使是大型圖紙，光柵化速度亦相當快。

## 前置作業

開始之前，請確保您已：

- 在專案中安裝 **Aspose.CAD for .NET**。您可以從[網站](https://reference.aspose.com/cad/net/)下載。  
- 準備一個範例 DGN 檔案（例如 `Nikon_D90_Camera.dgn`），並放置於已知目錄下。

## 匯入命名空間

先加入必要的 `using` 陳述式，以便存取 Aspose.CAD 類別。

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## 步驟 1：載入 DGN 檔案

將來源 DGN 載入至 `CadImage` 物件。此物件代表記憶體中的 CAD 圖紙，將作為光柵化的來源。

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Your code for further processing goes here
}
```

## 步驟 2：定義光柵化選項

設定 CAD 圖紙的光柵化方式。您可以在此控制影像尺寸、縮放比例與背景顏色。

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 600;
rasterizationOptions.PageHeight = 300;
rasterizationOptions.NoScaling = true;
rasterizationOptions.AutomaticLayoutsScaling = false;
```

## 步驟 3：選擇輸出格式（PNG 或 JPEG）

雖然本教學以 PNG 為主，但您也可能想 **save cad as jpeg**。建立相應的影像選項物件，並將光柵化設定附加上去。

```csharp
ImageOptionsBase options = new JpegOptions();   // Change to PngOptions() for PNG output
options.VectorRasterizationOptions = rasterizationOptions;
```

> **專業提示：** 若要產生 PNG 檔案，將 `new JpegOptions()` 改為 `new PngOptions()`。

## 步驟 4：儲存光柵影像

最後，對 `CadImage` 實例呼叫 `Save`，提供目標檔名與先前設定好的選項物件。

```csharp
cadImage.Save(MyDir + "ExportDGNToRasterImage_out.jpg", options);
```

如果您改用了 `PngOptions`，檔案將會儲存為 `ExportDGNToRasterImage_out.png`。

## 常見問題與解決方案

| 問題 | 原因 | 解決方式 |
|------|------|----------|
| **輸出影像為空白** | `NoScaling` 設定不正確或未選取版面 | 設定 `AutomaticLayoutsScaling = true` 或指定所需版面。 |
| **大型檔案記憶體不足** | 未使用串流載入巨型 DGN | 使用 `Image.Load(sourceFilePath, new LoadOptions { LoadOnDemand = true })`。 |
| **不支援的 DGN 版本** | MicroStation 版本過舊 | 確認使用最新的 Aspose.CAD 版本，以支援舊版格式。 |

## 常見問答

**Q: 可以將 DGN 匯出為 JPEG 以外的格式嗎？**  
A: 可以，Aspose.CAD for .NET 支援 PNG、BMP、GIF、TIFF 等，只需更換選項類別（例如 `new PngOptions()`）。

**Q: 轉換過程中應如何處理例外情況？**  
A: 將轉換程式碼包在 `try/catch` 區塊，並記錄 `Aspose.CAD.CadException` 以取得詳細錯誤資訊。

**Q: 有提供 Aspose.CAD for .NET 的試用版嗎？**  
A: 有，您可以免費試用。前往[此處](https://releases.aspose.com/)了解更多資訊。

**Q: 哪裡可以取得 Aspose.CAD for .NET 的支援或討論區？**  
A: 請前往[Aspose.CAD 論壇](https://forum.aspose.com/c/cad/19)與社群交流。

**Q: 如何取得 Aspose.CAD for .NET 的臨時授權？**  
A: 前往[此連結](https://purchase.aspose.com/temporary-license/)取得開發所需的臨時授權。

## 結論

您現在已學會如何使用 Aspose.CAD for .NET **convert dgn to png**（或 JPEG）。只要調整光柵化選項並切換影像選項類別，即可依專案需求客製化輸出。歡迎嘗試不同的頁面尺寸、DPI 設定與檔案格式，取得最適合您應用程式的點陣圖像。

---

**最後更新：** 2026-03-24  
**測試環境：** Aspose.CAD 24.11 for .NET  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}