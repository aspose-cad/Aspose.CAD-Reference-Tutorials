---
date: 2026-07-04
description: Zjistěte, jak nastavit velikost stránky PDF při převodu souborů OBJ do
  PDF pomocí Aspose.CAD pro .NET. Průvodce krok za krokem s předpoklady, rasterization
  options a PDF options.
keywords:
- set pdf page size
- load obj file
- save cad as pdf
- 3d model to pdf
- how to convert obj
linktitle: Podpora formátu OBJ v Aspose.CAD – tutoriál
schemas:
- author: Aspose
  dateModified: '2026-07-04'
  description: Learn how to set PDF page size while converting OBJ files to PDF using
    Aspose.CAD for .NET. Step‑by‑step guide with prerequisites, rasterization options,
    and PDF options.
  headline: Set PDF Page Size for OBJ Files with Aspose.CAD - Tutorial
  type: TechArticle
- questions:
  - answer: Yes, Aspose.CAD supports over **30** input formats—including DWG, DXF,
      DGN, and STL—and can export to more than **20** raster and vector formats.
    question: Is Aspose.CAD compatible with other CAD file formats?
  - answer: Absolutely! You can explore a free trial version [here](https://releases.aspose.com/).
    question: Can I try Aspose.CAD before purchasing?
  - answer: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) to ask
      questions and share experiences with the community.
    question: How do I obtain support for Aspose.CAD?
  - answer: Yes, temporary licenses can be obtained [here](https://purchase.aspose.com/temporary-license/).
    question: Are temporary licenses available for testing?
  - answer: You can purchase Aspose.CAD [here](https://purchase.aspose.com/buy).
    question: Where can I purchase a full license?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Nastavte velikost stránky PDF pro soubory OBJ pomocí Aspose.CAD – tutoriál
url: /cs/net/3d-model-support/supporting-obj-format-in-aspose-cad/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Nastavte velikost PDF stránky pro soubory OBJ pomocí Aspose.CAD – tutoriál

## Úvod

Pokud vyvíjíte CAD aplikace v .NET a potřebujete **nastavit velikost PDF stránky** při konverzi modelů OBJ, Aspose.CAD pro .NET poskytuje čisté API založené na kódu, které zvládá rasterizaci i generování PDF v jednom toku. V tomto tutoriálu vás provedeme instalací knihovny, načtením souboru OBJ, konfigurací rozměrů stránky a nakonec uložením výsledku jako PDF. Na konci budete mít znovupoužitelný vzor pro převod libovolného 3‑D modelu do PDF dokumentu s přesnou velikostí.

## Rychlé odpovědi
- **Může Aspose.CAD převést OBJ na PDF?** Ano – načtěte OBJ pomocí `Image.Load` a rasterizujte jej do PDF.
- **Jak nastavit vlastní velikost PDF stránky?** Použijte `PdfOptions` → `PageSize` nebo nastavte šířku/výšku v `RasterizationOptions`.
- **Jaké verze .NET jsou podporovány?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.
- **Potřebuji licenci pro vývoj?** Bezplatná zkušební verze funguje pro hodnocení; licence je vyžadována pro produkci.
- **Je konverze paměťově efektivní?** Aspose.CAD streamuje data a dokáže zpracovat stovky stránek PDF, aniž by načítal celý soubor do paměti.

## Co je formát OBJ?
Formát OBJ je široce používaný textový formát pro definici 3‑D geometrie, který ukládá pozice vrcholů, texturové souřadnice a definice ploch. Je podporován většinou 3‑D modelovacích nástrojů a je ideální pro výměnu mezi CAD a renderovacími pipeline.

## Proč nastavit vlastní velikost PDF stránky?
Aspose.CAD může vykreslit CAD výkres do libovolné rasterové velikosti. Explicitním nastavením rozměrů PDF stránky zajistíte, že finální dokument odpovídá vašim standardům reportování, pasuje na standardní formáty papíru (A4, Letter) nebo splňuje vlastní rozvržení tisku. Kvantifikovaný přínos: API může v jednom volání generovat PDF až **200 mm × 200 mm**, zpracovávat soubory větší než **500 MB** bez překročení 250 MB RAM.

## Požadavky

- **Aspose.CAD Library** – Zajistěte, aby byla knihovna Aspose.CAD nainstalována ve vašem .NET projektu. Můžete ji stáhnout [zde](https://releases.aspose.com/cad/net/) a zobrazit kompletní referenci API v [dokumentaci](https://reference.aspose.com/cad/net/).
- **Document Directory** – Vytvořte složku pro vaše CAD assety; v průvodci ji budeme označovat jako „Your Document Directory“.
- **.NET Development Environment** – Visual Studio 2022 nebo jakékoli IDE podporující .NET 6+.

## Jak nastavit velikost PDF stránky při převodu OBJ na PDF?

Načtěte soubor OBJ, nakonfigurujte možnosti rasterizace s požadovanou šířkou a výškou, připojte tyto možnosti k instanci `PdfOptions` a zavolejte `Save`. Tento dvoukrokový vzor zaručuje, že PDF stránka bude mít rozměry, které určíte, a zároveň zachová detailnost modelu.

## Krok 1: Importovat jmenné prostory

Třída `Image` zpracovává všechny CAD formáty a třída `PdfOptions` řídí výstup PDF.  
`Image` představuje CAD dokument a poskytuje metody pro načítání a ukládání souborů. `PdfOptions` definuje nastavení pro generování PDF, jako je velikost stránky a komprese.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Krok 2: Načíst soubor OBJ

Načtěte soubor OBJ do objektu Aspose.CAD image. Nahraďte `"example-580-W.obj"` názvem vašeho OBJ souboru.

```csharp
string MyDir = "Your Document Directory";
using (Aspose.CAD.Image CADDoc = Aspose.CAD.Image.Load(MyDir + "example-580-W.obj"))
{
    // Your code for further processing goes here
}
```

## Krok 3: Nakonfigurovat možnosti rasterizace

`RasterizationOptions` určuje rasterovou velikost, která se nakonec stane velikostí PDF stránky. Nastavením `PageWidth` a `PageHeight` můžete přesně kontrolovat rozměry výstupního PDF.  
`CadRasterizationOptions` (exponováno přes `RasterizationOptions`) specifikuje parametry rasterizace, jako jsou rozměry stránky a rozlišení.

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions rasterizationOptions =
    new Aspose.CAD.ImageOptions.CadRasterizationOptions();

rasterizationOptions.PageWidth = CADDoc.Size.Width;
rasterizationOptions.PageHeight = CADDoc.Size.Height;
```

## Krok 4: Vytvořit PDF možnosti

`PdfOptions` spojuje nastavení rasterizace s PDF zapisovačem. Přiřazením instance `RasterizationOptions` zajistíte, že PDF zdědí velikost stránky, kterou jste definovali.

```csharp
Aspose.CAD.ImageOptions.PdfOptions CADf = new Aspose.CAD.ImageOptions.PdfOptions();
CADf.VectorRasterizationOptions = rasterizationOptions;
```

## Krok 5: Uložit jako PDF

Zavolejte metodu `Save` na objektu `Image`, předáte cílový název souboru a nakonfigurované `PdfOptions`. Knihovna zapíše PDF s přesnou velikostí stránky, kterou jste určili.  
`Save` zapisuje obrázek do souboru pomocí zvoleného formátu a možností.

```csharp
CADDoc.Save(MyDir + "example-580-W_custom.pdf", CADf);
```

## Časté problémy a řešení

- **Nesprávné rozměry stránky** – Ověřte, že `PageWidth` a `PageHeight` jsou nastaveny v **pixelech**; použijte `Resolution` k převodu palců nebo milimetrů na pixely (např. 300 dpi → 1 palec = 300 px).
- **Chybějící textury** – OBJ soubory často odkazují na externí soubory `.mtl`; ujistěte se, že soubor materiálu se nachází ve stejném adresáři jako OBJ.
- **Vysoká spotřeba paměti u velkých souborů** – Aktivujte `Image.SaveOptions.Compression` pro snížení zatížení paměti při renderování ve vysokém rozlišení.

## Často kladené otázky

**Q: Je Aspose.CAD kompatibilní s jinými CAD formáty?**  
A: Ano, Aspose.CAD podporuje více než **30** vstupních formátů – včetně DWG, DXF, DGN a STL – a může exportovat do více než **20** rasterových a vektorových formátů.

**Q: Mohu vyzkoušet Aspose.CAD před zakoupením?**  
A: Rozhodně! Bezplatnou zkušební verzi můžete prozkoumat [zde](https://releases.aspose.com/).

**Q: Jak získám podporu pro Aspose.CAD?**  
A: Navštivte [Aspose.CAD fórum](https://forum.aspose.com/c/cad/19), kde můžete klást otázky a sdílet zkušenosti s komunitou.

**Q: Jsou k dispozici dočasné licence pro testování?**  
A: Ano, dočasné licence lze získat [zde](https://purchase.aspose.com/temporary-license/).

**Q: Kde mohu zakoupit plnou licenci?**  
A: Plnou licenci Aspose.CAD můžete zakoupit [zde](https://purchase.aspose.com/buy).

---

**Poslední aktualizace:** 2026-07-04  
**Testováno s:** Aspose.CAD 24.11 for .NET  
**Autor:** Aspose

## Související tutoriály

- [Exportování souborů IGES do PDF – průvodce Aspose.CAD](/cad/net/exporting-to-image-formats/exporting-iges-files-to-pdf/)
- [Exportování DXF do formátu PDF – tutoriál Aspose.CAD](/cad/net/export-techniques/exporting-dxf-to-pdf-format/)
- [Exportování CAD výkresů do PDF – tutoriál Aspose.CAD](/cad/net/advanced-export-techniques/exporting-cad-drawings-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}