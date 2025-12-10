---
date: 2025-12-07
description: Naučte se, jak nastavit velikost stránky PDF při převodu CAD na PDF pomocí
  Aspose.CAD pro Javu. Postupujte podle tohoto průvodce krok za krokem, abyste povolili
  sledování, převáděli CAD na PDF a efektivně ukládali CAD jako PDF.
linktitle: Set PDF Page Size – Enable Tracking for CAD Rendering
second_title: Aspose.CAD Java API
title: Jak nastavit velikost stránky PDF a povolit sledování procesu renderování CAD
url: /cs/java/advanced-cad-features/enable-tracking-for-cad-rendering-process/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Povolení sledování procesu vykreslování CAD

## Úvod

V tomto tutoriálu se naučíte, jak **nastavit velikost stránky PDF** při **převodu CAD do PDF** pomocí **Aspose.CAD for Java**. Povolením sledování získáte úplnou přehlednost o vykreslovacím řetězci, což usnadňuje ladění a optimalizaci převodu souborů CAD (např. DXF) do PDF. Ať už potřebujete **uložit CAD jako PDF**, generovat PDF z DXF, nebo jednoduše řídit rozměry výstupu, níže uvedené kroky vás provedou celým procesem.

## Rychlé odpovědi
- **Co dělá „nastavit velikost stránky PDF“?** Definuje šířku a výšku výsledné stránky PDF během vykreslování CAD.  
- **Proč povolit sledování?** Sledování zaznamenává každou fázi převodu, pomáhá odhalit úzká místa výkonu nebo chyby.  
- **Potřebuji licenci?** Bezplatná zkušební verze stačí pro hodnocení; pro produkční nasazení je vyžadována komerční licence.  
- **Jaké formáty CAD jsou podporovány?** DWG, DXF, DGN a mnoho dalších – úplný seznam najdete v dokumentaci Aspose.CAD.  
- **Mohu měnit rozměry stránky za běhu?** Ano – jednoduše upravte hodnoty `PageWidth` a `PageHeight` v `CadRasterizationOptions`.

## Co znamená „nastavit velikost stránky PDF“ při vykreslování CAD?

Nastavení velikosti stránky PDF říká rasterizátoru, jak velké má být plátno, když jsou vektorová data CAD rasterizována na stránku PDF. To je klíčové pro zachování vizuální věrnosti, zejména u detailních technických výkresů.

## Proč povolit sledování při vykreslování CAD?

Povolení sledování poskytuje podrobný záznam každého kroku – od načtení zdrojového souboru po zápis PDF výstupu. Pomáhá vám:

- Diagnostikovat, proč se konkrétní výkres může vykreslovat nesprávně.  
- Měřit čas potřebný pro každou fázi, což je užitečné při ladění výkonu.  
- Ověřit, že nastavená velikost stránky je skutečně použita.

## Požadavky

Před tím, než se pustíte do nastavení sledování, ujistěte se, že máte následující požadavky:

1. **Java vývojové prostředí** – Java 8 nebo novější nainstalovaná na vašem počítači.  
2. **Aspose.CAD knihovna** – Stáhněte a integrujte knihovnu Aspose.CAD do vašeho Java projektu. Odkaz ke stažení najdete [zde](https://releases.aspose.com/cad/java/).  
3. **Adresář dokumentů** – Připravte adresář pro uložení vašich CAD souborů a generovaných PDF.

## Importování jmenných prostorů

Ve vašem Java projektu importujte potřebné jmenné prostory pro využití funkcí Aspose.CAD. Přidejte následující řádky na začátek vašeho kódu:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;

import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Nastavení cesty k adresáři zdrojů

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

Nahraďte `"Your Document Directory"` skutečnou cestou k vašemu adresáři dokumentů.

## Načtení CAD souboru

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

Uveďte cestu k vašemu CAD souboru, ujistěte se, že se nachází v určeném adresáři dokumentů.

## Nastavení možností výstupu PDF

```java
OutputStream stream = new FileOutputStream(dataDir + "conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
```

Vytvořte výstupní stream a nastavte PDF možnosti pro převod.

## Konfigurace CadRasterizationOptions (Nastavení velikosti stránky PDF)

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);
cadRasterizationOptions.setPageHeight(600);
```

Zde **nastavujeme velikost stránky PDF** definováním `PageWidth` a `PageHeight`. Upravte tyto hodnoty tak, aby odpovídaly rozměrům požadovaným pro váš technický výkres. Tento krok přímo ovlivňuje, jak je CAD obsah škálován a vykreslen ve finálním PDF.

## Uložení PDF souboru

```java
image.save(stream, pdfOptions);
```

Uložte vykreslený PDF soubor s uvedenými možnostmi.

## Ověření povolení sledování

```java
System.out.println("Tracking enabled successfully for CAD rendering process.");
```

Potvrďte, že sledování bylo úspěšně povoleno pro proces vykreslování CAD.

## Časté problémy a řešení

| Symptom | Předpokládaná příčina | Řešení |
|---------|-----------------------|--------|
| Stránka PDF se zobrazuje prázdná | `PageWidth`/`PageHeight` nastaveno na 0 | Zajistěte, aby byly zadány nenulové rozměry. |
| Výstupní soubor je poškozen | Výstupní stream není uzavřen | Zavolejte `stream.close()` po `image.save(...)`. |
| Chybějící vrstvy v PDF | CAD soubor používá nepodporované entity | Ověřte, že formát souboru je plně podporován Aspose.CAD. |

## Často kladené otázky

### Q1: Je Aspose.CAD kompatibilní se všemi formáty CAD souborů?

A1: Aspose.CAD podporuje širokou škálu CAD formátů, včetně DWG, DXF, DGN a dalších. Podrobný seznam najdete v [dokumentaci](https://reference.aspose.com/cad/java/).

### Q2: Mohu přizpůsobit výstupní rozměry PDF souboru?

A2: Ano! Upravte parametry `PageWidth` a `PageHeight` v `CadRasterizationOptions` podle požadovaných rozměrů.

### Q3: Je k dispozici bezplatná zkušební verze Aspose.CAD pro Java?

A3: Ano, můžete si vyzkoušet možnosti Aspose.CAD získáním bezplatné zkušební verze [zde](https://releases.aspose.com/).

### Q4: Jak mohu získat komunitní podporu pro dotazy související s Aspose.CAD?

A4: Navštivte [Aspose.CAD fórum](https://forum.aspose.com/c/cad/19), kde můžete komunikovat s komunitou a požádat o pomoc.

### Q5: Jsou k dispozici dočasné licence pro Aspose.CAD?

A5: Ano, pokud potřebujete dočasnou licenci, můžete ji získat [zde](https://purchase.aspose.com/temporary-license/).

## Závěr

Gratulujeme! Nyní jste se naučili, jak **nastavit velikost stránky PDF** a povolit sledování pro vykreslování CAD pomocí **Aspose.CAD for Java**. Tento průvodce vás vybavuje pro **převod CAD do PDF**, **uložení CAD jako PDF** a generování PDF z DXF s plnou kontrolou nad rozměry stránky a podrobnými protokoly provedení. Nebojte se experimentovat s různými velikostmi stránek a prozkoumat další možnosti rasterizace, které vyhovují vašim specifickým technickým pracovním postupům.

---

**Poslední aktualizace:** 2025-12-07  
**Testováno s:** Aspose.CAD for Java 24.12 (nejnovější v době psaní)  
**Autor:** Aspose

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
