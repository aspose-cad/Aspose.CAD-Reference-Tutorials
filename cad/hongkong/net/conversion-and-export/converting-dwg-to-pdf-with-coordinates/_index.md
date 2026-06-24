---
date: 2026-04-03
description: 學習如何在 C# 中使用 Aspose.CAD 設定視口並將 DWG 轉換為 PDF。本 DWG 轉 PDF 教程展示了帶坐標的精確匯出。
keywords:
- how to set viewport
- dwg to pdf tutorial
- convert dwg to pdf c#
linktitle: 使用 C# 將 DWG 轉換為帶座標的 PDF
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: 在 C# 中將 DWG 轉換為 PDF 時設定視口與座標 - Aspose.CAD 教程
url: /zh-hant/net/conversion-and-export/converting-dwg-to-pdf-with-coordinates/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 C# 中使用座標將 DWG 轉換為 PDF - Aspose.CAD 教程

## 簡介

歡迎閱讀本完整教程，說明如何在使用 Aspose.CAD for .NET 轉換 DWG 檔案為 PDF 時 **how to set viewport** 並指定座標。透過控制視口，您可以獲得與需求區域完全相符的像素完美 PDF——非常適合建築圖紙、樓層平面圖預覽或任何 BIM 工作流程。

## 快速回答
- **What does “set viewport” mean?** 它定義了在光柵化過程中 CAD 圖形的可見區域和縮放比例。  
- **Which library handles the conversion?** Aspose.CAD for .NET.  
- **Do I need a license?** 免費試用可用於評估；商業授權則需於正式環境使用。  
- **Supported platforms?** Windows、Linux 與 macOS，支援 .NET 5/6/7 或 .NET Framework 4.6+。  
- **Typical implementation time?** 基本轉換大約需要 10‑15 分鐘。  

## 先決條件

在開始之前，請確保您已具備以下先決條件：

- **Aspose.CAD Library** – 下載並安裝適用於 .NET 的 Aspose.CAD 函式庫。您可於 [here](https://releases.aspose.com/cad/net/) 找到該函式庫。  
- **Development Environment** – Visual Studio、Rider 或任何支援 .NET 開發的 IDE。  
- **DWG File** – 準備好要轉換的 DWG 檔案。您可以使用提供的範例檔或自行的 DWG 檔案。  

## 如何設定視口以精確匯出 PDF

設定視口是讓您定義欲渲染圖形精確區域的核心步驟。在以下程式碼中，我們建立新的 `CadVportTableObject`，以左上角座標定位，並計算寬度、高度與長寬比。這就是 **how to set viewport** 的實作，驅動後續的轉換。

## 匯入命名空間

在您的 C# 專案中，匯入必要的命名空間：

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadParameters;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.ImageOptions;
```

讓我們逐步分解程式碼，以便更好地了解：

## 步驟 1：定義文件目錄

```csharp
string MyDir = "Your Document Directory";
```

## 步驟 2：設定來源 DWG 檔案路徑

```csharp
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";
```

## 步驟 3：載入 DWG 檔案並設定光柵化選項

```csharp
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
    rasterizationOptions.Layouts = new string[] { "Model" };
    rasterizationOptions.NoScaling = true;
```

## 步驟 4：定義座標與視口  

在此我們實際 **set the viewport**（how to set viewport），透過指定左上角座標、寬度與高度來設定欲匯出的區域。

```csharp
    Point topLeft = new Point(500, 1000);
    double width = 3108;
    double height = 2489;

    CadVportTableObject newView = new CadVportTableObject();
    newView.Name = new CadStringParameter();
    newView.Name.Init("*Active");
    newView.CenterPoint.X = topLeft.X + width / 2f;
    newView.CenterPoint.Y = topLeft.Y - height / 2f;
    newView.ViewHeight.Value = height;
    newView.ViewAspectRatio.Value = width / height;
```

## 步驟 5：套用視口設定

```csharp
    for (int i = 0; i < cadImage.ViewPorts.Count; i++)
    {
        CadVportTableObject currentView = (CadVportTableObject)(cadImage.ViewPorts[i]);
        if (cadImage.ViewPorts.Count == 1 || string.Equals(currentView.Name.Value.ToLowerInvariant(), "*active"))
        {
            cadImage.ViewPorts[i] = newView;
            break;
        }
    }
```

## 步驟 6：設定 PDF 選項並匯出  

現在我們將所有設定結合，使用剛才準備的光柵化選項 **convert DWG to PDF**。

```csharp
    Aspose.CAD.ImageOptions.PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions();
    pdfOptions.VectorRasterizationOptions = rasterizationOptions;

    MyDir = MyDir + "ConvertDWGToPDFBySupplyingCoordinates_out.pdf";
    cadImage.Save(MyDir, pdfOptions);
}
```

## 步驟 7：顯示成功訊息

```csharp
Console.WriteLine("\nThe DWG file exported successfully to PDF.\nFile saved at " + MyDir);
```

## 常見使用情境

- **Construction documentation** – 產生特定樓層平面圖區段的可列印 PDF。  
- **BIM coordination** – 僅匯出感興趣的區域以進行衝突偵測。  
- **Client presentations** – 提供選定房間或立面的乾淨 PDF，避免顯示整張圖紙。  

## 結論

恭喜！您已成功 **converted DWG to PDF**，並使用 Aspose.CAD for .NET 以精確座標完成 **how to set viewport**。本 **dwg to pdf tutorial** 展示了如何 **create pdf from dwg** 以及 **export dwg as pdf c#**，同時完整掌控輸出區域。

## 常見問題

### Q1: 我可以將 Aspose.CAD 用於其他 CAD 檔案格式嗎？

A1: 是的，Aspose.CAD 支援多種 CAD 格式，包括 DWG、DXF、DWF 等。

### Q2: 我該如何在轉換過程中處理錯誤？

A2: 使用 try‑catch 區塊實作錯誤處理機制，以捕捉並管理例外情況。

### Q3: Aspose.CAD 是否適用於 Windows 與 Linux 環境？

A3: 是的，Aspose.CAD 相容於 Windows 與 Linux 平台。

### Q4: 我可以進一步自訂 PDF 輸出嗎？

A4: 當然可以！請探索 Aspose.CAD 提供的豐富選項，以依您的具體需求自訂 PDF 輸出。

### Q5: 我可以在哪裡找到額外的支援或社群討論？

A5: 請前往 [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19) 取得社群支援與討論。

## 其他常見問題

**Q: 此方法是否適用於大型 DWG 檔案（數百 MB）？**  
A: 是的。光柵化以逐頁方式執行，您可以調整 `rasterizationOptions`（例如 `Resolution`）以在品質與記憶體使用之間取得平衡。

**Q: 我可以將多個視口匯出為不同的 PDF 頁面嗎？**  
A: 您可以遍歷 `cadImage.ViewPorts`，將每個視口設為活動，然後對每頁呼叫 `Save`，最後使用 Aspose.PDF 合併 PDF。

**Q: 是否可以為產生的 PDF 加入浮水印？**  
A: 在儲存 PDF 後，您可以使用 Aspose.PDF 重新開啟，並在交付給使用者前套用文字或圖片浮水印。

---

**最後更新：** 2026-04-03  
**測試版本：** Aspose.CAD 24.11 for .NET  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}