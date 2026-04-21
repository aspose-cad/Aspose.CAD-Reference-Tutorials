---
date: 2026-03-29
description: Naučte se, jak vytvořit PDF z CAD, nastavit velikost plátna a exportovat
  CAD do PDF nebo TIFF pomocí Aspose.CAD pro .NET v tomto krok‑za‑krokem průvodci.
linktitle: Setting Canvas Size and Mode
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: 'Jak vytvořit PDF z CAD: nastavte velikost plátna a režim v Aspose.CAD pro
  .NET'
url: /cs/net/cad-features-and-support/setting-canvas-size-and-mode/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Nastavení velikosti plátna a režimu v Aspose.CAD pro .NET

## Úvod

Připraveni **vytvořit PDF z CAD** souborů při kontrole výstupních rozměrů? V tomto tutoriálu vás provedeme nastavením velikosti plátna a režimu, načtením CAD souboru a exportem do PDF nebo TIFF pomocí Aspose.CAD pro .NET. Ať už potřebujete **převést DXF na PDF**, generovat vysoce rozlišené výkresy, nebo jen upravit oblast rasterizace, níže uvedené kroky vám poskytnou solidní, připravené řešení pro produkci.

## Rychlé odpovědi
- **Co znamená “create PDF from CAD”?** Převod CAD výkresu (např. DXF, DWG) do PDF dokumentu, který zachovává vektorové i rastrové detaily.  
- **Která volba řídí velikost výstupu?** `CadRasterizationOptions.PageWidth` a `PageHeight` (velikost plátna).  
- **Mohu také exportovat do TIFF?** Ano – použijte `TiffOptions` se stejnými nastaveními rasterizace.  
- **Potřebuji licenci pro produkci?** Vyžaduje se komerční licence; k dispozici je bezplatná zkušební verze.  
- **Podporované verze .NET?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## Co je “create PDF from CAD”?
Vytvoření PDF z CAD znamená renderování CAD výkresu do formátu orientovaného na stránku (PDF), který lze zobrazit, vytisknout nebo sdílet bez nutnosti CAD softwaru. Aspose.CAD provádí těžkou práci a umožňuje vám definovat velikost plátna, měřítko a výstupní formát.

## Proč nastavit velikost plátna při vytváření PDF z CAD?
Nastavení velikosti plátna vám dává přesnou kontrolu nad rozlišením a rozměry výsledného PDF nebo TIFF. To je zvláště užitečné, když:
- Připravujete výkresy k tisku na konkrétní formáty papíru.  
- Generujete miniatury nebo vysoce rozlišené obrázky pro náhled na webu.  
- Zajišťujete konzistentní rozvržení napříč více dokumenty.

## Požadavky

- Aspose.CAD Library: Download and install the Aspose.CAD library from the [Aspose.CAD website](https://releases.aspose.com/cad/net/).
- Development Environment: Ensure you have a .NET development environment set up on your machine.
- Sample CAD File: For this tutorial, we'll use a sample DXF file. You can find one in the [Aspose.CAD documentation](https://reference.aspose.com/cad/net/).

## Importovat jmenné prostory

First, import the namespaces required for CAD processing:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Jak vytvořit PDF z CAD s vlastním rozměrem plátna

### Krok 1: Načíst CAD soubor

We start by **loading the CAD file** (e.g., a DXF) into an `Image` object. This is the point where you **load CAD file** into memory.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (Image image = Image.Load(sourceFilePath))
{
    // Your code for further steps will go here
}
```

### Krok 2: Vytvořit CadRasterizationOptions

Create a `CadRasterizationOptions` instance and define the canvas size. The `PageWidth` and `PageHeight` properties let you **set canvas size** to the exact dimensions you need.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.AutomaticLayoutsScaling = true;
rasterizationOptions.NoScaling = false;
```

### Krok 3: Vytvořit PdfOptions (Export CAD do PDF)

Link the rasterization settings to a `PdfOptions` object. This configuration enables you to **export CAD to PDF** with the custom canvas you defined.

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

### Krok 4: Export do PDF (Převod DXF na PDF)

Now save the image as a PDF. This step **creates PDF from CAD** using the options we set.

```csharp
image.Save(MyDir + "result_out.pdf", pdfOptions);
```

### Krok 5: Vytvořit TiffOptions (Export CAD do TIFF)

If you also need a raster image, configure `TiffOptions`. The same rasterization options are reused, so the **export CAD to TIFF** respects the canvas size.

```csharp
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.VectorRasterizationOptions = rasterizationOptions;
```

### Krok 6: Export do TIFF

Finally, save the drawing as a TIFF file.

```csharp
image.Save(MyDir + "result_out.tiff", tiffOptions);
```

## Časté problémy a řešení

- **Canvas appears cropped** – Verify that `AutomaticLayoutsScaling` is set to `true` and `NoScaling` is `false` so the drawing scales to fit the canvas.  
- **Low‑resolution PDF** – Increase `PageWidth`/`PageHeight` or set `Resolution` on `CadRasterizationOptions`.  
- **File not found error** – Ensure `MyDir` points to a valid directory and the DXF file name matches exactly.

## Často kladené otázky

### Q1: Mohu použít Aspose.CAD s jinými .NET knihovnami?
A1: Yes, Aspose.CAD seamlessly integrates with other .NET libraries, providing enhanced capabilities for CAD manipulation.

### Q2: Je k dispozici bezplatná zkušební verze Aspose.CAD?
A2: Yes, you can explore the features of Aspose.CAD with a free trial. Visit [here](https://releases.aspose.com/) to get started.

### Q3: Jak mohu získat podporu pro Aspose.CAD?
A3: For support and discussions, visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19).

### Q4: Kde najdu komplexní dokumentaci pro Aspose.CAD?
A4: Refer to the [Aspose.CAD documentation](https://reference.aspose.com/cad/net/) for detailed information and examples.

### Q5: Jak si mohu zakoupit Aspose.CAD pro .NET?
A5: To purchase Aspose.CAD, visit the [purchase page](https://purchase.aspose.com/buy).

**Additional Q&A**

**Q: Can I export a multi‑page CAD drawing to a single PDF?**  
A: Yes. Set `PageCount` in `CadRasterizationOptions` and the library will concatenate pages into one PDF.

**Q: Does the canvas size affect vector data quality?**  
A: Vector data remains resolution‑independent; the canvas size only influences rasterized elements and image resolution.

---

**Last Updated:** 2026-03-29  
**Tested With:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}