---
date: 2025-12-25
description: Naučte se, jak exportovat DWG do BMP pomocí Aspose.CAD pro Javu. Tento
  krok‑za‑krokem průvodce ukazuje, jak upravit velikost CAD výkresu a efektivně převést
  CAD do BMP.
linktitle: Adjusting CAD Drawing Size Using Unit Type
second_title: Aspose.CAD Java API
title: Export DWG do BMP – úprava velikosti CAD pomocí typu jednotky (Java)
url: /cs/java/cad-file-manipulation/adjusting-cad-drawing-size-using-unit-type/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export DWG do BMP – Úprava velikosti CAD výkresu pomocí jednotky (Unit Type) s Aspose.CAD pro Java

## Introduction

Když potřebujete **export DWG do BMP**, je nezbytné řídit velikost výstupu a jednotku měření pro následné zpracování nebo tisk. V tomto tutoriálu se naučíte, jak upravit velikost CAD výkresu a převést CAD do BMP pomocí Aspose.CAD pro Java, přičemž použijete vlastnost `UnitType` k definování jednotky měření. Kroky jsou vysvětleny srozumitelně, takže je můžete sledovat i pokud jste s knihovnou noví.

## Quick Answers
- **Co znamená „export DWG do BMP“?** Převod DWG výkresu na rastrový obrázek BMP.  
- **Která vlastnost řídí velikost výstupu?** `CadRasterizationOptions.setUnitType()` nastavuje jednotku (např. centimetr).  
- **Potřebuji licenci pro spuštění kódu?** Bezplatná zkušební verze funguje pro hodnocení; licence je vyžadována pro produkční nasazení.  
- **Mohu zvolit jiné rozvržení?** Ano, použijte `setLayouts()` k určení modelových nebo papírových rozvržení.  
- **Jaké výstupní formáty jsou podporovány?** Kromě BMP můžete exportovat do PNG, JPEG, TIFF atd. změnou třídy možností.

## What is **export DWG to BMP**?

Export DWG do BMP znamená rasterizaci vektorového souboru DWG do bitmapového obrázku (BMP). To je užitečné, když potřebujete pixelově přesnou reprezentaci pro starší systémy, zpracování obrazu nebo jednoduché zobrazovací scénáře.

## Why adjust CAD drawing size with **Unit Type**?

Nastavení typu jednotky vám umožňuje řídit fyzické rozměry exportovaného obrázku bez nutnosti ručně počítat škálovací faktory. To zajišťuje, že bitmapa odpovídá reálným rozměrům (např. centimetry), což je klíčové pro inženýrské výkresy a tištěnou dokumentaci.

## Prerequisites

Before diving into the tutorial, make sure you have the following prerequisites in place:

- **Java vývojové prostředí** – Funkční JDK (8 nebo novější) a IDE nebo nástroj pro sestavení (Maven/Gradle).  
- **Aspose.CAD pro Java knihovna** – Stáhněte a integrujte knihovnu Aspose.CAD do svého Java projektu. Knihovnu můžete získat [zde](https://releases.aspose.com/cad/java/).

## Import Namespaces

Ve vašem Java kódu zahrňte potřebné jmenné prostory pro přístup k funkcím Aspose.CAD. Přidejte následující importy:

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Nyní rozdělíme proces úpravy velikosti CAD výkresu pomocí typu jednotky na zvládnutelné kroky:

## Step 1: Define Data Directory

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

Nastavte cestu ke složce, kde jsou umístěny vaše CAD soubory.

## Step 2: Load CAD Drawing

```java
String sourceFilePath = dataDir + "sample.dwg";
Image image = Image.load(sourceFilePath);
```

Načtěte CAD výkres pomocí třídy `Image` z Aspose.CAD.

## Step 3: Create BMP Options

```java
BmpOptions bmpOptions = new BmpOptions();
```

Vytvořte instanci třídy `BmpOptions` pro export rozvržení CAD do formátu BMP.

## Step 4: Configure Rasterization Options

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(cadRasterizationOptions);
```

Vytvořte instanci `CadRasterizationOptions` a přiřaďte ji k `BmpOptions` pro vektorovou rasterizaci.

## Step 5: Set Unit Type

```java
cadRasterizationOptions.setUnitType(UnitType.Centimeter);
```

Určete požadovaný typ jednotky pro CAD výkres. V tomto příkladu jsme nastavili **Centimeter**, což přímo ovlivňuje velikost exportovaného obrázku při **úpravě velikosti CAD výkresu**.

## Step 6: Set Layouts

```java
cadRasterizationOptions.setLayouts(new String[] { "Model" });
```

Definujte rozvržení, která mají být při exportu zohledněna. V tomto případě jsme vybrali rozvržení **"Model"**, ale můžete přepnout na papírová rozvržení, pokud je to potřeba.

## Step 7: Export to BMP

```java
String outPath = sourceFilePath + ".bmp";
image.save(outPath, bmpOptions);
```

Nakonec uložte upravený CAD výkres ve formátu BMP. Tento krok dokončuje workflow **export DWG do BMP** při zachování provedených úprav velikosti.

## Common Issues and Solutions

| Problém | Důvod | Řešení |
|-------|--------|-----|
| **Obrázek je příliš malý** | Jednotka není nastavena nebo je použita výchozí (pixel) | Zavolejte `setUnitType()` s požadovaným měřením (např. `UnitType.Centimeter`). |
| **Exportováno špatné rozvržení** | Chybný název rozvržení | Ověřte názvy rozvržení v CAD prohlížeči; použijte přesný řetězec v `setLayouts()`. |
| **Výjimka licence** | Spuštění bez platné licence v produkci | Použijte dočasnou nebo trvalou licenci, jak je popsáno v FAQ. |

## Frequently Asked Questions (Extended)

**Q: Mohu používat Aspose.CAD pro Java s jinými programovacími jazyky?**  
A: Aspose.CAD primárně podporuje Java, ale jsou k dispozici verze pro jiné jazyky, jako je .NET.

**Q: Existují licenční možnosti pro Aspose.CAD?**  
A: Ano, můžete prozkoumat licenční možnosti a zakoupit Aspose.CAD [zde](https://purchase.aspose.com/buy).

**Q: Je k dispozici bezplatná zkušební verze pro Aspose.CAD?**  
A: Samozřejmě, můžete získat bezplatnou zkušební verzi [zde](https://releases.aspose.com/).

**Q: Jak mohu získat podporu pro Aspose.CAD pro Java?**  
A: Navštivte fórum Aspose.CAD [zde](https://forum.aspose.com/c/cad/19) pro komplexní podporu.

**Q: Mohu získat dočasnou licenci pro Aspose.CAD?**  
A: Ano, můžete získat dočasnou licenci [zde](https://purchase.aspose.com/temporary-license/).

---

**Poslední aktualizace:** 2025-12-25  
**Testováno s:** Aspose.CAD for Java 24.10  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}