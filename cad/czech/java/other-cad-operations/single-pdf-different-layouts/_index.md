---
title: Vytváření dynamických PDF pomocí Aspose.CAD pro Java
linktitle: Jeden PDF s různými rozvrženími
second_title: Aspose.CAD Java API
description: Vytvářejte úžasné soubory PDF s různými rozvrženími z výkresů CAD pomocí Aspose.CAD pro Java. Snadná integrace a výkonné funkce pro vývojáře Java.
type: docs
weight: 16
url: /cs/java/other-cad-operations/single-pdf-different-layouts/
---
## Úvod

Vítejte ve světě Aspose.CAD for Java, výkonné knihovny, která umožňuje vývojářům bez námahy manipulovat s CAD výkresy. V tomto tutoriálu se ponoříme do vytváření jednotlivých PDF s různými rozvrženími pomocí Aspose.CAD pro Java. Ať už jste zkušený vývojář nebo teprve začínáte, tento podrobný průvodce vás provede celým procesem.

## Předpoklady

Než se vydáme na tuto cestu, ujistěte se, že máte splněny následující předpoklady:
- Prostředí Java: Ujistěte se, že máte na svém počítači nainstalovanou Javu.
-  Knihovna Aspose.CAD: Stáhněte a nainstalujte knihovnu Aspose.CAD pro Javu z[odkaz ke stažení](https://releases.aspose.com/cad/java/).
- Adresář dokumentů: Nastavte adresář pro své výkresy DWG.

## Importujte balíčky

Do svého projektu Java naimportujte potřebné balíčky:

```java
import com.aspose.cad.Image;
import com.aspose.cad.SizeF;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.VectorRasterizationOptions;
```

## Krok 1: Načtěte výkres CAD

 Začněte načtením výkresu CAD do a`CadImage` objekt:

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
CadImage cadImage = (CadImage)Image.load(dataDir + "City skyway map.dwg");
```

## Krok 2: Nakonfigurujte možnosti rastrování

Nastavte možnosti rastrování pro obrázek CAD:

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1000);
rasterizationOptions.setPageHeight(1000);
```

## Krok 3: Přizpůsobte velikosti stránky rozvržení

Definujte vlastní velikosti pro několik rozvržení ve výkresu CAD:

```java
rasterizationOptions.getLayoutPageSizes().addItem("ANSI C Plot", new SizeF(500, 1000));
rasterizationOptions.getLayoutPageSizes().addItem("8.5 x 11 Plot", new SizeF(1000, 100));
```

## Krok 4: Nastavte možnosti PDF

Nakonfigurujte možnosti PDF se začleněním nastavení rastrování:

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Krok 5: Uložit jako PDF

Uložte zpracovaný obrázek CAD jako PDF:

```java
cadImage.save(dataDir + "singlePDF_out.pdf", pdfOptions);
```

Gratulujeme! Úspěšně jste vytvořili jeden PDF s různými rozvrženími pomocí Aspose.CAD for Java.

## Závěr

V tomto tutoriálu jsme prozkoumali bezproblémovou integraci Aspose.CAD pro Java pro generování PDF s různými rozvrženími z CAD výkresů. Flexibilita a robustní funkce knihovny z ní činí ideální volbu pro manipulační úlohy CAD.

## FAQ

### Q1: Mohu používat Aspose.CAD for Java s jinými Java knihovnami?

Odpověď 1: Ano, Aspose.CAD for Java je navržen tak, aby se hladce integroval s jinými knihovnami Java a poskytoval rozsáhlé funkce.

### Q2: Je k dispozici zkušební verze?

 A2: Rozhodně! Máte přístup k bezplatné zkušební verzi[tady](https://releases.aspose.com/).

### Q3: Kde najdu další podporu?

 A3: Navštivte[Fórum Aspose.CAD](https://forum.aspose.com/c/cad/19) za podporu komunity a diskuze.

### Q4: Jak získám dočasnou licenci?

 A4: Můžete získat dočasnou licenci[tady](https://purchase.aspose.com/temporary-license/).

### Q5: Kde mohu zakoupit plnou verzi?

A5: Kupte si plnou verzi Aspose.CAD pro Java[tady](https://purchase.aspose.com/buy).