---
title: Nastavte velikost a režim plátna
linktitle: Nastavte velikost a režim plátna
second_title: Aspose.CAD Java API
description: Prozkoumejte sílu Aspose.CAD pro Java pomocí našeho podrobného průvodce nastavením velikosti a režimu plátna. Bez námahy převádějte soubory CAD do formátů PDF a TIFF.
weight: 16
url: /cs/java/advanced-cad-features/set-canvas-size-and-mode/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Nastavte velikost a režim plátna

## Úvod

Chcete využít sílu Aspose.CAD pro Java k vylepšení vašeho procesu konverze CAD? Tento komplexní průvodce vás provede kroky nastavení velikosti plátna a režimu pomocí Aspose.CAD pro Java. Ať už jste zkušený vývojář nebo teprve začínáte, tento tutoriál vám poskytne potřebné informace.

## Předpoklady

Než se pustíte do výukového programu, ujistěte se, že máte splněny následující předpoklady:

-  Aspose.CAD for Java: Ujistěte se, že máte ve svém prostředí Java nainstalovanou knihovnu Aspose.CAD. Můžete si jej stáhnout[tady](https://releases.aspose.com/cad/java/).

- Adresář dokumentů: Nastavte adresář dokumentů pro ukládání souborů CAD. Na tento adresář bude odkazováno v krocích výukového programu.

Nyní začneme s průvodcem krok za krokem.

## Importovat jmenné prostory

tomto kroku naimportujeme potřebné jmenné prostory pro nastartování vašeho projektu Aspose.CAD.
```java
import java.awt.Image;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## Krok 1: Import tříd Aspose.CAD

```java
// Cesta k adresáři prostředků.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
com.aspose.cad.Image objImage = com.aspose.cad.Image.load(srcFile);
```

 V tomto úryvku nastavíme cestu k adresáři prostředků a načteme soubor DXF pomocí Aspose.CAD's`Image` třída.

## Krok 2: Nastavte vlastnosti CadRasterizationOptions

```java
// Vytvořte instanci CadRasterizationOptions a nastavte její různé vlastnosti
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

 Zde vytvoříme instanci`CadRasterizationOptions` a konfigurovat vlastnosti, jako je šířka stránky, výška stránky a možnosti změny velikosti.

## Krok 3: Vytvořte PdfOptions a nastavte VectorRasterizationOptions

```java
// Vytvořte instanci PdfOptions
PdfOptions pdfOptions = new PdfOptions();

// Nastavte vlastnost VectorRasterizationOptions
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

 Nyní vytvoříme a`PdfOptions` instance a nastavte ji`VectorRasterizationOptions` vlastnost na dříve nakonfigurovanou`CadRasterizationOptions`.

## Krok 4: Export do PDF

```java
// Export CAD do PDF
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

Nakonec uložíme CAD obrázek do souboru PDF pomocí zadaných možností.

## Krok 5: Vytvořte TiffOptions a nastavte VectorRasterizationOptions

```java
// Vytvořte instanci TiffOptions
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);

// Nastavte vlastnost VectorRasterizationOptions
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
```

 tomto kroku nastavíme a`TiffOptions` instance a nakonfigurujte ji`VectorRasterizationOptions` vlastnictví.

## Krok 6: Export do TIFF

```java
// Export CAD do TIFF
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

Nakonec uložíme obrázek CAD do souboru TIFF pomocí zadaných možností.

## Závěr

 Gratulujeme! Úspěšně jste nastavili velikost a režim plátna pomocí Aspose.CAD for Java. Tento tutoriál poskytuje pevný základ pro vaše projekty konverze CAD. Prozkoumejte další funkce a možnosti v[Dokumentace Aspose.CAD](https://reference.aspose.com/cad/java/).

## FAQ

### Q1: Mohu použít Aspose.CAD pro Java s jinými frameworky Java?

Odpověď 1: Ano, Aspose.CAD je navržen tak, aby se hladce integroval s různými frameworky Java.

### Q2: Je k dispozici dočasná licence pro Aspose.CAD?

 A2: Ano, můžete získat dočasnou licenci[tady](https://purchase.aspose.com/temporary-license/).

### Q3: Kde mohu získat podporu komunity pro Aspose.CAD?

 A3: Navštivte[Fórum Aspose.CAD](https://forum.aspose.com/c/cad/19) za podporu komunity a diskuze.

### Q4: Mohu vyzkoušet Aspose.CAD zdarma?

 A4: Rozhodně! Získejte bezplatnou zkušební verzi[tady](https://releases.aspose.com/).

### Q5: Jak koupím Aspose.CAD pro Java?

 A5: Kupte si produkt[tady](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
