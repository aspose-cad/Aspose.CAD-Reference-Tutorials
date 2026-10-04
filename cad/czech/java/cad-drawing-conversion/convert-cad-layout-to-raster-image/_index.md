---
date: 2026-10-04
description: Zjistěte, jak rychle převést DWG na PNG a exportovat CAD jako PNG nebo
  jiné rastrové formáty pomocí Aspose.CAD for Java. Získejte vysoce kvalitní výsledky
  rychle.
keywords:
- convert dwg to png
- dwg to raster image
- convert cad to pdf
- export cad as png
- convert dwg to jpeg
lastmod: 2026-10-04
linktitle: Převod rozvržení CAD na rastrový obrazový formát
og_description: Rychle převádějte DWG na PNG pomocí Aspose.CAD for Java. Naučte se
  krok za krokem, jak exportovat CAD jako PNG, JPEG, TIFF a další.
og_image_alt: 'Developer guide: Convert DWG to PNG and other raster formats using
  Aspose.CAD for Java'
og_title: Převod DWG na PNG a další rastrové formáty pomocí Aspose.CAD for Java
schemas:
- author: Aspose
  dateModified: '2026-10-04'
  description: Learn how to quickly convert dwg to png and export cad as png or other
    raster formats using Aspose.CAD for Java. Get high‑quality results fast.
  headline: Convert DWG to PNG and other raster formats using Aspose.CAD for Java
  type: TechArticle
- description: Learn how to quickly convert dwg to png and export cad as png or other
    raster formats using Aspose.CAD for Java. Get high‑quality results fast.
  name: Convert DWG to PNG and other raster formats using Aspose.CAD for Java
  steps:
  - name: set up the resource directory
    text: Replace `"Your Document Directory"` with the absolute path where your CAD
      files reside. This directory will be used for both input and output files.
  - name: load the CAD file
    text: '`Image.load` parses the source file and creates an in‑memory representation
      that you can rasterize. You can load any supported format (DWG, DXF, DGN, etc.)
      – this is the **how to convert cad** part.'
  - name: configure rasterization options
    text: '`CadRasterizationOptions` defines how the vector data is turned into pixels.
      `setPageWidth` and `setPageHeight` control output resolution (larger values
      = higher DPI). `setLayouts` lets you **convert CAD to raster** for specific
      layouts; omit it to rasterize the whole drawing.'
  - name: set image options
    text: '`TiffOptions` (or `PngOptions` for PNG) tells Aspose which raster format
      to generate and lets you fine‑tune compression, color depth, and other format‑specific
      settings. Choose the options class that matches your desired output.'
  - name: save the resultant image
    text: Call `save` on the `Image` instance, passing the output file name and the
      options object. Change the file extension to `.png` (and use `PngOptions`) to
      **save CAD as PNG**. The same pattern works for JPEG, BMP, or PDF. > **Common
      pitfall:** Forgetting to match the file extension with the options cla
  type: HowTo
- questions:
  - answer: Yes, it supports over 30 CAD and raster formats, including DWG, DXF, DGN,
      and SVG.
    question: Is Aspose.CAD compatible with different CAD file formats?
  - answer: Absolutely. Adjust `setPageWidth`, `setPageHeight`, or `setResolution`
      in `CadRasterizationOptions` to achieve the desired DPI.
    question: Can I customize the resolution of the output raster image?
  - answer: Provide an array with all layout names to `setLayouts`, e.g., `new String[]{"Model","Layout1","Layout2"}`.
    question: How can I convert multiple CAD layouts in a single run?
  - answer: Yes—PNG, JPEG, BMP, PDF, and more are available via their respective `*Options`
      classes.
    question: Are there output formats besides TIFF supported?
  - answer: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for community
      support and official assistance.
    question: Where can I get help or share my experience with Aspose.CAD?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- convert dwg
- Aspose.CAD
- Java raster conversion
- CAD image processing
title: Převod DWG na PNG a další rastrové formáty pomocí Aspose.CAD for Java
url: /cs/java/cad-drawing-conversion/convert-cad-layout-to-raster-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Převod DWG na PNG a další rastrové formáty pomocí Aspose.CAD pro Java

## Úvod

`Aspose.CAD for Java` je knihovna, která umožňuje programový převod CAD souborů na rastrové obrázky, jako jsou PNG, JPEG a TIFF. Převod DWG na PNG (nebo jiné rastrové formáty obrázků) je běžná potřeba, když potřebujete sdílet CAD výkresy s kolegy, kteří nemají CAD prohlížeč, vložit návrhy do dokumentace nebo generovat miniatury pro webové galerie. V tomto průvodci se naučíte, jak rychle a spolehlivě převést dwg na png, ať už pracujete s kompletním výkresem nebo jen s konkrétním rozvržením. Můžete také potřebovat **convert CAD to raster** pro webové náhledy, nástroje pro reportování nebo mobilní aplikace.

## Rychlé odpovědi
- **Která knihovna zpracovává DWG na PNG?** Aspose.CAD for Java poskytuje konverzní motor.  
- **Které rastrové formáty mohu exportovat?** PNG, JPEG, TIFF, PDF, BMP a více než 30 dalších formátů.  
- **Potřebuji licenci pro testování?** Bezplatná zkušební verze funguje pro vývoj; pro produkci je vyžadována komerční licence.  
- **Mohu vybrat konkrétní rozvržení?** Ano – použijte `setLayouts` k cílení na „Model“, „Layout1“ atd.  
- **Je možné výstup s vysokým rozlišením?** Rozhodně – upravte `setPageWidth` a `setPageHeight` (nebo `setResolution`) pro kontrolu DPI.

## Co je „convert dwg to png“?

Převod dwg na png znamená transformaci vektorového výkresu DWG na pixelový PNG obrázek, který lze zobrazit v libovolném standardním prohlížeči obrázků. Tento proces rasterizuje vektorové entity, zachovává tloušťku čar, barvy a vrstvy a převádí je do bitmapy s pevně daným rozlišením. Výsledek je ideální pro vložení do PDF, Word dokumentů nebo webových stránek, kde je podpora vektorů omezená.

## Proč exportovat CAD jako PNG (nebo jiné rastrové formáty)?

Export CAD jako PNG poskytuje univerzální kompatibilitu, rychlé načítání a snadné vložení napříč všemi hlavními platformami. Rastrové obrázky se načítají okamžitě ve srovnání s otevíráním těžkého DWG souboru a PNG nabízí bezztrátovou kompresi, která zachovává vizuální věrnost. Kontrolou rozlišení, barvy pozadí a rozvržení zajistíte, že každý stakeholder vidí stejný vzhled, ať už je soubor zobrazen na desktopu, mobilním zařízení nebo v prohlížeči.

## Běžné případy použití

| Scénář | Proč pomáhá rasterový výstup |
|----------|------------------------|
| **Projektová dokumentace** | Vkládání PNG do PDF nebo Word dokumentů eliminuje potřebu CAD softwaru pro recenzenty. |
| **Webové portály** | Miniatury generované z DWG souborů se načítají okamžitě a zlepšují uživatelský zážitek. |
| **Mobilní aplikace** | Rastrové obrázky se zobrazují správně na zařízeních, která nemají CAD prohlížeče. |
| **Automatizované reportování** | Dávkový převod více rozvržení na PNG/JPEG pro zahrnutí do grafů nebo dashboardů. |

## Předpoklady

1. **Java vývojové prostředí** – nainstalovaný a nakonfigurovaný JDK 8 nebo novější.  
2. **Aspose.CAD for Java** – Stáhněte nejnovější JAR z [Aspose.CAD for Java documentation](https://reference.aspose.com/cad/java/).  

## Import jmenných prostorů

`com.aspose.cad.Image` je hlavní třída, která představuje libovolný CAD soubor v paměti. `com.aspose.cad.imageoptions.*` poskytuje objekty možností pro každý rastrový formát. Importujte třídy, které budete potřebovat k načtení výkresu, konfiguraci rasterizace a uložení výstupu.

> **Pro tip:** Pokud plánujete **export CAD jako PNG** místo TIFF, nahraďte `TiffOptions` za `PngOptions` (nalezeno v `com.aspose.cad.imageoptions.PngOptions`).

## Průvodce krok za krokem

### Krok 1: nastavení adresáře zdrojů

Nahraďte `"Your Document Directory"` absolutní cestou, kde se nacházejí vaše CAD soubory. Tento adresář bude použit jak pro vstupní, tak pro výstupní soubory.

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

### Krok 2: načtení CAD souboru

`Image.load` analyzuje zdrojový soubor a vytvoří v‑paměti reprezentaci, kterou můžete rasterizovat. Můžete načíst jakýkoli podporovaný formát (DWG, DXF, DGN atd.) – to je část **how to convert cad**.

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";
```

### Krok 3: konfigurace možností rasterizace

`CadRasterizationOptions` určuje, jak jsou vektorová data převedena na pixely. `setPageWidth` a `setPageHeight` řídí rozlišení výstupu (větší hodnoty = vyšší DPI). `setLayouts` vám umožňuje **convert CAD to raster** pro konkrétní rozvržení; pokud jej vynecháte, rasterizuje se celý výkres.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

### Krok 4: nastavení možností obrázku

`TiffOptions` (nebo `PngOptions` pro PNG) určuje Aspose, který rastrový formát má generovat, a umožňuje jemně doladit kompresi, barevnou hloubku a další nastavení specifická pro formát. Vyberte třídu možností, která odpovídá požadovanému výstupu.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1200);
rasterizationOptions.setPageHeight(1200);
rasterizationOptions.setLayouts(new String[] {"Model", "Layout1"});
```

### Krok 5: uložení výsledného obrázku

Zavolejte `save` na instanci `Image`, předáte název výstupního souboru a objekt možností. Změňte příponu souboru na `.png` (a použijte `PngOptions`) pro **save CAD as PNG**. Stejný postup funguje pro JPEG, BMP nebo PDF.

```java
ImageOptionsBase options = new TiffOptions(TiffExpectedFormat.Default);
options.setVectorRasterizationOptions(rasterizationOptions);
```

> **Častý úskalí:** Zapomenutí sladit příponu souboru s třídou možností způsobí `UnsupportedFormatException`. Vždy je udržujte v souladu.

## Běžné problémy a řešení

| Problém | Řešení |
|-------|----------|
| **Prázdný výstupní obrázek** | Ověřte, že názvy rozvržení v `setLayouts` přesně odpovídají těm ve zdrojovém CAD souboru. |
| **Nízká rozlišení PNG** | Zvyšte `setPageWidth` / `setPageHeight` nebo nastavte `setResolution` v možnostech rasterizace. |
| **Není podporována verze DWG** | Ujistěte se, že používáte nejnovější verzi Aspose.CAD; starší verze nemusí podporovat novější verze DWG. |
| **Chyby paměti u velkých souborů** | Zpracovávejte stránky po jedné nebo zvyšte haldu JVM (`-Xmx2g`). |

## Často kladené otázky

**Q: Je Aspose.CAD kompatibilní s různými CAD formáty souborů?**  
A: Ano, podporuje více než 30 CAD a rastrových formátů, včetně DWG, DXF, DGN a SVG.

**Q: Mohu přizpůsobit rozlišení výstupního rastrového obrázku?**  
A: Rozhodně. Upravením `setPageWidth`, `setPageHeight` nebo `setResolution` v `CadRasterizationOptions` dosáhnete požadovaného DPI.

**Q: Jak mohu převést více CAD rozvržení v jednom běhu?**  
A: Poskytněte pole se všemi názvy rozvržení do `setLayouts`, např. `new String[]{"Model","Layout1","Layout2"}`.

**Q: Existují výstupní formáty kromě TIFF podporované?**  
A: Ano – PNG, JPEG, BMP, PDF a další jsou dostupné prostřednictvím jejich odpovídajících `*Options` tříd.

**Q: Kde mohu získat pomoc nebo sdílet své zkušenosti s Aspose.CAD?**  
A: Navštivte [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) pro komunitní podporu a oficiální asistenci.

## Závěr

Postupným dodržením těchto kroků můžete **convert DWG to PNG**, **export CAD as PNG**, **save CAD as JPEG**, nebo vygenerovat jakýkoli jiný rastrový formát, který potřebujete. Aspose.CAD for Java provádí těžkou práci, což vám umožní soustředit se na integraci vysoce kvalitních obrázků do vašich aplikací, dokumentace nebo webových portálů. Podpora knihovny pro více než 30 formátů a schopnost renderovat stovky stránek výkresu bez načítání celého souboru do paměti z ní činí robustní volbu pro podnikovou rasterizaci CAD.

---

**Poslední aktualizace:** 2026-10-04  
**Testováno s:** Aspose.CAD for Java 24.12  
**Autor:** Aspose  







```java
image.save(dataDir + "conic_pyramid_layoutstorasterimage_out_.tiff", options);
```

```bash
java -jar aspose-cad.jar -i input.dwg -o output.png -w 1200 -h 1200
```

## Související tutoriály

- [Rychlý export DWG do PDF nebo rastrového formátu pomocí java CAD knihovny Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [Převod DWG na BMP pomocí Aspose.CAD for Java](/cad/java/cad-export-options/export-to-bmp/)
- [Export DWG do PDF: konkrétní rozvržení pomocí Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}