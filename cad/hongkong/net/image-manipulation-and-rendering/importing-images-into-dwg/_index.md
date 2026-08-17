---
date: 2026-08-17
description: 了解如何使用 C# 及 Aspose.CAD for .NET 為 DWG 檔案加入影像。本指南將逐步說明匯入影像、設定插入點以及匯出為
  PDF 的流程。
keywords:
- add image to dwg
- convert dwg to pdf
- set insertion point dwg
- embed png in dwg
- save dwg as pdf
lastmod: 2026-08-17
linktitle: 使用 C# 匯入影像至 DWG 檔案
og_description: 了解如何使用 C# 為 DWG 檔案加入影像。本教學涵蓋匯入影像、設定插入點，以及使用 Aspose.CAD 將 DWG 轉換為 PDF。
og_image_alt: Guide showing C# code to embed an image into a DWG file using Aspose.CAD
og_title: 如何使用 C# 及 Aspose.CAD 為 DWG 檔案加入影像
schemas:
- author: Aspose
  dateModified: '2026-08-17'
  description: Learn how to add image to dwg files using C# and Aspose.CAD for .NET.
    This guide walks you through importing images, setting insertion points, and exporting
    to PDF.
  headline: How to add image to dwg files with C# using Aspose.CAD
  type: TechArticle
- description: Learn how to add image to dwg files using C# and Aspose.CAD for .NET.
    This guide walks you through importing images, setting insertion points, and exporting
    to PDF.
  name: How to add image to dwg files with C# using Aspose.CAD
  steps:
  - name: set up your document directory
    text: Prepare the folder that contains the source DWG and the image you want to
      embed.
  - name: load the dwg file
    text: The `CadImage` class represents a DWG drawing and provides access to its
      entities, layers, and metadata.
  - name: define the image properties
    text: Create an `Image` object that points to the raster file (e.g., PNG) and
      specify its format.
  - name: set insertion point dwg and vectors
    text: Specify where the image should appear inside the drawing and how it should
      be scaled. The insertion point is defined by a 2‑D coordinate, while the vectors
      control width and height.
  - name: create and configure the raster image
    text: Instantiate a `RasterImage` object, assign the image data, and set any additional
      rendering options.
  - name: add image to dwg file
    text: Insert the configured raster image into the DWG’s entities collection so
      it becomes part of the drawing.
  - name: save as pdf (export dwg to pdf)
    text: After embedding the image you can **convert dwg to pdf** or **save dwg as
      pdf** with a single call. This is useful for sharing the drawing with stakeholders
      who don’t have CAD software.
  type: HowTo
- questions:
  - answer: The core library is .NET‑specific, but Aspose offers equivalent APIs for
      Java, Python and other platforms.
    question: Can I use Aspose.CAD for .NET with other programming languages?
  - answer: Yes, you can explore a free trial on the [Aspose free trial page](https://releases.aspose.com/).
    question: Is a free trial available for Aspose.CAD?
  - answer: The documentation is available in the [Aspose.CAD .NET API reference](https://reference.aspose.com/cad/net/).
    question: Where can I find detailed documentation for Aspose.CAD?
  - answer: Visit the [temporary license page](https://purchase.aspose.com/temporary-license/)
      to get a temporary license.
    question: How do I obtain a temporary license for Aspose.CAD?
  - answer: Yes, you can seek support and engage with the community in the [Aspose.CAD
      community forum](https://forum.aspose.com/c/cad/19).
    question: Are there community forums for Aspose.CAD support?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- CAD
- Aspose.CAD
- C# image processing
- DWG manipulation
title: 如何使用 C# 及 Aspose.CAD 為 DWG 檔案加入影像
url: /zh-hant/net/image-manipulation-and-rendering/importing-images-into-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何使用 C# 及 Aspose.CAD 為 DWG 檔案加入影像

## 介紹

在需要使用標誌、相片或點陣圖來豐富 CAD 繪圖時，將影像加入 DWG 檔案是一項常見需求。在本教學中，您將學習如何使用 C# 及 Aspose.CAD for .NET 以程式方式 **add image to dwg**，然後可選擇將結果轉換為 PDF。步驟已拆解，您可以直接複製貼上每個區段到自己的專案中。

## 快速解答
- **哪個函式庫負責此工作？** Aspose.CAD for .NET.
- **我可以嵌入 PNG 檔案嗎？** Yes – PNG, JPEG, BMP and other raster formats are supported.
- **開發時需要授權嗎？** A free trial works for testing; a commercial license is required for production.
- **支援 PDF 匯出嗎？** Absolutely – you can convert the updated DWG to PDF in one line.
- **相容的 .NET 版本有哪些？** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6/7.

## DWG 檔案是什麼？

DWG 檔案是 Autodesk AutoCAD 繪圖的原生二進位格式，用於儲存向量幾何、圖層與中繼資料。它在建築、工程與建設領域被廣泛使用，且 Aspose.CAD 能在不安裝 AutoCAD 的情況下讀寫此格式。

## 為何使用 Aspose.CAD 為 DWG 加入影像？

Aspose.CAD 支援 **50+ 輸入與輸出格式**，能在不將整個文件載入記憶體的情況下處理超過 500 MB 的檔案，並提供在無頭伺服器環境中可運作的確定性 API。這使得大量處理 DWG 繪圖既快速又可靠。

## 前置條件
- 具備 C# 程式設計的基本知識。
- 已安裝 Aspose.CAD for .NET。您可從 [Aspose.CAD for .NET 下載頁面](https://releases.aspose.com/cad/net/) 下載。亦可在 [Aspose 下載頁面](https://releases.aspose.com/) 探索其他 Aspose 產品。
- 開發環境，例如 Visual Studio 2022 或更新版本。

## 如何使用 Aspose.CAD 為 DWG 加入影像？

載入目標 DWG，建立描述欲嵌入圖片的點陣圖物件，設定插入點與縮放向量，然後將影像附加至圖面。最後，儲存已修改的 DWG 或直接匯出為 PDF。整個工作流程僅需少量 API 呼叫，對於一般的 2 頁圖紙，執行時間不到一秒。

### 匯入命名空間
加入您將需要的 CAD 類別所在的命名空間。

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

### 步驟 1：設定文件目錄
準備包含來源 DWG 與欲嵌入影像的資料夾。

```csharp
string MyDir = "Your Document Directory";
```

### 步驟 2：載入 DWG 檔案
`CadImage` 類別代表 DWG 繪圖，並提供對其實體、圖層與中繼資料的存取。

```csharp
string dwgPathToFile = MyDir + "Drawing11.dwg";
CadImage cadImage1 = (CadImage)Image.Load(dwgPathToFile);
```

### 步驟 3：定義影像屬性
建立指向點陣檔案（例如 PNG）的 `Image` 物件，並指定其格式。

```csharp
CadRasterImageDef cadRasterImageDef = new CadRasterImageDef("road-sign-custom.png", 640, 562);
cadRasterImageDef.ObjectHandle = "A3B4";
```

### 步驟 4：設定 DWG 插入點與向量
指定影像在圖面中的顯示位置與縮放方式。插入點以 2 維座標定義，向量則控制寬度與高度。

```csharp
Cad3DPoint insertionPoint = new Cad3DPoint(26.77, 22.35);
Cad3DPoint uVector = new Cad3DPoint(0.0061565450840500831, 0);
Cad3DPoint vVector = new Cad3DPoint(0, 0.0061565450840500822);
```

### 步驟 5：建立並設定點陣影像
實例化 `RasterImage` 物件，指派影像資料，並設定其他渲染選項。

```csharp
CadRasterImage cadRasterImage = new CadRasterImage(cadRasterImageDef, insertionPoint, uVector, vVector);
cadRasterImage.ImageDefReference = "A3B4";
cadRasterImage.DisplayFlags = 7;
cadRasterImage.ClippingState = 0;
cadRasterImage.ClipBoundaryVertexList.Add(new Cad2DPoint(-0.5, 0.5));
cadRasterImage.ClipBoundaryVertexList.Add(new Cad2DPoint(639.5, 561.5));
```

### 步驟 6：將影像加入 DWG 檔案
將已設定好的點陣影像插入 DWG 的實體集合，使其成為圖面的一部份。

```csharp
CadImage cadImage = (CadImage)cadImage1;
cadImage.BlockEntities["*Model_Space"].AddEntity(cadRasterImage);

List<CadBaseObject> list = new List<CadBaseObject>(cadImage.Objects);
list.Add(cadRasterImageDef);
cadImage.Objects = list.ToArray();
```

### 步驟 7：另存為 PDF（將 DWG 匯出為 PDF）
在嵌入影像後，您可以使用單一呼叫 **convert dwg to pdf** 或 **save dwg as pdf**。此功能方便將圖面分享給沒有 CAD 軟體的相關人員。

```csharp
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.VectorRasterizationOptions = cadRasterizationOptions;
cadRasterizationOptions.DrawType = CadDrawTypeMode.UseObjectColor;

cadRasterizationOptions.PageHeight = 1600;
cadRasterizationOptions.PageWidth = 1600;
cadRasterizationOptions.Layouts = new string[] { "Model" };
cadImage1.Save(MyDir + "export2.pdf", pdfOptions);
```

## 如何在嵌入影像後將 DWG 轉換為 PDF？

呼叫 `CadImage` 實例的 `Save` 方法，傳入 `SaveFormat.Pdf`，並可選擇 `PdfOptions` 物件以控制頁面大小、點陣化與中繼資料。Aspose.CAD 會保留嵌入的點陣影像、圖層與線寬，產生可在任何檢視器開啟的忠實 PDF 表現。此轉換僅需一行程式碼即可完成。

## 常見問題與解決方案
- **影像出現在錯誤位置** – 請再次確認插入點座標與方向向量；它們是相對於圖面的原點。
- **大型影像導致記憶體激增** – 在插入前使用點陣影像的 `Resize` 選項，或使用較低解析度的副本。
- **PDF 匯出失去向量品質** – 確保使用能保留向量資料的 `PdfOptions` 進行儲存；點陣影像會如實嵌入。

## 常見問答

**Q: 我可以在其他程式語言中使用 Aspose.CAD for .NET 嗎？**  
A: 核心函式庫是 .NET 專屬，但 Aspose 為 Java、Python 及其他平台提供等效的 API。

**Q: Aspose.CAD 有提供免費試用嗎？**  
A: 是的，您可在 [Aspose 免費試用頁面](https://releases.aspose.com/) 探索免費試用。

**Q: 我在哪裡可以找到 Aspose.CAD 的詳細文件？**  
A: 文件可於 [Aspose.CAD .NET API 參考文件](https://reference.aspose.com/cad/net/) 取得。

**Q: 我該如何取得 Aspose.CAD 的臨時授權？**  
A: 請前往 [臨時授權頁面](https://purchase.aspose.com/temporary-license/) 取得臨時授權。

**Q: 是否有 Aspose.CAD 社群論壇可供支援？**  
A: 是的，您可在 [Aspose.CAD 社群論壇](https://forum.aspose.com/c/cad/19) 尋求支援並與社群互動。

---

**最後更新：** 2026-08-17  
**測試版本：** Aspose.CAD 24.11 for .NET  
**作者：** Aspose

## 相關教學

- [將 DWG 匯出為 PDF 或點陣圖像 - Aspose.CAD 指南](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)
- [將 DWG 匯出為 DXF 格式（C#） - Aspose.CAD 教學](/cad/net/advanced-export-techniques/exporting-dwg-to-dxf/)
- [將特定版面匯出為 PDF - Aspose.CAD 指南](/cad/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}