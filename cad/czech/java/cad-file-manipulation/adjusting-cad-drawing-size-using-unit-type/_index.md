---
title: Úprava velikosti výkresu CAD pomocí typu jednotky s Aspose.CAD for Java
linktitle: Úprava velikosti výkresu CAD pomocí typu jednotky
second_title: Aspose.CAD Java API
description: Prozkoumejte sílu Aspose.CAD pro Java při úpravě velikosti výkresů CAD bez námahy. Postupujte podle našeho podrobného průvodce pro přesnost a přizpůsobivost.
weight: 14
url: /cs/java/cad-file-manipulation/adjusting-cad-drawing-size-using-unit-type/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Úprava velikosti výkresu CAD pomocí typu jednotky s Aspose.CAD for Java

## Úvod

neustále se vyvíjející oblasti počítačově podporovaného navrhování (CAD) je přesnost a přizpůsobivost prvořadá. Jedním z běžných požadavků je úprava velikosti výkresů CAD na základě konkrétních typů jednotek. Aspose.CAD for Java se ukazuje jako mocný spojenec, který poskytuje bezproblémové možnosti pro programovou manipulaci se soubory CAD.

## Předpoklady

Než se pustíte do výukového programu, ujistěte se, že máte splněny následující předpoklady:

- Vývojové prostředí Java: Ujistěte se, že máte na svém počítači nastavené funkční vývojové prostředí Java.

-  Knihovna Aspose.CAD for Java: Stáhněte si a integrujte knihovnu Aspose.CAD do svého projektu Java. Můžete získat knihovnu[tady](https://releases.aspose.com/cad/java/).

## Importovat jmenné prostory

Do kódu Java zahrňte potřebné jmenné prostory pro přístup k funkcím Aspose.CAD. Přidejte následující importy:

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Nyní si rozeberme proces úpravy velikosti výkresu CAD pomocí typu jednotky do zvládnutelných kroků:

## Krok 1: Definujte datový adresář

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

Nastavte cestu k adresáři, kde jsou umístěny vaše CAD soubory.

## Krok 2: Načtěte výkres CAD

```java
String sourceFilePath = dataDir + "sample.dwg";
Image image = Image.load(sourceFilePath);
```

 Načtěte výkres CAD pomocí Aspose.CAD's`Image` třída.

## Krok 3: Vytvořte možnosti BMP

```java
BmpOptions bmpOptions = new BmpOptions();
```

 Vytvořte instanci`BmpOptions` třídy pro export rozvržení CAD do formátu BMP.

## Krok 4: Nakonfigurujte možnosti rastrování

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(cadRasterizationOptions);
```

 Vytvořte instanci`CadRasterizationOptions` a spojte jej s`BmpOptions` pro vektorové rastrování.

## Krok 5: Nastavte typ jednotky

```java
cadRasterizationOptions.setUnitType(UnitType.Centimeter);
```

Zadejte požadovaný typ jednotky pro výkres CAD. V tomto příkladu jsme jej nastavili na Centimetr.

## Krok 6: Nastavte rozvržení

```java
cadRasterizationOptions.setLayouts(new String[] { "Model" });
```

Definujte rozvržení, která mají být zohledněna při exportu. V tomto případě jsme vybrali rozložení "Model".

## Krok 7: Export do BMP

```java
String outPath = sourceFilePath + ".bmp";
image.save(outPath, bmpOptions);
```

Nakonec uložte upravený CAD výkres ve formátu BMP.

## Závěr

S Aspose.CAD for Java se úprava velikostí výkresů CAD stává hračkou. Tento tutoriál vás provede celým procesem a zdůrazní význam každého kroku pro dosažení přesných výsledků.

## FAQ

### Q1: Mohu používat Aspose.CAD for Java s jinými programovacími jazyky?

A1: Aspose.CAD primárně podporuje Javu, ale jsou dostupné verze pro jiné jazyky, jako je .NET.

### Q2: Existují nějaké možnosti licencování pro Aspose.CAD?

 Odpověď 2: Ano, můžete prozkoumat možnosti licencování a zakoupit Aspose.CAD[tady](https://purchase.aspose.com/buy).

### Q3: Je k dispozici bezplatná zkušební verze pro Aspose.CAD?

 A3: Jistě, máte přístup k bezplatné zkušební verzi[tady](https://releases.aspose.com/).

### Q4: Jak mohu získat podporu pro Aspose.CAD pro Java?

 A4: Navštivte fórum Aspose.CAD[tady](https://forum.aspose.com/c/cad/19) za komplexní podporu.

### Q5: Mohu získat dočasnou licenci pro Aspose.CAD?

 A5: Ano, můžete získat dočasnou licenci[tady](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
