---
date: 2026-10-19
description: Naučte se, jak převést DWG na PDF v Java s Aspose.CAD. Tento step‑by‑step
  návod vám ukáže, jak exportovat AutoCAD PDF, uložit CAD jako PDF a použít licenci.
keywords:
- dwg to pdf java
- export autocad pdf
- java pdf export library
- aspose cad license
- save cad pdf
- customize pdf page size
lastmod: 2026-10-19
linktitle: Exportovat obrázky AutoCAD do PDF
og_description: Naučte se, jak převést DWG na PDF v Java s Aspose.CAD. Tento step‑by‑step
  návod vám ukáže, jak exportovat AutoCAD PDF, uložit CAD jako PDF a použít licenci.
og_image_alt: 'Tutorial: convert DWG to PDF in Java with Aspose.CAD'
og_title: Převod DWG na PDF v Java pomocí Aspose.CAD
schemas:
- author: Aspose
  dateModified: '2026-10-19'
  description: Learn how to convert DWG to PDF in Java with Aspose.CAD. This step‑by‑step
    guide shows you how to export AutoCAD PDF, save CAD as PDF, and apply a license.
  headline: Convert DWG to PDF in Java using Aspose.CAD
  type: TechArticle
- description: Learn how to convert DWG to PDF in Java with Aspose.CAD. This step‑by‑step
    guide shows you how to export AutoCAD PDF, save CAD as PDF, and apply a license.
  name: Convert DWG to PDF in Java using Aspose.CAD
  steps:
  - name: set the resource directory path
    text: Replace `"Your Document Directory"` with the absolute path to the folder
      you created in the prerequisites. > **Pro tip:** Use `Paths.get(...).toAbsolutePath()`
      to avoid path‑related errors on different operating systems.
  - name: load the CAD image
    text: Loading the CAD file into an `Image` object gives you full access to Aspose.CAD’s
      rasterization engine. The `Image` class loads the DWG file and prepares it for
      conversion. > **Why this matters:** Once the drawing is in memory, you can query
      its layouts, layers, and metadata before rasterizing.
  - name: set rasterization options
    text: Adjust `pageWidth` and `pageHeight` to **customize PDF page size**. Enabling
      `setTypeOfEntities(TypeOfEntities.Entities3D)` allows full 3‑D rendering when
      needed. The `RasterizationOptions` object controls DPI, page dimensions, and
      entity types for the output. - `pageWidth` / `pageHeight` are measur
  - name: configure PDF options
    text: Tie the rasterization settings to the PDF output, ensuring the vector data
      is correctly transformed. The `PdfOptions` class links the rasterization configuration
      with the final PDF file.
  - name: save the PDF
    text: The resulting file, `Export3DImagestoPDF_out_.pdf`, is a **save cad as pdf**
      representation of your original AutoCAD drawing. The `save` method writes the
      rasterized image to a PDF file on disk.
  type: HowTo
- questions:
  - answer: Yes – the library supports DWG, DXF, DWF, DGN, and over 30 additional
      formats, giving you flexibility across projects.
    question: Can I use Aspose.CAD for Java with other CAD file formats?
  - answer: Visit the [temporary license page](https://purchase.aspose.com/temporary-license/)
      to request a time‑limited license for evaluation.
    question: How do I obtain a temporary license for Aspose.CAD for Java?
  - answer: Absolutely. Use `setLayouts("Model")`, `setLayouts("Layout1")`, etc.,
      to choose which view is rendered into the PDF.
    question: Are there layout options for rasterization?
  - answer: Yes – modify `pageWidth` and `pageHeight` in the rasterization options
      to match any required page dimensions.
    question: Can I change the size of the output PDF file?
  - answer: The dedicated community is available at the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19)
      where you can ask questions and share solutions.
    question: Where can I get help if I run into problems?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- dwg to pdf
- aspose.cad
- java cad conversion
- export autocad pdf
title: Převod DWG na PDF v Java pomocí Aspose.CAD
url: /cs/java/cad-export-options/export-autocad-images-to-pdf/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export AutoCAD PDF – exportujte obrázky AutoCAD do PDF pomocí Aspose.CAD pro Java

## Úvod

Pokud potřebujete **převést DWG na PDF v Javě**, jste na správném místě. Tento tutoriál vám ukáže, jak exportovat obrázky AutoCAD do PDF pomocí Aspose.CAD pro Java, čistě‑Java knihovny, která zpracovává DWG, DXF, DWF a mnoho dalších CAD formátů bez nativních závislostí. Na konci budete schopni **uložit CAD jako PDF**, upravit možnosti rasterizace, jako je velikost stránky, a správně použít **licenci Aspose CAD** pro produkční nasazení.

## Rychlé odpovědi
- **Mohu převést DWG na PDF pomocí Javy?** Ano – Aspose.CAD pro Java nativně podporuje DWG, DXF a desítky dalších CAD formátů.  
- **Potřebuji licenci?** Trvalá **licence Aspose CAD** odstraňuje všechna omezení hodnocení; dočasná licence je k dispozici pro testování.  
- **Které verze Javy jsou podporovány?** Java 8 a vyšší jsou plně podporovány.  
- **Mohu řídit rozměry PDF stránky?** Rozhodně – nastavte `pageWidth` a `pageHeight` v možnostech rasterizace.  
- **Je možné 3‑D renderování?** Ano – povolte `TypeOfEntities.Entities3D` pro rasterizaci 3‑D entit.

## Co je export AutoCAD PDF?
Exportování AutoCAD PDF je proces převodu vektorových CAD výkresů do přenositelného PDF dokumentu. Zachovává vrstvy, tloušťky čar, barvy a volitelně 3‑D geometrii, což usnadňuje sdílení návrhů s klienty nebo jejich archivaci bez potřeby CAD softwaru.

## Proč převádět DWG na PDF pomocí Aspose.CAD pro Java?
Aspose.CAD podporuje **více než 50 vstupních a výstupních formátů**, zpracovává výkresy o stovkách stránek, aniž by načítal celý soubor do paměti, a běží na jakékoli platformě, která podporuje Java 8+. Knihovna vám dává plnou kontrolu nad DPI, velikostí stránky a rozvržením, takže můžete **přizpůsobit velikost PDF stránky** tak, aby odpovídala přesným specifikacím projektu, a to vše bez instalace nativních DLL.

## Požadavky

- **Java Development Kit** – JDK 8 nebo novější nainstalovaný na vašem pracovním stanici.  
- **Aspose.CAD pro Java** – stáhněte nejnovější JAR z [odkazu ke stažení](https://releases.aspose.com/cad/java/).  
- **Pracovní adresář** – složka, kde budou uloženy vaše zdrojové DWG soubory a vygenerované PDF.

## Import názvových prostorů

Třída `Image` představuje libovolný rasterizovatelný CAD výkres, zatímco `RasterizationOptions` a `PdfOptions` vám umožňují jemně doladit převod.

Třída `Image` je nejvyšší objekt Aspose.CAD, který drží CAD výkres v paměti.  
Třída `RasterizationOptions` definuje, jak jsou vektorová data rasterizována před zápisem do PDF.  
Třída `PdfOptions` spojuje nastavení rasterizace s PDF‑specifickými výstupními parametry.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

Nyní projdeme kód krok za krokem.

## Jak převést DWG na PDF pomocí Aspose.CAD pro Java?

Pro převod souboru DWG na PDF s Aspose.CAD pro Java načtěte výkres pomocí třídy Image, nakonfigurujte CadRasterizationOptions (např. DPI, velikost stránky a typy entit), zabalte tyto možnosti do PdfOptions a poté zavolejte metodu save s určením názvu souboru .pdf. Tento postup zajišťuje, že vektorová data jsou správně rasterizována a výsledné PDF odpovídá vašim požadavkům na rozvržení.

### Krok 1: nastavit cestu ke zdrojovému adresáři

Nahraďte `"Your Document Directory"` absolutní cestou ke složce, kterou jste vytvořili v požadavcích.

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
```

> **Tip:** Použijte `Paths.get(...).toAbsolutePath()` k vyhnutí se chybám souvisejícím s cestou na různých operačních systémech.

### Krok 2: načíst CAD obrázek

Načtení CAD souboru do objektu `Image` vám poskytuje plný přístup k rasterizačnímu enginu Aspose.CAD.

Třída `Image` načte DWG soubor a připraví jej pro převod.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

> **Proč je to důležité:** Jakmile je výkres v paměti, můžete před rasterizací dotazovat jeho rozvržení, vrstvy a metadata.

### Krok 3: nastavit možnosti rasterizace

Upravte `pageWidth` a `pageHeight` pro **přizpůsobení velikosti PDF stránky**. Povolením `setTypeOfEntities(TypeOfEntities.Entities3D)` umožníte plné 3‑D renderování podle potřeby.

Objekt `RasterizationOptions` řídí DPI, rozměry stránky a typy entit pro výstup.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setPageHeight(500);
// rasterizationOptions.setTypeOfEntities(TypeOfEntities.Entities3D);

rasterizationOptions.setLayouts(new String[] {"Model"});
```

- `pageWidth` / `pageHeight` jsou měřeny v bodech (1 pt = 1/72 in).  
- Odkomentujte řádek `setTypeOfEntities` pro 3‑D rasterizaci.  
- `setLayouts` vybírá, které rozvržení (Model, Layout1, atd.) bude renderováno.

### Krok 4: nakonfigurovat PDF možnosti

Propojte nastavení rasterizace s PDF výstupem, aby byla vektorová data správně transformována.

Třída `PdfOptions` spojuje konfiguraci rasterizace s finálním PDF souborem.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Krok 5: uložit PDF

Výsledný soubor `Export3DImagestoPDF_out_.pdf` je **uložení CAD jako PDF** reprezentace vašeho původního AutoCAD výkresu.

Metoda `save` zapíše rasterizovaný obrázek do PDF souboru na disku.

```java
cadImage.save(dataDir + "Export3DImagestoPDF_out_.pdf", pdfOptions);
```

## Časté problémy a řešení

| Symptom | Pravděpodobná příčina | Řešení |
|---------|-----------------------|--------|
| Prázdný výstup PDF | Možnosti rasterizace nejsou nastaveny nebo nesoulad rozvržení | Ověřte, že `setLayouts` odpovídá názvu rozvržení ve vašem CAD souboru. |
| Obrázek s nízkým rozlišením | `pageWidth`/`pageHeight` jsou příliš malé | Zvyšte rozměry nebo nastavte vyšší DPI pomocí `rasterizationOptions.setResolution(...)`. |
| Výjimka licence | Nebyla použita platná licence | Použijte **licenci Aspose CAD** nebo použijte dočasnou licenci pro testování. |

## Často kladené otázky

**Q: Mohu použít Aspose.CAD pro Java s jinými CAD formáty souborů?**  
A: Ano – knihovna podporuje DWG, DXF, DWF, DGN a více než 30 dalších formátů, což vám poskytuje flexibilitu napříč projekty.

**Q: Jak získám dočasnou licenci pro Aspose.CAD pro Java?**  
A: Navštivte [stránku s dočasnou licencí](https://purchase.aspose.com/temporary-license/), kde můžete požádat o časově omezenou licenci pro hodnocení.

**Q: Existují možnosti rozvržení pro rasterizaci?**  
A: Rozhodně. Použijte `setLayouts("Model")`, `setLayouts("Layout1")` atd., abyste vybrali, který pohled bude renderován do PDF.

**Q: Mohu změnit velikost výstupního PDF souboru?**  
A: Ano – upravte `pageWidth` a `pageHeight` v možnostech rasterizace tak, aby odpovídaly požadovaným rozměrům stránky.

**Q: Kde mohu získat pomoc, pokud narazím na problémy?**  
A: Vyhrazená komunita je k dispozici na [fóru Aspose.CAD](https://forum.aspose.com/c/cad/19), kde můžete klást otázky a sdílet řešení.

---

**Poslední aktualizace:** 2026-10-19  
**Testováno s:** Aspose.CAD pro Java 24.10  
**Autor:** Aspose

## Související tutoriály

- [Export DWG do PDF v Javě – Nastavit velikost PDF stránky pomocí Aspose.CAD](/cad/java/cad-export-options/export-to-pdf/)
- [Export DWG do PDF: Specifické rozvržení pomocí Aspose.CAD pro Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [Export DWG do PDF a povolit sledování s Aspose.CAD Java](/cad/java/additional-features/enable-tracking/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}