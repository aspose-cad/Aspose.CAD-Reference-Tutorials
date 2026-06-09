---
date: 2026-06-09
description: Zjistěte, jak převést DXF na WMF s Aspose.CAD pro Java, včetně bezplatné
  zkušební verze, podpory Java 8+ a volitelného exportu do PDF. Praktický návod krok
  za krokem s ukázkami kódu.
keywords:
- convert dxf to wmf
- aspose cad java
- aspose free trial
- aspose cad conversion
- export dxf pdf
linktitle: Export DXF do formátu WMF pomocí Javy
schemas:
- author: Aspose
  dateModified: '2026-06-09'
  description: Learn how to convert DXF to WMF with Aspose.CAD for Java, including
    a free trial, Java 8+ support, and optional PDF export. Step‑by‑step guide with
    code examples.
  headline: Convert DXF to WMF Using Aspose.CAD in Java
  type: TechArticle
- description: Learn how to convert DXF to WMF with Aspose.CAD for Java, including
    a free trial, Java 8+ support, and optional PDF export. Step‑by‑step guide with
    code examples.
  name: Convert DXF to WMF Using Aspose.CAD in Java
  steps:
  - name: Load DXF Drawing
    text: Image.load reads the DXF file into an Aspose.CAD Image object.
  - name: Configure Rasterization Options
    text: CadRasterizationOptions specifies page size, resolution, and background
      for rasterizing the CAD drawing.
  - name: Save as WMF
    text: ImageSaveOptions with SaveFormat.WMF tells Aspose.CAD to write the output
      as a Windows Metafile.
  - name: Dispose of Resources
    text: Calling image.close() releases native resources used by the Aspose.CAD Image
      object.
  - name: Optional – Export to PDF
    text: PdfOptions configures PDF‑specific settings when saving the image as a PDF
      document. > **Pro tip:** You can reuse the same `CadRasterizationOptions` object
      for PDF export by passing it to a `PdfOptions` instance, saving you a few lines
      of setup.
  type: HowTo
- questions:
  - answer: Yes. Load the file in a try‑with‑resources block and dispose of the `Image`
      object promptly. Adjust `CadRasterizationOptions.setPageWidth/Height` to a reasonable
      size to keep memory usage low.
    question: Can I convert large DXF files (hundreds of MB) without running out of
      memory?
  - answer: WMF is a flat vector format, so layer hierarchy is flattened, but line
      styles, colors, and hatch patterns are preserved.
    question: Does the WMF output retain layer information?
  - answer: Use `rasterizationOptions.setResolution(300);` to define DPI before saving.
    question: Is it possible to set a custom DPI for the WMF?
  - answer: Absolutely. Loop through a directory, load each file, and apply the same
      rasterization and save logic.
    question: Can I batch‑convert multiple DXF files in one run?
  - answer: Aspose.CAD for Java supports Java 8 and later, including Java 11, 17,
      and newer LTS releases.
    question: What versions of Java are supported?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Převod DXF na WMF pomocí Aspose.CAD v Javě
url: /cs/java/additional-features/export-dxf-to-wmf/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Převod DXF na WMF pomocí Aspose.CAD v Javě

## Úvod

V tomto tutoriálu se dozvíte, jak **převést DXF na WMF** pomocí Aspose.CAD pro Java. Ať už potřebujete vložit CAD výkresy do Windows‑založené zprávy, generovat lehké vektorové grafiky pro Office dokumenty, nebo automatizovat hromadné konverze, převod DXF na WMF je častý požadavek v inženýrských a reportovacích pipelinech. Provedeme vás načtením DXF výkresu, nastavením možností rasterizace, uložením výsledku jako WMF a volitelným exportem stejného výkresu do PDF.

## Rychlé odpovědi
- **Mohu převést DXF na WMF s bezplatnou zkušební verzí?** Ano – Aspose nabízí plně funkční 30‑denní zkušební verzi.  
- **Jaká verze Javy je vyžadována?** Java 8 nebo novější.  
- **Potřebuji licenci pro spuštění kódu?** Licence je vyžadována pro produkci; zkušební verze funguje pro vývoj a testování.  
- **Je konverze bezztrátová?** Vektorová data jsou zachována; možnosti rasterizace vám umožní řídit rozlišení.  
- **Mohu také exportovat stejný výkres do PDF?** Ano – viz krok „Export do PDF“ níže.

## Co je „převod DXF na WMF“?

Převod DXF na WMF znamená převzít soubor Drawing Exchange Format (DXF) – široce používaný CAD formát – a převést jej na Windows Metafile (WMF). WMF je vektorový formát obrázku, který se hladce integruje s Microsoft Office, Windows aplikacemi a mnoha nástroji pro tvorbu reportů.

## Proč používat Aspose.CAD pro Java?

Aspose.CAD pro Java poskytuje čistě Java engine bez nativních DLL, který převádí CAD soubory s **více než 99 % vektorovou věrností**, zachovává vrstvy, barvy, styly čar a šrafování. Podporuje **více než 50 vstupních a výstupních formátů** – včetně DXF, DWG, DGN, PDF, PNG, SVG a WMF – a umožňuje jemně nastavit velikost stránky, DPI a barvu pozadí pomocí vestavěných možností rasterizace. Stejné API také zpracovává exporty do PDF, PNG a SVG, čímž odstraňuje potřebu více knihoven.

### Klíčové výhody
- **Žádné externí závislosti** – čistá Java, funguje na jakémkoli OS, který podporuje Java.  
- **Vysoká věrnost vykreslování** – zachovává tloušťku čáry, barvu a detaily šrafování.  
- **Vestavěná rasterizace** – umožňuje řídit rozměry stránky, rozlišení a pozadí.  
- **Komplexní konverze** – stejné třídy exportují do WMF, PDF, PNG, SVG atd.

## Požadavky

Před začátkem se ujistěte, že máte:

- **Aspose.CAD for Java** integrován ve vašem projektu. Stáhněte jej z oficiální stránky: [Aspose.CAD Java download](https://releases.aspose.com/cad/java/).  
- **Adresář dokumentů**, kde jsou uloženy vaše DXF soubory (např. `Your Document Directory/DXFDrawings/`).

## Import jmenných prostorů

Následující importy přinášejí třídy Aspose.CAD potřebné pro načítání, rasterizaci a ukládání CAD souborů.
```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageSaveOptions;
import com.aspose.cad.fileformats.cad.CadRasterizationOptions;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.CadImageInfo;
import com.aspose.cad.fileformats.cad.CadImageInfo;
import java.awt.Color;
```

## Průvodce krok za krokem

### Jak převést DXF na WMF v Javě?

Načtěte svůj DXF soubor pomocí `Image.load("yourFile.dxf")`, nakonfigurujte `CadRasterizationOptions` pro požadovanou velikost stránky a DPI, a poté zavolejte `image.save("output.wmf", new ImageSaveOptions(SaveFormat.WMF))`. Tento tříkrokový vzor provádí kompletní konverzi při zachování vektorové kvality a vyžaduje jen několik řádků kódu.

#### Krok 1: Načíst DXF výkres

Image.load načte DXF soubor do objektu Aspose.CAD Image.
```java
import com.aspose.cad.Color;
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.WmfOptions;
```

#### Krok 2: Nastavit možnosti rasterizace

CadRasterizationOptions určuje velikost stránky, rozlišení a pozadí pro rasterizaci CAD výkresu.
```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DXFDrawings/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

#### Krok 3: Uložit jako WMF

ImageSaveOptions s SaveFormat.WMF říká Aspose.CAD, aby výstup zapsal jako Windows Metafile.
```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(100);
rasterizationOptions.setPageHeight(100);
WmfOptions wmfOptions = new WmfOptions();
```

#### Krok 4: Uvolnit prostředky

Voláním image.close() uvolníte nativní prostředky používané objektem Aspose.CAD Image.
```java
cadImage.save(dataDir+" example.ifc.wmf", wmfOptions);
```

#### Krok 5: Volitelně – Export do PDF

PdfOptions konfiguruje specifické nastavení PDF při ukládání obrázku jako PDF dokumentu.
```java
finally
{
  cadImage.dispose();
}
```

> **Tip:** Můžete znovu použít stejný objekt `CadRasterizationOptions` pro export do PDF tím, že jej předáte instanci `PdfOptions`, což vám ušetří několik řádků nastavení.

## Jak exportovat DXF do PDF pomocí Aspose CAD Java?

Export do PDF následuje stejné kroky načítání a rasterizace; stačí nahradit formát ukládání WMF formátem PDF. Použijte `new ImageSaveOptions(SaveFormat.Pdf)` a volitelně nastavte PDF‑specifické možnosti, jako je úroveň komprese nebo metadata autora. Tento jednorázový převod vytvoří prohledávatelný PDF s přesnou stránkovou strukturou, který odráží původní CAD rozvržení.

## Časté problémy a řešení

| Problém | Příčina | Řešení |
|-------|-------|-----|
| **`NullPointerException` on `cadImage.save`** | Proměnná `cadImage` není definována (měla by být `image`). | Nahraďte `cadImage` za `image` nebo přejmenujte proměnnou konzistentně. |
| **Output WMF is blank** | Velikost stránky rasterizace je příliš malá nebo je barva pozadí nastavena na průhlednou. | Zvyšte `PageWidth`/`PageHeight` nebo nastavte barvu pozadí pomocí `rasterizationOptions.setBackgroundColor(Color.WHITE);`. |
| **License exception** | Spuštění bez platné Aspose licence v produkci. | Aplikujte licenční soubor při startu aplikace: `License license = new License(); license.setLicense("Aspose.Total.Java.lic");`. |

## Závěr

Nyní máte kompletní, připravený workflow pro **převod DXF na WMF** pomocí Aspose.CAD pro Java, s volitelným krokem **exportovat stejný výkres do PDF**. Tento přístup vám poskytuje vysoce kvalitní vektorový výstup, který se hladce integruje s Windows‑založenými nástroji pro tvorbu reportů a dokumentace, a zároveň udržuje váš kód jednoduchý a bez závislostí.

## Často kladené otázky

### Q1: Kde najdu dokumentaci Aspose.CAD?
Odpověď: Dokumentaci můžete získat [zde](https://reference.aspose.com/cad/java/).

### Q2: Jak stáhnu Aspose.CAD pro Java?
Odpověď: Knihovnu stáhněte [zde](https://releases.aspose.com/cad/java/).

### Q3: Je k dispozici bezplatná zkušební verze?
Odpověď: Ano, bezplatnou zkušební verzi získáte [zde](https://releases.aspose.com/).

### Q4: Potřebujete dočasné licenční možnosti?
Odpověď: Prozkoumejte dočasné licence [zde](https://purchase.aspose.com/temporary-license/).

### Q5: Kde mohu získat podporu?
Odpověď: Navštivte fórum podpory Aspose.CAD [zde](https://forum.aspose.com/c/cad/19).

## Často kladené otázky

**Q: Mohu převést velké DXF soubory (stovky MB) bez vyčerpání paměti?**  
A: Ano. Načtěte soubor v bloku try‑with‑resources a rychle uvolněte objekt `Image`. Nastavte `CadRasterizationOptions.setPageWidth/Height` na rozumnou velikost, aby se udržovala nízká spotřeba paměti.

**Q: Zachovává výstup WMF informace o vrstvách?**  
A: WMF je plochý vektorový formát, takže hierarchie vrstev je zploštěna, ale styly čar, barvy a šrafování jsou zachovány.

**Q: Je možné nastavit vlastní DPI pro WMF?**  
A: Použijte `rasterizationOptions.setResolution(300);` pro definování DPI před uložením.

**Q: Mohu hromadně převádět více DXF souborů v jednom běhu?**  
A: Ano. Procházejte adresář, načtěte každý soubor a použijte stejnou logiku rasterizace a ukládání.

**Q: Jaké verze Javy jsou podporovány?**  
A: Aspose.CAD pro Java podporuje Java 8 a novější, včetně Java 11, 17 a novějších LTS verzí.

---

**Poslední aktualizace:** 2026-06-09  
**Testováno s:** Aspose.CAD for Java 24.11  
**Autor:** Aspose

```java
image.save(dataDir + "conic_pyramid_out_.pdf"); 
```

## Související tutoriály

- [Vytvořit PDF z CAD – Export DXF do PDF s Aspose.CAD pro Java](/cad/java/additional-features/export-dxf-to-pdf/)
- [Vytvořit PDF z DXF: Export vrstvy s Aspose.CAD pro Java](/cad/java/additional-features/export-specific-layer-to-pdf/)
- [Jak převést rozvržení DXF na JPEG obrázek s Aspose.CAD v Javě](/cad/java/additional-features/export-specific-layout-to-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}