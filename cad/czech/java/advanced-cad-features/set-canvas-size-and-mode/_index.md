---
date: 2026-08-29
description: Zjistěte, jak nastavit velikost stránky PDF a převést CAD na PDF pomocí
  Aspose.CAD pro Java, s automatic layout scaling a TIFF export.
keywords:
- set pdf page size
- convert cad to pdf
- canvas size java
- high resolution tiff
- change pdf dimensions
lastmod: 2026-08-29
linktitle: Nastavit velikost stránky PDF – převést CAD na PDF
og_description: Zjistěte, jak nastavit velikost stránky PDF při převodu výkresů CAD
  na PDF v Java pomocí Aspose.CAD. Tento průvodce zahrnuje canvas dimensions, automatic
  layout scaling a export do high‑resolution TIFF.
og_image_alt: Tutorial showing how to set pdf page size and convert CAD to PDF in
  Java
og_title: Nastavit velikost stránky PDF – převést CAD na PDF s Aspose v Java
schemas:
- author: Aspose
  dateModified: '2026-08-29'
  description: Learn how to set pdf page size and convert CAD to PDF using Aspose.CAD
    for Java, with automatic layout scaling and TIFF export.
  headline: Set pdf page size – convert cad to pdf (Java)
  type: TechArticle
- questions:
  - answer: No. Canvas size controls page dimensions; vector data remains resolution‑independent,
      ensuring crisp rendering at any zoom level.
    question: does the canvas size affect vector quality in the PDF?
  - answer: Yes. Adjust `rasterizationOptions.setResolution(dpiValue)` before creating
      `TiffOptions`.
    question: can I set a different DPI for the TIFF output?
  - answer: Use Aspose.PDF to load the generated PDF and call `pdf.getPages().setPageSize(PageSize.A4)`
      or a custom size.
    question: how can I change PDF dimensions for an existing PDF without re‑rendering
      the CAD?
  - answer: Keep `setAutomaticLayoutsScaling(true)` and avoid `setNoScaling(true)`;
      this retains layer visibility and layout fidelity.
    question: what is the best way to convert dxf to pdf while preserving layers?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- set pdf page size
- convert cad
- Aspose.CAD
- Java
- high resolution tiff
title: Nastavit velikost stránky PDF – převést CAD na PDF (Java)
url: /cs/java/advanced-cad-features/set-canvas-size-and-mode/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Nastavení velikosti PDF stránky – převod CAD na PDF (Java)

## Úvod

Pokud potřebujete **nastavit velikost PDF stránky** při převodu výkresů CAD na PDF, jste na správném místě. V tomto tutoriálu vám ukážeme, jak pomocí Aspose.CAD pro Java definovat přesné rozměry plátna, povolit automatické škálování rozvržení a poté exportovat výsledek jak do PDF, tak do TIFF. Ať už připravujete technické schémata k tisku nebo generujete miniatury pro webovou galerii, kontrola velikosti stránky a rozlišení výstupu je nezbytná.

## Rychlé odpovědi
- **Co znamená „převod CAD na PDF“?** Přeměna výkresu CAD (např. DXF, DWG) na PDF dokument, který lze zobrazit na jakékoli platformě.  
- **Mohu také exportovat do TIFF?** Ano — použijte `TiffOptions` k vytvoření vysoce rozlišených rastrových obrázků.  
- **Která možnost řídí velikost plátna v Javě?** `CadRasterizationOptions.setPageWidth/Height`.  
- **Co je automatické škálování rozvržení?** Příznak (`setAutomaticLayoutsScaling(true)`), který zachovává původní proporce rozvržení při změně velikosti plátna.  
- **Potřebuji licenci pro Aspose.CAD?** Pro produkční použití je vyžadována dočasná nebo trvalá licence.

## Jak nastavit velikost PDF stránky při převodu CAD na PDF v Javě

Načtěte svůj CAD soubor, nakonfigurujte `CadRasterizationOptions` s požadovanou šířkou a výškou, povolte automatické škálování rozvržení a poté uložte výsledek jako PDF. Tento dvoukrokový přístup vám umožní řídit přesné rozměry výstupní stránky bez ztráty vektorové kvality.

## Co je převod CAD na PDF?

Převod CAD na PDF znamená převést vektorové technické výkresy na PDF stránky, přičemž se zachová čára, vrstvy a geometrie a soubor bude univerzálně přístupný. Proces rasterizuje výkres podle zadaných možností a vytvoří PDF, které lze otevřít na jakémkoli zařízení bez nutnosti CAD softwaru a zachovává vizuální věrnost původního návrhu.

## Proč nastavit velikost plátna v Javě?

Nastavení velikosti plátna v Javě vám umožní definovat výstupní rozlišení a rozměry stránky, což zajišťuje, že výsledné PDF nebo TIFF odpovídá vašim požadavkům na tisk či zobrazení. Také získáte kontrolu nad chováním škálování, což je zásadní pro výkresy velkého formátu.

## Předpoklady

Před tím, než se pustíte do tutoriálu, ujistěte se, že máte následující předpoklady připravené:

- Aspose.CAD pro Java: Ujistěte se, že máte knihovnu Aspose.CAD nainstalovanou ve svém Java prostředí. Knihovnu Aspose.CAD pro Java můžete stáhnout [zde](https://releases.aspose.com/cad/java/).
- Adresář dokumentů: Vytvořte adresář pro ukládání vašich CAD souborů. Tento adresář bude odkazován v krocích tutoriálu.

Nyní pojďme na krok‑za‑krokem průvodce.

## Import jmenných prostorů

V tomto kroku importujeme potřebné jmenné prostory pro zahájení vašeho Aspose.CAD projektu.

`Image` je hlavní třída používaná k načtení CAD souborů.

```java
import java.awt.Image;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## Krok 1: importovat třídy Aspose.CAD

Třída `Image` poskytuje metody pro načítání a ukládání CAD výkresů.

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
com.aspose.cad.Image objImage = com.aspose.cad.Image.load(srcFile);
```

V tomto úryvku nastavujeme cestu k adresáři zdrojů a načítáme soubor DXF pomocí třídy `Image` z Aspose.CAD.

## Krok 2: nastavit vlastnosti CadRasterizationOptions (nastavit velikost plátna v Javě)

`CadRasterizationOptions` určuje nastavení rasterizace, jako je velikost stránky a škálování pro převod CAD → raster.

```java
// Create an instance of CadRasterizationOptions and set its various properties
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

Zde vytváříme instanci `CadRasterizationOptions` a konfiguruje vlastnosti jako šířka stránky, výška stránky a **automatické škálování rozvržení**. Toto je jádro **konfigurace režimu plátna** pro váš převod.

## Krok 3: vytvořit PdfOptions a nastavit vectorRasterizationOptions

`PdfOptions` definuje nastavení výstupu PDF pro převod.

```java
// Create an instance of PdfOptions
PdfOptions pdfOptions = new PdfOptions();

// Set the VectorRasterizationOptions property
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Nyní vytvoříme instanci `PdfOptions` a nastavíme její vlastnost `VectorRasterizationOptions` na dříve nakonfigurovaný `CadRasterizationOptions`.

## Krok 4: export do PDF (převod CAD na PDF)

```java
// Export CAD to PDF
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

Nakonec uložíme CAD obrázek do PDF souboru pomocí specifikovaných možností, čímž dokončíme proces **převodu CAD na PDF**.

## Krok 5: vytvořit TiffOptions a nastavit vectorRasterizationOptions (export CAD do TIFF)

`TiffOptions` konfiguruje parametry výstupu TIFF, jako je komprese a rozlišení.

```java
// Create an instance of TiffOptions
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);

// Set the VectorRasterizationOptions property
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
```

V tomto kroku nastavujeme instanci `TiffOptions` a konfiguruje její vlastnost `VectorRasterizationOptions`.

## Krok 6: export do TIFF

```java
// Export CAD to TIFF
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

Nakonec uložíme CAD obrázek do TIFF souboru pomocí specifikovaných možností, čímž demonstrujeme, jak **exportovat CAD do TIFF** po nastavení velikosti plátna.

## Časté problémy a řešení

| Problém | Příčina | Řešení |
|-------|-------|-----|
| Výstupní PDF je prázdný | `setNoScaling(true)` zakazuje vykreslování u některých výkresů | Odstraňte `setNoScaling(true)` nebo nastavte na `false`. |
| Rozlišení TIFF vypadá nízko | Šířka/výška stránky jsou příliš malé | Zvyšte hodnoty `setPageWidth` / `setPageHeight`. |
| Rozvržení je deformované | Automatické škálování rozvržení je vypnuto | Ujistěte se, že je povoleno `setAutomaticLayoutsScaling(true)`. |

## Proč upravovat velikost plátna a DPI?

Změna velikosti plátna přímo ovlivňuje rozlišení rasterizace výstupu. Pokud potřebujete **zvýšit rozlišení TIFF**, jednoduše zvýšte hodnoty `setPageWidth` / `setPageHeight` nebo zavolejte `rasterizationOptions.setResolution(300)` před vytvořením `TiffOptions`. To vám poskytne vysoce kvalitní rastrové obrázky vhodné pro tisk nebo podrobnou kontrolu.

## Často kladené otázky

**Q1: mohu použít Aspose.CAD pro Java s jinými Java frameworky?**  
A: Ano, Aspose.CAD je navržen tak, aby se bez problémů integroval s různými Java frameworky.

**Q2: je k dispozici dočasná licence pro Aspose.CAD?**  
A: Ano, dočasnou licenci získáte na stránce [zde](https://purchase.aspose.com/temporary-license/).

**Q3: kde mohu získat komunitní podporu pro Aspose.CAD?**  
A: Navštivte fórum Aspose.CAD [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) pro komunitní podporu a diskuze.

**Q4: mohu vyzkoušet Aspose.CAD zdarma?**  
A: Rozhodně! Stáhněte si bezplatnou zkušební verzi [zde](https://releases.aspose.com/).

**Q5: jak si mohu zakoupit Aspose.CAD pro Java?**  
A: Zakupte Aspose.CAD pro Java [zde](https://purchase.aspose.com/buy).

**Další otázky a odpovědi**

**Q: ovlivňuje velikost plátna vektorovou kvalitu v PDF?**  
A: Ne. Velikost plátna řídí rozměry stránky; vektorová data zůstávají rozlišením nezávislá, což zajišťuje ostré vykreslení při libovolném přiblížení.

**Q: mohu nastavit jiný DPI pro výstup TIFF?**  
A: Ano. Před vytvořením `TiffOptions` upravte `rasterizationOptions.setResolution(dpiValue)`.

**Q: jak mohu změnit rozměry PDF existujícího souboru bez opětovného renderování CAD?**  
A: Použijte Aspose.PDF k načtení vygenerovaného PDF a zavolejte `pdf.getPages().setPageSize(PageSize.A4)` nebo vlastní velikost.

**Q: jaký je nejlepší způsob převodu DXF na PDF při zachování vrstev?**  
A: Zachovejte `setAutomaticLayoutsScaling(true)` a vyhněte se `setNoScaling(true)`; tím se udrží viditelnost vrstev a věrnost rozvržení.

## Závěr

Gratulujeme! Úspěšně jste **převáděli CAD na PDF** a **exportovali CAD do TIFF** při **nastavení velikosti plátna v Javě**, povolili **automatické škálování rozvržení** a naučili se **konfigurovat režim plátna** pro výstupy vysoké kvality. Tento tutoriál poskytuje pevný základ pro vaše projekty převodu CAD. Prozkoumejte další funkce a možnosti v [dokumentaci Aspose.CAD](https://reference.aspose.com/cad/java/).

---

**Poslední aktualizace:** 2026-08-29  
**Testováno s:** Aspose.CAD pro Java 24.12  
**Autor:** Aspose

## Související tutoriály

- [Nastavení velikosti plátna – Pokročilé CAD funkce s Aspose.CAD pro Java](/cad/java/advanced-cad-features/)
- [Export DWG do PDF v Javě – Nastavení velikosti PDF stránky s Aspose.CAD](/cad/java/cad-export-options/export-to-pdf/)
- [Nastavení vlastní velikosti stránky – PDF z CAD s automatickým škálováním rozvržení](/cad/java/advanced-cad-features/setting-auto-layout-scaling/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}