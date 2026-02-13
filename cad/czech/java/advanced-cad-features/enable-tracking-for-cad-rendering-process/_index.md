---
date: 2026-02-12
description: Naučte se, jak nastavit velikost stránky PDF při převodu CAD do PDF pomocí
  Aspose.CAD pro Javu. Postupujte podle tohoto krok‑za‑krokem průvodce, abyste povolili
  sledování, převáděli CAD do PDF a efektivně ukládali CAD jako PDF.
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

V tomto tutoriálu se naučíte, jak **nastavit velikost stránky PDF** při **konverzi CAD do PDF** pomocí **Aspose.CAD for Java**. Povolením sledování získáte úplnou přehlednost o pipeline vykreslování, což usnadní ladění a optimalizaci konverze souborů CAD (např. DXF) do PDF. Ať už potřebujete **uložit CAD jako PDF**, generovat PDF z DXF, nebo jen kontrolovat rozměry výstupu, níže uvedené kroky vás provedou celým procesem.

## Rychlé odpovědi
- **Co dělá „nastavit velikost stránky PDF“?** Definuje šířku a výšku výsledné stránky PDF během vykreslování CAD.  
- **Proč povolit sledování?** Sledování zaznamenává každou fázi konverze, pomáhá odhalit úzká místa výkonu nebo chyby.  
- **Potřebuji licenci?** Bezplatná zkušební verze stačí pro hodnocení; pro produkční nasazení je vyžadována komerční licence.  
- **Jaké formáty CAD jsou podporovány?** DWG, DXF, DGN a mnoho dalších – kompletní seznam najdete v dokumentaci Aspose.CAD.  
- **Mohu měnit rozměry stránky za běhu?** Ano – jednoduše upravte hodnoty `PageWidth` a `PageHeight` v `CadRasterizationOptions`.

## Co znamená „nastavit velikost stránky PDF“ při vykreslování CAD?

Nastavení velikosti stránky PDF říká rasterizéru, jak velké má být plátno, když se vektorová data CAD převádějí na stránku PDF. To je klíčové pro zachování vizuální věrnosti, zejména u detailních technických výkresů.

## Proč povolit sledování při vykreslování CAD?

Povolení sledování poskytuje podrobný záznam každého kroku – od načtení zdrojového souboru po zápis výstupního PDF. Pomáhá vám:

- Diagnostikovat, proč se konkrétní výkres vykresluje nesprávně.  
- Změřit čas potřebný pro každou fázi, což je užitečné při ladění výkonu.  
- Ověřit, že nastavená velikost stránky byla skutečně použita.

## Předpoklady

Před nastavením sledování se ujistěte, že máte následující předpoklady:

1. **Java Development Environment** – Java 8 nebo novější nainstalovaná na vašem počítači.  
2. **Aspose.CAD Library** – Stáhněte a integrujte knihovnu Aspose.CAD do svého Java projektu. Odkaz ke stažení najdete [zde](https://releases.aspose.com/cad/java/).  
3. **Document Directory** – Připravte adresář pro uložení vašich CAD souborů a generovaných PDF.

## Import Namespaces

Ve vašem Java projektu importujte potřebné jmenné prostory, abyste mohli využívat funkce Aspose.CAD. Přidejte následující řádky na začátek kódu:

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

Uveďte cestu k vašemu CAD souboru, přičemž se ujistěte, že se nachází v určeném adresáři dokumentů.

## Nastavení možností výstupu PDF

```java
OutputStream stream = new FileOutputStream(dataDir + "conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
```

Vytvořte výstupní stream a nastavte možnosti PDF pro konverzi.

## Konfigurace CadRasterizationOptions (Nastavení velikosti stránky PDF)

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);
cadRasterizationOptions.setPageHeight(600);
```

Zde **nastavujeme velikost stránky PDF** definováním `PageWidth` a `PageHeight`. Upravené hodnoty odpovídají rozměrům požadovaným pro váš technický výkres. Toto je klíčový krok, který odpovídá na otázku **jak nastavit velikost PDF**, když **java cad to pdf**.

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

| Příznak | Pravděpodobná příčina | Oprava |
|---------|-----------------------|--------|
| Stránka PDF je prázdná | `PageWidth`/`PageHeight` nastaveny na 0 | Zajistěte, aby byly zadány nenulové rozměry. |
| Výstupní soubor je poškozený | Výstupní stream není uzavřen | Zavolejte `stream.close()` po `image.save(...)`. |
| V PDF chybí vrstvy | CAD soubor používá nepodporované entity | Ověřte, že formát souboru je plně podporován Aspose.CAD. |

## Často kladené otázky

### Q1: Je Aspose.CAD kompatibilní se všemi formáty CAD souborů?

A1: Aspose.CAD podporuje širokou škálu CAD formátů, včetně DWG, DXF, DGN a dalších. Kompletní seznam najdete v [dokumentaci](https://reference.aspose.com/cad/java/).

### Q2: Mohu přizpůsobit rozměry výstupního PDF souboru?

A2: Rozhodně! Upravením parametrů `PageWidth` a `PageHeight` v `CadRasterizationOptions` můžete nastavit požadované rozměry výstupu.

### Q3: Je k dispozici bezplatná zkušební verze Aspose.CAD for Java?

A3: Ano, schopnosti Aspose.CAD můžete vyzkoušet získáním bezplatné zkušební verze [zde](https://releases.aspose.com/).

### Q4: Jak získat podporu komunity pro dotazy související s Aspose.CAD?

A4: Navštivte [forum Aspose.CAD](https://forum.aspose.com/c/cad/19), kde můžete komunikovat s komunitou a žádat o pomoc.

### Q5: Existují dočasné licence pro Aspose.CAD?

A5: Ano, pokud potřebujete dočasnou licenci, můžete ji získat [zde](https://purchase.aspose.com/temporary-license/).

## Závěr

Gratulujeme! Nyní jste se naučili, jak **nastavit velikost stránky PDF** a povolit sledování pro vykreslování CAD pomocí **Aspose.CAD for Java**. Tento průvodce vás vybavuje k **konverzi CAD do PDF**, **ukládání CAD jako PDF** a generování PDF z DXF s plnou kontrolou nad rozměry stránky a podrobnými výkonnostními záznamy. Nebojte se experimentovat s různými velikostmi stránek a prozkoumat další možnosti rasterizace, aby vyhovovaly vašim specifickým inženýrským workflow.

---

**Poslední aktualizace:** 2026-02-12  
**Testováno s:** Aspose.CAD for Java 24.12 (nejnovější v době psaní)  
**Autor:** Aspose  

---

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}