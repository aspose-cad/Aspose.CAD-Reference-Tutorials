---
date: 2026-06-29
description: Naučte se, jak vytvořit PDF z DWG a přizpůsobit rozvržení PDF pomocí
  Aspose.CAD for Java. Snadná integrace pro vývojáře Java.
keywords:
- create pdf from dwg
- convert cad to pdf
- pdf different page sizes
- export dwg to pdf
- customize pdf layout
linktitle: Jedno PDF s různými rozvrženími
schemas:
- author: Aspose
  dateModified: '2026-06-29'
  description: Learn how to create PDF from DWG and customize PDF layout using Aspose.CAD
    for Java. Easy integration for Java developers.
  headline: Create PDF from DWG with Aspose.CAD for Java
  type: TechArticle
- questions:
  - answer: Yes, Aspose.CAD for Java integrates seamlessly with libraries such as
      Apache POI, Jackson, or Spring Boot.
    question: Can I use Aspose.CAD for Java with other Java libraries?
  - answer: Absolutely! You can access a free trial version [here](https://releases.aspose.com/).
    question: Is there a trial version available?
  - answer: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for community
      support and discussions.
    question: Where can I find additional support?
  - answer: You can obtain a temporary license [here](https://purchase.aspose.com/temporary-license/).
    question: How do I obtain a temporary license?
  - answer: Purchase the full version of Aspose.CAD for Java [here](https://purchase.aspose.com/buy).
    question: Where can I purchase the full version?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Vytvořte PDF z DWG pomocí Aspose.CAD for Java
url: /cs/java/other-cad-operations/single-pdf-different-layouts/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Vytvoření PDF z DWG pomocí Aspose.CAD pro Java

## Úvod

V tomto tutoriálu **vytvoříte PDF z DWG** souborů a použijete několik rozvržení velikostí stránek pomocí Aspose.CAD pro Java. Ať už potřebujete generovat stavební výkresy, inženýrské schémata nebo marketingové PDF, níže uvedené kroky vám ukážou, jak převést CAD výkresy do PDF, přizpůsobit rozměry každého rozvržení a vytvořit jeden vícestránkový dokument – vše bez opuštění vašeho Java prostředí.

## Rychlé odpovědi
- **Co tutoriál pokrývá?** Převod DWG výkresu do jednoho PDF s více velikostmi stránek.  
- **Která knihovna je vyžadována?** Aspose.CAD pro Java (nejnovější verze).  
- **Potřebuji licenci?** Bezplatná zkušební verze funguje pro vývoj; pro produkci je vyžadována komerční licence.  
- **Mohu exportovat i jiné formáty?** Ano – API také podporuje export do PNG, JPEG a SVG.  
- **Je Java 8 dostačující?** Knihovna funguje s Java 8 a novějšími runtimey.

## Co znamená „vytvořit pdf z dwg“?

**Vytvořit PDF z DWG** znamená převést nativní soubor AutoCAD DWG do PDF dokumentu při zachování vektorové věrnosti, vrstev a tlouštěk čar a umožnit přizpůsobení rozvržení. Aspose.CAD provádí tento převod kompletně v paměti, takže není potřeba externí CAD software a výsledné PDF lze přímo upravovat nebo tisknout.

## Proč přizpůsobit rozvržení PDF z DWG?

Aspose.CAD podporuje **více než 30 CAD formátů** a může generovat PDF až do **500 MB** bez načítání celého souboru do paměti. Definováním individuálních velikostí stránek pro každé rozvržení můžete vytvořit tiskové listy odpovídající ISO, ANSI nebo vlastním rozměrům – kvantifikovatelný přínos, který šetří čas a eliminuje ruční post‑processing.

## Předpoklady

Než se pustíme do práce, ujistěte se, že máte připravené následující předpoklady:
- Java prostředí: Ujistěte se, že máte na svém počítači nainstalovanou Javu.  
- Aspose.CAD knihovna: Stáhněte a nainstalujte knihovnu Aspose.CAD pro Java z [odkazu ke stažení](https://releases.aspose.com/cad/java/).  
- Složka dokumentů: Vytvořte složku pro své DWG výkresy.

## Import balíčků

Třída `CadImage` je jádrový objekt Aspose.CAD, který představuje CAD výkres v paměti. Načtěte potřebné jmenné prostory před zahájením práce:

```java
import com.aspose.cad.Image;
import com.aspose.cad.SizeF;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.VectorRasterizationOptions;
```

## Krok 1: Načtení CAD výkresu

`CadImage` načte DWG soubor a poskytne přístup k jeho vektorovým datům. Začněte načtením svého CAD výkresu do objektu `CadImage`:

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
CadImage cadImage = (CadImage)Image.load(dataDir + "City skyway map.dwg");
```

## Krok 2: Nastavení možností rasterizace

`RasterizationOptions` určuje, jak jsou CAD vektory rasterizovány před vložením do PDF. Nastavte možnosti rasterizace pro CAD obrázek:

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1000);
rasterizationOptions.setPageHeight(1000);
```

## Krok 3: Přizpůsobení velikostí stránek rozvržení

`PdfOptions` vám umožňuje přiřadit odlišné rozměry stránek každému rozvržení uvnitř DWG. Definujte vlastní velikosti pro několik rozvržení v CAD výkresu:

```java
rasterizationOptions.getLayoutPageSizes().addItem("ANSI C Plot", new SizeF(500, 1000));
rasterizationOptions.getLayoutPageSizes().addItem("8.5 x 11 Plot", new SizeF(1000, 100));
```

## Krok 4: Nastavení PDF možností

`PdfOptions` je kontejner, který kombinuje nastavení rasterizace a definice rozvržení. Nakonfigurujte PDF možnosti, zahrnující nastavení rasterizace:

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Krok 5: Uložení jako PDF

`PdfSaveOptions` dokončuje převod a zapíše výstupní soubor. Uložte zpracovaný CAD obrázek jako PDF:

```java
cadImage.save(dataDir + "singlePDF_out.pdf", pdfOptions);
```

Gratulujeme! Úspěšně jste **vytvořili pdf z dwg** s různými velikostmi stránek pomocí Aspose.CAD pro Java.

## Časté problémy a řešení

- **Prázdné stránky ve výstupním PDF** – Ujistěte se, že hodnoty `PageSize` odpovídají skutečným rozměrům rozvržení v DWG souboru.  
- **Chyby nedostatku paměti u velkých výkresů** – Použijte `CadImage.load(..., LoadOptions)` s `LoadOptions.setLoadMode(LoadMode.Memory)`, aby se soubor streamoval místo úplného načtení.  
- **Nesprávné měřítko** – Upravit `RasterizationOptions.setPageWidth` a `setPageHeight`, aby odpovídaly požadovanému DPI (bodů na palec).

## Často kladené otázky

**Q: Mohu použít Aspose.CAD pro Java s jinými Java knihovnami?**  
A: Ano, Aspose.CAD pro Java se bez problémů integruje s knihovnami jako Apache POI, Jackson nebo Spring Boot.

**Q: Je k dispozici zkušební verze?**  
A: Rozhodně! Bezplatnou zkušební verzi můžete získat [zde](https://releases.aspose.com/).

**Q: Kde najdu další podporu?**  
A: Navštivte [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) pro komunitní podporu a diskuse.

**Q: Jak získat dočasnou licenci?**  
A: Dočasnou licenci můžete získat [zde](https://purchase.aspose.com/temporary-license/).

**Q: Kde mohu zakoupit plnou verzi?**  
A: Plnou verzi Aspose.CAD pro Java zakoupíte [zde](https://purchase.aspose.com/buy).

---

**Poslední aktualizace:** 2026-06-29  
**Testováno s:** Aspose.CAD pro Java 24.10  
**Autor:** Aspose

## Související tutoriály

- [Export DWG do PDF nebo rastru pomocí Aspose.CAD pro Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [Export CAD rozvržení do PDF s Aspose.CAD pro Java](/cad/java/cad-export-options/export-cad-layouts-to-pdf/)
- [Export konkrétního DWG rozvržení do PDF pomocí Aspose.CAD pro Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< blocks/products/products-backtop-button >}}
{{< /blocks/products/pf/main-wrap-class >}}