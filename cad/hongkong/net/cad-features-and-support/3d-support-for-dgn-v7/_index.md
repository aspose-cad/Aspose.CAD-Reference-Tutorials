---
date: 2026-03-24
description: 學習如何使用 Aspose.CAD for .NET 將 DGN 轉換為 PDF（及 PNG），支援 DGN V7 的 3D 功能——一步一步的指南。
linktitle: 3D Support for DGN V7
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: 使用 Aspose.CAD for .NET 將 DGN 轉換為 PDF（支援 3D）
url: /zh-hant/net/cad-features-and-support/3d-support-for-dgn-v7/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.CAD for .NET 轉換 DGN 為 PDF（支援 3D）

## 介紹

在現代 CAD 工作流程中，能夠快速 **convert DGN to PDF** 並保留 3‑D 幾何資訊是相當重要的。無論是產生文件、與非 CAD 利害關係人分享設計，或是歸檔專案，Aspose.CAD for .NET 都提供可靠的方式，將 DGN V7 檔案轉換為高品質的 PDF（甚至 PNG）輸出。本教學將逐步說明如何啟用 3D 支援，並從 DGN 檔案產生 PDF。

## 快速回答
- **本教學涵蓋什麼內容？** 啟用 3D 支援並使用 Aspose.CAD for .NET 將 DGN V7 轉換為 PDF。  
- **主要產出格式為何？** PDF（可選 PNG 匯出）。  
- **需要授權嗎？** 免費試用可用於測試；正式環境需購買商業授權。  
- **支援的 .NET 版本？** .NET Framework 4.5 以上、.NET Core 3.1 以上、.NET 5/6 以上。  
- **實作大約需要多久？** 基本轉換約 10‑15 分鐘即可完成。

## 什麼是「convert DGN to PDF」？

將 DGN 轉換為 PDF 意指把 MicroStation DGN 檔案中儲存的向量資料渲染成可在任何裝置上檢視的可攜式文件格式，無需專業 CAD 軟體。透過 Aspose.CAD 的 3‑D 光柵化引擎，轉換過程會保留版面、顏色與深度資訊，呈現忠實的視覺效果。

## 為何選擇 Aspose.CAD 進行此轉換？

- **完整 3‑D 光柵化** – 保留深度與版面資訊。  
- **無外部相依** – 純 .NET 函式庫，無需安裝 MicroStation。  
- **多種輸出格式** – PDF、PNG、JPEG、TIFF 等（次要關鍵字 *convert dgn to png* 亦內建支援）。  
- **跨平台** – 可在 Windows、Linux 與 macOS 上執行。

## 前置條件

開始之前，請確保您已具備以下項目：

- 已安裝 Aspose.CAD for .NET。可從 [Aspose.CAD for .NET download page](https://releases.aspose.com/cad/net/) 下載。  
- 一個欲處理的有效 DGN V7 檔案。  
- .NET 開發環境（Visual Studio、VS Code 或 CLI）。安裝說明請參考 [.NET documentation](https://docs.microsoft.com/en-us/dotnet/core/install/)。

## 匯入命名空間

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

上述命名空間讓您可以使用 Aspose.CAD 的核心類別與標準 .NET 工具。

## 步驟 1：設定環境

定義來源 DGN 檔案所在位置與輸出 PDF 的儲存路徑。

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";
```

> **小技巧：** 使用 `Path.Combine` 以確保路徑在不同平台上皆正確。

## 步驟 2：載入 DGN 檔案

使用 `Image.Load` 建立 `DgnImage` 實例，為光柵化做準備。

```csharp
using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Code snippet continues...
}
```

## 步驟 3：設定匯出選項

建立 `PdfOptions` 並搭配 `CadRasterizationOptions`。在此您可以控制頁面尺寸、背景色與要匯出的版面（視圖）。

```csharp
var options = new PdfOptions
{
    VectorRasterizationOptions = new CadRasterizationOptions
    {
        PageWidth = 1500,
        PageHeight = 1500,
        CenterDrawing = true,
        AutomaticLayoutsScaling = true,
        BackgroundColor = Color.Black,
        Layouts = new string[] { "1", "2", "3", "9" } // Export specific views
    }
};
```

若需 **convert DGN to PNG**，只要將 `PdfOptions` 換成 `PngOptions`，其餘光柵化設定保持不變。

## 步驟 4：儲存結果

最後，將渲染後的輸出寫入指定位置。

```csharp
string outFile = "Your Output Directory"; // Specify the output directory
dgnImage.Save(outFile, options);
```

執行完畢後，您會在目標資料夾中看到 PDF 檔（若改用 PNG，則會得到 PNG 檔），其內容忠實呈現原始 3‑D DGN 圖面。

## 常見問題與技巧

- **版面遺失：** 確認 `Layouts` 中的版面名稱與 DGN 檔案內相符，否則會被忽略。  
- **大型檔案：** 逐步調整 `PageWidth`/`PageHeight`，避免記憶體使用過高。  
- **顏色準確度：** 若背景顯得過暗，請確認 `BackgroundColor` 已設定為期望的顏色（例如 `Color.White`）。

## 結論

現在您已掌握如何使用 Aspose.CAD for .NET 以完整 3‑D 支援 **convert DGN to PDF**。此工作流程可整合至自動化管線、桌面工具或 Web 服務，將 CAD 視覺化結果提供給任何觀眾。

## 常見問答

### Q1: 可以同時處理多個 DGN 檔案嗎？

A1: 可以，您只需將程式碼改寫為在迴圈或批次處理系統中逐一處理多個檔案。

### Q2: Aspose.CAD for .NET 還支援哪些匯出格式？

A2: 支援多種格式，包括 PDF、PNG、JPG 等。詳情請參考 [documentation](https://reference.aspose.com/cad/net/)。

### Q3: Aspose.CAD for .NET 是否相容最新的 .NET Core 版本？

A3: 相容，請確保您的環境已安裝相對應的版本。

### Q4: 我可以進一步自訂匯出設定嗎？

A4: 當然可以！提供的程式碼僅為起點，您可在 [Aspose.CAD documentation](https://reference.aspose.com/cad/net/) 中探索更多選項與設定。

### Q5: 我該向哪裡尋求協助或分享使用經驗？

A5: 加入 Aspose.CAD 社群的 [forum](https://forum.aspose.com/c/cad/19)，與其他開發者交流並取得協助。

---

**最後更新：** 2026-03-24  
**測試環境：** Aspose.CAD 24.11 for .NET  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}