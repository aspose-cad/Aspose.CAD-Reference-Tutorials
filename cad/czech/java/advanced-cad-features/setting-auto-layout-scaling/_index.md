---
date: 2026-08-29
description: Naučte se, jak nastavit vlastní velikost stránky PDF a vytvořit PDF z
  CAD pomocí Aspose.CAD pro Java. Tento podrobný průvodce popisuje export CAD do PDF
  s Auto Layout Scaling.
keywords:
- custom pdf page size
- create pdf from cad
- dwg to pdf java
- custom page size pdf
- java convert cad pdf
lastmod: 2026-08-29
linktitle: Nastavení Auto Layout Scaling
og_description: Nastavte vlastní velikost stránky PDF při konverzi souborů CAD do
  PDF pomocí Aspose.CAD pro Java. Postupujte podle podrobného průvodce, použijte Auto
  Layout Scaling a dosáhněte dokonalých výsledků rozložení.
og_image_alt: 'Tutorial: set custom pdf page size for CAD to PDF conversion using
  Aspose.CAD Java'
og_title: Nastavte vlastní velikost stránky PDF pro export CAD PDF – Aspose.CAD Java
schemas:
- author: Aspose
  dateModified: '2026-08-29'
  description: Learn how to set a custom pdf page size and create PDF from CAD using
    Aspose.CAD for Java. This step‑by‑step guide covers export CAD to PDF with Auto
    Layout Scaling.
  headline: How to set custom pdf page size for CAD PDF export
  type: TechArticle
- description: Learn how to set a custom pdf page size and create PDF from CAD using
    Aspose.CAD for Java. This step‑by‑step guide covers export CAD to PDF with Auto
    Layout Scaling.
  name: How to set custom pdf page size for CAD PDF export
  steps:
  - name: load the CAD file
    text: Loading the source file is the first step in **how to export CAD** to a
      PDF document.
  - name: create rasterization options
    text: The `CadRasterizationOptions` class defines how the CAD drawing is rasterized
      and which page dimensions to use. It also lets you control DPI, background color,
      and other rendering details.
  - name: set auto layout scaling
    text: Enable the automatic scaling feature. This is the core of **how to set scaling**
      for a CAD‑to‑PDF conversion.
  - name: create PDF options
    text: Link the rasterization settings to the PDF export options.
  - name: export to PDF
    text: Finally, save the rendered image as a PDF file. This step completes the
      **convert dxf to pdf** workflow. Repeat the steps above for any additional CAD
      files you need to process, whether they are **DWG**, **DWF**, or other supported
      formats.
  type: HowTo
- questions:
  - answer: Aspose.CAD for Java supports a broad range of formats, including DWG,
      DXF, DWF, and more than 30 additional CAD types.
    question: Is Aspose.CAD for Java compatible with all CAD file formats?
  - answer: Yes, the `CadRasterizationOptions` class provides properties for fine‑tuning
      scaling, DPI, background color, and other rasterization settings.
    question: Can I customize the scaling options further?
  - answer: Refer to the [documentation](https://reference.aspose.com/cad/java/) for
      in‑depth information and examples.
    question: Where can I find additional documentation for Aspose.CAD for Java?
  - answer: Yes, you can explore a [free trial](https://releases.aspose.com/) to experience
      the capabilities of Aspose.CAD for Java.
    question: Is there a free trial available for Aspose.CAD for Java?
  - answer: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) to connect
      with the community and seek support.
    question: How can I seek assistance or engage in discussions about Aspose.CAD
      for Java?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- custom pdf page size
- Aspose.CAD
- Java CAD conversion
title: Jak nastavit vlastní velikost stránky PDF pro export CAD PDF
url: /cs/java/advanced-cad-features/setting-auto-layout-scaling/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Nastavit vlastní velikost PDF stránky – vytvořit PDF z CAD s automatickým škálováním rozvržení

## Úvod

Pokud potřebujete **nastavit vlastní velikost PDF stránky** při **vytváření PDF z CAD** souborů rychle a s dokonalým škálováním, Aspose.CAD pro Java vám to umožní. Auto Layout Scaling automaticky mění velikost CAD rozvržení tak, aby vyplnily cílové rozměry stránky, čímž zajistí, že výsledné PDF odpovídá zamýšlené velikosti listu bez ohledu na původní výkres. V tomto tutoriálu projdeme kompletní proces – od načtení DXF souboru po export PDF – a zdůrazníme **export CAD do PDF** možnosti knihovny a ukážeme, jak můžete také **převést DWG na PDF** nebo **zvýšit rozlišení PDF**, pokud je to potřeba.

## Rychlé odpovědi
- **Co dělá Auto Layout Scaling?** Automaticky mění velikost CAD rozvržení tak, aby se vešla do cílových rozměrů stránky při rasterizaci.  
- **Jaké CAD formáty mohu převést?** Jakýkoli formát podporovaný Aspose.CAD (např. DXF, DWG, DWF) lze převést do PDF.  
- **Potřebuji licenci pro produkční použití?** Ano, pro ne‑evaluační použití je vyžadována komerční licence.  
- **Jak dlouho trvá typický převod?** Na moderním hardwaru se standardní soubor převádí za méně než sekundu.  
- **Mohu změnit velikost stránky?** Samozřejmě – použijte `CadRasterizationOptions` k nastavení vlastních rozměrů stránky.

## Co je „vytvořit PDF z CAD“?

Vytvoření PDF z CAD znamená převést vektorový inženýrský výkres (DXF, DWG, atd.) na rastrový PDF dokument. PDF zachová vizuální věrnost původního výkresu a bude široce zobrazitelné na jakékoli platformě, a může být otevřeno na zařízeních, která nepodporují nativní CAD formáty.

## Proč použít automatické škálování rozvržení?

Auto Layout Scaling zaručuje, že každé rozvržení plně vyplní PDF stránku bez ručních výpočtů, šetří vám čas a eliminuje chyby škálování. Také zajišťuje, že tloušťky čar a barvy jsou přesně zachovány napříč různými výstupními velikostmi. Poskytuje konzistentní, vysoce kvalitní výstup u desítek CAD souborů a podporuje dávkové zpracování pro velké projekty.

## Předpoklady

1. **Aspose.CAD pro Java knihovna** – stáhněte nejnovější verzi ze [stránky ke stažení](https://releases.aspose.com/cad/java/).  
2. **Adresář zdrojů** – vytvořte složku na svém počítači pro uložení CAD souborů; nahraďte `"Your Document Directory"` v kódu touto cestou.  
3. **Ukázkový CAD soubor** – pro tento návod použijeme `conic_pyramid.dxf`, který je součástí sady vzorových dat Aspose.

## Importovat jmenné prostory

Nejprve importujte požadované třídy. To nám poskytne přístup k načítání obrázků, rasterizaci a funkcím exportu PDF.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Jak nastavit vlastní velikost stránky pro PDF z CAD

Než se pustíme do krok‑za‑krokem kódu, objasníme, proč jsou vlastní rozměry stránky důležité. Nastavení **vlastní velikosti PDF stránky** vám umožní odpovídat průmyslovým standardům (A4, A1, Letter) nebo definovat vlastní plátno, což je nezbytné pro regulační podání, technické příručky nebo vysoce rozlišené tiskové úlohy.

### Krok 1: načíst CAD soubor

Načtení zdrojového souboru je prvním krokem v **tom, jak exportovat CAD** do PDF dokumentu.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

### Krok 2: vytvořit rasterizační možnosti

Třída `CadRasterizationOptions` definuje, jak je CAD výkres rasterizován a jaké rozměry stránky se použijí. Také vám umožní řídit DPI, barvu pozadí a další podrobnosti renderování.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
```

### Krok 3: nastavit automatické škálování rozvržení

Povolte funkci automatického škálování. Toto je jádro **tomu, jak nastavit škálování** pro převod CAD‑na‑PDF.

```java
rasterizationOptions.setAutomaticLayoutsScaling(true);
```

### Krok 4: vytvořit PDF možnosti

Propojte rasterizační nastavení s možnostmi exportu PDF.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Krok 5: exportovat do PDF

Nakonec uložte vykreslený obrázek jako PDF soubor. Tento krok dokončuje **workflow převodu dxf na pdf**.

```java
image.save(dataDir + "result_out_.pdf", pdfOptions);
```

Opakujte výše uvedené kroky pro jakékoli další CAD soubory, které potřebujete zpracovat, ať už jsou to **DWG**, **DWF**, nebo jiné podporované formáty.

## Běžné případy použití

| Scénář | Proč nastavit vlastní velikost stránky? |
|----------|-----------------------------|
| **Podání stavebního výkresu** | Zarovnává PDF s běžnými formáty A1/A2 požadovanými regulačními orgány. |
| **Vkládání do technických příruček** | Zaručuje, že výkres zapadne do předdefinovaného rozvržení příručky bez dalšího škálování. |
| **Vysoké rozlišení tisku** | Umožňuje zvýšit DPI (např. `rasterizationOptions.setResolution(300)`) při zachování konzistentních rozměrů stránky. |

## Běžné problémy a řešení

| Příznak | Pravděpodobná příčina | Oprava |
|---------|--------------|-----|
| Prázdný PDF výstup | Rasterizační možnosti nejsou nastaveny nebo je špatná cesta k souboru | Ověřte cestu `srcFile` a ujistěte se, že `setPageWidth/Height` nejsou nula |
| Deformované škálování | `setAutomaticLayoutsScaling` zůstalo `false` | Povolte automatické škálování nebo ručně vypočítejte škálovací faktor |
| Chybějící vrstvy | Zdrojový DXF obsahuje nepodporované entity | Zkontrolujte poznámky k vydání Aspose.CAD pro podporované typy entit |

Aspose.CAD podporuje převod **30+ CAD formátů** a může zpracovat soubory až do **500 MB** bez načítání celého dokumentu do paměti, což poskytuje rychlé, paměťově úsporné převody pro podnikovou zátěž.

## Často kladené otázky

**Q: Je Aspose.CAD pro Java kompatibilní se všemi CAD formáty?**  
A: Aspose.CAD pro Java podporuje širokou škálu formátů, včetně DWG, DXF, DWF a více než 30 dalších CAD typů.

**Q: Mohu dále přizpůsobit možnosti škálování?**  
A: Ano, třída `CadRasterizationOptions` poskytuje vlastnosti pro jemné ladění škálování, DPI, barvy pozadí a dalších rasterizačních nastavení.

**Q: Kde najdu další dokumentaci k Aspose.CAD pro Java?**  
A: Viz [dokumentace](https://reference.aspose.com/cad/java/) pro podrobné informace a příklady.

**Q: Je k dispozici bezplatná zkušební verze Aspose.CAD pro Java?**  
A: Ano, můžete vyzkoušet [bezplatnou verzi](https://releases.aspose.com/) a poznat možnosti Aspose.CAD pro Java.

**Q: Jak mohu získat podporu nebo se zapojit do diskusí o Aspose.CAD pro Java?**  
A: Navštivte [forum Aspose.CAD](https://forum.aspose.com/c/cad/19), kde se můžete spojit s komunitou a získat podporu.

**Další časté otázky**

**Q: Jak převést DWG soubor na PDF místo DXF?**  
A: Stejný kód funguje; stačí změnit příponu souboru v `srcFile` na `.dwg`.

**Q: Mohu nastavit vlastní DPI pro PDF s vyšším rozlišením?**  
A: Ano, použijte `rasterizationOptions.setResolution(300);` (nebo jakékoliv DPI, které potřebujete).

**Q: Je možné vložit písma do generovaného PDF?**  
A: Aspose.CAD rasterizuje výkres, takže písma jsou vykreslena jako vektory; samostatné vkládání písem není vyžadováno.

## Závěr

Po přečtení tohoto průvodce nyní víte, jak **nastavit vlastní velikost PDF stránky** a **vytvořit PDF z CAD** souborů pomocí Aspose.CAD pro Java s Auto Layout Scaling. Proces zjednodušuje **export CAD do PDF** workflow, zajišťuje konzistentní škálování a šetří vám cenný čas vývoje. Nebojte se experimentovat s různými velikostmi stránek, rozlišením a CAD formáty, aby vyhovovaly potřebám vašeho projektu, ať už **převádíte DWG na PDF**, **zvyšujete rozlišení PDF**, nebo budujete **java CAD na PDF** dávkový procesor.

---

**Poslední aktualizace:** 2026-08-29  
**Testováno s:** Aspose.CAD pro Java 24.12 (nejnovější)  
**Autor:** Aspose

## Související tutoriály

- [Jak nastavit velikost PDF stránky a povolit sledování procesu renderování CAD pomocí Aspose.CAD pro Java](/cad/java/advanced-cad-features/enable-tracking-for-cad-rendering-process/)
- [Nastavit velikost PDF stránky – převést CAD na PDF (Java)](/cad/java/advanced-cad-features/set-canvas-size-and-mode/)
- [Rychle exportovat DWG do PDF nebo rastrově pomocí java CAD knihovny Aspose.CAD pro Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}