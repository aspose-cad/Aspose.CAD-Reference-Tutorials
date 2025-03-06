---
title: 在 C# 中開啟和存取 DWFX 檔案 - Aspose.CAD 指南
linktitle: 在 C# 中開啟和存取 DWFX 文件
second_title: Aspose.CAD .NET - CAD 和 BIM 檔案格式
description: 了解如何使用 Aspose.CAD for .NET 在 C# 中開啟和存取 DWFX 檔案。無縫整合到您的應用程式中的逐步指南。
weight: 12
url: /zh-hant/net/dwg-file-manipulation/opening-and-accessing-dwfx-files/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 C# 中開啟和存取 DWFX 檔案 - Aspose.CAD 指南

## 介紹

歡迎使用我們的逐步指南，了解如何使用強大的 Aspose.CAD for .NET 程式庫在 C# 中開啟和存取 DWFX 檔案。如果您是一位希望將 CAD 功能整合到 C# 應用程式中的開發人員，那麼您來對地方了。在本教程中，我們將引導您完成整個過程，將其分解為簡單的步驟，以便所有技能水平的開發人員都可以使用它。

## 先決條件

在我們深入學習本教程之前，請確保您具備以下先決條件：

1.  Aspose.CAD for .NET 程式庫：確保您已安裝 Aspose.CAD for .NET 程式庫。你可以下載它[這裡](https://releases.aspose.com/cad/net/).

2. 文檔目錄：設定一個目錄來儲存 DWFX 檔案。記下 C# 程式碼中的來源目錄和輸出目錄。

## 導入命名空間

在您的 C# 專案中，首先匯入必要的命名空間：

```csharp
using Aspose.CAD.ImageOptions;
using System;
```

這些命名空間提供了在應用程式中處理 CAD 檔案所需的基本類別和功能。

## 第 1 步：設定來源目錄和輸出目錄

```csharp
string SourceDir = "Your Document Directory";
string OutputDir = "Your Document Directory";
```

將「您的文件目錄」替換為來源目錄和輸出目錄的實際路徑。

## 步驟2：載入DWFX文件

```csharp
using (Image cadDrawing = Image.Load(SourceDir + "Tyrannosaurus.dwfx"))
```

使用以下命令載入 DWFX 文件`Image.Load`方法。將“Tyrannosaurus.dwfx”替換為 DWFX 檔案的實際名稱。

## 步驟 3：配置光柵化選項

```csharp
var rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = cadDrawing.Size.Width;
rasterizationOptions.PageHeight = cadDrawing.Size.Height;
```

根據載入的 CAD 繪圖的大小配置光柵化選項。

## 第 4 步：另存為 PDF

```csharp
PdfOptions CADf = new PdfOptions();
CADf.VectorRasterizationOptions = rasterizationOptions;
cadDrawing.Save(OutputDir + "OpenDwfxFile_out.pdf", CADf);
```

將載入的 DWFX 檔案另存為 PDF，套用配置的光柵化選項。

## 步驟5：顯示成功訊息

```csharp
Console.WriteLine("OpenDwfxFile executed successfully");
```

將成功訊息列印到控制台以確認程式碼成功執行。

## 結論

恭喜！您已成功學習如何使用 Aspose.CAD for .NET 在 C# 中開啟和存取 DWFX 檔案。本指南涵蓋了從設定目錄到載入、設定和儲存 CAD 檔案的基本步驟。

## 常見問題解答

### Q1：Aspose.CAD for .NET 是否與所有 DWFX 檔案相容？

A1：Aspose.CAD for .NET 支援多種 CAD 格式，包括 DWFX。但是，建議檢查文件以了解特定的相容性詳細資訊。

### 問題 2：在哪裡可以找到 Aspose.CAD for .NET 的文件？

 A2：文檔可用[這裡](https://reference.aspose.com/cad/net/).

### Q3：我可以在購買前試用 Aspose.CAD for .NET 嗎？

 A3：是的，您可以下載免費試用版[這裡](https://releases.aspose.com/).

### 問題 4：如何取得 Aspose.CAD for .NET 的臨時許可？

 A4：可以獲得臨時許可證[這裡](https://purchase.aspose.com/temporary-license/).

### Q5：需要支援或有更多問題？

A5：訪問[Aspose.CAD論壇](https://forum.aspose.com/c/cad/19)尋求幫助。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
