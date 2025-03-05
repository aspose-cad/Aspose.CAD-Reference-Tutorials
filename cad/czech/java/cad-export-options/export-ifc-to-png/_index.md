---
title: Exportujte IFC do PNG pomocí Aspose.CAD pro Javu
linktitle: Export IFC do PNG
second_title: Aspose.CAD Java API
description: Převeďte IFC na PNG bez námahy pomocí Aspose.CAD pro Java. Postupujte podle našeho podrobného návodu.
type: docs
weight: 18
url: /cs/java/cad-export-options/export-ifc-to-png/
---
## Úvod

Vítejte v tomto podrobném návodu k exportu IFC (Industry Foundation Classes) do PNG pomocí Aspose.CAD for Java. Aspose.CAD je výkonná Java knihovna, která poskytuje rozsáhlé možnosti pro práci se soubory CAD, včetně formátu IFC. V tomto tutoriálu vás provedeme procesem převodu souboru IFC na obrázek PNG s podrobným vysvětlením v každém kroku.

## Předpoklady

Než začneme, ujistěte se, že máte splněny následující předpoklady:

-  Knihovna Aspose.CAD: Stáhněte a nainstalujte knihovnu Aspose.CAD pro Javu z[odkaz ke stažení](https://releases.aspose.com/cad/java/).

- Adresář dokumentů: Připravte si v systému adresář, kde je umístěn váš soubor IFC.

## Importovat jmenné prostory

Do svého projektu Java importujte potřebné jmenné prostory, jak je uvedeno níže:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

## Krok 1: Načtěte soubor IFC

```java
String dataDir = "Your Document Directory" + "ExportingIFC/";
String fileName = dataDir + "example.ifc";
IfcImage cadImage = (IfcImage)Image.load(fileName);
```

Tento krok zahrnuje načtení souboru IFC pomocí Aspose.CAD.

## Krok 2: Nastavte možnosti vektoru

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
```

Nakonfigurujte možnosti vektoru pro rastrování, určete šířku a výšku stránky.

## Krok 3: Nastavte možnosti PNG

```java
PngOptions pngOptions = new PngOptions();
pngOptions.setVectorRasterizationOptions(vectorOptions);
```

Nastavte možnosti PNG, včetně možností vektorového rastrování.

## Krok 4: Uložte jako PNG

```java
String outPath = dataDir + "example.png";
cadImage.save(outPath, pngOptions);
```

Uložte zpracovaný obrázek ve formátu PNG.

## Závěr

Gratulujeme! Úspěšně jste převedli soubor IFC na PNG pomocí Aspose.CAD for Java. Tento výukový program poskytuje komplexního průvodce, který zajišťuje, že můžete tuto funkci bez problémů integrovat do svých projektů.

## FAQ

### Q1: Je Aspose.CAD kompatibilní se všemi verzemi souborů IFC?

 A1: Aspose.CAD podporuje různé verze souborů IFC. Odkazovat na[dokumentace](https://reference.aspose.com/cad/java/) pro podrobnosti o kompatibilitě.

### Q2: Mohu dále přizpůsobit možnosti rasterizace?

 A2: Rozhodně! Prozkoumat[dokumentace](https://reference.aspose.com/cad/java/) pro pokročilé možnosti přizpůsobení.

### Q3: Je k dispozici zkušební verze?

A3: Ano, máte přístup k bezplatné zkušební verzi[tady](https://releases.aspose.com/).

### Q4: Jak mohu získat dočasné licencování pro Aspose.CAD?

 A4: Získejte dočasnou licenci od[tento odkaz](https://purchase.aspose.com/temporary-license/).

### Q5: Kde mohu hledat pomoc nebo diskutovat o problémech?

A5: Navštivte[Fórum Aspose.CAD](https://forum.aspose.com/c/cad/19) za podporu komunity.
