---
date: 2026-03-21
description: Aspose.CAD for .NET kullanarak DWG'den PDF oluşturmayı ve DWG içinde
  DGN'yi dışa aktarmayı öğrenin. Bu rehber ayrıca DWG'yi PDF'ye dönüştürmeyi ve PDF
  seçeneklerini ayarlamayı gösterir.
linktitle: Export DGN as Part of DWG
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: DWG'den PDF Oluştur ve DGN'yi DWG'nin Bir Parçası Olarak Dışa Aktar – Aspose.CAD
  for .NET
url: /tr/net/cad-export-formats/export-dgn-as-part-of-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG'den PDF Oluşturma ve DGN'yi DWG'nin Bir Parçası Olarak Dışa Aktarma – Aspose.CAD for .NET

## Introduction

Eğer **DWG'den PDF oluşturma** işlemini yaparken aynı zamanda bir DGN tasarımını DWG'nin bir parçası olarak gömmek istiyorsanız, Aspose.CAD for .NET bu süreci oldukça basitleştirir. Bu öğreticide tüm iş akışını adım adım inceleyeceğiz: bir DWG dosyasını yükleme, gömülü DGN alt katmanını bulma, rasterleştirme seçeneklerini yapılandırma ve sonunda sonucu bir PDF belgesine dışa aktarma. İster toplu dönüşüm aracı, ister raporlama motoru, ister CAD‑BIM entegrasyon servisi geliştirin, aşağıdaki adımlar size sağlam ve üretime hazır bir temel sağlayacak.

## Quick Answers
- **DWG → PDF dönüşümünü hangi kütüphane yönetir?** Aspose.CAD for .NET  
- **PDF oluştururken bir DGN alt katmanı dışa aktarabilir miyim?** Yes – the underlay is accessed via `CadDgnUnderlay`.  
- **PDF seçeneklerini hangi yöntem ayarlar?** `PdfOptions` together with `CadRasterizationOptions`.  
- **Ticari kullanım için lisansa ihtiyacım var mı?** Yes, a valid Aspose.CAD license is required.  
- **Desteklenen .NET sürümleri?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## What is “create PDF from DWG”?

DWG dosyasından PDF oluşturmak, vektör çizimini raster ya da vektör‑tabanlı bir PDF belgesine dönüştürmek anlamına gelir. Bu süreç, CAD yazılımı olmayan paydaşlarla çizimleri paylaşmak, arşivlemek veya yazdırılabilir raporlar üretmek için faydalıdır. Aspose.CAD, DWG varlıklarını ayrıştırma ve `PdfOptions` aracılığıyla çıktıyı ince ayarlarla kontrol etme işini üstlenerek görevi basitleştirir.

## Why export DGN as part of a DWG?

Bir DGN alt katmanı genellikle MicroStation projelerinden referans geometrisini temsil eder. DGN'yi DWG ile birlikte dışa aktararak orijinal tasarım bağlamını korur ve downstream kullanıcıların tam çizim setini görmesini sağlarsınız. Bu, DWG ve DGN dosyalarının birlikte bulunduğu çok disiplinli projelerde özellikle değerlidir.

## Prerequisites

- **Aspose.CAD for .NET** – download it [here](https://releases.aspose.com/cad/net/).  
- **Development Environment** – Visual Studio (any recent version) or your preferred .NET IDE.  
- **Basic C# knowledge** – you should be comfortable with C# syntax and .NET project structure.

## Import Namespaces

Add the required `using` directives at the top of your C# source file:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Step‑by‑Step Guide

### Step 1: Define File Paths

Set the input DWG file and the output PDF name.

```csharp
// Input and Output file paths
string fileName = "BlockRefDgn.dwg";
string outPath = fileName + ".pdf";
```

### Step 2: Create `PdfOptions` Instance (set pdf options)

`PdfOptions` lets you control how the PDF is generated, such as page size, compression, and metadata.

```csharp
// Create an instance of PdfOptions class for exporting DWG to PDF
PdfOptions exportOptions = new PdfOptions();
```

### Step 3: Load the DWG File

Load the DWG as a `CadImage` so you can inspect its entities.

```csharp
// Load the existing DWG file as an image and convert it to CadImage type
using (CadImage cadImage = (CadImage)Image.Load(fileName))
```

### Step 4: Iterate Through Entities

Walk through every entity in the drawing to locate the DGN underlay.

```csharp
// Iterate through each entity inside the DWG file
foreach (CadBaseEntity baseEntity in cadImage.Entities)
```

### Step 5: Check Entity Type (how to export dgn)

Identify whether the current entity is a DGN underlay.

```csharp
// Check if the entity is an image definition
if (baseEntity.TypeName == CadEntityTypeName.DGNUNDERLAY)
```

### Step 6: Get Underlay Path

Retrieve the external reference path of the DGN file.

```csharp
// If it's an image definition, get the external reference to the object
CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
Console.WriteLine(dgnFile.UnderlayPath);
```

### Step 7: Define Rasterization Options (convert dwg to pdf)

Configure how the DWG is rasterized before being placed into the PDF.

```csharp
// Define settings for CadRasterizationOptions object
exportOptions.VectorRasterizationOptions = new CadRasterizationOptions()
{
    PageWidth = 1600,
    PageHeight = 1600,
    Layouts = new string[] { "Model" },
    AutomaticLayoutsScaling = false,
    NoScaling = true,
    BackgroundColor = Color.Black,
    DrawType = CadDrawTypeMode.UseObjectColor
};
```

### Step 8: Export DWG to PDF

Finally, save the rendered image as a PDF file.

```csharp
// Export the DWG to PDF by calling Save method
cadImage.Save(outPath, exportOptions);
```

## Common Issues and Solutions

| Issue | Reason | Fix |
|-------|--------|-----|
| **`Image.Load` throws “File not found”** | Incorrect path or missing file. | Use an absolute path or ensure the DWG is copied to the output folder. |
| **Underlay path is empty** | DGN underlay not embedded or reference broken. | Verify the DWG actually contains a DGN underlay and that the external DGN file is accessible. |
| **PDF output is blank** | Rasterization options set to zero size. | Adjust `PageWidth`/`PageHeight` or set `NoScaling = false`. |
| **License exception** | Running without a valid Aspose.CAD license. | Apply the license before loading the image: `License lic = new License(); lic.SetLicense("Aspose.CAD.lic");` |

## Frequently Asked Questions

### Q1: Can I use Aspose.CAD for .NET in my commercial projects?
A1: Yes, you can. Visit [here](https://purchase.aspose.com/buy) to explore licensing options.

### Q2: Are there any limitations on the size of DWG files I can process?
A2: Aspose.CAD supports handling large DWG files, but hardware limitations may apply.

### Q3: Is there a trial version available?
A3: Yes, you can get a free trial [here](https://releases.aspose.com/).

### Q4: How can I get temporary licenses?
A4: Temporary licenses can be obtained [here](https://purchase.aspose.com/temporary-license/).

### Q5: Where can I seek assistance if I encounter issues?
A5: You can visit the Aspose.CAD forum [here](https://forum.aspose.com/c/cad/19) for support.

**Q: How do I set additional PDF metadata (author, title, etc.)?**  
A: Use `exportOptions.Metadata` properties before calling `Save`.

**Q: Can I export multiple layouts into separate PDF pages?**  
A: Yes – set `Layouts = new string[] { "Layout1", "Layout2" }` in `CadRasterizationOptions`.

**Q: Does Aspose.CAD support converting DWG to other image formats?**  
A: Absolutely. You can export to PNG, JPEG, SVG, and more by using the corresponding `Image.Save` overloads.

---

**Last Updated:** 2026-03-21  
**Tested With:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}