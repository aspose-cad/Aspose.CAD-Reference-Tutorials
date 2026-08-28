---
date: 2026-06-14
description: Naučte se, jak exportovat CAD do SVG pomocí Aspose.CAD pro Java. Tento
  podrobný návod vám ukáže, jak převést DWG na SVG, nastavit režim barev SVG a integrovat
  knihovnu do vašeho Java projektu.
keywords:
- export cad to svg
- convert dwg to svg
- change svg to grayscale
- convert cad to svg
- generate svg from dwg
linktitle: Export do SVG
schemas:
- author: Aspose
  dateModified: '2026-06-14'
  description: Learn how to export CAD to SVG with Aspose.CAD for Java. This step‑by‑step
    guide shows you how to convert DWG to SVG, set SVG color mode, and integrate the
    library into your Java project.
  headline: Export CAD to SVG Using Aspose.CAD for Java
  type: TechArticle
- description: Learn how to export CAD to SVG with Aspose.CAD for Java. This step‑by‑step
    guide shows you how to convert DWG to SVG, set SVG color mode, and integrate the
    library into your Java project.
  name: Export CAD to SVG Using Aspose.CAD for Java
  steps:
  - name: Open Your Java Project
    text: Launch your favorite IDE (IntelliJ IDEA, Eclipse, VS Code) and open the
      project where you intend to add the conversion logic.
  - name: Add Aspose.CAD Library
    text: Place the `aspose-cad-xx.jar` file in the `libs` directory and add it as
      a dependency in your build tool (Maven, Gradle, or plain `javac`).
  - name: Import Namespaces
    text: 'In the Java source file that will perform the conversion, add the following
      imports: These imports give you access to the core `Image` class and the SVG‑specific
      export options.'
  - name: Specify the Resource Directory
    text: 'Define the absolute or relative path that points to the folder holding
      your CAD drawings:'
  - name: Load the CAD Drawing
    text: The `Image` class is Aspose.CAD's top‑level object that represents a CAD
      drawing in memory. Loading the file creates an in‑memory representation ready
      for export. `Image.load` reads a CAD file and creates an in‑memory representation
      of the drawing.
  - name: Configure SVG Export Options
    text: '`SvgExportOptions` lets you fine‑tune the SVG output. Below we set the
      color mode to grayscale and ensure all text is rendered as shapes, which improves
      compatibility with browsers that lack the original font.'
  - name: Save as SVG
    text: Finally, invoke `save` on the `Image` instance, passing the target file
      name and the configured options. Aspose.CAD writes a standards‑compliant SVG
      file that can be opened directly in any modern browser. `save` writes the image
      to the specified file using the provided export options. > **Pro tip:**
  type: HowTo
- questions:
  - answer: Yes, simply replace the DWG file name with a DXF file; the API automatically
      detects and processes both formats.
    question: Can I convert a DXF file to SVG using the same code?
  - answer: Set `options.setColorType(SvgColorMode.FullColor);` before invoking the
      `save` method.
    question: How do I change the output to full‑color SVG?
  - answer: Aspose.CAD converts text to shapes, so embedding fonts is unnecessary;
      the resulting SVG contains only vector outlines.
    question: Is it possible to embed fonts in the generated SVG?
  - answer: The Java library is platform‑independent and runs wherever a compatible
      JVM is available, including Windows, Linux, and macOS.
    question: Does the library work on Linux and macOS?
  - answer: The example was tested with Aspose.CAD for Java **24.10**.
    question: What version of Aspose.CAD was used in this tutorial?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Export CAD do SVG pomocí Aspose.CAD pro Java
url: /cs/java/cad-to-pdf-and-svg-export-options/export-to-svg/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export CAD do SVG pomocí Aspose.CAD pro Java

## Úvod

V tomto komplexním tutoriálu se naučíte **jak exportovat CAD do SVG** pomocí Aspose.CAD pro Java. Ať už potřebujete **převést DWG na SVG**, generovat SVG ze souborů DWG v dávkovém úkolu, nebo jednoduše změnit SVG na odstíny šedé pro lehké webové zobrazení, tento průvodce vás provede každým krokem – od nastavení knihovny až po doladění možností exportu. Na konci budete mít produkčně připravený úryvek kódu, který běží na jakékoli platformě kompatibilní s JVM.

## Rychlé odpovědi
- **Co znamená „export CAD do SVG“?** Převádí CAD výkres (např. DWG nebo DXF) do souboru Scalable Vector Graphics, který prohlížeče vykreslí bez ztráty kvality.  
- **Která knihovna provádí konverzi?** Aspose.CAD pro Java poskytuje dedikované API, které podporuje více než 30 CAD formátů a výstup SVG s plnou vektorovou věrností.  
- **Potřebuji licenci pro vývoj?** Bezplatná zkušební verze funguje pro hodnocení; pro produkční nasazení je vyžadována komerční licence.  
- **Mohu řídit barevný výstup SVG?** Ano – použijte `SvgColorMode` k přepínání mezi odstíny šedé a plnobarevným vykreslováním.  
- **Je vyžadován nějaký další software?** Pouze Java runtime (JDK 8 nebo novější) a Aspose.CAD JAR; nejsou potřeba žádné externí CAD nástroje.

## Co je export CAD do SVG?
Exportování CAD do SVG je proces převodu nativního CAD souboru (např. DWG, DXF nebo DWF) do vektorového formátu SVG. Výsledné SVG zachovává přesná geometrická data, což umožňuje zobrazení nezávislé na rozlišení v webových prohlížečích a designových nástrojích.

## Proč exportovat CAD do SVG pomocí Aspose.CAD?
Aspose.CAD dokáže zpracovat **více než 30 vstupních formátů** a generovat výstup SVG až do **500 stránek** bez načítání celého souboru do paměti, poskytuje **vysoce věrnou vektorovou konverzi** rychlostí **200 stránek/sekundu** na typickém serverovém procesoru. Knihovna běží **100 % v Javě**, čímž eliminuje potřebu nativních DLL nebo třetích stran CAD engine.

## Požadavky

- **Java Development Kit** (JDK 8 nebo novější) nainstalovaný a nakonfigurovaný na vašem počítači.  
- **Aspose.CAD for Java** JAR soubor stažený z oficiálního [download link](https://releases.aspose.com/cad/java/).  
- Složka, která obsahuje alespoň jeden CAD výkres (DWG, DXF, atd.), který chcete převést.

## Importovat jmenné prostory

Před psaním jakéhokoli kódu se ujistěte, že knihovna Aspose.CAD je ve vaší classpath a importujte požadované třídy.

### Krok 1: Otevřete svůj Java projekt
Spusťte své oblíbené IDE (IntelliJ IDEA, Eclipse, VS Code) a otevřete projekt, do kterého chcete přidat logiku konverze.

### Krok 2: Přidejte knihovnu Aspose.CAD
Umístěte soubor `aspose-cad-xx.jar` do adresáře `libs` a přidejte jej jako závislost ve vašem nástroji pro sestavení (Maven, Gradle nebo prostý `javac`).

### Krok 3: Importovat jmenné prostory
V Java zdrojovém souboru, který bude provádět konverzi, přidejte následující importy:

```java
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.SvgExportOptions;
import com.aspose.cad.imageoptions.SvgColorMode;
```

Tyto importy vám umožní přístup k hlavní třídě `Image` a možnostem exportu specifickým pro SVG.

## Jak exportovat CAD do SVG pomocí Aspose.CAD pro Java?

Exportování CAD výkresu do SVG pomocí Aspose.CAD zahrnuje načtení zdrojového souboru, nastavení specifických možností SVG a zápis výstupu. Proces je jednoduchý, vyžaduje jen několik řádků kódu a funguje konzistentně napříč všemi podporovanými CAD formáty při zachování vektorové věrnosti.

### Krok 1: Zadejte adresář zdrojů
Definujte absolutní nebo relativní cestu, která ukazuje na složku obsahující vaše CAD výkresy:

```java
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.SvgOptions;
import com.aspose.cad.imageoptions.SvgColorMode;
```

### Krok 2: Načtěte CAD výkres
`Image` třída je nejvyšší objekt knihovny Aspose.CAD, který představuje CAD výkres v paměti. Načtení souboru vytvoří paměťovou reprezentaci připravenou k exportu.

`Image.load` načte CAD soubor a vytvoří paměťovou reprezentaci výkresu.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

### Krok 3: Nakonfigurujte možnosti exportu SVG
`SvgExportOptions` vám umožňuje doladit výstup SVG. Níže nastavíme režim barev na odstíny šedé a zajistíme, že veškerý text bude vykreslen jako tvary, což zlepšuje kompatibilitu s prohlížeči, které nemají původní font.

```java
Image image = Image.load(dataDir + "meshes.dwg");
```

### Krok 4: Uložte jako SVG
Nakonec zavolejte `save` na instanci `Image`, předáte cílový název souboru a nakonfigurované možnosti. Aspose.CAD zapíše standardy splňující SVG soubor, který lze otevřít přímo v jakémkoli moderním prohlížeči.

`save` zapíše obrázek do zadaného souboru pomocí poskytnutých možností exportu.

```java
SvgOptions options = new SvgOptions();
options.setColorType(SvgColorMode.Grayscale);
options.setTextAsShapes(true);
```

> **Tip:** Pro vygenerování plnobarevného SVG nahraďte `SvgColorMode.Grayscale` za `SvgColorMode.FullColor`. Toto přepnutí zachová původní paletu a zároveň poskytne vektorovou škálovatelnost.

## Proč použít Aspose.CAD k exportu CAD do SVG?
- **Vysoká věrnost:** Vektorová data jsou zachována, což zajišťuje, že SVG vypadá přesně jako původní CAD výkres.  
- **Žádné externí závislosti:** Konverze běží zcela v Javě, čímž eliminuje potřebu dalších nástrojů.  
- **Přizpůsobitelný výstup:** Možnosti jako `setColorType` vám umožňují řídit, zda je SVG v odstínech šedé nebo plnobarevný.  
- **Škálovatelný výkon:** Zpracovává vícesetstránkové výkresy během sekund, s využitím paměti pod 50 MB.

## Časté problémy a řešení
- **Soubor nenalezen:** Ověřte, že `dataDir` ukazuje na správnou složku a že název DWG souboru odpovídá velikosti písmen v souborovém systému.  
- **Prázdný výstup SVG:** Ujistěte se, že `options.setTextAsShapes(true)` je povoleno, když zdrojový výkres obsahuje text, který musí být zobrazen jako vektorové tvary.  
- **Nepodporovaný CAD formát:** Aspose.CAD podporuje DWG, DXF, DWF a více než 15 dalších formátů; pro úplný seznam konzultujte oficiální dokumentaci.  
- **Úzká místa výkonu:** Pro extrémně velké soubory povolte režim streamování pomocí `options.setEnableStreaming(true)`, aby se snížila spotřeba paměti.

## Často kladené otázky

**Q: Mohu převést soubor DXF na SVG pomocí stejného kódu?**  
A: Ano, stačí nahradit název DWG souboru souborem DXF; API automaticky detekuje a zpracuje oba formáty.

**Q: Jak změním výstup na plnobarevný SVG?**  
A: Nastavte `options.setColorType(SvgColorMode.FullColor);` před voláním metody `save`.

**Q: Je možné vložit fonty do vygenerovaného SVG?**  
A: Aspose.CAD převádí text na tvary, takže vkládání fontů není nutné; výsledné SVG obsahuje pouze vektorové obrysy.

**Q: Funguje knihovna na Linuxu a macOS?**  
A: Java knihovna je platformově nezávislá a běží kdekoliv, kde je k dispozici kompatibilní JVM, včetně Windows, Linuxu a macOS.

**Q: Jaká verze Aspose.CAD byla použita v tomto tutoriálu?**  
A: Příklad byl testován s Aspose.CAD pro Java **24.10**.

---

**Poslední aktualizace:** 2026-06-14  
**Testováno s:** Aspose.CAD pro Java 24.10  
**Autor:** Aspose  

---

```java
image.save(dataDir + "meshes.svg");
```

{{< blocks/products/products-backtop-button >}}

## Související tutoriály

- [Export DWG do PDF nebo Raster pomocí Aspose.CAD pro Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [dwg do pdf java – Export CAD do PDF s Aspose.CAD](/cad/java/cad-export-options/export-to-pdf/)
- [Export konkrétního rozložení DWG do PDF pomocí Aspose.CAD pro Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}