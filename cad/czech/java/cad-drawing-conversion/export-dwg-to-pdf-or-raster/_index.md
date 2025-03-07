---
title: Export DWG do PDF nebo rastru pomocí Aspose.CAD for Java
linktitle: Export DWG do PDF nebo rastru
second_title: Aspose.CAD Java API
description: Prozkoumejte bezproblémový proces exportu souborů DWG do PDF nebo rastrových obrázků v Javě pomocí Aspose.CAD. Tento průvodce krok za krokem zajišťuje přesnost a efektivitu.
weight: 13
url: /cs/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export DWG do PDF nebo rastru pomocí Aspose.CAD for Java

## Úvod

dynamickém světě počítačově podporovaného navrhování (CAD) je efektivní zpracování výkresů zásadní. Aspose.CAD for Java poskytuje výkonné řešení pro export souborů DWG do PDF nebo rastrových obrázků. Tento tutoriál vás provede celým procesem a zajistí, že využijete plný potenciál Aspose.CAD pro Javu.

## Předpoklady

Než se pustíte do výukového programu, ujistěte se, že máte následující:

- Základní znalost programování v Javě.
-  Nainstalovaná knihovna Aspose.CAD for Java. Pokud ne, stáhněte si ji[tady](https://releases.aspose.com/cad/java/).
- Soubor DWG pro testovací účely. Můžete použít poskytnutý soubor "Bottom_plate.dwg".

## Importovat jmenné prostory

Ve svém projektu Java naimportujte potřebné jmenné prostory, abyste proces nastartovali:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.UnitType;
```

## Krok 1: Načtěte soubor DWG

 Začněte načtením souboru DWG pomocí Aspose.CAD's`Image` třída:

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Bottom_plate.dwg";
Image objImage = Image.load(srcFile);
```

## Krok 2: Určete typ jednotky

Dále zkontrolujte typ jednotky načteného souboru DWG:

```java
Boolean currentUnitIsMetric = IsMetric(objImage.getUnitType());
int currentUnitCoefficient = objImage.getUnitType();
```

## Krok 3: Nastavte možnosti rastrování

Na základě typu jednotky nakonfigurujte možnosti rastrování:

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();

if (currentUnitIsMetric) {
    // Metrické jednotky
    double metersCoeff = 1 / 1000.0;
    double scaleFactor = metersCoeff / currentUnitCoefficient;
    rasterizationOptions.setPageWidth((float)(210 * scaleFactor));
    rasterizationOptions.setPageHeight((float)(297 * scaleFactor));
    rasterizationOptions.setUnitType(UnitType.Millimeter);
} else {
    // Imperiální jednotky
    rasterizationOptions.setPageWidth((float)(8.27f / currentUnitCoefficient));
    rasterizationOptions.setPageHeight((float)(11.69f / currentUnitCoefficient));
    rasterizationOptions.setUnitType(UnitType.Inch);
}
```

## Krok 4: Nakonfigurujte možnosti PDF

Nastavení možností exportu PDF:

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());
```

## Krok 5: Uložit jako PDF

Nakonec uložte soubor DWG jako PDF:

```java
objImage.save(dataDir + "Saved.pdf", pdfOptions);
```

A tady to máte! Úspěšně jste exportovali soubor DWG do PDF pomocí Aspose.CAD for Java.

## Závěr

Tento výukový program poskytuje podrobného průvodce využitím Aspose.CAD for Java k exportu souborů DWG do PDF nebo rastrových obrázků. Tato knihovna zjednodušuje proces a umožňuje vám efektivně pracovat s výkresy CAD ve vašich aplikacích Java.

## FAQ

### Q1: Mohu použít Aspose.CAD pro Java s jinými frameworky Java?

Odpověď 1: Ano, Aspose.CAD for Java se hladce integruje s populárními frameworky Java.

### Q2: Je k dispozici dočasná licence pro Aspose.CAD pro Java?

 A2: Ano, můžete získat dočasnou licenci[tady](https://purchase.aspose.com/temporary-license/).

### Q3: Kde najdu podporu pro Aspose.CAD pro Java?

 A3: Navštivte[Fórum Aspose.CAD](https://forum.aspose.com/c/cad/19) za pomoc od komunity.

### Q4: Jak si mohu zakoupit licenci pro Aspose.CAD for Java?

 A4: Můžete si zakoupit licenci[tady](https://purchase.aspose.com/buy).

### Q5: Jaké jednotky Aspose.CAD pro Java podporuje?

A5: Aspose.CAD for Java podporuje metrické i imperiální jednotky.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
