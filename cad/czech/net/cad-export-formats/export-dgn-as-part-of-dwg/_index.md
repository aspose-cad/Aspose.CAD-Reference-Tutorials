---
date: 2026-03-21
description: Naučte se, jak vytvořit PDF z DWG a exportovat DGN jako součást DWG pomocí
  Aspose.CAD pro .NET. Tento průvodce také ukazuje, jak převést DWG na PDF a nastavit
  možnosti PDF.
linktitle: Export DGN as Part of DWG
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Vytvořte PDF z DWG a exportujte DGN jako součást DWG – Aspose.CAD pro .NET
url: /cs/net/cad-export-formats/export-dgn-as-part-of-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Vytvoření PDF z DWG a export DGN jako součást DWG – Aspose.CAD pro .NET

## Úvod

Pokud potřebujete **vytvořit PDF ze souborů DWG** a zároveň vložit návrh DGN jako součást DWG, Aspose.CAD pro .NET to činí jednoduchým. V tomto tutoriálu projdeme celý pracovní postup: načtení DWG, vyhledání vloženého DGN podkladu, nastavení možností rasterizace a nakonec export výsledku do PDF dokumentu. Ať už vytváříte nástroj pro hromadnou konverzi, reportingový engine nebo službu pro integraci CAD‑BIM, níže uvedené kroky vám poskytnou pevný, produkčně připravený základ.

## Rychlé odpovědi
- **Která knihovna provádí konverzi DWG → PDF?** Aspose.CAD pro .NET  
- **Mohu exportovat DGN podklad při vytváření PDF?** Ano – podklad je přístupný přes `CadDgnUnderlay`.  
- **Která metoda nastavuje možnosti PDF?** `PdfOptions` spolu s `CadRasterizationOptions`.  
- **Potřebuji licenci pro komerční použití?** Ano, je vyžadována platná licence Aspose.CAD.  
- **Podporované verze .NET?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## Co znamená „vytvořit PDF z DWG“?

Vytvoření PDF ze souboru DWG znamená vykreslení vektorového výkresu do rastrového nebo vektorového PDF dokumentu. Tento proces je užitečný pro sdílení výkresů se stranami, které nemají CAD software, archivaci nebo generování tisknutelných zpráv. Aspose.CAD zjednodušuje úlohu tím, že se postará o těžkou část parsování entit DWG a poskytuje jemnou kontrolu nad výstupem pomocí `PdfOptions`.

## Proč exportovat DGN jako součást DWG?

DGN podklad často představuje referenční geometrii z projektů MicroStation. Exportem DGN spolu s DWG zachováte původní kontext návrhu, což zajišťuje, že koncoví uživatelé uvidí kompletní sadu výkresů. To je zvláště cenné v multidisciplinárních projektech, kde koexistují soubory DWG i DGN.

## Požadavky

- **Aspose.CAD pro .NET** – stáhněte si jej [zde](https://releases.aspose.com/cad/net/).  
- **Vývojové prostředí** – Visual Studio (jakákoli recentní verze) nebo vaše preferované .NET IDE.  
- **Základní znalost C#** – měli byste být obeznámeni se syntaxí C# a strukturou .NET projektu.

## Import jmenných prostorů

Přidejte požadované `using` direktivy na začátek vašeho C# souboru:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Průvodce krok za krokem

### Krok 1: Definujte cesty k souborům

Nastavte vstupní soubor DWG a název výstupního PDF.

```csharp
// Input and Output file paths
string fileName = "BlockRefDgn.dwg";
string outPath = fileName + ".pdf";
```

### Krok 2: Vytvořte instanci `PdfOptions` (nastavte možnosti PDF)

`PdfOptions` vám umožňuje řídit, jak je PDF generováno, např. velikost stránky, kompresi a metadata.

```csharp
// Create an instance of PdfOptions class for exporting DWG to PDF
PdfOptions exportOptions = new PdfOptions();
```

### Krok 3: Načtěte soubor DWG

Načtěte DWG jako `CadImage`, abyste mohli prozkoumat jeho entity.

```csharp
// Load the existing DWG file as an image and convert it to CadImage type
using (CadImage cadImage = (CadImage)Image.Load(fileName))
```

### Krok 4: Procházejte entity

Projděte každou entitu ve výkresu a najděte DGN podklad.

```csharp
// Iterate through each entity inside the DWG file
foreach (CadBaseEntity baseEntity in cadImage.Entities)
```

### Krok 5: Zkontrolujte typ entity (jak exportovat dgn)

Identifikujte, zda je aktuální entita DGN podklad.

```csharp
// Check if the entity is an image definition
if (baseEntity.TypeName == CadEntityTypeName.DGNUNDERLAY)
```

### Krok 6: Získejte cestu k podkladu

Získejte cestu k externímu referenčnímu souboru DGN.

```csharp
// If it's an image definition, get the external reference to the object
CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
Console.WriteLine(dgnFile.UnderlayPath);
```

### Krok 7: Definujte možnosti rasterizace (převod dwg na pdf)

Nastavte, jak bude DWG rasterizováno před vložením do PDF.

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

### Krok 8: Exportujte DWG do PDF

Nakonec uložte vykreslený obrázek jako PDF soubor.

```csharp
// Export the DWG to PDF by calling Save method
cadImage.Save(outPath, exportOptions);
```

## Časté problémy a řešení

| Problém | Důvod | Řešení |
|---------|-------|--------|
| **`Image.Load` vyhazuje „File not found“** | Nesprávná cesta nebo chybějící soubor. | Použijte absolutní cestu nebo zajistěte, aby byl DWG zkopírován do výstupní složky. |
| **Cesta k podkladu je prázdná** | DGN podklad není vložen nebo je odkaz poškozen. | Ověřte, že DWG skutečně obsahuje DGN podklad a že je externí soubor DGN přístupný. |
| **Výstupní PDF je prázdné** | Možnosti rasterizace jsou nastaveny na nulovou velikost. | Upravit `PageWidth`/`PageHeight` nebo nastavit `NoScaling = false`. |
| **Licence výjimka** | Spouštění bez platné licence Aspose.CAD. | Aplikujte licenci před načtením obrázku: `License lic = new License(); lic.SetLicense("Aspose.CAD.lic");` |

## Často kladené otázky

### Q1: Mohu použít Aspose.CAD pro .NET ve svých komerčních projektech?
A1: Ano, můžete. Navštivte [zde](https://purchase.aspose.com/buy) pro informace o licencování.

### Q2: Existují nějaká omezení velikosti souborů DWG, které mohu zpracovat?
A2: Aspose.CAD podporuje práci s velkými soubory DWG, ale mohou platit omezení hardwaru.

### Q3: Je k dispozici zkušební verze?
A3: Ano, můžete získat bezplatnou zkušební verzi [zde](https://releases.aspose.com/).

### Q4: Jak získám dočasné licence?
A4: Dočasné licence lze získat [zde](https://purchase.aspose.com/temporary-license/).

### Q5: Kde mohu získat pomoc, pokud narazím na problémy?
A5: Navštivte fórum Aspose.CAD [zde](https://forum.aspose.com/c/cad/19) pro podporu.

**Q: Jak nastavit další metadata PDF (autor, název atd.)?**  
A: Použijte vlastnosti `exportOptions.Metadata` před voláním `Save`.

**Q: Mohu exportovat více rozvržení do samostatných stránek PDF?**  
A: Ano – nastavte `Layouts = new string[] { "Layout1", "Layout2" }` v `CadRasterizationOptions`.

**Q: Podporuje Aspose.CAD konverzi DWG do jiných formátů obrázků?**  
A: Rozhodně. Můžete exportovat do PNG, JPEG, SVG a dalších pomocí odpovídajících přetížení `Image.Save`.

---

**Poslední aktualizace:** 2026-03-21  
**Testováno s:** Aspose.CAD 24.11 pro .NET  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}