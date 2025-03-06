---
title: Konverze Java DGN do JPEG pomocí výukového programu Aspose.CAD
linktitle: Export DGN ve formátu AutoCAD do formátu rastrového obrázku
second_title: Aspose.CAD Java API
description: Naučte se exportovat soubory DGN do obrázků JPEG v Javě pomocí Aspose.CAD. Tento návod krok za krokem vás bez námahy provede celým procesem.
weight: 13
url: /cs/java/dgn-export-options/exporting-dgn-to-raster-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konverze Java DGN do JPEG pomocí výukového programu Aspose.CAD

## Úvod

Vítejte v tomto komplexním tutoriálu o exportu souborů DGN (Design) do formátu rastrových obrázků pomocí Aspose.CAD pro Java. Aspose.CAD je výkonná knihovna, která umožňuje vývojářům v Javě bezproblémově pracovat se soubory CAD. V tomto tutoriálu vás provedeme procesem převodu souborů DGN na obrázky JPEG a poskytneme vám podrobné pokyny a příklady kódu.

## Předpoklady

Než se pustíte do výukového programu, ujistěte se, že máte splněny následující předpoklady:
1.  Knihovna Aspose.CAD: Ujistěte se, že máte nainstalovanou knihovnu Aspose.CAD for Java. Můžete si jej stáhnout[tady](https://releases.aspose.com/cad/java/).
2. Java Development Kit (JDK): Ujistěte se, že máte na svém počítači nainstalovanou Javu.
3. Integrované vývojové prostředí (IDE): Použijte IDE kompatibilní s Java, jako je IntelliJ nebo Eclipse.

## Importujte balíčky

Ve svém projektu Java naimportujte potřebné balíčky pro Aspose.CAD. Přidejte do kódu následující řádky:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
```

## Krok 1: Načtěte soubor DGN

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
DgnImage dgnImage = (DgnImage) Image.load(dataDir + "Nikon_D90_Camera.dgn");
```

## Krok 2: Vytvořte objekt JpegOptions

```java
ImageOptionsBase options = new JpegOptions();
```

## Krok 3: Přiřaďte možnosti rastrování

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(600);
vectorOptions.setPageHeight(400);
vectorOptions.setNoScaling(true);
vectorOptions.setAutomaticLayoutsScaling(false);
options.setVectorRasterizationOptions(vectorOptions);
```

## Krok 4: Uložte převedený obrázek

```java
OutputStream outStream = new FileOutputStream(dataDir + "ExportDGNToRasterImage_Out.jpg");
dgnImage.save(outStream, options);
```

Opakujte tyto kroky pro vaše konkrétní soubory DGN a odpovídajícím způsobem upravte cesty k souborům.

## Závěr

Gratulujeme! Úspěšně jste se naučili, jak exportovat soubory DGN do formátu rastrových obrázků pomocí Aspose.CAD for Java. Tento tutoriál vás vybavil znalostmi pro začlenění této funkce do vašich aplikací Java.

## FAQ

### Q1: Mohu použít Aspose.CAD for Java s jinými formáty souborů CAD?

Odpověď 1: Ano, Aspose.CAD podporuje různé formáty CAD a poskytuje všestranné řešení pro vývojáře v jazyce Java.

### Q2: Je k dispozici bezplatná zkušební verze pro Aspose.CAD pro Javu?

 A2: Ano, máte přístup k bezplatné zkušební verzi[tady](https://releases.aspose.com/).

### Q3: Kde najdu dokumentaci k Aspose.CAD for Java?

 A3: Viz dokumentace[tady](https://reference.aspose.com/cad/java/).

### Q4: Jak mohu získat podporu pro Aspose.CAD pro Java?

 A4: Navštivte fórum podpory[tady](https://forum.aspose.com/c/cad/19).

### Q5: Kde si mohu zakoupit licenci na Aspose.CAD for Java?

 A5: Můžete si koupit licenci[tady](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
