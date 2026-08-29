---
date: 2026-06-19
description: Naučte se, jak nastavit časový limit při ukládání CAD výkresů s Aspose.CAD
  pro Java. Zvyšte výkon, vyhněte se zablokování a efektivně exportujte CAD do PDF.
keywords:
- how to set timeout
- convert dwg to pdf
- export cad to pdf
linktitle: Nastavit časový limit při ukládání
schemas:
- author: Aspose
  dateModified: '2026-06-19'
  description: Learn how to set timeout on saving CAD drawings with Aspose.CAD for
    Java. Boost performance, avoid hangs, and export CAD to PDF efficiently.
  headline: How to Set Timeout on Save for CAD with Aspose.CAD
  type: TechArticle
- description: Learn how to set timeout on saving CAD drawings with Aspose.CAD for
    Java. Boost performance, avoid hangs, and export CAD to PDF efficiently.
  name: How to Set Timeout on Save for CAD with Aspose.CAD
  steps:
  - name: Set Source and Output Directories
    text: Ensure you have the correct source and output directories for your CAD drawings.
  - name: Create Interruption Token Source
    text: Initialize an interruption token source to manage interruptions during the
      save operation.
  - name: Load CAD Drawing
    text: The `CadImage` class is Aspose.CAD's core object that represents a CAD drawing
      in memory, offering methods for rendering and conversion.
  - name: Configure Rasterization Options
    text: '`CadRasterizationOptions` specifies how the CAD drawing is rasterized into
      an image. Configure rasterization options for the CAD drawing.'
  - name: Configure PDF Options
    text: '`PdfOptions` defines settings for saving a CAD drawing as a PDF document.
      Set up PDF options with vector rasterization options and the interruption token.'
  - name: Save Drawing with Timeout
    text: Save the CAD drawing to a PDF file with the specified timeout.
  - name: Handle Interruption
    text: '`OperationCanceledException` is thrown when a save operation exceeds the
      specified timeout. Create a thread to handle the save operation and interrupt
      it after a specified timeout.'
  type: HowTo
- questions:
  - answer: Yes, wrap each conversion in its own thread with a separate interruption
      token to enforce per‑file time limits.
    question: Can I use this feature to convert DWG to PDF in a batch job?
  - answer: The timeout mechanism is tied to the `InterruptionTokenSource` and works
      with any format that respects the token, including PDF, PNG, and SVG.
    question: Does the timeout work on all output formats?
  - answer: Aspose.CAD automatically discards incomplete output, so you won’t end
      up with corrupted PDFs.
    question: What happens to partially written files after a timeout?
  - answer: Yes, a valid Aspose.CAD license is required for commercial deployments;
      a free trial is available for evaluation.
    question: Is a license required for production use?
  - answer: The official Aspose.CAD documentation provides additional code snippets
      and best‑practice guidelines.
    question: Where can I find more examples of using interruption tokens?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Jak nastavit časový limit při ukládání pro CAD s Aspose.CAD
url: /cs/java/other-cad-operations/put-timeout-on-save/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak nastavit časový limit při ukládání pro CAD s Aspose.CAD

## Úvod

V tomto komplexním průvodci se naučíte **jak nastavit časový limit** při ukládání CAD výkresů pomocí Aspose.CAD pro Java. Použití časového limitu zabraňuje dlouho běžícím operacím ukládání, aby zablokovaly vaši aplikaci, což je zvláště důležité, když potřebujete **exportovat CAD do PDF** nebo **převést DWG do PDF** ve scénářích dávkového zpracování. Aspose.CAD pro Java podporuje více než 50 CAD formátů a dokáže zpracovat soubory s několika stovkami stránek, aniž by načítal celý dokument do paměti, což vám poskytuje předvídatelný výkon a využití zdrojů.

## Rychlé odpovědi
- **Co dělá časový limit?** Přeruší operaci ukládání po uplynutí určené doby, uvolní vlákno a zabrání únikům zdrojů.  
- **Která třída řídí časový limit?** `InterruptionTokenSource` poskytuje token pro zrušení používaný ukládací rutinou.  
- **Mohu stále exportovat CAD do PDF po uplynutí časového limitu?** Ano – můžete zachytit výjimku přerušení a znovu ji provést nebo zaznamenat selhání.  
- **Potřebuji speciální licenci?** Běžná licence Aspose.CAD stačí; funkce časového limitu je vestavěná.  
- **Je tento přístup bezpečný pro vlákna?** Ano, pokud každé ukládání běží ve svém vlastním vlákně s vlastním tokenem.

## Co je časový limit v operacích ukládání CAD?
Časový limit je konfigurovatelný časový limit, který po překročení vynutí zastavení procesu ukládání a vyvolá výjimku přerušení. To chrání vaši Java aplikaci před neomezeným zablokováním způsobeným složitými výkresy nebo úzkými místy I/O.

## Proč nastavit časový limit při ukládání CAD souborů?
Aspose.CAD může **převést DWG do PDF** a **exportovat CAD do PDF** za méně než sekundu pro typické výkresy, ale extrémně velké nebo poškozené soubory mohou trvat minuty. Definováním časového limitu zajistíte, že žádné jednotlivé ukládání nepřesáhne například 30 sekund, což udržuje stabilní propustnost dávky a zabraňuje nedostatku vláken.

## Požadavky

Before diving into the tutorial, make sure you have the following prerequisites in place:
- **Aspose.CAD for Java Library** – Ujistěte se, že máte knihovnu Aspose.CAD pro Java integrovánu ve svém projektu. Knihovnu můžete stáhnout z [webové stránky](https://releases.aspose.com/cad/java/).
- **Vývojové prostředí** – Nastavte své Java vývojové prostředí se všemi potřebnými nástroji a závislostmi.

## Import balíčků

To get started, import the required packages into your Java project. Add the following lines at the beginning of your Java file:

```java
import com.aspose.cad.Image;
import com.aspose.cad.InterruptionTokenSource;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.concurrent.TimeUnit;
```

Nyní rozdělíme ukázkový kód na krok‑za‑krokem instrukce:

## Jak nastavit časový limit při ukládání CAD výkresů?

Načtěte svůj CAD soubor, vytvořte `InterruptionTokenSource` s požadovaným časovým limitem a předávejte token do možností ukládání PDF. Pokud operace překročí časový limit, Aspose.CAD vyhodí `OperationCanceledException`, kterou můžete zachytit a elegantně ošetřit selhání.

### Krok 1: Nastavte zdrojové a výstupní adresáře

```java
final String SourceDir = Utils.getDataDir_DWGDrawings();
final String OutputDir = Utils.getDataDir_Output();
```

Ujistěte se, že máte správné zdrojové a výstupní adresáře pro své CAD výkresy.

### Krok 2: Vytvořte zdroj tokenu přerušení

```java
final InterruptionTokenSource source = new com.aspose.cad.InterruptionTokenSource();
```

Inicializujte zdroj tokenu přerušení pro správu přerušení během operace ukládání.

### Krok 3: Načtěte CAD výkres

`CadImage` třída je jádrový objekt Aspose.CAD, který představuje CAD výkres v paměti a nabízí metody pro vykreslování a konverzi.

```java
final CadImage cadImageBig = (CadImage)Image.load(SourceDir + "Drawing11.dwg");
```

### Krok 4: Nakonfigurujte možnosti rasterizace

`CadRasterizationOptions` určuje, jak je CAD výkres rasterizován do obrázku.

```java
CadRasterizationOptions rasterizationOptionsBig = new CadRasterizationOptions();
rasterizationOptionsBig.setPageWidth(cadImageBig.getSize().getWidth() / 2);
rasterizationOptionsBig.setPageHeight(cadImageBig.getSize().getHeight() / 2);
```

Nakonfigurujte možnosti rasterizace pro CAD výkres.

### Krok 5: Nakonfigurujte PDF možnosti

`PdfOptions` definuje nastavení pro uložení CAD výkresu jako PDF dokument.

```java
final PdfOptions CADfBig = new PdfOptions();
CADfBig.setVectorRasterizationOptions(rasterizationOptionsBig);
CADfBig.setInterruptionToken(source.getToken());
```

Nastavte PDF možnosti s vektorovými možnostmi rasterizace a tokenem přerušení.

### Krok 6: Uložte výkres s časovým limitem

```java
cadImageBig.save(OutputDir + "PutTimeoutOnSave_out.pdf", CADfBig);
```

Uložte CAD výkres do PDF souboru s určeným časovým limitem.

### Krok 7: Ošetřete přerušení

`OperationCanceledException` je vyvolána, když operace ukládání překročí určený časový limit.

```java
java.lang.Thread thread = new java.lang.Thread(new Runnable() {
    @Override
    public void run() {
        try {
            cadImageBig.save(OutputDir + "PutTimeoutOnSave_out.pdf", CADfBig);
        } catch (Throwable th) {
            System.out.println("interrupted !!!");
        }
    }
});
thread.start();
TimeUnit.SECONDS.sleep(3);
source.interrupt();
thread.join();
```

Vytvořte vlákno pro provedení operace ukládání a přerušte jej po uplynutí určeného časového limitu.

## Časté problémy a řešení

- **Časový limit je příliš krátký** – Pokud dostáváte častá přerušení, zvyšte hodnotu časového limitu, aby vyhovovala větším výkresům.  
- **InterruptedException není zachycena** – Vždy obalte volání ukládání do try‑catch bloku pro `OperationCanceledException`, aby se zabránilo zhroucení aplikace.  
- **Spotřeba paměti** – Použijte `PdfOptions.setVectorRasterizationOptions` pro streamování výstupu místo načítání celého souboru do paměti.

## Často kladené otázky

**Q: Mohu tuto funkci použít k převodu DWG do PDF ve dávkovém úkolu?**  
A: Ano, zabalte každý převod do vlastního vlákna s odděleným tokenem přerušení, aby se vynutily časové limity na soubor.

**Q: Funguje časový limit na všech výstupních formátech?**  
A: Mechanismus časového limitu je svázán s `InterruptionTokenSource` a funguje s jakýmkoli formátem, který token respektuje, včetně PDF, PNG a SVG.

**Q: Co se stane s částečně zapsanými soubory po uplynutí časového limitu?**  
A: Aspose.CAD automaticky zahodí neúplný výstup, takže nebudete mít poškozené PDF soubory.

**Q: Je licence vyžadována pro produkční použití?**  
A: Ano, platná licence Aspose.CAD je vyžadována pro komerční nasazení; k dispozici je bezplatná zkušební verze pro hodnocení.

**Q: Kde mohu najít více příkladů použití tokenů přerušení?**  
A: Oficiální dokumentace Aspose.CAD poskytuje další ukázky kódu a osvědčené postupy.

## Další zdroje

- [stránka vydání](https://releases.aspose.com/cad/java/) – Přímá stránka pro stažení nejnovějších vydání Aspose.CAD pro Java.  
- [dokumentace](https://reference.aspose.com/cad/java/) – Kompletní reference API a vývojářské příručky.  
- [tento odkaz](https://releases.aspose.com/) – Obecná vydání produktů Aspose.  
- [zde](https://purchase.aspose.com/temporary-license/) – Získat dočasnou licenci pro testování.  
- [Aspose.CAD fórum](https://forum.aspose.com/c/cad/19) – Podpora komunity a diskuse.

## Závěr

Nyní jste zvládli **jak nastavit časový limit** pro ukládání CAD výkresů s Aspose.CAD pro Java. Integrací `InterruptionTokenSource` do vašeho pracovního postupu můžete spolehlivě **exportovat CAD do PDF** nebo **převést DWG do PDF** bez rizika dlouhých zablokování, což udržuje vaši aplikaci responzivní a škálovatelnou.

---

**Poslední aktualizace:** 2026-06-19  
**Testováno s:** Aspose.CAD for Java 24.12  
**Autor:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Související tutoriály

- [Export DWG do PDF nebo rastrování pomocí Aspose.CAD pro Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [Export konkrétního DWG rozvržení do PDF pomocí Aspose.CAD pro Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [Převod DWG do PNG a dalších rastrových formátů pomocí Aspose.CAD pro Java](/cad/java/cad-drawing-conversion/convert-cad-layout-to-raster-image/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}