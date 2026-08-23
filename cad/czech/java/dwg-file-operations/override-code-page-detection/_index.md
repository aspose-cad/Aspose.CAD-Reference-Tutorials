---
date: 2026-05-20
description: Zjistěte, jak převést DWG na PDF a přitom přepsat automatickou detekci
  kódové stránky pomocí Aspose.CAD for Java. Obsahuje kroky exportu DWG do PDF, tipy
  na kódování a řešení problémů.
keywords:
- convert dwg pdf
- export dwg to pdf
- Aspose.CAD Java
linktitle: Přepsání automatické detekce kódové stránky v souborech DWG
schemas:
- author: Aspose
  dateModified: '2026-05-20'
  description: Learn how to convert DWG to PDF while overriding automatic code page
    detection using Aspose.CAD for Java. Includes export dwg to pdf steps, encoding
    tips, and troubleshooting.
  headline: Convert DWG to PDF – Override Code Page Detection in Java
  type: TechArticle
- description: Learn how to convert DWG to PDF while overriding automatic code page
    detection using Aspose.CAD for Java. Includes export dwg to pdf steps, encoding
    tips, and troubleshooting.
  name: Convert DWG to PDF – Override Code Page Detection in Java
  steps:
  - name: Set Up the Java Project
    text: Create a Maven or Gradle project and add the Aspose.CAD JAR to the classpath.
      This ensures the IDE can resolve the imported classes and that the runtime can
      locate the library.
  - name: Load the DWG File with a Specified Code Page
    text: Tell Aspose.CAD which encoding to use and whether to attempt recovery of
      malformed CIF/MIF data.
  - name: Export the CAD Image to PDF
    text: With the correct code page applied, you can safely export the drawing. The
      `PdfOptions` object lets you fine‑tune the PDF output (compression, rasterization,
      etc.).
  - name: Verify Success
    text: A simple console message confirms that the process completed without exceptions.
      You can repeat these steps for multiple DWG files, adjusting the source path
      and output name as needed.
  type: HowTo
- questions:
  - answer: It forces Aspose.CAD to use a specific character encoding instead of guessing.
    question: What does “override code page” mean?
  - answer: Yes – after setting the correct code page, you can save the CAD image
      as PDF.
    question: Can I export DWG directly to PDF?
  - answer: '`CodePages.Japanese` and `MifCodePages.Japanese` are the right choices.'
    question: Which encoding works for Japanese text?
  - answer: A commercial license is required; a temporary license is available for
      testing.
    question: Do I need a license for production use?
  - answer: Any recent version that supports `LoadOptions` and `PdfOptions`.
    question: What version of Aspose.CAD is needed?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Převod DWG na PDF – Přepsání detekce kódové stránky v Javě
url: /cs/java/dwg-file-operations/override-code-page-detection/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Převod DWG na PDF – Přepsání detekce kódové stránky v Javě

V tomto komplexním tutoriálu se naučíte **jak převést DWG na PDF** při přepsání automatické detekce kódové stránky, která může poškozovat text. Aspose.CAD pro Java vám poskytuje přesnou kontrolu nad kódováním znaků, což umožňuje obnovit poškozená data CIF/MIF a generovat spolehlivý výstup PDF. Ať už vytváříte dávkový převaděč nebo přidáváte zpracování CAD do větší Java služby, níže uvedené kroky vás provedou celým pracovním postupem – od nastavení projektu až po ověření.

## Rychlé odpovědi
- **Co znamená „přepsání kódové stránky“?** Vynutí, aby Aspose.CAD použil konkrétní kódování znaků místo hádání.
- **Mohu exportovat DWG přímo do PDF?** Ano – po nastavení správné kódové stránky můžete uložit CAD obrázek jako PDF.
- **Které kódování funguje pro japonský text?** `CodePages.Japanese` a `MifCodePages.Japanese` jsou správné volby.
- **Potřebuji licenci pro produkční použití?** Je vyžadována komerční licence; dočasná licence je k dispozici pro testování.
- **Jaká verze Aspose.CAD je potřeba?** Jakákoli recentní verze, která podporuje `LoadOptions` a `PdfOptions`.

## Co je „export CAD do PDF“?
Export CAD do PDF převádí vektorový DWG výkres na univerzálně zobrazitelný PDF dokument s pevnou rozložením. Konverze zachovává všechny geometrické entity, čáry, vrstvy a vložený text, přičemž výkres zploští do formátu, který lze snadno sdílet, tisknout, archivovat nebo vkládat do jiných aplikací bez nutnosti CAD softwaru.

## Proč přepsat automatickou detekci kódové stránky?
Manuální zadání kódové stránky zaručuje, že bajty textu jsou interpretovány správně, čímž se odstraní poškozené znaky, které se často objevují, když automatická detekce Aspose.CAD uhodne nesprávné staré kódování. To je nezbytné pro ne‑latinské skripty, jako jsou japonština, cyrilice nebo arabština, a zajišťuje, že exportované PDF odpovídá původnímu návrhu.

## Požadavky
- **Java vývojové prostředí** – JDK 8+ a vaše preferované IDE.  
- **Aspose.CAD pro Java** – Stáhněte knihovnu z oficiálního webu [zde](https://releases.aspose.com/cad/java/).  
- **Ukázkový soubor DWG** – Použijte poskytnutý `SimpleEntities.dwg` nebo jakýkoli DWG, který potřebujete převést.

## Import balíčků
Třídy `Document`, `LoadOptions` a `PdfOptions` jsou jádrem konverzního procesu.

Třída `Document` představuje CAD výkres v paměti a poskytuje metody pro načtení, manipulaci a uložení souboru v různých formátech.

Třída `LoadOptions` vám umožňuje specifikovat kódovou stránku a možnosti obnovy při načítání souboru DWG.

Třída `PdfOptions` řídí nastavení specifická pro PDF, jako je komprese, rasterizace a metadata.

Ve vašem Java projektu importujte potřebné třídy Aspose.CAD:

```java
import com.aspose.cad.CodePages;
import com.aspose.cad.Image;
import com.aspose.cad.LoadOptions;
import com.aspose.cad.MifCodePages;
import com.aspose.cad.fileformats.cad.CadImage;
```

## Jak převést DWG na PDF s přepsáním kódové stránky?
Načtěte soubor DWG pomocí `LoadOptions` a specifikujte přesnou kódovou stránku, poté zavolejte metodu `save` na výsledném `CadImage` s nakonfigurovanou instancí `PdfOptions`. Tento dvoustupňový přístup zajišťuje, že text je interpretován správně a že generované PDF zachovává věrnost původního výkresu, vrstvy a vektorovou kvalitu.

### Krok 1: Nastavení Java projektu
Vytvořte Maven nebo Gradle projekt a přidejte JAR Aspose.CAD do classpath. Tím zajistíte, že IDE dokáže rozpoznat importované třídy a runtime najde knihovnu.

### Krok 2: Načtení souboru DWG s určenou kódovou stránkou
Sdělte Aspose.CAD, které kódování použít a zda se má pokusit o obnovu poškozených dat CIF/MIF.

```java
String SourceDir = "Your Document Directory";
String dwgPathToFile = SourceDir + "SimpleEntites.dwg";
LoadOptions opts = new LoadOptions();
opts.setSpecifiedEncoding(CodePages.Japanese);
opts.setSpecifiedMifEncoding(MifCodePages.Japanese);
opts.setRecoverMalformedCifMif(false);
CadImage cadImage = (CadImage) Image.load(dwgPathToFile, opts);
```

### Krok 3: Export CAD obrázku do PDF
S aplikovanou správnou kódovou stránkou můžete bezpečně exportovat výkres. Objekt `PdfOptions` vám umožňuje jemně doladit výstup PDF (komprese, rasterizace atd.).

```java
// Perform export or other operations with cadImage
// For example, exporting to PDF
PdfOptions pdfOptions = new PdfOptions();
cadImage.save("output.pdf", pdfOptions);
```

### Krok 4: Ověření úspěchu
Jednoduchá zpráva v konzoli potvrzuje, že proces byl dokončen bez výjimek.

```java
System.out.println("OverrideAutomaticCodePageDetectionDwg executed successfully");
```

Tyto kroky můžete opakovat pro více souborů DWG, podle potřeby upravovat cestu ke zdroji a název výstupu.

## Časté problémy a řešení
- **Stále se objevují špatné znaky:** Zkontrolujte, že `specifiedEncoding` odpovídá kódové stránce původního DWG. V případě potřeby použijte jiný výčet `CodePages`.
- **`NullPointerException` při `cadImage.save`:** Ujistěte se, že soubor DWG se načte správně; ověřte cestu a oprávnění k souboru.
- **Velikost PDF je velká:** Povolit kompresi v `PdfOptions` (např. `pdfOptions.setCompress(true)`) pro snížení velikosti souboru bez ztráty kvality.

## Často kladené otázky

**Q1: Je Aspose.CAD kompatibilní se všemi verzemi souborů DWG?**  
A1: Aspose.CAD podporuje více než 30 verzí DWG, včetně AutoCAD 2018 a starších verzí.

**Q2: Mohu použít Aspose.CAD pro komerční projekty?**  
A2: Ano, pro produkční použití je vyžadována komerční licence. Licenci můžete získat [zde](https://purchase.aspose.com/buy).

**Q3: Existují nějaká omezení ve verzi zdarma?**  
A1: Zkušební verze ukládá omezení velikosti a funkcí; podrobnosti najdete v oficiální dokumentaci.

**Q4: Jak mohu získat podporu pro Aspose.CAD?**  
A4: Navštivte komunitní [Aspose.CAD fórum](https://forum.aspose.com/c/cad/19) pro pomoc a diskuse.

**Q5: Je k dispozici dočasná licence pro testovací účely?**  
A5: Ano, dočasnou licenci lze požádat [zde](https://purchase.aspose.com/temporary-license/).

---

**Poslední aktualizace:** 2026-05-20  
**Testováno s:** Aspose.CAD for Java 24.11 (latest at time of writing)  
**Autor:** Aspose

## Související tutoriály

- [Export DWG do PDF a převod CAD výkresů – Aspose.CAD Java tutoriál](/cad/java/cad-drawing-conversion/)
- [Export konkrétního rozvržení DWG do PDF pomocí Aspose.CAD pro Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [Export DWG do PDF nebo rastru pomocí Aspose.CAD pro Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< blocks/products/products-backtop-button >}}

{{< /blocks/products/pf/main-wrap-class >}}