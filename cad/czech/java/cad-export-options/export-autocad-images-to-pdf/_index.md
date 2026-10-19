---
date: 2026-10-19
description: Zjistěte, jak exportovat výkresy AutoCAD do PDF s vlastní velikostí stránky
  PDF pomocí Aspose.CAD pro Java. Tento krok‑za‑krokem průvodce pokrývá převod DWG
  do PDF, možnosti rasterizace a licencování.
keywords:
- custom pdf page size
- export autocad to pdf
- save cad as pdf
- generate pdf from dwg
- dwg to pdf java
lastmod: 2026-10-19
linktitle: Exportovat obrázky AutoCAD do PDF
og_description: Nastavte vlastní velikost PDF stránky při exportu výkresů AutoCAD
  do PDF pomocí Aspose.CAD pro Java. Naučte se převod DWG na PDF, nastavení rasterizace
  a licencování během několika minut.
og_image_alt: Guide showing how to export AutoCAD drawings to PDF with custom page
  dimensions using Aspose.CAD for Java
og_title: Nastavte vlastní velikost PDF stránky pro export AutoCAD pomocí Aspose.CAD
schemas:
- author: Aspose
  dateModified: '2026-10-19'
  description: Learn how to export AutoCAD drawings to PDF with a custom PDF page
    size using Aspose.CAD for Java. This step‑by‑step guide covers converting DWG
    to PDF, rasterization options, and licensing.
  headline: Set custom PDF page size for AutoCAD export with Aspose.CAD
  type: TechArticle
- description: Learn how to export AutoCAD drawings to PDF with a custom PDF page
    size using Aspose.CAD for Java. This step‑by‑step guide covers converting DWG
    to PDF, rasterization options, and licensing.
  name: Set custom PDF page size for AutoCAD export with Aspose.CAD
  steps:
  - name: set the resource directory path
    text: '> **Pro tip:** Replace `"Your Document Directory"` with the absolute path
      to the folder you created in the prerequisites.'
  - name: load the CAD image
    text: The `Image` class loads the CAD file and gives you access to Aspose.CAD’s
      rasterization engine. > **Why this matters:** Once the CAD file is loaded, you
      can manipulate rasterization options before rendering to PDF.
  - name: set rasterization options
    text: The `CadRasterizationOptions` class specifies how the CAD drawing is rasterized
      before being saved as PDF. Adjust `pageWidth` and `pageHeight` to define a **custom
      PDF page size**. You can also enable 3‑D rendering by uncommenting the `setTypeOfEntities`
      line. - `pageWidth` / `pageHeight` – measured
  - name: configure PDF options
    text: The `PdfOptions` class holds PDF‑specific settings and links the rasterization
      options to the output file, ensuring the custom page dimensions are applied
      correctly.
  - name: save the PDF
    text: The `save` method writes the rendered image to the specified PDF file. The
      resulting file, `Export3DImagestoPDF_out_.pdf`, is a **save cad as pdf** representation
      of your original AutoCAD drawing with the exact page dimensions you specified.
  type: HowTo
- questions:
  - answer: Yes, the library supports DWG, DXF, DWF, DGN, and many more, giving you
      flexibility across projects.
    question: Can I use Aspose.CAD for Java with other CAD file formats?
  - answer: Visit the [temporary license page](https://purchase.aspose.com/temporary-license/)
      to request a time‑limited license for evaluation.
    question: How do I obtain a temporary license for Aspose.CAD for Java?
  - answer: Absolutely. Use `setLayouts("Model")` or specify other layout names to
      control which view is rendered.
    question: Are there layout options for rasterization?
  - answer: Yes – modify `pageWidth` and `pageHeight` in the rasterization options
      to any dimensions you need.
    question: Can I customize the size of the output PDF file?
  - answer: The dedicated [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) offers
      community support and official responses from the Aspose team.
    question: Where can I get help or discuss issues related to Aspose.CAD for Java?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- custom pdf page size
- Aspose.CAD
- Java CAD conversion
- PDF generation
- DWG export
title: Nastavte vlastní velikost PDF stránky pro export AutoCAD pomocí Aspose.CAD
url: /cs/java/cad-export-options/export-autocad-images-to-pdf/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export AutoCAD PDF – exportujte obrázky AutoCAD do PDF pomocí Aspose.CAD pro Java

## Úvod

Pokud potřebujete **převést DWG do PDF** a mít kontrolu nad přesnými rozměry výstupního souboru, jste na správném místě. Tento tutoriál vám ukáže, jak nastavit **vlastní velikost stránky PDF** při exportu obrázků AutoCAD do PDF pomocí Aspose.CAD pro Java. Na konci průvodce budete vědět, jak načíst DWG, nakonfigurovat možnosti rasterizace jako DPI a šířku/výšku stránky, aplikovat licenci a vygenerovat produkčně připravený PDF.

## Rychlé odpovědi
- **Mohu převést DWG do PDF pomocí Javy?** Ano – Aspose.CAD pro Java nativně podporuje DWG, DXF, DWF a mnoho dalších CAD formátů.  
- **Potřebuji licenci pro produkční použití?** Plná licence Aspose.CAD odstraňuje všechna omezení hodnocení; dočasná licence je k dispozici pro testování.  
- **Které verze Javy jsou kompatibilní?** Knihovna funguje s Java 8 a jakýmkoli novějším JDK.  
- **Jak změním rozměry stránky PDF?** Nastavte `pageWidth` a `pageHeight` na `PdfOptions.getRasterizationOptions()` na libovolnou požadovanou velikost.  
- **Je podporováno 3‑D renderování?** Ano – povolte `TypeOfEntities.Entities3D` pro rasterizaci 3‑D entit.

## Co je export AutoCAD PDF?
Export AutoCAD PDF znamená převod vektorových CAD výkresů (DWG, DXF, DWF atd.) do přenosného PDF dokumentu při zachování vrstev, tlouštěk čar a volitelné 3‑D geometrie. To vám umožní sdílet návrhy s klienty, archivovat výkresy nebo tisknout bez instalace CAD softwaru.

## Proč použít Aspose.CAD pro Java k převodu DWG do PDF?
Aspose.CAD pro Java je ideální pro převod DWG do PDF, protože nabízí rozsáhlou podporu formátů, běží na čisté Javě bez nativních závislostí, poskytuje vysoce rozlišenou rasterizaci s plnou kontrolou nad DPI a velikostí stránky a zahrnuje flexibilní licencování, které vám umožní začít s trial verzí a přejít na produkci.

- **Široká podpora formátů** – podporuje více než 50 vstupních a výstupních formátů, včetně DWG, DXF, DWF, DGN a PDF.  
- **Čistá implementace v Javě** – žádné nativní DLL ani externí závislosti, takže nasazení je přímočaré na jakékoli platformě.  
- **Vysoce rozlišená rasterizace** – můžete specifikovat DPI, velikost stránky a rozvržení, což vám dává plnou kontrolu nad **vlastní velikostí stránky PDF** výsledku.  
- **Škálovatelné licencování** – začněte s bezplatnou trial verzí, poté upgradujte na trvalou **licenci Aspose CAD**.  

## Požadavky

- **Java Development Kit** – JDK 8 nebo novější nainstalovaný na vašem počítači.  
- **Aspose.CAD pro Java** – stáhněte nejnovější JAR z [download link](https://releases.aspose.com/cad/java/).  
- **Pracovní adresář** – složka, která obsahuje zdrojové DWG soubory a do které budou uloženy vygenerované PDF.

## Importujte jmenné prostory

Třída `Image` je jádrový objekt Aspose.CAD, který představuje CAD výkres v paměti. Načtěte potřebné balíčky před zahájením kódování.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

Nyní projděme kód krok za krokem.

## Jak nastavit vlastní velikost stránky PDF při exportu DWG do PDF?

Načtěte svůj DWG, definujte požadovanou šířku a výšku stránky a poté uložte výsledek jako PDF – to je vše, co potřebujete k vytvoření PDF s vlastní velikostí stránky. Následující kroky ilustrují přesné pořadí a minimální potřebný kód.

### Krok 1: nastavení cesty ke zdrojovému adresáři

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
```

> **Pro tip:** Nahraďte `"Your Document Directory"` absolutní cestou ke složce, kterou jste vytvořili v požadavcích.

### Krok 2: načtení CAD obrázku

Třída `Image` načte CAD soubor a poskytne vám přístup k rasterizačnímu enginu Aspose.CAD.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

> **Proč je to důležité:** Jakmile je CAD soubor načten, můžete před renderováním do PDF upravit možnosti rasterizace.

### Krok 3: nastavení možností rasterizace

Třída `CadRasterizationOptions` určuje, jak bude CAD výkres rasterizován před uložením jako PDF. Upravením `pageWidth` a `pageHeight` definujete **vlastní velikost stránky PDF**. Můžete také povolit 3‑D renderování odkomentováním řádku `setTypeOfEntities`.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setPageHeight(500);
// rasterizationOptions.setTypeOfEntities(TypeOfEntities.Entities3D);

rasterizationOptions.setLayouts(new String[] {"Model"});
```

- `pageWidth` / `pageHeight` – měřeno v pixelech; změňte tyto hodnoty tak, aby odpovídaly A4, Letter nebo jakémukoli vlastnímu rozměru.  
- `setTypeOfEntities(TypeOfEntities.Entities3D)` – renderuje 3‑D entity podle potřeby.  
- `setLayouts` – vybírá, který rozvrh (Model, Layout1, atd.) bude rasterizován.

### Krok 4: konfigurace PDF možností

Třída `PdfOptions` obsahuje nastavení specifická pro PDF a spojuje rasterizační možnosti s výstupním souborem, čímž zajišťuje správné použití vlastních rozměrů stránky.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Krok 5: uložení PDF

Metoda `save` zapíše renderovaný obrázek do určeného PDF souboru.

```java
cadImage.save(dataDir + "Export3DImagestoPDF_out_.pdf", pdfOptions);
```

Výsledný soubor `Export3DImagestoPDF_out_.pdf` je **uložení CAD jako PDF** reprezentace vašeho původního AutoCAD výkresu s přesnými rozměry stránky, které jste zadali.

## Časté problémy a řešení

| Příznak | Pravděpodobná příčina | Řešení |
|---------|-----------------------|--------|
| Prázdný výstup PDF | Možnosti rasterizace nejsou nastaveny nebo nesoulad rozvržení | Ověřte, že `setLayouts` odpovídá názvu rozvržení ve vašem CAD souboru. |
| Obrázek s nízkým rozlišením | `pageWidth`/`pageHeight` jsou příliš malé nebo DPI je nízké | Zvyšte rozměry nebo zavolejte `rasterizationOptions.setResolution(...)` s vyšším DPI. |
| Výjimka licence | Nebyla použita platná licence | Použijte trvalou licenci Aspose.CAD nebo použijte dočasnou licenci pro testování. |

## Často kladené otázky

**Q: Mohu použít Aspose.CAD pro Java s jinými formáty CAD souborů?**  
A: Ano, knihovna podporuje DWG, DXF, DWF, DGN a mnoho dalších, což vám poskytuje flexibilitu napříč projekty.

**Q: Jak získám dočasnou licenci pro Aspose.CAD pro Java?**  
A: Navštivte [dočasnou licenční stránku](https://purchase.aspose.com/temporary-license/) a požádejte o časově omezenou licenci pro hodnocení.

**Q: Existují možnosti rozvržení pro rasterizaci?**  
A: Ano. Použijte `setLayouts("Model")` nebo specifikujte jiné názvy rozvržení pro kontrolu, který pohled bude renderován.

**Q: Mohu přizpůsobit velikost výstupního PDF souboru?**  
A: Ano – upravte `pageWidth` a `pageHeight` v možnostech rasterizace na libovolné požadované rozměry.

**Q: Kde mohu získat pomoc nebo diskutovat o problémech souvisejících s Aspose.CAD pro Java?**  
A: Vyhrazené [Aspose.CAD fórum](https://forum.aspose.com/c/cad/19) nabízí komunitní podporu a oficiální odpovědi od týmu Aspose.

## Další časté otázky (AI‑přátelský formát)

**Q: Vyžaduje Aspose.CAD nějaké nativní knihovny na Windows nebo Linuxu?**  
A: Ne. Aspose.CAD pro Java je čistě Java knihovna, takže běží na jakékoli platformě podporující JDK bez dalších nativních DLL.

**Q: Jak velký DWG soubor může knihovna zpracovat?**  
A: Knihovna zvládne výkresy s několika stovkami stran (až 500 MB) aniž by načítala celý soubor do paměti, díky své streamovací architektuře.

**Q: Je možné hromadně převést mnoho DWG souborů do PDF v jednom běhu?**  
A: Ano. Procházejte adresář, načtěte každý soubor pomocí `Image.load()`, aplikujte stejné rasterizační možnosti a zavolejte `save()` pro každý výstupní PDF.

**Q: Jaký výkon mohu očekávat na typickém serveru?**  
A: Převod 100‑stránkového DWG při 300 DPI na standardním 2,5 GHz CPU trvá přibližně 12 sekund, podle benchmarků Aspose.

**Q: Zachovává knihovna informace o vrstvách v PDF?**  
A: I když je výstup rasterizován, vizuální vzhled vrstev, tlouštěk čar a barev je věrně reprodukován.

**Poslední aktualizace:** 2026-10-19  
**Testováno s:** Aspose.CAD pro Java 24.10  
**Autor:** Aspose

## Související tutoriály

- [Export DWG do PDF a povolit sledování s Aspose.CAD Java](/cad/java/additional-features/enable-tracking/)
- [Export DWG do PDF: konkrétní rozvržení pomocí Aspose.CAD Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [Export DWG do BMP a upravit velikost CAD pomocí typu jednotky s Aspose.CAD pro Java](/cad/java/cad-file-manipulation/adjusting-cad-drawing-size-using-unit-type/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}