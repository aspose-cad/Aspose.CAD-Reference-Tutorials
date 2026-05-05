---
date: 2026-02-15
description: Naučte se nastavit velikost stránky PDF a převádět CAD do PDF pomocí
  Aspose.CAD pro Javu, s automatickým škálováním rozvržení a exportem do TIFF.
linktitle: Set PDF Page Size – Convert CAD to PDF
second_title: Aspose.CAD Java API
title: Nastavit velikost stránky PDF – převést CAD na PDF (Java)
url: /cs/java/advanced-cad-features/set-canvas-size-and-mode/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Nastavení velikosti plátna a režimu

## Úvod

Pokud potřebujete **nastavit velikost PDF stránky** při konverzi výkresů CAD do PDF, jste na správném místě. V tomto tutoriálu vám ukážeme, jak použít Aspose.CAD pro Java k definování přesných rozměrů plátna, povolení automatického škálování rozvržení a následnému exportu výsledku do PDF i TIFF. Ať už připravujete technické schémata k tisku nebo generujete náhledy pro webovou galerii, kontrola velikosti stránky a rozlišení výstupu je nezbytná.

## Rychlé odpovědi
- **Co znamená „převést CAD do PDF“?** Přeměna CAD výkresu (např. DXF, DWG) na PDF dokument, který lze zobrazit na jakékoli platformě.  
- **Mohu také exportovat do TIFF?** Ano — použijte `TiffOptions` k vytvoření vysoce rozlišených rastrových obrázků.  
- **Která volba řídí velikost plátna v Javě?** `CadRasterizationOptions.setPageWidth/Height`.  
- **Co je automatické škálování rozvržení?** Příznak (`setAutomaticLayoutsScaling(true)`), který zachovává původní proporce rozvržení při změně velikosti plátna.  
- **Potřebuji licenci pro Aspose.CAD?** Pro produkční použití je vyžadována dočasná nebo trvalá licence.

## Jak nastavit velikost PDF stránky při konverzi CAD do PDF (Java)

Nastavení velikosti PDF stránky (nebo plátna) vám umožní určit konečné rozměry dokumentu, což je zvláště užitečné, když musíte **změnit rozměry PDF** tak, aby odpovídaly tiskovým standardům nebo požadavkům UI. Níže projdeme každý krok a vysvětlíme *proč* stojí za každým řádkem kódu.

## Co je **convert CAD to PDF**?

Převod CAD do PDF znamená převést vektorové technické výkresy na PDF stránky, přičemž se zachová čárová práce, vrstvy a geometrie a soubor se zpřístupní univerzálně.

## Proč nastavit velikost plátna **java**?

Nastavení velikosti plátna v Javě vám umožní definovat výstupní rozlišení a rozměry stránky, čímž zajistíte, že výsledné PDF nebo TIFF splní vaše požadavky na tisk či zobrazení. Navíc získáte kontrolu nad chováním škálování, což je zásadní pro výkresy velkého formátu.

## Požadavky

Než se pustíte do tutoriálu, ujistěte se, že máte následující předpoklady:

- Aspose.CAD for Java: Ujistěte se, že máte knihovnu Aspose.CAD nainstalovanou ve svém Java prostředí. Můžete si ji stáhnout [zde](https://releases.aspose.com/cad/java/).
- Dokumentový adresář: Vytvořte adresář pro ukládání vašich CAD souborů. Tento adresář bude v tutoriálu odkazován.

Nyní pojďme na krok‑za‑krokem průvodce.

## Import Namespaces

V tomto kroku naimportujeme potřebné jmenné prostory, abychom mohli spustit váš projekt Aspose.CAD.

```java
import java.awt.Image;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## Krok 1: Import Aspose.CAD Classes

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
com.aspose.cad.Image objImage = com.aspose.cad.Image.load(srcFile);
```

V tomto úryvku nastavujeme cestu k adresáři s prostředky a načítáme DXF soubor pomocí třídy `Image` z Aspose.CAD.

## Krok 2: Nastavení vlastností **CadRasterizationOptions** (set canvas size java)

```java
// Create an instance of CadRasterizationOptions and set its various properties
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

Zde vytváříme instanci `CadRasterizationOptions` a konfigurujeme vlastnosti jako šířka stránky, výška stránky a **automatické škálování rozvržení**. Toto je jádro **configure canvas mode** pro vaši konverzi.

## Krok 3: Vytvoření PdfOptions a nastavení VectorRasterizationOptions

```java
// Create an instance of PdfOptions
PdfOptions pdfOptions = new PdfOptions();

// Set the VectorRasterizationOptions property
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Nyní vytvoříme instanci `PdfOptions` a nastavíme její vlastnost `VectorRasterizationOptions` na dříve nakonfigurovaný `CadRasterizationOptions`.

## Krok 4: Export do PDF (convert cad to pdf)

```java
// Export CAD to PDF
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

Nakonec uložíme CAD obrázek do PDF souboru pomocí zadaných možností, čímž dokončíme proces **convert CAD to PDF**.

## Krok 5: Vytvoření TiffOptions a nastavení VectorRasterizationOptions (export cad to tiff)

```java
// Create an instance of TiffOptions
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);

// Set the VectorRasterizationOptions property
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
```

V tomto kroku vytvoříme instanci `TiffOptions` a nakonfigurujeme její vlastnost `VectorRasterizationOptions`.

## Krok 6: Export do TIFF

```java
// Export CAD to TIFF
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

Nakonec uložíme CAD obrázek do TIFF souboru pomocí zadaných možností, čímž demonstrujeme, jak **export CAD to TIFF** po nastavení velikosti plátna.

## Časté problémy a řešení

| Problém | Příčina | Řešení |
|---------|---------|--------|
| Výstupní PDF je prázdný | `setNoScaling(true)` zakazuje vykreslování u některých výkresů | Odstraňte `setNoScaling(true)` nebo nastavte na `false`. |
| Rozlišení TIFF vypadá nízko | Šířka/výška stránky je příliš malá | Zvyšte hodnoty `setPageWidth` / `setPageHeight`. |
| Rozvržení je deformované | Automatické škálování rozvržení je vypnuto | Ujistěte se, že je povoleno `setAutomaticLayoutsScaling(true)`. |

## Proč upravit velikost plátna a DPI?

Změna velikosti plátna přímo ovlivňuje rozlišení rasterizace výstupu. Pokud potřebujete **zvýšit rozlišení TIFF**, jednoduše zvýšte hodnoty `setPageWidth` / `setPageHeight` nebo zavolejte `rasterizationOptions.setResolution(300)` před vytvořením `TiffOptions`. Tím získáte vysoce kvalitní rastrové obrázky vhodné pro tisk nebo detailní kontrolu.

## Často kladené otázky

### Q1: Mohu použít Aspose.CAD pro Java s jinými Java frameworky?

A1: Ano, Aspose.CAD je navržen tak, aby se bez problémů integroval s různými Java frameworky.

### Q2: Je k dispozici dočasná licence pro Aspose.CAD?

A2: Ano, dočasnou licenci můžete získat [zde](https://purchase.aspose.com/temporary-license/).

### Q3: Kde mohu získat komunitní podporu pro Aspose.CAD?

A3: Navštivte [Aspose.CAD fórum](https://forum.aspose.com/c/cad/19) pro komunitní podporu a diskuze.

### Q4: Můžu vyzkoušet Aspose.CAD zdarma?

A4: Samozřejmě! Získejte bezplatnou zkušební verzi [zde](https://releases.aspose.com/).

### Q5: Jak si mohu zakoupit Aspose.CAD pro Java?

A5: Produkt můžete zakoupit [zde](https://purchase.aspose.com/buy).

**Další otázky a odpovědi**

**Q: Ovlivňuje velikost plátna kvalitu vektorů v PDF?**  
A: Ne. Velikost plátna řídí rozměry stránky; vektorová data zůstávají rozlišením nezávislá, což zajišťuje ostré vykreslení při libovolném přiblížení.

**Q: Mohu nastavit jiné DPI pro výstup TIFF?**  
A: Ano. Před vytvořením `TiffOptions` upravte `rasterizationOptions.setResolution(dpiValue)`.

**Q: Jak mohu **změnit rozměry PDF** u existujícího PDF bez pře‑renderování CAD?**  
A: Použijte Aspose.PDF k načtení vygenerovaného PDF a zavolejte `pdf.getPages().setPageSize(PageSize.A4)` nebo vlastní velikost.

**Q: Jaký je nejlepší způsob **převodu dxf do pdf** při zachování vrstev?**  
A: Zachovejte `setAutomaticLayoutsScaling(true)` a vyhněte se `setNoScaling(true)`; tím se udrží viditelnost vrstev a věrnost rozvržení.

## Závěr

Gratulujeme! Úspěšně jste **převáděli CAD do PDF** a **exportovali CAD do TIFF** při **nastavení velikosti plátna java**, povolili **automatické škálování rozvržení** a naučili se **konfigurovat režim plátna** pro výstupy vysoké kvality. Tento tutoriál poskytuje pevný základ pro vaše projekty konverze CAD. Prozkoumejte další funkce a možnosti v [dokumentaci Aspose.CAD](https://reference.aspose.com/cad/java/).

---

**Poslední aktualizace:** 2026-02-15  
**Testováno s:** Aspose.CAD for Java 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}