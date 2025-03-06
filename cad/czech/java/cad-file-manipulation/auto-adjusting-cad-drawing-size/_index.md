---
title: Automatické nastavení velikosti výkresu CAD pomocí Aspose.CAD pro Java
linktitle: Automatické nastavení velikosti výkresu CAD
second_title: Aspose.CAD Java API
description: Prozkoumejte bezproblémový proces automatického přizpůsobení velikostí výkresů CAD v Javě pomocí Aspose.CAD. Postupujte podle našeho podrobného průvodce pro efektivní manipulaci se soubory CAD.
weight: 13
url: /cs/java/cad-file-manipulation/auto-adjusting-cad-drawing-size/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Automatické nastavení velikosti výkresu CAD pomocí Aspose.CAD pro Java

## Úvod

Ve světě CAD (Computer-Aided Design) je úprava velikostí výkresů běžným požadavkem a s Aspose.CAD pro Javu se to stává bezproblémovým procesem. Tato výkonná knihovna poskytuje komplexní nástroje pro práci se soubory CAD v aplikacích Java. V tomto tutoriálu prozkoumáme krok za krokem proces automatického přizpůsobení velikostí výkresů CAD pomocí Aspose.CAD.

## Předpoklady

Než se pustíte do výukového programu, ujistěte se, že máte splněny následující předpoklady:

1.  Vývojové prostředí Java: Ujistěte se, že máte na svém počítači nainstalovanou Javu. Můžete si jej stáhnout[tady](https://www.java.com/en/download/).

2.  Knihovna Aspose.CAD: Stáhněte a nainstalujte knihovnu Aspose.CAD pro Javu z[tady](https://releases.aspose.com/cad/java/).

3. Ukázkový soubor CAD: V adresáři dokumentů mějte k dispozici vzorový soubor CAD (např. sample.dwg).

## Importovat jmenné prostory

Do své Java aplikace zahrňte potřebné jmenné prostory, abyste mohli využívat funkce Aspose.CAD. Zde je příklad:

```java

import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Nyní si rozdělme proces automatického přizpůsobení velikostí výkresů CAD do zvládnutelných kroků.

## Krok 1: Načtěte výkres CAD

```java
String dataDir = "Your Document Directory" + "CADConversion/";
String sourceFilePath = dataDir + "sample.dwg";
Image objImage = Image.load(sourceFilePath);
```

Tento krok zahrnuje načtení výkresu CAD ze zadané cesty k souboru.

## Krok 2: Vytvořte BmpOptions

```java
BmpOptions bmpOptions = new BmpOptions();
```

 Vytvořte instanci`BmpOptions` třídy, která bude sloužit k nastavení různých možností pro formát BMP.

## Krok 3: Vytvořte CadRasterizationOptions

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(cadRasterizationOptions);
```

 Vytvořte instanci`CadRasterizationOptions` pro přizpůsobení nastavení rasterizace pro soubor CAD.

## Krok 4: Nastavte vlastnost rozvržení

```java
cadRasterizationOptions.setLayouts(new String[]{"Model"});
```

Určete rozvržení, která chcete zahrnout do výstupu. V tomto případě použijeme rozložení "Model".

## Krok 5: Export do formátu BMP

```java
String outPath = sourceFilePath + ".bmp";
objImage.save(outPath, bmpOptions);
```

Nakonec uložte upravený CAD výkres ve formátu BMP do zadané výstupní cesty.

Opakujte tyto kroky ve své aplikaci Java a pomocí Aspose.CAD for Java úspěšně automaticky upravíte velikost výkresu CAD.

## Závěr

tomto tutoriálu jsme prošli procesem automatického přizpůsobení velikostí výkresů CAD pomocí Aspose.CAD pro Java. Tato knihovna zjednodušuje manipulaci se soubory CAD a poskytuje vývojářům robustní řešení.

## FAQ

### Q1: Je Aspose.CAD kompatibilní s různými formáty souborů CAD?

Odpověď 1: Ano, Aspose.CAD podporuje různé formáty CAD, včetně DWG, DXF, DGN a dalších.

### Q2: Mohu použít Aspose.CAD pro komerční projekty?

 A2: Rozhodně! Návštěva[tady](https://purchase.aspose.com/buy) prozkoumat možnosti licencování.

### Q3: Jak mohu získat dočasné licence pro testovací účely?

 A3: Získejte dočasnou licenci[tady](https://purchase.aspose.com/temporary-license/) pro testování a hodnocení.

### Q4: Kde najdu podporu pro Aspose.CAD?

 A4: Připojte se ke komunitě Aspose.CAD[Fórum](https://forum.aspose.com/c/cad/19) za pomoc a diskuze.

### Q5: Je k dispozici bezplatná zkušební verze pro Aspose.CAD pro Javu?

 A5: Ano, máte přístup k bezplatné zkušební verzi[tady](https://releases.aspose.com/) prozkoumat možnosti knihovny.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
