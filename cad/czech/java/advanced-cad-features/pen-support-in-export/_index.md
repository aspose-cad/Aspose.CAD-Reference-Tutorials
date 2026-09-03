---
date: 2026-08-29
description: Naučte se, jak vytvořit PDF z CAD pomocí Aspose.CAD for Java s přizpůsobením
  pera. Tento krok‑za‑krokem průvodce ukazuje, jak efektivně exportovat CAD do PDF.
keywords:
- create pdf from cad
- export cad to pdf
- convert ddx to pdf
- aspose cad java
- java convert cad pdf
lastmod: 2026-08-29
linktitle: Podpora pera při exportu
og_description: Vytvořte PDF z CAD s podporou pera pomocí Aspose.CAD for Java. Tento
  průvodce vás provede exportem CAD do PDF, přizpůsobením pera a nejlepšími postupy
  během méně než 10 minut.
og_image_alt: Screenshot of Java code exporting a CAD drawing to PDF with custom pen
  settings
og_title: Jak vytvořit PDF z CAD s podporou pera při exportu
schemas:
- author: Aspose
  dateModified: '2026-08-29'
  description: Learn how to create PDF from CAD using Aspose.CAD for Java with pen
    customization. This step‑by‑step guide shows export CAD to PDF efficiently.
  headline: How to create pdf from cad with pen support in export
  type: TechArticle
- questions:
  - answer: Converting a CAD drawing (e.g., DXF) into a PDF document while retaining
      vector quality for easy sharing and printing.
    question: What does “create PDF from CAD” mean?
  - answer: Aspose.CAD for Java’s `PenOptions` class.
    question: Which library handles pen customization?
  - answer: Yes – the same pen settings apply to PNG, BMP, TIFF, and more.
    question: Can I use this for other formats?
  - answer: A valid Aspose.CAD license is required for production use; otherwise evaluation
      mode adds a watermark.
    question: Do I need a license?
  - answer: Java 8 or higher.
    question: What’s the minimum Java version?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- create pdf from cad
- aspose cad
- java cad conversion
- pdf export
- pen support
title: Jak vytvořit PDF z CAD s podporou pera při exportu
url: /cs/java/advanced-cad-features/pen-support-in-export/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Podpora pera při exportu

## Úvod

Ve světě rychlých konverzí CAD často potřebujete **vytvořit PDF z CAD** souborů a zachovat vizuální věrnost. Aspose.CAD pro Java to usnadňuje a nabízí bohaté možnosti, jako je přizpůsobení pera, které vám umožní doladit styl čar během exportu. V tomto průvodci projdeme kompletním praktickým příkladem, který ukazuje, jak **exportovat CAD do PDF** s vlastními nastaveními pera, takže můžete přímo z výkresů DXF generovat profesionální PDF.

## Rychlé odpovědi
- **Co znamená “create PDF from CAD”?** Převod CAD výkresu (např. DXF) do PDF dokumentu při zachování vektorové kvality pro snadné sdílení a tisk.  
- **Která knihovna zajišťuje přizpůsobení pera?** Třída `PenOptions` v Aspose.CAD pro Java.  
- **Lze to použít i pro jiné formáty?** Ano – stejná nastavení pera platí pro PNG, BMP, TIFF a další.  
- **Potřebuji licenci?** Pro produkční použití je vyžadována platná licence Aspose.CAD; v režimu hodnocení se přidává vodoznak.  
- **Jaká je minimální verze Javy?** Java 8 nebo novější.

## Co znamená “create PDF from CAD”?

Vytvoření PDF z CAD znamená převod CAD výkresu (například souboru DXF) do PDF dokumentu při zachování vektorové kvality, což umožňuje snadné sdílení, tisk a archivaci bez nutnosti mít nainstalovaný CAD software. Tento převod zachovává přesnou geometrii, tloušťky čar a barvy, takže PDF věrně reprezentuje původní návrh.

## Proč použít podporu pera při exportu CAD do PDF?

Podpora pera vám umožňuje řídit zakončení čar, spoje a tloušťku, což vám dává možnost sladit výstup s firemní identitou nebo technickými standardy. Přizpůsobením per můžete zajistit, že měřicí čáry, řezy nebo zvýrazněné prvky vypadají přesně podle očekávání, což je zvláště cenné, když výchozí vykreslování nesplňuje přísné inženýrské nebo publikační požadavky.

## Jak vytvořit PDF z CAD – krok za krokem průvodce
Níže najdete praktický návod, který pokrývá vše od nastavení vývojového prostředí, načtení souboru DXF, konfigurace rasterizačních a penových možností až po generování finálního PDF. Dodržením jednotlivých kroků získáte připravené řešení pro **export CAD do PDF** s plnou kontrolou nad styly čar, zakončeními a tloušťkou.

## Požadavky

- **Java vývojové prostředí** – funkční JDK (8 nebo novější) a IDE nebo nástroj pro sestavení dle vašeho výběru.  
- **Aspose.CAD knihovna** – stáhněte nejnovější JAR z oficiální stránky [download Aspose.CAD for Java](https://releases.aspose.com/cad/java/).  
- **Ukázkový soubor DXF** – v tomto tutoriálu použijeme `conic_pyramid.dxf`.

Nyní, když máme vše připravené, pojďme se ponořit do kódu.

## Importovat jmenné prostory

Importní příkazy přinášejí požadované třídy Aspose.CAD do Java souboru, aby mohly být v kódu použity.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.PenOptions;
import com.aspose.cad.internal.imaging.LineCap;
```

## Krok 1: definovat adresář dokumentu

`dataDir` je složka, která obsahuje vaše zdrojové DXF soubory a kam bude uložen vygenerovaný PDF. Použití absolutní cesty zabraňuje nejasnostem při spuštění aplikace z různých pracovních adresářů.

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

> **Tip:** Nahraďte `"Your Document Directory"` absolutní cestou, kde se nacházejí vaše DXF soubory.

## Krok 2: načíst soubor CAD

`Image.load` načte CAD soubor a vrátí objekt `CadImage`, který představuje výkres v paměti a je připraven k dalšímu zpracování.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
CadImage cadImage = (CadImage) Image.load(srcFile);
```

Instance `CadImage` vám poskytuje přístup k možnostem rasterizace, vrstvám a dalším metadatům výkresu.

## Krok 3: nakonfigurovat možnosti rasterizace

`RasterizationOptions` určuje, jak bude CAD výkres vykreslen do mezilehlého rastrového obrazu před vložením do PDF. Úprava šířky a výšky stránky (často násobené 100) poskytuje vysoké rozlišení vhodné pro tisk.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(cadImage.getWidth() * 100);
rasterizationOptions.setPageHeight(cadImage.getHeight() * 100);
```

## Krok 4: přizpůsobit možnosti pera

`PenOptions` umožňuje nastavit počáteční a koncové zakončení pera, tloušťku čáry a styl spojů. Zde nastavujeme oba konce na `Flat`; můžete experimentovat s `Round` nebo `Square` pro různé vizuální efekty.

```java
PenOptions penOts = new PenOptions();
penOts.setStartCap(LineCap.Flat);
penOts.setEndCap(LineCap.Flat);
```

## Krok 5: nakonfigurovat možnosti exportu PDF

`PdfOptions` spojuje nastavení rasterizace s procesem exportu do PDF, zajišťuje správné vložení rastrového obrazu a respektování všech vlastních nastavení pera.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Krok 6: uložit exportovaný PDF

Volání `save` zapíše PDF soubor pojmenovaný `9LHATT-A56_generated.pdf` do vašeho adresáře `dataDir`, včetně vlastního stylu pera, který jste definovali.

```java
cadImage.save((dataDir + "9LHATT-A56_generated.pdf"), pdfOptions);
```

Spuštěním tohoto řádku získáte PDF, které zachovává vektorovou kvalitu a zároveň aplikuje vaše úpravy pera.

## Běžné případy použití

- **Technická dokumentace** – vložit přesné inženýrské výkresy do PDF manuálů pro techniky v terénu.  
- **Automatizované reportování** – generovat PDF z CAD dat za běhu ve webových službách nebo dávkových úlohách.  
- **Kontrola kvality** – použít vlastní zakončení čar k zvýraznění měřicích čar nebo tolerancí, což usnadní inspekční zprávy.

## Řešení problémů a tipy

- **Nesprávná cesta k souboru** – ujistěte se, že `dataDir` končí oddělovačem souborů (`/` nebo `\\`).  
- **Chybějící licence** – bez platné licence knihovna běží v režimu hodnocení a do výstupního PDF přidává vodoznaky.  
- **Neočekávané styly čar** – zkontrolujte, že `PenOptions` jsou nastaveny **před** voláním `save`; jinak se použije výchozí konfigurace pera.

## Často kladené otázky

### Q1: Mohu přizpůsobit možnosti pera pro formáty jiné než PDF?

A1: Ano, přizpůsobení pera ukázané v tomto tutoriálu je použitelné pro různé formáty obrázků, včetně PDF, PNG, BMP, GIF, JPEG2000, JPEG, PSD, TIFF a WMF.

### Q2: Jak mohu nastavit různé počáteční a koncové zakončení pro pera?

A2: Využijte třídu `PenOptions` k nastavení požadovaných počátečních a koncových zakončení, což poskytuje flexibilitu při definování vzhledu čar.

### Q3: Co se stane, pokud nevyjádřím možnosti pera?

A3: Pokud nejsou možnosti pera explicitně nastaveny, systém použije výchozí pera, která se mohou lišit v různých kontextech.

### Q4: Existují specifické úvahy ohledně možností rasterizace?

A4: Úpravou šířky a výšky stránky v možnostech rasterizace můžete řídit rozměry exportovaného obrazu.

### Q5: Kde mohu najít další podporu nebo diskuse komunity?

A5: Navštivte fórum komunity Aspose.CAD na [Aspose.CAD community forum](https://forum.aspose.com/c/cad/19) pro podporu a diskuse.

---

**Poslední aktualizace:** 2026-08-29  
**Testováno s:** Aspose.CAD 24.11 for Java  
**Autor:** Aspose

## Související tutoriály

- [Export DWG do PDF v Javě – nastavit velikost stránky PDF pomocí Aspose.CAD](/cad/java/cad-export-options/export-to-pdf/)
- [Vytvořit PDF z DXF pomocí Aspose.CAD pro Java](/cad/java/additional-features/render-dxf-as-pdf/)
- [Export CAD do PDF: Exportovat rozvržení CAD do PDF s Aspose.CAD pro Java](/cad/java/cad-export-options/export-cad-layouts-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}