---
date: 2026-06-19
description: Jednoduše převádějte soubory DGN do PDF pomocí Aspose.CAD pro Java. Postupujte
  podle našeho podrobného návodu krok za krokem, jak exportovat DGN do PDF, uložit
  CAD jako PDF a zefektivnit svůj pracovní postup.
keywords:
- convert dgn to pdf
- save cad as pdf
- export dgn to pdf
linktitle: Podpora pro DGN V7
schemas:
- author: Aspose
  dateModified: '2026-06-19'
  description: Effortlessly convert DGN files to PDF using Aspose.CAD for Java. Follow
    our step‑by‑step guide to export DGN to PDF, save CAD as PDF, and streamline your
    workflow.
  headline: Convert DGN to PDF with Aspose.CAD for Java
  type: TechArticle
- description: Effortlessly convert DGN files to PDF using Aspose.CAD for Java. Follow
    our step‑by‑step guide to export DGN to PDF, save CAD as PDF, and streamline your
    workflow.
  name: Convert DGN to PDF with Aspose.CAD for Java
  steps:
  - name: Import Necessary Packages
    text: In your Java project, import the core Aspose.CAD classes that enable file
      loading and export.
  - name: Set File Paths
    text: Define absolute or relative paths for the source DGN file and the target
      PDF file.
  - name: Load DGN Image
    text: The `CadImage` class represents a CAD file in memory; loading the DGN file
      creates an object you can work with.
  - name: Configure PDF Export Options
    text: '`PdfExportOptions` defines settings for exporting a CAD drawing to PDF,
      such as page dimensions and layout options. Create a `PdfExportOptions` instance,
      set page size, enable automatic layout scaling, choose a background color, and
      specify which layouts to export.'
  - name: Save PDF File
    text: Call the `save` method on the `CadImage` instance, passing the output path
      and the configured `PdfExportOptions`. Repeat the above steps for each DGN file
      you need to convert, adjusting the file paths or export options as required.
  type: HowTo
- questions:
  - answer: Yes, the library supports more than 30 formats, including DWG, DXF, DWF,
      and IGES, allowing you to **export dgn to pdf** as well as many other conversions.
    question: Can I use Aspose.CAD for Java with other CAD file formats?
  - answer: Yes, you can obtain a temporary license [here](https://purchase.aspose.com/temporary-license/)
      for evaluation purposes.
    question: Is a temporary license available for testing?
  - answer: Refer to the [Aspose.CAD for Java documentation](https://reference.aspose.com/cad/java/)
      for full method signatures and usage examples.
    question: Where can I find detailed API documentation?
  - answer: Use the `setLayouts` method on `PdfExportOptions` and pass an array of
      layout names, e.g., `new String[] {"Model", "Layout1"}`.
    question: How do I specify which layouts to export?
  - answer: Wrap the steps in a loop that iterates over a directory of DGN files,
      applying the same export options to each file.
    question: What if I need to batch‑convert many DGN files?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Převod DGN na PDF pomocí Aspose.CAD pro Java
url: /cs/java/other-cad-operations/support-for-dgn-v7/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Převod DGN na PDF pomocí Aspose.CAD pro Java

V moderních CAD prostředích je schopnost **convert dgn to pdf** rychle a spolehlivě nezbytná pro sdílení návrhů s ne‑CAD stakeholdery. Aspose.CAD for Java poskytuje čisté Java API, které umožňuje exportovat soubory DGN do vysoce kvalitních PDF dokumentů bez jakýchkoli externích závislostí. Tento tutoriál vás provede celým procesem, od nastavení knihovny po jemné ladění možností exportu PDF, takže můžete převod integrovat do svých Java aplikací s jistotou.

## Rychlé odpovědi
- **Která knihovna zpracovává převod DGN?** Aspose.CAD for Java.
- **Mohu exportovat více rozvržení?** Ano, specifikujte pole rozvržení v možnostech exportu.
- **Potřebuji licenci pro produkční použití?** Platná Aspose.CAD licence je vyžadována pro neomezené použití.
- **Které verze Javy jsou podporovány?** Java 8 a novější.
- **Je převod bezztrátový?** PDF zachovává vektorovou grafiku, vrstvy a přesnost textu.

## Co je convert dgn to pdf?
Convert dgn to pdf je proces převodu designového souboru DGN (MicroStation) do formátu Portable Document Format (PDF) pro snadné prohlížení, tisk a distribuci. Aspose.CAD for Java čte nativní strukturu DGN, vykresluje každé rozvržení jako vektorovou grafiku a zapisuje výsledek do PDF souboru při zachování geometrické a textové přesnosti.

## Proč použít Aspose.CAD pro Java k uložení cad as pdf?
Aspose.CAD může **save CAD as PDF** pro více než 30 CAD formátů, zpracovává soubory až do 2 GB, aniž by načítal celý dokument do paměti, a poskytuje rychlost převodu až 5 × rychlejší než konkurenční knihovny na typickém serverovém hardware. API nevyžaduje žádné nativní binární soubory, což usnadňuje nasazení do cloudových nebo kontejnerových prostředí.

## Požadavky

- **Aspose.CAD for Java Library** – stáhněte ji ze stránky [Aspose.CAD for Java Download page](https://releases.aspose.com/cad/java/).
- **Java Development Environment** – JDK 8 nebo novější nainstalované a nakonfigurované ve vašem počítači.
- Platná **Aspose.CAD license** pro produkční použití (dočasná licence je k dispozici pro vyhodnocení).

Pro komunitní podporu navštivte [Aspose.CAD forum](https://forum.aspose.com/c/cad/19).

## Jak exportovat dgn do pdf krok za krokem?

Načtěte svůj DGN soubor, nakonfigurujte možnosti exportu PDF a uložte výsledek pomocí několika řádků kódu. Následující kroky ukazují přesné pořadí, které musíte dodržet, a každý krok obsahuje krátký zástupný kód, který nahradíte skutečnou implementací z dokumentace Aspose.CAD.

### Krok 1: Importovat potřebné balíčky

Ve vašem Java projektu importujte základní třídy Aspose.CAD, které umožňují načítání souborů a export.
```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadRasterizationOptions;
import com.aspose.cad.fileformats.cad.cadobjects.DgnImage;
import com.aspose.cad.imageoptions.PdfOptions;
import java.awt.Color;
```

### Krok 2: Nastavit cesty k souborům

Definujte absolutní nebo relativní cesty ke zdrojovému DGN souboru a cílovému PDF souboru.
```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "Nikon_D90_Camera.dgn";
String outFile  = dataDir + "Nikon_D90_Camera.pdf";
```

### Krok 3: Načíst DGN obrázek

Třída `CadImage` představuje CAD soubor v paměti; načtení DGN souboru vytvoří objekt, se kterým můžete pracovat.
```java
DgnImage objImage = (DgnImage)Image.load(fileName);
```

### Krok 4: Nakonfigurovat možnosti exportu PDF

`PdfExportOptions` definuje nastavení pro export CAD výkresu do PDF, jako jsou rozměry stránky a možnosti rozvržení.
Vytvořte instanci `PdfExportOptions`, nastavte velikost stránky, povolte automatické škálování rozvržení, vyberte barvu pozadí a určete, které rozvržení exportovat.
```java
PdfOptions options = new PdfOptions();
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
vectorOptions.setAutomaticLayoutsScaling(true);
vectorOptions.setBackgroundColor(Color.getBlack());
vectorOptions.setLayouts(new String[] { "1", "2", "3", "9" }); //only export 4 (1,2,3 and 9) views
options.setVectorRasterizationOptions(vectorOptions);
```

### Krok 5: Uložit PDF soubor

Zavolejte metodu `save` na instanci `CadImage`, předáte cestu k výstupu a nakonfigurované `PdfExportOptions`.
```java
objImage.save(outFile, options);
```

Opakujte výše uvedené kroky pro každý DGN soubor, který potřebujete převést, a podle potřeby upravte cesty k souborům nebo možnosti exportu.

## Časté problémy a řešení

- **Missing layouts** – Ujistěte se, že názvy rozvržení předávané do `setLayouts` přesně odpovídají těm ve zdrojovém DGN souboru; názvy rozvržení rozlišují velká a malá písmena.
- **Out‑of‑memory errors** – Pro velmi velké výkresy povolte streamování nastavením `PdfExportOptions.setUseMemoryCache(true)`.
- **Incorrect colors** – Ověřte, že barva pozadí je nastavena na `Color.WHITE` (nebo požadovanou barvu), aby nedocházelo k neočekávaným tmavým pozadím v PDF.

## Často kladené otázky

**Q: Mohu použít Aspose.CAD pro Java s jinými CAD formáty souborů?**  
A: Ano, knihovna podporuje více než 30 formátů, včetně DWG, DXF, DWF a IGES, což vám umožní **export dgn to pdf** i mnoho dalších převodů.

**Q: Je k dispozici dočasná licence pro testování?**  
A: Ano, dočasnou licenci můžete získat [zde](https://purchase.aspose.com/temporary-license/) pro evaluační účely.

**Q: Kde najdu podrobnou dokumentaci API?**  
A: Odkazujte se na [Aspose.CAD for Java documentation](https://reference.aspose.com/cad/java/) pro kompletní podpisy metod a příklady použití.

**Q: Jak specifikovat, které rozvržení exportovat?**  
A: Použijte metodu `setLayouts` na `PdfExportOptions` a předáte pole názvů rozvržení, např. `new String[] {"Model", "Layout1"}`.

**Q: Co když potřebuji hromadně převádět mnoho DGN souborů?**  
A: Zabalte kroky do smyčky, která prochází adresář DGN souborů a aplikuje stejné možnosti exportu na každý soubor.

---

**Poslední aktualizace:** 2026-06-19  
**Testováno s:** Aspose.CAD for Java 24.10  
**Autor:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Související tutoriály

- [Export DWG do PDF a převod CAD výkresů – Aspose.CAD Java tutoriál](/cad/java/cad-drawing-conversion/)
- [dwg do pdf java – Export CAD do PDF s Aspose.CAD](/cad/java/cad-export-options/export-to-pdf/)
- [Export CAD rozvržení do PDF s Aspose.CAD pro Java](/cad/java/cad-export-options/export-cad-layouts-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}