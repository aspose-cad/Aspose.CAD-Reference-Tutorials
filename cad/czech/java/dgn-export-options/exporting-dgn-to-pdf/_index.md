---
title: Bez námahy Export DGN do AutoCAD PDF pomocí Aspose.CAD pro Java
linktitle: Export DGN ve formátu AutoCAD do PDF
second_title: Aspose.CAD Java API
description: Prozkoumejte podrobného průvodce exportem souborů DGN do formátu AutoCAD ve formátu PDF pomocí Aspose.CAD for Java. Zvyšte bez námahy možnosti zpracování CAD vaší aplikace Java.
weight: 12
url: /cs/java/dgn-export-options/exporting-dgn-to-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Bez námahy Export DGN do AutoCAD PDF pomocí Aspose.CAD pro Java

## Úvod

Vítejte v tomto komplexním tutoriálu o použití Aspose.CAD for Java k exportu souborů DGN ve formátu AutoCAD do PDF. Pokud chcete vylepšit schopnost své aplikace Java zpracovávat soubory CAD, Aspose.CAD je vynikající volbou. V tomto tutoriálu vás krok za krokem provedeme procesem exportu souborů DGN.


## Předpoklady
Než se pustíme do výukového programu, ujistěte se, že máte následující předpoklady:
-  Knihovna Aspose.CAD: Ujistěte se, že máte nainstalovanou knihovnu Aspose.CAD pro Javu. Můžete si jej stáhnout[tady](https://releases.aspose.com/cad/java/).
- Adresář dokumentů: Nastavte adresář dokumentů, kde budou uloženy vaše vstupní a výstupní soubory.

## Importujte balíčky

Do svého projektu Java importujte potřebné balíčky pro přístup k funkcím Aspose.CAD:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

Nyní si ukázkový kód rozdělíme do několika kroků:

## Krok 1: Definujte cesty k souboru

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "Nikon_D90_Camera.dgn";
String outFile  = dataDir + "Nikon_D90_Camera.pdf";
```

Nezapomeňte nahradit „Adresář vašich dokumentů“ skutečnou cestou, kde jsou umístěny vaše soubory.

## Krok 2: Načtěte obrázek DGN

```java
DgnImage objImage = (DgnImage) Image.load(fileName);
```

Načtěte soubor DGN pomocí Aspose.CAD.

## Krok 3: Nastavte možnosti exportu PDF

```java
PdfOptions options = new PdfOptions();
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
vectorOptions.setAutomaticLayoutsScaling(true);
vectorOptions.setLayouts(new String[] { "1", "2", "3", "9" }); // Export konkrétních pohledů
options.setVectorRasterizationOptions(vectorOptions);
```

Definujte možnosti exportu PDF, včetně rozměrů stránky a předvoleb rozvržení.

## Krok 4: Uložte soubor PDF

```java
objImage.save(outFile, options);
```

Uložte exportovaný soubor PDF.

Opakujte tyto kroky pro všechny další soubory DGN, které chcete převést. Gratulujeme! Úspěšně jste exportovali soubory DGN do formátu AutoCAD v PDF pomocí Aspose.CAD for Java.

## Závěr

tomto tutoriálu jsme prozkoumali, jak využít Aspose.CAD pro Java k vylepšení možností zpracování souborů CAD vaší aplikace. Pomocí snadno pochopitelných kroků a příkladů kódu můžete nyní bez problémů exportovat soubory DGN do formátu AutoCAD ve formátu PDF.

## FAQ

### Q1: Je Aspose.CAD kompatibilní se všemi formáty souborů CAD?

A1: Ano, Aspose.CAD podporuje širokou škálu CAD formátů, což zajišťuje všestrannost při manipulaci s různými typy souborů.

### Q2: Mohu přizpůsobit nastavení exportu PDF?

A2: Rozhodně. Jak je uvedeno ve výukovém programu, můžete upravit možnosti, jako jsou rozměry a rozvržení stránky, aby vyhovovaly vašim požadavkům.

### Q3: Kde najdu další podporu nebo pomoc?

 A3: Navštivte[Fórum Aspose.CAD](https://forum.aspose.com/c/cad/19) za podporu komunity a diskuze.

### Q4: Je k dispozici bezplatná zkušební verze?

 A4: Ano, máte přístup k bezplatné zkušební verzi[tady](https://releases.aspose.com/).

### Q5: Jak mohu získat dočasnou licenci?

 A5: Získejte dočasnou licenci[tady](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
