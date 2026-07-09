---
date: 2026-07-09
description: Naučte se, jak převést IGES do PDF pomocí Aspose.CAD pro .NET. Postupujte
  podle tohoto krok‑za‑krokem průvodce a exportujte soubory IGES do PDF rychle a přesně.
keywords:
- convert iges to pdf
- export iges as pdf
- create pdf from iges
- convert cad file to pdf
- generate pdf from cad
lastmod: 2026-07-09
linktitle: Export souborů IGES do PDF
og_description: Převod IGES do PDF pomocí Aspose.CAD pro .NET. Tento tutoriál ukazuje,
  jak efektivně exportovat soubory IGES do PDF bez psaní kódu.
og_image_alt: Guide showing conversion of IGES files to PDF with Aspose.CAD in .NET
og_title: Převod IGES do PDF – Rychlý průvodce Aspose.CAD
schemas:
- author: Aspose
  dateModified: '2026-07-09'
  description: Learn how to convert IGES to PDF using Aspose.CAD for .NET. Follow
    this step‑by‑step guide to export IGES files as PDF quickly and accurately.
  headline: Convert IGES to PDF with Aspose.CAD – Quick Guide
  type: TechArticle
- description: Learn how to convert IGES to PDF using Aspose.CAD for .NET. Follow
    this step‑by‑step guide to export IGES files as PDF quickly and accurately.
  name: Convert IGES to PDF with Aspose.CAD – Quick Guide
  steps:
  - name: Set up Your Project
    text: Create a new .NET console or class‑library project, or open an existing
      one where you want to add the conversion feature.
  - name: Add Aspose.CAD Reference
    text: Add the downloaded Aspose.CAD DLL to your project references. In Visual
      Studio, right‑click **References → Add Reference → Browse** and select the DLL.
  - name: Initialize the Path
    text: Define the folder that contains your IGES file and the output location.
  - name: Load the CAD Image
    text: '`Image.Load` reads the IGES file and creates an in‑memory representation.
      The `Image` class is Aspose.CAD''s primary entry point for any CAD format.'
  - name: Configure Rasterization Options
    text: '`PdfOptions` (derived from `CadRasterizationOptions`) lets you set page
      size, resolution, and vector‑preserving flags. The `PdfOptions` class defines
      how the CAD drawing is rasterized and saved as PDF.'
  - name: Save as PDF
    text: Finally, write the PDF file to disk. With these six straightforward steps,
      you have successfully **convert iges to pdf** using Aspose.CAD for .NET.
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD works in ASP.NET, ASP.NET Core, and other web frameworks,
      providing server‑side conversion without UI dependencies.
    question: Can I use Aspose.CAD for .NET in a web application?
  - answer: Explore the comprehensive documentation [here](https://reference.aspose.com/cad/net/)
      for detailed insights into all supported features.
    question: Where can I find additional documentation for Aspose.CAD?
  - answer: Yes, you can access a free trial [here](https://releases.aspose.com/)
      to evaluate the library before purchasing.
    question: Is there a free trial available?
  - answer: For temporary licenses, visit [this link](https://purchase.aspose.com/temporary-license/)
      to get the required licensing information.
    question: How can I obtain a temporary license?
  - answer: Join the Aspose.CAD community on the [support forum](https://forum.aspose.com/c/cad/19)
      for prompt help and discussions.
    question: Need assistance or have questions?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- convert iges to pdf
- Aspose.CAD
- .NET CAD conversion
title: Převod IGES do PDF pomocí Aspose.CAD – Rychlý průvodce
url: /cs/net/exporting-to-image-formats/exporting-iges-files-to-pdf/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Převod IGES na PDF pomocí Aspose.CAD

## Úvod

Ve rychle se rozvíjejícím světě počítačově podporovaného návrhu je **convert IGES to PDF** rutinní úkol, který inženýři a architekti provádějí denně. Ať už potřebujete tisknutelný dokument pro revizi klienta nebo lehký archiv pro správu verzí, exportování souborů IGES do PDF zachovává původní geometrii a zároveň činí soubor univerzálně přístupným. Tento tutoriál vás provede přesné kroky převodu IGES na PDF pomocí Aspose.CAD pro .NET, abyste mohli proces automatizovat v jakékoli .NET aplikaci.

## Rychlé odpovědi
- **Jaká knihovna provádí převod?** Aspose.CAD for .NET.
- **Kolik řádků kódu je potřeba?** Obvykle dva řádky: načíst IGES soubor a zavolat `Save`.
- **Mohu ovládat velikost stránky a kvalitu?** Ano, pomocí `CadRasterizationOptions`.
- **Je pro produkci potřeba licence?** Komerční licence je vyžadována; k dispozici je bezplatná zkušební verze. Dočasnou licenci můžete získat [this link](https://purchase.aspose.com/temporary-license/).
- **Které verze .NET jsou podporovány?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## Co je “convert IGES to PDF”?
*Converting IGES to PDF* znamená převzít neutrální CAD výměnný soubor (IGES) a vykreslit jej jako Portable Document Format (PDF), který lze otevřít na jakémkoli zařízení bez CAD softwaru. Převod zachovává vektorovou geometrii, vrstvy a anotace a zároveň je zploští do dokumentu s pevně daným rozložením.

## Proč použít Aspose.CAD pro tento převod?
Aspose.CAD podporuje **30+ CAD a BIM formátů** a může zpracovávat soubory až do **2 GB** bez načítání celého dokumentu do paměti, což poskytuje rychlý server‑side převod bez jakýchkoli třetích závislostí. Tento kvantifikovatelný výkon jej činí ideálním pro dávkové zpracování a cloud‑based služby.

## Předpoklady

Před zahájením se ujistěte, že máte následující:

1. **Aspose.CAD for .NET Library** – stáhněte ji z [here](https://releases.aspose.com/cad/net/). API referenci můžete také zobrazit [here](https://reference.aspose.com/cad/net/).  
2. **.NET vývojové prostředí** – Visual Studio, Rider nebo jakékoli IDE, které podporuje .NET 5+.

Nyní, když jsou předpoklady splněny, importujme jmenné prostory potřebné pro převod.

## Importovat jmenné prostory

Třída `Image` je hlavní třída představující CAD výkres v paměti. `CadRasterizationOptions` definuje, jak je CAD výkres rasterizován pro vektorový výstup. Třída `PdfOptions` určuje nastavení výstupu pro PDF soubory.

``` 
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
```

Tyto jmenné prostory poskytují základní funkčnost pro načítání, rasterizaci a ukládání CAD výkresů.

## Jak převést IGES na PDF pomocí Aspose.CAD?

Načtěte IGES soubor pomocí `Image.Load` a okamžitě zavolejte `Save` s možností rasterizace PDF – to je kompletní převod ve dvou příkazech. Knihovna automaticky zajišťuje vektorové vykreslování, vkládání fontů a škálování stránek, takže získáte věrnou PDF repliku původního IGES modelu.

### Krok 1: Nastavte svůj projekt

Vytvořte nový .NET konzolový nebo knihovní projekt, nebo otevřete existující, do kterého chcete přidat funkci převodu.

### Krok 2: Přidejte odkaz na Aspose.CAD

Přidejte stažený Aspose.CAD DLL do referencí projektu. Ve Visual Studio klikněte pravým tlačítkem **References → Add Reference → Browse** a vyberte DLL.

### Krok 3: Inicializujte cestu

Definujte složku, která obsahuje váš IGES soubor, a výstupní umístění.

``` 
string sourceDir = @"C:\CAD\Source";
string outputDir = @"C:\CAD\Output";
string igesFile = Path.Combine(sourceDir, "sample.iges");
string pdfFile = Path.Combine(outputDir, "sample.pdf");
```

### Krok 4: Načtěte CAD obrázek

`Image.Load` načte IGES soubor a vytvoří jeho reprezentaci v paměti.

``` 
Image cadImage = Image.Load(igesFile);
```

Třída `Image` je hlavním vstupním bodem Aspose.CAD pro jakýkoli CAD formát.

### Krok 5: Nakonfigurujte možnosti rasterizace

`PdfOptions` (odvozené od `CadRasterizationOptions`) vám umožňuje nastavit velikost stránky, rozlišení a příznaky zachování vektorů.

``` 
PdfOptions pdfOptions = new PdfOptions
{
    VectorRasterizationOptions = new CadRasterizationOptions
    {
        PageWidth = 842,      // A4 width in points
        PageHeight = 595,     // A4 height in points
        Resolution = 300      // 300 DPI for high‑quality output
    }
};
```

Třída `PdfOptions` určuje, jak je CAD výkres rasterizován a uložen jako PDF.

### Krok 6: Uložte jako PDF

Nakonec zapište PDF soubor na disk.

``` 
cadImage.Save(pdfFile, pdfOptions);
```

S těmito šesti jednoduchými kroky jste úspěšně **convert iges to pdf** pomocí Aspose.CAD pro .NET.

## Časté úskalí a tipy

- **Velké soubory:** Zvyšte `Resolution` pouze pokud potřebujete detailnější výstup; vyšší DPI spotřebuje více paměti.  
- **Chybějící fonty:** Ujistěte se, že všechny vlastní fonty použité v IGES souboru jsou nainstalovány na serveru; jinak budou nahrazeny.  
- **Dávkový převod:** Zabalte logiku načtení‑uložení do smyčky `foreach` pro automatické zpracování více IGES souborů.

## Často kladené otázky

**Q: Mohu použít Aspose.CAD pro .NET ve webové aplikaci?**  
A: Ano, Aspose.CAD funguje v ASP.NET, ASP.NET Core a dalších webových frameworkech, poskytuje server‑side převod bez UI závislostí.

**Q: Kde mohu najít další dokumentaci pro Aspose.CAD?**  
A: Prozkoumejte komplexní dokumentaci [here](https://reference.aspose.com/cad/net/) pro podrobné informace o všech podporovaných funkcích.

**Q: Je k dispozici bezplatná zkušební verze?**  
A: Ano, můžete získat bezplatnou zkušební verzi [here](https://releases.aspose.com/) pro vyzkoušení knihovny před zakoupením.

**Q: Jak mohu získat dočasnou licenci?**  
A: Pro dočasné licence navštivte [this link](https://purchase.aspose.com/temporary-license/) pro získání potřebných licenčních informací.

**Q: Potřebujete pomoc nebo máte otázky?**  
A: Připojte se ke komunitě Aspose.CAD na [support forum](https://forum.aspose.com/c/cad/19) pro rychlou pomoc a diskusi.

---

**Last Updated:** 2026-07-09  
**Tested With:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using static Aspose.CAD.Examples.CSharp.DWG_Drawings.SupportMLeaderEntityForDWGFormat;
using Aspose.CAD.ImageOptions;
```

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "figa2.igs";
```

```csharp
using (Image cadImage = Image.Load(sourceFilePath))
{
    // Your code goes here
}
```

```csharp
CadRasterizationOptions options = new CadRasterizationOptions
{
    PageHeight = 1000,
    PageWidth = 1000,
};

PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = options;
```

```csharp
cadImage.Save(MyDir + "figa2.pdf", pdfOptions);
```

Pro další zdroje viz hlavní stránku vydání [here](https://releases.aspose.com/). Pokud potřebujete pomoc, navštivte [support forum](https://forum.aspose.com/c/cad/19).

## Související tutoriály

- [Export DWG do PDF nebo rastrových obrázků – průvodce Aspose.CAD](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)
- [Export DXF do PDF formátu – tutoriál Aspose.CAD](/cad/net/export-techniques/exporting-dxf-to-pdf-format/)
- [Export DGN do PDF v Aspose.CAD pro .NET](/cad/net/cad-export-formats/export-dgn-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}