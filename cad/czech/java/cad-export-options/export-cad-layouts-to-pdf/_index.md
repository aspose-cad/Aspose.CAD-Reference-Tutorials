---
title: Export CAD rozložení do PDF pomocí Aspose.CAD pro Java
linktitle: Export CAD rozložení do PDF
second_title: Aspose.CAD Java API
description: Prozkoumejte Aspose.CAD for Java a snadno exportujte rozvržení CAD do PDF. Efektivní, spolehlivý a přívětivý pro vývojáře.
weight: 11
url: /cs/java/cad-export-options/export-cad-layouts-to-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export CAD rozložení do PDF pomocí Aspose.CAD pro Java

## Úvod

V neustále se vyvíjející oblasti počítačově podporovaného navrhování (CAD) vyniká Aspose.CAD for Java jako výkonný nástroj pro manipulaci a konverzi souborů CAD. V tomto tutoriálu vás provedeme procesem exportu rozvržení CAD do PDF pomocí Aspose.CAD for Java. Ať už jste zkušený vývojář nebo se jen ponoříte do světa CAD, tento podrobný průvodce vám pomůže využít plný potenciál této všestranné Java knihovny.

## Předpoklady

Než se pustíme do výukového programu, ujistěte se, že máte splněny následující předpoklady:

-  Aspose.CAD for Java: Ujistěte se, že máte nainstalovanou knihovnu. Můžete si jej stáhnout z webu Aspose[tady](https://releases.aspose.com/cad/java/).

- Vývojové prostředí Java: Ujistěte se, že máte na svém počítači nastavené vývojové prostředí Java.

Nyní, když máte vše nastaveno, můžeme začít s tutoriálem.

## Importovat jmenné prostory

Ve svém kódu Java začněte importováním potřebných jmenných prostorů. Tyto importy poskytují přístup ke třídám a metodám potřebným pro práci s Aspose.CAD for Java.

```java
import com.aspose.cad.Image;
import com.aspose.cad.InterpolationMode;
import com.aspose.cad.SmoothingMode;
import com.aspose.cad.TextRenderingHint;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

## Krok 1: Načtěte soubor CAD

 Začněte načtením souboru CAD do aplikace Java pomocí souboru`Image.load` metoda. Nahradit`"conic_pyramid.dxf"` s cestou k vašemu CAD souboru.

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

## Krok 2: Nastavte možnosti rastrování

 Vytvořte instanci`CadRasterizationOptions` definovat, jak mají být entity CAD rastrovány. Upravte parametry, jako je šířka stránky, výška stránky a měřítko rozvržení, podle vašich požadavků.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(false);
rasterizationOptions.setContentAsBitmap(true);
rasterizationOptions.setLayouts(new String[]{"Model"});
```

## Krok 3: Nastavte možnosti PDF

 Vytvořte instanci`PdfOptions` a spojte jej s možnostmi rasterizace. Dále nastavte možnosti grafiky pro export PDF, jako je režim vyhlazování, nápověda k vykreslení textu a režim interpolace.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
rasterizationOptions.getGraphicsOptions().setSmoothingMode(SmoothingMode.HighQuality);
rasterizationOptions.getGraphicsOptions().setTextRenderingHint(TextRenderingHint.AntiAliasGridFit);
rasterizationOptions.getGraphicsOptions().setInterpolationMode(InterpolationMode.HighQualityBicubic);
```

## Krok 4: Export do PDF

 Nakonec exportujte rozvržení CAD do souboru PDF pomocí`save` metoda`cadImage` objekt.

```java
cadImage.save(dataDir + "CADLayoutsToPDF_out_.pdf", pdfOptions);
```

Gratulujeme! Úspěšně jste exportovali rozvržení CAD do PDF pomocí Aspose.CAD for Java. Neváhejte a prozkoumejte další funkce a funkce nabízené Aspose.CAD, abyste zlepšili své zkušenosti s manipulací se soubory CAD.

## Závěr

V tomto tutoriálu jsme prošli procesem exportu CAD rozvržení do PDF pomocí Aspose.CAD for Java. Díky svým robustním funkcím a snadno použitelnému rozhraní API umožňuje Aspose.CAD vývojářům efektivně pracovat se soubory CAD v jejich aplikacích Java.

## FAQ

### Q1: Mohu použít Aspose.CAD for Java s jinými formáty souborů CAD?

 Odpověď 1: Ano, Aspose.CAD podporuje různé formáty CAD, včetně DWG, DXF, DWF a dalších. Zkontrolujte dokumentaci[tady](https://reference.aspose.com/cad/java/) pro úplný seznam.

### Q2: Je k dispozici bezplatná zkušební verze pro Aspose.CAD pro Javu?

 Odpověď 2: Ano, funkce Aspose.CAD můžete prozkoumat pomocí bezplatné zkušební verze[tady](https://releases.aspose.com/).

### Q3: Jak mohu získat podporu pro Aspose.CAD pro Java?

 Odpověď 3: Navštivte fórum Aspose.CAD[tady](https://forum.aspose.com/c/cad/19) za podporu komunity. Pro prémiovou podporu zvažte zakoupení licence[tady](https://purchase.aspose.com/buy).

### Q4: Jaký je rozdíl mezi automatickým a manuálním měřítkem rozvržení?

Odpověď 4: Automatické měřítko rozvržení upravuje velikost rozvržení na základě zadaných rozměrů stránky, zatímco ruční změna měřítka umožňuje nastavit vlastní hodnoty měřítka.

### Q5: Mohu přizpůsobit vzhled exportovaných souborů PDF?

Odpověď 5: Ano, můžete upravit možnosti grafiky v kódu a řídit tak kvalitu a vzhled exportovaného PDF.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
