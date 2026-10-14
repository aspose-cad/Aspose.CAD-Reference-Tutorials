---
date: 2026-10-14
description: Zjistěte, jak Java CAD knihovna Aspose.CAD pro Java může rychle a přesně
  exportovat DWG do PDF nebo rastrových obrázků.
keywords:
- export dwg pdf
- high quality pdf
- dwg to pdf tutorial
- aspose cad java
- java cad library
lastmod: 2026-10-14
linktitle: Export DWG PDF a rastrových obrázků
og_description: Exportujte DWG PDF rychle s Aspose.CAD pro Java. Zjistěte, jak provádět
  vysoce kvalitní konverzi do PDF, možnosti rasterizace a licencování v tomto podrobném
  průvodci.
og_image_alt: Tutorial showing Java code to convert DWG drawings to PDF and raster
  formats with Aspose.CAD
og_title: Exportovat DWG PDF a rastrové obrázky pomocí Java CAD knihovny Aspose.CAD
schemas:
- author: Aspose
  dateModified: '2026-10-14'
  description: Learn how the Java CAD library Aspose.CAD for Java can export DWG to
    PDF or raster images quickly and accurately.
  headline: Export DWG PDF and raster images using Java CAD library Aspose.CAD
  type: TechArticle
- description: Learn how the Java CAD library Aspose.CAD for Java can export DWG to
    PDF or raster images quickly and accurately.
  name: Export DWG PDF and raster images using Java CAD library Aspose.CAD
  steps:
  - name: Load the DWG file
    text: First, load your DWG drawing using the `Image` class. This creates an in‑memory
      representation that Aspose.CAD can work with.
  - name: Determine unit type
    text: Understanding whether the drawing uses metric or imperial units is essential
      for correct scaling. The helper method `IsMetric` (implementation omitted for
      brevity) returns a boolean flag.
  - name: Set rasterization options
    text: The `CadRasterizationOptions` class defines rasterization parameters such
      as DPI, page size, and unit conversion. Based on the unit system, configure
      page size, scaling, and the target unit type. These options drive how the DWG
      is rasterized before being wrapped into a PDF.
  - name: Configure PDF options (pdf options cad)
    text: The `PdfOptions` class specifies PDF‑specific settings, including compression
      and metadata. Create a `PdfOptions` instance and attach the rasterization settings.
      This tells Aspose.CAD how to embed the rasterized content into the final PDF.
  - name: Save as PDF
    text: The `save` method writes the image to the given file path using the supplied
      options. Finally, export the drawing to a PDF file. The `save` method takes
      the output path and the configured `PdfOptions`. When the code finishes, you’ll
      find **Saved.pdf** in your `DWGDrawings` folder, ready for distribu
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD for Java seamlessly integrates with popular Java frameworks
      such as Spring, Jakarta EE, and Android.
    question: Can I use Aspose.CAD for Java with other Java frameworks?
  - answer: Yes, you can obtain a temporary license **[obtain a temporary license](https://purchase.aspose.com/temporary-license/)**.
    question: Is a temporary license available for Aspose.CAD for Java?
  - answer: Visit the **[Aspose.CAD forum](https://forum.aspose.com/c/cad/19)** for
      assistance from the community and Aspose engineers.
    question: Where can I find support for Aspose.CAD for Java?
  - answer: You can purchase a license **[purchase a license](https://purchase.aspose.com/buy)**.
    question: How can I purchase a license for Aspose.CAD for Java?
  - answer: Aspose.CAD for Java supports both metric and imperial units, automatically
      detecting the drawing’s unit system.
    question: What units does Aspose.CAD for Java support?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- export dwg
- aspose.cad
- java cad conversion
title: Exportovat DWG PDF a rastrové obrázky pomocí Java CAD knihovny Aspose.CAD
url: /cs/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export DWG PDF a rastrových obrázků pomocí Java CAD knihovny Aspose.CAD

## Úvod

Export DWG do PDF je častý požadavek pro inženýry, architekty a všechny, kteří potřebují sdílet CAD výkresy bez odhalení nativního formátu souboru. S **Aspose.CAD for Java** můžete **export dwg pdf** — nebo rastrové obrázky — pouze pomocí několika řádků Java kódu, přičemž zachováte vektorovou věrnost a přesnost rozvržení. Tento tutoriál vás provede načtením souboru DWG, nastavením rasterizace a uložením výsledku jako vysoce kvalitního PDF nebo obrázku. Také uvidíte, proč je Aspose.CAD preferovanou Java CAD knihovnou pro spolehlivou, multiplatformní konverzi.

Pro zaměřený průvodce pouze konverzí do PDF viz [Návod na export DWG do PDF](/java/cad-drawing-conversion/export-dwg-to-pdf/).

## Rychlé odpovědi
- **Co tento tutoriál pokrývá?** Export DWG souborů do PDF nebo rastrových obrázků pomocí Aspose.CAD for Java.  
- **Potřebuji licenci?** Pro hodnocení je k dispozici bezplatná dočasná licence; pro produkční nasazení je vyžadována plná licence.  
- **Která verze Javy je podporována?** Jakékoli prostředí Java 8+ funguje s nejnovějším Aspose.CAD Java API.  
- **Mohu převést DWG do jiných formátů obrázků?** Ano – stejné možnosti rasterizace vám umožní výstup do PNG, JPEG, BMP atd.  
- **Jak dlouho trvá konverze?** Obvykle méně než sekunda pro standardní výkresy; větší soubory mohou trvat několik sekund.

## Proč je Java CAD knihovna nejlepší volbou pro konverzi DWG?

Aspose.CAD for Java je nejlepší volbou, protože poskytuje čistě Java implementaci, která nevyžaduje žádné nativní DLL, automaticky detekuje metrické nebo imperiální jednotky, poskytuje rastrový výstup až do 1200 DPI a generuje PDF zachovávající vektory bez externích závislostí. Knihovna také nabízí flexibilní licenční model, který vám umožní začít s dočasnou licencí a rozšířit na podnikovou úroveň.

## Co je „export dwg to pdf“?

`Export dwg pdf` je proces převodu nativního souboru DWG výkresu do PDF dokumentu při zachování vektorových dat, vrstev a měřítka. Tato konverze vytváří zařízení‑nezávislý soubor, který lze zobrazit na jakékoli platformě bez potřeby AutoCADu. Protože PDF zachovává vektorové informace, text zůstává prohledávatelný a grafika ostrá při libovolném zvětšení, což je ideální pro dokumentaci, revizi klientem a archivaci.

## Proč použít Aspose.CAD Java pro tuto konverzi?

Měli byste použít Aspose.CAD Java, protože knihovna interně zpracovává převod jednotek, rasterizaci a vkládání PDF, čímž eliminuje potřebu nástrojů třetích stran nebo složitých příkazových řetězců. Její API je navrženo pro vývojáře: jediný objekt `Image` představuje výkres a několik konfiguračních objektů vám umožní jemně nastavit DPI, velikost stránky a kompresi. Výsledek je konzistentní, opakovatelný výstup napříč prostředími Windows, Linux a macOS.

## Požadavky

- Základní znalost programování v Javě.  
- Knihovna Aspose.CAD for Java nainstalována. Pokud jste ji ještě ne stáhli, získáte ji **[stáhnout Aspose.CAD for Java](https://releases.aspose.com/cad/java/)**.  
- Soubor DWG pro testování – ve vodítku je použita ukázka **Bottom_plate.dwg**.

## Import jmenných prostorů

Ve vašem Java projektu importujte potřebné třídy pro zahájení konverze:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.UnitType;
```

## Průvodce krok za krokem

### Krok 1: Načtení souboru DWG

Nejprve načtěte svůj DWG výkres pomocí třídy `Image`. Tím vytvoříte paměťovou reprezentaci, se kterou může Aspose.CAD pracovat.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Bottom_plate.dwg";
Image objImage = Image.load(srcFile);
```

### Krok 2: Určení typu jednotek

Pochopení, zda výkres používá metrické nebo imperiální jednotky, je nezbytné pro správné měřítko. Pomocná metoda `IsMetric` (implementace vynechána pro stručnost) vrací boolean flag.

```java
Boolean currentUnitIsMetric = IsMetric(objImage.getUnitType());
int currentUnitCoefficient = objImage.getUnitType();
```

### Krok 3: Nastavení možností rasterizace

Třída `CadRasterizationOptions` definuje parametry rasterizace, jako jsou DPI, velikost stránky a převod jednotek. Na základě systému jednotek nastavte velikost stránky, měřítko a cílový typ jednotek. Tyto možnosti určují, jak bude DWG rasterizován před zabalením do PDF.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();

if (currentUnitIsMetric) {
    // Metric units
    double metersCoeff = 1 / 1000.0;
    double scaleFactor = metersCoeff / currentUnitCoefficient;
    rasterizationOptions.setPageWidth((float)(210 * scaleFactor));
    rasterizationOptions.setPageHeight((float)(297 * scaleFactor));
    rasterizationOptions.setUnitType(UnitType.Millimeter);
} else {
    // Imperial units
    rasterizationOptions.setPageWidth((float)(8.27f / currentUnitCoefficient));
    rasterizationOptions.setPageHeight((float)(11.69f / currentUnitCoefficient));
    rasterizationOptions.setUnitType(UnitType.Inch);
}
```

### Krok 4: Konfigurace PDF možností (pdf options cad)

Třída `PdfOptions` určuje nastavení specifické pro PDF, včetně komprese a metadat. Vytvořte instanci `PdfOptions` a připojte nastavení rasterizace. Tím řeknete Aspose.CAD, jak vložit rasterizovaný obsah do finálního PDF.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());
```

### Krok 5: Uložení jako PDF

Metoda `save` zapíše obrázek na zadanou cestu souboru pomocí poskytnutých možností. Nakonec exportujte výkres do PDF souboru. Metoda `save` přijímá výstupní cestu a nakonfigurované `PdfOptions`.

```java
objImage.save(dataDir + "Saved.pdf", pdfOptions);
```

Po dokončení kódu najdete **Saved.pdf** ve složce `DWGDrawings`, připravený k distribuci nebo archivaci.

## Jak převést DWG na rastrové obrázky pomocí Java CAD knihovny?

Můžete převést DWG na rastrové formáty výměnou `PdfOptions` za třídu specifickou pro rastrové možnosti, jako je `PngOptions` nebo `JpegOptions`. Znovu použijte stejnou instanci `CadRasterizationOptions`, upravte výstupní formát a zavolejte metodu `save` s novým objektem možností. Tento přístup vám umožní generovat soubory PNG, JPEG, BMP nebo TIFF jednou změnou řádku, přičemž workflow zůstane konzistentní.

## Jak generovat PDF DWG pomocí PDF možností CAD?

Výše uvedený příklad již **generuje pdf dwg** výstup. Pro jemné doladění velikosti PDF povolte kompresi voláním `pdfOptions.setCompress(true)`. Můžete také vložit vlastní metadata, nastavit verzi PDF nebo přidat ochranu heslem pomocí dalších vlastností `PdfOptions`. Tyto úpravy vám poskytují plnou kontrolu nad finálním PDF bez opuštění Java kódu.

## Časté problémy a tipy

- **Nesprávná velikost stránky** – Dvakrát zkontrolujte logiku převodu jednotek; nesoulad koeficientů může vést k příliš velkým stránkám.  
- **Chybějící fonty nebo tloušťky čar** – Ujistěte se, že DWG odkazuje na všechny externí zdroje před konverzí.  
- **Výkon u velkých výkresů** – Zvyšte nastavení `DPI` v `CadRasterizationOptions` pouze když je vyžadována vyšší kvalita; nižší DPI urychlí zpracování.  
- **Licenční otázky** – Pro hodnocení můžete použít **dočasnou licenci Aspose**; pro produkční nasazení je vyžadována plná licence.

## Často kladené otázky

**Q: Mohu použít Aspose.CAD for Java s jinými Java frameworky?**  
A: Ano, Aspose.CAD for Java se bez problémů integruje s populárními Java frameworky jako Spring, Jakarta EE a Android.

**Q: Je k dispozici dočasná licence pro Aspose.CAD for Java?**  
A: Ano, můžete získat dočasnou licenci **[získat dočasnou licenci](https://purchase.aspose.com/temporary-license/)**.

**Q: Kde mohu najít podporu pro Aspose.CAD for Java?**  
A: Navštivte **[Aspose.CAD fórum](https://forum.aspose.com/c/cad/19)** pro pomoc od komunity a inženýrů Aspose.

**Q: Jak mohu zakoupit licenci pro Aspose.CAD for Java?**  
A: Můžete zakoupit licenci **[zakoupit licenci](https://purchase.aspose.com/buy)**.

**Q: Jaké jednotky Aspose.CAD for Java podporuje?**  
A: Aspose.CAD for Java podporuje jak metrické, tak imperiální jednotky, automaticky detekuje systém jednotek výkresu.

**Q: Mohu převést DWG do jiných formátů obrázků (např. PNG, JPEG) pomocí stejného API?**  
A: Rozhodně. Nahraďte `PdfOptions` vhodnými možnostmi pro rastrový obrázek (např. `PngOptions`) a znovu použijte stejný `CadRasterizationOptions`.

## Závěr

Tento tutoriál ukázal, jak **export dwg pdf** a rastrové obrázky pomocí **java cad knihovny** Aspose.CAD for Java. Dodržením průvodce krok za krokem můžete integrovat spolehlivou CAD konverzi do jakékoli Java aplikace, ať už potřebujete PDF pro dokumentaci nebo rastrové obrázky pro webové zobrazení. Čistě Java povaha knihovny, vysoká kvalita výstupu a flexibilní licencování z ní činí solidní volbu jak pro malé utility, tak pro rozsáhlé podnikově řetězce.

---

**Poslední aktualizace:** 2026-10-14  
**Testováno s:** Aspose.CAD for Java 24.10  
**Autor:** Aspose

## Související tutoriály

- [Export DWG do PDF: Specifické rozložení pomocí Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [Export DWG do PDF v Javě – Nastavení velikosti PDF stránky pomocí Aspose.CAD](/cad/java/cad-export-options/export-to-pdf/)
- [Export DWG do PDF s skrytými čarami – Aspose.CAD for Java](/cad/java/cad-text-and-formatting/support-hidden-lines-in-dwg/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}