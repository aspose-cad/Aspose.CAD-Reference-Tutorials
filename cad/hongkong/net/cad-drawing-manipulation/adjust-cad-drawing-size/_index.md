---
date: 2026-03-19
description: 了解如何在 .NET 中使用 Aspose.CAD 重新調整 CAD 圖紙大小，包括如何縮放 CAD 圖紙單位及調整版面尺寸。請跟隨我們的逐步指南。
linktitle: Adjusting CAD Drawing Size
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: 如何使用 Aspose.CAD for .NET 調整 CAD 圖紙尺寸
url: /zh-hant/net/cad-drawing-manipulation/adjust-cad-drawing-size/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何使用 Aspose.CAD for .NET 調整 CAD 圖紙大小

## 介紹

如果您需要 **直接在 .NET 應用程式中調整 CAD** 檔案的大小，您來對地方了。在本教學中，我們將示範如何變更 CAD 單位設定、縮放 CAD 圖紙尺寸，並以程式方式使用 Aspose.CAD for .NET 調整 CAD 大小。完成本指南後，您將擁有一套可直接投入生產環境的完整 CAD 調整解決方案。

## 快速回答
- **需要哪個函式庫？** Aspose.CAD for .NET  
- **可以變更單位類型嗎？** 可以 – 在 `CadRasterizationOptions` 中設定 `UnitType`  
- **正式環境需要授權嗎？** 非試用版使用時必須擁有有效的 Aspose.CAD 授權  
- **範例匯出為哪種影像格式？** BMP（任何支援的點陣格式皆可）  
- **程式碼行數多少？** 完整的調整操作少於 30 行  

## 「如何調整 CAD」實務上是什麼意思？
調整 CAD 圖紙大小是指將向量資料以特定比例或單位（例如公分、英吋）轉換為點陣圖像。當您需要在報告中嵌入圖紙、產生縮圖，或將 CAD 視覺效果整合至網頁時，這項功能相當實用。

## 為什麼要使用 Aspose.CAD 調整 CAD 大小？
- **不需外部 CAD 軟體** – 所有操作皆在 .NET 程式碼內完成。  
- **細緻的單位、版面與點陣化設定控制**。  
- **跨格式支援** – 同一段程式碼可同時處理 DWG、DXF、DWF 等多種格式。  

## 前置條件

在開始之前，請確保您已具備：

- Aspose.CAD for .NET 函式庫：從 [Aspose.CAD for .NET 下載頁面](https://releases.aspose.com/cad/net/) 下載並安裝。  
- 範例 CAD 圖紙：例如 `sample.dwg`，放置於專案的 document 目錄下。  

## 匯入命名空間

首先，匯入可讓您使用 Aspose.CAD 類別的命名空間。

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## 步驟 1：載入 CAD 圖紙

將來源檔案載入為 `Image` 物件。此物件代表記憶體中的 CAD 圖紙，並作為後續所有操作的基礎。

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "sample.dwg";

// Load a CAD drawing in an instance of Image
using (var image = Aspose.CAD.Image.Load(sourceFilePath))
{
    // Your code here...
}
```

## 步驟 2：建立 BmpOptions（或其他點陣格式）

`BmpOptions` 告訴 Aspose.CAD 在儲存為位圖時如何渲染向量資料。您也可以依需求改用 `PngOptions`、`JpegOptions` 等其他格式。

```csharp
Aspose.CAD.ImageOptions.BmpOptions bmpOptions = new Aspose.CAD.ImageOptions.BmpOptions();
```

## 步驟 3：設定 CadRasterizationOptions

`CadRasterizationOptions` 包含縮放、單位轉換與版面選擇等核心設定。將它指派給 `BmpOptions` 的 `VectorRasterizationOptions` 屬性，可確保點陣化器使用您自訂的設定。

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions cadRasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
bmpOptions.VectorRasterizationOptions = cadRasterizationOptions;
```

## 步驟 4：設定 UnitType（變更 CAD 單位）

此處將 CAD 單位從預設值改為公分。這正是 **change cad unit** 關鍵字所在之處，會直接影響最終影像的大小。

```csharp
cadRasterizationOptions.UnitType = Aspose.CAD.ImageOptions.UnitType.Centimeter;
```

## 步驟 5：選擇版面（設定 CAD 版面）

若圖紙包含多個版面（例如 Model、Sheet1），請指定要點陣化的版面。正確選擇版面是 **set cad layouts** 以產生調整後輸出的關鍵。

```csharp
cadRasterizationOptions.Layouts = new string[] { "Model" };
```

## 步驟 6：匯出為 BMP（調整 CAD 圖紙大小）

最後，將點陣化的影像儲存下來。輸出檔案會反映您先前設定的新尺寸、單位與版面——即完成 **resize CAD drawing** 的全部流程。

```csharp
string outPath = sourceFilePath + ".bmp";
image.Save(outPath, bmpOptions);
```

現在您已取得一個代表調整後 CAD 圖紙的 BMP 檔案，可供後續處理或顯示使用。

## 常見問題與解決方案

| 問題 | 為何會發生 | 解決方式 |
|------|------------|----------|
| 輸出影像模糊 | 預設 DPI（每英吋點數）過低 | 在儲存前設定 `cadRasterizationOptions.Resolution = 300;` |
| 版面顯示錯誤 | 版面名稱拼寫錯誤 | 使用 CAD 檢視器或 `Layouts` 集合確認正確的版面名稱 |
| 單位換算不正確 | 公制與英制混用 | 確認 `UnitType` 與目標測量系統相符 |

## 常見問答

### Q1：Aspose.CAD for .NET 是否支援所有 CAD 格式？

A1：Aspose.CAD for .NET 支援多種 CAD 格式，包括 DWG、DXF、DWF 等。完整支援清單請參閱[文件說明](https://reference.aspose.com/cad/net/)。

### Q2：可以同時調整多個版面嗎？

A2：可以，透過在 `CadRasterizationOptions` 的 `Layouts` 陣列中加入多個版面即可一次處理。

### Q3：在哪裡可以取得 Aspose.CAD for .NET 的技術支援？

A3：請前往[Aspose.CAD 論壇](https://forum.aspose.com/c/cad/19)取得社群支援與協助。

### Q4：有提供免費試用嗎？

A4：有，您可前往[免費試用頁面](https://releases.aspose.com/)體驗 Aspose.CAD for .NET 的功能。

### Q5：如何取得 Aspose.CAD for .NET 的臨時授權？

A5：請至[此處](https://purchase.aspose.com/temporary-license/)申請測試用的臨時授權。

## 常見問答

**Q：如何在不變更單位類型的情況下縮放 CAD 圖紙？**  
A：調整 `CadRasterizationOptions` 的 `Zoom` 屬性（例如 `cadRasterizationOptions.Zoom = 2.0;`）即可在保持原始單位的前提下將尺寸放大兩倍。

**Q：可以匯出成 BMP 以外的格式嗎？**  
A：當然可以。只要將 `BmpOptions` 換成 `PngOptions`、`JpegOptions` 或其他支援的點陣格式類別即可。

**Q：能否批次處理資料夾內的多個圖紙？**  
A：可以。遍歷目錄中的檔案，套用相同的點陣化邏輯，並以唯一名稱儲存每個輸出檔案。

---

**最後更新日期：** 2026-03-19  
**測試環境：** Aspose.CAD for .NET 24.11（撰寫時的最新版本）  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}