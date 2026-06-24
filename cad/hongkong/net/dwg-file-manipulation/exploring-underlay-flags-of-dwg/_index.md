---
date: 2026-04-09
description: 在本逐步指南中，學習如何使用 Aspose.CAD for .NET 將 DWG 轉換為圖像，以及如何讀取底圖旗標。
keywords:
- convert dwg to image
- how to read underlay
- Aspose.CAD DWG underlay flags
linktitle: 探索 DWG 檔案的底圖旗標
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: 將 DWG 轉換為圖像 – 探索 DWG 檔案的底圖旗標 - Aspose.CAD 教程
url: /zh-hant/net/dwg-file-manipulation/exploring-underlay-flags-of-dwg/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 探索 DWG 檔案的 Underlay 旗標 - Aspose.CAD 教程

## 介紹

如果您正深入研究 CAD 檔案，特別是 DWG 檔案，並且想要 **將 DWG 轉換為影像** 同時了解 **如何讀取 Underlay 旗標**，那麼您來對地方了。本教學使用功能強大的 Aspose.CAD for .NET 函式庫，逐步說明如何擷取 Underlay 資訊並自信地將圖面渲染為影像。

## 快速解答
- **「將 DWG 轉換為影像」是什麼意思？**  
  即使用 Aspose.CAD 將 DWG 圖面渲染成點陣格式（PNG、JPEG 等）。
- **哪個方法可取得 Underlay 旗標？**  
  載入 DWG 後，存取 `CadUnderlay` 物件的 `Flags` 屬性。
- **使用 Aspose.CAD 是否需要授權？**  
  評估期間可使用臨時授權；正式環境需購買完整授權。
- **支援哪些 .NET 版本？**  
  .NET Framework 4.6+、.NET Core 3.1+、.NET 5/6 及更新版本。
- **可以擷取 Underlay 幾何資訊嗎？**  
  可以——包括 Underlay 路徑、插入點、縮放、旋轉以及旗標狀態。

## 「將 DWG 轉換為影像」是什麼以及為何重要？

將 DWG 檔案轉換為影像，可讓您在瀏覽器中顯示 CAD 圖面、嵌入報告，或與沒有 CAD 檢視器的利害關係人分享。渲染時，您常需要檢查 **Underlay** 物件（例如 DGN 參照），確保其正確顯示。了解 Underlay 旗標有助於在產生最終影像前，排除裁切、單色渲染與可見性問題。

## 前置條件

- 具備基本的 C# 與 .NET 程式設計知識。  
- 已安裝 **Aspose.CAD for .NET** 函式庫。若尚未取得，請前往 **[此處](https://releases.aspose.com/cad/net/)** 下載。  
- 測試用的 DWG 檔案——本教學全程使用樣本檔 **「BlockRefDgn.dwg」**。

## 匯入命名空間

開始之前，先匯入必要的命名空間：

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## 第一步：載入 DWG 檔案並轉換為 `CadImage`

首先，載入 DWG 檔案並將其轉型為 `CadImage`。此物件讓您存取圖面中的所有實體，包括 Underlay。

```csharp
string fileName = MyDir + "BlockRefDgn.dwg";

// Load DWG file and convert to CadImage
using (CadImage image = (CadImage)Image.Load(fileName))
{
    // Your code for subsequent steps will go here
}
```

## 第二步：遍歷實體

接著，遍歷圖面中的每個實體。此步驟可協助您定位 Underlay 物件。

```csharp
foreach (CadBaseEntity entity in image.Entities)
{
    // Your code for subsequent steps will go here
}
```

## 第三步：檢查 `CadDgnUnderlay` 類型

透過檢查執行時類型來辨識 Underlay 實體。`CadDgnUnderlay` 類別代表嵌入於 DWG 的 DGN Underlay。

```csharp
if (entity is CadDgnUnderlay)
{
    // Your code for subsequent steps will go here
}
```

## 第四步：存取 Underlay 旗標

取得 `CadDgnUnderlay` 後，將其轉型為 `CadUnderlay`，即可讀取其屬性與旗標狀態。旗標告訴您 Underlay 是否可見、是否被裁切，或是否以單色方式渲染。

```csharp
CadUnderlay underlay = entity as CadUnderlay;

Console.WriteLine(underlay.UnderlayPath);
Console.WriteLine(underlay.UnderlayName);
Console.WriteLine(underlay.InsertionPoint.X);
Console.WriteLine(underlay.InsertionPoint.Y);
Console.WriteLine(underlay.RotationAngle);
Console.WriteLine(underlay.ScaleX);
Console.WriteLine(underlay.ScaleY);
Console.WriteLine(underlay.ScaleZ);
Console.WriteLine((underlay.Flags & UnderlayFlags.UnderlayIsOn) == UnderlayFlags.UnderlayIsOn);
Console.WriteLine((underlay.Flags & UnderlayFlags.ClippingIsOn) == UnderlayFlags.ClippingIsOn);
Console.WriteLine((underlay.Flags & UnderlayFlags.Monochrome) != UnderlayFlags.Monochrome);
```

### 輸出說明

- **UnderlayPath / UnderlayName** – 外部 DGN 檔案所在位置。  
- **InsertionPoint (X, Y)** – Underlay 在 DWG 空間中的插入座標。  
- **RotationAngle** – Underlay 的旋轉角度。  
- **ScaleX / ScaleY / ScaleZ** – 各軸的縮放比例。  
- **Flags** – 布林值，分別表示可見性 (`UnderlayIsOn`)、裁切 (`ClippingIsOn`) 與單色渲染 (`Monochrome`)。

## 常見問題與解決方案

| 問題 | 原因 | 解決方式 |
|------|------|----------|
| 旗標檢查無輸出 | 當 Underlay 被關閉時，旗標預設為 0。 | 確認 DWG 確實包含已啟用的 Underlay，或在原始 CAD 檔案中切換可見性。 |
| `Invalid cast` 例外 | 該實體不是 `CadDgnUnderlay`。 | 在轉型前先使用 `if (entity is CadDgnUnderlay)` 進行類型檢查。 |
| 旗標提取後影像渲染失敗 | Underlay 可能被裁切或關閉，導致區域為空白。 | 在最終渲染前調整旗標（`UnderlayIsOn = true`、`ClippingIsOn = false`）。 |

## 常見問答

### Q1: 我可以在 .NET 中使用 Aspose.CAD 處理其他 CAD 檔案格式嗎？

A1: Aspose.CAD 支援多種 CAD 格式，包括 DWG、DXF、DGN 等。完整列表請參閱文件。

### Q2: 是否提供 Aspose.CAD for .NET 的臨時授權？

A2: 有，您可在 **[此處](https://purchase.aspose.com/temporary-license/)** 取得臨時授權。

### Q3: 在哪裡可以取得 Aspose.CAD for .NET 的支援？

A3: 請前往支援論壇 **[此處](https://forum.aspose.com/c/cad/19)** 尋求協助。

### Q4: 如何購買 Aspose.CAD for .NET？

A4: 您可於 **[此處](https://purchase.aspose.com/buy)** 完成購買。

### Q5: 是否有免費試用版？

A5: 有，請至 **[此處](https://releases.aspose.com/)** 下載免費試用版。

## 結論

恭喜您！您已成功學會 **將 DWG 轉換為影像**，同時掌握使用 Aspose.CAD for .NET 讀取 Underlay 旗標的技巧。透過本知識，您可以：

- 將 DWG 圖面渲染為網頁或報告用的點陣影像。  
- 檢查並操作 Underlay 屬性，確保正確顯示。  
- 在產生最終影像前，除錯可見性、裁切與單色問題。

歡迎探索 Aspose.CAD 的其他功能，如圖層管理、文字擷取與批次轉換，進一步擴充您的 CAD 自動化工作流程。

---

**最後更新：** 2026-04-09  
**測試環境：** Aspose.CAD for .NET 24.11  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}