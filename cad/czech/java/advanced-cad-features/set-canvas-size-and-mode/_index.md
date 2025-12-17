---
date: 2025-12-10
description: Naučte se, jak převést CAD na PDF pomocí Aspose.CAD pro Javu při nastavení
  velikosti plátna, automatického škálování rozvržení a exportu do TIFF.
linktitle: Convert CAD to PDF – Set Canvas Size & Mode
second_title: Aspose.CAD Java API
title: Převést CAD na PDF – Nastavit velikost plátna a režim (Java)
url: /cs/java/advanced-cad-features/set-canvas-size-and-mode/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Nastavení velikosti plátna a režimu

## Úvod

Hledáte **convert CAD to PDF** a chcete mít plnou kontrolu nad velikostí plátna a režimem vykreslování? Tento komplexní průvodce vás provede přesné kroky, jak nastavit velikost plátna v Javě, povolit automatické škálování rozvržení a poté exportovat výsledek do formátů PDF i TIFF pomocí Aspose.CAD. Ať už vylepšujete produkční pipeline nebo experimentujete s prototypem, najdete zde jasné, praktické instrukce.

## Rychlé odpovědi
- **Co znamená “convert CAD to PDF”?** Převod CAD výkresu (např. DXF, DWG) do PDF dokumentu, který lze zobrazit na jakékoli platformě.  
- **Mohu také exportovat do TIFF?** Ano—použijte `TiffOptions` k vytvoření vysoce rozlišených rastrových obrázků.  
- **Která volba řídí velikost plátna v Javě?** `CadRasterizationOptions.setPageWidth/Height`.  
- **Co je automatické škálování rozvržení?** Příznak (`setAutomaticLayoutsScaling(true)`), který zachovává původní proporce rozvržení při změně velikosti plátna.  
- **Potřebuji licenci pro Aspose.CAD?** Pro produkční použití je vyžadována dočasná nebo trvalá licence.

## Co je **convert CAD to PDF**?

Převod CAD do PDF znamená převzetí vektorových technických výkresů a jejich vykreslení jako PDF stránky, přičemž se zachovává čárová práce, vrstvy a geometrie a soubor je zpřístupněn univerzálně.

## Proč nastavit velikost plátna **java**?

Nastavení velikosti plátna v Javě vám umožní definovat výstupní rozlišení a rozměry stránky, což zajišťuje, že výsledné PDF nebo TIFF odpovídá vašim požadavkům na tisk nebo zobrazení. Také vám dává kontrolu nad chováním škálování, což je nezbytné pro výkresy ve velkém formátu.

## Požadavky

Před ponořením se do tutoriálu se ujistěte, že máte následující požadavky připravené:

- Aspose.CAD for Java: Ujistěte se, že máte knihovnu Aspose.CAD nainstalovanou ve vašem Java prostředí. Můžete si ji stáhnout [zde](https://releases.aspose.com/cad/java/).
- Document Directory: Nastavte adresář dokumentů pro uložení vašich CAD souborů. Tento adresář bude odkazován v krocích tutoriálu.

Nyní začněme s krok‑za‑krokem průvodcem.

## Importovat jmenné prostory

V tomto kroku naimportujeme potřebné jmenné prostory pro zahájení vašeho projektu Aspose.CAD.

```java
import java.awt.Image;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## Krok 1: Importovat třídy Aspose.CAD

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
com.aspose.cad.Image objImage = com.aspose.cad.Image.load(srcFile);
```

V tomto úryvku nastavíme cestu k adresáři zdrojů a načteme soubor DXF pomocí třídy `Image` z Aspose.CAD.

## Krok 2: Nastavit vlastnosti **CadRasterizationOptions** (set canvas size java)

```java
// Create an instance of CadRasterizationOptions and set its various properties
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

Zde vytvoříme instanci `CadRasterizationOptions` a nakonfigurujeme vlastnosti jako šířka stránky, výška stránky a **automatic layout scaling**. Toto je jádro **configure canvas mode** pro vaše převody.

## Krok 3: Vytvořit PdfOptions a nastavit VectorRasterizationOptions

```java
// Create an instance of PdfOptions
PdfOptions pdfOptions = new PdfOptions();

// Set the VectorRasterizationOptions property
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Nyní vytvoříme instanci `PdfOptions` a nastavíme její vlastnost `VectorRasterizationOptions` na dříve nakonfigurovaný `CadRasterizationOptions`.

## Krok 4: Export do PDF (convert cad to pdf)

```java
// Export CAD to PDF
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

Nakonec uložíme CAD obrázek do PDF souboru pomocí zadaných možností, čímž dokončíme proces **convert CAD to PDF**.

## Krok 5: Vytvořit TiffOptions a nastavit VectorRasterizationOptions (export cad to tiff)

```java
// Create an instance of TiffOptions
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);

// Set the VectorRasterizationOptions property
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
```

V tomto kroku nastavíme instanci `TiffOptions` a nakonfigurujeme její vlastnost `VectorRasterizationOptions`.

## Krok 6: Export do TIFF

```java
// Export CAD to TIFF
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

Nakonec uložíme CAD obrázek do TIFF souboru pomocí zadaných možností, což demonstruje, jak **export CAD to TIFF** po nastavení velikosti plátna.

## Časté problémy a řešení

| Problém | Příčina | Řešení |
|-------|-------|-----|
| Výstupní PDF je prázdný | `setNoScaling(true)` zakazuje vykreslování u některých výkresů | Odstraňte `setNoScaling(true)` nebo jej nastavte na `false`. |
| Rozlišení TIFF vypadá nízké | Šířka/výška stránky je příliš malá | Zvyšte hodnoty `setPageWidth` / `setPageHeight`. |
| Rozvržení vypadá zkresleně | Automatické škálování rozvržení je vypnuto | Ujistěte se, že `setAutomaticLayoutsScaling(true)` je povoleno. |

## Závěr

Gratulujeme! Úspěšně jste **convert CAD to PDF** a **export CAD to TIFF** při **set canvas size java**, povoleném **automatic layout scaling** a naučili se, jak **configure canvas mode** pro výstupy vysoké kvality. Tento tutoriál poskytuje pevný základ pro vaše projekty převodu CAD. Prozkoumejte další funkce a možnosti v [dokumentaci Aspose.CAD](https://reference.aspose.com/cad/java/).

## Často kladené otázky

### Q1: Můžu použít Aspose.CAD pro Java s jinými Java frameworky?

A1: Ano, Aspose.CAD je navržen tak, aby se bez problémů integroval s různými Java frameworky.

### Q2: Je k dispozici dočasná licence pro Aspose.CAD?

A2: Ano, můžete získat dočasnou licenci [zde](https://purchase.aspose.com/temporary-license/).

### Q3: Kde mohu získat komunitní podporu pro Aspose.CAD?

A3: Navštivte [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) pro komunitní podporu a diskuse.

### Q4: Můžu vyzkoušet Aspose.CAD zdarma?

A4: Rozhodně! Získejte bezplatnou zkušební verzi [zde](https://releases.aspose.com/).

### Q5: Jak mohu zakoupit Aspose.CAD pro Java?

A5: Zakupte produkt [zde](https://purchase.aspose.com/buy).

**Q: Ovlivňuje velikost plátna kvalitu vektoru v PDF?**  
A: Ne. Velikost plátna řídí rozměry stránky; vektorová data zůstávají nezávislá na rozlišení, což zajišťuje ostré vykreslení při libovolném přiblížení.

**Q: Můžu nastavit jinou DPI pro výstup TIFF?**  
A: Ano. Před vytvořením `TiffOptions` upravte `rasterizationOptions.setResolution(dpiValue)`.

---

**Last Updated:** 2025-12-10  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}