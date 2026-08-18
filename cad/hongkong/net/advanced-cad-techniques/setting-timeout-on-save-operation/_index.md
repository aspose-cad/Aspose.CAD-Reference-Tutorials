---
date: 2026-03-05
description: 了解如何在使用 Aspose.CAD for .NET 將 DWG 轉換為 PDF 時設定儲存作業的逾時時間，提升 .NET 應用程式的效能與控制力。
linktitle: Setting Timeout on Save Operation
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: 設定儲存操作的逾時 - Aspose.CAD 教學
url: /zh-hant/net/advanced-cad-techniques/setting-timeout-on-save-operation/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何在保存操作上設定逾時 - Aspose.CAD 教程

## 介紹

在本指南中，您將學習 **how to set timeout** 在 CAD 保存操作上的設定方法，這項技術可防止長時間執行的轉換變成無回應的程序。當您在批次作業或 Web 服務中 **convert DWG to PDF** 或 **export CAD PDF** 時，管理逾時尤其有用。Aspose.CAD for .NET 提供了簡潔的 API，讓您在利用其強大光柵化引擎的同時，仍能控制保存操作。

## 快速回答
- **逾時控制什麼？** 若執行時間超過指定期間，將中止保存/匯出操作。  
- **哪種格式受益最大？** 將大型 DWG 檔案轉換為 PDF 或光柵圖像時，處理時間可能會有較大差異。  
- **是否需要授權？** 生產環境必須使用有效的 Aspose.CAD 授權；免費試用版可用於評估。  
- **我可以自訂時長嗎？** 可以——只需更改 `Thread.Sleep` 的值（毫秒）以符合您的情境。  
- **此方法是否支援非同步？** 範例使用 `Task.Factory.StartNew`，可輕鬆整合至非同步工作流程。

## 在 CAD 保存的情境中，「設定逾時」是什麼意思？
設定逾時即是將 `InterruptionToken` 附加至保存選項，並在預定的時間間隔後觸發中斷。這可防止操作無限期掛起，讓效能更可預測，資源管理也更完善。

## 為什麼要使用 Aspose.CAD 轉換 DWG 為 PDF 並設定逾時？
- **可靠性：** 保證失控的轉換不會阻塞您的服務。  
- **可擴展性：** 讓您能平行處理多個檔案，而不必擔心單一檔案卡住整條流水線。  
- **品質：** 在加入安全控制的同時，仍保留 Aspose.CAD 的高保真光柵化效果。

## 前置條件

在開始之前，請確保您已具備以下項目：

- **Aspose.CAD for .NET** – 已整合至您的專案中。您可以在此處下載 [here](https://releases.aspose.com/cad/net/)。  
- **文件目錄** – 用於存放來源 DWG 檔案與輸出 PDF 的資料夾。

## 匯入命名空間

首先，匯入提供光柵化、PDF 選項以及中斷機制所需類別的命名空間。

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Threading;
using System.Threading.Tasks;
```

## 如何在保存操作上設定逾時

以下為逐步說明。每一步皆包含簡短說明，並附上原始程式碼區塊（保持不變）。

### 步驟 1：載入 CAD 圖紙

我們從指定目錄載入來源 DWG 檔案。`Image.Load` 方法會回傳代表 CAD 圖紙的 `Image` 物件。

```csharp
// Example: Loading CAD Drawing
string SourceDir = "Your Document Directory";
string OutputDir = "Your Document Directory";

using (Image cadDrawing = Image.Load(SourceDir + "Drawing11.dwg"))
{
    // Code for subsequent steps will be placed here
}
```

### 步驟 2：設定光柵化選項

設定光柵化選項，使匯出的 PDF 與原始圖紙尺寸相符。此處可控制頁面寬度、高度以及其他渲染設定。

```csharp
// Example: Configuring Rasterization Options
var rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = cadDrawing.Size.Width;
rasterizationOptions.PageHeight = cadDrawing.Size.Height;
```

### 步驟 3：建立 PDF 選項（匯出 CAD PDF）

建立 `PdfOptions` 實例並附加光柵化設定。此物件將傳遞給 `Save` 方法，以產生 DWG 檔案的 PDF 版本。

```csharp
// Example: Creating PDF Options
PdfOptions CADf = new PdfOptions();
CADf.VectorRasterizationOptions = rasterizationOptions;
```

### 步驟 4：實作逾時機制

我們使用 `InterruptionTokenSource` 取得可中斷保存操作的 token。背景工作執行匯出，而主執行緒則以 `Thread.Sleep` 進入指定的逾時時長（例如 10 秒）。睡眠結束後，若操作仍在執行，呼叫 `Interrupt()` 以取消它。

```csharp
// Example: Implementing Timeout Mechanism
using (var its = new InterruptionTokenSource())
{
    CADf.InterruptionToken = its.Token;

    var exportTask = Task.Factory.StartNew(() =>
    {
        cadDrawing.Save(OutputDir + "PutTimeoutOnSave_out.pdf", CADf);
    });

    Thread.Sleep(10000); // Set your desired timeout duration in milliseconds
    its.Interrupt();

    exportTask.Wait();
}
```

### 步驟 5：完成並確認

匯出（或中斷）完成後，於主控台寫入確認訊息。實際應用中您可能會記錄結果或觸發事件。

```csharp
// Example: Finalizing and Confirming
Console.WriteLine("PutTimeoutOnSave executed successfully");
```

## 常見問題與解決方案

| 問題 | 原因 | 解決方案 |
|------|------|----------|
| 匯出無限期掛起 | 未附加中斷 token | 確保在啟動任務前設定 `CADf.InterruptionToken = its.Token;` |
| PDF 為空白或損毀 | 輸出目錄路徑不正確 | 檢查 `OutputDir` 是否以路徑分隔符結尾，且檔名有效 |
| 逾時過短導致過早中止 | `Thread.Sleep` 時間對大型檔案太低 | 增加睡眠時長，或根據檔案大小計算自適應逾時 |

## 常見問答

**Q1：我可以自訂逾時時長嗎？**  
A：當然可以。只需修改傳入 `Thread.Sleep` 的值（毫秒），以符合您的效能預期。

**Q2：還有其他光柵化選項嗎？**  
A：有。`CadRasterizationOptions` 提供 `Resolution`、`BackgroundColor`、`DrawType` 等屬性，可微調 PDF 輸出。

**Q3：我該如何在應用程式中處理中斷？**  
A：如範例所示，使用 `InterruptionToken` 與 `InterruptionTokenSource` 類別。它們提供執行緒安全的方式來中止長時間執行的操作。

**Q4：Aspose.CAD 是否同時支援 2D 與 3D CAD 檔案？**  
A：是的。它支援多種 2D 與 3D 格式，包括 DWG、DXF、DGN 等。

**Q5：我可以在哪裡取得更多協助或社群支援？**  
A：請造訪 [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) 參與社群討論、取得範例程式碼與故障排除建議。

## 結論

透過上述步驟，您現在已掌握 **how to set timeout** 在 CAD 保存操作上的設定方式，能可靠地 **convert DWG to PDF** 或 **export CAD PDF** 檔案，同時避免程式變成無回應。將此模式套用於批次轉換、Web 服務或任何自動化流水線，即可提升可預測性。

---

**Last Updated:** 2026-03-05  
**Tested With:** Aspose.CAD 24.12 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}