---
title: DGN do PDF Průvodce převodem - Aspose.CAD pro Javu
linktitle: Podpora pro DGN V7
second_title: Aspose.CAD Java API
description: Bez námahy převádějte soubory DGN do PDF pomocí Aspose.CAD pro Java. Postupujte podle našeho podrobného průvodce pro bezproblémovou integraci a efektivní pracovní postup.
weight: 11
url: /cs/java/other-cad-operations/support-for-dgn-v7/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DGN do PDF Průvodce převodem - Aspose.CAD pro Javu

## Úvod

V dynamickém světě CAD (Computer-Aided Design) je efektivní převod souborů DGN (Design) do PDF (Portable Document Format) zásadním požadavkem. Aspose.CAD for Java se ukazuje jako výkonné řešení, které nabízí bezproblémovou integraci a robustní funkce. Cílem tohoto podrobného průvodce je provést vás procesem exportu souborů DGN do PDF pomocí Aspose.CAD for Java a zajistit hladký a efektivní pracovní postup.

## Předpoklady

Než se pustíte do výukového programu, ujistěte se, že máte splněny následující předpoklady:
-  Aspose.CAD for Java Library: Stáhněte a nainstalujte knihovnu z[Aspose.CAD for Java Download page](https://releases.aspose.com/cad/java/).
- Vývojové prostředí Java: Ujistěte se, že máte na svém počítači nastavené vývojové prostředí Java.

## Importujte balíčky

Začněte importem potřebných balíčků do vašeho projektu Java:

## Krok 1: Importujte potřebné balíčky

Ve svém projektu Java importujte požadované balíčky pro Aspose.CAD for Java.
```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadRasterizationOptions;
import com.aspose.cad.fileformats.cad.cadobjects.DgnImage;
import com.aspose.cad.imageoptions.PdfOptions;
import java.awt.Color;
```

## Krok 2: Nastavte cesty k souboru

Definujte cesty pro váš vstupní soubor DGN a výstupní soubor PDF.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "Nikon_D90_Camera.dgn";
String outFile  = dataDir + "Nikon_D90_Camera.pdf";
```

## Krok 3: Načtěte obrázek DGN

Načtěte obrázek DGN pomocí knihovny Aspose.CAD.

```java
DgnImage objImage = (DgnImage)Image.load(fileName);
```

## Krok 4: Nakonfigurujte možnosti exportu PDF

Nastavte možnosti pro export do PDF, včetně rozměrů stránky, automatického měřítka rozvržení, barvy pozadí a konkrétních rozvržení k exportu.

```java
PdfOptions options = new PdfOptions();
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
vectorOptions.setAutomaticLayoutsScaling(true);
vectorOptions.setBackgroundColor(Color.getBlack());
vectorOptions.setLayouts(new String[] { "1", "2", "3", "9" }); //exportovat pouze 4 (1,2,3 a 9) pohledů
options.setVectorRasterizationOptions(vectorOptions);
```

## Krok 5: Uložte soubor PDF

Uložte obrázek DGN jako soubor PDF se zadanými možnostmi.

```java
objImage.save(outFile, options);
```

Opakujte tyto kroky pro různé soubory DGN a podle potřeby upravte cesty k souborům a možnosti.

## Závěr

S Aspose.CAD for Java se převod souborů DGN do PDF stává přímočarým procesem. Tato příručka vás vybaví znalostmi pro bezproblémovou integraci knihovny do vašich projektů Java a usnadní efektivní převod souborů CAD.

## FAQ

### Q1: Mohu použít Aspose.CAD for Java s jinými formáty souborů CAD?

Odpověď 1: Ano, Aspose.CAD podporuje různé formáty CAD a poskytuje všestranné funkce nad rámec převodu DGN do PDF.

### Q2: Je k dispozici dočasná licence pro Aspose.CAD pro Java?

 A2: Ano, můžete získat dočasnou licenci[tady](https://purchase.aspose.com/temporary-license/) pro testovací účely.

### Q3: Jak mohu vyhledat podporu nebo se zeptat na Aspose.CAD pro Java?

 A3: Navštivte[Fórum Aspose.CAD](https://forum.aspose.com/c/cad/19)spojit se s komunitou a vyhledat pomoc.

### Q4: Jaká rozvržení mohu exportovat při převodu DGN do PDF?

 A4: Můžete určit rozvržení k exportu přizpůsobením`setLayouts` pole v kódu.

### Q5: Kde najdu komplexní dokumentaci k Aspose.CAD for Java?

 A5: Viz[Aspose.CAD pro dokumentaci Java](https://reference.aspose.com/cad/java/) pro podrobné informace.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
