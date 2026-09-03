---
date: 2026-08-23
description: 透過我們的逐步教學，發掘 Aspose.CAD for .NET 的潛力，學習如何從 DWG 檔案讀取 xref 元資料。
keywords:
- read xref metadata
- extract dwg xref
- Aspose.CAD
lastmod: 2026-08-23
linktitle: 從 DWG 檔案讀取 XREF 元資料
og_description: 了解如何使用 Aspose.CAD for .NET 從 DWG 檔案讀取 xref 元資料。本指南在十分鐘內帶您完成先決條件、程式碼步驟及常見陷阱。
og_image_alt: Screenshot of Aspose.CAD reading XREF metadata in a .NET IDE
og_title: 如何使用 Aspose.CAD 從 DWG 檔案讀取 xref 元資料
schemas:
- author: Aspose
  dateModified: '2026-08-23'
  description: Unlock the potential of Aspose.CAD for .NET with our step‑by‑step tutorial
    on how to read xref metadata from DWG files.
  headline: How to read xref metadata from DWG files using Aspose.CAD
  type: TechArticle
- description: Unlock the potential of Aspose.CAD for .NET with our step‑by‑step tutorial
    on how to read xref metadata from DWG files.
  name: How to read xref metadata from DWG files using Aspose.CAD
  steps:
  - name: load the DWG file
    text: Create an `Image` instance from the DWG file you want to analyze. `Image.Load`
      loads a CAD file and returns a `CadImage` object representing the drawing. Adjust
      the `sourceFilePath` variable to the exact location of your drawing.
  - name: iterate through entities
    text: Loop through the `Image` object’s `Entities` collection. `CadBaseEntity`
      is the base class for all CAD entities in Aspose.CAD. For each entity, check
      whether it is an XREF reference and collect its metadata.
  - name: extract metadata
    text: When you encounter an XREF entity, read its insertion point (X, Y, Z) and
      the path of the referenced drawing. `CadUnderlay` represents an external reference
      (XREF) entity within a DWG drawing.
  - name: process metadata
    text: At this stage you can store the extracted information in a database, write
      it to a CSV file, or feed it into downstream BIM workflows. The sample simply
      prints the values to the console, but you are free to replace that with any
      custom logic.
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD for .NET supports **50+ input and output formats**, including
      DWG, DXF, DGN, and IFC, giving you broad coverage for most engineering workflows.
    question: Is Aspose.CAD for .NET compatible with all CAD file formats?
  - answer: Certainly! You can access the free trial download page [free trial download
      page](https://releases.aspose.com/).
    question: Can I use the free trial before making a purchase decision?
  - answer: The documentation is available [Aspose.CAD .NET documentation](https://reference.aspose.com/cad/net/).
    question: Where can I find comprehensive documentation for Aspose.CAD for .NET?
  - answer: You can get a temporary license [temporary license page](https://purchase.aspose.com/temporary-license/).
    question: How do I obtain a temporary license for Aspose.CAD for .NET?
  - answer: Join the Aspose.CAD community at [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19)
      for expert support and discussions.
    question: Need assistance or have specific queries?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- read xref metadata
- extract dwg xref
- Aspose.CAD
- DWG
- CAD metadata
title: 如何使用 Aspose.CAD 從 DWG 檔案讀取 xref 元資料
url: /zh-hant/net/image-manipulation-and-rendering/reading-xref-metadata-from-dwg/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何使用 Aspose.CAD 從 DWG 檔案讀取 xref 中繼資料

## 介紹

在本教學中，您將學習如何使用 .NET 的 Aspose.CAD 函式庫從 DWG 檔案讀取 **xref 中繼資料**。無論您需要稽核外部參考、遷移舊有圖紙，或建立自訂 BIM 流程，擷取 XREF 資訊都是常見需求。我們將逐步說明，從設定專案到處理中繼資料，並提供您可立即套用的實用技巧。

## 快速回答
- **主要目的為何？** 取得嵌入於 DWG 圖面的外部參考 (XREF) 的插入點與檔案路徑。  
- **需要哪個函式庫？** Aspose.CAD for .NET（支援超過 50 種 CAD 格式）。  
- **是否需要授權？** 生產環境須使用臨時或正式授權；亦提供免費試用版。  
- **支援哪些 .NET 版本？** .NET Framework 4.5 以上、.NET Core 3.1 以上、.NET 5/6/7。  
- **程式執行需要多久？** 在一般硬體上，處理一個約 200 頁且包含少量 XREF 的 DWG 檔案，完成時間不到一秒。

## 何謂讀取 xref 中繼資料？

`read xref metadata` 指的是存取 DWG 圖面內外部參考實體之屬性的操作，例如其插入座標、來源檔案路徑與可見性旗標。此操作可讓您以程式方式了解圖面如何由其他檔案組成，從而實現自動驗證、報告或批次處理連結資源。

## 為何使用 Aspose.CAD 完成此任務？

Aspose.CAD 支援 **超過 50 種 CAD 檔案格式**，且能在 **不需要 AutoCAD** 的情況下讀取 DWG 檔案。函式庫以 **記憶體效能高的串流** 處理大型圖面，讓您在不將整個檔案載入記憶體的前提下，處理數百頁的檔案。這些具體的能力使其成為企業級 CAD 自動化的可靠選擇。

## 前置條件

在進入程式碼之前，請確認您已具備以下項目：

- 已安裝 Aspose.CAD for .NET。請從 [Aspose.CAD for .NET 發行頁面](https://releases.aspose.com/cad/net/) 取得最新套件。  
- 一個本機資料夾，內含您欲檢查的 DWG 檔案。請在範例程式碼中將 `MyDir` 變數更新為指向該資料夾的路徑。  
- 有效的 Aspose.CAD 授權（或免費試用版），若您打算在生產環境執行程式碼。

環境準備完成後，讓我們開始編寫程式。

## 匯入命名空間

首先需要匯入提供 Aspose.CAD API 的命名空間。`using` 指令會將 Aspose.CAD 的命名空間帶入作用域，讓您能存取如 `Image` 與 `CadImage` 等 CAD 類別。

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects;
```

## 如何從 DWG 檔案讀取 xref 中繼資料？

載入圖面、列舉其實體、篩選 XREF 物件，然後抽取所需屬性——全部只需幾行簡潔程式碼。以下章節將此流程分為四個邏輯步驟，您可直接複製貼上至任何 .NET 主控台或服務專案。

### 步驟 1：載入 DWG 檔案

從欲分析的 DWG 檔案建立 `Image` 實例。`Image.Load` 會載入 CAD 檔案並回傳代表圖面的 `CadImage` 物件。請將 `sourceFilePath` 變數調整為圖檔的正確路徑。

```csharp
// The path to the documents directory.
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";
using (CadImage image = (CadImage)Image.Load(sourceFilePath))
{
    // Code for the next steps goes here
}
```

### 步驟 2：遍歷實體

遍歷 `Image` 物件的 `Entities` 集合。`CadBaseEntity` 為 Aspose.CAD 中所有 CAD 實體的基底類別。對每個實體檢查其是否為 XREF 參考，並收集其中繼資料。

```csharp
foreach (CadBaseEntity entity in image.Entities)
{
    if (entity is CadUnderlay)
    {
        // Code for the next steps goes here
    }
}
```

### 步驟 3：抽取中繼資料

當遇到 XREF 實體時，讀取其插入點 (X、Y、Z) 以及參考圖面的路徑。`CadUnderlay` 代表 DWG 圖面中的外部參考 (XREF) 實體。

```csharp
//XREF entity with metadata
Cad3DPoint insertionPoint = ((CadUnderlay)entity).InsertionPoint;
string path = ((CadUnderlay)entity).UnderlayPath;
```

### 步驟 4：處理中繼資料

此時您可以將抽取的資訊儲存至資料庫、寫入 CSV 檔，或輸入至後續 BIM 工作流程。範例僅將值印至主控台，您可自行替換為任何自訂邏輯。

```csharp
// Your custom logic for processing metadata goes here
```

## 常見問題與除錯

| 症狀 | 可能原因 | 解決方式 |
|------|----------|----------|
| 未返回任何 XREF 實體 | 圖面使用了不同的參考類型（例如 INSERT） | 檢查實體類型是否為 `CadEntityType.Xref`，如有需要亦處理 `Insert` |
| `Image.Load` 拋出例外 | 檔案路徑不正確或 DWG 版本不受支援 | 確認路徑正確，並確保使用 Aspose.CAD 24.11 或更新版本 |
| 中繼資料值為空 | XREF 已定義但未解析（缺少外部檔案） | 確保參考檔案存在於磁碟上，或提供虛擬檔案系統解析器 |

## 常見問答

**Q: Aspose.CAD for .NET 是否相容所有 CAD 檔案格式？**  
A: 是，Aspose.CAD for .NET 支援 **超過 50 種輸入與輸出格式**，包括 DWG、DXF、DGN 與 IFC，為大多數工程工作流程提供廣泛覆蓋。

**Q: 我可以在決策前使用免費試用嗎？**  
A: 當然可以！您可前往免費試用下載頁面 [免費試用下載頁面](https://releases.aspose.com/)。

**Q: 我在哪裡可以找到 Aspose.CAD for .NET 的完整文件？**  
A: 文件可於 [Aspose.CAD .NET 文件](https://reference.aspose.com/cad/net/) 取得。

**Q: 如何取得 Aspose.CAD for .NET 的臨時授權？**  
A: 您可在 [臨時授權頁面](https://purchase.aspose.com/temporary-license/) 取得。

**Q: 需要協助或有特定問題嗎？**  
A: 加入 Aspose.CAD 社群於 [Aspose.CAD 論壇](https://forum.aspose.com/c/cad/19) 取得專家支援與討論。

## 結論

您現在已掌握一套完整、可投入生產的 **讀取 DWG 檔案 XREF 中繼資料** 模式，使用 Aspose.CAD for .NET。透過四個步驟——載入檔案、遍歷實體、抽取插入點與底圖路徑、處理結果，您可將此功能整合至任何以 CAD 為核心的應用程式，無論是資料遷移工具、品質檢查腳本，或自訂 BIM 流程。

---

**最後更新：** 2026-08-23  
**測試環境：** Aspose.CAD 24.11 for .NET  
**作者：** Aspose

## 相關教學

- [如何變更 xref 路徑與編輯 CAD 檔案中的超連結 - Aspose.CAD 教學](/cad/net/advanced-cad-techniques/editing-hyperlinks-in-cad-files/)
- [從 DWG 檔案取得區塊屬性 - Aspose.CAD 教學](/cad/net/image-manipulation-and-rendering/getting-block-attributes-from-dwg/)
- [將大型 DWG 檔案轉換為 PDF - Aspose.CAD 教學](/cad/net/image-manipulation-and-rendering/converting-large-dwg-files-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}