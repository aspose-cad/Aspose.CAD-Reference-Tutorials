---
date: 2026-07-18
description: Jak exportovat CAD do PNG pomocí Aspose.CAD pro .NET. Převádějte soubory
  IFC na vysoce kvalitní PNG obrázky rychle a spolehlivě.
keywords:
- how to export cad to png
- Aspose.CAD IFC conversion
- CAD to PNG .NET
lastmod: 2026-07-18
linktitle: Export souborů IFC do PNG
og_description: Jak exportovat CAD do PNG pomocí Aspose.CAD pro .NET. Naučte se krok
  za krokem převod souborů IFC do PNG obrázků bez nutnosti kódu.
og_image_alt: Guide showing IFC to PNG conversion with Aspose.CAD for .NET
og_title: Jak exportovat CAD do PNG – Průvodce Aspose.CAD .NET
schemas:
- author: Aspose
  dateModified: '2026-07-18'
  description: How to export CAD to PNG using Aspose.CAD for .NET. Convert IFC files
    to high‑quality PNG images quickly and reliably.
  headline: How to Export CAD to PNG – Exporting IFC Files with Aspose.CAD
  type: TechArticle
- questions:
  - answer: No, Aspose.CAD for .NET is specifically designed for Windows environments.
    question: Can I use Aspose.CAD for .NET on macOS or Linux?
  - answer: Yes, you can obtain a temporary license from [here](https://purchase.aspose.com/temporary-license/)
      for evaluation.
    question: Is a temporary license available for testing purposes?
  - answer: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for community
      support and discussions.
    question: How can I get support for Aspose.CAD?
  - answer: Refer to the [Aspose.CAD documentation](https://reference.aspose.com/cad/net/)
      for detailed information and examples.
    question: Where can I find comprehensive documentation?
  - answer: Check the documentation or seek assistance on the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19).
    question: What if I encounter issues during installation?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- export cad
- Aspose.CAD
- IFC to PNG
- .NET image conversion
title: Jak exportovat CAD do PNG – Export souborů IFC s Aspose.CAD
url: /cs/net/exporting-to-image-formats/exporting-ifc-files-to-png/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak exportovat CAD do PNG – Exportování souborů IFC pomocí Aspose.CAD

## Úvod

Pokud potřebujete **jak exportovat cad do png**, Aspose.CAD pro .NET nabízí spolehlivý, bezkódový způsob, jak převést modely IFC (Industry Foundation Classes) na ostré rastrové obrázky PNG. V tomto tutoriálu projdeme celý pracovní postup – od instalace knihovny po uložení finálního PNG – abyste mohli převod integrovat do jakékoli .NET aplikace s jistotou.

## Rychlé odpovědi
- **Jaká knihovna provádí konverzi?** Aspose.CAD pro .NET.
- **Podporovaný zdrojový formát?** IFC (Industry Foundation Classes) soubory.
- **Cílový formát obrázku?** PNG, s plnou kontrolou nad velikostí a rozlišením.
- **Minimální verze .NET?** .NET Framework 4.5+ nebo .NET Core 3.1+.
- **Požadavek na licenci?** Platná licence Aspose.CAD pro produkční použití.

## Co je „jak exportovat cad do png“?

Tento výraz odkazuje na proces převodu souborů CAD, jako je IFC, do formátu Portable Network Graphics (PNG). Tato konverze umožňuje snadné prohlížení, sdílení a vkládání CAD vizualizací do webových stránek, dokumentace nebo zpráv, poskytuje lehký, široce podporovaný formát, který zachovává vizuální věrnost bez nutnosti specializovaných CAD prohlížečů.

## Proč použít Aspose.CAD pro tuto konverzi?

Aspose.CAD podporuje **více než 50 formátů CAD a BIM** a dokáže zpracovat stovky stránek IFC modelů, aniž by načítal celý soubor do paměti. Poskytuje rychlé, paměťově úsporné konverze na standardním serverovém hardware, automaticky zpracovává vrstvy, tloušťky čar a mapování barev a nabízí rozsáhlé konfigurační možnosti pro kvalitu a velikost výstupu.

## Předpoklady

### 1. Instalace Aspose.CAD
Ujistěte se, že máte nainstalovaný Aspose.CAD pro .NET. Můžete jej stáhnout ze stránky vydání [zde](https://releases.aspose.com/cad/net/).

### 2. Adresář dokumentů
Vytvořte určený adresář pro své dokumenty. V ukázkovém příkladu proměnná `MyDir` představuje adresář dokumentů.

## Importovat jmenné prostory
Nyní, když jsou předpoklady připraveny, importujte jmenné prostory potřebné pro práci s Aspose.CAD ve vašem .NET projektu.

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using Aspose.CAD.FileFormats.Ifc;
```

## Jak exportovat CAD do PNG?

`IfcImage` představuje IFC CAD obrázek, který lze rasterizovat do rastrových formátů, jako je PNG. Načtěte svůj IFC soubor pomocí `new IfcImage("source.ifc")`, nakonfigurujte rasterizaci pomocí `RasterizationOptions`, nastavte specifické volby pro PNG pomocí `PngOptions` a nakonec zavolejte `Save(outputPath, pngOptions)`. Tento kompletní tok převádí CAD model na vysoce rozlišený PNG během několika řádků kódu, automaticky zpracovává vrstvy, barvy a tloušťky čar.

## Krok 1: Načíst soubor IFC
Třída `IfcImage` načte IFC model a připraví jej k rasterizaci.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "example.ifc";
using (IfcImage cadImage = (IfcImage)Image.Load(sourceFilePath))
{
```

V tomto kroku inicializujeme objekt Aspose.CAD `IfcImage` a načteme do něj soubor IFC.

## Krok 2: Nastavit možnosti rasterizace
Třída `RasterizationOptions` určuje, jak jsou vektorová data převáděna na rastrové obrázky, včetně šířky stránky, výšky a barvy pozadí.

```csharp
    CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
   
    rasterizationOptions.PageWidth = 100;
    rasterizationOptions.PageHeight = 100;
```

Definujte možnosti rasterizace pro nastavení šířky a výšky stránky výstupního PNG.

## Krok 3: Nastavit PNG možnosti
Třída `PngOptions` obsahuje nastavení specifická pro výstup PNG, jako je úroveň komprese a barevná hloubka.

```csharp
    PngOptions pngOptions = new PngOptions();
    pngOptions.VectorRasterizationOptions = rasterizationOptions;
```

Vytvořte PNG možnosti a přiřaďte k nim dříve definované možnosti rasterizace.

## Krok 4: Specifikovat výstupní cestu
Výstupní cesta určuje, kam bude vygenerovaný PNG soubor uložen.

```csharp
    // Set output path as well
    string outPath = sourceFilePath + ".png";
    cadImage.Save(outPath, pngOptions);
}
```

Definujte výstupní cestu pro PNG soubor, zajistěte, aby měl stejný název jako zdrojový soubor s příponou „.png“. Nakonec uložte převedený obrázek.

## Časté problémy a řešení
- **Chybějící písma nebo styly čar:** Ujistěte se, že IFC soubor odkazuje na všechny požadované zdroje; Aspose.CAD vloží chybějící prostředky, pokud je to možné.
- **Velké soubory způsobují špičky v paměti:** Použijte vlastnost `MemoryLimit` na `RasterizationOptions` pro omezení využití paměti.
- **Nesprávné barvy:** Ověřte, že definice barev ve zdrojovém IFC jsou v souladu se schématem IFC; Aspose.CAD respektuje standardní mapování barev.

## Často kladené otázky

**Q: Mohu použít Aspose.CAD pro .NET na macOS nebo Linuxu?**  
A: Ne, Aspose.CAD pro .NET je specificky navržen pro Windows prostředí.

**Q: Je k dispozici dočasná licence pro testovací účely?**  
A: Ano, dočasnou licenci můžete získat [zde](https://purchase.aspose.com/temporary-license/) pro vyhodnocení.

**Q: Jak mohu získat podporu pro Aspose.CAD?**  
A: Navštivte [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) pro komunitní podporu a diskuse.

**Q: Kde najdu komplexní dokumentaci?**  
A: Odkazujte na [dokumentaci Aspose.CAD](https://reference.aspose.com/cad/net/) pro podrobné informace a příklady.

**Q: Co dělat, když narazím na problémy během instalace?**  
A: Zkontrolujte dokumentaci nebo požádejte o pomoc na [forum Aspose.CAD](https://forum.aspose.com/c/cad/19).

---

**Poslední aktualizace:** 2026-07-18  
**Testováno s:** Aspose.CAD 24.11 pro .NET  
**Autor:** Aspose

## Související tutoriály

- [Převést CAD výkres na rastrový obrázek v Aspose.CAD pro .NET](/cad/net/cad-drawing-manipulation/convert-cad-drawing-to-raster-image/)
- [Jednoduchý převod STL do PNG pomocí Aspose.CAD pro .NET](/cad/net/stl-file-export/exporting-stl-files-to-png/)
- [Exportovat CAD rozvržení do rastrových formátů obrázků v Aspose.CAD pro .NET](/cad/net/cad-export-formats/export-cad-layouts-to-raster-image-formats/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}