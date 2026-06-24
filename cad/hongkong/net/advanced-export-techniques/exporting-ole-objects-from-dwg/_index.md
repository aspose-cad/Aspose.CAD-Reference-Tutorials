---
description: 學習如何使用 Aspose.CAD for .NET 將 DWG 轉換為 PNG，並從 DWG 檔案中提取 OLE 物件——快速、以程式碼為主的指南。
linktitle: Exporting OLE Objects from DWG Files
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: 將 DWG 轉換為 PNG 並匯出 OLE 物件 - Aspose.CAD 教學
url: /zh-hant/net/advanced-export-techniques/exporting-ole-objects-from-dwg/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 從 DWG 檔案匯出 OLE 物件 - Aspose.CAD 教程

## Introduction

如果您需要在 **convert DWG to PNG** 的同時抽取內嵌的 OLE 物件，您來對地方了。Aspose.CAD for .NET 讓這兩步驟的流程變得簡單，只需幾行 C# 程式碼即可自動化抽取與光柵化。接下來的幾分鐘，我們將從環境設定一路走到將每個 DWG 儲存為包含抽取後 OLE 資料的 PNG。

## Quick Answers
- **What does this tutorial cover?** Converting DWG to PNG and extracting OLE objects using Aspose.CAD for .NET.  
- **Do I need a license?** A free trial works for development; a commercial license is required for production.  
- **Which .NET versions are supported?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Can I process multiple DWG files at once?** Yes – the sample loops through an array of file names.  
- **Where can I find more examples?** Check the official Aspose.CAD documentation and forum links below.

## What is **convert DWG to PNG**?
將 DWG（AutoCAD 繪圖）轉換為 PNG 圖像會將向量資料光柵化，讓它更容易在網頁、報告或其他不原生支援 DWG 的應用程式中檢視或嵌入。若檔案中包含 OLE 物件，轉換過程中即可將它們抽取並另存為獨立資產。

## Why extract OLE objects from CAD files?
許多 DWG 繪圖會將試算表、圖表或其他 Office 文件以 OLE 物件形式嵌入。抽取這些物件可讓您重新使用原始資料、自動化報表，或在不遺失嵌入資訊的情況下遷移至新格式。

## Prerequisites

- Aspose.CAD for .NET Library: Make sure you have the library installed. You can download it from the [Aspose.CAD for .NET download page](https://releases.aspose.com/cad/net/).
- Document Directory: Set up a directory where your DWG files are stored. Replace `"Your Document Directory"` in the provided code snippet with the actual path.

## Import Namespaces

In your .NET project, import the required namespaces:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Step‑by‑Step Guide

### Step 1: Set the Document Directory

```csharp
string MyDir = "Your Document Directory";
```

Replace `"Your Document Directory"` with the path where your DWG files are located.

### Step 2: List the DWG files you want to process

```csharp
string[] files = new string[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

### Step 3: Configure export options for PNG conversion

```csharp
PngOptions pngOptions = new PngOptions { };
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.VectorRasterizationOptions = rasterizationOptions;
rasterizationOptions.Layouts = new string[] { "Layout1" };
```

You can tweak `CadRasterizationOptions` (e.g., `PageWidth`, `PageHeight`, `BackgroundColor`) to match your desired output resolution.

### Step 4: Iterate through each DWG and perform the conversion

```csharp
foreach (string file in files)
{
    using (CadImage cadImage = (CadImage)Image.Load(MyDir + file))
    {
        cadImage.Save(MyDir + file + "_out.png", pngOptions);
    }
}
```

During this loop the library automatically **extracts OLE objects** embedded in each drawing and includes them in the generated PNG. If you need the raw OLE streams, you can access `cadImage.OleObjects` collection – a handy way to **how to extract ole** data programmatically.

## Common Issues & Troubleshooting

- **Missing layout name** – Ensure the layout you specify (`"Layout1"` in the example) exists in the source DWG; otherwise the rasterizer falls back to the default model space.
- **Large files cause memory pressure** – Process files one at a time (as shown) and dispose of `CadImage` objects promptly with `using`.
- **Unexpected colors** – Set `rasterizationOptions.BackgroundColor` to match the drawing’s background if transparency is required.

## Frequently Asked Questions

### Q1: Is Aspose.CAD for .NET suitable for both junior and senior CAD files?
A1: Yes, Aspose.CAD for .NET is versatile and can handle a wide range of CAD files, including both junior and senior variants.

### Q2: Can I customize export options for different layouts?
A2: Absolutely! As shown in the tutorial, you can tailor export options, including layouts, to suit your specific needs.

### Q3: Where can I find detailed documentation for Aspose.CAD for .NET?
A3: Explore the [Aspose.CAD for .NET documentation](https://reference.aspose.com/cad/net/) for in‑depth information and examples.

### Q4: Is there a free trial available?
A4: Yes, you can experience the capabilities of Aspose.CAD for .NET with a free trial. Visit [this link](https://releases.aspose.com/) to get started.

### Q5: How can I get support or connect with the community?
A5: For support and community engagement, visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19).

### Q6: How do I **extract OLE from CAD** files without converting to PNG?
A6: Use the `CadImage.OleObjects` collection after loading the DWG; you can iterate through each `OleObject` and save its raw data to a file.

## Conclusion

You’ve now seen how to **convert DWG to PNG** while seamlessly **extracting OLE objects** using Aspose.CAD for .NET. This approach saves time, eliminates manual copy‑paste steps, and integrates cleanly into automated pipelines. Feel free to experiment with other raster formats (JPEG, BMP) or explore the rich set of CAD manipulation features Aspose offers.

---

**Last Updated:** 2026-03-13  
**Tested With:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}