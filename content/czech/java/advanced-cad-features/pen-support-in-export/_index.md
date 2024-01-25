---
title: Podpora pera v exportu
linktitle: Podpora pera v exportu
second_title: Aspose.CAD Java API
description: Ovládněte přizpůsobení pera v exportu CAD pomocí Aspose.CAD pro Java. Postupujte podle našeho podrobného průvodce pro bezproblémovou integraci.
type: docs
weight: 13
url: /cs/java/advanced-cad-features/pen-support-in-export/
---
## Úvod

neustále se vyvíjejícím prostředí převodů CAD (Computer-Aided Design) se Aspose.CAD for Java ukazuje jako výkonný nástroj, který nabízí rozsáhlé možnosti pro manipulaci se soubory CAD. Mezi jeho všestrannými funkcemi vyniká podpora přizpůsobení pera během exportu, která uživatelům umožňuje přizpůsobit vzhled exportovaných obrázků. Tento tutoriál vás provede procesem využití podpory pera ve funkci exportu se zaměřením na praktickou implementaci pomocí Javy.

## Předpoklady

Než se pustíte do výukového programu, ujistěte se, že máte splněny následující předpoklady:

- Vývojové prostředí Java: Ujistěte se, že máte na svém počítači nastavené funkční vývojové prostředí Java.

-  Knihovna Aspose.CAD: Stáhněte si a integrujte knihovnu Aspose.CAD do svého projektu Java. Knihovnu najdete[tady](https://releases.aspose.com/cad/java/).

Nyní se vrhněme na tutoriál a prozkoumáme kroky pro využití podpory pera během exportu CAD.

## Importovat jmenné prostory

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.PenOptions;
import com.aspose.cad.internal.imaging.LineCap;
```

## Krok 1: Definujte svůj adresář dokumentů

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

Ujistěte se, že jste nahradili "Your Document Directory" skutečnou cestou k vašim CAD dokumentům.

## Krok 2: Načtěte soubor CAD

```java
String srcFile = dataDir + "conic_pyramid.dxf";
CadImage cadImage = (CadImage) Image.load(srcFile);
```

Tento krok zahrnuje načtení souboru CAD, v tomto případě „conic_pyramid.dxf“, pomocí knihovny Aspose.CAD.

## Krok 3: Nakonfigurujte možnosti rastrování

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(cadImage.getWidth() * 100);
rasterizationOptions.setPageHeight(cadImage.getHeight() * 100);
```

Upravte šířku a výšku stránky podle svých konkrétních požadavků. Tyto hodnoty určují rozměry exportovaného obrázku.

## Krok 4: Přizpůsobte možnosti pera

```java
PenOptions penOts = new PenOptions();
penOts.setStartCap(LineCap.Flat);
penOts.setEndCap(LineCap.Flat);
```

Přizpůsobte si začátek a konec pera podle potřeby. Toto přizpůsobení platí při exportu objektu CadImage do různých obrazových formátů.

## Krok 5: Nakonfigurujte možnosti exportu PDF

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Zadejte možnosti vektorové rastrování, včetně dříve nakonfigurovaných možností rastrování.

## Krok 6: Uložte exportovaný soubor PDF

```java
cadImage.save((dataDir + "9LHATT-A56_generated.pdf"), pdfOptions);
```

Uložte exportovaný soubor PDF se zadaným názvem souboru (v tomto příkladu "9LHATT-A56_generated.pdf") a nakonfigurovanými možnostmi.

## Závěr

Na závěr, využití podpory pera během exportu CAD pomocí Aspose.CAD for Java umožňuje uživatelům přizpůsobit vzhled exportovaných obrázků. Podle tohoto podrobného průvodce jste se naučili, jak hladce integrovat přizpůsobení pera do vašeho pracovního postupu konverze CAD.

## FAQ

### Q1: Mohu přizpůsobit možnosti pera pro jiné formáty než PDF?

Odpověď 1: Ano, přizpůsobení pera uvedené v tomto kurzu lze použít pro různé formáty obrázků, včetně PDF, PNG, BMP, GIF, JPEG2000, JPEG, PSD, TIFF a WMF.

### Q2: Jak mohu zacházet s různými počátečními a koncovými uzávěry pro pera?

 A2: Využijte`PenOptions` třídy pro nastavení požadovaného začátku a konce, což nabízí flexibilitu při definování vzhledu čar.

### Q3: Co když neurčím možnosti pera?

Odpověď 3: Pokud možnosti pera nejsou explicitně nastaveny, systém použije svá výchozí pera, která se mohou v různých kontextech lišit.

### Q4: Existují konkrétní úvahy pro možnosti rasterizace?

A4: Upravte šířku a výšku stránky v možnostech rastrování, abyste řídili rozměry exportovaného obrázku.

### Q5: Kde najdu další podporu nebo komunitní diskuse?

 A5: Prozkoumejte fórum komunity Aspose.CAD na adrese[tady](https://forum.aspose.com/c/cad/19) za podporu a diskuze.