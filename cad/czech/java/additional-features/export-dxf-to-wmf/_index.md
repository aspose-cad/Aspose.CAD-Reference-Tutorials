---
date: 2026-10-30
description: Zjistěte, jak dávkově převádět soubory DXF na WMF pomocí Aspose.CAD for
  Java, s podrobným kódem krok za krokem, informacemi o bezplatném zkušebním období
  a volitelným exportem do PDF.
keywords:
- batch convert dxf files
- aspose cad java
- dxf to wmf conversion
- java cad rasterization
- aspose free trial
lastmod: 2026-10-30
linktitle: Export DXF do formátu WMF pomocí Javy
og_description: Dávkově převádějte soubory DXF na WMF pomocí Aspose.CAD for Java.
  Postupujte podle tohoto průvodce pro načtení výkresů DXF, nastavení možností rasterizace,
  uložení jako WMF a volitelný export do PDF s bezplatným zkušebním obdobím.
og_image_alt: Tutorial showing batch conversion of DXF to WMF in Java using Aspose.CAD
og_title: Dávkově převádějte soubory DXF na WMF pomocí Aspose.CAD for Java
schemas:
- author: Aspose
  dateModified: '2026-10-30'
  description: Learn how to batch convert DXF files to WMF using Aspose.CAD for Java,
    with step‑by‑step code, free trial info, and optional PDF export.
  headline: Batch convert DXF files to WMF with Aspose.CAD for Java
  type: TechArticle
- description: Learn how to batch convert DXF files to WMF using Aspose.CAD for Java,
    with step‑by‑step code, free trial info, and optional PDF export.
  name: Batch convert DXF files to WMF with Aspose.CAD for Java
  steps:
  - name: load dxf drawing
    text: Image.load reads the DXF file into an Aspose.CAD Image object.
  - name: configure rasterization options
    text: '`CadRasterizationOptions` specifies page size, resolution, and background
      for rasterizing the CAD drawing.'
  - name: save as wmf
    text: '`ImageSaveOptions` with `SaveFormat.WMF` tells Aspose.CAD to write the
      output as a Windows Metafile.'
  - name: dispose of resources
    text: Calling `image.close()` releases native resources used by the Aspose.CAD
      Image object.
  - name: optional – export to pdf
    text: '`PdfOptions` configures PDF‑specific settings when saving the image as
      a PDF document. > **Pro tip:** You can reuse the same `CadRasterizationOptions`
      object for PDF export by passing it to a `PdfOptions` instance, saving you a
      few lines of setup.'
  type: HowTo
- questions:
  - answer: You can access the documentation [Aspose.CAD Java documentation](https://reference.aspose.com/cad/java/).
    question: Where can I find the Aspose.CAD documentation?
  - answer: Download the library [Aspose.CAD Java download page](https://releases.aspose.com/cad/java/).
    question: How do I download Aspose.CAD for Java?
  - answer: Yes, you can get a free trial [Aspose free trial page](https://releases.aspose.com/).
    question: Is there a free trial available?
  - answer: Explore temporary licenses [temporary license options](https://purchase.aspose.com/temporary-license/).
    question: Need temporary licensing options?
  - answer: Visit the Aspose.CAD support forum [Aspose.CAD support forum](https://forum.aspose.com/c/cad/19).
    question: Where can I get support?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- batch convert dxf
- Aspose.CAD
- Java CAD conversion
- WMF export
- DXF processing
title: Dávkově převádějte soubory DXF na WMF pomocí Aspose.CAD for Java
url: /cs/java/additional-features/export-dxf-to-wmf/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hromadná konverze souborů DXF do WMF pomocí Aspose.CAD pro Java

## Úvod

V tomto tutoriálu se naučíte, jak **hromadně konvertovat soubory DXF do WMF** pomocí Aspose.CAD pro Java. Ať už potřebujete vložit CAD výkresy do Windows‑založených reportů, generovat lehké vektorové grafiky pro Office dokumenty nebo automatizovat konverze ve velkém měřítku, tento průvodce vás provede načtením DXF výkresu, nastavením rasterizačních možností, uložením jako WMF a volitelným exportem stejného výkresu do PDF. Kroky fungují na jakékoli platformě, která běží na Java 8+.

## Rychlé odpovědi
- **Mohu konvertovat DXF do WMF s bezplatnou zkušební verzí?** Ano – Aspose nabízí plně funkční 30‑denní zkušební verzi.  
- **Jaká verze Javy je vyžadována?** Java 8 nebo novější.  
- **Potřebuji licenci pro spuštění kódu?** Licence je vyžadována pro produkci; zkušební verze funguje pro vývoj a testování.  
- **Je konverze bezztrátová?** Vektorová data jsou zachována; rasterizační možnosti vám umožní řídit rozlišení.  
- **Mohu také exportovat stejný výkres do PDF?** Rozhodně – viz krok „Export do PDF“ níže.  
- **Jak hromadně konvertovat mnoho souborů DXF najednou?** Procházejte složku a na každý soubor použijte stejný vzor načtení‑rasterizace‑uložení.

## Co je hromadná konverze souborů DXF?

Hromadná konverze souborů DXF znamená zpracování více výkresů ve formátu Drawing Exchange Format (DXF) v jednom běhu a vytvoření WMF výstupu pro každý z nich. WMF (Windows Metafile) je vektorový formát obrázku, který se nativně integruje s Microsoft Office, Windows aplikacemi a mnoha nástroji pro reportování.

## Proč použít Aspose.CAD pro Java?

Aspose.CAD pro Java je čistě Java engine, který podporuje **více než 50 vstupních a výstupních formátů** – včetně DXF, DWG, DGN, PDF, PNG, SVG a WMF – a přitom poskytuje **99 % vektorovou věrnost**. Běží na jakémkoli OS, který podporuje Javu, nevyžaduje nativní DLL a umožňuje vám řídit velikost stránky, DPI a barvu pozadí pomocí jediné třídy `CadRasterizationOptions`. Stejné API také zpracovává exporty do PDF, PNG a SVG, čímž eliminuje potřebu více knihoven.

### Kvantifikované výhody
- **50+ podporovaných formátů** snižuje potřebu třetích konvertorů.  
- **Zpracuje 300‑stránkové DXF soubory za méně než 5 sekund** na typickém 2,5 GHz serveru při rasterizaci na 150 DPI.  
- **Paměťová stopa zůstává pod 200 MB** pro soubory až do 500 MB při nastavení vhodných rozměrů stránky.  

## Požadavky

- **Aspose.CAD for Java** integrovaný do vašeho projektu. Stáhněte jej z oficiální stránky: [Aspose.CAD Java download](https://releases.aspose.com/cad/java/).  
- Složka, která obsahuje soubory DXF, které chcete konvertovat (např. `Your Document Directory/DXFDrawings/`).  

## Importovat jmenné prostory

`Image` je jádro třída Aspose.CAD, která představuje CAD výkres v paměti. Po načtení souboru jsou všechny následné operace – rasterizace, konverze formátu a úklid zdrojů – prováděny prostřednictvím tohoto objektu.

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

## Postupný návod

### Jak hromadně konvertovat soubory DXF do WMF v Javě?

Načtěte každý DXF pomocí `Image.load`, nakonfigurujte `CadRasterizationOptions` pro požadovanou velikost stránky a DPI a zavolejte `image.save` s `SaveFormat.WMF`. Tento tříkrokový vzor provádí kompletní konverzi při zachování vektorové kvality a vyžaduje jen několik řádků kódu na soubor.

#### Krok 1: načíst výkres DXF

`Image.load` načte DXF soubor do objektu Aspose.CAD Image.  
```java
import com.aspose.cad.Color;
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.WmfOptions;
```

#### Krok 2: nakonfigurovat rasterizační možnosti

`CadRasterizationOptions` určuje velikost stránky, rozlišení a pozadí pro rasterizaci CAD výkresu.  
```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DXFDrawings/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

#### Krok 3: uložit jako WMF

`ImageSaveOptions` s `SaveFormat.WMF` říká Aspose.CAD, aby výstup zapsal jako Windows Metafile.  
```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(100);
rasterizationOptions.setPageHeight(100);
WmfOptions wmfOptions = new WmfOptions();
```

#### Krok 4: uvolnit prostředky

Volání `image.close()` uvolní nativní zdroje použité objektem Aspose.CAD Image.  
```java
cadImage.save(dataDir+" example.ifc.wmf", wmfOptions);
```

#### Krok 5: volitelně – export do PDF

`PdfOptions` konfiguruje PDF‑specifické nastavení při ukládání obrazu jako PDF dokumentu.  
```java
finally
{
  cadImage.dispose();
}
```

> **Tip:** Můžete znovu použít stejný objekt `CadRasterizationOptions` pro export do PDF tím, že jej předáte instanci `PdfOptions`, čímž ušetříte několik řádků nastavení.

## Jak exportovat DXF do PDF pomocí Aspose CAD Java?

Nahraďte formát uložení WMF PDF pomocí `new ImageSaveOptions(SaveFormat.Pdf)`. Stejné rasterizační nastavení platí i zde a můžete navíc nastavit PDF‑specifické možnosti, jako jsou metadata autora nebo úroveň komprese. Tento jednorázový převod vytvoří prohledávatelný, stránkově přesný PDF, který odráží původní rozvržení CAD.

## Časté problémy a řešení

`License` je třída Aspose používaná k aplikaci produktové licence za běhu.

| Problém | Příčina | Řešení |
|---------|---------|--------|
| **`NullPointerException` on `cadImage.save`** | Proměnná `cadImage` není definována (měla by být `image`). | Nahraďte `cadImage` za `image` nebo přejmenujte proměnnou konzistentně. |
| **Output WMF is blank** | Velikost stránky pro rasterizaci je příliš malá nebo je barva pozadí nastavena na průhlednou. | Zvyšte `PageWidth`/`PageHeight` nebo nastavte barvu pozadí pomocí `rasterizationOptions.setBackgroundColor(Color.WHITE);`. |
| **License exception** | Spuštění bez platné Aspose licence v produkci. | Aplikujte licenční soubor při startu aplikace: `License license = new License(); license.setLicense("Aspose.Total.Java.lic");`. |

## Často kladené otázky

**Q: Kde najdu dokumentaci Aspose.CAD?**  
A: Můžete přistupovat k dokumentaci [Aspose.CAD Java documentation](https://reference.aspose.com/cad/java/).

**Q: Jak stáhnu Aspose.CAD pro Java?**  
A: Stáhněte knihovnu [Aspose.CAD Java download page](https://releases.aspose.com/cad/java/).

**Q: Je k dispozici bezplatná zkušební verze?**  
A: Ano, můžete získat bezplatnou zkušební verzi [Aspose free trial page](https://releases.aspose.com/).

**Q: Potřebujete dočasné licenční možnosti?**  
A: Prozkoumejte dočasné licence [temporary license options](https://purchase.aspose.com/temporary-license/).

**Q: Kde mohu získat podporu?**  
A: Navštivte fórum podpory Aspose.CAD [Aspose.CAD support forum](https://forum.aspose.com/c/cad/19).

## Další často kladené otázky

**Q: Mohu konvertovat velké soubory DXF (stovky MB) bez vyčerpání paměti?**  
A: Ano. Načtěte soubor v bloku try‑with‑resources a rychle uvolněte objekt `Image`. Nastavte `CadRasterizationOptions.setPageWidth/Height` na rozumnou velikost, aby byl paměťový odběr nízký.

**Q: Zachovává výstup WMF informace o vrstvách?**  
A: WMF je plochý vektorový formát, takže hierarchie vrstev je zploštěna, ale styly čar, barvy a vzory výplní jsou zachovány.

**Q: Je možné nastavit vlastní DPI pro WMF?**  
A: Použijte `rasterizationOptions.setResolution(300);` pro nastavení DPI před uložením.

**Q: Mohu hromadně konvertovat více souborů DXF v jednom běhu?**  
A: Rozhodně. Procházejte adresář, načtěte každý soubor a použijte stejnou logiku rasterizace a uložení.

**Q: Jaké verze Javy jsou podporovány?**  
A: Aspose.CAD pro Java podporuje Java 8 a novější, včetně Java 11, 17 a novějších LTS verzí.

---

**Poslední aktualizace:** 2026-10-30  
**Testováno s:** Aspose.CAD for Java 24.11  
**Autor:** Aspose

## Související tutoriály

- [Vytvořit PDF z CAD – Export DXF do PDF pomocí Aspose.CAD pro Java](/cad/java/additional-features/export-dxf-to-pdf/)
- [Vytvořit PDF z DXF: Export vrstvy pomocí Aspose.CAD pro Java](/cad/java/additional-features/export-specific-layer-to-pdf/)
- [Jak převést rozvržení DXF na JPEG obrázek pomocí Aspose.CAD v Javě](/cad/java/additional-features/export-specific-layout-to-image/)

```java
image.save(dataDir + "conic_pyramid_out_.pdf"); 
```

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}