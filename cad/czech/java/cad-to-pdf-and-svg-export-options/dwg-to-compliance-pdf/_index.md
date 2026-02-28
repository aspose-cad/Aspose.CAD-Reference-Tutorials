---
date: 2026-02-28
description: Naučte se, jak převést DWG na PDF pomocí Aspose.CAD pro Java a rychle
  a přesně vytvářet soubory kompatibilní s PDF/A1a a PDF/A1b.
linktitle: DWG to Compliance PDF
second_title: Aspose.CAD Java API
title: Převod DWG do PDF (PDF/A1a a A1b) pomocí Aspose.CAD pro Javu
url: /cs/java/cad-to-pdf-and-svg-export-options/dwg-to-compliance-pdf/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Převod DWG na PDF (PDF/A1a a A1b) pomocí Aspose.CAD pro Java

## Úvod

V moderních inženýrských a návrhových pracovních postupech je **convert DWG to PDF** každodenní požadavek pro sdílení, archivaci a dodržování průmyslových standardních formátů dokumentů. PDF/A‑1a a PDF/A‑1b jsou nejrozšířenější archivní standardy, které zaručují, že vaše výkresy se zobrazí stejným způsobem na jakémkoli systému. Aspose.CAD pro Java usnadňuje tento převod, je spolehlivý a plně programovatelný. V tomto tutoriálu se přesně naučíte, jak převést soubory DWG na PDF/A‑kompatibilní PDF pomocí několika řádků Java kódu.

## Rychlé odpovědi
- **Jaká knihovna provádí převod?** Aspose.CAD for Java  
- **Které standardy PDF/A jsou podporovány?** PDF/A‑1a a PDF/A‑1b  
- **Potřebuji licenci pro testování?** Ano – dočasná licence je k dispozici od Aspose.  
- **Jaká je minimální verze Javy?** Doporučuje se Java 8 nebo novější.  
- **Mohu hromadně zpracovávat více souborů DWG?** Rozhodně – opakujte kroky pro každý soubor nebo projděte složku ve smyčce.

## Co je “convert DWG to PDF” a proč je to důležité?

Převod výkresu DWG na PDF vytvoří univerzálně zobrazitelný dokument při zachování vektorové věrnosti. Když zvolíte soulad s PDF/A‑1a nebo PDF/A‑1b, soubor také vloží barevné profily, písma a metadata potřebná pro dlouhodobou archivaci, což je nezbytné pro regulační podání, stavební dokumentaci a dodávky klientům.

## Proč použít Aspose.CAD pro Java?

- **Plná podpora verzí DWG** – od starších R12 až po nejnovější vydání.  
- **Žádné externí závislosti** – knihovna funguje ihned, není potřeba žádný CAD software.  
- **Detailní kontrola** – můžete nastavit možnosti rasterizace, DPI, velikost stránky a soulad s PDF/A.  
- **Vysoký výkon** – vhodné pro hromadné zpracování tisíců výkresů.

## Požadavky

Před začátkem se ujistěte, že máte:

- Vývojové prostředí Java (JDK 8 nebo novější) s vaším oblíbeným IDE.  
- Knihovnu Aspose.CAD pro Java – stáhněte ji z [download link](https://releases.aspose.com/cad/java/).  
- Složku, která obsahuje DWG výkresy, které chcete převést.

## Import jmenných prostorů

Nejprve importujte třídy, které budete potřebovat. Udržení importů na začátku souboru usnadňuje čtení a údržbu kódu.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfCompliance;
import com.aspose.cad.imageoptions.PdfDocumentOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Krok 1: Nastavte adresář zdrojů

Definujte cestu, kde se nacházejí vaše soubory DWG. Upravit řetězec tak, aby ukazoval na vaši skutečnou složku.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

## Krok 2: Načtěte soubor DWG

Použijte `Image.load` k načtení souboru DWG do paměti. Tento objekt bude později uložen jako PDF.

```java
String srcFile = dataDir + "Bottom_plate.dwg";
Image objImage = Image.load(srcFile);
```

## Krok 3: Vytvořte PDF možnosti

Vytvořte instanci `PdfOptions` a připojte objekt `CadRasterizationOptions`. Možnosti rasterizace vám umožní řídit, jak jsou vektorová data vykreslena v PDF.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());
```

## Krok 4: Nastavte základní PDF možnosti (Soulad)

Zde říkáte Aspose.CAD, jakou úroveň souladu s PDF/A potřebujete. Příklad začíná s PDF/A‑1a.

```java
pdfOptions.setCorePdfOptions(new PdfDocumentOptions());
pdfOptions.getCorePdfOptions().setCompliance(PdfCompliance.PdfA1a);
```

## Krok 5: Uložte PDF se souladem PDF/A‑1a

Nyní zapíšete PDF soubor na disk. Výstupní soubor bude splňovat PDF/A‑1a, připravený pro archivaci.

```java
objImage.save(dataDir + "Saved1.pdf", pdfOptions);
```

## Krok 6: Změňte soulad na PDF/A‑1b a uložte znovu

Pokud potřebujete místo toho PDF/A‑1b, stačí přepnout příznak souladu a uložit druhý soubor.

```java
pdfOptions.getCorePdfOptions().setCompliance(PdfCompliance.PdfA1b);
objImage.save(dataDir + "Saved.pdf", pdfOptions);
```

> **Tip:** Zabalte logiku převodu do znovupoužitelné metody, abyste ji mohli volat pro každý DWG ve složce, čímž snížíte duplicitní kód a zlepšíte udržovatelnost.

## Běžné případy použití

| Scénář | Proč PDF/A? |
|----------|------------|
| **Regulační podání** | Zaručuje dlouhodobou čitelnost a právní přijatelnost. |
| **Dodávky klientům** | Klienti mohou soubor otevřít bez jakéhokoli CAD softwaru. |
| **Systémy správy dokumentů** | PDF/A soubory jsou indexovány a prohledávatelné ve většině DMS platforem. |

## Běžné problémy a řešení

- **Chybějící písma nebo symboly** – Ujistěte se, že soubor DWG obsahuje všechna potřebná písma, nebo nastavte `CadRasterizationOptions.setEmbedFonts(true)`.  
- **Velká velikost souboru** – Snižte DPI v možnostech rasterizace nebo povolte kompresi pomocí `PdfDocumentOptions.setCompress(true)`.  
- **Licence nebyla nalezena** – Aplikujte dočasnou nebo trvalou licenci před převodem; jinak se objeví vodoznak.

## Často kladené otázky

**Q: Je Aspose.CAD kompatibilní se všemi verzemi souborů DWG?**  
A: Aspose.CAD podporuje širokou škálu verzí DWG, včetně nejnovějších vydání. Viz [documentation](https://reference.aspose.com/cad/java/) pro podrobný seznam kompatibility.

**Q: Mohu přizpůsobit nastavení výstupu PDF?**  
A: Rozhodně! Možnosti jako velikost stránky, DPI, vektorová rasterizace a soulad s PDF/A jsou všechny konfigurovatelné přes `PdfOptions` a `CadRasterizationOptions`.

**Q: Je k dispozici dočasná licence pro testování?**  
A: Ano, můžete získat dočasnou licenci pro hodnocení z [this link](https://purchase.aspose.com/temporary-license/).

**Q: Kde mohu získat komunitní podporu?**  
A: [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) je skvělé místo pro kladení otázek a sdílení zkušeností.

**Q: Můžu vyzkoušet Aspose.CAD zdarma před zakoupením?**  
A: Samozřejmě! Stáhněte si bezplatnou zkušební verzi z [here](https://releases.aspose.com/) a prozkoumejte kompletní sadu funkcí.

---

**Last Updated:** 2026-02-28  
**Testováno s:** Aspose.CAD for Java 24.11 (latest at time of writing)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}