---
date: 2026-01-04
description: Naučte se, jak **uložit CAD jako PNG** a snadno exportovat OLE objekty
  z CAD souborů pomocí Aspose.CAD pro Javu. Rychlé nastavení, kompletní ukázkový kód
  a tipy na osvědčené postupy.
linktitle: Export OLE Objects from CAD
second_title: Aspose.CAD Java API
title: Uložte CAD jako PNG a exportujte OLE objekty pomocí Aspose.CAD pro Javu
url: /cs/java/cad-to-pdf-and-svg-export-options/export-ole-objects-from-cad/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Uložte CAD jako PNG a exportujte OLE objekty pomocí Aspose.CAD pro Java

## Úvod

Ve rychle se vyvíjejícím světě počítačově podporovaného navrhování (CAD) může schopnost **save CAD as PNG** a zároveň extrahovat vložené OLE (Object Linking and Embedding) objekty dramaticky zjednodušit váš pracovní postup. Ať už vytváříte nástroj pro hromadnou konverzi, generujete miniatury pro webový portál, nebo jen potřebujete archivovat OLE obsah, Aspose.CAD pro Java vám poskytuje čistý programový způsob, jak to provést. V tomto tutoriálu projdeme celý proces, od nastavení projektu až po export každého OLE objektu jako PNG obrázku.

## Rychlé odpovědi
- **Mohu exportovat OLE objekty přímo do PNG?** Ano – Aspose.CAD načte CAD soubor a umožní vám rasterizovat každý layout do PNG.  
- **Jaká verze Javy je vyžadována?** Java 8 nebo novější.  
- **Potřebuji licenci pro tuto funkci?** Bezplatná zkušební verze funguje pro hodnocení; licence je vyžadována pro produkci.  
- **Zůstane vektorová data zachována?** PNG rasterizace zachovává vizuální věrnost, ale výstup je raster, ne vektor.  
- **Je podporáno hromadné zpracování?** Rozhodně – iterujte přes pole souborů, jak je ukázáno v ukázkovém kódu.

## Požadavky

- **Java Development Kit (JDK)** – Java 8+ nainstalována a nakonfigurována.  
- **Aspose.CAD for Java** – Stáhněte si nejnovější knihovnu z [download link](https://releases.aspose.com/cad/java/).  
- **CAD zdrojové soubory** – Jakékoli DWG/DXF/DGN soubory, které obsahují OLE objekty, jež chcete exportovat.

## Importujte jmenné prostory

Pro práci s CAD soubory musíte importovat základní třídy Aspose.CAD. Zachovejte blok importu přesně tak, jak je zobrazen – poskytuje třídy použité později v tutoriálu.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

## Jak uložit CAD jako PNG

Níže je stručný, krok za krokem průvodce, který ukazuje **jak exportovat OLE objekty a uložit CAD jako PNG**. Každý krok obsahuje krátké vysvětlení následované přesným kódem, který musíte zkopírovat do svého projektu.

### Krok 1: Nastavte adresář dokumentů

Definujte složku, která obsahuje vaše CAD výkresy. Nahraďte zástupný text skutečnou cestou na vašem počítači.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

### Krok 2: Definujte názvy CAD souborů

Uveďte každý CAD soubor, který chcete zpracovat. Můžete přidat tolik položek, kolik potřebujete.

```java
String[] files = new String[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

### Krok 3: Nastavte možnosti exportu PNG

Nastavte parametry rasterizace. Zde cílíme na konkrétní layout (`Layout1`) a používáme výchozí PNG možnosti.

```java
PngOptions pngOptions = new PngOptions();
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.setVectorRasterizationOptions(rasterizationOptions);
rasterizationOptions.setLayouts(new String[] { "Layout1" });
```

### Krok 4: Procházejte CAD soubory a uložte jako PNG

Načtěte každý CAD soubor, rasterizujte OLE objekty a zapište výstupní PNG soubor. Přípona `_out.png` vám pomůže identifikovat vygenerované obrázky.

```java
for(String file : files)
{
    CadImage cadImage = (CadImage)Image.load(dataDir + file);
    cadImage.save(dataDir + file + "_out.png", pngOptions);
}
```

## Časté problémy a řešení

| Problém | Proč se stane | Oprava |
|---------|----------------|-----|
| **`Image.load` throws `FileNotFoundException`** | Cesta `dataDir` je nesprávná nebo název souboru obsahuje překlep. | Zkontrolujte řetězec adresáře a ujistěte se, že názvy souborů přesně odpovídají, včetně mezer. |
| Output PNG is blank | Název layoutu neexistuje ve zdrojovém CAD souboru. | Použijte `cadImage.getLayouts()` k vypsání dostupných layoutů a poté aktualizujte `rasterizationOptions.setLayouts(...)`. |
| Large CAD files cause OutOfMemoryError | Rasterizace obrázků s vysokým rozlišením spotřebuje hodně paměti heap. | Zvyšte heap JVM (`-Xmx2g`) nebo snižte rozlišení rasterizace pomocí `rasterizationOptions.setResolution(...)`. |

## Často kladené otázky

### Q1: Je Aspose.CAD kompatibilní se všemi CAD formáty souborů?

**A1:** Aspose.CAD podporuje různé CAD formáty, včetně DWG, DXF a DGN. Kompletní seznam najdete v [documentation](https://reference.aspose.com/cad/java/).

### Q2: Mohu přizpůsobit nastavení exportu pro OLE objekty?

**A2:** Ano, Aspose.CAD poskytuje rozsáhlé možnosti pro přizpůsobení nastavení exportu, což vám umožní přizpůsobit výstup vašim konkrétním požadavkům.

### Q3: Je k dispozici bezplatná zkušební verze Aspose.CAD?

**A3:** Ano, můžete prozkoumat možnosti Aspose.CAD získáním bezplatné zkušební verze [zde](https://releases.aspose.com/).

### Q4: Kde mohu získat komunitní podporu pro Aspose.CAD?

**A4:** Připojte se ke komunitě Aspose.CAD na [forum](https://forum.aspose.com/c/cad/19), kde můžete požádat o pomoc a sdílet své zkušenosti.

### Q5: Jak mohu zakoupit licenci pro Aspose.CAD?

**A5:** Navštivte [purchase page](https://purchase.aspose.com/buy) a získejte licenci, která vyhovuje vašim vývojářským potřebám.

## Závěr

Po provedení těchto pěti jednoduchých kroků můžete **save CAD as PNG** a extrahovat každý vložený OLE objekt pomocí několika řádků Java kódu. Tento přístup je ideální pro hromadné konverze, automatizované reportování nebo jakýkoli scénář, kde potřebujete rastrové obrázky CAD obsahu bez ručního exportu. Klidně experimentujte s různými možnostmi rasterizace, aby odpovídaly vašim požadavkům na kvalitu a výkon.

---

**Poslední aktualizace:** 2026-01-04  
**Testováno s:** Aspose.CAD for Java 24.12 (latest at time of writing)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}