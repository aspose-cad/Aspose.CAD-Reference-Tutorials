---
date: 2026-03-31
description: 使用 Aspose.CAD for .NET 將 DWG 轉換為 PDF，並支援 .NET Core PDF 轉換。請參考我們的逐步指南。
keywords:
- convert dwg to pdf
- net core pdf conversion
- aspose cad compliance pdf
- dwg to pdf conversion .net
- cad file format conversion
linktitle: 將 DWG 轉換為合規 PDF
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: 使用 Aspose.CAD for .NET 將 DWG 轉換為 PDF（合規）
url: /zh-hant/net/conversion-and-export/converting-dwg-to-compliance-pdf/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 轉換 DWG 為 PDF – Aspose.CAD 教程

## 介紹

歡迎！在本教學中，您將學習 **如何使用 Aspose.CAD .NET 函式庫將 DWG 轉換為 PDF**。無論您是開發桌面工具、Web 服務，或是必須產生符合 PDF/A‑1a 或 PDF/A‑1b 標準文件的 .NET Core 應用程式，本指南都會一步步帶您完成——從載入 DWG 檔案到儲存符合標準的 PDF。

完成本指南後，您將擁有一段可直接放入任何 .NET 專案的可執行程式碼片段。

## 快速回答
- **需要哪個函式庫？** Aspose.CAD for .NET（支援 .NET Framework 與 .NET Core）。  
- **支援哪些 PDF 合規等級？** PDF/A‑1a 與 PDF/A‑1b。  
- **測試需要授權嗎？** 免費試用版可完美用於開發；正式上線需購買商業授權。  
- **可以在 .NET Core 上執行嗎？** 可以 – 相同程式碼可在 .NET Core、.NET 5/6+ 上執行。  
- **一般實作時間多久？** 基本轉換大約 10 分鐘即可完成。

## 什麼是「convert DWG to PDF」？

DWG 是 AutoCAD 繪圖的原生檔案格式，而 PDF 是一種通用的可檢視文件格式。將 DWG 轉換為 PDF 可讓沒有 CAD 軟體的利害關係人也能檢視圖紙，且 PDF/A 合規可確保長期保存與法律接受度。

## 為何在 .NET Core 中使用 Aspose.CAD 進行 PDF 轉換？

- **零安裝 CAD 引擎** – 不需要 AutoCAD 或其他第三方二進位檔。  
- **完整 .NET Core 相容性** – 一次編寫，隨處執行。  
- **內建 PDF/A 合規** – 只需變更一個屬性即可產生符合保存需求的 PDF。  
- **高保真光柵化** – 保留線寬、顏色與圖層。

## 前置條件

在開始撰寫程式碼前，請確保您已具備：

- **Aspose.CAD for .NET** – 前往[此處](https://releases.aspose.com/cad/net/)下載。  
- **.NET 開發環境**（Visual Studio 2022、VS Code 搭配 C# 擴充功能，或您慣用的任何 IDE）。  
- **範例 DWG 檔案**（本教學使用 `Bottom_plate.dwg`）。

## 匯入命名空間

在您的 .NET 專案中，匯入使用 Aspose.CAD 功能所需的命名空間。

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
```

接下來，我們將把轉換流程拆解為清晰的步驟。

## 步驟 1：載入 DWG 檔案

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";

Aspose.CAD.Image cadImage = Aspose.CAD.Image.Load(sourceFilePath);
```

*說明：*  
`Image.Load` 會自動偵測 DWG 格式，並建立一個記憶體中的表示 (`cadImage`)，之後可用於光柵化或匯出。

## 步驟 2：設定光柵化選項

建立 `CadRasterizationOptions` 實例，並設定背景色、頁寬、頁高等屬性。

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions
{
    BackgroundColor = Aspose.CAD.Color.White,
    PageWidth = 1600,
    PageHeight = 1600
};
```

*為何重要：*  
光柵化會把向量 CAD 資料轉成 PDF 可嵌入的點陣圖。調整 `PageWidth`/`PageHeight` 即可控制最終 PDF 的解析度。

## 步驟 3：建立 PDF 選項

建立 `PdfOptions` 實例，並設定向量光柵化選項。

```csharp
PdfOptions pdfOptions = new PdfOptions
{
    VectorRasterizationOptions = rasterizationOptions,
    CorePdfOptions = new PdfDocumentOptions { Compliance = PdfCompliance.PdfA1a }
};
```

*提示：*  
之後將 `PdfCompliance` 改為 `PdfA1b`，即可在不更動光柵化設定的前提下產生不同的 PDF/A 等級。

## 步驟 4：儲存為 PDF（A1a 合規）

將 CAD 圖像儲存為符合 A1a 標準的 PDF。

```csharp
cadImage.Save(MyDir + "PDFA1_A.pdf", pdfOptions);
```

*結果：*  
`PDFA1_A.pdf` 為 PDF/A‑1a 合規檔案，適用於嚴格的保存需求。

## 步驟 5：儲存為 PDF（A1b 合規）

將合規類型改為 A1b，並儲存 CAD 圖像為符合 PDF/A 的 PDF。

```csharp
pdfOptions.CorePdfOptions.Compliance = PdfCompliance.PdfA1b;
cadImage.Save(MyDir + "PDFA1_B.pdf", pdfOptions);
```

*結果：*  
`PDFA1_B.pdf` 符合 PDF/A‑1b 合規，較為寬鬆但仍廣受接受於保存用途。

## 常見問題與解決方案

| 問題 | 原因 | 解決方式 |
|-------|-------|-----|
| **PDF 輸出空白** | 未設定光柵化選項（例如背景色透明） | 設定 `BackgroundColor = Aspose.CAD.Color.White` 或其他可見顏色。 |
| **大型 DWG 記憶體不足** | 將極大圖檔一次載入記憶體 | 使用較低的 `PageWidth`/`PageHeight`，或盡可能分段處理檔案。 |
| **合規錯誤** | 使用較舊的 Aspose.CAD 版本未支援 PDF/A | 升級至最新的 Aspose.CAD 版本（請於下載頁面確認）。 |

## 常見問答（新）

**Q: 可以使用 Aspose.CAD 將其他 CAD 格式轉為合規 PDF 嗎？**  
A: 可以，Aspose.CAD 支援多種格式（DWG、DXF、DGN 等），皆可匯出為 PDF/A。

**Q: Aspose.CAD 是否相容 .NET Core？**  
A: 完全相容。相同 API 可在 .NET Framework、.NET Core 與 .NET 5/6+ 上執行。

**Q: Aspose.CAD 有哪些授權方案？**  
A: 您可於[此處](https://purchase.aspose.com/buy)了解授權選項。

**Q: 有免費試用版嗎？**  
A: 有，請至[此處](https://releases.aspose.com/)取得免費試用。

**Q: 如需 Aspose.CAD 支援，該去哪裡？**  
A: 前往 [Aspose.CAD 論壇](https://forum.aspose.com/c/cad/19) 取得相關協助。

## 結論

現在您已掌握使用 Aspose.CAD for .NET 進行 **DWG 轉 PDF** 並符合 PDF/A 標準的完整、可投入生產的範例。相同做法同樣適用於 .NET Core 專案，為桌面、Web 或雲端應用提供彈性解決方案。歡迎自行嘗試不同的光柵化設定、頁面尺寸或合規等級，以符合您的特定需求。

---

**最後更新：** 2026-03-31  
**測試環境：** Aspose.CAD 24.12 for .NET  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}