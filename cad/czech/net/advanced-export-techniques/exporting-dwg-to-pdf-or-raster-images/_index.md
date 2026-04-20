---
date: 2026-03-16
description: Naučte se, jak převést DWG na PDF nebo rastrové obrázky pomocí Aspose.CAD
  pro .NET. Tento krok‑za‑krokem návod na převod CAD do PDF pokrývá export DWG do
  obrazových formátů, jako je PNG, a ukazuje, jak efektivně exportovat DWG do souborů
  s obrázky.
linktitle: Exporting DWG to PDF or Raster Images
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Jak převést DWG na PDF a rastrové obrázky pomocí Aspose.CAD pro .NET
url: /cs/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export DWG do PDF nebo rastrových obrázků – průvodce Aspose.CAD

## Úvod

Pokud potřebujete **převést DWG do PDF** (nebo do rastrových formátů, jako je PNG) přímo z .NET aplikace, jste na správném místě. V tomto tutoriálu vás provedeme přesnými kroky potřebnými k použití Aspose.CAD pro .NET k provedení konverze, vysvětlíme, proč je knihovna solidní volbou, a ukážeme, jak pomocí několika řádků kódu zpracovat výstup jak do PDF, tak do obrázku.

## Rychlé odpovědi
- **Jaká knihovna zpracovává konverzi DWG?** Aspose.CAD for .NET  
- **Mohu exportovat DWG do PNG i do PDF?** Ano – stejné rasterizační možnosti fungují pro oba formáty.  
- **Potřebuji licenci pro vývoj?** Bezplatná zkušební verze funguje pro testování; pro produkci je vyžadována komerční licence.  
- **Jaké verze .NET jsou podporovány?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Je převod jednotek prováděn automaticky?** Můžete definovat systém jednotek ručně (metrický nebo imperiální) podle ukázky v kódu.

## Co znamená „převést DWG do PDF“?
Převod DWG do PDF znamená převzít CAD výkres (DWG) a vykreslit jej do přenosného, pouze pro čtení určeného dokumentu (PDF). To je užitečné pro sdílení návrhů se zúčastněnými stranami, které nemají CAD software, pro tvorbu tisknutelné dokumentace nebo archivaci výkresů v univerzálně čitelném formátu.

## Proč použít Aspose.CAD pro tuto konverzi?
- **Žádné externí závislosti** – knihovna funguje zcela v řízeném kódu.  
- **Vysoká věrnost** – zachovává vrstvy, tloušťky čar a informace o rozvržení.  
- **Vestavěné rasterizační možnosti** – umožňují export do PNG, JPEG, BMP atd. pomocí jediného konfiguračního objektu.  
- **Cross‑platform** – funguje na Windows, Linuxu i macOS s .NET Core.

## Předpoklady

Než se pustíme do tutoriálu, ujistěte se, že máte následující připravené:

- Základní znalost programování v .NET.  
- Knihovna Aspose.CAD pro .NET nainstalována. Pokud ne, stáhněte ji [zde](https://releases.aspose.com/cad/net/).  
- Vaše oblíbené integrované vývojové prostředí (IDE) nastavené pro vývoj v .NET.

## Importujte jmenné prostory

Začněme importováním potřebných jmenných prostorů ve vašem .NET projektu. Tím zajistíte přístup k funkcionalitě Aspose.CAD ve vašem kódu.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
```

## Krok 1: Načtení souboru DWG

Začněte načtením souboru DWG, který chcete převést. Nahraďte `"Your Document Directory"` cestou k vašemu souboru DWG.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Your code for loading DWG goes here
}
```

## Krok 2: Nastavení exportu do PDF (Jak exportovat DWG do PDF)

Nyní nakonfigurujme nastavení exportu do PDF. Tento příklad ukazuje, jak nastavit rozvržení a zpracovat převod jednotek.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new string[] { "Model" };

// Check and define the unit system
bool currentUnitIsMetric = false;
double currentUnitCoefficient = 1.0;
DefineUnitSystem(cadImage.UnitType, out currentUnitIsMetric, out currentUnitCoefficient);

// Your code for setting up PDF export goes here
```

## Krok 3: Export do PDF

Proveďte export do PDF pomocí nakonfigurovaných nastavení.

```csharp
PdfOptions pdfOptions = new PdfOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath, pdfOptions);
```

## Krok 4: Export do rastrových obrázků (export dwg do obrázku)

Rozšiřte funkcionalitu o export do rastrových obrázků, například PNG.

```csharp
// A4 size at 300 DPI - 2480 x 3508
rasterizationOptions.PageHeight = 3508;
rasterizationOptions.PageWidth = 2480;

PngOptions pngOptions = new PngOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath.Replace("pdf", "png"), pngOptions);
```

## Časté problémy a řešení

| Problém | Proč k tomu dochází | Jak opravit |
|-------|----------------|------------|
| **Prázdné stránky v PDF** | Rozvržení není správně specifikováno | Ujistěte se, že `rasterizationOptions.Layouts` obsahuje správný název rozvržení (např. `"Model"`). |
| **Nesprávné rozměry** | Neshoda DPI nebo velikosti stránky | Upravte hodnoty `PageHeight`, `PageWidth` a DPI v `CadRasterizationOptions`. |
| **Jednotky jsou špatné** | Převod jednotek není definován | Použijte `DefineUnitSystem` k nastavení `currentUnitIsMetric` a `currentUnitCoefficient` na základě `cadImage.UnitType`. |
| **Výjimka licence** | Omezení zkušební verze | Aplikujte dočasnou nebo trvalou licenci před voláním `Image.Load`. |

## Často kladené otázky

### Q1: Mohu používat Aspose.CAD pro .NET ve svých komerčních projektech?
A1: Ano, můžete. Navštivte [purchase.aspose.com/buy](https://purchase.aspose.com/buy) pro podrobnosti o licencování.

### Q2: Je k dispozici bezplatná zkušební verze?
A2: Samozřejmě! Získejte svou bezplatnou zkušební verzi [zde](https://releases.aspose.com/).

### Q3: Jak mohu získat podporu pro Aspose.CAD pro .NET?
A3: Navštivte [Aspose.CAD fórum](https://forum.aspose.com/c/cad/19) pro komunitní podporu.

### Q4: Mohu získat dočasnou licenci pro testovací účely?
A4: Ano, dočasnou licenci můžete získat [zde](https://purchase.aspose.com/temporary-license/).

### Q5: Kde mohu najít podrobnou dokumentaci?
A5: Dokumentace je dostupná na [Aspose.CAD](https://reference.aspose.com/cad/net/).

### Q6: Jak **uložit CAD jako PNG** s vysokou kvalitou?
A6: Nastavte `PageHeight` a `PageWidth` na požadované rozměry v pixelech a v `CadRasterizationOptions` zvolte DPI 300 nebo vyšší.

### Q7: Jaký je nejlepší způsob **jak převést dwg**, když zdrojový soubor obsahuje více rozvržení?
A7: Naplněte `rasterizationOptions.Layouts` všemi názvy rozvržení, které chcete exportovat, poté projděte každé rozvržení ve smyčce a zavolejte `Save` pro každý výstupní formát.

**Poslední aktualizace:** 2026-03-16  
**Testováno s:** Aspose.CAD 24.11 pro .NET  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}