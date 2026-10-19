---
date: 2026-10-19
description: Naučte se, jak vytvořit PNG miniatury souborů IFC pomocí Aspose.CAD for
  Java během několika řádků kódu.
keywords:
- create png thumbnail ifc
- ifc to png conversion
- aspose cad java
- java image processing
- bIM visualization
lastmod: 2026-10-19
linktitle: Exportovat IFC do PNG
og_description: Vytvořte PNG miniatury souborů IFC snadno s Aspose.CAD for Java. Tento
  průvodce krok za krokem ukazuje, jak načíst, rasterizovat a uložit modely IFC jako
  vysoce kvalitní PNG obrázky.
og_image_alt: Developer guide showing Java code that converts IFC files to PNG thumbnails
  using Aspose.CAD
og_title: Vytvořit PNG miniaturu IFC pomocí Aspose.CAD for Java
schemas:
- author: Aspose
  dateModified: '2026-10-19'
  description: Learn how to create PNG thumbnail IFC files with Aspose.CAD for Java
    in just a few lines of code.
  headline: How to create PNG thumbnail IFC with Aspose.CAD for Java
  type: TechArticle
- description: Learn how to create PNG thumbnail IFC files with Aspose.CAD for Java
    in just a few lines of code.
  name: How to create PNG thumbnail IFC with Aspose.CAD for Java
  steps:
  - name: load the IFC file
    text: First, point to the folder where your IFC file lives and load it with `CadImage.load`.
      `CadImage.load` reads a CAD file and returns an image object that can be rasterized.
      > **Why this matters:** Loading the file as a `CadImage` gives you access to
      vector‑raster conversion options that control resol
  - name: set rasterization options
    text: Define the output dimensions and any other vector‑related settings through
      `VectorRasterizationOptions`. `VectorRasterizationOptions` lets you specify
      output size, background color, and other rasterization parameters. > Adjust
      `PageWidth` and `PageHeight` to control the final PNG resolution, which i
  - name: configure PNG options
    text: Link the rasterization options to the PNG exporter by creating a `PngOptions`
      instance.
  - name: save the image as PNG
    text: Finally, write the rasterized image to disk using the `save` method. `save`
      writes the rasterized image to the specified file path in the chosen format.
      > After this step you have successfully **created a PNG thumbnail IFC** and
      can use the resulting `example.png` anywhere you need a raster image.
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD supports many formats (DWG, DXF, DGN, etc.). Simply change
      the file extension and load the appropriate image class.
    question: Can I use this approach to convert other CAD formats to PNG?
  - answer: DPI is controlled indirectly via `PageWidth`/`PageHeight`. Adjust these
      values relative to the desired physical size to achieve the required DPI.
    question: Does the library let me set a custom DPI?
  - answer: PNG is a lossless format, so the rasterized image retains the full visual
      fidelity of the original vector data.
    question: Is the PNG output loss‑less?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- ifc conversion
- png thumbnail
- aspose.cad
- java image processing
- bim visualization
title: Jak vytvořit PNG miniaturu IFC pomocí Aspose.CAD for Java
url: /cs/java/cad-export-options/export-ifc-to-png/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export IFC do PNG pomocí Aspose.CAD pro Java

## Úvod

V tomto tutoriálu se naučíte, jak **vytvořit PNG miniaturu IFC** souborů pomocí Aspose.CAD pro Java. Ať už potřebujete rychlé náhledy pro BIM portál, generovat miniatury pro systém správy dokumentů, nebo automatizovat hromadné konverze, níže uvedené kroky vám umožní rasterizovat 3‑D IFC model do ostrého 2‑D PNG obrázku během několika řádků Java kódu.

## Rychlé odpovědi
- **Jaká knihovna je vyžadována?** Aspose.CAD pro Java.  
- **Mohu vytvořit PNG miniaturu IFC během několika řádků kódu?** Ano – celý workflow se vejde do méně než 20 řádků.  
- **Potřebuji licenci pro produkci?** Dočasná licence stačí pro testování; plná licence je vyžadována pro komerční nasazení.  
- **Je výstup škálovatelný?** Můžete nastavit libovolné rozměry v pixelech, takže PNG se přizpůsobí jakékoli požadované velikosti.  
- **Jaká verze Javy je podporována?** Java 8 nebo vyšší.

## Co znamená „převést IFC na PNG“?
Převod IFC (Industry Foundation Classes) na PNG znamená rasterizaci 3‑D modelu budovy do 2‑D bitmapového obrázku. Tento proces vytvoří vizuální miniaturu, kterou lze zobrazit v prohlížečích, reportech nebo mobilních aplikacích bez nutnosti plnohodnotného CAD prohlížeče.

## Proč použít Aspose.CAD pro Java?
Aspose.CAD podporuje **více než 30 CAD a BIM formátů**, včetně IFC, DWG, DXF a DGN, a dokáže zpracovat soubory až do **2 GB** bez načítání celého dokumentu do paměti. Knihovna je čistě Java, má **žádné externí závislosti** a běží na Windows, Linuxu i macOS, což ji činí ideální pro server‑side generování obrázků.  
Poskytuje vysoce výkonnou rasterizaci, rozsáhlou podporu formátů a snadnou integraci do Java aplikací.

## Předpoklady

- **Aspose.CAD knihovna** – stáhněte nejnovější JAR z [download link](https://releases.aspose.com/cad/java/).  
- **Java Development Kit** – JDK 8 nebo novější nainstalovaný na vašem počítači.  
- **IFC zdrojový soubor** – umístěte soubor do složky, na kterou můžete odkazovat z kódu.

## Import namespaces

Balíček `com.aspose.cad` poskytuje všechny třídy, které potřebujete. `CadImage` je vstupní bod pro načítání CAD souborů, zatímco `PngOptions` konfiguruje nastavení rasterizace.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

## Jak vytvořit PNG miniaturu IFC v Javě?

Načtěte IFC soubor, definujte možnosti rasterizace a uložte výsledek jako PNG obrázek – to je kompletní workflow konverze. Následující sekce rozebírají každý krok, takže můžete úryvky kódu zkopírovat do svého projektu a spustit je okamžitě.

### Krok 1: načíst IFC soubor
Nejprve uveďte cestu ke složce, kde se váš IFC soubor nachází, a načtěte jej pomocí `CadImage.load`.  
`CadImage.load` načte CAD soubor a vrátí objekt obrázku, který lze rasterizovat.

```java
String dataDir = "Your Document Directory" + "ExportingIFC/";
String fileName = dataDir + "example.ifc";
IfcImage cadImage = (IfcImage)Image.load(fileName);
```

> **Proč je to důležité:** Načtení souboru jako `CadImage` vám poskytuje přístup k možnostem vektor‑raster konverze, které řídí rozlišení, barvu pozadí a tloušťku čáry.

### Krok 2: nastavit možnosti rasterizace
Definujte výstupní rozměry a další nastavení související s vektorem pomocí `VectorRasterizationOptions`.  
`VectorRasterizationOptions` vám umožňuje specifikovat velikost výstupu, barvu pozadí a další parametry rasterizace.

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
```

> Upravit `PageWidth` a `PageHeight` pro kontrolu konečného rozlišení PNG, což je nezbytné, když **save PNG java** soubory pro vysoce kvalitní tisk nebo webové miniatury.

### Krok 3: nakonfigurovat PNG možnosti
Propojte možnosti rasterizace s PNG exportérem vytvořením instance `PngOptions`.

```java
PngOptions pngOptions = new PngOptions();
pngOptions.setVectorRasterizationOptions(vectorOptions);
```

### Krok 4: uložit obrázek jako PNG
Nakonec zapište rasterizovaný obrázek na disk pomocí metody `save`.  
`save` zapíše rasterizovaný obrázek na zadanou cestu ve zvoleném formátu.

```java
String outPath = dataDir + "example.png";
cadImage.save(outPath, pngOptions);
```

> Po tomto kroku jste úspěšně **vytvořili PNG miniaturu IFC** a můžete použít výsledný `example.png` kdekoliv, kde potřebujete rastrový obrázek.

## Běžné případy použití
- **Generování miniatur** pro BIM modely ve webových portálech.  
- **Vkládání snímků půdorysů** do PDF nebo Word reportů.  
- **Automatizovaná hromadná konverze** velkých IFC knihoven pro archivaci nebo migrační projekty.

## Řešení problémů a tipy
- **Problémy s pamětí:** U velkých IFC souborů zvyšte heap JVM (`-Xmx2g` nebo vyšší).  
- **Chybějící textury:** Ujistěte se, že externí zdroje IFC souboru jsou dostupné z `dataDir`.  
- **Profesionální tip:** Použijte `vectorOptions.setBackgroundColor(Color.getWhite())`, pokud preferujete bílé pozadí místo výchozího transparentního PNG.

## Často kladené otázky

### Q1: Je Aspose.CAD kompatibilní se všemi verzemi IFC souborů?
A1: Aspose.CAD podporuje různé verze IFC. Podrobné informace o kompatibilitě najdete v [documentation](https://reference.aspose.com/cad/java/).

### Q2: Mohu dále přizpůsobit možnosti rasterizace?
A2: Rozhodně! Prozkoumejte [documentation](https://reference.aspose.com/cad/java/) pro pokročilá nastavení jako kontrola DPI, anti‑aliasing a tloušťka čáry.

### Q3: Je k dispozici zkušební verze?
A3: Ano, můžete si stáhnout bezplatnou zkušební verzi z [Aspose.CAD free trial](https://releases.aspose.com/).

### Q4: Jak získat dočasnou licenci pro testování?
A4: Získejte dočasnou licenci na stránce [Aspose.CAD temporary license page](https://purchase.aspose.com/temporary-license/).

### Q5: Kde mohu klást otázky nebo hlásit problémy?
A5: Připojte se ke komunitě na [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) a získáte podporu od inženýrů Aspose i ostatních vývojářů.

## Často kladené otázky

**Q: Mohu tímto přístupem převést i jiné CAD formáty na PNG?**  
A: Ano, Aspose.CAD podporuje mnoho formátů (DWG, DXF, DGN atd.). Stačí změnit příponu souboru a načíst odpovídající třídu obrázku.

**Q: Umožňuje knihovna nastavit vlastní DPI?**  
A: DPI je řízeno nepřímo pomocí `PageWidth`/`PageHeight`. Upravením těchto hodnot relativně k požadované fyzické velikosti dosáhnete požadovaného DPI.

**Q: Je výstup PNG bezztrátový?**  
A: PNG je bezztrátový formát, takže rasterizovaný obrázek zachovává plnou vizuální věrnost původních vektorových dat.

## Závěr

Nyní máte kompletní, připravenou metodu pro **vytvoření PNG miniatury IFC** pomocí Aspose.CAD pro Java. Integrujte tyto kroky do desktopových nástrojů, server‑side služeb nebo cloudových funkcí a automatizujte BIM vizualizační pipeline a poskytujte rychlé, vysoce kvalitní miniatury koncovým uživatelům.

---

**Poslední aktualizace:** 2026-10-19  
**Testováno s:** Aspose.CAD pro Java 24.11  
**Autor:** Aspose

## Související tutoriály

- [How to Convert STL to PNG with Aspose.CAD for Java](/cad/java/cad-export-options/export-stl-to-png/)
- [Convert DWG to PNG – Save CAD as PNG Using Aspose.CAD for Java](/cad/java/cad-drawing-conversion/convert-cad-drawing-to-raster-image/)
- [Export DWG to PDF in Java – Set PDF Page Size with Aspose.CAD](/cad/java/cad-export-options/export-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}